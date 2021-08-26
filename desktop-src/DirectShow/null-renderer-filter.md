---
description: Der Nullrendererfilter ist ein Renderer, der jedes empfangene Beispiel verwirft, ohne die Beispieldaten anzuzeigen oder zu rendern.
ms.assetid: 2954762d-2ae6-4e38-ac88-5390a081897e
title: NULL-Rendererfilter (Qedit.h)
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
ms.openlocfilehash: 2686c64b3251616ac8cefbe81a77282e5b1a7c6847ef965b6361759118b74756
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050880"
---
# <a name="null-renderer-filter"></a>NULL-Rendererfilter

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Releases von Windows entfernt werden.\]

 

Der Nullrendererfilter ist ein Renderer, der jedes empfangene Beispiel verwirft, ohne die Beispieldaten anzuzeigen oder zu rendern.



| Bezeichnung | Wert |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------|
| Filterschnittstellen                        | [**IBaseFilter,**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) [**IMediaPosition,**](/windows/desktop/api/Control/nn-control-imediaposition) [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) |
| Eingabepinmedientypen                    | Beliebiger Medientyp                                                                                                       |
| Eingabepinschnittstellen                     | [**IMemInputPin,**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) [**IPin,**](/windows/desktop/api/Strmif/nn-strmif-ipin) [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)               |
| Medientypen des Ausgabepins                   | Nicht zutreffend                                                                                                      |
| Ausgabepinschnittstellen                    | Nicht zutreffend                                                                                                      |
| Filtern von CLSID                             | CLSID \_ NullRenderer                                                                                                  |
| CLSID der Eigenschaftenseite                      | Keine Eigenschaftenseite.                                                                                                    |
| Ausführbare Datei                               | Qedit.dll                                                                                                            |
| [Verdienst](merit.md)                       | NOT USE (NICHT \_ \_ \_ VERWENDEN)                                                                                                  |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                        |



 

## <a name="remarks"></a>Hinweise

Verwenden Sie diesen Filter, wenn ein Ausgabepin im Diagramm eine Downstreamverbindung erfordert, Sie die Daten jedoch nicht von diesem Pin rendern möchten. Indem Sie den Ausgabepin mit dem NULL-Renderer verbinden, schließen Sie die Verbindung ab, ohne die Daten zu rendern.

Obwohl dieser Filter keine Stichproben rendert, wartet er auf die Präsentationszeit der einzelnen Stichproben, bevor das Beispiel verworfen wird. Daher wird das Diagramm mit der normalen Rate ausgeführt. Wenn sie möchten, dass das Diagramm so schnell wie möglich ausgeführt wird, legen Sie die Verweisuhr auf **NULL** fest. Weitere Informationen finden Sie unter [Festlegen der Graph Uhr](setting-the-graph-clock.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[DirectShow Editing Services-Objekte](directshow-editing-services-objects.md)
</dt> </dl>

 

 




