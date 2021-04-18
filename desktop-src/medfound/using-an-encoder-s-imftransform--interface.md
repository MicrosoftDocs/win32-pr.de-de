---
description: Zum Umstellen von Mediendateien in das ASF-Format können Sie Windows Media Encoder verwenden. Um diese Encoder verwenden zu können, müssen Sie beim System registriert werden.
ms.assetid: 96f19dfb-a328-41db-8fa8-77f052b1a192
title: Erstellen eines Encoders mithilfe von cokreateingestance
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28a19a3ec13f60e7f602fa4f16854efa060dd96d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358811"
---
# <a name="creating-an-encoder-by-using-cocreateinstance"></a>Erstellen eines Encoders mithilfe von cokreateingestance

Zum Umstellen von Mediendateien in das ASF-Format können Sie Windows Media Encoder verwenden. Um diese Encoder verwenden zu können, müssen Sie beim System registriert werden. Encoder werden als [Media Foundation Transformationen](media-foundation-transforms.md) (MFTs) implementiert und müssen die IMF Transform-Schnittstelle verfügbar machen. In diesem Thema wird beschrieben, wie eine Anwendung einen Zeiger auf die imftransform-Schnittstelle des erforderlichen MFT-Encoders erhält und diese für die Verwendung instanziieren kann.

Weitere Informationen zur encoderregistrierung finden Sie unter [Instanziieren eines Encoders MFT](instantiating-the-encoder-mft.md).

-   [Verwenden der IMF Transform-Schnittstelle eines Encoders](#creating-an-encoder-by-using-cocreateinstance)
    -   [Beispiel für Codierungs Erstellung](#encoder-creation-example)
-   [Zugehörige Themen](#related-topics)

## <a name="using-an-encoders-imftransform-interface"></a>Verwenden der IMF Transform-Schnittstelle eines Encoders

Nach erfolgreicher Registrierung von Windows Media Encoder beim System kann eine Anwendung die Encoder durch Aufrufen von [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum)auflisten. Um nach dem richtigen Encoder zu suchen, müssen Sie Folgendes angeben:

-   Die GUID, die die Kategorie darstellt, bei der es sich entweder um einen **\_ \_ \_ Audioencoder der MFT-Kategorie** oder um einen **\_ \_ Video \_ Encoder für die MFT**

-   Das Format, das verglichen werden soll. Dies wird in der [**MFT- \_ Register \_ Type \_ Info**](/windows/win32/api/mfobjects/ns-mfobjects-mft_register_type_info) -Struktur festgelegt, die den Haupttyp und den Untertyp des Medientyps angibt, in dem der Encoder Beispiele generiert. Diese Struktur wird im *poutputtype* -Parameter übergeben. Informationen zu den unterstützten Typen finden Sie unter [Medientyp-GUIDs](media-type-guids.md).

    > [!Note]  
    > Die Eingabetyp Informationen im *pinputtype* -Parameter sind nicht erforderlich. Dies liegt daran, dass der Eingabetyp der Anwendung bekannt ist und der Encoder erwartet, dass der Eingabedaten Strom ein unkomprimiertes Format hat.

     

[**Mfitenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) gibt ein Array von [**IMF Transform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Zeigern für die Encoder-MFTs zurück, die den Suchkriterien entsprechen. Sie können einen Encoder instanziieren, indem Sie die com-Funktion **CoCreateInstance** aufrufen und die CLSID des Encoders übergeben, den Sie verwenden möchten. Diese Funktion gibt einen Zeiger auf die **imftransform** -Schnittstelle zurück, die den Encoder darstellt. Weitere Informationen zu diesem Funktions aufzurufen finden Sie in der Windows SDK-Dokumentation für die Component Object Model (com).

### <a name="encoder-creation-example"></a>Beispiel für Codierungs Erstellung

Im folgenden Codebeispiel wird gezeigt, wie ein Audio-oder Video Encoder erstellt wird.


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

[Instanziieren eines MFT-Encoders](instantiating-the-encoder-mft.md)
</dt> <dt>

[Windows Media Encoder](windows-media-encoders.md)
</dt> </dl>

 

 



