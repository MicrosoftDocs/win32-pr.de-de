---
description: Zertifikatsperrlisten
ms.assetid: 146e7e4a-4281-4f5c-8346-d6c0d5f5442f
title: Zertifikatsperrlisten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b51ddee9f77b147d69b8895b3335d41e041da7f2
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "106343132"
---
# <a name="certificate-revocation-lists"></a><span data-ttu-id="e2c9e-103">Zertifikatsperrlisten</span><span class="sxs-lookup"><span data-stu-id="e2c9e-103">Certificate Revocation Lists</span></span>

<span data-ttu-id="e2c9e-104">In diesem Thema wird beschrieben, wie Sie die Zertifikat Sperr Liste (CRL) für widerrufene Treiber bei Verwendung des Certified Output Protection-Protokolls (COPP) untersuchen.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-104">This topic describes how to examine the certificate revocation list (CRL) for revoked drivers when using Certified Output Protection Protocol (COPP).</span></span>

<span data-ttu-id="e2c9e-105">Die Zertifikat Sperr Liste enthält Digests von gesperrten Zertifikaten und kann nur von Microsoft bereitgestellt und signiert werden.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-105">The CRL contains digests of revoked certificates and can be provided and signed only by Microsoft.</span></span> <span data-ttu-id="e2c9e-106">Die CRL wird über Digital Rights Management (DRM)-Lizenzen verteilt.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-106">The CRL is distributed through digital rights management (DRM) licenses.</span></span> <span data-ttu-id="e2c9e-107">Die CRL kann alle Zertifikate in der Zertifikat Kette des Treibers widerrufen.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-107">The CRL can revoke any certificate in the driver's certificates chain.</span></span> <span data-ttu-id="e2c9e-108">Wenn ein Zertifikat in der Kette widerrufen wird, werden dieses Zertifikat und alle in der Kette untergeordneten Zertifikate ebenfalls gesperrt.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-108">If any certificate in the chain is revoked, then that certificate and all of the certificates below it in the chain are also revoked.</span></span>

<span data-ttu-id="e2c9e-109">Zum erhalten der CRL muss die Anwendung das Windows Media-Format SDK, Version 9 oder höher, verwenden und die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="e2c9e-109">To get the CRL, the application must use the Windows Media Format SDK, version 9 or later, and perform the following steps:</span></span>

1.  <span data-ttu-id="e2c9e-110">Rufen Sie **wmkreatereader** auf, um das Windows Media Format SDK Reader-Objekt zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-110">Call **WMCreateReader** to create the Windows Media Format SDK reader object.</span></span>
2.  <span data-ttu-id="e2c9e-111">Fragen Sie das Reader-Objekt für die **iwmdrmreader** -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-111">Query the reader object for the **IWMDRMReader** interface.</span></span>
3.  <span data-ttu-id="e2c9e-112">Rufen Sie **iwmdrmreader:: getdrmproperty** mit dem Wert g \_ wszwmdrmnet- \_ Widerruf auf, um die CRL abzurufen.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-112">Call **IWMDRMReader::GetDRMProperty** with a value of g\_wszWMDRMNet\_Revocation to get the CRL.</span></span> <span data-ttu-id="e2c9e-113">Sie müssen diese Methode zweimal ausführen: einmal, um die Größe des zuzuordnenden Puffers abzurufen, und einmal, um den Puffer zu füllen.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-113">You must call this method twice: Once to get the size of the buffer to allocate, and once to fill the buffer.</span></span> <span data-ttu-id="e2c9e-114">Der zweite-Rückruf gibt eine Zeichenfolge zurück, die die CRL enthält.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-114">The second call returns a string that contains the CRL.</span></span> <span data-ttu-id="e2c9e-115">Die gesamte Zeichenfolge ist Base-64-codiert.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-115">The entire string is base-64 encoded.</span></span>
4.  <span data-ttu-id="e2c9e-116">Decodieren Sie die Base-64-codierte Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-116">Decode the base-64 encoded string.</span></span> <span data-ttu-id="e2c9e-117">Hierfür können Sie die **cryptstringto Binary** -Funktion verwenden.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-117">You can use the **CryptStringToBinary** function to do this.</span></span> <span data-ttu-id="e2c9e-118">Diese Funktion ist Teil von CryptoAPI.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-118">This function is part of CryptoAPI.</span></span>

> [!Note]  
> <span data-ttu-id="e2c9e-119">Um die **iwmdrmreader** -Schnittstelle verwenden zu können, müssen Sie eine statische DRM-Bibliothek von Microsoft abrufen und Ihre Anwendung mit dieser Bibliotheksdatei verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-119">To use the **IWMDRMReader** interface, you must obtain a static DRM library from Microsoft and link your application to this library file.</span></span> <span data-ttu-id="e2c9e-120">Weitere Informationen finden Sie im Thema zum Abrufen der erforderlichen DRM-Bibliothek in der Dokumentation zum Windows Media-Format-SDK.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-120">For more information, see the topic "Obtaining the Required DRM Library" in the Windows Media Format SDK documentation.</span></span>

 

<span data-ttu-id="e2c9e-121">Wenn die Zertifikat Sperr Liste nicht auf dem Computer des Benutzers vorhanden ist, gibt die **getdrmproperty** -Methode die \_ \_ \_ nicht unterstützte Eigenschaft "NS E DRM" zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="e2c9e-121">If the CRL is not present on the user's computer, the **GetDRMProperty** method returns NS\_E\_DRM\_UNSUPPORTED\_PROPERTY.</span></span> <span data-ttu-id="e2c9e-122">Derzeit besteht die einzige Möglichkeit zum Abrufen der CRL darin, eine DRM-Lizenz zu erwerben.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-122">Currently, the only way to obtain the CRL is to acquire a DRM license.</span></span>

<span data-ttu-id="e2c9e-123">Der folgende Code zeigt eine Funktion, die die CRL zurückgibt:</span><span class="sxs-lookup"><span data-stu-id="e2c9e-123">The following code shows a function that returns the CRL:</span></span>


```C++
////////////////////////////////////////////////////////////////////////
//  Name: GetCRL
//  Description: Gets the certificate revocation list (CRL).
//
//  ppBuffer: Receives a pointer to the buffer that contains the CRL.
//  pcbBuffer: Receives the size of the buffer returned in ppBuffer.
//
//  The caller must free the returned buffer by calling CoTaskMemFree.
////////////////////////////////////////////////////////////////////////
HRESULT GetCRL(BYTE **ppBuffer, DWORD *pcbBuffer)
{
    IWMReader *pReader = NULL;
    IWMDRMReader *pDrmReader = NULL;
    HRESULT hr = S_OK;

    // DRM attribute data.
    WORD cbAttributeLength = 0;
    BYTE *pDataBase64 = NULL;
    WMT_ATTR_DATATYPE type;

    // Buffer for base-64 decoded CRL.
    BYTE *pCRL = NULL;
    DWORD cbCRL = 0;

    // Create the WMReader object.
    hr = WMCreateReader(NULL, 0, &pReader);

    // Query for the IWMDRMReader interface.
    if (SUCCEEDED(hr))
    {
        hr = pReader->QueryInterface(
            IID_IWMDRMReader, (void**)&pDrmReader);
    }

    // Call GetDRMProperty once to find the size of the buffer.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            NULL,
            &cbAttributeLength
            );
    }

    // Allocate a buffer.
    if (SUCCEEDED(hr))
    {
        pDataBase64 = (BYTE*)CoTaskMemAlloc(cbAttributeLength);
        if (pDataBase64 == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Call GetDRMProperty again to get the property.
    if (SUCCEEDED(hr))
    {
        hr = pDrmReader->GetDRMProperty(
            g_wszWMDRMNET_Revocation,
            &type,
            pDataBase64,
            &cbAttributeLength
            );
    }

    // Find the size of the buffer for the base-64 decoding.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            NULL,                   // Buffer (NULL).
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Allocate a buffer for the CRL.
    if (SUCCEEDED(hr))
    {
        pCRL = (BYTE*)CoTaskMemAlloc(cbCRL);
        if (pCRL == NULL)
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Base-64 decode to get the CRL.
    if (SUCCEEDED(hr))
    {
        BOOL bResult = CryptStringToBinary(
            (WCHAR*)pDataBase64,    // Base-64 encoded string.
            0,                      // Null-terminated.
            CRYPT_STRING_BASE64,    
            pCRL,                   // Buffer.
            &cbCRL,                 // Receives the size of the buffer. 
            NULL, NULL              // Optional.
            );
        if (!bResult)
        {
            hr = __HRESULT_FROM_WIN32(GetLastError());
        }
    }

    // Return the buffer to the caller. Caller must free the buffer.
    if (SUCCEEDED(hr))
    {
        *ppBuffer = pCRL;
        *pcbBuffer = cbCRL;
    }
    else
    {
        CoTaskMemFree(pCRL);
    }

    CoTaskMemFree(pDataBase64);
    SAFE_RELEASE(pReader);
    SAFE_RELEASE(pDrmReader);
    return hr;
}
```



<span data-ttu-id="e2c9e-124">Anschließend muss die Anwendung überprüfen, ob die CRL gültig ist.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-124">Next, the application must verify that the CRL is valid.</span></span> <span data-ttu-id="e2c9e-125">Vergewissern Sie sich hierzu, dass das Zertifikat der CRL, das Teil der Zertifikat Sperr Liste ist, direkt vom Microsoft-Stamm Zertifikat signiert ist und dass der Wert des signcrl-Elements auf 1 festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-125">To do so, verify that the CRL certificate, which is part of the CRL, is directly signed by the Microsoft Root Certificate and has the SignCRL element value set to 1.</span></span> <span data-ttu-id="e2c9e-126">Überprüfen Sie außerdem die Signatur der CRL.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-126">Also, verify the signature of the CRL.</span></span>

<span data-ttu-id="e2c9e-127">Nachdem die CRL überprüft wurde, kann Sie von der Anwendung gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-127">After the CRL is verified, the application can store it.</span></span> <span data-ttu-id="e2c9e-128">Die CRL-Versionsnummer sollte vor dem Speichern auch geprüft werden, damit die Anwendung immer die neueste Version speichert.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-128">The CRL version number should also be checked before storing so that the application always stores the newest version.</span></span>

<span data-ttu-id="e2c9e-129">Die CRL weist das folgende Format auf.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-129">The CRL has the following format.</span></span>



| <span data-ttu-id="e2c9e-130">`Section`</span><span class="sxs-lookup"><span data-stu-id="e2c9e-130">Section</span></span>            | <span data-ttu-id="e2c9e-131">Contents</span><span class="sxs-lookup"><span data-stu-id="e2c9e-131">Contents</span></span>                                                             |
|--------------------|----------------------------------------------------------------------|
| <span data-ttu-id="e2c9e-132">Header</span><span class="sxs-lookup"><span data-stu-id="e2c9e-132">Header</span></span>             | <span data-ttu-id="e2c9e-133">32-Bit-CRL version32-Bit-Anzahl von Einträgen</span><span class="sxs-lookup"><span data-stu-id="e2c9e-133">32-bit CRL version32-bit number of entries</span></span>                           |
| <span data-ttu-id="e2c9e-134">Sperr Einträge</span><span class="sxs-lookup"><span data-stu-id="e2c9e-134">Revocation Entries</span></span> | <span data-ttu-id="e2c9e-135">Mehrere 160-Bit-Sperr Einträge</span><span class="sxs-lookup"><span data-stu-id="e2c9e-135">Multiple 160-bit revocation entries</span></span>                                  |
| <span data-ttu-id="e2c9e-136">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="e2c9e-136">Certificate</span></span>        | <span data-ttu-id="e2c9e-137">32-Bit-Zertifikat mit Längen variabler Länge</span><span class="sxs-lookup"><span data-stu-id="e2c9e-137">32-bit certificate lengthVariable-length certificate</span></span>                 |
| <span data-ttu-id="e2c9e-138">Signatur</span><span class="sxs-lookup"><span data-stu-id="e2c9e-138">Signature</span></span>          | <span data-ttu-id="e2c9e-139">8-Bit-Signatur type16-Bit-Signatur Längen variabler Länge</span><span class="sxs-lookup"><span data-stu-id="e2c9e-139">8-bit signature type16-bit signature lengthVariable-length signature</span></span> |



 

> [!Note]  
> <span data-ttu-id="e2c9e-140">Alle ganzzahligen Werte sind unsigniert und werden in der Big-Endian-Notation (netzwerkbyte Reihenfolge) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-140">All integer values are unsigned and are represented in big-endian (network byte order) notation.</span></span>

 

<span data-ttu-id="e2c9e-141">CRL-Abschnitts Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="e2c9e-141">CRL Section Descriptions</span></span>

<dl> <dt>

<span data-ttu-id="e2c9e-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span><span class="sxs-lookup"><span data-stu-id="e2c9e-142"><span id="Header"></span><span id="header"></span><span id="HEADER"></span>Header</span></span>
</dt> <dd>

<span data-ttu-id="e2c9e-143">Der-Header enthält die Versionsnummer der CRL und die Anzahl der Sperr Einträge in der CRL.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-143">The header contains the version number of the CRL and the number of revocation entries in the CRL.</span></span> <span data-ttu-id="e2c9e-144">Eine CRL kann NULL oder mehr Einträge enthalten.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-144">A CRL can contain zero or more entries.</span></span>

</dd> <dt>

<span data-ttu-id="e2c9e-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Sperr Einträge</span><span class="sxs-lookup"><span data-stu-id="e2c9e-145"><span id="Revocation_entries"></span><span id="revocation_entries"></span><span id="REVOCATION_ENTRIES"></span>Revocation entries</span></span>
</dt> <dd>

<span data-ttu-id="e2c9e-146">Jeder Sperr Eintrag ist der 160-Bit-Digest eines gesperrten Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-146">Each revocation entry is the 160-bit digest of a revoked certificate.</span></span> <span data-ttu-id="e2c9e-147">Vergleichen Sie diesen Digest mit dem DigestValue-Element innerhalb des Zertifikats.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-147">Compare this digest with the DigestValue element within the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="e2c9e-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Stellt</span><span class="sxs-lookup"><span data-stu-id="e2c9e-148"><span id="Certificate"></span><span id="certificate"></span><span id="CERTIFICATE"></span>Certificate</span></span>
</dt> <dd>

<span data-ttu-id="e2c9e-149">Der Abschnitt Zertifikat enthält einen 32-Bit-Wert, der die Länge (in Bytes) des XML-Zertifikats und seiner Zertifikat Kette sowie ein Bytearray angibt, das sowohl das XML-Zertifikat der Zertifizierungsstelle als auch die Zertifikat Kette enthält, die Microsoft als Stamm hat.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-149">The certificate section contains a 32-bit value indicating the length (in bytes) of the XML certificate and its certificate chain, along with a byte array that contains both the XML certificate of the Certificate Authority (CA) and the certificate chain that has Microsoft as the Root.</span></span> <span data-ttu-id="e2c9e-150">Das Zertifikat muss von einer Zertifizierungsstelle signiert werden, die über die Berechtigung zum Ausstellen von CRLs verfügt.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-150">The certificate must be signed by a CA that has the authority to issue CRLs.</span></span>

> [!Note]  
> <span data-ttu-id="e2c9e-151">Das Zertifikat darf nicht auf Null enden.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-151">The certificate must not be null-terminated.</span></span>

 

</dd> <dt>

<span data-ttu-id="e2c9e-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Unter</span><span class="sxs-lookup"><span data-stu-id="e2c9e-152"><span id="Signature"></span><span id="signature"></span><span id="SIGNATURE"></span>Signature</span></span>
</dt> <dd>

<span data-ttu-id="e2c9e-153">Der Signatur Abschnitt enthält den Typ und die Länge der Signatur sowie die digitale Signatur selbst.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-153">The signature section contains the signature type and length, and the digital signature itself.</span></span> <span data-ttu-id="e2c9e-154">Der 8-Bit-Typ wird auf 2 festgelegt, um anzugeben, dass SHA-1 mit 1024-Bit-RSA-Verschlüsselung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-154">The 8-bit type is set to 2 to indicate that it uses SHA-1 with 1024-bit RSA encryption.</span></span> <span data-ttu-id="e2c9e-155">Die Länge ist ein 16-Bit-Wert, der die Länge der digitalen Signatur in Bytes enthält.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-155">The length is a 16-bit value containing the length of the digital signature in bytes.</span></span> <span data-ttu-id="e2c9e-156">Die digitale Signatur wird über alle vorherigen Abschnitte der CRL berechnet.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-156">The digital signature is calculated over all prior sections of the CRL.</span></span>

<span data-ttu-id="e2c9e-157">Die Signatur wird mit dem digitalen rsassa-PSS-Signatur Schema berechnet, das in PKCS \# 1 (Version 2,1) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-157">The signature is calculated using the RSASSA-PSS digital signature scheme that is defined in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="e2c9e-158">Bei der Hash Funktion handelt es sich um SHA-1, der in Federal Information Processing Standard (FI) 180-2 definiert ist, und die Masken Generierungs Funktion ist MGF1, die in Abschnitt B. 2.1 in PKCS \# 1 (Version 2,1) definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-158">The hash function is SHA-1, which is defined in Federal Information Processing Standard (FIPS) 180-2, and the mask generation function is MGF1, which is defined in section B.2.1 in PKCS \#1 (version 2.1).</span></span> <span data-ttu-id="e2c9e-159">Der RSASP1-und der RSAVP1-Vorgang verwenden RSA mit einem 1024-Bit-Modulo mit einem Verifizierungs Exponent von 65537.</span><span class="sxs-lookup"><span data-stu-id="e2c9e-159">The RSASP1 and RSAVP1 operations use RSA with a 1024-bit modulus with a verification exponent of 65537.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="e2c9e-160">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="e2c9e-160">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e2c9e-161">Verwenden des Certified Output Protection-Protokolls (COPP)</span><span class="sxs-lookup"><span data-stu-id="e2c9e-161">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)
</dt> </dl>

 

 



