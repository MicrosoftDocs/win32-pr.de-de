---
description: In diesem Thema wird das Signieren eines XPS-Dokuments beschrieben.
ms.assetid: fbe64aed-6b07-49de-910c-18be68cb65a2
title: Signieren eines Dokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef544b2c34af19282d697676d22903948355d23e18e1c646df691c720052cc4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119033878"
---
# <a name="sign-a-document"></a>Signieren eines Dokuments

In diesem Thema wird das Signieren eines XPS-Dokuments beschrieben.

Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss unter [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).

Um ein XPS-Dokument zu signieren, laden Sie es zunächst in einen Signatur-Manager, wie unter [Initialisieren des Signatur-Managers beschrieben.](initialize-the-signature-manager.md)

So signieren Sie ein Dokument, das in einen Signatur-Manager geladen wurde:

1.  Instanziieren Sie eine [**IXpsSigningOptions-Schnittstelle.**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
2.  Legen Sie die Signaturrichtlinie fest.
3.  Legen Sie die Signaturmethode fest. URI-Zeichenfolgenkonst constants der Signaturmethode werden in cryptxml.h definiert. Weitere Informationen zu gültigen Signaturmethodenwerten finden Sie unter [**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).
4.  Legen Sie die Digestmethode fest. URI-Zeichenfolgenkonst constants der Digestmethode werden in "cryptxml.h" definiert. Informationen zu gültigen Digestmethodenwerten finden Sie unter [**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).
5.  Laden Sie das Zertifikat wie unter [Laden eines Zertifikats aus einer Datei beschrieben.](load-a-certificate-from-a-file.md)
6.  Stellen Sie sicher, dass das Zertifikat die Signaturmethode unterstützt, wie unter Überprüfen, ob ein [Zertifikat eine Signaturmethode unterstützt beschrieben wird.](verify-a-certificate-supports-a-signature-method.md)
7.  Stellen Sie sicher, dass die Digestmethode vom System unterstützt wird, wie unter [Überprüfen, ob das System eine Digestmethode unterstützt.](verify-a-certificate-supports-a-digest-method.md)
8.  Betten Sie bei Bedarf die Zertifikate der Zertifikatvertrauenskette in das XPS-Dokument ein, wie unter Einbetten von [Zertifikatketten in ein Dokument beschrieben.](embedding-certificate-trust-chains-in-a-document.md)
9.  Signieren Sie das XPS-Dokument.

Das folgende Codebeispiel veranschaulicht die Verwendung der vorherigen Schritte in einem Programm.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Hinzufügen einer Signaturanforderung zu einem XPS-Dokument](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Überprüfen von Dokumentsignaturen](verify-document-signatures.md)
</dt> <dt>

**Wird in diesem Abschnitt verwendet**
</dt> <dt>

[**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**IXpsSignatureManager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**IXpsSignatureManager::CreateSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[**IXpsSignatureManager::Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[**IXpsSigningOptions::SetDigestMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[**IXpsSigningOptions::SetPolicy**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[**IXpsSigningOptions::SetSignatureMethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[**\_ \_ XPS-SIGN-RICHTLINIE**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Kryptografie-API](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Kryptografiefunktionen](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Laden eines Zertifikats aus einer Datei](load-a-certificate-from-a-file.md)
</dt> <dt>

[Überprüfen, ob ein Zertifikat eine Signaturmethode unterstützt](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Überprüfen, ob das System eine Digestmethode unterstützt](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Einbetten von Zertifikatketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[XPS Digital Signature-API-Fehler](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS-Dokumentfehler](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
