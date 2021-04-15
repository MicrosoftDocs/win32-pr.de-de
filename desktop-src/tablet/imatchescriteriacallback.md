---
description: Macht eine Methode verfügbar, um auszuwerten, ob ein icontextnode-Objekt bestimmte Kriterien erfüllt oder nicht.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: Imatchescriteria-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IMatchesCriteriaCallBack
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 960bd221bdd1f621f6ec4deb5ea167f5bf9ee4d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525319"
---
# <a name="imatchescriteriacallback-interface"></a>Imatchescriteria-Schnittstelle

Macht eine Methode verfügbar, um auszuwerten, ob ein [**icontextnode**](icontextnode.md) -Objekt bestimmte Kriterien erfüllt oder nicht.

## <a name="members"></a>Member

Die **imatchescriteria** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle. **Imatchescriteria acallback** weist auch diese Typen von Membern auf:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **imatcheskriteriacallback** -Schnittstelle verfügt über diese Methoden.



| Methode                                                                      | BESCHREIBUNG                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**Evaluatecontextnode**](imatchescriteriacallback-evaluatecontextnode.md) | Wertet beim Überschreiben in einer abgeleiteten Klasse aus, ob ein bestimmtes [**icontextnode**](icontextnode.md) -Objekt die Kriterien erfüllt.<br/> |



 

## <a name="remarks"></a>Bemerkungen

Um die [**iinkanalyzer:: findnodeswithcallback-Methode**](iinkanalyzer-findnodeswithcallback.md) oder die [**iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)zu verwenden, erstellen Sie eine Klasse, die **imatchescriteria acallback** implementiert. Implementieren Sie [**imatchescriteria acallback:: evaluatecontextnode**](imatchescriteriacallback-evaluatecontextnode.md) , um **Variant \_ true** zurückzugeben, wenn das [**icontextnode**](icontextnode.md) -Objekt mit Ihren Kriterien übereinstimmt, und andernfalls **\_ false** . Für einige Kriterien müssen Sie möglicherweise eine Möglichkeit zur Initialisierung oder Beibehaltung des Zustands Ihres **imatchescriteria** -Objekts bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer:: findnodeswithcallback-Methode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**Iinkanalyzer:: findnodeswithcallbackinsubtree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

