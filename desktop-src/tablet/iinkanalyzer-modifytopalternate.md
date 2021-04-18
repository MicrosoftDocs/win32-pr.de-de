---
description: Ändert die aktuelle obere Alternative in die angegebene alternative und löscht den bestätentyp für alle icontextnode-Objekte, die der alternativen zugeordnet sind.
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'Iinkanalyzer:: ModifyTopAlternate-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da2fcde7015e993e13e47673b271c560b6c3d72a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354499"
---
# <a name="iinkanalyzermodifytopalternate-method"></a>Iinkanalyzer:: ModifyTopAlternate-Methode

Ändert die aktuelle obere Alternative in die angegebene alternative und löscht den bestätentyp für alle [**icontextnode**](icontextnode.md) -Objekte, die der alternativen zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*palternate* \[ in\]
</dt> <dd>

Das [**ianalysisalternate**](ianalysisalternate.md) -Objekt, das die neue obere Alternative enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Um Analyse Alternativen zu erhalten, verwenden Sie die [**iinkanalyzer:: getalteraten-Methode**](iinkanalyzer-getalternates.md), die [**iinkanalyzer:: getalternatesforcontextnodes-Methode**](iinkanalyzer-getalternatesforcontextnodes.md)oder die [**iinkanalyzer:: getalternatesforstriche-Methode**](iinkanalyzer-getalternatesforstrokes.md). Verwenden Sie die [**ianalysisalternate:: getalternatenodes-Methode**](ianalysisalternate-getalternatenodes.md), um die [**icontextnode**](icontextnode.md) -Objekte zu erhalten, die einer alternativen Analyse zugeordnet sind.

Verwenden Sie [**icontextnode:: Confirm**](icontextnode-confirm.md), um den bestätentyp für einen Kontext Knoten zu ändern.

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

[**Ianalysisalternate**](ianalysisalternate.md)
</dt> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**ConfirmationType**](confirmationtype.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




