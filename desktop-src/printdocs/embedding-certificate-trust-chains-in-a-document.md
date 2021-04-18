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
# <a name="embed-certificate-chains-in-a-document"></a>Einbinden von Zertifikat Ketten in ein Dokument

In diesem Thema wird beschrieben, wie die Zertifikate, die eine Zertifikatskette bilden, in ein XPS-Dokument eingebettet werden. Eine Zertifikat Kette besteht aus allen Zertifikaten, mit Ausnahme des Stamm Zertifikats, die zum zertifizieren des Antragstellers erforderlich sind, der durch das Endzertifikat identifiziert wird.

Um eine Zertifikat Kette in ein XPS-Dokument einzubetten, erstellen Sie zunächst die Zertifikat Kette, wie im folgenden Codebeispiel veranschaulicht.

Die Methode " **kreatecertificatechain** " im Codebeispiel akzeptiert " *CertificateStore* " als Parameter, bei dem es sich um einen **HCERTSTORE** -Wert handelt. Wenn dieser Wert **null** ist, werden die Zertifikate vom Zertifikat Server des Client Computers abgerufen. Wenn der Wert das Handle für einen Zertifikat Speicher ist, werden die Zertifikate aus dem Speicher abgerufen, auf den von *CertificateStore* und vom Zertifikat Server des Client Computers verwiesen wird.


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



Im folgenden Codebeispiel wird eine Zertifikat Kette aus Zertifikaten erstellt und dann zu einem XPS-Dokument hinzugefügt. Beachten Sie, dass [**CertGetCertificateChain**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain) die Zertifikat Kette erstellt, in der zuerst das Signaturzertifikat und das Stamm Zertifikat zuletzt verwendet werden. In diesem Beispiel werden das Signaturzertifikat und das Stamm Zertifikat nicht hinzugefügt. Die Signatur Zertifikate werden mit einem Aufruf der [**ixpssignaturemanager:: Sign**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-sign) -Methode hinzugefügt, die die letzte Signatur Methode sein sollte, die für das Dokument aufgerufen wird. Das Stamm Zertifikat wird nicht hinzugefügt, wenn das Dokument signiert wird, da es vom Zertifikat Server des Client Computers bereitgestellt werden muss, wenn die Signatur überprüft wird.


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

[Überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Überprüfen, ob das System eine Digest-Methode unterstützt](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

**In diesem Beispiel verwendet**
</dt> <dt>

[**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CertGetCertificateChain dokumentiert**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**Crypt- \_ OID- \_ Informationen**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

[**Iopccertifiaseeset**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateset)
</dt> <dt>

[**Ixpssigningoptions**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssigningoptions)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Kryptografieapi](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Kryptografiefunktionen](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Digitale Zertifikate](/windows/desktop/SecCrypto/digital-certificates)
</dt> <dt>

[Zertifikat Ketten](/windows/desktop/SecCrypto/certificate-chains)
</dt> <dt>

[Zertifikat Vertrauensstellungs Überprüfung](/windows/desktop/SecCrypto/certificate-trust-verification)
</dt> <dt>

[XPS-Fehler bei der digitalen Signatur-API](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS-Dokument Fehler](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
