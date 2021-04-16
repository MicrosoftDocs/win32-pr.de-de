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
# <a name="codec-merit"></a>Codec-Verdienst

Ab Windows 7 kann einem Media Foundation Codec ein *Verdienst* Wert zugewiesen werden. Wenn Codecs aufgelistet werden, werden Codecs mit höherem Wert gegenüber Codecs bevorzugt, die einen niedrigeren Wert haben. Codecs mit einem beliebigen Wert werden gegenüber Codecs bevorzugt, ohne dass ein zugewiesener Verdienst zugewiesen wird. Ausführliche Informationen zur Codec-Enumeration finden Sie unter MF-Datei ( [**MF**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)).

Verdienst Werte werden von Microsoft zugewiesen. Derzeit sind nur Hardware Codecs berechtigt, einen Verdienst Wert zu erhalten. Der Codec-Anbieter hat auch ein digitales Zertifikat ausgestellt, das verwendet wird, um den Wert des Codec-Werts zu überprüfen. Zum Abrufen eines Zertifikats senden Sie eine e-Mail-Anforderung an wmla@microsoft.com . Zum Abrufen eines Zertifikats gehört das Signieren einer Lizenz und das Bereitstellen eines Satzes von Informationsdateien an Microsoft.

Der Codec-Verdienst funktioniert wie folgt:

1.  Der Codec-Anbieter implementiert eine der folgenden Aktionen:
    -   Ein AVStream-Mini Treiber. Media Foundation stellt einen Standard Proxy-MFT für AVStream-Treiber bereit. Dies ist die empfohlene Option.
    -   Eine Media Foundation Transformation (MFT), die als Proxy für die Hardware fungiert. Weitere Informationen finden Sie unter [Hardware-MFTs](hardware-mfts.md).
2.  Der Verdienst Wert des Codecs wird in der Registrierung für die schnelle Suche gespeichert.
3.  Die Funktion " [**MF-UMEX**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) " sortiert Codecs in der Reihenfolge der Vorzüge. Codecs mit Verdienst Werten werden in der Liste hinter lokal registrierten Codecs angezeigt (siehe [**MF tregisterlocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), jedoch vor anderen Codecs.
4.  Wenn der MFT erstellt wird, wird der Codec-Verdienst mithilfe der OPM-API ( [Output Protection Manager](output-protection-manager.md) ) überprüft.
5.  Bei einem Proxy-MFT implementiert der Codec die [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Schnittstelle. Für einen AVStream-Treiber implementiert der Codec den \_ opmvideooutput-Eigenschaften Satz "kspropsetid".

Das folgende Diagramm zeigt, wie das Verdienst in beiden Fällen überprüft wird:

![das Diagramm zeigt zwei Prozesse: eine Leads durch den Media Foundation-Proxy-MFT und den AVStream-Treiber, die andere über den benutzerdefinierten Proxy-MFT](images/codecmerit.png)

## <a name="custom-proxy-mft"></a>Benutzerdefinierter Proxy-MFT

Wenn Sie einen Proxy-MFT für den Hardwarecodec bereitstellen, implementieren Sie den Codec-Verdienst wie folgt:

1.  Implementieren Sie die [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) -Schnittstelle in der MFT. Der Beispielcode wird im nächsten Abschnitt dieses Themas gezeigt.
2.  Fügen Sie das Attribut Attribut " [MFT \_ Codec \_ Verdienst \_ ](mft-codec-merit-attribute.md) " der Registrierung wie folgt hinzu:

    1.  Rufen Sie [**mfkreateattributs**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attribut Speicher zu erstellen.
    2.  Wenden Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) an, um das Attribut Attribut Attribut für [MFT- \_ Codec \_ \_](mft-codec-merit-attribute.md) festzulegen. Der Wert des-Attributs ist der der Codec zugewiesene Verdienst.
    3.  Wenden Sie sich an [**mftregister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) , um die MFT zu registrieren. Übergeben Sie den Attribut Speicher im *pattributes* -Parameter.

3.  Die Anwendung ruft [**MF-UMEX**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex)auf. Diese Funktion gibt ein Array von [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeigern zurück, eines für jeden Codec, der mit den enumerationskriterien übereinstimmt.
4.  Die Anwendung ruft [**imfaktivate:: activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) auf, um die MFT zu erstellen.
5.  Die [**activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) -Methode ruft die [**mfgetmftmerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) -Funktion auf, um das Zertifikat und den Verdienst Wert zu überprüfen.
6.  Die [**mfgetmftmerit**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) -Funktion ruft [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) auf und sendet eine [**OPM \_ get \_ Codec- \_ Informations**](opm-get-codec-info.md) Status Anforderung. Diese Status Anforderung gibt den zugewiesenen Verdienst Wert des Codecs zurück. Wenn dieser Wert nicht mit dem Registrierungs Wert identisch ist, kann [**activateobject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) fehlschlagen.

Der folgende Code zeigt, wie Sie den Verdienst Wert der Registrierung hinzufügen, wenn Sie die MFT registrieren:


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



### <a name="implementing-iopmvideooutput-for-codec-merit"></a>Implementieren von IOPMVideoOutput für Codec-Verdienste

Der folgende Code zeigt, wie [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) für Codec-Verdienste implementiert wird. Eine allgemeinere Erörterung der OPM-API finden Sie unter [Output Protection Manager](output-protection-manager.md).

> [!Note]  
> Der hier gezeigte Code hat keine Verschleierung oder andere Sicherheitsmechanismen. Es soll die grundlegende Implementierung des OPM-Handshake und der Status Anforderung zeigen.

 

In diesem Beispiel wird davon ausgegangen, dass *g \_ testCert* ein Bytearray ist, das die Zertifikatskette des Codecs enthält, und *g \_ PrivateKey* ist ein Bytearray, das den privaten Schlüssel aus dem Zertifikat enthält:


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



Generieren Sie in der [**IOPMVideoOutput:: startinitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) -Methode eine Zufallszahl für den Handshake. Diese Nummer und das Zertifikat an den Aufrufer zurückgeben:


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



Die [**IOPMVideoOutput:: FinishInitialization**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) -Methode schließt den OPM-Handshake ab:


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



Implementieren Sie in der [**IOPMVideoOutput:: GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) -Methode die [**OPM \_ get \_ Codec \_ Info**](opm-get-codec-info.md) Status Request. Bei den Eingabedaten handelt es sich um eine [**OPM \_ get \_ Codec \_ Info \_ Parameters**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) -Struktur, die die CLSID Ihres MFT enthält. Bei den Ausgabedaten handelt es sich um eine [**OPM \_ get- \_ Codec- \_ \_ Informations**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) Struktur, die den Codec-Verdienst enthält.


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



Die [**GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) -Methode muss eine Nachrichtenauthentifizierungscode (Mac) mithilfe des OMAC-1-Algorithmus berechnen. Weitere [Informationen finden Sie unter Berechnen des OMAC-1-Werts](opm-example-code.md).

Es ist nicht erforderlich, andere OPM-Status Anforderungen zu unterstützen.

Die [**IOPMVideoOutput:: COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) -Methode und die [**IOPMVideoOutput:: Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) -Methode sind für Codec-Verdienste nicht erforderlich, sodass diese Methoden **E \_ notimpl** zurückgeben können.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Media Foundation Transformationen](media-foundation-transforms.md)
</dt> <dt>

[Schreiben eines benutzerdefinierten MFT](writing-a-custom-mft.md)
</dt> </dl>

 

 



