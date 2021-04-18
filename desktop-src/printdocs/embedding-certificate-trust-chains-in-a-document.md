---
description: In diesem Thema wird beschrieben, wie die Zertifikate, die eine Zertifikatskette bilden, in ein XPS-Dokument eingebettet werden.
ms.assetid: c6aae8ff-2e1e-43de-9105-171e4187d193
title: Einbinden von Zertifikat Ketten in ein Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee6476e0c187cf1a62915f0a3ab2b7949586baa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358421"
---
# <a name="embed-certificate-chains-in-a-document"></a><span data-ttu-id="c0ade-103">Einbinden von Zertifikat Ketten in ein Dokument</span><span class="sxs-lookup"><span data-stu-id="c0ade-103">Embed Certificate Chains in a Document</span></span>

<span data-ttu-id="c0ade-104">In diesem Thema wird beschrieben, wie die Zertifikate, die eine Zertifikatskette bilden, in ein XPS-Dokument eingebettet werden.</span><span class="sxs-lookup"><span data-stu-id="c0ade-104">This topic describes how to embed the certificates that make up a certificate chain into an XPS document.</span></span> <span data-ttu-id="c0ade-105">Eine Zertifikat Kette besteht aus allen Zertifikaten, mit Ausnahme des Stamm Zertifikats, die zum zertifizieren des Antragstellers erforderlich sind, der durch das Endzertifikat identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="c0ade-105">A certificate chain consists of all the certificates, except the root certificate, that are needed to certify the subject identified by the end certificate.</span></span>

<span data-ttu-id="c0ade-106">Um eine Zertifikat Kette in ein XPS-Dokument einzubetten, erstellen Sie zunächst die Zertifikat Kette, wie im folgenden Codebeispiel veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="c0ade-106">To embed a certificate chain into an XPS document, first create the certificate chain as illustrated in the following code example.</span></span>

<span data-ttu-id="c0ade-107">Die Methode " **kreatecertificatechain** " im Codebeispiel akzeptiert " *CertificateStore* " als Parameter, bei dem es sich um einen **HCERTSTORE** -Wert handelt.</span><span class="sxs-lookup"><span data-stu-id="c0ade-107">The **CreateCertificateChain** method in the code example accepts *certificateStore* as a parameter, which is an **HCERTSTORE** value.</span></span> <span data-ttu-id="c0ade-108">Wenn dieser Wert **null** ist, werden die Zertifikate vom Zertifikat Server des Client Computers abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c0ade-108">If this value is **NULL**, the certificates will be retrieved from the client computer's certificate server.</span></span> <span data-ttu-id="c0ade-109">Wenn der Wert das Handle für einen Zertifikat Speicher ist, werden die Zertifikate aus dem Speicher abgerufen, auf den von *CertificateStore* und vom Zertifikat Server des Client Computers verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="c0ade-109">If the value is the handle to a certificate store, the certificates will be retrieved from that store referenced by *certificateStore* as well as from the client computer's certificate server.</span></span>


```C++
HRESULT 
CreateCertificateChain (
    __in PCCERT_CONTEXT            certificate,
    __in HCERTSTORE                certificateStore,
    __out PCCERT_CHAIN_CONTEXT* certificateChain
)
{
    HRESULT  hr = S_OK;

    CERT_CHAIN_PARA certificateChainParameters = {0};

    certificateChainParameters.cbSize = sizeof(CERT_CHAIN_PARA);
    certificateChainParameters.RequestedUsage.dwType = USAGE_MATCH_TYPE_AND;

    // CertGetCertificateChain builds a certificate chain that starts 
    //  from the PCCERT_CONTEXT structure provided by the caller.
    //  After the certificate chain has been successfully created, 
    //  then the authenticity of the certificate can be determined 
    //  by examining the errors, if any, that occurred while the chain
    //  was created.
    BOOL successCreatingCertChain = CertGetCertificateChain (
        NULL,
        certificate,
        NULL,
        certificateStore,
        &certificateChainParameters,
        CERT_CHAIN_REVOCATION_CHECK_CHAIN_EXCLUDE_ROOT,
        NULL,
        certificateChain);

    if (!successCreatingCertChain)
    {
        hr = HRESULT_FROM_WIN32(GetLastError());
    }
    return hr;
}
```



<span data-ttu-id="c0ade-110">Im folgenden Codebeispiel wird eine Zertifikat Kette aus Zertifikaten erstellt und dann zu einem XPS-Dokument hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c0ade-110">The following code example creates a certificate chain from certificates and then adds these certificates to an XPS document.</span></span> <span data-ttu-id="c0ade-111">Beachten Sie, dass [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) die Zertifikat Kette erstellt, in der zuerst das Signaturzertifikat und das Stamm Zertifikat zuletzt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c0ade-111">Note that [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) creates the certificate chain in which the signing certificate is first and the root certificate is last.</span></span> <span data-ttu-id="c0ade-112">In diesem Beispiel werden das Signaturzertifikat und das Stamm Zertifikat nicht hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="c0ade-112">The signing certificate and the root certificate are not added in this example.</span></span> <span data-ttu-id="c0ade-113">Die Signatur Zertifikate werden mit einem Aufruf der [**ixpssignaturemanager:: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) -Methode hinzugefügt, die die letzte Signatur Methode sein sollte, die für das Dokument aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c0ade-113">The signing certificates will be added with a call to the [**IXpsSignatureManager::Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) method, which should be the last signature method called on the document.</span></span> <span data-ttu-id="c0ade-114">Das Stamm Zertifikat wird nicht hinzugefügt, wenn das Dokument signiert wird, da es vom Zertifikat Server des Client Computers bereitgestellt werden muss, wenn die Signatur überprüft wird.</span><span class="sxs-lookup"><span data-stu-id="c0ade-114">The root certificate is not added when the document is signed, because it must be provided by the client computer's certificate server when the signature is validated.</span></span>


```C++
HRESULT
EmbedCertificateChainInXpsPackage (
    __in IXpsSigningOptions *signingOptions,
    __in PCCERT_CONTEXT signingCertificate
)
{
    HRESULT                 hr                           = S_OK;
    PCCERT_CHAIN_CONTEXT    certificateChainContext      = NULL;
    IOpcCertificateSet      *certificateSetToUpdate      = NULL;
    DWORD                   certificateChainContextIndex = 0;

    // Create the entire certificate chain that originates 
    //  from the certificate that is used to sign the XPS document.
    hr = CreateCertificateChain(
        signingCertificate, 
        NULL, 
        &certificateChainContext);

    if (SUCCEEDED(hr))
    {
        // The signing options of an XPS document contain a pointer to 
        //  an IOpcCertificateSet interface that can be retrieved by 
        //  calling the GetCertificateSet method.
        hr = signingOptions->GetCertificateSet(&certificateSetToUpdate);
    }
    if (SUCCEEDED(hr))
    {
        // for each certificate chain context in this certificate...
        for (certificateChainContextIndex = 0; 
             certificateChainContextIndex < certificateChainContext->cChain; 
             certificateChainContextIndex++)
        {
            // inside a certificate chain context, 
            DWORD adjustedSimpleChainStartIndex = 0;
            DWORD adjustedSimpleChainEndIndex = 0;
            DWORD simpleCertChainIndex = 0;
            CERT_SIMPLE_CHAIN  *simpleCertificateChainWithinContext = NULL;

            // get the information about the certificate chain
            //  set the first item in the certificate chain to load
            //  Ignore the first PCCERT_CONTEXT in the first CERT_SIMPLE_CHAIN
            //  because this is the certificate that was used to build
            //  the chain and is already loaded in the document
            if (certificateChainContextIndex == 0)
            {
                adjustedSimpleChainStartIndex = 1;
            }
            else
            {
                adjustedSimpleChainStartIndex = 0;
            }
                    
            //  get the last item in the certificate chain
            simpleCertificateChainWithinContext = 
                certificateChainContext->rgpChain[certificateChainContextIndex];
            adjustedSimpleChainEndIndex = 
                simpleCertificateChainWithinContext->cElement;

            // Ignore the last PCCERT_CONTEXT in the last CERT_SIMPLE_CHAIN
            //  because this is the root certificate that must be retrieved
            //  from the client computer's certificate server.
            if (certificateChainContextIndex == certificateChainContext->cChain - 1)
            {
                if (adjustedSimpleChainEndIndex != 0)
                {
                    adjustedSimpleChainEndIndex = adjustedSimpleChainEndIndex - 1;
                }
            }

            // for each certificate chain in this context...
            for (simpleCertChainIndex = adjustedSimpleChainStartIndex; 
                 simpleCertChainIndex < adjustedSimpleChainEndIndex;
                 simpleCertChainIndex++)
            {
                // Add the certificate to the XPS document.
                PCCERT_CONTEXT certificateToEmbed = 
                    simpleCertificateChainWithinContext->rgpElement[simpleCertChainIndex]->pCertContext;
                if (FAILED(hr = certificateSetToUpdate->Add(certificateToEmbed)))
                {
                    break; // out of for loop with failed hr
                }
            }
        }
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="c0ade-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="c0ade-115">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="c0ade-116">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="c0ade-116">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="c0ade-117">Laden eines Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="c0ade-117">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="c0ade-118">Überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt</span><span class="sxs-lookup"><span data-stu-id="c0ade-118">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="c0ade-119">Überprüfen, ob das System eine Digest-Methode unterstützt</span><span class="sxs-lookup"><span data-stu-id="c0ade-119">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

<span data-ttu-id="c0ade-120">**In diesem Beispiel verwendet**</span><span class="sxs-lookup"><span data-stu-id="c0ade-120">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="c0ade-121">**CERT- \_ Kontext**</span><span class="sxs-lookup"><span data-stu-id="c0ade-121">**CERT\_CONTEXT**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[<span data-ttu-id="c0ade-122">**CertGetCertificateChain dokumentiert**</span><span class="sxs-lookup"><span data-stu-id="c0ade-122">**CertGetCertificateChain**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[<span data-ttu-id="c0ade-123">**Crypt- \_ OID- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="c0ade-123">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[<span data-ttu-id="c0ade-124">**Iopccertifiaseeset**</span><span class="sxs-lookup"><span data-stu-id="c0ade-124">**IOpcCertificateSet**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[<span data-ttu-id="c0ade-125">**Ixpssigningoptions**</span><span class="sxs-lookup"><span data-stu-id="c0ade-125">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

<span data-ttu-id="c0ade-126">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="c0ade-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="c0ade-127">Kryptografieapi</span><span class="sxs-lookup"><span data-stu-id="c0ade-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="c0ade-128">Kryptografiefunktionen</span><span class="sxs-lookup"><span data-stu-id="c0ade-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="c0ade-129">Digitale Zertifikate</span><span class="sxs-lookup"><span data-stu-id="c0ade-129">Digital Certificates</span></span>](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[<span data-ttu-id="c0ade-130">Zertifikat Ketten</span><span class="sxs-lookup"><span data-stu-id="c0ade-130">Certificate Chains</span></span>](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[<span data-ttu-id="c0ade-131">Zertifikat Vertrauensstellungs Überprüfung</span><span class="sxs-lookup"><span data-stu-id="c0ade-131">Certificate Trust Verification</span></span>](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[<span data-ttu-id="c0ade-132">XPS-Fehler bei der digitalen Signatur-API</span><span class="sxs-lookup"><span data-stu-id="c0ade-132">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="c0ade-133">XPS-Dokument Fehler</span><span class="sxs-lookup"><span data-stu-id="c0ade-133">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="c0ade-134">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="c0ade-134">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
