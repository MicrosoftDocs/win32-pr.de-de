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
ms.openlocfilehash: 64647cbcbcc836c400890fb173a29c76f8723029
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908808"
---
# <a name="null-renderer-filter"></a>NULL-Rendererfilter

> [!Note]  
> \[Veraltet. Diese API kann aus zukünftigen Versionen von Windows entfernt werden.\]

 

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
| [Verdienst](merit.md)                       | NICHT \_ \_ VERWENDEN \_                                                                                                  |
| [Filterkategorie](filter-categories.md) | CLSID \_ LegacyAmFilterCategory                                                                                        |



 

## <a name="remarks"></a>Bemerkungen

Verwenden Sie diesen Filter, wenn ein Ausgabepin im Diagramm eine Downstreamverbindung erfordert, Sie die Daten jedoch nicht von diesem Pin rendern möchten. Indem Sie den Ausgabepin mit dem NULL-Renderer verbinden, schließen Sie die Verbindung ab, ohne die Daten zu rendern.

Obwohl dieser Filter keine Stichproben rendert, wartet er auf die Präsentationszeit der einzelnen Stichproben, bevor das Beispiel verworfen wird. Daher wird das Diagramm mit der normalen Rate ausgeführt. Wenn das Diagramm so schnell wie möglich ausgeführt werden soll, legen Sie die Referenzuhr auf **NULL fest.** Weitere Informationen finden Sie unter [Setting the Graph Clock](setting-the-graph-clock.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------|------------------------------------------------------------------------------------|
| Header<br/> | <dl> <dt>Qedit.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[DirectShow Editing Services Objects](directshow-editing-services-objects.md)
</dt> </dl>

 

 




