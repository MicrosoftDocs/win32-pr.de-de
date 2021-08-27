---
description: Tritt ein, wenn der IInkAnalyzer bereit ist, seine Hintergrundanalyseergebnisse mit dem aktuellen Zustand abzustimmen.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: _IAnalysisEvents::ReadyToReconcile-Ereignis (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.ReadyToReconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b65606675d8ae5aed694df87f35667a71fad2576344231a4e329783be4b31426
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120111270"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a>\_IAnalysisEvents::ReadyToReconcile-Ereignis

Tritt ein, wenn [**der IInkAnalyzer**](iinkanalyzer.md) bereit ist, seine Hintergrundanalyseergebnisse mit dem aktuellen Zustand abzustimmen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis verfügt über keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

[**IInkAnalyzer**](iinkanalyzer.md) führt eine automatische Abstimmung durch, wenn das **AnalysisModes \_ AutomaticReconciliation-Flag** des Freihandanalysetools festgelegt ist (siehe [**IInkAnalyzer::SetAnalysisModes-Methode).**](iinkanalyzer-setanalysismodes.md) Wenn das **AnalysisModes \_ AutomaticReconciliation-Flag** nicht festgelegt ist, muss Ihre Anwendung die Ergebnisse der Hintergrundanalyse manuell abstimmen.

Führen Sie die folgenden Schritte aus, um eine manuelle Abstimmung durchzuführen.

1.  Löschen Sie das **AnalysisModes \_ AutomaticReconciliation-Flag** des Freihandanalysetools.
2.  Behandeln Sie das **\_ IAnalysisEvents::ReadyToReconcile-Ereignis.**
3.  Rufen Sie zum Abstimmen der Analyseergebnisse die [**IInkAnalyzer::Reconcile-Methode**](iinkanalyzer-reconcile.md) aus dem Ereignishandler für das **\_ IAnalysisEvents::ReadyToReconcile-Ereignis** auf. Um den aktuellen Hintergrundanalysevorgang abzubrechen, rufen Sie die [**IInkAnalyzer::Abort-Methode**](iinkanalyzer-abort.md) aus dem -Ereignishandler für das **\_ IAnalysisEvents::ReadyToReconcile-Ereignis** auf.

[**IInkAnalyzer**](iinkanalyzer.md) löst dieses Ereignis aus, bevor es das [**\_ IAnalysisProxyEvents::InkAnalyzerStateChanging-Ereignis**](-ianalysisproxyevents-inkanalyzerstatechanging.md) auslöst.

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit [**IInkAnalyzer**](iinkanalyzer.md)finden Sie unter [Datenproxy mit Freihandanalyse.](data-proxy-with-ink-analysis.md)

[**IInkAnalyzer**](iinkanalyzer.md) löst dieses Ereignis während der Hintergrundanalyse aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**Analysismodes**](analysismodes.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer::Reconcile-Methode**](iinkanalyzer-reconcile.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




