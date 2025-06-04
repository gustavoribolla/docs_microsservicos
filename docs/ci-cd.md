# CI/CD

A entrega contínua da aplicação foi automatizada utilizando o Jenkins, uma das ferramentas de integração contínua mais consolidadas do mercado.

## Jenkins

O Jenkins é uma plataforma de automação open-source amplamente utilizada para CI/CD. Ele permite a orquestração de pipelines que automatizam desde os testes até o deploy em produção.

![Jenkins](images/jenkins1.png)

## Pipeline de Deploy

Na nossa solução, o Jenkins foi configurado para realizar o `kubectl apply` dos manifests diretamente no cluster gerenciado pela AWS através do EKS.

### Etapas principais do pipeline:

1. **Checkout do repositório** com os manifests e a aplicação.
2. **Build da imagem** da aplicação e push para o repositório.
3. **Deploy automatizado** via `kubectl apply -f` dos arquivos YAML na AWS.

Esse processo garante que qualquer mudança realizada no código seja rapidamente propagada para o ambiente em nuvem, assegurando confiabilidade e agilidade no ciclo de vida da aplicação.

---

*Autores: Gustavo Colombi Ribolla e Rafaela Afférri de Oliveira*