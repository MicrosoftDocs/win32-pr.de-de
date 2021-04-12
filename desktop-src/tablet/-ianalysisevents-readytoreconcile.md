---
description: Tritt auf, wenn iinkanalyzer bereit ist, die Ergebnisse der Hintergrundanalyse mit dem aktuellen Zustand abzustimmen.
ms.assetid: 63cf48eb-9d1e-4017-a4eb-55d811f7e6cf
title: '_IAnalysisEvents:: Read ytor econcile-Ereignis (iacom. h)'
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
ms.openlocfilehash: 4f3144f34dc680f9bc31f51b9e6b4284a70fb9bc
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219049"
---
# <a name="_ianalysiseventsreadytoreconcile-event"></a>\_Ianalysissevents:: lesereitor-Ereignis

Tritt auf, wenn [**iinkanalyzer**](iinkanalyzer.md) bereit ist, die Ergebnisse der Hintergrundanalyse mit dem aktuellen Zustand abzustimmen.

## <a name="syntax"></a>Syntax


```C++
HRESULT ReadyToReconcile();
```



## <a name="parameters"></a>Parameter

Dieses Ereignis weist keine Parameter auf.

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Der [**iinkanalyzer**](iinkanalyzer.md) führt eine automatische Abstimmung durch, wenn das Flag " **\_ automatisismodes automatianvermittlungs** " des Ink Analyzer festgelegt ist (siehe [**iinkanalyzer:: setanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md)). Wenn das **AnalysisModes \_ automatikreversöhnung** -Flag nicht festgelegt ist, muss Ihre Anwendung die Ergebnisse der Hintergrundanalyse manuell abstimmen.

Führen Sie die folgenden Schritte aus, um die manuelle Abstimmung durchzuführen.

1.  Löschen Sie das Flag " **automatisismodes \_ automatikredelegat** " der Ink Analyzer.
2.  Behandeln Sie das **\_ ianalysissevents:: leserytoreconcile** -Ereignis.
3.  Um die Analyseergebnisse abzugleichen, müssen Sie die [**Methoden Methode iinkanalyzer::**](iinkanalyzer-reconcile.md) abgestimmt aus dem Ereignishandler für das **\_ ianalysisevents:: Read ytoreconcile** -Ereignis abrufen. Um den aktuellen Hintergrundanalyse Vorgang abzubrechen, rufen Sie die [**iinkanalyzer:: Abort-Methoden**](iinkanalyzer-abort.md) Methode aus dem Ereignishandler für das **\_ ianalysisevents:: leserytoreconcile** -Ereignis auf.

Der [**iinkanalyzer**](iinkanalyzer.md) löst dieses Ereignis aus, bevor es das [**\_ ianalysisproxyevents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) -Ereignis auslöst.

Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

Der [**iinkanalyzer**](iinkanalyzer.md) löst dieses Ereignis während der Hintergrundanalyse aus.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_Ianalysil Vents**](-ianalysisevents.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**\_Ianalysisproxyevents**](-ianalysisproxyevents.md)
</dt> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Iinkanalyzer:: abgestimmt-Methode**](iinkanalyzer-reconcile.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




