---
description: In diesem Thema wird beschrieben, wie überprüft wird, ob das System eine Digest-Methode unterstützt.
ms.assetid: dd1b53cd-66b9-46b3-89ad-ee84b4690e1e
title: Überprüfen, ob das System eine Digest-Methode unterstützt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9acf3e0c2c7f4927fc6047c88039e443e2db3e71
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868015"
---
# <a name="verify-the-system-supports-a-digest-method"></a>Überprüfen, ob das System eine Digest-Methode unterstützt

In diesem Thema wird beschrieben, wie überprüft wird, ob das System eine Digest-Methode unterstützt.

Digitale XPS-Signaturen verwenden die Crypto-API, die Methoden bereitstellt, um zu überprüfen, ob das System eine bestimmte Digest-Methode unterstützt. Um die Funktion " **cryptxmlenumalgorithminfo** " der kryptografieapi zum Auflisten der vom System unterstützten Digest-Methoden zu verwenden, muss der Aufrufer eine Rückruf Methode und eine Datenstruktur bereitstellen. Die Funktion " **cryptxmlenumalgorithminfo** " übergibt die Enumerationsdaten über die Rückruf Methode an den Aufrufer zurück.

Die in diesem Beispiel verwendete Datenstruktur ist im folgenden Codebeispiel dargestellt und enthält die folgenden Felder:

| Feld                            | BESCHREIBUNG                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| **userdigestalgorithm**          | Ein **LPWSTR** -Feld, das auf die Zeichenfolge verweist, die den URI des zu überprüfenden Digest-Algorithmus enthält. |
| **userdigestalgorithmsupported** | Ein **boolescher** Wert, der angibt, ob der Digest-Algorithmus vom Zertifikat unterstützt wird.           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



Die Crypto-API-Methode, die die Digest-Methoden auflistet, verwendet eine Rückruf Methode, um Daten an den Aufrufer zurückzugeben. **Cryptxmlenumalgorithminfo** listet die Digest-Methoden auf, die vom System unterstützt werden, und ruft die Rückruf Methode für jede aufgeführte Digest-Methode auf, bis die Rückruf Methode **false** zurückgibt oder alle vom System unterstützten Digest-Methoden aufgelistet werden. Die Rückruf Methode in diesem Beispiel vergleicht die von **cryptxmlenumschlag** -Methode übergebenen Digest-Methode mit der Digest-Methode, die von der aufrufenden Methode bereitgestellt wird.


```C++
BOOL WINAPI 
EnumDigestMethodCallback (
    __in   const CRYPT_XML_ALGORITHM_INFO *certMethodInfo,
    __inout_opt  void                     *userArg
)
{
    // MAX_ALG_ID_LEN is used to set the maximum length of the 
    // algorithm URI in the string comparison. The URI is not 
    // likely to be longer than 128 characters so a fixed-size
    // buffer is used in this example.
    // To make this function more robust, consider
    // setting this value dynamically.
    static const  size_t MAX_ALG_ID_LEN = 128;
    DigestMethodData   *certificateAlgorithmData = 
        (DigestMethodData*)userArg;

    if (NULL != userArg) {
        // Assign user data to local data structure
        certificateAlgorithmData = (DigestMethodData*)userArg;
    } else {
        // Unable to continue this enumeration without 
        //  data from calling method.
        return FALSE;
    }
    
    // For each algorithm in the enumeration, check to see 
    //  if the URI of the current supported algorithm matches 
    //  the URI passed in userArg.
    int cmpResult = 0;
    cmpResult = wcsncmp( 
        certMethodInfo->wszAlgorithmURI, 
        certificateAlgorithmData->userDigestAlgorithm, 
        MAX_ALG_ID_LEN );

    if ( 0 == cmpResult )
    {
        // This is a match...
        //  set supported value to true
        certificateAlgorithmData->userDigestAlgorithmSupported = TRUE;
        //  ...and return FALSE to stop any further enumeration
        return FALSE;
    } 
    else
    {
        // no match was found
        // return TRUE to continue enumeration
        return TRUE;
    }
}
```



Das folgende Codebeispiel umschließt die Validierungs Funktionen in eine einzelne-Methode, die einen **booleschen** Wert zurückgibt, der angibt, ob das System die Digest-Methode unterstützt.


```C++
BOOL 
SupportsDigestAlgorithm (
    __in LPCWSTR digestMethodToCheck
)
{
    HRESULT  hr = S_OK;

    // Initialize the structure that will hold information about the 
    //  digest method to check
    DigestMethodData  certificateAlgorithmData;

    certificateAlgorithmData.userDigestAlgorithmSupported = FALSE;
    certificateAlgorithmData.userDigestAlgorithm = digestMethodToCheck;

    // Enumerate the algorithms that are supported on the system, 
    //  the callback method compares each supported algorithm to the one
    //  passed in digestMethodToCheck and returns true in the
    //  certificateAlgorithmData.userDigestAlgorithmSupported field if
    //  the provided digest algorithm is supported by system.
    //
    // Note that CRYPT_XML_GROUP_ID_HASH is set to enumerate 
    //  digest methods
    hr = CryptXmlEnumAlgorithmInfo(
        CRYPT_XML_GROUP_ID_HASH,       // NOTE: CRYPT_XML_GROUP_ID_HASH
        CRYPT_XML_FLAG_DISABLE_EXTENSIONS,
        (void*)&certificateAlgorithmData,
        EnumDigestMethodCallback);

    return certificateAlgorithmData.userDigestAlgorithmSupported;
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

[Einbinden von Zertifikat Ketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**In diesem Beispiel verwendet**
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

 

 
