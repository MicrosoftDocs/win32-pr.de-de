---
description: In diesem Thema wird beschrieben, wie Sie die Zertifikate, aus denen eine Zertifikatkette erstellt wird, in ein XPS-Dokument einbetten.
ms.assetid: c6aae8ff-2e1e-43de-9105-171e4187d193
title: Einbetten von Zertifikatketten in ein Dokument
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e23e47b4cd0d140d7200fb8aa01642ea5fbb731e49dcc289f596a054b0accbf3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119447580"
---
# <a name="embed-certificate-chains-in-a-document"></a>Einbetten von Zertifikatketten in ein Dokument

In diesem Thema wird beschrieben, wie Sie die Zertifikate, aus denen eine Zertifikatkette erstellt wird, in ein XPS-Dokument einbetten. Eine Zertifikatkette besteht aus allen Zertifikaten mit Ausnahme des Stammzertifikats, die zum Zertifizieren des durch das Endzertifikat identifizierten Subjekts erforderlich sind.

Um eine Zertifikatkette in ein XPS-Dokument einbetten zu können, erstellen Sie zunächst die Zertifikatkette, wie im folgenden Codebeispiel gezeigt.

Die **CreateCertificateChain-Methode** im Codebeispiel akzeptiert *certificateStore* als Parameter, bei dem es sich um einen **HCERTSTORE-Wert** handelt. Wenn dieser Wert **NULL ist,** werden die Zertifikate vom Zertifikatserver des Clientcomputers abgerufen. Wenn der Wert das Handle für einen Zertifikatspeicher ist, werden die Zertifikate aus diesem Speicher abgerufen, auf den *certificateStore* verweist, sowie vom Zertifikatserver des Clientcomputers.


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



Im folgenden Codebeispiel wird eine Zertifikatkette aus Zertifikaten erstellt und anschließend einem XPS-Dokument hinzufügt. Beachten [**Sie, dass CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) die Zertifikatkette erstellt, in der das Signaturzertifikat zuerst und das Stammzertifikat das letzte ist. Das Signaturzertifikat und das Stammzertifikat werden in diesem Beispiel nicht hinzugefügt. Die Signaturzertifikate werden mit einem Aufruf der [**IXpsSignatureManager::Sign-Methode**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) hinzugefügt. Dies sollte die letzte Signaturmethode sein, die für das Dokument aufgerufen wird. Das Stammzertifikat wird nicht hinzugefügt, wenn das Dokument signiert ist, da es beim Überprüfen der Signatur vom Zertifikatserver des Clientcomputers bereitgestellt werden muss.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Laden eines Zertifikats aus einer Datei](load-a-certificate-from-a-file.md)
</dt> <dt>

[Überprüfen, ob ein Zertifikat eine Signaturmethode unterstützt](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Überprüfen, ob das System eine Digestmethode unterstützt](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

**Wird in diesem Beispiel verwendet**
</dt> <dt>

[**\_CERT-KONTEXT**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**CRYPT \_ OID \_ INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[**IOpcCertificateSet**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[**IXpsSigningOptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Kryptografie-API](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Kryptografiefunktionen](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Digitale Zertifikate](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[Zertifikatketten](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[Überprüfung der Zertifikatvertrauensstellung](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[XPS Digital Signature-API-Fehler](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS-Dokumentfehler](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
