- 👋 Hi, I’m @Marcoslima21
- 👀 I’m interested in ...
- 🌱 I’m currently learning ...
- 💞️ I’m looking to collaborate on ...
- 📫 How to reach me ...

<!---
Marcoslima21/Marcoslima21 is a ✨ special ✨ repository because its `README.md` (this file) appears on your GitHub profile.
You can click the Preview link to take a look at your changes.
--->
git clone https://seu-repositorio.git
cd seu-repositorio
/seu-repositorio
├── /src
│   ├── main.py
│   └── finance_manager.py
├── /tests
│   └── test_finance_manager.py
├── README.md
└── requirements.txt
class FinanceManager:
    def __init__(self):
        self.balance = 0

    def deposit(self, amount):
        self.balance += amount
        return self.balance

    def withdraw(self, amount):
        if amount <= self.balance:
            self.balance -= amount
            return self.balance
        else:
            return "Saldo insuficiente"

    def get_balance(self):
        return self.balance
import unittest
from finance_manager import FinanceManager

class TestFinanceManager(unittest.TestCase):
    def test_deposit(self):
        manager = FinanceManager()
        self.assertEqual(manager.deposit(100), 100)

    def test_withdraw_sufficient_funds(self):
        manager = FinanceManager()
        manager.deposit(100)
        self.assertEqual(manager.withdraw(50), 50)

    def test_withdraw_insufficient_funds(self):
        manager = FinanceManager()
        self.assertEqual(manager.withdraw(50), "Saldo insuficiente")

if __name__ == '__main__':
    unittest.main()
    # requirements.txt
git add .
git commit -m "Adicionar estrutura inicial do projeto"
git push origin master
