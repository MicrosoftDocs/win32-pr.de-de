---
description: In diesem Thema wird beschrieben, wie Sie überprüfen, ob ein Zertifikat eine bestimmte Signatur Methode unterstützt.
ms.assetid: c7a23ace-4e9c-4de2-994e-2aa9c70a30b6
title: Überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27da9ae31c3cf0c4e453a5507d93d1505606e859
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868012"
---
# <a name="verify-that-a-certificate-supports-a-signature-method"></a>Überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt

In diesem Thema wird beschrieben, wie Sie überprüfen, ob ein Zertifikat eine bestimmte Signatur Methode unterstützt.

Der **cryptxmlenumalgorithminfo** in der kryptografieapi von Microsoft listet die Eigenschaften eines Zertifikats auf und wird in diesem Codebeispiel verwendet, um die Signatur Methoden aufzulisten, die das Zertifikat unterstützt. Um **cryptxmlenumalgorithminfo** zum Auflisten der Signatur Methoden zu verwenden, die das Zertifikat unterstützt, muss der Aufrufer eine Rückruf Methode und eine Datenstruktur im Aufruf von **cryptxmlenumalgorithminfo** bereitstellen, sodass Daten an die Rückruf Methode übergeben werden können.

Die im nächsten Codebeispiel verwendete Datenstruktur verfügt über die folgenden Felder:

| Feld                               | BESCHREIBUNG                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| **usersignaturealgorithmzu Check**   | Ein **LPWSTR** -Feld, das auf die Zeichenfolge verweist, die den URI des Signatur Algorithmus enthält, der geprüft werden soll.                             |
| **certificatealgorithminfo**        | Ein Zeiger auf eine **crypt- \_ OID \_** -Informationsstruktur, die Informationen über einen Signatur Algorithmus enthält, der vom Zertifikat unterstützt wird. |
| **usersignaturealgorithmsupported** | Ein **boolescher** Wert, der angibt, ob der Signatur Algorithmus vom Zertifikat unterstützt wird.                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



Die kryptografieapi-Methode, die das Zertifikat überprüft, verwendet eine Rückruf Methode, um Daten an den Aufrufer zurückzugeben **Cryptxmlenumalgorithminfo** listet die Signatur Methoden auf, die das Zertifikat unterstützt, und ruft die Rückruf Methode für jede Signatur Methode auf, bis die Rückruf Methode **false** zurückgibt oder alle Signatur Methoden im Zertifikat aufgezählt wurden.

Die Rückruf Methode im nächsten Codebeispiel sucht nach einer Signatur Methode, die von **cryptxmlenenalgorithminfo** übergangen wird und mit der Signatur Methode übereinstimmt, die von der aufrufenden Methode bereitgestellt wird. Wenn eine Entsprechung gefunden wird, überprüft die Rückruf Methode, ob die Signatur Methode auch vom System unterstützt wird. Wenn die Signatur Methoden Stimmen und vom System unterstützt werden, wird die Signatur Methode als vom System unterstützt gekennzeichnet, und die Rückruf Methode gibt **false** zurück.


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



Im folgenden Codebeispiel wird die Validierungsfunktion in eine einzelne Methode umschlossen. Diese Methode gibt einen **booleschen** Wert zurück, der angibt, ob das Zertifikat die Signatur Methode unterstützt und ob die Signatur Methode vom System unterstützt wird.


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

[Überprüfen, ob das System eine Digest-Methode unterstützt](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[Einbinden von Zertifikat Ketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**In diesem Beispiel verwendet**
</dt> <dt>

[**Cryptfindoidinfo**](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[**Crypt- \_ OID- \_ Informationen**](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

**Cryptxmlenenalgorithminfo**
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Kryptografieapi](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Kryptografiefunktionen](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[XPS-Fehler bei der digitalen Signatur-API](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS-Dokument Fehler](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
