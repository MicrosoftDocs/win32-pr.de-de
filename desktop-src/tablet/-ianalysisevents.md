---
description: Gibt Ereignisse an, die den Analyseschritten eines IInkAnalyzer-Objekts zugeordnet sind.
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
ms.openlocfilehash: 2f49455e3e6fb68b2884cda380c304d7655b70d49ff338bcfb7c36904b449019
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452165"
---
# <a name="_ianalysisevents-interface"></a>\_IAnalysisEvents-Schnittstelle

Gibt Ereignisse an, die den Analyseschritten eines [**IInkAnalyzer-Objekts**](iinkanalyzer.md) zugeordnet sind.

-   [Ereignisse](/windows)

### <a name="events"></a>Ereignisse

Die **\_ IAnalysisEvents-Schnittstelle** verfügt über diese Ereignisse.



| Ereignis                                                               | BESCHREIBUNG                                                                                                                                                                                    |
|:--------------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Aktivität**](-ianalysisevents-activity.md)                       | Tritt bei Aufrufen der [**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md) oder [**der IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md) auf.<br/> |
| [**IntermediateResults**](-ianalysisevents-intermediateresults.md) | Tritt ein, wenn die aktuelle Zwischenanalysephase abgeschlossen ist.<br/>                                                                                                                    |
| [**Readytoreconcile**](-ianalysisevents-readytoreconcile.md)       | Tritt ein, wenn [**der IInkAnalyzer**](iinkanalyzer.md) bereit ist, seine Hintergrundanalyseergebnisse mit dem aktuellen Zustand abzustimmen.<br/>                                                  |
| [**Ergebnisse**](-ianalysisevents-results.md)                         | Tritt ein, wenn die letzte Analysephase abgeschlossen ist.<br/>                                                                                                                                   |
| [**UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)   | Tritt ein, bevor [**IInkAnalyzer**](iinkanalyzer.md) auf Strichdaten zugreift.<br/>                                                                                                        |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/> |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                     |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

