---
description: Ruft Flags ab, die Steuern, wie iinkanalyzer eine Handschrift Analyse ausführt.
ms.assetid: 982cb9cd-2d73-4064-9a6e-fe123adf0fb6
title: 'Iinkanalyzer:: getanalysismodes-Methode (iacom. h)'
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
ms.openlocfilehash: d03ec255b10dd607889768795b00f5b2aff4dc11
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368097"
---
# <a name="iinkanalyzergetanalysismodes-method"></a>Iinkanalyzer:: getanalysismodes-Methode

Ruft Flags ab, die Steuern, wie [**iinkanalyzer**](iinkanalyzer.md) eine Handschrift Analyse ausführt.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetAnalysisModes(
  [out] AnalysisModes *pAnalysisMode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*panalysismode* \[ vorgenommen\]
</dt> <dd>

Eine bitweise Kombination der [**AnalysisModes**](analysismodes.md) -Enumerationswerte.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

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

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Iinkanalyzer:: abtanalysismodes-Methode**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




