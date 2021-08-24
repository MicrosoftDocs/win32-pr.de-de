---
description: Ruft eine geordnete Auflistung von IInkAnalysisRecognizer-Objekten ab.
ms.assetid: 67399237-38e2-4905-a97c-10ca72c7799b
title: IInkAnalyzer::GetInkAnalysisRecognizersByPriority-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetInkAnalysisRecognizersByPriority
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fc663385006eedaca163f529af1f9f8a2da2eb5d3d41db823ffb53ee91775b93
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713410"
---
# <a name="iinkanalyzergetinkanalysisrecognizersbypriority-method"></a>IInkAnalyzer::GetInkAnalysisRecognizersByPriority-Methode

Ruft eine geordnete Auflistung von [**IInkAnalysisRecognizer-Objekten**](iinkanalysisrecognizer.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetInkAnalysisRecognizersByPriority(
  [out] IInkAnalysisRecognizers **ppInkAnalysisRecognizers
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ppInkAnalysisRecognizers* \[ out\]
</dt> <dd>

Eine geordnete Auflistung von [**IInkAnalysisRecognizer-Objekten.**](iinkanalysisrecognizer.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**IUnknown::Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) auf *ppInkAnalysisRecognizers* auf, wenn Sie das Objekt nicht mehr verwenden müssen.

 

Die Reihenfolge der Erkennungen in dieser Auflistung gibt die Reihenfolge an, in der [**IInkAnalyzer**](iinkanalyzer.md) die verfügbaren Erkennungen auswertet. **IInkAnalyzer** verwendet die Sprache der Striche als primäres Kriterium für die Anwendung eines [**IInkAnalysisRecognizer.**](iinkanalysisrecognizer.md) Als sekundäres Kriterium vergleicht **der IInkAnalyzer** Analysehinweisinformationen mit den unterstützten Funktionen eines **IInkAnalysisRecognizer-Objekts** (siehe [**IInkAnalysisRecognizer::GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)). Weitere Informationen zu Analysehinweisen finden Sie unter [**IInkAnalyzer::CreateAnalysisHint-Methode.**](iinkanalyzer-createanalysishint.md)

Wenn mehr als ein [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) einen Sprachbezeichner unterstützt, verwendet [**IInkAnalyzer**](iinkanalyzer.md) einen "first-fit"-Algorithmus, um den ersten **IInkAnalysisRecognizer** auszuwählen, um Striche dieser Sprache zu analysieren.

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

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer::SetHighestPriorityInkAnalysisRecognizer-Methode**](iinkanalyzer-sethighestpriorityinkanalysisrecognizer.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

