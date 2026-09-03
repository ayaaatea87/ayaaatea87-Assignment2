# SSH

**SSH (Secure Shell)**

هو بروتوكول بيستخدم لعمل اتصال آمن بين جهازك و GitHub أو أي Remote Server.

في GitHub بنستخدم SSH علشان نقدر نعمل **Authentication** من غير ما نكتب username/password كل مرة.

### SSH Key

الـSSH بيعتمد على اتنين Keys:

* **Public Key** → بنضيفه على GitHub.
* **Private Key** → بيفضل عندنا على الجهاز وممنوع نشاركه مع أي حد.

### Generate SSH Key

```bash
ssh-keygen -t ed25519 -C "your_email@example.com"
```

الأمر ده بيعمل SSH Key جديد.

### Check SSH Connection

```bash
ssh -T git@github.com
```

بنستخدمه علشان نتأكد إن الـSSH connection بين جهازنا وGitHub شغال.

### Clone Using SSH

```bash
git clone git@github.com:username/repository.git
```

بدل ما نستخدم HTTPS، نقدر نستخدم SSH URL في الـclone.