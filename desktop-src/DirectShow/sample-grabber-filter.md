---
description: Der Filter Sample Grabber bietet eine Möglichkeit zum Abrufen von Stichproben, wenn sie durch das Filterdiagramm übergeben werden.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Beispielgrabfilter (Qedit.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Sample
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f0b0ddffe2bc769b7c2371ef93091d8c1daf379c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909668"
---
# <a name="sample-grabber-filter"></a>Beispielgrabfilter

> [!Note]  
> \[Veraltet. Diese API wird möglicherweise aus zukünftigen Versionen von Windows entfernt.\]

 

Der Filter Sample Grabber bietet eine Möglichkeit zum Abrufen von Stichproben, wenn sie durch das Filterdiagramm übergeben werden. Es handelt sich um einen Transformationsfilter mit einem Eingabepin und einem Ausgabepin. Alle Stichproben werden unverändert nachgelagert übergibt, sodass Sie sie in ein Filterdiagramm einfügen können, ohne den Datenstrom zu ändern. Ihre Anwendung kann dann einzelne Beispiele aus dem Filter abrufen, indem sie Methoden auf der [**ISampleGrabber-Schnittstelle**](isamplegrabber.md) aufruft.

Wenn Sie Beispiele abrufen möchten, ohne die Daten zu rendern, verbinden Sie den Sample Grabber-Filter mit dem [**Filter NULL-Renderer.**](null-renderer-filter.md)



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filtern von Schnittstellen                        | [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **ISampleGrabber**](isamplegrabber.md)                                                                       |
| Eingabepin-Medientypen                    | Ein beliebiger Medientyp.                                                                                                                                    |
| Eingabepinschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Ausgabepin-Medientypen                   | Ein beliebiger Medientyp. Entspricht dem Eingabemedientyp.                                                                                                          |
| Schnittstellen für Ausgabepins                    | [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking,**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| Filtern von CLSID                             | CLSID \_ SampleGrabber                                                                                                                               |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite.                                                                                                                                  |
| Ausführbare Datei                               | Qedit.dll                                                                                                                                          |
| [Verdienst](merit.md)                       | NOT USE (NICHT \_ \_ \_ VERWENDEN)                                                                                                                                |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Um diesen Filter zu verwenden, fügen Sie ihn dem Filterdiagramm hinzu, und rufen [**Sie ISampleGrabber::SetMediaType**](isamplegrabber-setmediatype.md) mit dem gewünschten Medientyp auf. Diese Methode gibt den Medientyp für die Ein- und Ausgabe-PIN-Verbindungen des Filters an. Verbinden Sie den Filter dann mit anderen Filtern im Diagramm.

Wenn Sie [**ISampleGrabber::SetBufferSamples**](isamplegrabber-setbuffersamples.md) mit dem Wert **TRUE** aufrufen, puffert der Filter jedes empfangene Beispiel, bevor er es nachgeschaltet übergibt. Rufen Sie die [**ISampleGrabber::GetCurrentBuffer-Methode**](isamplegrabber-getcurrentbuffer.md) auf, um den aktuellen Inhalt des Puffers abzurufen. Alternativ können Sie [**ISampleGrabber::SetCallback**](isamplegrabber-setcallback.md) aufrufen, damit der Filter immer dann eine Rückruffunktion aufruft, wenn er ein Beispiel empfängt.

Der Filter weist die folgenden Einschränkungen für Videoformate auf:

-   Videotypen mit top-down-Ausrichtung (negative **biHeight)** werden nicht unterstützt.
-   Die [**Formatstruktur VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) wird nicht unterstützt (Formattyp entspricht **FORMAT \_ VideoInfo2**).
-   Sie lehnt alle Videotypen ab, bei denen der Oberflächenschritt nicht mit der Videobreite übereinstimmt.

Daher stellt der Sample Grabber für einige Videotypen keine Verbindung mit dem Video Mixing Renderer (VMR) herstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow Editing Services Objects](directshow-editing-services-objects.md)
</dt> <dt>

[Verwenden des Beispielgrabbers](using-the-sample-grabber.md)
</dt> </dl>

 

 




