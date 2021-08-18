---
description: Wendet die Ergebnisse einer Hintergrund-Ink-Analyse auf die Kontextknotenstruktur für die Teile der Struktur an, die seit dem Aufruf der IInkAnalyzer::BackgroundAnalyze-Methode nicht von der Anwendung geändert wurden.
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: IInkAnalyzer::Reconcile-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Reconcile
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 3b16497a7f7822bf1557e3e686a81497a4e3723e71f115a1a7d6aa59d8381db2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092030"
---
# <a name="iinkanalyzerreconcile-method"></a>IInkAnalyzer::Reconcile-Methode

Wendet die Ergebnisse eines Hintergrund-Ink-Analyse-Vorgangs auf die Kontextknotenstruktur für die Teile der Struktur an, die seit dem Aufruf der [**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)nicht von der Anwendung geändert wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Standardmäßig führt [**IInkAnalyzer**](iinkanalyzer.md) unmittelbar vor dem Auslösung der [**\_ Ereignisse IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md) und [**\_ IAnalysisEvents::Results**](-ianalysisevents-results.md) eine automatische Abstimmungsphase aus.

Um die automatische Abstimmung zu deaktivieren, deaktivieren Sie das **AnalysisModes \_ AutomaticReconciliation-Flag** aus den Analysemodi des Freischaltanalyse-Analysegeräts (siehe [**IInkAnalyzer::SetAnalysisModes-Methode**](iinkanalyzer-setanalysismodes.md) und [**AnalysisModes**](analysismodes.md)). Die [**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md) gibt einen Fehler zurück, wenn die automatische Abstimmung deaktiviert ist und Ihre Anwendung das [**\_ IAnalysisEvents::ReadyToReconcile-Ereignis**](-ianalysisevents-readytoreconcile.md) nicht behandelt. Ihre Anwendung muss die **IInkAnalyzer::Reconcile-Methode** aufrufen, bevor [**der IInkAnalyzer**](iinkanalyzer.md) die Ergebnisse weiter verarbeiten oder die weitere Analyse für die entsprechende Analysephase fortsetzen kann.

Ihre Anwendung kann während der Hintergrundanalyse Änderungen an der Kontextknotenstruktur des [**IInkAnalyzer-Objekts**](iinkanalyzer.md) vornehmen, z. B. das Hinzufügen oder Entfernen von Strichen und das Ändern von Strichdaten. Solche Änderungen können Teile der Ergebnisse der Hintergrundanalyse für ungültig erklären. Diese Methode wendet Analyseergebnisse nur auf die Kontextknotenstruktur des Analysegeräts für die Teile der Struktur an, die ihre Anwendung nicht geändert hat. Diese Methode fügt auch Bereiche mit ungültigen Analyseergebnissen zum dirty-Bereich des **IInkAnalyzer-Objekts** hinzu (siehe [**IInkAnalyzer::GetDirtyRegion-Methode**](iinkanalyzer-getdirtyregion.md)).

Weitere Informationen zur Verwendung von zum Analysieren von Ink finden Sie unter [Übersicht über die Ink-Analyse.](ink-analysis-overview.md) [**AnalysisModes**](analysismodes.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




