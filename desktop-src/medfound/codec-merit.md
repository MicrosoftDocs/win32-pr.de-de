---
description: Codec-Verdienst
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Codec-Verdienst
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ecd177c3c32084a030ce75c15cecd5d4c04fc3f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556796"
---
# <a name="codec-merit"></a><span data-ttu-id="7966d-103">Codec-Verdienst</span><span class="sxs-lookup"><span data-stu-id="7966d-103">Codec Merit</span></span>

<span data-ttu-id="7966d-104">Ab Windows 7 kann einem Media Foundation Codec ein *Verdienst* Wert zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="7966d-104">Starting in Windows 7, a Media Foundation codec can be assigned a *merit* value.</span></span> <span data-ttu-id="7966d-105">Wenn Codecs aufgelistet werden, werden Codecs mit höherem Wert gegenüber Codecs bevorzugt, die einen niedrigeren Wert haben.</span><span class="sxs-lookup"><span data-stu-id="7966d-105">When codecs are enumerated, codecs with higher merit are preferred over codecs with lower merit.</span></span> <span data-ttu-id="7966d-106">Codecs mit einem beliebigen Wert werden gegenüber Codecs bevorzugt, ohne dass ein zugewiesener Verdienst zugewiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7966d-106">Codecs with any merit value are preferred over codecs without an assigned merit.</span></span> <span data-ttu-id="7966d-107">Ausführliche Informationen zur Codec-Enumeration finden Sie unter MF-Datei ( [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)).</span><span class="sxs-lookup"><span data-stu-id="7966d-107">For details about codec enumeration, see [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span>

<span data-ttu-id="7966d-108">Verdienst Werte werden von Microsoft zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7966d-108">Merit values are assigned by Microsoft.</span></span> <span data-ttu-id="7966d-109">Derzeit sind nur Hardware Codecs berechtigt, einen Verdienst Wert zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7966d-109">Currently, only hardware codecs are eligible to receive a merit value.</span></span> <span data-ttu-id="7966d-110">Der Codec-Anbieter hat auch ein digitales Zertifikat ausgestellt, das verwendet wird, um den Wert des Codec-Werts zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7966d-110">The codec vendor is also issued a digital certificate, which is used to verify the codec's merit value.</span></span> <span data-ttu-id="7966d-111">Zum Abrufen eines Zertifikats senden Sie eine e-Mail-Anforderung an wmla@microsoft.com .</span><span class="sxs-lookup"><span data-stu-id="7966d-111">To obtain a certificate, send an email request to wmla@microsoft.com.</span></span> <span data-ttu-id="7966d-112">Zum Abrufen eines Zertifikats gehört das Signieren einer Lizenz und das Bereitstellen eines Satzes von Informationsdateien an Microsoft.</span><span class="sxs-lookup"><span data-stu-id="7966d-112">The process for obtaining a certificate includes signing a license and providing a set of information files to Microsoft.</span></span>

<span data-ttu-id="7966d-113">Der Codec-Verdienst funktioniert wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7966d-113">Codec merit works as follows:</span></span>

1.  <span data-ttu-id="7966d-114">Der Codec-Anbieter implementiert eine der folgenden Aktionen:</span><span class="sxs-lookup"><span data-stu-id="7966d-114">The codec vendor implements one of the following:</span></span>
    -   <span data-ttu-id="7966d-115">Ein AVStream-Mini Treiber.</span><span class="sxs-lookup"><span data-stu-id="7966d-115">An AVStream mini-driver.</span></span> <span data-ttu-id="7966d-116">Media Foundation stellt einen Standard Proxy-MFT für AVStream-Treiber bereit.</span><span class="sxs-lookup"><span data-stu-id="7966d-116">Media Foundation provides an standard proxy MFT for AVStream drivers.</span></span> <span data-ttu-id="7966d-117">Dies ist die empfohlene Option.</span><span class="sxs-lookup"><span data-stu-id="7966d-117">This is the recommended option.</span></span>
    -   <span data-ttu-id="7966d-118">Eine Media Foundation Transformation (MFT), die als Proxy für die Hardware fungiert.</span><span class="sxs-lookup"><span data-stu-id="7966d-118">A Media Foundation transform (MFT) that acts as a proxy to the hardware.</span></span> <span data-ttu-id="7966d-119">Weitere Informationen finden Sie unter [Hardware-MFTs](hardware-mfts.md).</span><span class="sxs-lookup"><span data-stu-id="7966d-119">For more information, see [Hardware MFTs](hardware-mfts.md).</span></span>
2.  <span data-ttu-id="7966d-120">Der Verdienst Wert des Codecs wird in der Registrierung für die schnelle Suche gespeichert.</span><span class="sxs-lookup"><span data-stu-id="7966d-120">The codec's merit value is stored in the registry for quick lookup.</span></span>
3.  <span data-ttu-id="7966d-121">Die Funktion " [**MF-UMEX**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) " sortiert Codecs in der Reihenfolge der Vorzüge.</span><span class="sxs-lookup"><span data-stu-id="7966d-121">The [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function sorts codecs in order of merit.</span></span> <span data-ttu-id="7966d-122">Codecs mit Verdienst Werten werden in der Liste hinter lokal registrierten Codecs angezeigt (siehe [**MF tregisterlocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), jedoch vor anderen Codecs.</span><span class="sxs-lookup"><span data-stu-id="7966d-122">Codecs with merit values appear in the list behind locally registered codecs (see [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), but ahead of other codecs.</span></span>
4.  <span data-ttu-id="7966d-123">Wenn der MFT erstellt wird, wird der Codec-Verdienst mithilfe der OPM-API ( [Output Protection Manager](output-protection-manager.md) ) überprüft.</span><span class="sxs-lookup"><span data-stu-id="7966d-123">When the MFT is created, the codec's merit is verified using the [Output Protection Manager](output-protection-manager.md) (OPM) API.</span></span>
5.  <span data-ttu-id="7966d-124">Bei einem Proxy-MFT implementiert der Codec die [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7966d-124">For a proxy MFT, the codec implements the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface.</span></span> <span data-ttu-id="7966d-125">Für einen AVStream-Treiber implementiert der Codec den \_ opmvideooutput-Eigenschaften Satz "kspropsetid".</span><span class="sxs-lookup"><span data-stu-id="7966d-125">For an AVStream driver, the codec implements the KSPROPSETID\_OPMVideoOutput property set.</span></span>

<span data-ttu-id="7966d-126">Das folgende Diagramm zeigt, wie das Verdienst in beiden Fällen überprüft wird:</span><span class="sxs-lookup"><span data-stu-id="7966d-126">The following diagram shows how merit is verified in both cases:</span></span>

![das Diagramm zeigt zwei Prozesse: eine Leads durch den Media Foundation-Proxy-MFT und den AVStream-Treiber, die andere über den benutzerdefinierten Proxy-MFT](images/codecmerit.png)

## <a name="custom-proxy-mft"></a><span data-ttu-id="7966d-128">Benutzerdefinierter Proxy-MFT</span><span class="sxs-lookup"><span data-stu-id="7966d-128">Custom Proxy MFT</span></span>

<span data-ttu-id="7966d-129">Wenn Sie einen Proxy-MFT für den Hardwarecodec bereitstellen, implementieren Sie den Codec-Verdienst wie folgt:</span><span class="sxs-lookup"><span data-stu-id="7966d-129">If you provide a proxy MFT for the hardware codec, implement the codec merit value as follows:</span></span>

1.  <span data-ttu-id="7966d-130">Implementieren Sie die [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Schnittstelle in der MFT.</span><span class="sxs-lookup"><span data-stu-id="7966d-130">Implement the [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) interface in the MFT.</span></span> <span data-ttu-id="7966d-131">Der Beispielcode wird im nächsten Abschnitt dieses Themas gezeigt.</span><span class="sxs-lookup"><span data-stu-id="7966d-131">Example code is shown in the next section of this topic.</span></span>
2.  <span data-ttu-id="7966d-132">Fügen Sie das Attribut Attribut " [MFT \_ Codec \_ Verdienst \_ ](mft-codec-merit-attribute.md) " der Registrierung wie folgt hinzu:</span><span class="sxs-lookup"><span data-stu-id="7966d-132">Add the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute to the registry, as follows:</span></span>

    1.  <span data-ttu-id="7966d-133">Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attribut Speicher zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7966d-133">Call [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) to create a new attribute store.</span></span>
    2.  <span data-ttu-id="7966d-134">Wenden Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) an, um das Attribut Attribut Attribut für [MFT- \_ Codec \_ \_](mft-codec-merit-attribute.md) festzulegen.</span><span class="sxs-lookup"><span data-stu-id="7966d-134">Call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) to set the [MFT\_CODEC\_MERIT\_Attribute](mft-codec-merit-attribute.md) attribute.</span></span> <span data-ttu-id="7966d-135">Der Wert des-Attributs ist der der Codec zugewiesene Verdienst.</span><span class="sxs-lookup"><span data-stu-id="7966d-135">The value of the attribute is the codec's assigned merit.</span></span>
    3.  <span data-ttu-id="7966d-136">Wenden Sie sich an [**mftregister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) , um die MFT zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="7966d-136">Call [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) to register the MFT.</span></span> <span data-ttu-id="7966d-137">Übergeben Sie den Attribut Speicher im *pattributes* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="7966d-137">Pass the attribute store in the *pAttributes* parameter.</span></span>

3.  <span data-ttu-id="7966d-138">Die Anwendung ruft [**MF-UMEX**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)auf.</span><span class="sxs-lookup"><span data-stu-id="7966d-138">The application calls [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).</span></span> <span data-ttu-id="7966d-139">Diese Funktion gibt ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern zurück, eines für jeden Codec, der mit den enumerationskriterien übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="7966d-139">This function returns an array of [**IMFActivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) pointers, one for each codec that matches the enumeration criteria.</span></span>
4.  <span data-ttu-id="7966d-140">Die Anwendung ruft [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) auf, um die MFT zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="7966d-140">The application calls [**IMFActivate::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) to create the MFT.</span></span>
5.  <span data-ttu-id="7966d-141">Die [**activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode ruft die [**mfgetmftmerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) -Funktion auf, um das Zertifikat und den Verdienst Wert zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="7966d-141">The [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) method calls the [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function to verify the certificate and the merit value.</span></span>
6.  <span data-ttu-id="7966d-142">Die [**mfgetmftmerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) -Funktion ruft [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) auf und sendet eine [**OPM \_ get \_ Codec- \_ Informations**](opm-get-codec-info.md) Status Anforderung.</span><span class="sxs-lookup"><span data-stu-id="7966d-142">The [**MFGetMFTMerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) function calls [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) and sends an [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="7966d-143">Diese Status Anforderung gibt den zugewiesenen Verdienst Wert des Codecs zurück.</span><span class="sxs-lookup"><span data-stu-id="7966d-143">This status request returns the codec's assigned merit value.</span></span> <span data-ttu-id="7966d-144">Wenn dieser Wert nicht mit dem Registrierungs Wert identisch ist, kann [**activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="7966d-144">If this value does not match the registry value, [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) may fail.</span></span>

<span data-ttu-id="7966d-145">Der folgende Code zeigt, wie Sie den Verdienst Wert der Registrierung hinzufügen, wenn Sie die MFT registrieren:</span><span class="sxs-lookup"><span data-stu-id="7966d-145">The following code shows how to add the merit value to the registry when you register the MFT:</span></span>


```C++
// Shows how to register an MFT with a merit value.

HRESULT RegisterMFTWithMerit()
{
    // The following media types would apply to an H.264 decoder, 
    // and are used here as an example.

    MFT_REGISTER_TYPE_INFO aDecoderInputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_H264 },
    };

    MFT_REGISTER_TYPE_INFO aDecoderOutputTypes[] = 
    {
        { MFMediaType_Video, MFVideoFormat_RGB32 }
    };
    
    // Create an attribute store to hold the merit attribute.
    HRESULT hr = S_OK;
    IMFAttributes *pAttributes = NULL;

    hr = MFCreateAttributes(&pAttributes, 1);

    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetUINT32(
            MFT_CODEC_MERIT_Attribute, 
            DECODER_MERIT   // Use the codec's assigned merit value.
            );
    }

    // Register the decoder for MFTEnum(Ex).
    if (SUCCEEDED(hr))
    {
        hr = MFTRegister(
            CLSID_MPEG1SampleDecoder,                   // CLSID
            MFT_CATEGORY_VIDEO_DECODER,                 // Category
            const_cast<LPWSTR>(SZ_DECODER_NAME),        // Friendly name
            0,                                          // Flags
            ARRAYSIZE(aDecoderInputTypes),              // Number of input types
            aDecoderInputTypes,                         // Input types
            ARRAYSIZE(aDecoderOutputTypes),             // Number of output types
            aDecoderOutputTypes,                        // Output types
            pAttributes                                 // Attributes 
            );
    }

    SafeRelease(&pAttributes);
    return hr;
}
```



### <a name="implementing-iopmvideooutput-for-codec-merit"></a><span data-ttu-id="7966d-146">Implementieren von IOPMVideoOutput für Codec-Verdienste</span><span class="sxs-lookup"><span data-stu-id="7966d-146">Implementing IOPMVideoOutput for Codec Merit</span></span>

<span data-ttu-id="7966d-147">Der folgende Code zeigt, wie [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) für Codec-Verdienste implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="7966d-147">The following code shows how to implement [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) for codec merit.</span></span> <span data-ttu-id="7966d-148">Eine allgemeinere Erörterung der OPM-API finden Sie unter [Output Protection Manager](output-protection-manager.md).</span><span class="sxs-lookup"><span data-stu-id="7966d-148">For a more general discussion of the OPM API, see [Output Protection Manager](output-protection-manager.md).</span></span>

> [!Note]  
> <span data-ttu-id="7966d-149">Der hier gezeigte Code hat keine Verschleierung oder andere Sicherheitsmechanismen.</span><span class="sxs-lookup"><span data-stu-id="7966d-149">The code shown here has no obfuscation or other security mechanisms.</span></span> <span data-ttu-id="7966d-150">Es soll die grundlegende Implementierung des OPM-Handshake und der Status Anforderung zeigen.</span><span class="sxs-lookup"><span data-stu-id="7966d-150">It is meant to show the basic implementation of the OPM handshake and status request.</span></span>

 

<span data-ttu-id="7966d-151">In diesem Beispiel wird davon ausgegangen, dass *g \_ testCert* ein Bytearray ist, das die Zertifikatskette des Codecs enthält, und *g \_ PrivateKey* ist ein Bytearray, das den privaten Schlüssel aus dem Zertifikat enthält:</span><span class="sxs-lookup"><span data-stu-id="7966d-151">This example assumes that *g\_TestCert* is a byte array that contains the codec's certificate chain, and *g\_PrivateKey* is a byte array that contains the private key from the certificate:</span></span>


```C++
// Byte array that contains the codec's certificate.

const BYTE g_TestCert[] =
{
    // ... (certificate not shown)
```




```C++
// Byte array that contains the private key from the certificate.

const BYTE g_PrivateKey[] = 
{
    // .... (key not shown)
```



<span data-ttu-id="7966d-152">Generieren Sie in der [**IOPMVideoOutput:: startinitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) -Methode eine Zufallszahl für den Handshake.</span><span class="sxs-lookup"><span data-stu-id="7966d-152">In the [**IOPMVideoOutput::StartInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) method, generate a random number for the handshake.</span></span> <span data-ttu-id="7966d-153">Diese Nummer und das Zertifikat an den Aufrufer zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="7966d-153">Return this number and the certificate to the caller:</span></span>


```C++
STDMETHODIMP CodecMerit::StartInitialization(
    OPM_RANDOM_NUMBER *prnRandomNumber,
    BYTE **ppbCertificate,
    ULONG *pulCertificateLength
    )
{
    HRESULT hr = S_OK;

    DWORD cbCertificate = sizeof(g_TestCert);
    const BYTE *pCertificate = g_TestCert;

    // Generate the random number for the OPM handshake.
    hr = BCryptGenRandom(
        NULL,  
        (PUCHAR)&m_RandomNumber, 
        sizeof(m_RandomNumber),
        BCRYPT_USE_SYSTEM_PREFERRED_RNG
        );

    // Allocate the buffer to copy the certificate.
    if (SUCCEEDED(hr))
    {
        *ppbCertificate = (PBYTE)CoTaskMemAlloc(cbCertificate);

        if (*ppbCertificate == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    // Copy the certificate and the random number.
    if (SUCCEEDED(hr))
    {
        *pulCertificateLength = cbCertificate;
        CopyMemory(*ppbCertificate, pCertificate, cbCertificate);
        *prnRandomNumber = m_RandomNumber;
    }
    return hr;
}
```



<span data-ttu-id="7966d-154">Die [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) -Methode schließt den OPM-Handshake ab:</span><span class="sxs-lookup"><span data-stu-id="7966d-154">The [**IOPMVideoOutput::FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) method completes the OPM handshake:</span></span>


```C++
STDMETHODIMP CodecMerit::FinishInitialization(
    const OPM_ENCRYPTED_INITIALIZATION_PARAMETERS *pParameters
    )
{
    HRESULT hr = S_OK;
    BCRYPT_ALG_HANDLE hAlg = NULL;
    BCRYPT_KEY_HANDLE hKey = NULL;
    BCRYPT_OAEP_PADDING_INFO paddingInfo = {0};
    DWORD DecryptedLength = 0;
    PBYTE pbDecryptedParams = NULL;

    // The caller should pass the following structure in
    // pParameters:

    typedef struct {
        GUID  guidCOPPRandom;   // Our random number.
        GUID  guidKDI;          // AES signing key.
        DWORD StatusSeqStart;   // Status sequence number.
        DWORD CommandSeqStart;  // Command sequence number.
    } InitParams;

    paddingInfo.pszAlgId = BCRYPT_SHA512_ALGORITHM;

    //  Decrypt the input using the decoder's private key.

    hr = BCryptOpenAlgorithmProvider(
        &hAlg,
        BCRYPT_RSA_ALGORITHM,
        MS_PRIMITIVE_PROVIDER,
        0
        );

    //  Import the private key.
    if (SUCCEEDED(hr))
    {
        hr = BCryptImportKeyPair(
            hAlg,
            NULL,
            BCRYPT_RSAPRIVATE_BLOB,
            &hKey,
            (PUCHAR)g_PrivateKey, //pbData,
            sizeof(g_PrivateKey), //cbData,
            0
            );
    }

    //  Decrypt the input data.

    if (SUCCEEDED(hr))
    {
        hr = BCryptDecrypt(
            hKey,
            (PBYTE)pParameters,
            OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
            &paddingInfo,
            NULL,
            0,
            NULL,
            0,
            &DecryptedLength,
            BCRYPT_PAD_OAEP
            );
    }

    if (SUCCEEDED(hr))
    {
        pbDecryptedParams = new (std::nothrow) BYTE[DecryptedLength];

        if (pbDecryptedParams == NULL) 
        {
            hr = E_OUTOFMEMORY;
        }
    }

    if (SUCCEEDED(hr))
    {
         hr = BCryptDecrypt(
             hKey,
             (PBYTE)pParameters,
             OPM_ENCRYPTED_INITIALIZATION_PARAMETERS_SIZE,
             &paddingInfo,
             NULL,
             0,
             pbDecryptedParams,
             DecryptedLength,
             &DecryptedLength,
             BCRYPT_PAD_OAEP
             );
    }

    if (SUCCEEDED(hr))
    {
        InitParams *Params = (InitParams *)pbDecryptedParams;
        
        //  Check the random number.
        if (0 != memcmp(&m_RandomNumber, &Params->guidCOPPRandom, sizeof(m_RandomNumber)))
        {
            hr = E_ACCESSDENIED;
        } 
        else 
        {
            //  Save the key and the sequence numbers.

            CopyMemory(m_AESKey.abRandomNumber, &Params->guidKDI, sizeof(m_AESKey));
            m_StatusSequenceNumber = Params->StatusSeqStart;
            m_CommandSequenceNumber = Params->CommandSeqStart;
        }
    }

    //  Clean up.

    if (hKey)
    {
        BCryptDestroyKey(hKey);
    }
    if (hAlg)
    {
        BCryptCloseAlgorithmProvider(hAlg, 0);
    }
    delete [] pbDecryptedParams;

    return hr;
}
```



<span data-ttu-id="7966d-155">Implementieren Sie in der [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) -Methode die [**OPM \_ get \_ Codec \_ Info**](opm-get-codec-info.md) Status Request.</span><span class="sxs-lookup"><span data-stu-id="7966d-155">In the [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method, implement the [**OPM\_GET\_CODEC\_INFO**](opm-get-codec-info.md) status request.</span></span> <span data-ttu-id="7966d-156">Bei den Eingabedaten handelt es sich um eine [**OPM \_ get \_ Codec \_ Info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) -Struktur, die die CLSID Ihres MFT enthält.</span><span class="sxs-lookup"><span data-stu-id="7966d-156">The input data is an [**OPM\_GET\_CODEC\_INFO\_PARAMETERS**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) structure that contains the CLSID of your MFT.</span></span> <span data-ttu-id="7966d-157">Bei den Ausgabedaten handelt es sich um eine [**OPM \_ get- \_ Codec- \_ \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) Struktur, die den Codec-Verdienst enthält.</span><span class="sxs-lookup"><span data-stu-id="7966d-157">The output data is an [**OPM\_GET\_CODEC\_INFO\_INFORMATION**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) structure that contains the codec merit.</span></span>


```C++
STDMETHODIMP CodecMerit::GetInformation( 
    const OPM_GET_INFO_PARAMETERS *Parameters,
    OPM_REQUESTED_INFORMATION *pRequest
    )
{

    HRESULT hr = S_OK;
    OPM_GET_CODEC_INFO_PARAMETERS *CodecInfoParameters;

    //  Check the MAC.
    OPM_OMAC Tag = { 0 };

    hr = ComputeOMAC(
        m_AESKey, 
        (PBYTE)Parameters + OPM_OMAC_SIZE, 
        sizeof(OPM_GET_INFO_PARAMETERS) - OPM_OMAC_SIZE, 
        &Tag
        );

    if (SUCCEEDED(hr))
    {
        if (0 != memcmp(Tag.abOMAC, &Parameters->omac, OPM_OMAC_SIZE))
        {
            hr = E_ACCESSDENIED;
        }
    }

    // Validate the status sequence number. This must be consecutive
    // from the previous sequence number.

    if (SUCCEEDED(hr))
    {
        if (Parameters->ulSequenceNumber != m_StatusSequenceNumber++)
        {
            hr = E_ACCESSDENIED;
        }
    }

    //  Check the status request.

    if (SUCCEEDED(hr))
    {
        if (Parameters->guidInformation != OPM_GET_CODEC_INFO) 
        {
            hr = E_NOTIMPL;
        }
    }

    //  Check parameters.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;

        if (Parameters->cbParametersSize > OPM_GET_INFORMATION_PARAMETERS_SIZE ||
            Parameters->cbParametersSize < sizeof(ULONG) ||
            Parameters->cbParametersSize - sizeof(ULONG) != CodecInfoParameters->cbVerifier
            ) 
        {
            hr = E_INVALIDARG;
        }
    }

    //  The input data should consist of the CLSID of the decoder.

    if (SUCCEEDED(hr))
    {
        CodecInfoParameters = (OPM_GET_CODEC_INFO_PARAMETERS *)Parameters->abParameters;
    
        if (CodecInfoParameters->cbVerifier != sizeof(CLSID) ||
            0 != memcmp(&CLSID_MPEG1SampleDecoder,
                        CodecInfoParameters->Verifier,
                        CodecInfoParameters->cbVerifier)) 
        {
            hr = E_ACCESSDENIED;
        }
    }

    if (SUCCEEDED(hr))
    {
        // Now return the decoder merit to the caller.

        ZeroMemory(pRequest, sizeof(OPM_REQUESTED_INFORMATION));

        OPM_GET_CODEC_INFO_INFORMATION *pInfo = 
            (OPM_GET_CODEC_INFO_INFORMATION *)pRequest->abRequestedInformation;

        pInfo->Merit = DECODER_MERIT;
        pInfo->rnRandomNumber = Parameters->rnRandomNumber;

        pRequest->cbRequestedInformationSize = sizeof(OPM_GET_CODEC_INFO_INFORMATION);

        //  Sign it with the key.

        hr = ComputeOMAC(
            m_AESKey, 
            (PBYTE)pRequest + OPM_OMAC_SIZE, 
            sizeof(OPM_REQUESTED_INFORMATION) - OPM_OMAC_SIZE, 
            &pRequest->omac
            );
    }

    return hr;
}
```



<span data-ttu-id="7966d-158">Die [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) -Methode muss eine Nachrichtenauthentifizierungscode (Mac) mithilfe des OMAC-1-Algorithmus berechnen. Weitere [Informationen finden Sie unter Berechnen des OMAC-1-Werts](opm-example-code.md).</span><span class="sxs-lookup"><span data-stu-id="7966d-158">The [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) method must compute a Message Authentication Code (MAC) using the OMAC-1 algorithm; see [Computing the OMAC-1 Value](opm-example-code.md).</span></span>

<span data-ttu-id="7966d-159">Es ist nicht erforderlich, andere OPM-Status Anforderungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7966d-159">It is not necessary to support any other OPM status requests.</span></span>

<span data-ttu-id="7966d-160">Die [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) -Methode und die [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) -Methode sind für Codec-Verdienste nicht erforderlich, sodass diese Methoden **E \_ notimpl** zurückgeben können.</span><span class="sxs-lookup"><span data-stu-id="7966d-160">The [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) and [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) methods are not required for codec merit, so these methods can return **E\_NOTIMPL**.</span></span>


```C++
STDMETHODIMP CodecMerit::COPPCompatibleGetInformation( 
    const OPM_COPP_COMPATIBLE_GET_INFO_PARAMETERS *pParameters,
    OPM_REQUESTED_INFORMATION *pRequestedInformation)
{
    return E_NOTIMPL;
}

STDMETHODIMP CodecMerit::Configure( 
    const OPM_CONFIGURE_PARAMETERS *pParameters,
    ULONG ulAdditionalParametersSize,
    const BYTE *pbAdditionalParameters)
{
    return E_NOTIMPL;
}
```



## <a name="related-topics"></a><span data-ttu-id="7966d-161">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="7966d-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7966d-162">Media Foundation Transformationen</span><span class="sxs-lookup"><span data-stu-id="7966d-162">Media Foundation Transforms</span></span>](media-foundation-transforms.md)
</dt> <dt>

[<span data-ttu-id="7966d-163">Schreiben eines benutzerdefinierten MFT</span><span class="sxs-lookup"><span data-stu-id="7966d-163">Writing a Custom MFT</span></span>](writing-a-custom-mft.md)
</dt> </dl>

 

 



