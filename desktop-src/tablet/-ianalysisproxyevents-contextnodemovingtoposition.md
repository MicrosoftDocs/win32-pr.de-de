---
description: Tritt ein, bevor IInkAnalyzer ein IContextNode-Objekt an eine neue Position in der Auflistung der Unterknoten des übergeordneten Knotens verschiebt.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: _IAnalysisProxyEvents::ContextNodeMovingToPosition-Ereignis (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeMovingToPosition
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4cd814e45692d90c77bad8c46fea5dfd8534bd769a07a9d0bc1648ecafc7b2f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117857149"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a>\_IAnalysisProxyEvents::ContextNodeMovingToPosition-Ereignis

Tritt ein, bevor [**IInkAnalyzer**](iinkanalyzer.md) ein [**IContextNode-Objekt**](icontextnode.md) an eine neue Position in der Auflistung der Unterknoten des übergeordneten Knotens verschiebt.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContextNodeMovingToPosition(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pISubNodeToMove,
  [in] IContextNode *pParentContextNode,
  [in] ULONG        ulNewIndex
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInkAnalyzer* \[ In\]
</dt> <dd>

Das [**IInkAnalyzer-Objekt,**](iinkanalyzer.md) das das [**IContextNode-Objekt**](icontextnode.md) bewegt.

</dd> <dt>

*pISubNodeToMove* \[ In\]
</dt> <dd>

Das zu verschiebende [**IContextNode-Objekt.**](icontextnode.md)

</dd> <dt>

*pParentContextNode* \[ In\]
</dt> <dd>

Das übergeordnete [**IContextNode-Objekt**](icontextnode.md) von *pISubNodeToMove.*

</dd> <dt>

*ulNewIndex* \[ In\]
</dt> <dd>

Der neue Speicherort von *pISubNodeToMove* in der Sammlung der Untergeordneten Knoten des übergeordneten Knotens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der des [**IInkAnalyzer**](iinkanalyzer.md)synchronisiert wird. Dieses Ereignis tritt während der Abstimmungsphase der Freihandanalyse oder als Reaktion auf eine Freihandanalysemethode auf, die einen [**IContextNode**](icontextnode.md) innerhalb der Auflistung der Unterknoten des übergeordneten Knotens verschiebt (siehe [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) und [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)).

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit [**IInkAnalyzer**](iinkanalyzer.md)finden Sie unter [Datenproxy mit Freihandanalyse.](data-proxy-with-ink-analysis.md)

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

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IContextNode::GetParentNode**](icontextnode-getparentnode.md)
</dt> <dt>

[**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




