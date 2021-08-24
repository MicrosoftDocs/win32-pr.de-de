---
description: In diesem Thema wird beschrieben, wie Sie ein Zertifikat aus einer Zertifikatdatei laden.
ms.assetid: 60cced55-9fcc-4fce-a462-7abf3f4466f0
title: Laden eines Zertifikats aus einer Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e73161b133fec74478643baa8453421130b3f3ad18ff4e75429d79b3312919b5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119099094"
---
# <a name="load-a-certificate-from-a-file"></a>Laden eines Zertifikats aus einer Datei

In diesem Thema wird beschrieben, wie Sie ein Zertifikat aus einer Zertifikatdatei laden.

So laden Sie ein Zertifikat aus einer Zertifikatdatei

1.  Öffnen Sie die Zertifikatdatei für den Lesezugriff.
2.  Lesen Sie den Inhalt der Zertifikatdatei in den Zertifikatpuffer.
3.  Erstellen Sie ein Zertifikat mit dem Inhalt des Puffers.


```C++
// In the interest of simplicity, this example
//  uses a fixed-length buffer to hold the certificate. 
// A more robust solution would be to query the size
//  of the certificate file and dynamically
//  allocate a buffer of that size or greater.
#define CERTIFICATE_BUFFER_SIZE 1024

HRESULT  hr                  = S_OK;
BYTE     certEncoded[CERTIFICATE_BUFFER_SIZE] = {0};
DWORD    certEncodedSize     = 0L;
HANDLE   certFileHandle      = NULL;
BOOL     result              = FALSE;

// open the certificate file
certFileHandle = CreateFile(certFile, 
    GENERIC_READ, 
    0, 
    NULL, 
    OPEN_EXISTING, 
    FILE_ATTRIBUTE_NORMAL, 
    NULL);
if (INVALID_HANDLE_VALUE == certFileHandle) {
    hr = HRESULT_FROM_WIN32(GetLastError());
}

if (SUCCEEDED(hr)) {
    // if the buffer is large enough
    //  read the certificate file into the buffer
    if (GetFileSize (certFileHandle, NULL) <= CERTIFICATE_BUFFER_SIZE) {
        result = ReadFile(certFileHandle, 
            certEncoded, 
            CERTIFICATE_BUFFER_SIZE, 
            &certEncodedSize, 
            NULL);
        if (!result) {
            // the read failed, return the error as an HRESULT
            hr = HRESULT_FROM_WIN32(GetLastError());
        } else {
            hr = S_OK;
        }
    } else {
        // The certificate file is larger than the allocated buffer.
        //  To handle this error, you could dynamically allocate
        //  the certificate buffer based on the file size returned or 
        //  use a larger static buffer.
        hr = HRESULT_FROM_WIN32(ERROR_MORE_DATA);
    }    
}
if (SUCCEEDED(hr))
{
    // create a certificate from the contents of the buffer
    *cert = CertCreateCertificateContext(X509_ASN_ENCODING, 
        certEncoded, 
        certEncodedSize);
    if (!(*cert)) {
        hr = HRESULT_FROM_WIN32(GetLastError());
        CloseHandle(certFileHandle);
        hr = E_FAIL;
    } else {
        hr = S_OK;
    }
}
// close the certificate file
if (NULL != certFileHandle) CloseHandle(certFileHandle);
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Überprüfen, ob das System eine Digestmethode unterstützt](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Überprüfen, ob ein Zertifikat eine Signaturmethode unterstützt](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Einbetten von Zertifikatketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Wird in diesem Beispiel verwendet**
</dt> <dt>

[**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea)
</dt> <dt>

[**ReadFile**](/windows/desktop/api/fileapi/nf-fileapi-readfile)
</dt> <dt>

[**CertCreateCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certcreatecertificatecontext)
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Kryptografie-API](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Kryptografiefunktionen](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[XPS Digital Signature-API-Fehler](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS-Dokumentfehler](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
