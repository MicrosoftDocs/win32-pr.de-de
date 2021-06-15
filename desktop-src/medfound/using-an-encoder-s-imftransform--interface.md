---
description: Zum Konvertieren von Mediendateien in das ASF-Format können Sie Windows Media Encoder verwenden. Erfahren Sie mehr über das Erstellen eines Encoders mit CoCreateInstance.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Erstellen eines Encoders mit coCreateInstance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15c4cdf7b72bbfee97031088502113d085738981
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112068466"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a>Erstellen eines Encoders mit coCreateInstance

Zum Konvertieren von Mediendateien in das ASF-Format können Sie Windows Media Encoder verwenden. Um diese Encoder verwenden zu können, müssen sie beim System registriert werden. Encoder werden als [Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) implementiert und müssen die INTERFACESTransform-Schnittstelle verfügbar machen. In diesem Thema wird beschrieben, wie eine Anwendung einen Zeiger auf die MSITransform-Schnittstelle des erforderlichen MFT-Encoders abrufen und zur Verwendung instanziieren kann.

Informationen zur Encoderregistrierung finden Sie unter [Instanziieren eines Encoder-MFT.](instantiating-the-encoder-mft.md)

-   [Verwenden der INTERFACESTransform-Schnittstelle eines Encoders](#creating-an-encoder-by-using-cocreateinstance)
    -   [Beispiel für die Encodererstellung](#encoder-creation-example)
-   [Verwandte Themen](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a>Verwenden der INTERFACESTransform-Schnittstelle eines Encoders

Nach erfolgreicher Registrierung von Windows Media Encodern beim System kann eine Anwendung die Encoder aufzählen, indem [**sie MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)aufruft. Um nach dem richtigen Encoder zu suchen, müssen Sie Folgendes angeben:

-   Die GUID, die die Kategorie darstellt, bei der es sich entweder um **MFT \_ CATEGORY AUDIO \_ \_ ENCODER** oder **MFT CATEGORY VIDEO ENCODER \_ \_ \_ handelt.**

-   Das abzugleichende Format. Dies wird in der [**MFT \_ REGISTER TYPE \_ \_ INFO-Struktur**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) festgelegt, die den Haupttyp und Untertyp des Medientyps angibt, in dem der Encoder Stichproben generiert. Diese Struktur wird im *pOutputType-Parameter* übergeben. Informationen zu den unterstützten Typen finden Sie unter [Medientyp-GUIDs.](media-type-guids.md)

    > [!Note]  
    > Die Eingabetypinformationen im *pInputType-Parameter* sind nicht erforderlich. Dies liegt daran, dass der Eingabetyp der Anwendung bekannt ist und der Encoder erwartet, dass der Eingabestream in einem nicht komprimierten Format vorliegt.

     

[**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) gibt ein Array von [**POINTERTransform-Zeigern**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) für die Encoder-MFTs zurück, die den Suchkriterien entsprechen. Sie können einen Encoder instanziieren, indem Sie die COM-Funktion **CoCreateInstance** aufrufen und die CLSID des Encoders übergeben, den Sie verwenden möchten. Diese Funktion gibt einen Zeiger auf die **INTERFACESTransform-Schnittstelle** zurück, die den Encoder darstellt. Weitere Informationen zu diesem Funktionsaufruf finden Sie in der Windows SDK-Dokumentation für die Component Object Model (COM).

### <a name="encoder-creation-example"></a>Beispiel für die Encodererstellung

Das folgende Codebeispiel zeigt, wie Sie einen Audio- oder Videoencoder erstellen.


```C++
HRESULT FindEncoder(
    const GUID& subtype, 
    BOOL bAudio, 
    IMFTransform **ppEncoder
    )
{
    HRESULT hr = S_OK;
    UINT32 count = 0;

    CLSID *ppCLSIDs = NULL;

    MFT_REGISTER_TYPE_INFO info = { 0 };

    info.guidMajorType = bAudio ? MFMediaType_Audio : MFMediaType_Video;
    info.guidSubtype = subtype;

    hr = MFTEnum(   
        bAudio ? MFT_CATEGORY_AUDIO_ENCODER : MFT_CATEGORY_VIDEO_ENCODER,
        0,          // Reserved
        NULL,       // Input type
        &info,      // Output type
        NULL,       // Reserved
        &ppCLSIDs,
        &count
        );

    if (SUCCEEDED(hr) && count == 0)
    {
        hr = MF_E_TOPO_CODEC_NOT_FOUND;
    }

    // Create the first encoder in the list.

    if (SUCCEEDED(hr))
    {
        hr = CoCreateInstance(ppCLSIDs[0], NULL,
            CLSCTX_INPROC_SERVER, IID_PPV_ARGS(ppEncoder));
    }

    CoTaskMemFree(ppCLSIDs);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Instanziieren eines Encoder-MFT](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 



