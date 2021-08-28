---
description: Bricht den aktuellen Analysevorgang ab.
ms.assetid: 909bfa66-b6df-4730-95b7-809fc2170e85
title: IInkAnalyzer::Abort-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.Abort
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f52b2037210e39533d1247cb338bb22a7785f354dbca6b615c6ada67eff3bb5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119773600"
---
# <a name="iinkanalyzerabort-method"></a>IInkAnalyzer::Abort-Methode

Bricht den aktuellen Analysevorgang ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT Abort(
  [out] IAnalysisRegion **ppAbortedRegion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppAbortedRegion* \[ out\]
</dt> <dd>

Ein Zeiger auf eine [**IAnalysisRegion,**](ianalysisregion.md) die den geänderten Bereich (siehe [**IInkAnalyzer::GetDirtyRegion-Methode)**](iinkanalyzer-getdirtyregion.md)des aktuellen Analysevorgangs darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) für *ppAbortedRegion* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

Diese Methode bricht den aktuellen Analysevorgang ab.

Wenn *ppAbortedRegion* **NULL** ist, führt diese Methode den Abbruch wie gewohnt aus, da dies angibt, dass der Aufrufer kein Interesse am Rückgabewert hat.

**Die IInkAnalyzer::Abort-Methode** stillt die [**\_ Ereignisse IAnalysisEvents::Results**](-ianalysisevents-results.md) und [**\_ IAnalysisEvents::Activity**](-ianalysisevents-activity.md) für den aktuellen Analysevorgang.

**Die IInkAnalyzer::Abort-Methode** wird asynchron ausgeführt, bis der aktuelle Hintergrundanalysevorgang abgebrochen wird. Da der Abbruchvorgang asynchron ist, kann die Anwendung andere Aufgaben ausführen, während die aktuellen Analysevorgänge abgebrochen werden.

Wenn keine Analysevorgänge ausgeführt werden, gibt diese Methode einen leeren Analysebereich zurück.

Wenn ein Analysevorgang ausgeführt wird, bricht diese Methode den Vorgang ab.

Wenn sowohl synchrone als auch asynchrone Analysevorgänge ausgeführt werden, bricht diese Methode den synchronen Vorgang ab.

Wenn diese Methode für denselben Analysevorgang mehr als einmal aufgerufen wird, gibt der erste Aufruf den geänderten Bereich für den Vorgang zurück, und die nachfolgenden Aufrufe geben einen leeren Bereich zurück.

Wenn Ihre Anwendung eine eigene Datenstruktur beibehält, die mit der der [**IInkAnalyzer**](iinkanalyzer.md)synchronisiert wird, kann der Aufruf der **IInkAnalyzer::Abort-Methode** ihr Dokument mit Teilergebnissen belassen. Um dies zu vermeiden, rufen Sie die **IInkAnalyzer::Abort-Methode** nicht zwischen dem Empfang des [**\_ IAnalysisProxyEvents::InkAnalyzerStateChanging-Ereignisses**](-ianalysisproxyevents-inkanalyzerstatechanging.md) und dem Zeitpunkt auf, zu dem **IInkAnalyzer** das  [**\_ IAnalysisEvents::IntermediateResults-**](-ianalysisevents-intermediateresults.md) oder [**\_ IAnalysisEvents::Results-Ereignis**](-ianalysisevents-results.md) empfängt.

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit dem Ink-Analysetools finden Sie unter [Datenproxy mit Ink-Analyse.](data-proxy-with-ink-analysis.md)

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

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer::GetDirtyRegion-Methode**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[**IInkAnalyzer::SetDirtyRegion-Methode**](iinkanalyzer-setdirtyregion.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

