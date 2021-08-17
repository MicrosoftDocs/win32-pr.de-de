---
description: Macht eine Methode verfügbar, um zu bewerten, ob ein IContextNode-Objekt ein angegebenes Kriterium erfüllt oder fehlschlägt.
ms.assetid: 8b094882-e739-4088-87de-6ef4719b0b5b
title: IMatchesCriteriaCallBack-Schnittstelle (IACom.h)
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
ms.openlocfilehash: bc661f47c77d615df95f63e58beccbbf125b93078392a63f86ed50f52cc5636d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118718969"
---
# <a name="imatchescriteriacallback-interface"></a>IMatchesCriteriaCallBack-Schnittstelle

Macht eine Methode verfügbar, um zu bewerten, ob ein [**IContextNode-Objekt**](icontextnode.md) ein angegebenes Kriterium erfüllt oder fehlschlägt.

## <a name="members"></a>Member

Die **IMatchesCriteriaCallBack-Schnittstelle** erbt von der [**IUnknown-Schnittstelle.**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) **IMatchesCriteriaCallBack** verfügt auch über diese Membertypen:

-   [Methoden](#methods)

### <a name="methods"></a>Methoden

Die **IMatchesCriteriaCallBack-Schnittstelle** verfügt über diese Methoden.



| Methode                                                                      | Beschreibung                                                                                                                                  |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|
| [**EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) | Wertet beim Überschreiben in einer abgeleiteten Klasse aus, ob ein angegebenes [**IContextNode-Objekt**](icontextnode.md) die Kriterien erfüllt.<br/> |



 

## <a name="remarks"></a>Hinweise

Um die [**IInkAnalyzer::FindNodesWithCallBack-Methode**](iinkanalyzer-findnodeswithcallback.md) oder [**die IInkAnalyzer::FindNodesWithCallBackInSubTree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)zu verwenden, erstellen Sie eine Klasse, die **IMatchesCriteriaCallBack implementiert.** Implementieren [**Sie IMatchesCriteriaCallBack::EvaluateContextNode**](imatchescriteriacallback-evaluatecontextnode.md) so, dass **VARIANT \_ TRUE** zurückgegeben wird, wenn das [**IContextNode-Objekt**](icontextnode.md) Ihren Kriterien entspricht, andernfalls **VARIANT \_ FALSE.** Bei einigen Kriterien müssen Sie möglicherweise eine Möglichkeit zum Initialisieren oder Verwalten des Zustands Ihres **IMatchesCriteriaCallBack-Objekts** bereitstellen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer::FindNodesWithCallBack-Methode**](iinkanalyzer-findnodeswithcallback.md)
</dt> <dt>

[**IInkAnalyzer::FindNodesWithCallBackInSubTree-Methode**](iinkanalyzer-findnodeswithcallbackinsubtree.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

