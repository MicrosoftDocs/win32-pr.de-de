---
description: Tritt ein, bevor der IInkAnalyzer ein IContextNode-Objekt verschiebt, indem der übergeordnete Knoten geändert wird.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: _IAnalysisProxyEvents::ContextNodeReparenting -Ereignis (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeReparenting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eafb37fd4083f0ecf7c68eaf45fc3339a730e818864f4be15eca4b94d4bd5b7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857109"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a>\_IAnalysisProxyEvents::ContextNodeReparenting-Ereignis

Tritt ein, bevor [**der IInkAnalyzer ein**](iinkanalyzer.md) [**IContextNode-Objekt**](icontextnode.md) verschiebt, indem der übergeordnete Knoten geändert wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContextNodeReparenting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pNewParentContextNode,
  [in] IContextNode *pContextNodeToBeReparented
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInkAnalyzer* \[ In\]
</dt> <dd>

Das [**IInkAnalyzer-Objekt,**](iinkanalyzer.md) das das [**IContextNode-Objekt**](icontextnode.md) bewegt.

</dd> <dt>

*pNewParentContextNode* \[ In\]
</dt> <dd>

Das neue übergeordnete [**IContextNode-Objekt.**](icontextnode.md)

</dd> <dt>

*pContextNodeToBeReparented* \[ In\]
</dt> <dd>

Das [**IContextNode-Objekt,**](icontextnode.md) das verschoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur bei behält, die mit der von [**IInkAnalyzer synchronisiert wird.**](iinkanalyzer.md) Dieses Ereignis tritt während der Abstimmungsphase der Ink-Analyse oder als Reaktion auf eine Methode auf, die einen [**IContextNode**](icontextnode.md) von einer Auflistung von UntergeordnetenNodes in eine andere verschiebt (siehe [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) und [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit [**IInkAnalyzer**](iinkanalyzer.md)finden Sie unter [Datenproxy mit Ink-Analyse.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




