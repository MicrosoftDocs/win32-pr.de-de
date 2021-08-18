---
description: Entfernt einen Analysehinweis aus IInkAnalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: IInkAnalyzer::D eleteAnalysisHint-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.DeleteAnalysisHint
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6f514f20ed99f7fc56725f582b815639cb9d8b3179e9e428845d7e066b6e3bf2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967289"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a>IInkAnalyzer::D eleteAnalysisHint-Methode

Entfernt einen Analysehinweis aus [**IInkAnalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pHintToDelete* \[ In\]
</dt> <dd>

Der Analysehinweis von [**IInkAnalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Durch das Entfernen eines Analysehinweises wird der Bereich des Hinweises nicht für die Erneute Analyse bezeichnet. Um den Bereich innerhalb des Hinweises für die Erneute Analyse zu markieren, verwenden Sie die [**IInkAnalyzer::SetDirtyRegion-Methode,**](iinkanalyzer-setdirtyregion.md) um den dirty-Bereich auf die Vereinigung des aktuellen dirty-Bereichs und -Bereichs des Analysehinweises zu setzen.

Der Hinweis wird aus dem Analyseprogramm entfernt. [**IContextNode selbst**](icontextnode.md) wird jedoch nicht gelöscht.

Diese Methode gibt einen Fehlercode zurück, wenn *pHintToDelete* ein [**IContextNode**](icontextnode.md) ist, der nicht vom Typ AnalysisHint ist (siehe [**IContextNode::GetType**](icontextnode-gettype.md)).

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

[**IInkAnalyzer::CreateAnalysisHint-Methode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**IInkAnalyzer::GetAnalysisHints-Methode**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**IInkAnalyzer::GetAnalysisHintsByName-Methode**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




