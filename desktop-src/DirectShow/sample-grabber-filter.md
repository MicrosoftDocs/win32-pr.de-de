---
description: Der Sample Grabber-Filter bietet eine Möglichkeit zum Abrufen von Beispielen beim Durchlaufen des Filter Diagramms.
ms.assetid: 3c2fb52f-2b44-449a-ae96-3cf35a0a401d
title: Beispiel für einen Grabber Filter (qedit. h)
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
ms.openlocfilehash: 18cedd24b0ddcb8f71373641905228f8252ae4ef
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368303"
---
# <a name="sample-grabber-filter"></a>Beispiel für einen Grabber Filter

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Der Sample Grabber-Filter bietet eine Möglichkeit zum Abrufen von Beispielen beim Durchlaufen des Filter Diagramms. Es handelt sich um einen Transformations Filter mit einer Eingabe-und einer Ausgabepin. Alle Beispiele bleiben unverändert, sodass Sie Sie in ein Filter Diagramm einfügen können, ohne den Datenstream zu ändern. Die Anwendung kann dann einzelne Beispiele aus dem Filter abrufen, indem Sie Methoden für die [**isamplegrabber**](isamplegrabber.md) -Schnittstelle aufrufen.

Wenn Sie Beispiele abrufen möchten, ohne die Daten zu rendern, verbinden Sie den Sample Grabber Filter mit dem Filter [**null-Renderer**](null-renderer-filter.md) .



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **isamplegrabber**](isamplegrabber.md)                                                                       |
| Eingabe-PIN-Medientypen                    | Ein beliebiger Medientyp.                                                                                                                                    |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)                                             |
| Ausgabe-PIN-Medientypen                   | Ein beliebiger Medientyp. Entspricht dem Eingabe Medientyp.                                                                                                          |
| PIN-Schnittstellen                    | [**Imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol) |
| CLSID Filtern                             | CLSID- \_ samplegrabber                                                                                                                               |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite.                                                                                                                                  |
| Ausführbare Datei                               | Qedit.dll                                                                                                                                          |
| [Verdienst](merit.md)                       | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                                                                |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                                                      |



 

## <a name="remarks"></a>Bemerkungen

Wenn Sie diesen Filter verwenden möchten, fügen Sie ihn dem Filter Diagramm hinzu, und nennen Sie [**isamplegrabber:: setmediatype**](isamplegrabber-setmediatype.md) mit dem gewünschten Medientyp. Diese Methode gibt den Medientyp für die Eingabe-und Ausgabe-PIN-Verbindungen des Filters an. Verbinden Sie den Filter dann mit anderen Filtern im Diagramm.

Wenn Sie [**isamplegrabber:: setbuffersamples**](isamplegrabber-setbuffersamples.md) mit dem Wert **true** aufrufen, puffert der Filter jedes empfangene Beispiel, bevor es nach unten übergeben wird. Rufen Sie die [**isamplegrabber:: getcurrentbuffer**](isamplegrabber-getcurrentbuffer.md) -Methode auf, um den aktuellen Inhalt des Puffers abzurufen. Alternativ können Sie [**isamplegrabber:: SetCallback**](isamplegrabber-setcallback.md) aufrufen, damit der Filter immer dann eine Rückruffunktion aufruft, wenn er ein Beispiel empfängt.

Für den Filter gelten die folgenden Einschränkungen für Videoformate:

-   Video Typen mit der Top-Down-Ausrichtung (negative **biheight**) werden nicht unterstützt.
-   Die [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) -Format Struktur (formatType entspricht **Format \_ VideoInfo2**) wird nicht unterstützt.
-   Alle Videotypen, bei denen der Surface-Stride nicht mit der Video Breite identisch ist, werden abgelehnt.

Folglich stellt der Sample Grabber für einige Video Typen keine Verbindung mit dem Video Mischungs-Renderer (VMR) her.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Qedit. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Bearbeitungs Dienste-Objekte](directshow-editing-services-objects.md)
</dt> <dt>

[Verwenden der Beispiel-Grabber](using-the-sample-grabber.md)
</dt> </dl>

 

 




