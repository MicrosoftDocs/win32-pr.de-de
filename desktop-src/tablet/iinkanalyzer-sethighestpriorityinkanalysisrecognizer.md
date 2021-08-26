---
description: Verschiebt den angegebenen IInkAnalysisRecognizer an die erste Position in der Liste der Freihanderkennungen des IInkAnalyzer-Objekts.
ms.assetid: 9126187f-02dd-4988-91b8-c4f3d3b6f773
title: IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetHighestPriorityInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8404a2e1e89980ce5e8cadac1a468b3383d37d4952349f3702539975a304ac92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119935210"
---
# <a name="iinkanalyzersethighestpriorityinkanalysisrecognizer-method"></a>IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer-Methode

Verschiebt den angegebenen [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) an die erste Position in der Liste der Freihanderkennungen des [**IInkAnalyzer-Objekts.**](iinkanalyzer.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT SetHighestPriorityInkAnalysisRecognizer(
  [in] IInkAnalysisRecognizer *pInkAnalysisRecognizer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInkAnalysisRecognizer* \[ In\]
</dt> <dd>

Der [**IInkAnalysisRecognizer,**](iinkanalysisrecognizer.md) der an der ersten Position positioniert werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Rufen Sie die [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)auf, um die Liste der Freihanderkennungen in der Prioritätsreihenfolge abzurufen.

Diese Methode wirkt sich nicht auf die Reihenfolge der restlichen [**IInkAnalysisRecognizer-Objekte**](iinkanalysisrecognizer.md) in der Liste der Freihanderkennungen des [**IInkAnalyzer-Objekts**](iinkanalyzer.md) aus.

Die Reihenfolge der Freihanderkennungen, die von der [**IInkAnalyzer::GetInkAnalysisRecognizersByPriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) zurückgegeben werden, gibt die Reihenfolge an, in der [**IInkAnalyzer**](iinkanalyzer.md) die verfügbaren [**IInkAnalysisRecognizer-Objekte**](iinkanalysisrecognizer.md) auswertet.

Die Verwendung der Ink-Erkennungen wird basierend auf ihrer Reihenfolge in der Liste ausgewertet.

Während der Freihandanalyse durchläuft [**der IInkAnalyzer**](iinkanalyzer.md) die Freihanderkennungen in seiner Liste, bis er eine Erkennung findet, die die Sprache und andere Eigenschaften der Striche unterstützt. Diese Erkennung wird für die Erkennung von Ink für diese Striche verwendet.

Wenn [**IInkAnalyzer**](iinkanalyzer.md) während der Analyse keinen [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) findet, der eine Reihe von Strichen während der Analyse unterstützt, generiert **IInkAnalyzer** eine [**IAnalysisWarning**](ianalysiswarning.md) mit dem Warnungscode **AnalysisWarningCode \_ InkAnalysisRecognizerNotInstalled** (siehe [**IAnalysisWarning::GetWarningCode**](ianalysiswarning-getwarningcode.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::GetInkAnalysisRecognizersByPriority-Methode**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




