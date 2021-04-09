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
# <a name="verify-that-a-certificate-supports-a-signature-method"></a><span data-ttu-id="5c3aa-103">Überprüfen, ob ein Zertifikat eine Signatur Methode unterstützt</span><span class="sxs-lookup"><span data-stu-id="5c3aa-103">Verify That a Certificate Supports a Signature Method</span></span>

<span data-ttu-id="5c3aa-104">In diesem Thema wird beschrieben, wie Sie überprüfen, ob ein Zertifikat eine bestimmte Signatur Methode unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-104">This topic describes how to verify that a certificate supports a specific signature method.</span></span>

<span data-ttu-id="5c3aa-105">Der **cryptxmlenumalgorithminfo** in der kryptografieapi von Microsoft listet die Eigenschaften eines Zertifikats auf und wird in diesem Codebeispiel verwendet, um die Signatur Methoden aufzulisten, die das Zertifikat unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-105">The **CryptXmlEnumAlgorithmInfo** in the Microsoft Crypto API enumerates the properties of a certificate and is used in this code example to enumerate the signature methods that the certificate supports.</span></span> <span data-ttu-id="5c3aa-106">Um **cryptxmlenumalgorithminfo** zum Auflisten der Signatur Methoden zu verwenden, die das Zertifikat unterstützt, muss der Aufrufer eine Rückruf Methode und eine Datenstruktur im Aufruf von **cryptxmlenumalgorithminfo** bereitstellen, sodass Daten an die Rückruf Methode übergeben werden können.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-106">To use **CryptXmlEnumAlgorithmInfo** to enumerate the signature methods that the certificate supports, the caller must provide a callback method and a data structure in the call to **CryptXmlEnumAlgorithmInfo**, allowing it to pass data to the callback method.</span></span>

<span data-ttu-id="5c3aa-107">Die im nächsten Codebeispiel verwendete Datenstruktur verfügt über die folgenden Felder:</span><span class="sxs-lookup"><span data-stu-id="5c3aa-107">The data structure used in the next code example has the following fields:</span></span>

| <span data-ttu-id="5c3aa-108">Feld</span><span class="sxs-lookup"><span data-stu-id="5c3aa-108">Field</span></span>                               | <span data-ttu-id="5c3aa-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5c3aa-109">Description</span></span>                                                                                                                               |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5c3aa-110">**usersignaturealgorithmzu Check**</span><span class="sxs-lookup"><span data-stu-id="5c3aa-110">**userSignatureAlgorithmToCheck**</span></span>   | <span data-ttu-id="5c3aa-111">Ein **LPWSTR** -Feld, das auf die Zeichenfolge verweist, die den URI des Signatur Algorithmus enthält, der geprüft werden soll.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-111">An **LPWSTR** field that points to the string that contains the URI of the signature algorithm to be checked.</span></span>                             |
| <span data-ttu-id="5c3aa-112">**certificatealgorithminfo**</span><span class="sxs-lookup"><span data-stu-id="5c3aa-112">**certificateAlgorithmInfo**</span></span>        | <span data-ttu-id="5c3aa-113">Ein Zeiger auf eine **crypt- \_ OID \_** -Informationsstruktur, die Informationen über einen Signatur Algorithmus enthält, der vom Zertifikat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-113">A pointer to a **CRYPT\_OID\_INFO** structure that contains information about a signature algorithm that is supported by the certificate.</span></span> |
| <span data-ttu-id="5c3aa-114">**usersignaturealgorithmsupported**</span><span class="sxs-lookup"><span data-stu-id="5c3aa-114">**userSignatureAlgorithmSupported**</span></span> | <span data-ttu-id="5c3aa-115">Ein **boolescher** Wert, der angibt, ob der Signatur Algorithmus vom Zertifikat unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-115">A **Boolean** value that indicates whether the signature algorithm is supported by the certificate.</span></span>                                       |



 


```C++
struct SignatureMethodData
{
    LPCWSTR             userSignatureAlgorithmToCheck; 
    PCCRYPT_OID_INFO    certificateAlgorithmInfo; 
    BOOL                userSignatureAlgorithmSupported; 
};
```



<span data-ttu-id="5c3aa-116">Die kryptografieapi-Methode, die das Zertifikat überprüft, verwendet eine Rückruf Methode, um Daten an den Aufrufer zurückzugeben</span><span class="sxs-lookup"><span data-stu-id="5c3aa-116">The Crypto API method that checks the certificate uses a callback method to return data to the caller.</span></span> <span data-ttu-id="5c3aa-117">**Cryptxmlenumalgorithminfo** listet die Signatur Methoden auf, die das Zertifikat unterstützt, und ruft die Rückruf Methode für jede Signatur Methode auf, bis die Rückruf Methode **false** zurückgibt oder alle Signatur Methoden im Zertifikat aufgezählt wurden.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-117">**CryptXmlEnumAlgorithmInfo** enumerates the signature methods that the certificate supports, and calls the callback method for each signature method until the callback method returns **FALSE** or until all signature methods in the certificate have been enumerated.</span></span>

<span data-ttu-id="5c3aa-118">Die Rückruf Methode im nächsten Codebeispiel sucht nach einer Signatur Methode, die von **cryptxmlenenalgorithminfo** übergangen wird und mit der Signatur Methode übereinstimmt, die von der aufrufenden Methode bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-118">The callback method in the next code example searches for a signature method passed in by **CryptXmlEnumAlgorithmInfo** that matches the signature method provided by the calling method.</span></span> <span data-ttu-id="5c3aa-119">Wenn eine Entsprechung gefunden wird, überprüft die Rückruf Methode, ob die Signatur Methode auch vom System unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-119">When a match is found, the callback method checks whether the signature method is also supported by the system.</span></span> <span data-ttu-id="5c3aa-120">Wenn die Signatur Methoden Stimmen und vom System unterstützt werden, wird die Signatur Methode als vom System unterstützt gekennzeichnet, und die Rückruf Methode gibt **false** zurück.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-120">If the signature methods match and are supported by the system, the signature method is marked as system-supported and the callback method returns **FALSE**.</span></span>


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



<span data-ttu-id="5c3aa-121">Im folgenden Codebeispiel wird die Validierungsfunktion in eine einzelne Methode umschlossen.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-121">The following code example wraps the validation functionality into a single method.</span></span> <span data-ttu-id="5c3aa-122">Diese Methode gibt einen **booleschen** Wert zurück, der angibt, ob das Zertifikat die Signatur Methode unterstützt und ob die Signatur Methode vom System unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="5c3aa-122">This method returns a **Boolean** value that indicates whether the certificate supports the signature method and whether the signature method is supported by the system.</span></span>


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



## <a name="related-topics"></a><span data-ttu-id="5c3aa-123">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="5c3aa-123">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="5c3aa-124">**Next Steps**</span><span class="sxs-lookup"><span data-stu-id="5c3aa-124">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="5c3aa-125">Laden eines Zertifikats aus einer Datei</span><span class="sxs-lookup"><span data-stu-id="5c3aa-125">Load a Certificate from a File</span></span>](load-a-certificate-from-a-file.md)
</dt> <dt>

[<span data-ttu-id="5c3aa-126">Überprüfen, ob das System eine Digest-Methode unterstützt</span><span class="sxs-lookup"><span data-stu-id="5c3aa-126">Verify the System Supports a Digest Method</span></span>](verify-a-certificate-supports-a-digest-method.md)
</dt> <dt>

[<span data-ttu-id="5c3aa-127">Einbinden von Zertifikat Ketten in ein Dokument</span><span class="sxs-lookup"><span data-stu-id="5c3aa-127">Embed Certificate Chains in a Document</span></span>](embedding-certificate-trust-chains-in-a-document.md)
</dt> <dt>

<span data-ttu-id="5c3aa-128">**In diesem Beispiel verwendet**</span><span class="sxs-lookup"><span data-stu-id="5c3aa-128">**Used in This Example**</span></span>
</dt> <dt>

[<span data-ttu-id="5c3aa-129">**Cryptfindoidinfo**</span><span class="sxs-lookup"><span data-stu-id="5c3aa-129">**CryptFindOIDInfo**</span></span>](/windows/desktop/api/wincrypt/nf-wincrypt-cryptfindoidinfo)
</dt> <dt>

[<span data-ttu-id="5c3aa-130">**Crypt- \_ OID- \_ Informationen**</span><span class="sxs-lookup"><span data-stu-id="5c3aa-130">**CRYPT\_OID\_INFO**</span></span>](/windows/desktop/api/wincrypt/ns-wincrypt-crypt_oid_info)
</dt> <dt>

<span data-ttu-id="5c3aa-131">**Cryptxmlenenalgorithminfo**</span><span class="sxs-lookup"><span data-stu-id="5c3aa-131">**CryptXmlEnumAlgorithmInfo**</span></span>
</dt> <dt>

<span data-ttu-id="5c3aa-132">**Weitere Informationen**</span><span class="sxs-lookup"><span data-stu-id="5c3aa-132">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="5c3aa-133">Kryptografieapi</span><span class="sxs-lookup"><span data-stu-id="5c3aa-133">Cryptography API</span></span>](/windows/desktop/SecCrypto/cryptography-portal)
</dt> <dt>

[<span data-ttu-id="5c3aa-134">Kryptografiefunktionen</span><span class="sxs-lookup"><span data-stu-id="5c3aa-134">Cryptography Functions</span></span>](/windows/desktop/SecCrypto/cryptography-functions)
</dt> <dt>

[<span data-ttu-id="5c3aa-135">XPS-Fehler bei der digitalen Signatur-API</span><span class="sxs-lookup"><span data-stu-id="5c3aa-135">XPS Digital Signature API Errors</span></span>](xps-digital-signatures-errors.md)
</dt> <dt>

[<span data-ttu-id="5c3aa-136">XPS-Dokument Fehler</span><span class="sxs-lookup"><span data-stu-id="5c3aa-136">XPS Document Errors</span></span>](xps-document-errors.md)
</dt> <dt>

[<span data-ttu-id="5c3aa-137">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="5c3aa-137">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
