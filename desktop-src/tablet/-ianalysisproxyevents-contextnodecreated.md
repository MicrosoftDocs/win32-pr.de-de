---
description: Tritt ein, nachdem IInkAnalyzer ein IContextNode-Objekt erstellt hat.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: _IAnalysisProxyEvents::ContextNodeCreated-Ereignis (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeCreated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5938ffda54542602248c5d04da0726d932b381aaff092f1c2038dd37ae4631e7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675867"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a>\_IAnalysisProxyEvents::ContextNodeCreated-Ereignis

Tritt ein, nachdem [**IInkAnalyzer ein**](iinkanalyzer.md) [**IContextNode-Objekt erstellt**](icontextnode.md) hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInkAnalyzer* \[ In\]
</dt> <dd>

Der [**IInkAnalyzer, der**](iinkanalyzer.md) das [**IContextNode-Objekt**](icontextnode.md) erstellt.

</dd> <dt>

*pContextNodeCreated* \[ In\]
</dt> <dd>

Das neue [**IContextNode-Objekt.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur bei behält, die mit der von [**IInkAnalyzer synchronisiert wird.**](iinkanalyzer.md) Dieses Ereignis tritt während der Abstimmungsphase der Ink-Analyse oder als Reaktion auf eine Ink Analyzer-Methode auf, die einen [**IContextNode erstellt.**](icontextnode.md)

Wenn [**der IInkAnalyzer**](iinkanalyzer.md) einen [**IContextNode**](icontextnode.md)erstellt, enthält der neue **IContextNode** keine Striche, enthält keine Links zu anderen **IContextNode-Objekten** und verfügt möglicherweise nicht über alle festgelegten Eigenschaften. Außerdem wird der neue **IContextNode** am Ende der Auflistung der Untergeordneten Knoten des übergeordneten Knotens hinzugefügt (siehe [**IContextNode::GetParentNode**](icontextnode-getparentnode.md) und [**IContextNode::GetSubNodes**](icontextnode-getsubnodes.md)). Nach diesem Ereignis kann **der IInkAnalyzer** die folgenden Ereignisse aus der NSD-2016-2016-2016-2016-2016-

-   Das [**\_ IAnalysisProxyEvents::StrokeReparented-Ereignis,**](-ianalysisproxyevents-strokereparented.md) wenn ein Strich von einem Kontextknoten auf einen anderen verschoben wird.
-   Das [**\_ IAnalysisProxyEvents::ContextNodeLinkAdding-Ereignis,**](-ianalysisproxyevents-contextnodelinkadding.md) wenn es einem [**IContextNode**](icontextnode.md)einen [**IContextLink**](icontextlink.md) hinzufügt.
-   Das [**\_ IAnalysisProxyEvents::ContextNodeMovingToPosition-Ereignis,**](-ianalysisproxyevents-contextnodemovingtoposition.md) wenn es die Reihenfolge eines [**IContextNode**](icontextnode.md) innerhalb der Auflistung der Untergeordneten Knoten des übergeordneten Knotens ändert.
-   Der [**IInkAnalyzer**](iinkanalyzer.md) löst das [**\_ IAnalysisProxyEvents::ContextNodePropertiesUpdated-Ereignis**](-ianalysisproxyevents-contextnodepropertiesupdated.md) aus, nachdem der Zustand des [**IContextNode**](icontextnode.md) für diese Analysephase behoben wurde.

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

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




