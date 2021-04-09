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
# <a name="verify-the-system-supports-a-digest-method"></a><span data-ttu-id="79e82-103">Überprüfen, ob das System eine Digest-Methode unterstützt</span><span class="sxs-lookup"><span data-stu-id="79e82-103">Verify the System Supports a Digest Method</span></span>

<span data-ttu-id="79e82-104">In diesem Thema wird beschrieben, wie überprüft wird, ob das System eine Digest-Methode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79e82-104">This topic describes how to verify that the system supports a digest method.</span></span>

<span data-ttu-id="79e82-105">Digitale XPS-Signaturen verwenden die Crypto-API, die Methoden bereitstellt, um zu überprüfen, ob das System eine bestimmte Digest-Methode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79e82-105">XPS Digital Signatures use the Crypto API, which provides methods for verifying that the system supports a specific digest method.</span></span> <span data-ttu-id="79e82-106">Um die Funktion " **cryptxmlenumalgorithminfo** " der kryptografieapi zum Auflisten der vom System unterstützten Digest-Methoden zu verwenden, muss der Aufrufer eine Rückruf Methode und eine Datenstruktur bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="79e82-106">To use the Crypto API's **CryptXmlEnumAlgorithmInfo** function to enumerate the digest methods that are supported by the system, the caller must provide a callback method and a data structure.</span></span> <span data-ttu-id="79e82-107">Die Funktion " **cryptxmlenumalgorithminfo** " übergibt die Enumerationsdaten über die Rückruf Methode an den Aufrufer zurück.</span><span class="sxs-lookup"><span data-stu-id="79e82-107">The **CryptXmlEnumAlgorithmInfo** function passes the enumeration data back to the caller by way of the callback method.</span></span>

<span data-ttu-id="79e82-108">Die in diesem Beispiel verwendete Datenstruktur ist im folgenden Codebeispiel dargestellt und enthält die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="79e82-108">The data structure used in this example is shown in the following code example and contains the following fields:</span></span>

| <span data-ttu-id="79e82-109">Feld</span><span class="sxs-lookup"><span data-stu-id="79e82-109">Field</span></span>                            | <span data-ttu-id="79e82-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="79e82-110">Description</span></span>                                                                                                |
|----------------------------------|------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="79e82-111">**userdigestalgorithm**</span><span class="sxs-lookup"><span data-stu-id="79e82-111">**userDigestAlgorithm**</span></span>          | <span data-ttu-id="79e82-112">Ein **LPWSTR** -Feld, das auf die Zeichenfolge verweist, die den URI des zu überprüfenden Digest-Algorithmus enthält.</span><span class="sxs-lookup"><span data-stu-id="79e82-112">An **LPWSTR** field that points to the string that contains the URI of the digest algorithm to be checked.</span></span> |
| <span data-ttu-id="79e82-113">**userdigestalgorithmsupported**</span><span class="sxs-lookup"><span data-stu-id="79e82-113">**userDigestAlgorithmSupported**</span></span> | <span data-ttu-id="79e82-114">Ein **boolescher** Wert, der angibt, ob der Digest-Algorithmus vom Zertifikat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="79e82-114">A **Boolean** value that indicates whether the digest algorithm is supported by the certificate.</span></span>           |



 


```C++
struct DigestMethodData
{
    LPCWSTR userDigestAlgorithm; 
    BOOL    userDigestAlgorithmSupported;
};
```



<span data-ttu-id="79e82-115">Die Crypto-API-Methode, die die Digest-Methoden auflistet, verwendet eine Rückruf Methode, um Daten an den Aufrufer zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="79e82-115">The Crypto API method that enumerates the digest methods uses a callback method to return data to the caller.</span></span> <span data-ttu-id="79e82-116">**Cryptxmlenumalgorithminfo** listet die Digest-Methoden auf, die vom System unterstützt werden, und ruft die Rückruf Methode für jede aufgeführte Digest-Methode auf, bis die Rückruf Methode **false** zurückgibt oder alle vom System unterstützten Digest-Methoden aufgelistet werden.</span><span class="sxs-lookup"><span data-stu-id="79e82-116">**CryptXmlEnumAlgorithmInfo** enumerates the digest methods that are supported by the system, and it calls the callback method for each digest method that it enumerates, until the callback method returns **FALSE** or until all digest methods supported by the system are enumerated.</span></span> <span data-ttu-id="79e82-117">Die Rückruf Methode in diesem Beispiel vergleicht die von **cryptxmlenumschlag** -Methode übergebenen Digest-Methode mit der Digest-Methode, die von der aufrufenden Methode bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="79e82-117">The callback method in this example compares the digest method that is passed in by **CryptXmlEnumAlgorithmInfo** with the digest method provided by the calling method.</span></span>


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



<span data-ttu-id="79e82-118">Das folgende Codebeispiel umschließt die Validierungs Funktionen in eine einzelne-Methode, die einen **booleschen** Wert zurückgibt, der angibt, ob das System die Digest-Methode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="79e82-118">The following code sample wraps the validation functionality into a single method, which returns a **Boolean** value that indicates whether the system supports the digest method.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="79e82-119">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="79e82-119">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="79e82-120">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="79e82-120">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="79e82-121">Laden eines Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="79e82-121">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="79e82-122">Überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt</span><span class="sxs-lookup"><span data-stu-id="79e82-122">Verify That a Certificate Supports a Signature Method</span></span>](verify-a-certificate-supports-a-signature-method.md)
</dt> <dt>

[<span data-ttu-id="79e82-123">Einbinden von Zertifikat Ketten in ein Dokument</span><span class="sxs-lookup"><span data-stu-id="79e82-123">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="79e82-124">**In diesem Beispiel verwendet**</span><span class="sxs-lookup"><span data-stu-id="79e82-124">**Used in This Example**</span></span>
</dt> <dt>

<span data-ttu-id="79e82-125">**Cryptxmlenenalgorithminfo**</span><span class="sxs-lookup"><span data-stu-id="79e82-125">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="79e82-126">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="79e82-126">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="79e82-127">Kryptografieapi</span><span class="sxs-lookup"><span data-stu-id="79e82-127">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="79e82-128">Kryptografiefunktionen</span><span class="sxs-lookup"><span data-stu-id="79e82-128">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="79e82-129">XPS-Fehler bei der digitalen Signatur-API</span><span class="sxs-lookup"><span data-stu-id="79e82-129">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="79e82-130">XPS-Dokument Fehler</span><span class="sxs-lookup"><span data-stu-id="79e82-130">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="79e82-131">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="79e82-131">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
