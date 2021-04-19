---
description: In diesem Thema wird beschrieben, wie die Signaturen in einem XPS-Dokument überprüft werden und wie die Zertifikate überprüft werden, die mit diesen Signaturen verknüpft sind.
ms.assetid: fd12abaf-dc0f-4db1-837d-c116627bcc7e
title: Überprüfen von Dokument Signaturen und Zertifikaten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47dfee91437f7cc36e754e8c1f97fa89cd2387af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363699"
---
# <a name="verify-document-signatures-and-certificates"></a>Überprüfen von Dokument Signaturen und Zertifikaten

In diesem Thema wird beschrieben, wie die Signaturen in einem XPS-Dokument überprüft werden und wie die Zertifikate überprüft werden, die mit diesen Signaturen verknüpft sind.

Bevor Sie die folgenden Codebeispiele in Ihrem Programm verwenden, lesen Sie den Haftungsausschluss in [Common Digital Signature Programming Tasks](basic-digital-signature-programming-tasks.md).

Im folgenden Codebeispiel werden die digitalen Signaturen überprüft, die in einem XPS-Dokument gefunden werden.

Führen Sie die folgenden Schritte aus, um die Signaturen in einem XPS-Dokument zu überprüfen:

1.  Laden Sie das Dokument in einen Signatur-Manager, wie unter [Initialisieren des Signatur-Managers](initialize-the-signature-manager.md)beschrieben.
2.  Die Sammlung von Signaturen aus dem Digital Signature Manager zu erhalten.
3.  Gibt die Anzahl der Signaturen in der Auflistung an.
4.  Für jede Signatur in der Auflistung wird die Methode [**Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) aufgerufen, wie im folgenden Codebeispiel gezeigt.


```C++
HRESULT
VerifyAllDigitalSignaturesAndAuthenticateCertificates(
    IXpsSignatureManager *signatureManager
)
{
    HRESULT                       hr                              = S_OK;
    IXpsSignature                 *signature                      = NULL;
    IXpsSignatureCollection       *signaturesInDocument           = NULL;
    UINT32                        numberOfSignaturesInDocument    = NULL;

    hr = signatureManager->GetSignatures(&signaturesInDocument);
    if (SUCCEEDED(hr)) {
        hr = signaturesInDocument->GetCount(&numberOfSignaturesInDocument);
    }

    if (SUCCEEDED(hr)) {
        // Check each signature in the XPS document that was opened in
        //  the signature manager.
        for (UINT32 index = 0; index < numberOfSignaturesInDocument; index++)
        {
            // Get the signature in the current index of the 
            //  IXpsSignatureCollection object
            hr = signaturesInDocument->GetAt(index, &signature);

            if (SUCCEEDED(hr)) {
                PCCERT_CONTEXT       signingCertificate = NULL;
                XPS_SIGNATURE_STATUS signatureStatus; 

                signatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                // Verify the signature and authenticate 
                //  its signing certificate
                hr = VerifySignatureAndCertificates (
                        signature,
                        &signingCertificate,
                        &signatureStatus);
                if (FAILED(hr)) {
                    // If a FACILITY_SECURITY error code is returned then 
                    //  the current certificate was not the 
                    //    signing certificate, so continue with 
                    //  the enumeration.
                    if (HRESULT_FACILITY(hr) != FACILITY_SECURITY)
                    {
                        // If the error was not a FACILITY_SECURITY error  
                        //  then exit and return the error
                        break; // out of for loop
                    }
                }
                // release pointers for next loop
                if (NULL != signature) {
                    signature->Release(); 
                    signature = NULL; 
                }
                if (NULL != signingCertificate) {
                    CertFreeCertificateContext (signingCertificate); 
                    signingCertificate = NULL;
                }
            }
        }
    }
    if (NULL != signaturesInDocument) signaturesInDocument->Release();
    
    return hr;
}
```



Überprüfen Sie zum Überprüfen einer digitalen Signatur zunächst die vom Signaturzertifikat erstellte Signatur, und überprüfen Sie dann das Signaturzertifikat. Die im folgenden Codebeispiel verwendete Validierungsmethode speichert die Zertifikate in einem temporären Zertifikat Speicher zwischen, den die kryptografieapi-Funktionen verwenden, wenn Sie später in diesem Beispiel aufgerufen werden.

Um einen temporären Zertifikat Speicher zu erstellen, führen Sie die folgenden Schritte aus:

1.  Erstellen Sie einen temporären Zertifikat Speicher für die Zertifikate, die von der Signatur verwendet werden.
2.  Iterieren Sie den Zertifikats Satz der Signatur, und laden Sie jedes Zertifikat in den temporären Zertifikat Speicher.


```C++
HRESULT VerifySignatureAndCertificates (
    IXpsSignature           *signature,
    PCCERT_CONTEXT          *signingCertificate,
    XPS_SIGNATURE_STATUS    *signatureStatus
)
{
    HRESULT                         hr                        = S_OK;
    BOOL                            moreCertificates          = FALSE;
    IOpcCertificateEnumerator       *certificatesInSignature  = NULL;
    
    HCERTSTORE                      signatureCertificateStore = NULL;
    
    // Create a temporary certificate store.  
    signatureCertificateStore = CertOpenStore(
        CERT_STORE_PROV_MEMORY, 
        X509_ASN_ENCODING, 
        NULL, 
        0, 
        NULL);

    // Create a certificate enumerator to store the certificates 
    //  that are associated with the current signature.
    hr = signature->GetCertificateEnumerator(&certificatesInSignature);

    if (SUCCEEDED(hr))
    {
    // We need to call the MoveNext method to initialize the enumerator.
        hr = certificatesInSignature->MoveNext(&moreCertificates);
    }
    if (SUCCEEDED(hr))
    {
        // Iterate through the certificates in the signature, 
        //  and add each one to the temporary certificate store.  
        //  This temporary  certificate store simplifies 
        //  authentication of the signing certificate.
        while (moreCertificates)
        {
            PCCERT_CONTEXT certificate  = NULL;
            hr = certificatesInSignature->GetCurrent(&certificate);
            if (SUCCEEDED(hr))
            {
                // got the next certificate so
                // add the current certificate to the temporary certificate store.
                if (!CertAddCertificateContextToStore(signatureCertificateStore,
                    certificate,
                    CERT_STORE_ADD_REPLACE_EXISTING,
                    NULL))
                {
                    hr = E_FAIL;
                    // ERROR: could not add the certificate to the certificate store
                    break; // out of while loop
                }
                CertFreeCertificateContext (certificate);
            }
            else
            {
                // unable to get the certificate so skip
            }

            // move to next certificate in set
            if (FAILED(hr = certificatesInSignature->MoveNext(&moreCertificates)))
            {
                // ERROR: could not move to the next certificate in the enumerator
                break; // out of while loop
            }
            // moreCertificates == FALSE when the end of the set has been reached.
        }//End while
    }
    if (NULL != certificatesInSignature) certificatesInSignature->Release();

```



Führen Sie die folgenden Schritte aus, um die digitale Signatur und das Zertifikat zu überprüfen, das zum Signieren des Dokuments verwendet wird:

1.  Suchen Sie das Signaturzertifikat durch Durchlaufen der Zertifikate, die von der Signatur verwendet werden.
2.  Testen Sie das Zertifikat, indem Sie die Signatur mit dem Zertifikat überprüfen. Das Signaturzertifikat wird gefunden, wenn [**die Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) -Methode einen [**XPS \_ -Signatur Status des \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status) **\_ \_ \_ gültigen XPS** -Signatur Status oder **XPS-Signatur Status " \_ \_ \_ fragwürdig**" zurückgibt und keinen Funktions **\_ Sicherheits** Fehler zurückgibt.


```C++
    // Reset the enumerator
    hr = signature->GetCertificateEnumerator(&certificatesInSignature);
    if (SUCCEEDED (hr))
    {
        moreCertificates = FALSE;
        hr = certificatesInSignature->MoveNext(&moreCertificates);
    }
    if (SUCCEEDED(hr))
    {
        // Iterate through the certificates in the signature,
        //  and call the IXpsSignature.Verify() method
        //  on each certificate.  
        // A signature can include an entire certificate chain, and so 
        //  only one of the certificates found in this enumeration 
        //  is the certificate that was used to sign the package. 
        //  The signing certificate is the one to authenticate.  
        // To find the signing certificate,  iterate through 
        //  the certificates in the signature and select the certificate that 
        //  returns an XPS_SIGNATURE_STATUS of XPS_SIGNATURE_STATUS_VALID
        //  or XPS_SIGNATURE_STATUS_QUESTIONABLE and does not return a
        //  FACILITY_SECURITY error.
        XPS_SIGNATURE_STATUS localSignatureStatus;
        localSignatureStatus = XPS_SIGNATURE_STATUS_INCOMPLIANT;
        do
        {
            PCCERT_CONTEXT certificate = NULL;
            DWORD certificateStatus = NULL;

            if (FAILED(hr = certificatesInSignature->GetCurrent(&certificate)))
            {
                // We will skip corrupted certificates
                // free this one and move to the next
                CertFreeCertificateContext (certificate);
                hr = certificatesInSignature->MoveNext(&moreCertificates);
                if (FAILED(hr))
                {
                    // ERROR: could not move to the next 
                    //  certificate in the enumerator
                    break; // out of do loop with failed hr
                }
                // continue with next loop iteration
                continue;
            }
            
            // Verify that the signature conforms to the XPS signing policy.
            hr = signature->Verify(certificate, &localSignatureStatus);
            if (FAILED(hr))
            {
                // If a FACILITY_SECURITY error code is returned, then the
                //  current certificate was not the signing certificate,
                //  so continue to the next certificate.
                if (HRESULT_FACILITY(hr) == FACILITY_SECURITY)
                {
                    // free this one and move to the next
                    CertFreeCertificateContext (certificate);
                    hr = certificatesInSignature->MoveNext(&moreCertificates);
                    if (FAILED(hr))
                    {
                        // ERROR: could not move to the next certificate 
                        //  in the enumerator
                        break; // out of do loop with failed hr
                    }
                    continue;
                }
                // ERROR: An attempt to verify the signature has failed
                break; // out of do loop with failed hr
            }
            // if verification was successful, localSignatureStatus will
            //  contain the status of the signature.
            //
            // do loop continues in next code example
```



Wenn das Signaturzertifikat gefunden wurde, führen Sie die folgenden Schritte aus:

1.  Speichert den zurückgegebenen Signatur Status.
2.  Aktualisieren Sie ggf. den lokalen Status, damit nachfolgende Zertifikat Tests durchgeführt werden:
    1.  Wenn der Signatur Status "erfolgreich" lautet, legen Sie den lokalen Status auf "fragwürdig" fest, um die Zertifikate zu testen.
    2.  Wenn der Signatur Status inkompatibel ist, belassen Sie den lokalen Status als nicht kompatibel.
    3.  Wenn der Signatur Status beschädigt oder unvollständig lautet, legen Sie den lokalen Status auf "beschädigt" fest.

Der Signatur Status "nicht **\_ \_ \_ kompatibel** " bedeutet, dass Teile des XPS-Dokuments, die nicht signiert werden sollten, signiert wurden oder Teile des XPS-Dokuments, die signiert werden sollten, nicht. Wenn die [**Überprüfung**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify) diesen Signatur Status zurückgibt, ist eine weitere Überprüfung der Signatur unnötig.


```C++
            // continuing do loop from previous code example
            *signingCertificate = certificate;
            *signatureStatus = localSignatureStatus;
            
            // note that this test should only downgrade the 
            // signature status, it should not upgrade it.
            switch (localSignatureStatus) {
                case XPS_SIGNATURE_STATUS_VALID:
                case XPS_SIGNATURE_STATUS_QUESTIONABLE:
                    // the signature is valid or questionable so
                    // save the actual status and set the new status
                    // to questionable so the certificates will be checked.
                    localSignatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    break;

                case XPS_SIGNATURE_STATUS_INCOMPLIANT:
                    // the signature is not compliant 
                    break;

                case XPS_SIGNATURE_STATUS_INCOMPLETE:
                case XPS_SIGNATURE_STATUS_BROKEN:
                    // The Windows 7 XPS viewer displays incomplete signatures
                    // and broken signatures as broken.
                    *signatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                    localSignatureStatus = XPS_SIGNATURE_STATUS_BROKEN;
                    break;

                default:
                    // there should be no other possible status values
                    break;
            }
            // do loop continues in next code example
```



Führen Sie die folgenden Schritte aus, um die Vertrauenswürdigkeit des Zertifikats zu überprüfen, wenn der Signatur Status gültig oder fragwürdig ist:

1.  Den Zertifikats Vertrauens Status erhalten.
2.  Wertet den zurückgegebenen Zertifikats Vertrauensstellungs Status aus.
3.  Gibt den resultierenden Status zurück.

Im nächsten Codebeispiel wird nicht auf jeden möglichen Zertifikats Vertrauensstellungs Status getestet. Weitere Informationen zu den Status Werten, die zurückgegeben werden können, finden Sie unter [**CERT \_ Trust \_ Status**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status).


```C++
            // continuing do loop from previous code example
            //
            // at this point, localSignatureStatus should be less than or 
            // equal to what it was before the test.

            // Check the certificate to see if it is valid
            if ((localSignatureStatus == XPS_SIGNATURE_STATUS_VALID) || 
                (localSignatureStatus == XPS_SIGNATURE_STATUS_QUESTIONABLE))
            {
                // This call builds the certificate trust chain from the 
                //  supplied certificate.  The certificate chain is used to
                //  authenticate the supplied certificate.
                hr = GetCertificateTrustStatus (
                    *signingCertificate, 
                    &signatureCertificateStore,
                    &certificateStatus);
                if (FAILED(hr))
                {
                    // ERROR: An attempt to authenticate the certificate 
                    //  has failed
                    break; // out of do loop with failed hr
                }

                // The Crypt API returns a status that can contain more than
                //  one status value.
                // statusFlagMask is set to test all bits except for the
                //  CERT_TRUST_REVOCATION_STATUS_UNKNOWN
                //  CERT_TRUST_IS_OFFLINE_REVOCATION
                //  CERT_TRUST_IS_NOT_TIME_VALID
                //  values because, for this test, these are not considered
                //  to be error conditions.
                DWORD statusFlagMask = ~(
                    CERT_TRUST_REVOCATION_STATUS_UNKNOWN | 
                    CERT_TRUST_IS_OFFLINE_REVOCATION | 
                    CERT_TRUST_IS_NOT_TIME_VALID);

                if (CERT_TRUST_NO_ERROR == (certificateStatus & statusFlagMask))
                {
                    // If *signatureStatus is already 
                    //    XPS_SIGNATURE_STATUS_VALID then there is no need to 
                    //    change the status as the certificate status has no 
                    //    certificate trust errors.
                    // If *signatureStatus is already 
                    //  XPS_SIGNATURE_STATUS_QUESTIONABLE then we will not
                    //  upgrade the trust status of the signature just 
                    //  because there is no trust issue with the certificate.
                }
                else
                {
                    // If trust errors were detected with the certificate, 
                    //  then this XPS signature is given a status of 
                    //  XPS_SIGNATURE_STATUS_QUESTIONABLE
                    *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                }

                // Handle additional certificate errors.  
                //  This is not an exhaustive list of possible errors.

                if (certificateStatus & CERT_TRUST_IS_NOT_TIME_VALID)
                {
                    // The XPS Viewer considers signatures with 
                    //  expired certificates as valid.
                }
                if (certificateStatus & CERT_TRUST_IS_PARTIAL_CHAIN)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }

                if (certificateStatus & CERT_TRUST_IS_NOT_SIGNATURE_VALID)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }

                if (certificateStatus & CERT_TRUST_IS_SELF_SIGNED)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }
                
                if (certificateStatus & CERT_TRUST_IS_UNTRUSTED_ROOT)
                {
                    // This test ensures that we only degrade the 
                    //  trust status and never upgrade it
                    if (XPS_SIGNATURE_STATUS_VALID == *signatureStatus)
                    {
                        *signatureStatus = XPS_SIGNATURE_STATUS_QUESTIONABLE;
                    }
                }
            }//End if

            hr = certificatesInSignature->MoveNext(&moreCertificates);
            if (FAILED(hr))
            {
                // ERROR: could not move to the next 
                //  certificate in the enumerator
                break; // out of do loop with failed hr
            }
        } while((*signatureStatus != XPS_SIGNATURE_STATUS_VALID) && 
                    moreCertificates);
    } // end if successful

    if (NULL != certificatesInSignature) certificatesInSignature->Release();

    return hr;
}
```



Im nächsten Codebeispiel wird der Zertifikat Vertrauensstellungs Status durch Aufrufen der-Methode abgerufen, die im folgenden Codebeispiel gezeigt wird.


```C++
HRESULT GetCertificateTrustStatus(
    __in PCCERT_CONTEXT certificate,
    __in HCERTSTORE* certificateStore,
    __out DWORD* certificateStatus
)
{
    HRESULT    hr = S_OK;

    // The certificate chain that will be created from 
    //  the PCCERT_CONTEXT object passed in.  
    PCCERT_CHAIN_CONTEXT    certificateChain =    NULL;

    hr = CreateCertificateChain(
        certificate, 
        *certificateStore, 
        &certificateChain);

    if (SUCCEEDED(hr)) { 
        *certificateStatus = 
            certificateChain->TrustStatus.dwErrorStatus;
    }

    return hr;
}
```



Die im vorangehenden Codebeispiel verwendete Zertifikat Kette wird erstellt, indem die im folgenden Codebeispiel gezeigte-Methode aufgerufen wird.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**In diesem Abschnitt verwendet**
</dt> <dt>

[**Zertifikat \_ Ketten \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_chain_context)
</dt> <dt>

[**CERT- \_ Kontext**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_context)
</dt> <dt>

[**CERT \_ Trust- \_ Status**](/windows/desktop/api/wincrypt/ns-wincrypt-cert_trust_status)
</dt> <dt>

[**Certaddcertificatcher econtextto Store**](/windows/desktop/api/wincrypt/nf-wincrypt-certaddcertificatecontexttostore)
</dt> <dt>

[**CertOpenStore übergebene**](/windows/desktop/api/wincrypt/nf-wincrypt-certopenstore)
</dt> <dt>

[**CertGetCertificateChain dokumentiert**](/windows/desktop/api/wincrypt/nf-wincrypt-certgetcertificatechain)
</dt> <dt>

[**Iopccertificateenumerator**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopccertificateenumerator)
</dt> <dt>

[**Iopccertificateenumerator:: GetCurrent**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-getcurrent)
</dt> <dt>

[**Iopccertificateenumerator:: "muvenext"**](/previous-versions/windows/desktop/api/msopc/nf-msopc-iopccertificateenumerator-movenext)
</dt> <dt>

[**Ixpssignature**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignature)
</dt> <dt>

[**Ixpssignature:: getcertificateenumerator**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-getcertificateenumerator)
</dt> <dt>

[**Ixpssignature:: Verify**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignature-verify)
</dt> <dt>

[**Ixpssignaturückruf**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturecollection)
</dt> <dt>

[**Ixpssignatuerinnerungs:: GetAt**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getat)
</dt> <dt>

[**Ixpssignatuerinnerungs:: GetCount**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturecollection-getcount)
</dt> <dt>

[**Ixpssignaturemanager**](/windows/desktop/api/xpsdigitalsignature/nn-xpsdigitalsignature-ixpssignaturemanager)
</dt> <dt>

[**Ixpssignaturemanager:: getsignaturen**](/windows/desktop/api/xpsdigitalsignature/nf-xpsdigitalsignature-ixpssignaturemanager-getsignatures)
</dt> <dt>

[**Status der XPS- \_ Signatur \_**](/windows/win32/api/xpsdigitalsignature/ne-xpsdigitalsignature-xps_signature_status)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Einbinden von Zertifikat Ketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

[XPS-Fehler bei der digitalen Signatur-API](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS-Dokument Fehler](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
