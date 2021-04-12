---
description: Entfernt einen Analyse Hinweis aus iinkanalyzer.
ms.assetid: ba5498d4-d31c-4b3f-9004-0448e18d4835
title: Iinkanalyzer::D eleteanalysishint-Methode (iacom. h)
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
ms.openlocfilehash: f84f718701abd5bc76b55427aab9df072f758c3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129468"
---
# <a name="iinkanalyzerdeleteanalysishint-method"></a>Iinkanalyzer::D eleteanalysishint-Methode

Entfernt einen Analyse Hinweis aus [**iinkanalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT DeleteAnalysisHint(
  [in] IContextNode *pHintToDelete
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*phintto DELETE* \[ in\]
</dt> <dd>

Der Analyse Hinweis von [**iinkanalyzer**](iinkanalyzer.md).

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Durch das Entfernen eines Analyse Hinweises wird der Bereich des Hinweises für die erneute Analyse nicht markiert. Um den Bereich innerhalb des Hinweises für die erneute Analyse zu markieren, verwenden Sie die [**iinkanalyzer:: setdirtyregion-Methode**](iinkanalyzer-setdirtyregion.md) , um den geänderten Bereich auf die Vereinigung des aktuellen geänderten Bereichs und Bereichs des Analyse Hinweises festzulegen.

Der Hinweis wird aus dem Analyzer entfernt. der [**icontextnode**](icontextnode.md) selbst wird jedoch nicht gelöscht.

Diese Methode gibt einen Fehlercode zurück, wenn ' *phintdedelete* ' ein [**icontextnode**](icontextnode.md) ist, der nicht vom Typ ' AnalysisHint ' ist (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)).

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

[**Iinkanalyzer:: feateanalysishint-Methode**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**Iinkanalyzer:: GetAnalysisHints-Methode**](iinkanalyzer-getanalysishints.md)
</dt> <dt>

[**Iinkanalyzer:: getanalysishintsbyname-Methode**](iinkanalyzer-getanalysishintsbyname.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




