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
# <a name="sign-a-document"></a>Signieren eines Dokuments

In diesem Thema wird beschrieben, wie Sie ein XPS-Dokument signieren.

Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).

Zum Signieren eines XPS-Dokuments laden Sie es zunächst in einen Signatur-Manager, wie unter [Initialisieren des Signatur-Managers](initialize-the-signature-manager.md)beschrieben.

So signieren Sie ein Dokument, das in einen Signatur-Manager geladen wurde:

1.  Instanziieren Sie eine [**ixpssigningoptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions) -Schnittstelle.
2.  Legen Sie die Signatur Richtlinie fest.
3.  Legen Sie die Signatur Methode fest. URI-Zeichen folgen Konstanten der Signatur Methode sind in "cryptxml. h" definiert. Weitere Informationen zu gültigen Signatur Methoden Werten finden Sie unter [**ixpssigningoptions:: setsignaturemethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod).
4.  Legen Sie die Digest-Methode fest. URI-Zeichenfolge Konstanten der Digest-Methode sind in "cryptxml. h" definiert. Informationen zu gültigen Digest-Methoden Werten finden Sie unter [**ixpssigningoptions:: setdigestmethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod).
5.  Laden Sie das Zertifikat wie unter [Laden eines Zertifikats aus einer Datei](load-a-certificate-from-a-file.md)beschrieben.
6.  Vergewissern Sie sich, dass das Zertifikat die Signatur Methode unterstützt, wie unter [überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt](verify-a-certificate-supports-a-signature-method.md).
7.  Überprüfen Sie, ob die Digest-Methode vom System unterstützt wird, wie unter [überprüfen, ob das System eine Digest-Methode unterstützt](verify-a-certificate-supports-a-digest-method.md).
8.  Betten Sie ggf. die Zertifikate der Zertifikats Vertrauenskette in das XPS-Dokument ein, wie unter [Einbetten von Zertifikat Ketten in einem Dokument](embedding-certificate-trust-chains-in-a-document.md)beschrieben.
9.  Signieren Sie das XPS-Dokument.

Im folgenden Codebeispiel wird veranschaulicht, wie die vorangehenden Schritte in einem Programm verwendet werden.


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

[Hinzufügen einer Signatur Anforderung zu einem XPS-Dokument](add-a-signature-request-to-a-document.md)
</dt> <dt>

[Überprüfen von Dokument Signaturen](verify-document-signatures.md)
</dt> <dt>

**In diesem Abschnitt verwendet**
</dt> <dt>

[**Certfreecertififeecontext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext)
</dt> <dt>

[**Ixpssignaturemanager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**Ixpssignaturemanager:: kreatesigningoptions**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-createsigningoptions)
</dt> <dt>

[**Ixpssignaturemanager:: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign)
</dt> <dt>

[**Ixpssigningoptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

[**Ixpssigningoptions:: setdigestmethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setdigestmethod)
</dt> <dt>

[**Ixpssigningoptions:: setpolicy**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setpolicy)
</dt> <dt>

[**Ixpssigningoptions:: setsignaturemethod**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssigningoptions-setsignaturemethod)
</dt> <dt>

[**XPS- \_ Signatur \_ Richtlinie**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_sign_policy)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Kryptografieapi](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Kryptografiefunktionen](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Laden eines Zertifikats aus einer Datei](load-a-certificate-from-a-file.md)
</dt> <dt>

[Überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Überprüfen, ob das System eine Digest-Methode unterstützt](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Einbinden von Zertifikat Ketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[XPS-Fehler bei der digitalen Signatur-API](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS-Dokument Fehler](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
