---
description: Codec-Vererzung
ms.assetid: 4ed594a0-2cc2-40d2-9b5c-dee59916fa1b
title: Codec-Vererzung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b56112942aa8378b2016616d0e090e17eb7225ca27b363c96e37eb7cccb6286e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118065123"
---
# <a name="codec-merit"></a>Codec-Vererzung

Ab Windows 7 kann einem Media Foundation Codec ein *Wert* zugewiesen werden. Wenn Codecs aufzählt werden, werden Codecs mit höheren Vorteilen gegenüber Codecs mit geringeren Vorteilen bevorzugt. Codecs mit einem beliebigen Wert werden vor Codecs ohne zugewiesene Vorteile bevorzugt. Ausführliche Informationen zur Codecenumeration finden Sie unter [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex).

Werte werden von Microsoft zugewiesen. Derzeit sind nur Hardwarecodecs berechtigt, einen Wert zu erhalten. Dem Codecanbieter wird auch ein digitales Zertifikat ausgestellt, mit dem der Wert des Codecs überprüft wird. Um ein Zertifikat zu erhalten, senden Sie eine E-Mail-Anforderung an wmla@microsoft.com . Der Prozess zum Abrufen eines Zertifikats umfasst das Signieren einer Lizenz und das Bereitstellen eines Satzes von Informationsdateien für Microsoft.

Codec-Vorteile funktionieren wie folgt:

1.  Der Codecanbieter implementiert eine der folgenden Funktionen:
    -   Ein AVStream-Minitreiber. Media Foundation stellt einen Standardproxy-MFT für AVStream-Treiber bereit. Dies ist die empfohlene Option.
    -   Eine Media Foundation Transformation (MFT), die als Proxy für die Hardware fungiert. Weitere Informationen finden Sie unter [Hardware-MFTs.](hardware-mfts.md)
2.  Der Wert des Codecs wird zur schnellen Suche in der Registrierung gespeichert.
3.  Die [**MFTEnumEx-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) sortiert Codecs in der Reihenfolge der Vorteile. Codecs mit Mehrwertwerten werden in der Liste hinter lokal registrierten Codecs angezeigt (siehe [**MFTRegisterLocal**](/windows/desktop/api/mfapi/nf-mfapi-mftregisterlocal)), aber vor anderen Codecs.
4.  Wenn der MFT erstellt wird, wird die Leistung des Codecs mithilfe der OPM-API [(Output Protection Manager)](output-protection-manager.md) überprüft.
5.  Für einen Proxy-MFT implementiert der Codec die [**IOPMVideoOutput-Schnittstelle.**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) Für einen AVStream-Treiber implementiert der Codec den KSPROPSETID \_ OPMVideoOutput-Eigenschaftensatz.

Das folgende Diagramm zeigt, wie die Leistung in beiden Fällen überprüft wird:

![Diagramm mit zwei Prozessen: einer führt über media foundation proxy mft und avstream driver, der andere über benutzerdefinierte Proxy mft](images/codecmerit.png)

## <a name="custom-proxy-mft"></a>Benutzerdefinierter Proxy-MFT

Wenn Sie einen Proxy-MFT für den Hardwarecodec bereitstellen, implementieren Sie den Codecwert wie folgt:

1.  Implementieren Sie die [**IOPMVideoOutput-Schnittstelle**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) im MFT. Beispielcode wird im nächsten Abschnitt dieses Themas gezeigt.
2.  Fügen Sie der Registrierung das [Attribut MFT \_ CODEC ATTRIBUTE \_ \_ wie](mft-codec-merit-attribute.md) folgt hinzu:

    1.  Rufen Sie [**MFCreateAttributes**](/windows/desktop/api/mfapi/nf-mfapi-mfcreateattributes) auf, um einen neuen Attributspeicher zu erstellen.
    2.  Rufen Sie [**DIE ATTRIBUTEAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32) auf, um das [Attribut MFT CODEC \_ \_ ATTRIBUTE \_](mft-codec-merit-attribute.md) festzulegen. Der Wert des Attributs ist der zugewiesene Vorteil des Codecs.
    3.  Rufen Sie [**MFTRegister**](/windows/desktop/api/mfapi/nf-mfapi-mftregister) auf, um den MFT zu registrieren. Übergeben Sie den Attributspeicher im *pAttributes-Parameter.*

3.  Die Anwendung ruft [**MFTEnumEx auf.**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) Diese Funktion gibt ein Array von [**POINTERActivate-Zeigern**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) zurück, eines für jeden Codec, der den Enumerationskriterien entspricht.
4.  Die Anwendung ruft [**DIE AKTIONACTIVATE::ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) auf, um den MFT zu erstellen.
5.  Die [**ActivateObject-Methode**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) ruft die [**MFGetMFTMerit-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) auf, um das Zertifikat und den Wert zu überprüfen.
6.  Die [**MFGetMFTMerit-Funktion**](/windows/desktop/api/mfapi/nf-mfapi-mfgetmftmerit) ruft [**IOPMVideoOutput::GetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) auf und sendet eine [**OPM \_ GET CODEC \_ INFO-Statusanforderung. \_**](opm-get-codec-info.md) Diese Statusanforderung gibt den zugewiesenen Wert des Codecs zurück. Wenn dieser Wert nicht mit dem Registrierungswert übereinstimmt, schlägt [**ActivateObject**](/windows/desktop/api/mfobjects/nf-mfobjects-imfactivate-activateobject) möglicherweise fehl.

Der folgende Code zeigt, wie Sie der Registrierung beim Registrieren von MFT den Wert "value" hinzufügen:


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



### <a name="implementing-iopmvideooutput-for-codec-merit"></a>Implementieren von IOPMVideoOutput für Codecs

Der folgende Code zeigt, wie [**IOPMVideoOutput**](/windows/desktop/api/opmapi/nn-opmapi-iopmvideooutput) für Codecs implementiert wird. Eine allgemeinere Erläuterung der OPM-API finden Sie unter [Output Protection Manager](output-protection-manager.md).

> [!Note]  
> Der hier gezeigte Code enthält keine Verschleierung oder andere Sicherheitsmechanismen. Es soll die grundlegende Implementierung des OPM-Handshakes und der Statusanforderung anzeigen.

 

In diesem Beispiel wird davon ausgegangen, dass *g \_ TestCert* ein Bytearray ist, das die Zertifikatkette des Codecs enthält, und *g \_ PrivateKey* ein Bytearray, das den privaten Schlüssel aus dem Zertifikat enthält:


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



Generieren Sie in der [**IOPMVideoOutput::StartInitialization-Methode**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-startinitialization) eine Zufallszahl für den Handshake. Geben Sie diese Nummer und das Zertifikat an den Aufrufer zurück:


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



Die [**IOPMVideoOutput::FinishInitialization-Methode**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-finishinitialization) schließt den OPM-Handshake ab:


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



Implementieren Sie in der [**IOPMVideoOutput::GetInformation-Methode**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) die [**Statusanforderung OPM \_ GET CODEC \_ \_ INFO.**](opm-get-codec-info.md) Die Eingabedaten sind eine [**OPM \_ GET CODEC \_ INFO \_ \_ PARAMETERS-Struktur,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_parameters) die die CLSID Ihres MFT enthält. Die Ausgabedaten sind eine [**OPM \_ GET CODEC \_ INFO \_ \_ INFORMATION-Struktur,**](/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_codec_info_information) die den Codecverwerter enthält.


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



Die [**GetInformation-Methode**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-getinformation) muss einen Nachrichtenauthentifizierungscode (MAC) mit dem OMAC-1-Algorithmus berechnen. siehe [Berechnen des OMAC-1-Werts.](opm-example-code.md)

Es ist nicht erforderlich, andere OPM-Statusanforderungen zu unterstützen.

Die Methoden [**IOPMVideoOutput::COPPCompatibleGetInformation**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-coppcompatiblegetinformation) und [**IOPMVideoOutput::Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure) sind für codec-Vorteile nicht erforderlich, sodass diese Methoden **E \_ NOTIMPL** zurückgeben können.


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

 

 



