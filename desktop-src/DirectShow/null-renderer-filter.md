---
description: Der NULL-rendererfilter ist ein Renderer, der alle empfangenen Beispiele verwirft, ohne die Beispiel Daten anzuzeigen oder zu rendern.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: NULL-rendererfilter (qedit. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Null Renderer Filter
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: 7ff6c728276ca3fd69c14e304780b1d70c563265
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106371418"
---
# <a name="null-renderer-filter"></a>NULL-rendererfilter

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

Der NULL-rendererfilter ist ein Renderer, der alle empfangenen Beispiele verwirft, ohne die Beispiel Daten anzuzeigen oder zu rendern.



|                                          |                                                                                                                      |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Filter Schnittstellen                        | [**Ibasefilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**imediaposition**](/windows/desktop/api/Control/nn-control-imediaposition), [**imediaseeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) |
| Eingabe-PIN-Medientypen                    | Beliebige Medientyp                                                                                                       |
| PIN-Eingabeschnittstellen                     | [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**iqualitycontrol**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)               |
| Ausgabe-PIN-Medientypen                   | Nicht zutreffend                                                                                                      |
| PIN-Schnittstellen                    | Nicht zutreffend                                                                                                      |
| CLSID Filtern                             | CLSID- \_ nullrenderer                                                                                                  |
| CLSID der Eigenschaften Seite                      | Keine Eigenschaften Seite.                                                                                                    |
| Ausführbare Datei                               | Qedit.dll                                                                                                            |
| [Verdienst](merit.md)                       | das Verdienst wird \_ \_ nicht \_ verwendet.                                                                                                  |
| [Filter Kategorie](filter-categories.md) | CLSID \_ legacyamfiltercategory                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diesen Filter, wenn eine Ausgabepin im Diagramm eine Downstreamverbindung erfordert, Sie aber nicht möchten, dass die Daten aus dieser Pin rendertet werden. Indem Sie die Ausgabe-PIN mit dem NULL-Renderer verbinden, vervollständigen Sie die Verbindung, ohne die Daten zu rendern.

Obwohl dieser Filter keine Beispiele renderei, wartet er auf die Präsentationszeit der einzelnen Beispiele, bevor das Beispiel verworfen wird. Daher wird das Diagramm mit dem normalen Satz ausgeführt. Wenn Sie möchten, dass das Diagramm so schnell wie möglich ausgeführt wird, legen Sie die Referenzuhr auf **null** fest. Weitere Informationen finden Sie unter [Festlegen der diagrammuhr](setting-the-graph-clock.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>"Qedit. h"</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow-Bearbeitungs Dienste-Objekte](directshow-editing-services-objects.md)
</dt> </dl>

 

 




