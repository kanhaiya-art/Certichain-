# CertiChain

A mobile-friendly Streamlit demo for certificate file verification and hash-linked records.

## Features
- Dashboard with sample certificates and ledger status
- Upload a PDF/image/text file and compare its SHA-256 fingerprint
- Generate and register fictional demo certificates
- Explore linked ledger records and export JSON
- Safe tampering simulation

## Deploy from your phone
1. Create a **public** GitHub repository named `CertiChain`.
2. Upload the project files and folders (not the ZIP itself).
3. Open Streamlit Community Cloud and choose **Create app**.
4. Select your repository, branch `main`, and main file `app.py`.
5. Deploy. Keep `requirements.txt`, `certichain_core.py`, `.streamlit/`, and `samples/` in the repository.

## Run locally
```bash
python -m pip install -r requirements.txt
python -m streamlit run app.py
```

## Demo
1. Download one of the sample PDFs on the dashboard.
2. Open **Verify certificate** and upload the unchanged PDF.
3. Generate a fictional certificate, download it, then verify it.
4. Open **Ledger explorer** and run the tampering simulation.

## Important limitations
This is an educational prototype, not a decentralized blockchain. SHA-256 matching confirms exact file-byte equality with a registered record; it does not authenticate the issuer. The ledger is stored in a local JSON file and may reset on cloud restarts. Do not upload private certificates.
