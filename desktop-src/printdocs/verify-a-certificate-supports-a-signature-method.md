---
description: In diesem Thema wird beschrieben, wie überprüft wird, ob ein Zertifikat eine bestimmte Signaturmethode unterstützt.
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: Überprüfen, ob ein Zertifikat eine Signaturmethode unterstützt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 177859dd78d30ee9f9147cee7ca01311ed95c0733115cd939dde8aa6ec70f5b9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119098712"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a>Überprüfen, ob ein Zertifikat eine Signaturmethode unterstützt

In diesem Thema wird beschrieben, wie überprüft wird, ob ein Zertifikat eine bestimmte Signaturmethode unterstützt.

Die **CryptXmlEnumAlgorithmInfo** in der Microsoft Crypto-API enumeriert die Eigenschaften eines Zertifikats und wird in diesem Codebeispiel zum Aufzählen der Signaturmethoden verwendet, die das Zertifikat unterstützt. Um **CryptXmlEnumAlgorithmInfo** zum Aufzählen der signaturmethoden zu verwenden, die das Zertifikat unterstützt, muss der Aufrufer eine Rückrufmethode und eine Datenstruktur im Aufruf von **CryptXmlEnumAlgorithmInfo** bereitstellen, sodass daten an die Rückrufmethode übergeben werden können.

Die im nächsten Codebeispiel verwendete Datenstruktur enthält die folgenden Felder:

| Feld                               | Beschreibung                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **userSignatureAlgorithmToCheck**   | Ein **LPWSTR-Feld,** das auf die Zeichenfolge zeigt, die den URI des zu überprüfenden Signaturalgorithmus enthält.                             |
| **certificateAlgorithmInfo**        | Ein Zeiger auf eine **\_ CRYPT-OID-INFO-Struktur, \_** die Informationen zu einem Signaturalgorithmus enthält, der vom Zertifikat unterstützt wird. |
| **userSignatureAlgorithmSupported** | Ein **boolescher Wert,** der angibt, ob der Signaturalgorithmus vom Zertifikat unterstützt wird.                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



Die Crypto-API-Methode, die das Zertifikat überprüft, verwendet eine Rückrufmethode, um Daten an den Aufrufer zurück zu geben. **CryptXmlEnumAlgorithmInfo** aufzählt die Signaturmethoden, die das Zertifikat unterstützt, und ruft die Rückrufmethode für jede Signaturmethode auf, bis die Rückrufmethode **FALSE** zurückgibt oder bis alle Signaturmethoden im Zertifikat aufzählt wurden.

Die Rückrufmethode im nächsten Codebeispiel sucht nach einer Signaturmethode, die von **CryptXmlEnumAlgorithmInfo** übergeben wird und der signaturmethode entspricht, die von der aufrufenden Methode bereitgestellt wird. Wenn eine Übereinstimmung gefunden wird, überprüft die Rückrufmethode, ob die Signaturmethode auch vom System unterstützt wird. Wenn die Signaturmethoden übereinstimmen und vom System unterstützt werden, wird die Signaturmethode als vom System unterstützt markiert, und die Rückrufmethode gibt **FALSE zurück.**


```C++
BOOL WINAPI 
EnumSignatureMethodCallback (
    __in const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt void *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, you might consider
    // setting this value dynamically.
    static const size_t MAX_ALG_ID_LEN = 128;
    SignatureMethodData *certificateAlgorithmData = NULL;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (SignatureMethodData*)userArg;
    } else {
        // Unable to continue this enumeration 
        //   without data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see if the URI 
    //  of the algorithm supported by the certificate matches the URI 
    //  of the algorithm being tested.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userSignatureAlgorithmToCheck, 
        MAX_ALG_ID_LEN );
    if ( 0 == cmpResult )
    {
        // This is a match...
        // Check to see if the algorithm supported by the 
        //  certificate matches any of the supported algorithms 
        //  on the system.
        cmpResult = wcsncmp(
            certMethodInfo->wszCNGExtraAlgid, 
            certificateAlgorithmData->certificateAlgorithmInfo->pwszCNGAlgid, 
            MAX_ALG_ID_LEN );
        if ( 0 == cmpResult )
        {
            // This is also a match so set the field in the data structure
            //   provided by the calling method.
            certificateAlgorithmData->userSignatureAlgorithmSupported = TRUE;
            // A match was found so there is no point in continuing 
            //  the enumeration.
            return FALSE;
        }
    }
    // The enumeration stops when the callback method returns FALSE. 
    //   If here, then return TRUE because a matching algorithm has
    //   not been found.
    return TRUE;
}
```



Im folgenden Codebeispiel wird die Validierungsfunktion in eine einzelne Methode umschließen. Diese Methode gibt einen **booleschen Wert** zurück, der angibt, ob das Zertifikat die Signaturmethode unterstützt und ob die Signaturmethode vom System unterstützt wird.


```C++
BOOL 
SupportsSignatureAlgorithm (
    __in LPCWSTR signingMethodToCheck,
    __in PCCERT_CONTEXT certificateToCheck
)
{
    HRESULT     hr = S_OK;

    // Initialize the structure that contains the   
    //  information about the signature algorithm to check
    SignatureMethodData        certificateAlgorithmData;

    certificateAlgorithmData.userSignatureAlgorithmSupported = 
        FALSE;
    certificateAlgorithmData.userSignatureAlgorithmToCheck = 
        signingMethodToCheck;

    // Call the crypt API to get information about the algorithms
    //   that are supported by the certificate and initialize 
    //   certificateAlgorithmData
    certificateAlgorithmData.certificateAlgorithmInfo = CryptFindOIDInfo (
        CRYPT_OID_INFO_OID_KEY,
        certificateToCheck->pCertInfo->SubjectPublicKeyInfo.Algorithm.pszObjId,
        CRYPT_PUBKEY_ALG_OID_GROUP_ID | CRYPT_OID_PREFER_CNG_ALGID_FLAG);

    if (certificateAlgorithmData.certificateAlgorithmInfo != NULL)
    {
        // Enumerate the algorithms that are supported by the 
        //   certificate, and use our callback method to determine if
        //   the user supplied signature algorithm is supported by 
        //     the certificate.
        //
        // Note that CRYPT_XML_GROUP_ID_SIGN is used to enumerate
        //  the signature methods
        hr = CryptXmlEnumAlgorithmInfo(
            CRYPT_XML_GROUP_ID_SIGN,  // NOTE: CRYPT_XML_GROUP_ID_SIGN
            CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
            (void*)&certificateAlgorithmData,
            EnumSignatureMethodCallback);
        // when the enumeration has returned successfully, 
        //  certificateAlgorithmData.userSignatureAlgorithmSupported
        //  will be TRUE if the signing method is supported by
        //  the certificate
    }
    return certificateAlgorithmData.userSignatureAlgorithmSupported;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Next Steps**
</dt> <dt>

[Laden eines Zertifikats aus einer Datei](load-a-certificate-from-a-file.md)
</dt> <dt>

[Überprüfen, ob das System eine Digestmethode unterstützt](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Einbetten von Zertifikatketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**Wird in diesem Beispiel verwendet**
</dt> <dt>

[**CryptFindOIDInfo**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[**CRYPT \_ OID \_ INFO**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

**CryptXmlEnumAlgorithmInfo**
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

 

 
