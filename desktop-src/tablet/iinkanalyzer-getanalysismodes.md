---
description: Ruft Flags ab, die steuern, wie der IInkAnalyzer die Ink-Analyse durchführt.
ms.assetid: 982cb9cd-2d73-4064-9a6e-fe123adf0fb6
title: IInkAnalyzer::GetAnalysisModes-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4fd83c0991c0740b1341c490e08b19d143eb110f2714bfbbe82aa3a962106bc0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118043680"
---
# <a name="iinkanalyzergetanalysismodes-method"></a>IInkAnalyzer::GetAnalysisModes-Methode

Ruft Flags ab, die steuern, wie [**der IInkAnalyzer**](iinkanalyzer.md) die Ink-Analyse durchführt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAnalysisModes(
  [out] AnalysisModes *pAnalysisMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pAnalysisMode* \[ out\]
</dt> <dd>

Eine bitweise Kombination der [**AnalysisModes-Enumerationswerte.**](analysismodes.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

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

[**Analysismodes**](analysismodes.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer::SetAnalysisModes-Methode**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




