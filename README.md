# 📦 Repositório de Manifestos - Projeto Hello-App (GitOps)

![Gerenciado por](https://img.shields.io/badge/Gerenciado%20por-GitHub%20Actions-2671E5?style=for-the-badge&logo=githubactions)
![Princípio](https://img.shields.io/badge/Princípio-GitOps-F4866D?style=for-the-badge&logo=argo)
![Kubernetes](https://img.shields.io/badge/kubernetes-%23326ce5.svg?style=for-the-badge&logo=kubernetes&logoColor=white)
![YAML](https://img.shields.io/badge/YAML-121011?style=for-the-badge&logo=yaml&logoColor=white)

---

## 🎯 Propósito deste Repositório

Este repositório armazena os manifestos Kubernetes (`deployment.yaml` e `service.yaml`) para a aplicação `hello-app`.

Ele atua como a **"fonte da verdade" (Source of Truth)** para o ArgoCD, implementando o princípio de GitOps. O ArgoCD monitora este repositório e garante que o estado do cluster Kubernetes seja idêntico ao estado definido nos arquivos deste repositório.

---

## ⚠️ Gerenciamento Automatizado

**Este repositório é gerenciado automaticamente pela pipeline de CI/CD.**

Os arquivos aqui, especificamente a **tag da imagem** no `k8s/deployment.yaml`, são atualizados por um workflow de GitHub Actions que roda no repositório principal da aplicação.

Qualquer alteração manual na tag da imagem será sobrescrita pelo próximo build bem-sucedido da pipeline.

* **Repositório da Aplicação (CI/CD):** [https://github.com/Luisdevux/hello-app](https://github.com/Luisdevux/hello-app)

---

## 🏗️ Estrutura

```bash
📦 hello-manifests
┗ 📂 k8s
  ┣ 📜 deployment.yaml
  ┗ 📜 service.yaml
```

---