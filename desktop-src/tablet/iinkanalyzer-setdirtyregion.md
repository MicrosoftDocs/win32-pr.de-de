---
description: Ändert den Bereich, der sich seit dem letzten Analysevorgang geändert hat.
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: IInkAnalyzer::SetDirtyRegion-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a39fc420b368911788efcb9462c9c4be5b4828c82906ef2c94bb5be99ca17568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091470"
---
# <a name="iinkanalyzersetdirtyregion-method"></a>IInkAnalyzer::SetDirtyRegion-Methode

Ändert den Bereich, der sich seit dem letzten Analysevorgang geändert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pDirtyRegion* \[ In\]
</dt> <dd>

Eine [**IAnalysisRegion,**](ianalysisregion.md) die den Bereich beschreibt, der sich seit dem letzten Analysevorgang geändert hat.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Diese Methode identifiziert die Bereiche, die analysiert oder erneut analysiert werden müssen. Alle [**IInkAnalyzer-Methoden,**](iinkanalyzer.md) die Strichdaten hinzufügen, aktualisieren oder entfernen, aktualisieren den geänderten Bereich. So markieren Sie manuell einen Bereich für die Erneute Analyse:

1.  Verwenden Sie die [**IInkAnalyzer::GetDirtyRegion-Methode, um den dirty-Bereich zu erhalten.**](iinkanalyzer-getdirtyregion.md)
2.  Verwenden [**Sie die IAnalysisRegion::UnionRegion-Methode**](ianalysisregion-unionregion.md) oder die [**IAnalysisRegion::UnionRectangle-Methode,**](ianalysisregion-unionrectangle.md) um den Bereich aus Schritt 1 dem Bereich hinzuzufügen.
3.  Verwenden **Sie die IInkAnalyzer::SetDirtyRegion-Methode,** um den geänderten Bereich zu aktualisieren.

Der [**IInkAnalyzer**](iinkanalyzer.md) analysiert während eines Aufrufs der [**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md) oder [**der IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)Ink innerhalb seines dirty-Region. Der **IInkAnalyzer** kann den Analysevorgang jedoch um benachbarte Regionen erweitern.

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

[**IInkAnalyzer::AddStroke-Methode**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokeForLanguage-Methode**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokes-Methode**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer::AddStrokesForLanguage-Methode**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStroke-Methode**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer::RemoveStrokes-Methode**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IInkAnalyzer::UpdateStrokesData-Methode**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




