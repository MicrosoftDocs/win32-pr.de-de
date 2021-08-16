---
description: Die IMediaDet-Schnittstelle ruft Informationen zu einer Mediendatei ab, z. B. die Anzahl der Streams, den Medientyp, die Dauer und die Bildfrequenz jedes Streams.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: IMediaDet-Schnittstelle (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMediaDet
api_type:
- COM
api_location:
- strmiids.lib
- strmiids.dll
ms.openlocfilehash: abdf913ab74e6f0f988449a14b84b5be109b9380ebbfb2473edd4a9980f3c577
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117819032"
---
# <a name="imediadet-interface"></a>IMediaDet-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Releases von Windows.\]

 

Die -Schnittstelle ruft Informationen zu einer Mediendatei ab, z. B. die Anzahl der Streams, den Medientyp, die Dauer und die `IMediaDet` Bildfrequenz jedes Streams. Sie enthält auch Methoden zum Abrufen einzelner Frames aus einem Videostream. Das [Media Detector-Objekt (MediaDet)](media-detector--mediadet.md) macht diese Schnittstelle verfügbar.

Führen Sie die folgenden Schritte aus, um Informationen zu einer Datei über diese Schnittstelle zu erhalten:

1.  Erstellen Sie eine Instanz des MediaDet-Objekts, indem Sie **CoCreateInstance aufrufen.** Die Klassen-ID ist CLSID \_ MediaDet.
2.  Rufen [**Sie IMediaDet::p ut \_ Filename**](imediadet-put-filename.md) auf, um den Namen der Quelldatei anzugeben.
3.  Rufen [**Sie IMediaDet::get \_ OutputStreams auf,**](imediadet-get-outputstreams.md) um die Anzahl der Ausgabestreams in der Quelle zu erhalten.
4.  Rufen [**Sie IMediaDet::p ut \_ CurrentStream auf,**](imediadet-put-currentstream.md) um einen bestimmten Stream anzugeben.
5.  Rufen Sie eine der folgenden Methoden auf:
    -   [**IMediaDet::get \_ FrameRate**](imediadet-get-framerate.md)
    -   [**IMediaDet::get \_ StreamLength**](imediadet-get-streamlength.md)
    -   [**IMediaDet::get \_ StreamMediaType**](imediadet-get-streammediatype.md)
    -   [**IMediaDet::get \_ StreamType**](imediadet-get-streamtype.md)

Rufen Sie zum Abrufen eines [**Videoframes IMediaDet::GetBitmapBits**](imediadet-getbitmapbits.md) oder [**IMediaDet::WriteBitmapBits auf.**](imediadet-writebitmapbits.md) Der zurückgegebene Frame hat immer das 24-Bit-RGB-Format.

> [!Note]  
> Verwenden Sie nicht dasselbe MediaDet-Objekt mit mehreren Dateien. Verwenden Sie separate MediaDet-Instanzen, um Informationen oder Videoframes aus mehr als einer Datei zu erhalten.

 

Die **IMediaDet-Schnittstelle** unterstützt [**keine VIDEOINFOHEADER2-Formate,**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) daher können Sie diese Schnittstelle nicht verwenden, um Interlacingfelder oder Informationen zum Interlacing zu erhalten. Wenn der Upstreamdecoder nur **VIDEOINFOHEADER2 unterstützt,** können Sie auch nicht `IMediaDet` verwenden. Dies kann beispielsweise bei einem MPEG-2-Decoder der Fall sein. Außerdem ignoriert die Schnittstelle alle Streams in der Datei, `IMediaDet` die keine Video- oder Audiodaten sind. Wenn die Datei z. B. einen Audiostream, einen Datenstrom und einen Videostream enthält, werden von der **\_ Get OutputStreams-Methode** nur zwei Streams (Audio und Video) ausgegeben.

## <a name="members"></a>Member

Die **IMediaDet-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/win32/api/unknwn/nn-unknwn-iunknown) **IMediaDet verfügt** auch über diese Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMediaDet-Schnittstelle** verfügt über diese Methoden.



| Methode                                                        | Beschreibung                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**EnterBitmapGrabMode**](imediadet-enterbitmapgrabmode.md)  | Schaltet die Medienerkennung in den Bitmap-Greifmodus um und sucht das Filterdiagramm zu einem angegebenen Zeitpunkt.<br/> |
| [**Get \_ CurrentStream**](imediadet-get-currentstream.md)     | Ruft die Datenstromnummer ab, die derzeit von der Medienerkennung verwendet wird.<br/>                               |
| [**Get \_ Filename**](imediadet-get-filename.md)               | Ruft den Namen der Quelldatei ab, die derzeit von der Medienerkennung verwendet wird.<br/>                     |
| [**Filter \_ "get"**](imediadet-get-filter.md)                   | Ruft einen Zeiger auf den Quellfilter ab, der derzeit von der Medienerkennung verwendet wird.<br/>                  |
| [**Get \_ FrameRate**](imediadet-get-framerate.md)             | Ruft die Framerate des aktuellen Streams ab.<br/>                                                 |
| [**Get \_ OutputStreams**](imediadet-get-outputstreams.md)     | Ruft die Anzahl der Audio- und Videostreams ab, die in der Medienquelle enthalten sind.<br/>                  |
| [**Get \_ StreamLength**](imediadet-get-streamlength.md)       | Ruft die Dauer des aktuellen Streams ab.<br/>                                                   |
| [**get \_ StreamMediaType**](imediadet-get-streammediatype.md) | Ruft den Medientyp des aktuellen Streams ab.<br/>                                                 |
| [**get \_ StreamType**](imediadet-get-streamtype.md)           | Ruft den GUID (Globally Unique Identifier) für den Medientyp des aktuellen Streams ab.<br/>       |
| [**Get \_ StreamTypeB**](imediadet-get-streamtypeb.md)         | Ruft eine Zeichenfolge ab, die die GUID des Medientyps für den aktuellen Stream darstellt.<br/>              |
| [**GetBitmapBits**](imediadet-getbitmapbits.md)              | Ruft einen Videoframe zur angegebenen Medienzeit ab.<br/>                                            |
| [**GetSampleGrabber**](imediadet-getsamplegrabber.md)        | Ruft einen Zeiger auf die [**ISampleGrabber-Schnittstelle**](isamplegrabber.md) ab.<br/>                  |
| [**put \_ CurrentStream**](imediadet-put-currentstream.md)     | Gibt die Datenstromnummer an, die von der Medienerkennung verwendet werden soll.<br/>                                      |
| [**put \_ Filename**](imediadet-put-filename.md)               | Gibt den Namen der Quelldatei an, die von der Medienerkennung verwendet werden soll.<br/>                            |
| [**Put \_ Filter**](imediadet-put-filter.md)                   | Gibt einen Quellfilter an, der von der Medienerkennung verwendet werden soll.<br/>                                        |
| [**WriteBitmapBits**](imediadet-writebitmapbits.md)          | Ruft einen Videoframe zur angegebenen Medienzeit ab und schreibt ihn in eine Datei.<br/>                    |



 

## <a name="remarks"></a>Hinweise

> [!Note]  
> Die Headerdatei Qedit.h ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Um Qedit.h zu erhalten, laden Sie das Microsoft Windows SDK-Update für Windows Vista und [.NET Framework 3.0 herunter.](https://msdn.microsoft.com/windowsvista/bb980924.aspx) Qedit.h ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3.5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>Qedit.h</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>Strmiids.lib</dt> </dl> |



 

 
