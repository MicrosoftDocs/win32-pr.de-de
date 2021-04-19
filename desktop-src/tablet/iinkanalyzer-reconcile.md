---
description: 'Wendet die Ergebnisse eines Hintergrund-frei Hand Analyse Vorgangs auf die Kontext Knoten Struktur für die Teile der Struktur an, die seit dem Ansichts Vorgang der iinkanalyzer:: BackgroundAnalyze-Methode nicht von der Anwendung geändert wurden.'
ms.assetid: 60e15d4f-6e81-48b9-b7f3-97d2de5c0c1c
title: 'Iinkanalyzer:: abgestimmt-Methode (iacom. h)'
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
ms.openlocfilehash: 33229c7da47f294f317d2216d9e9bf4f6b114599
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345736"
---
# <a name="iinkanalyzerreconcile-method"></a>Iinkanalyzer:: abgestimmt-Methode

Wendet die Ergebnisse eines Hintergrund-frei Hand Analyse Vorgangs auf die Kontext Knoten Struktur für die Teile der Struktur an, die seit dem Ansichts Vorgang der [**iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)nicht von der Anwendung geändert wurden.

## <a name="syntax"></a>Syntax


```C++
HRESULT Reconcile();
```



## <a name="parameters"></a>Parameter

Diese Methode hat keine Parameter.

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Standardmäßig führt [**iinkanalyzer**](iinkanalyzer.md) sofort vor dem Auflösen der [**\_ ianalysitsvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) -und [**\_ ianalysilvents:: results**](-ianalysisevents-results.md) -Ereignisse eine automatische Abstimmungsphase aus.

Um die automatische Abstimmung zu deaktivieren, löschen Sie das **AnalysisModes-Flag \_ automatikreversöhnung** aus den Analyse Modi von Ink Analyzer (siehe [**iinkanalyzer:: setanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md) und [**AnalysisModes**](analysismodes.md)). Die [**Methode "iinkanalyzer:: BackgroundAnalyze Method**](iinkanalyzer-backgroundanalyze.md) " gibt einen Fehler zurück, wenn die automatische Abstimmung deaktiviert ist und die Anwendung das [**\_ ianalysisevents:: Read ytoreconcile**](-ianalysisevents-readytoreconcile.md) -Ereignis nicht behandelt. Die Anwendung muss die **Methode iinkanalyzer::** abgestimmt-Methode aufruft, bevor der [**iinkanalyzer**](iinkanalyzer.md) die Ergebnisse weiterverarbeiten oder die weitere Analyse für die entsprechende Analysephase fortsetzen kann.

Die Anwendung kann Änderungen vornehmen, z. b. das Hinzufügen oder Entfernen von Strichen und das Ändern von Strich Daten in der Kontext Knoten Struktur des [**iinkanalyzer**](iinkanalyzer.md) -Objekts während der Hintergrundanalyse. Solche Änderungen können Teile der Ergebnisse der Hintergrundanalyse für ungültig erklären. Diese Methode wendet Analyseergebnisse nur auf die Kontext Knoten Struktur des Analyzers für die Teile der Struktur an, die Ihre Anwendung nicht geändert hat. Diese Methode fügt auch Regionen, die ungültige Analyseergebnisse enthalten, in den geänderten Bereich des **iinkanalyzer** -Objekts ein (siehe [**iinkanalyzer:: getdirtyregion-Methode**](iinkanalyzer-getdirtyregion.md)).

Weitere Informationen zur Verwendung von zum Analysieren von frei Hand Eingaben finden Sie unter [Übersicht über](ink-analysis-overview.md)die frei Hand Analyse. [**AnalysisModes**](analysismodes.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**\_Ianalysissevents:: luytor econcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




