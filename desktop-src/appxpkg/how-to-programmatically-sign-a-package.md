---
title: Programm gesteuertes Signieren eines App-Pakets (C++)
description: Erfahren Sie, wie Sie ein App-Paket mithilfe der SignerSignEx2-Funktion signieren.
ms.assetid: 1183D665-83C9-4BE7-9C8D-834484B8C57F
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0310ba2a934a6986809329a12afa8ee20b2f6591
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "103724681"
---
# <a name="how-to-programmatically-sign-an-app-package-c"></a>Programm gesteuertes Signieren eines App-Pakets (C++)

Erfahren Sie, wie Sie ein App-Paket mithilfe der [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) -Funktion signieren.

Wenn Sie Windows-App-Pakete mithilfe der [Paket-API](interfaces.md)Programm gesteuert erstellen möchten, müssen Sie die APP-Pakete auch signieren, bevor Sie bereitgestellt werden können. Die Paket-API bietet keine spezielle Methode zum Signieren von App-Paketen. Verwenden Sie stattdessen die standardmäßigen [Kryptografiefunktionen](/windows/desktop/SecCrypto/cryptography-functions) zum Signieren Ihrer APP-Pakete.

## <a name="what-you-need-to-know"></a>Was Sie wissen müssen

### <a name="technologies"></a>Technologien

-   [Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
-   [Verpacken, Bereitstellung und Abfrage von Windows-apps](appx-portal.md)
-   [Kryptografiefunktionen](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a>Voraussetzungen

-   Sie benötigen eine gepackte Windows-app. Informationen zum Erstellen eines App-Pakets finden [Sie unter Erstellen eines App-Pakets](how-to-create-a-package.md).
-   Sie benötigen ein Code Signaturzertifikat, das zum Signieren des App-Pakets geeignet ist. Informationen zum Erstellen eines Test Code Signatur Zertifikats finden Sie unter [Erstellen eines App-Paket-Signatur Zertifikats](how-to-create-a-package-signing-certificate.md). Laden Sie dieses Signaturzertifikat in eine [**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Struktur. Sie können z. b. [**pfximportcertstore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) und [**certfindcertifikateinstore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) verwenden, um ein Signaturzertifikat zu laden.
-   Mit Windows 8 wird die [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) -Funktion eingeführt. Verwenden Sie **SignerSignEx2** , wenn Sie Windows-App-Pakete signieren.

## <a name="instructions"></a>Anweisungen

### <a name="step-1-define-the-required-structures-for-signersignex2"></a>Schritt 1: Definieren der erforderlichen Strukturen für SignerSignEx2

Zusätzlich zum Wincrypt. h-Header hängt die [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) -Funktion von vielen Strukturen ab, die in keiner SDK-Header Datei definiert sind. Um **SignerSignEx2** zu verwenden, müssen Sie diese Strukturen selbst definieren:


```C++
typedef struct _SIGNER_FILE_INFO
{
    DWORD cbSize;
    LPCWSTR pwszFileName;
    HANDLE hFile;
}SIGNER_FILE_INFO, *PSIGNER_FILE_INFO;
 
typedef struct _SIGNER_BLOB_INFO
{
    DWORD cbSize;
    GUID *pGuidSubject;
    DWORD cbBlob;
    BYTE *pbBlob;
    LPCWSTR pwszDisplayName;
}SIGNER_BLOB_INFO, *PSIGNER_BLOB_INFO;
 
typedef struct _SIGNER_SUBJECT_INFO
{
    DWORD cbSize;
    DWORD *pdwIndex;
    DWORD dwSubjectChoice;
    union
    {
        SIGNER_FILE_INFO *pSignerFileInfo;
        SIGNER_BLOB_INFO *pSignerBlobInfo;
    };
}SIGNER_SUBJECT_INFO, *PSIGNER_SUBJECT_INFO;
 
// dwSubjectChoice should be one of the following:
#define SIGNER_SUBJECT_FILE    0x01
#define SIGNER_SUBJECT_BLOB    0x02
 
typedef struct _SIGNER_ATTR_AUTHCODE
{
    DWORD cbSize;
    BOOL fCommercial;
    BOOL fIndividual;
    LPCWSTR pwszName;
    LPCWSTR pwszInfo;
}SIGNER_ATTR_AUTHCODE, *PSIGNER_ATTR_AUTHCODE;
 
typedef struct _SIGNER_SIGNATURE_INFO
{
    DWORD cbSize;
    ALG_ID algidHash;
    DWORD dwAttrChoice;
    union
    {
        SIGNER_ATTR_AUTHCODE *pAttrAuthcode;
    };
    PCRYPT_ATTRIBUTES psAuthenticated;
    PCRYPT_ATTRIBUTES psUnauthenticated;
}SIGNER_SIGNATURE_INFO, *PSIGNER_SIGNATURE_INFO;
 
// dwAttrChoice should be one of the following:
#define SIGNER_NO_ATTR          0x00
#define SIGNER_AUTHCODE_ATTR    0x01
 
typedef struct _SIGNER_PROVIDER_INFO
{
    DWORD cbSize;
    LPCWSTR pwszProviderName;
    DWORD dwProviderType;
    DWORD dwKeySpec;
    DWORD dwPvkChoice;
    union
    {
        LPWSTR pwszPvkFileName;
        LPWSTR pwszKeyContainer;
    };
}SIGNER_PROVIDER_INFO, *PSIGNER_PROVIDER_INFO;
 
//dwPvkChoice should be one of the following:
#define PVK_TYPE_FILE_NAME       0x01
#define PVK_TYPE_KEYCONTAINER    0x02
 
typedef struct _SIGNER_SPC_CHAIN_INFO
{
    DWORD cbSize;
    LPCWSTR pwszSpcFile;
    DWORD dwCertPolicy; 
    HCERTSTORE hCertStore;
}SIGNER_SPC_CHAIN_INFO, *PSIGNER_SPC_CHAIN_INFO;
 
typedef struct _SIGNER_CERT_STORE_INFO
{
    DWORD cbSize;
    PCCERT_CONTEXT pSigningCert;
    DWORD dwCertPolicy;
    HCERTSTORE hCertStore;
}SIGNER_CERT_STORE_INFO, *PSIGNER_CERT_STORE_INFO;
 
//dwCertPolicy can be a combination of the following flags:
#define SIGNER_CERT_POLICY_STORE            0x01
#define SIGNER_CERT_POLICY_CHAIN            0x02
#define SIGNER_CERT_POLICY_SPC              0x04
#define SIGNER_CERT_POLICY_CHAIN_NO_ROOT    0x08
 
typedef struct _SIGNER_CERT
{
    DWORD cbSize;
    DWORD dwCertChoice;
    union
    {
        LPCWSTR pwszSpcFile;
        SIGNER_CERT_STORE_INFO *pCertStoreInfo;
        SIGNER_SPC_CHAIN_INFO *pSpcChainInfo;
    };
    HWND hwnd;
}SIGNER_CERT, *PSIGNER_CERT;
 
//dwCertChoice should be one of the following
#define SIGNER_CERT_SPC_FILE     0x01
#define SIGNER_CERT_STORE        0x02
#define SIGNER_CERT_SPC_CHAIN    0x03
 
typedef struct _SIGNER_CONTEXT
{
    DWORD cbSize;
    DWORD cbBlob;
    BYTE *pbBlob;
}SIGNER_CONTEXT, *PSIGNER_CONTEXT;
 
typedef struct _SIGNER_SIGN_EX2_PARAMS
{
    DWORD dwFlags;
    PSIGNER_SUBJECT_INFO pSubjectInfo;
    PSIGNER_CERT pSigningCert;
    PSIGNER_SIGNATURE_INFO pSignatureInfo;
    PSIGNER_PROVIDER_INFO pProviderInfo;
    DWORD dwTimestampFlags;
    PCSTR pszAlgorithmOid;
    PCWSTR pwszTimestampURL;
    PCRYPT_ATTRIBUTES pCryptAttrs;
    PVOID pSipData;
    PSIGNER_CONTEXT *pSignerContext;
    PVOID pCryptoPolicy;
    PVOID pReserved;
} SIGNER_SIGN_EX2_PARAMS, *PSIGNER_SIGN_EX2_PARAMS;
 
typedef struct _APPX_SIP_CLIENT_DATA
{
    PSIGNER_SIGN_EX2_PARAMS pSignerParams;
    IUnknown* pAppxSipState;
} APPX_SIP_CLIENT_DATA, *PAPPX_SIP_CLIENT_DATA;
```



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a>Schritt 2: SignerSignEx2 zum Signieren des App-Pakets anrufen

Nachdem Sie die im vorherigen Schritt angegebenen erforderlichen Strukturen definiert haben, können Sie eine beliebige der Optionen verwenden, die in der [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) -Funktion verfügbar sind, um ein App-Paket zu signieren. Wenn Sie **SignerSignEx2** mit Windows-App-Paketen verwenden, gelten die folgenden Einschränkungen:

-   Sie müssen einen Zeiger auf eine **AppX \_ SIP- \_ Client \_ Daten** Struktur als *psipdata* -Parameter angeben, wenn Sie ein App-Paket signieren. Sie müssen den **psignerparser** -Member von **AppX SIP- \_ \_ Client \_ Daten** mit denselben Parametern auffüllen, die Sie zum Signieren des App-Pakets verwenden. Zu diesem Zweck definieren Sie die gewünschten Parameter in der **Signatur Geber \_ Sign \_ ex2 \_ para** meters-Struktur, weisen die Adresse dieser Struktur **psignerpara** Metern zu und verweisen dann direkt auf die Member der Struktur, wenn Sie [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)aufgerufen haben.
-   Nachdem Sie [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)aufgerufen haben, müssen Sie den **pappxsipstate** für *psipdata* freigeben, indem [**Sie IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf **pappxsipstate** aufrufen, wenn er nicht **null** ist.
-   Der **algidhash** -Member der **\_ Signatur \_ Informations** Struktur der Signatur Geber muss mit dem Hash Algorithmus identisch sein, der beim Erstellen des App-Pakets verwendet wurde. Informationen dazu, wie Sie den Hash Algorithmus aus dem App-Paket ermitteln, finden Sie unter [Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md). Der Standard Algorithmus von Windows 8, den [makeappx](make-appx-package--makeappx-exe-.md) und Visual Studio zum Erstellen von App-Paketen verwenden, ist "algidhash = calg \_ SHA \_ 256".
-   Wenn Sie die Signatur auch Zeitstempel für das App-Paket verwenden möchten, müssen Sie dies während des Aufrufens von [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) tun, indem Sie die optionalen Zeitstempel Parameter von **SignerSignEx2**(*dwtimestampflags*, *psztimestampalgorithmuid*, *pwszhttptimestamp*, *psrequest*) bereitstellen. Das Aufrufen von [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) oder der zugehörigen Varianten für ein App-Paket, das bereits signiert ist, wird nicht unterstützt.

Hier sehen Sie einen Beispielcode, in dem gezeigt wird, wie [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)aufgerufen wird:


```C++
HRESULT SignAppxPackage(
    _In_ PCCERT_CONTEXT signingCertContext,
    _In_ LPCWSTR packageFilePath)
{
    HRESULT hr = S_OK;
 
    // Initialize the parameters for SignerSignEx2
    DWORD signerIndex = 0;
 
    SIGNER_FILE_INFO fileInfo = {};
    fileInfo.cbSize = sizeof(SIGNER_FILE_INFO);
    fileInfo.pwszFileName = packageFilePath;
 
    SIGNER_SUBJECT_INFO subjectInfo = {};
    subjectInfo.cbSize = sizeof(SIGNER_SUBJECT_INFO);
    subjectInfo.pdwIndex = &signerIndex;
    subjectInfo.dwSubjectChoice = SIGNER_SUBJECT_FILE;
    subjectInfo.pSignerFileInfo = &fileInfo;
 
    SIGNER_CERT_STORE_INFO certStoreInfo = {};
    certStoreInfo.cbSize = sizeof(SIGNER_CERT_STORE_INFO);
    certStoreInfo.dwCertPolicy = SIGNER_CERT_POLICY_CHAIN_NO_ROOT;
    certStoreInfo.pSigningCert = signingCertContext;
 
    SIGNER_CERT cert = {};
    cert.cbSize = sizeof(SIGNER_CERT);
    cert.dwCertChoice = SIGNER_CERT_STORE;
    cert.pCertStoreInfo = &certStoreInfo;
 
    // The algidHash of the signature to be created must match the
    // hash algorithm used to create the app package
    SIGNER_SIGNATURE_INFO signatureInfo = {};
    signatureInfo.cbSize = sizeof(SIGNER_SIGNATURE_INFO);
    signatureInfo.algidHash = CALG_SHA_256; 
    signatureInfo.dwAttrChoice = SIGNER_NO_ATTR;
 
    SIGNER_SIGN_EX2_PARAMS signerParams = {};
    signerParams.pSubjectInfo = &subjectInfo;
    signerParams.pSigningCert = &cert;
    signerParams.pSignatureInfo = &signatureInfo;
 
    APPX_SIP_CLIENT_DATA sipClientData = {};
    sipClientData.pSignerParams = &signerParams;
    signerParams.pSipData = &sipClientData;
 
    // Type definition for invoking SignerSignEx2 via GetProcAddress
    typedef HRESULT (WINAPI *SignerSignEx2Function)(
        DWORD,
        PSIGNER_SUBJECT_INFO,
        PSIGNER_CERT,
        PSIGNER_SIGNATURE_INFO,
        PSIGNER_PROVIDER_INFO,
        DWORD,
        PCSTR,
        PCWSTR,
        PCRYPT_ATTRIBUTES,
        PVOID,
        PSIGNER_CONTEXT *,
        PVOID,
        PVOID); 
 
    // Load the SignerSignEx2 function from MSSign32.dll
    HMODULE msSignModule = LoadLibraryEx(
        L"MSSign32.dll", 
        NULL, 
        LOAD_LIBRARY_SEARCH_SYSTEM32);

    if (msSignModule)
    {
        SignerSignEx2Function SignerSignEx2 = reinterpret_cast<SignerSignEx2Function>(
            GetProcAddress(msSignModule, "SignerSignEx2"));
        if (SignerSignEx2)
        {
            hr = SignerSignEx2(
                signerParams.dwFlags,
                signerParams.pSubjectInfo,
                signerParams.pSigningCert,
                signerParams.pSignatureInfo,
                signerParams.pProviderInfo,
                signerParams.dwTimestampFlags,
                signerParams.pszAlgorithmOid,
                signerParams.pwszTimestampURL,
                signerParams.pCryptAttrs,
                signerParams.pSipData,
                signerParams.pSignerContext,
                signerParams.pCryptoPolicy,
                signerParams.pReserved);
        }
        else
        {
            DWORD lastError = GetLastError();
            hr = HRESULT_FROM_WIN32(lastError);
        }
 
        FreeLibrary(msSignModule);
    }
    else
    {
        DWORD lastError = GetLastError();
        hr = HRESULT_FROM_WIN32(lastError);
    }
 
    // Free any state used during app package signing
    if (sipClientData.pAppxSipState)
    {
        sipClientData.pAppxSipState->Release();
    }
 
    return hr;
}
```



## <a name="remarks"></a>Bemerkungen

Nachdem Sie das App-Paket signiert haben, können Sie auch versuchen, die Signatur Programm gesteuert zu validieren, indem Sie die [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) -Funktion mit der **wintrust- \_ Aktion \_ generic \_ Verify \_ v2** verwenden. In diesem Fall gibt es keine besonderen Überlegungen für die Verwendung von **WinVerifyTrust** mit Windows-App-Paketen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))
</dt> <dt>

[Verpacken von APIs](interfaces.md)
</dt> <dt>

[Kryptografiefunktionen](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 