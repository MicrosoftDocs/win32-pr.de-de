---
description: In diesem Thema wird beschrieben, wie Sie überprüfen, ob das System eine Digestmethode unterstützt.
ms.assetid: dd1b53cd-66b9-46b3-89ad-ee84b4690e1e
title: Überprüfen, ob das System eine Digestmethode unterstützt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 272db3f7169ba66fdaa67c2943030d53e7c75927c2024750d405aa9a8246949e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119600300"
---
# <a name="verify-the-system-supports-a-digest-method"></a>Überprüfen, ob das System eine Digestmethode unterstützt

In diesem Thema wird beschrieben, wie Sie überprüfen, ob das System eine Digestmethode unterstützt.

XPS Digital Signatures verwendet die Kryptografie-API, die Methoden zur Überprüfung bereitstellt, ob das System eine bestimmte Digestmethode unterstützt. Um die **CryptXmlEnumAlgorithmInfo-Funktion** der Crypto-API zum Auflisten der digest-Methoden zu verwenden, die vom System unterstützt werden, muss der Aufrufer eine Rückrufmethode und eine Datenstruktur bereitstellen. Die **CryptXmlEnumAlgorithmInfo-Funktion** übergibt die Enumerationsdaten über die Rückrufmethode zurück an den Aufrufer.

Die in diesem Beispiel verwendete Datenstruktur wird im folgenden Codebeispiel gezeigt und enthält die folgenden Felder:

| Feld                            | Beschreibung                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| **userDigestAlgorithm**          | Ein **LPWSTR-Feld,** das auf die Zeichenfolge zeigt, die den URI des zu überprüfenden Digestalgorithmus enthält. |
| **userDigestAlgorithmSupported** | Ein **boolescher** Wert, der angibt, ob der Digestalgorithmus vom Zertifikat unterstützt wird.           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



Die Crypto-API-Methode, die die Digestmethoden aufzählt, verwendet eine Rückrufmethode, um Daten an den Aufrufer zurückzugeben. **CryptXmlEnumAlgorithmInfo** listet die vom System unterstützten Digestmethoden auf und ruft die Rückrufmethode für jede Digestmethode auf, die sie aufzählt, bis die Rückrufmethode **FALSE** zurückgibt oder bis alle vom System unterstützten Digestmethoden aufzählt werden. Die Rückrufmethode in diesem Beispiel vergleicht die digest-Methode, die von **CryptXmlEnumAlgorithmInfo** übergeben wird, mit der digest-Methode, die von der aufrufenden Methode bereitgestellt wird.


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



Das folgende Codebeispiel umschließt die Validierungsfunktionalität in eine einzelne Methode, die einen **booleschen** Wert zurückgibt, der angibt, ob das System die Digestmethode unterstützt.


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

[Überprüfen, ob ein Zertifikat eine Signaturmethode unterstützt](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[Einbetten von Zertifikatketten in ein Dokument](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

**In diesem Beispiel verwendet**
</dt> <dt>

**CryptXmlEnumAlgorithmInfo**
</dt> <dt>

**Weitere Informationen**
</dt> <dt>

[Kryptografie-API](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[Kryptografiefunktionen](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[Fehler bei der API für digitale XPS-Signaturen](xps-digital-signatures-errors.md)
</dt> <dt>

[XPS-Dokumentfehler](xps-document-errors.md)
</dt> <dt>

[XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
