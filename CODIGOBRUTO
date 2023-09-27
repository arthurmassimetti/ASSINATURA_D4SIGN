from selenium import webdriver
from selenium.webdriver.common.by import By
import os
import time
from selenium.webdriver.support.wait import WebDriverWait
from selenium.common.exceptions import NoSuchElementException
from selenium.webdriver.common.action_chains import ActionChains
import pyautogui

# Diretório onde estão os arquivos PDF
pasta_pdfs = "C:/Users/ProOcupacional/Downloads/pdfassinar"


while True:
    try:
        for nome_arquivo in os.listdir(pasta_pdfs):
            if nome_arquivo.endswith('.pdf'):
                # Diretório onde estão os arquivos PDF
                pasta_pdfs = "C:/Users/ProOcupacional/Downloads/pdfassinar"

                # URL do site onde você deseja fazer o upload
                url_site = 'https://secure.d4sign.com.br/login.html'

                # Inicialize o driver do Selenium (certifique-se de ter o WebDriver adequado instalado e configurado)
                driver = webdriver.Chrome()  # Você precisa ter o ChromeDriver instalado para usar o Chrome

                # Abra a página da web
                driver.get(url_site)
                driver.maximize_window()

                # Encontre os elementos na página de login
                campo_email = driver.find_element(By.XPATH, '/html/body/div/div/div/div/div/div[1]/form/div[2]/input')
                campo_senha = driver.find_element(By.XPATH,
                                                  '/html/body/div/div/div/div/div/div[1]/form/div[3]/div[2]/div[1]/input[1]')
                botao_logar = driver.find_element(By.XPATH, '/html/body/div/div/div/div/div/div[1]/form/div[3]/button')

                # Faça login
                campo_email.send_keys("EMAIL PARA ACESSO")
                campo_senha.send_keys("SENHA PARA ACESSO")
                botao_logar.click()
                wait = WebDriverWait(driver, 30)
                time.sleep(1)

                # Loop através dos arquivos no diretório
                caminho_arquivo = os.path.join(pasta_pdfs, nome_arquivo)
                cliquearqueivoenviar = driver.find_element(By.XPATH,
                                                           "/html/body/div[2]/div/div[2]/div[2]/div[2]/div/div[3]/div/div/a/p[2]").click()
                time.sleep(2)
                pcmsoclique = driver.find_element(By.XPATH,
                                                  "/html/body/div[7]/div[2]/div/div[2]/div[1]/div/form/select/option[2]").click()
                time.sleep(1)

                # Localize o elemento de entrada de arquivo (input type="file") na página
                elemento_input_arquivo = driver.find_element(By.XPATH,
                                                             '/html/body/div[7]/div[2]/div/div[2]/div[1]/div/form/div/span/input')

                # Envie o caminho do arquivo para o elemento de entrada de arquivo
                elemento_input_arquivo.send_keys(caminho_arquivo)

                # Aguarde o upload ser concluído (você pode ajustar o tempo de espera conforme necessário)
                time.sleep(6)  # Aguarda 5 segundos (ajuste conforme necessário)

                wait = WebDriverWait(driver, 30)
                time.sleep(9)

                pyautogui.click(713, 800)
                time.sleep(3)
                pyautogui.click(713, 800)
                time.sleep(2)
                contatos = driver.find_element(By.XPATH, "//a[contains(text(), 'Contatos')]").click()
                time.sleep(2)
                pyautogui.click(613, 446)
                time.sleep(3)
                confirmaassina = driver.find_element(By.XPATH,
                                                     "/html/body/div[5]/div[2]/div/div[2]/div[1]/div[4]/div[1]/button").click()
                time.sleep(1)
                fechaassina = driver.find_element(By.XPATH, "/html/body/div[5]/div[2]/div/div[1]/button").click()
                wait = WebDriverWait(driver, 30)
                elemento = driver.find_element(By.XPATH,
                                               '/html/body/div[3]/div/div[2]/div/div[2]/div[2]/div[4]/div/div/canvas[15]')
                # Role a tela até o elemento visível
                actions = ActionChains(driver)
                actions.move_to_element(elemento)
                actions.perform()
                pyautogui.click(1215, 484)
                time.sleep(1)
                enviarassinatura = driver.find_element(By.XPATH,
                                                       "/html/body/div[3]/div/div[2]/div/div[1]/div/div/div/div[5]/div/div[4]/button").click()
                time.sleep(1)
                enviarparaassinatura = driver.find_element(By.XPATH,
                                                           "/html/body/div[5]/div[2]/div/div[2]/div[1]/form[1]/input[5]").click()
                os.remove(caminho_arquivo)
                driver.close()


    except:
        print("ERRO TRY FULL CODE")
        continue
