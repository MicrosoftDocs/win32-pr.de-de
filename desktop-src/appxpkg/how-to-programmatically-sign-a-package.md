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
# <a name="how-to-programmatically-sign-an-app-package-c"></a><span data-ttu-id="7f869-103">Programm gesteuertes Signieren eines App-Pakets (C++)</span><span class="sxs-lookup"><span data-stu-id="7f869-103">How to programmatically sign an app package (C++)</span></span>

<span data-ttu-id="7f869-104">Erfahren Sie, wie Sie ein App-Paket mithilfe der [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) -Funktion signieren.</span><span class="sxs-lookup"><span data-stu-id="7f869-104">Learn how to sign an app package by using the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function.</span></span>

<span data-ttu-id="7f869-105">Wenn Sie Windows-App-Pakete mithilfe der [Paket-API](interfaces.md)Programm gesteuert erstellen möchten, müssen Sie die APP-Pakete auch signieren, bevor Sie bereitgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="7f869-105">If you want to programmatically create Windows app packages by using the [Packaging API](interfaces.md), you also need to sign the app packages before they can be deployed.</span></span> <span data-ttu-id="7f869-106">Die Paket-API bietet keine spezielle Methode zum Signieren von App-Paketen.</span><span class="sxs-lookup"><span data-stu-id="7f869-106">The Packaging API doesn't provide a specialized method for signing app packages.</span></span> <span data-ttu-id="7f869-107">Verwenden Sie stattdessen die standardmäßigen [Kryptografiefunktionen](/windows/desktop/SecCrypto/cryptography-functions) zum Signieren Ihrer APP-Pakete.</span><span class="sxs-lookup"><span data-stu-id="7f869-107">Instead, use the standard [cryptography functions](/windows/desktop/SecCrypto/cryptography-functions) to sign your app packages.</span></span>

## <a name="what-you-need-to-know"></a><span data-ttu-id="7f869-108">Was Sie wissen müssen</span><span class="sxs-lookup"><span data-stu-id="7f869-108">What you need to know</span></span>

### <a name="technologies"></a><span data-ttu-id="7f869-109">Technologien</span><span class="sxs-lookup"><span data-stu-id="7f869-109">Technologies</span></span>

-   <span data-ttu-id="7f869-110">[Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7f869-110">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
-   [<span data-ttu-id="7f869-111">Verpacken, Bereitstellung und Abfrage von Windows-apps</span><span class="sxs-lookup"><span data-stu-id="7f869-111">Packaging, deployment, and query of Windows apps</span></span>](appx-portal.md)
-   [<span data-ttu-id="7f869-112">Kryptografiefunktionen</span><span class="sxs-lookup"><span data-stu-id="7f869-112">cryptography functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)

### <a name="prerequisites"></a><span data-ttu-id="7f869-113">Voraussetzungen</span><span class="sxs-lookup"><span data-stu-id="7f869-113">Prerequisites</span></span>

-   <span data-ttu-id="7f869-114">Sie benötigen eine gepackte Windows-app.</span><span class="sxs-lookup"><span data-stu-id="7f869-114">You need to have a packaged Windows app.</span></span> <span data-ttu-id="7f869-115">Informationen zum Erstellen eines App-Pakets finden [Sie unter Erstellen eines App-Pakets](how-to-create-a-package.md).</span><span class="sxs-lookup"><span data-stu-id="7f869-115">For info about creating an app package, see [How to create an app package](how-to-create-a-package.md).</span></span>
-   <span data-ttu-id="7f869-116">Sie benötigen ein Code Signaturzertifikat, das zum Signieren des App-Pakets geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="7f869-116">You need to have a code signing certificate that is appropriate for signing the app package.</span></span> <span data-ttu-id="7f869-117">Informationen zum Erstellen eines Test Code Signatur Zertifikats finden Sie unter [Erstellen eines App-Paket-Signatur Zertifikats](how-to-create-a-package-signing-certificate.md).</span><span class="sxs-lookup"><span data-stu-id="7f869-117">For info about creating a test code signing certificate, see [How to create an app package signing certificate](how-to-create-a-package-signing-certificate.md).</span></span> <span data-ttu-id="7f869-118">Laden Sie dieses Signaturzertifikat in eine [**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) Struktur.</span><span class="sxs-lookup"><span data-stu-id="7f869-118">Load this signing certificate into a [**CERT\_CONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context) structure.</span></span> <span data-ttu-id="7f869-119">Sie können z. b. [**pfximportcertstore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) und [**certfindcertifikateinstore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) verwenden, um ein Signaturzertifikat zu laden.</span><span class="sxs-lookup"><span data-stu-id="7f869-119">For example, you can use [**PFXImportCertStore**](/windows/desktop/api/wincrypt/nf-wincrypt-pfximportcertstore) and [**CertFindCertificateInStore**](/windows/desktop/api/wincrypt/nf-wincrypt-certfindcertificateinstore) to load a signing certificate.</span></span>
-   <span data-ttu-id="7f869-120">Mit Windows 8 wird die [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) -Funktion eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7f869-120">Windows 8 introduces the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function.</span></span> <span data-ttu-id="7f869-121">Verwenden Sie **SignerSignEx2** , wenn Sie Windows-App-Pakete signieren.</span><span class="sxs-lookup"><span data-stu-id="7f869-121">Use **SignerSignEx2** when you sign Windows app packages.</span></span>

## <a name="instructions"></a><span data-ttu-id="7f869-122">Anweisungen</span><span class="sxs-lookup"><span data-stu-id="7f869-122">Instructions</span></span>

### <a name="step-1-define-the-required-structures-for-signersignex2"></a><span data-ttu-id="7f869-123">Schritt 1: Definieren der erforderlichen Strukturen für SignerSignEx2</span><span class="sxs-lookup"><span data-stu-id="7f869-123">Step 1: Define the required structures for SignerSignEx2</span></span>

<span data-ttu-id="7f869-124">Zusätzlich zum Wincrypt. h-Header hängt die [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) -Funktion von vielen Strukturen ab, die in keiner SDK-Header Datei definiert sind.</span><span class="sxs-lookup"><span data-stu-id="7f869-124">In addition to the Wincrypt.h header, the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function depends on many structures that aren't defined in any SDK header file.</span></span> <span data-ttu-id="7f869-125">Um **SignerSignEx2** zu verwenden, müssen Sie diese Strukturen selbst definieren:</span><span class="sxs-lookup"><span data-stu-id="7f869-125">To use **SignerSignEx2**, you must define these structures yourself:</span></span>


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



### <a name="step-2-call-signersignex2-to-sign-the-app-package"></a><span data-ttu-id="7f869-126">Schritt 2: SignerSignEx2 zum Signieren des App-Pakets anrufen</span><span class="sxs-lookup"><span data-stu-id="7f869-126">Step 2: Call SignerSignEx2 to sign the app package</span></span>

<span data-ttu-id="7f869-127">Nachdem Sie die im vorherigen Schritt angegebenen erforderlichen Strukturen definiert haben, können Sie eine beliebige der Optionen verwenden, die in der [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) -Funktion verfügbar sind, um ein App-Paket zu signieren.</span><span class="sxs-lookup"><span data-stu-id="7f869-127">After you define the required structures that are specified in the previous step, you can use any of the options available on the [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) function to sign an app package.</span></span> <span data-ttu-id="7f869-128">Wenn Sie **SignerSignEx2** mit Windows-App-Paketen verwenden, gelten die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="7f869-128">When you use **SignerSignEx2** with Windows app packages, these restrictions apply:</span></span>

-   <span data-ttu-id="7f869-129">Sie müssen einen Zeiger auf eine **AppX \_ SIP- \_ Client \_ Daten** Struktur als *psipdata* -Parameter angeben, wenn Sie ein App-Paket signieren.</span><span class="sxs-lookup"><span data-stu-id="7f869-129">You must provide a pointer to an **APPX\_SIP\_CLIENT\_DATA** structure as the *pSipData* parameter when you sign an app package.</span></span> <span data-ttu-id="7f869-130">Sie müssen den **psignerparser** -Member von **AppX SIP- \_ \_ Client \_ Daten** mit denselben Parametern auffüllen, die Sie zum Signieren des App-Pakets verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f869-130">You must populate the **pSignerParams** member of **APPX\_SIP\_CLIENT\_DATA** with the same parameters that you use to sign the app package.</span></span> <span data-ttu-id="7f869-131">Zu diesem Zweck definieren Sie die gewünschten Parameter in der **Signatur Geber \_ Sign \_ ex2 \_ para** meters-Struktur, weisen die Adresse dieser Struktur **psignerpara** Metern zu und verweisen dann direkt auf die Member der Struktur, wenn Sie [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)aufgerufen haben.</span><span class="sxs-lookup"><span data-stu-id="7f869-131">To do this, define your desired parameters on the **SIGNER\_SIGN\_EX2\_PARAMS** structure, assign the address of this structure to **pSignerParams**, and then directly reference the structure's members as well when you call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2).</span></span>
-   <span data-ttu-id="7f869-132">Nachdem Sie [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)aufgerufen haben, müssen Sie den **pappxsipstate** für *psipdata* freigeben, indem [**Sie IUnknown:: Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf **pappxsipstate** aufrufen, wenn er nicht **null** ist.</span><span class="sxs-lookup"><span data-stu-id="7f869-132">After you call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2), you must free the **pAppxSipState** on the *pSipData* by calling [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) on **pAppxSipState** if it's not **NULL**.</span></span>
-   <span data-ttu-id="7f869-133">Der **algidhash** -Member der **\_ Signatur \_ Informations** Struktur der Signatur Geber muss mit dem Hash Algorithmus identisch sein, der beim Erstellen des App-Pakets verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7f869-133">The **algidHash** member of the **SIGNER\_SIGNATURE\_INFO** structure must be the same hash algorithm that was used in creating the app package.</span></span> <span data-ttu-id="7f869-134">Informationen dazu, wie Sie den Hash Algorithmus aus dem App-Paket ermitteln, finden Sie unter [Signieren eines App-Pakets mit SignTool](how-to-sign-a-package-using-signtool.md).</span><span class="sxs-lookup"><span data-stu-id="7f869-134">For info about how to determine the hash algorithm from the app package, see [How to sign an app package using SignTool](how-to-sign-a-package-using-signtool.md).</span></span> <span data-ttu-id="7f869-135">Der Standard Algorithmus von Windows 8, den [makeappx](make-appx-package--makeappx-exe-.md) und Visual Studio zum Erstellen von App-Paketen verwenden, ist "algidhash = calg \_ SHA \_ 256".</span><span class="sxs-lookup"><span data-stu-id="7f869-135">The Windows 8 default algorithm that [MakeAppx](make-appx-package--makeappx-exe-.md) and Visual Studio use to create app packages is “algidHash = CALG\_SHA\_256”.</span></span>
-   <span data-ttu-id="7f869-136">Wenn Sie die Signatur auch Zeitstempel für das App-Paket verwenden möchten, müssen Sie dies während des Aufrufens von [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) tun, indem Sie die optionalen Zeitstempel Parameter von **SignerSignEx2**(*dwtimestampflags*, *psztimestampalgorithmuid*, *pwszhttptimestamp*, *psrequest*) bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="7f869-136">If you want to time stamp the signature on the app package as well, you must do so during the call to [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2) by providing **SignerSignEx2**'s optional time stamping parameters (*dwTimestampFlags*, *pszTimestampAlgorithmOid*, *pwszHttpTimeStamp*, *psRequest*).</span></span> <span data-ttu-id="7f869-137">Das Aufrufen von [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) oder der zugehörigen Varianten für ein App-Paket, das bereits signiert ist, wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7f869-137">Calling [**SignerTimeStampEx3**](/windows/desktop/SecCrypto/signertimestampex3) or its variants on an app package that is already signed is unsupported.</span></span>

<span data-ttu-id="7f869-138">Hier sehen Sie einen Beispielcode, in dem gezeigt wird, wie [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2)aufgerufen wird:</span><span class="sxs-lookup"><span data-stu-id="7f869-138">Here is some example code that shows how to call [**SignerSignEx2**](/windows/desktop/SecCrypto/signersignex2):</span></span>


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



## <a name="remarks"></a><span data-ttu-id="7f869-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7f869-139">Remarks</span></span>

<span data-ttu-id="7f869-140">Nachdem Sie das App-Paket signiert haben, können Sie auch versuchen, die Signatur Programm gesteuert zu validieren, indem Sie die [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) -Funktion mit der **wintrust- \_ Aktion \_ generic \_ Verify \_ v2** verwenden.</span><span class="sxs-lookup"><span data-stu-id="7f869-140">After you sign the app package, you can also attempt to validate the signature programmatically by using the [**WinVerifyTrust**](/windows/desktop/api/wintrust/nf-wintrust-winverifytrust) function with **WINTRUST\_ACTION\_GENERIC\_VERIFY\_V2**.</span></span> <span data-ttu-id="7f869-141">In diesem Fall gibt es keine besonderen Überlegungen für die Verwendung von **WinVerifyTrust** mit Windows-App-Paketen.</span><span class="sxs-lookup"><span data-stu-id="7f869-141">There are no special considerations in this case for using **WinVerifyTrust** with Windows app packages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f869-142">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7f869-142">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="7f869-143">[Einführung in die Codesignatur](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7f869-143">[Introduction to Code Signing](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/ms537361(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7f869-144">Verpacken von APIs</span><span class="sxs-lookup"><span data-stu-id="7f869-144">Packaging API</span></span>](interfaces.md)
</dt> <dt>

[<span data-ttu-id="7f869-145">Kryptografiefunktionen</span><span class="sxs-lookup"><span data-stu-id="7f869-145">cryptography functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> </dl>

 

 