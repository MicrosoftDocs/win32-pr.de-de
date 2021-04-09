---
description: In diesem Thema wird beschrieben, wie Sie ein XPS-Dokument signieren.
ms.assetid: fbe64aed-6b07-49de-910c-18be68cb65a2
title: Signieren eines Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a4ad07323a26d21f9010c3fd54c708880b90173
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864747"
---
# <a name="sign-a-document"></a><span data-ttu-id="cc9a4-103">Signieren eines Dokuments</span><span class="sxs-lookup"><span data-stu-id="cc9a4-103">Sign a Document</span></span>

<span data-ttu-id="cc9a4-104">In diesem Thema wird beschrieben, wie Sie ein XPS-Dokument signieren.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-104">This topic describes how to sign an XPS document.</span></span>

<span data-ttu-id="cc9a4-105">Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="cc9a4-105">Before using the following code examples in your program, read the disclaimer in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).</span></span>

<span data-ttu-id="cc9a4-106">Zum Signieren eines XPS-Dokuments laden Sie es zunächst in einen Signatur-Manager, wie unter [Initialisieren des Signatur-Managers](initialize-the-signature-manager.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-106">To sign an XPS document, first load it into a signature manager as described in [Initialize the Signature Manager](initialize-the-signature-manager.md).</span></span>

<span data-ttu-id="cc9a4-107">So signieren Sie ein Dokument, das in einen Signatur-Manager geladen wurde:</span><span class="sxs-lookup"><span data-stu-id="cc9a4-107">To sign a document that has been loaded into a signature manager:</span></span>

1.  <span data-ttu-id="cc9a4-108">Instanziieren Sie eine [**ixpssigningoptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-108">Instantiate an [**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) interface.</span></span>
2.  <span data-ttu-id="cc9a4-109">Legen Sie die Signatur Richtlinie fest.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-109">Set the signing policy.</span></span>
3.  <span data-ttu-id="cc9a4-110">Legen Sie die Signatur Methode fest.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-110">Set the signature method.</span></span> <span data-ttu-id="cc9a4-111">URI-Zeichen folgen Konstanten der Signatur Methode sind in "cryptxml. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-111">Signature method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="cc9a4-112">Weitere Informationen zu gültigen Signatur Methoden Werten finden Sie unter [**ixpssigningoptions:: setsignaturemethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span><span class="sxs-lookup"><span data-stu-id="cc9a4-112">For more information about valid signature method values, see [**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).</span></span>
4.  <span data-ttu-id="cc9a4-113">Legen Sie die Digest-Methode fest.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-113">Set the digest method.</span></span> <span data-ttu-id="cc9a4-114">URI-Zeichenfolge Konstanten der Digest-Methode sind in "cryptxml. h" definiert.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-114">Digest method URI string constants are defined in cryptxml.h.</span></span> <span data-ttu-id="cc9a4-115">Informationen zu gültigen Digest-Methoden Werten finden Sie unter [**ixpssigningoptions:: setdigestmethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span><span class="sxs-lookup"><span data-stu-id="cc9a4-115">For information about valid digest method values, see [**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).</span></span>
5.  <span data-ttu-id="cc9a4-116">Laden Sie das Zertifikat wie unter [Laden eines Zertifikats aus einer Datei](load-a-certificate-from-a-file.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-116">Load the certificate as described in [Load a Certificate From a File](load-a-certificate-from-a-file.md).</span></span>
6.  <span data-ttu-id="cc9a4-117">Vergewissern Sie sich, dass das Zertifikat die Signatur Methode unterstützt, wie unter [überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt](verify-a-certificate-supports-a-signature-method.md).</span><span class="sxs-lookup"><span data-stu-id="cc9a4-117">Verify that the certificate supports the signature method, as described in [Verify That a Certificate Supports a Signature Method](verify-a-certificate-supports-a-signature-method.md).</span></span>
7.  <span data-ttu-id="cc9a4-118">Überprüfen Sie, ob die Digest-Methode vom System unterstützt wird, wie unter [überprüfen, ob das System eine Digest-Methode unterstützt](verify-a-certificate-supports-a-digest-method.md).</span><span class="sxs-lookup"><span data-stu-id="cc9a4-118">Verify that the digest method is supported by the system, as described in [Verify the System Supports a Digest Method](verify-a-certificate-supports-a-digest-method.md).</span></span>
8.  <span data-ttu-id="cc9a4-119">Betten Sie ggf. die Zertifikate der Zertifikats Vertrauenskette in das XPS-Dokument ein, wie unter [Einbetten von Zertifikat Ketten in einem Dokument](embedding-certificate-trust-chains-in-a-document.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-119">If required, embed the certificates of the certificate trust chain in the XPS document as described in [Embed Certificate Chains in a Document](embedding-certificate-trust-chains-in-a-document.md).</span></span>
9.  <span data-ttu-id="cc9a4-120">Signieren Sie das XPS-Dokument.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-120">Sign the XPS document.</span></span>

<span data-ttu-id="cc9a4-121">Im folgenden Codebeispiel wird veranschaulicht, wie die vorangehenden Schritte in einem Programm verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cc9a4-121">The following code example illustrates how to use the preceding steps in a program.</span></span>


```C++
    // this example requires:
    //        cryptxml.h
    // and refers to local methods that are described
    // in other topics

    HRESULT                hr               = S_OK;
    BOOL                   supported        = FALSE;
    BOOL                   succeeded        = FALSE;
    IXpsSigningOptions     *signingOptions  = NULL;
    IXpsSignature          *signature       = NULL;
    PCCERT_CONTEXT         certificate      = NULL;
    
    // Instantiate an IXpsSigningOptions interface.
    hr = signatureManager->CreateSigningOptions (&signingOptions);
    
    if (SUCCEEDED(hr)) {
        // Set the signing policy to indicate the document parts 
        //  to sign.
        hr = signingOptions->SetPolicy (XPS_SIGN_POLICY_CORE_PROPERTIES);
    }

    if (SUCCEEDED(hr)) {
        // Set the digital signature method to use to generate the 
        //    signature hash value. 
        //
        // The signature method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetSignatureMethod (
            wszURI_XMLNS_DIGSIG_RSA_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Set the digest method to use.
        //
        // The digest method used in this example is 
        //    defined in cryptxml.h.
        hr = signingOptions->SetDigestMethod (wszURI_XMLNS_DIGSIG_SHA1);
    }

    if (SUCCEEDED(hr)) {
        // Load a certificate from a certificate file
        hr = LoadCertificateFromFile (signingCertificate, &certificate);
    }

    if (SUCCEEDED(hr)) {
        // Verify the certificate supports the digest method
        supported = SupportsDigestAlgorithm (
            wszURI_XMLNS_DIGSIG_SHA1);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Verify the signature method is supported by the certificate
        //  and the system
        supported = SupportsSignatureAlgorithm(
            wszURI_XMLNS_DIGSIG_RSA_SHA1, certificate);
        if (!supported) hr = E_FAIL;
    }

    if (SUCCEEDED(hr)) {
        // Embed the certificate trust chain in the XPS package (optional).
        hr = EmbedCertificateChainInXpsPackage (signingOptions, certificate);
    }

    if (SUCCEEDED(hr)) {
        // Sign the XPS document
        hr = signatureManager->Sign (signingOptions, certificate, &signature);
    }

 //<Free the certificate context
    if (NULL != certificate) CertFreeCertificateContext (certificate);

    if (NULL != signingOptions) signingOptions->Release();
    if (NULL != signature) signature->Release();
```



## <a name="related-topics"></a><span data-ttu-id="cc9a4-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="cc9a4-122">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="cc9a4-123">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-123">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="cc9a4-124">Hinzufügen einer Signatur Anforderung zu einem XPS-Dokument</span><span class="sxs-lookup"><span data-stu-id="cc9a4-124">Add a Signature Request to an XPS Document</span></span>](add-a-signature-request-to-a-document.md)
</dt> <dt>

[<span data-ttu-id="cc9a4-125">Überprüfen von Dokument Signaturen</span><span class="sxs-lookup"><span data-stu-id="cc9a4-125">Verify Document Signatures</span></span>](verify-document-signatures.md)
</dt> <dt>

<span data-ttu-id="cc9a4-126">**In diesem Abschnitt verwendet**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-126">**Used in This Section**</span></span>
</dt> <dt>

[<span data-ttu-id="cc9a4-127">**Certfreecertififeecontext**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-127">**CertFreeCertificateContext**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[<span data-ttu-id="cc9a4-128">**Ixpssignaturemanager**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-128">**IXpsSignatureManager**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[<span data-ttu-id="cc9a4-129">**Ixpssignaturemanager:: kreatesigningoptions**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-129">**IXpsSignatureManager::CreateSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[<span data-ttu-id="cc9a4-130">**Ixpssignaturemanager:: Sign**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-130">**IXpsSignatureManager::Sign**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[<span data-ttu-id="cc9a4-131">**Ixpssigningoptions**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-131">**IXpsSigningOptions**</span></span>](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[<span data-ttu-id="cc9a4-132">**Ixpssigningoptions:: setdigestmethod**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-132">**IXpsSigningOptions::SetDigestMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[<span data-ttu-id="cc9a4-133">**Ixpssigningoptions:: setpolicy**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-133">**IXpsSigningOptions::SetPolicy**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[<span data-ttu-id="cc9a4-134">**Ixpssigningoptions:: setsignaturemethod**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-134">**IXpsSigningOptions::SetSignatureMethod**</span></span>](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[<span data-ttu-id="cc9a4-135">**XPS- \_ Signatur \_ Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-135">**XPS\_SIGN\_POLICY**</span></span>](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

<span data-ttu-id="cc9a4-136">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="cc9a4-136">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="cc9a4-137">Kryptografieapi</span><span class="sxs-lookup"><span data-stu-id="cc9a4-137">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="cc9a4-138">Kryptografiefunktionen</span><span class="sxs-lookup"><span data-stu-id="cc9a4-138">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="cc9a4-139">Laden eines Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="cc9a4-139">Load a Certificate From a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="cc9a4-140">Überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt</span><span class="sxs-lookup"><span data-stu-id="cc9a4-140">Verify a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="cc9a4-141">Überprüfen, ob das System eine Digest-Methode unterstützt</span><span class="sxs-lookup"><span data-stu-id="cc9a4-141">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="cc9a4-142">Einbinden von Zertifikat Ketten in ein Dokument</span><span class="sxs-lookup"><span data-stu-id="cc9a4-142">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[<span data-ttu-id="cc9a4-143">XPS-Fehler bei der digitalen Signatur-API</span><span class="sxs-lookup"><span data-stu-id="cc9a4-143">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="cc9a4-144">XPS-Dokument Fehler</span><span class="sxs-lookup"><span data-stu-id="cc9a4-144">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="cc9a4-145">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="cc9a4-145">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
