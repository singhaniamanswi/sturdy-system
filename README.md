# sturdy-system
import subprocess

def run_command(command):
    """Runs a git command"""
    try:
        subprocess.run(command,check=True)except subprocess.CalledProcessError:
        print("❌ Error while running command:",command)def init_repo():
    print("📦 Initializing Git repository...")run_command(["git","init"])def add_files():
    print("➕ Adding all files...")run_command(["git","add","."])def commit_changes(message):
    print("✅ Committing changes...")run_command(["git","commit","-m",message])def main():
    print("🔹 Git Automation Program 🔹")commit_message=input("Enter commit message: ")init_repo()add_files()commit_changes(commit_message)print("🎉 Git operations completed successfully!")if __name__=="__main__":
    main()
