---
description: Wertet beim Überschreiben in einer abgeleiteten Klasse aus, ob ein bestimmtes icontextnode-Objekt die Kriterien erfüllt.
ms.assetid: ade8e59c-6aeb-4a87-a95d-229f8f0b2223
title: 'Imatchescriteria acallback:: evaluatecontextnode-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack.EvaluateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 554cf451396101de2238258de0a0706956f24a02
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348165"
---
# <a name="imatchescriteriacallbackevaluatecontextnode-method"></a>Imatchescriteria acallback:: evaluatecontextnode-Methode

Wertet beim Überschreiben in einer abgeleiteten Klasse aus, ob ein bestimmtes [**icontextnode**](icontextnode.md) -Objekt die Kriterien erfüllt.

## <a name="syntax"></a>Syntax


```C++
HRESULT EvaluateContextNode(
  [in]  IContextNode *pContextNodeToEvaluate,
  [out] VARIANT_BOOL *pbResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcontextnodebug* \[ in\]
</dt> <dd>

Das [**icontextnode**](icontextnode.md) -Objekt, das ausgewertet werden soll.

</dd> <dt>

*pbresult* \[ vorgenommen\]
</dt> <dd>

**Variant \_ TRUE** , wenn *pcontextnodebug* den Kriterien entspricht. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Um die [**iinkanalyzer:: findnodeswithcallback-Methode**](iinkanalyzer-findnodeswithcallback.md) oder die [**iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)zu verwenden, erstellen Sie eine Klasse, die [**imatchescriteria acallback**](imatchescriteriacallback.md)implementiert. Implementieren Sie **imatchescriteria acallback:: evaluatecontextnode** , um **Variant \_ true** zurückzugeben, wenn das [**icontextnode**](icontextnode.md) -Objekt mit Ihren Kriterien übereinstimmt, und andernfalls **\_ false** . Für einige Kriterien müssen Sie möglicherweise eine Möglichkeit zur Initialisierung oder Beibehaltung des Zustands Ihres **imatchescriteria** -Objekts bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Imatcheskriteriacallback**](imatchescriteriacallback.md)
</dt> <dt>

[**Iinkanalyzer:: findnodeswithcallback-Methode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




