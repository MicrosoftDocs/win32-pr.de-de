---
description: Ändert Flags, die steuern, wie der IInkAnalyzer die Ink-Analyse durchführt.
ms.assetid: cb82edd0-1f15-4313-a286-1fcd715ac6df
title: IInkAnalyzer::SetAnalysisModes-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetAnalysisModes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c7edd167cd40b80a01fd2f23243c931fe6a15795da08d7735b6e2433c462ee01
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091500"
---
# <a name="iinkanalyzersetanalysismodes-method"></a>IInkAnalyzer::SetAnalysisModes-Methode

Ändert Flags, die steuern, wie [**der IInkAnalyzer**](iinkanalyzer.md) die Ink-Analyse durchführt.

## <a name="syntax"></a>Syntax


```C++
HRESULT SetAnalysisModes(
  [in] AnalysisModes analysisMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*analysisMode* \[ In\]
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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Analysismodes**](analysismodes.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer::GetAnalysisModes-Methode**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




