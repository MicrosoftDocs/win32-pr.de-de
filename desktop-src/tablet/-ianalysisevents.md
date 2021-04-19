---
description: Gibt Ereignisse an, die den Analyse Schritten eines iinkanalyzer-Objekts zugeordnet sind.
ms.assetid: 8cb75f99-aa39-44d1-a055-dc1fb3f6b292
title: _IAnalysisEvents-Schnittstelle
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents
api_type:
- COM
api_location: ''
ms.openlocfilehash: 90e32669d8b542202f6166052c072f224bb2954a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360681"
---
# <a name="_ianalysisevents-interface"></a>\_Ianalysil Vents-Schnittstelle

Gibt Ereignisse an, die den Analyse Schritten eines [**iinkanalyzer**](iinkanalyzer.md) -Objekts zugeordnet sind.

-   [Ereignisse](/windows)

### <a name="events"></a>Ereignisse

Die **\_ ianalysil Vents** -Schnittstelle enthält diese Ereignisse.



| Ereignis                                                               | BESCHREIBUNG                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktivität**](-ianalysisevents-activity.md)                       | Tritt bei Aufrufen der [**iinkanalyzer:: Analysis-Methode**](iinkanalyzer-analyze.md) oder der [**iinkanalyzer:: BackgroundAnalyze-Methoden**](iinkanalyzer-backgroundanalyze.md) Methode auf.<br/> |
| [**IntermediateResults**](-ianalysisevents-intermediateresults.md) | Tritt auf, wenn die aktuelle zwischen Analysephase abgeschlossen ist.<br/>                                                                                                                    |
| [**"Read ytor econcile"**](-ianalysisevents-readytoreconcile.md)       | Tritt auf, wenn [**iinkanalyzer**](iinkanalyzer.md) bereit ist, die Ergebnisse der Hintergrundanalyse mit dem aktuellen Zustand abzustimmen.<br/>                                                  |
| [**Ergebnisse**](-ianalysisevents-results.md)                         | Tritt auf, wenn die abschließende Analysephase abgeschlossen ist.<br/>                                                                                                                                   |
| [**Updatestrokescache**](-ianalysisevents-updatestrokescache.md)   | Tritt auf, bevor der [**iinkanalyzer**](iinkanalyzer.md) auf Stroke-Daten zugreift.<br/>                                                                                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_Ianalysisproxyevents**](-ianalysisproxyevents.md)
</dt> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

