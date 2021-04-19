---
description: Die imediadet-Schnittstelle ruft Informationen über eine Mediendatei ab, wie z. b. die Anzahl der Streams sowie den Medientyp, die Dauer und die Framerate der einzelnen Datenströme.
ms.assetid: 596fc84e-a88a-4e1b-aa48-b6dc9031db31
title: Imediadet-Schnittstelle (qedit. h)
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
ms.openlocfilehash: ca5c87a1424872491aba5dcf4e01011872e9ff36
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369415"
---
# <a name="imediadet-interface"></a>Imediadet-Schnittstelle

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Die `IMediaDet` -Schnittstelle ruft Informationen zu einer Mediendatei ab, z. b. die Anzahl der Streams und den Medientyp, die Dauer und die Framerate der einzelnen Datenströme. Sie enthält auch Methoden zum Abrufen einzelner Frames aus einem Videostream. Das [Media Detector-Objekt (mediadet)](media-detector--mediadet.md) macht diese Schnittstelle verfügbar.

Führen Sie die folgenden Schritte aus, um Informationen zu einer Datei zu erhalten, die diese Schnittstelle verwendet:

1.  Erstellen Sie eine Instanz des mediadet-Objekts durch Aufrufen von **CoCreateInstance**. Die Klassen-ID ist CLSID \_ mediadet.
2.  Nennen Sie [**imediadet::p UT \_ filename**](imediadet-put-filename.md) , um den Namen der Quelldatei anzugeben.
3.  Rufen Sie [**imediadet:: get \_ outputstreams**](imediadet-get-outputstreams.md) auf, um die Anzahl der Ausgabedaten Ströme in der Quelle abzurufen.
4.  Nennen Sie [**imediadet::p UT \_ currentstream**](imediadet-put-currentstream.md) , um einen bestimmten Stream anzugeben.
5.  Wenden Sie eine der folgenden Methoden an:
    -   [**Imediadet:: get \_ Framerate**](imediadet-get-framerate.md)
    -   [**Imediadet:: get \_ streamlength**](imediadet-get-streamlength.md)
    -   [**Imediadet:: get \_ streammediatype**](imediadet-get-streammediatype.md)
    -   [**Imediadet:: get \_ Streamtype**](imediadet-get-streamtype.md)

Um einen Videorahmen abzurufen, rufen Sie [**imediadet:: getbitmapbits**](imediadet-getbitmapbits.md) oder [**imediadet:: Write-Bitmapbits**](imediadet-writebitmapbits.md)auf. Der zurückgegebene Frame weist immer das 24-Bit-RGB-Format auf.

> [!Note]  
> Verwenden Sie nicht dasselbe mediadet-Objekt mit mehreren Dateien. Um Informationen oder Video Frames aus mehr als einer Datei zu erhalten, verwenden Sie separate mediadet-Instanzen.

 

Die **imediadet** -Schnittstelle unterstützt keine [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Formate, sodass Sie diese Schnittstelle nicht verwenden können, um Zeilen Sprung Felder oder Informationen über das Durchschneiden zu erhalten. Auch wenn der upstreamdecoder nur **VIDEOINFOHEADER2** unterstützt, können Sie nicht verwenden `IMediaDet` . Dies kann beispielsweise bei einem MPEG-2-Decoder der Fall sein. Außerdem ignoriert die- `IMediaDet` Schnittstelle alle Streams in der Datei, die keine Video-oder Audiodaten sind. Wenn die Datei z. b. einen Audiostream, einen Datenstrom und einen Videostream enthält, meldet die **get \_ outputstreams** -Methode nur zwei Streams (Audiodaten und Videos).

## <a name="members"></a>Member

Die **imediadet** -Schnittstelle erbt von der [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imediadet** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **imediadet** -Schnittstelle verfügt über diese Methoden.



| Methode                                                        | BESCHREIBUNG                                                                                                |
|:--------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------|
| [**Enterbitmapgrabmode**](imediadet-enterbitmapgrabmode.md)  | Schaltet den Medien Detektor in den bitmapingmodus um und sucht das Filter Diagramm zu einem bestimmten Zeitpunkt.<br/> |
| [**\_currentstream erhalten**](imediadet-get-currentstream.md)     | Ruft die streamnummer ab, die derzeit vom Medien Erkennungs Modul verwendet wird.<br/>                               |
| [**\_Dateiname erhalten**](imediadet-get-filename.md)               | Ruft den Namen der Quelldatei ab, die derzeit vom Medien Erkennungs Modul verwendet wird.<br/>                     |
| [**\_Filter erhalten**](imediadet-get-filter.md)                   | Ruft einen Zeiger auf den Quell Filter ab, der derzeit vom Medien Erkennungs Modul verwendet wird.<br/>                  |
| [**\_Framerate erhalten**](imediadet-get-framerate.md)             | Ruft die Framerate des aktuellen Streams ab.<br/>                                                 |
| [**get \_ outputstreams**](imediadet-get-outputstreams.md)     | Ruft die Anzahl der in der Medienquelle enthaltenen Audiodaten und Videostreams ab.<br/>                  |
| [**\_streamlength erhalten**](imediadet-get-streamlength.md)       | Ruft die Dauer des aktuellen Streams ab.<br/>                                                   |
| [**get \_ streammediatype**](imediadet-get-streammediatype.md) | Ruft den Medientyp des aktuellen Streams ab.<br/>                                                 |
| [**\_Streamtype aufrufen**](imediadet-get-streamtype.md)           | Ruft den Globally Unique Identifier (GUID) für den Medientyp des aktuellen Streams ab.<br/>       |
| [**\_streamtypeb aufrufen**](imediadet-get-streamtypeb.md)         | Ruft eine Zeichenfolge ab, die die GUID des Medientyps für den aktuellen Stream darstellt.<br/>              |
| [**Getbitmapbits**](imediadet-getbitmapbits.md)              | Ruft einen Videoframe zum angegebenen Zeitpunkt der Medien ab.<br/>                                            |
| [**Getsamplegrabber**](imediadet-getsamplegrabber.md)        | Ruft einen Zeiger auf die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle ab.<br/>                  |
| [**\_currentstream platzieren**](imediadet-put-currentstream.md)     | Gibt die Datenstrom Nummer an, die vom Medien Detektor verwendet werden soll.<br/>                                      |
| [**\_Dateiname einfügen**](imediadet-put-filename.md)               | Gibt den Namen der Quelldatei an, die vom Medien Detektor verwendet werden soll.<br/>                            |
| [**\_Filter platzieren**](imediadet-put-filter.md)                   | Gibt einen Quell Filter für das zu verwendende Medien Erkennungs Modul an.<br/>                                        |
| [**"Beschreib tebitmapbits"**](imediadet-writebitmapbits.md)          | Ruft einen Videoframe zum angegebenen Zeitpunkt der Medien ab und schreibt ihn in eine Datei.<br/>                    |



 

## <a name="remarks"></a>Bemerkungen

> [!Note]  
> Die Header Datei "qedit. h" ist nicht mit Direct3D-Headern nach Version 7 kompatibel.

 

> [!Note]  
> Zum Abrufen von "qedit. h" Laden Sie das [Microsoft Windows SDK Update für Windows Vista und .NET Framework 3,0](https://msdn.microsoft.com/windowsvista/bb980924.aspx)herunter. "Qedit. h" ist im Microsoft Windows SDK für Windows 7 und .NET Framework 3,5 Service Pack 1 nicht verfügbar.

 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|--------------------|-----------------------------------------------------------------------------------------|
| Header<br/>  | <dl> <dt>"Qedit. h"</dt> </dl>      |
| Bibliothek<br/> | <dl> <dt>"" "" ". Lib"</dt> </dl> |



 

 
