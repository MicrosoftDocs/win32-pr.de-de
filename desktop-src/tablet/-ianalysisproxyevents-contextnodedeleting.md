---
description: Tritt ein, bevor IInkAnalyzer ein IContextNode-Objekt löscht.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: _IAnalysisProxyEvents::ContextNodeDeleting-Ereignis (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0610aa6a68814e291b3d0da09669eb6834ed78de0bcfc88044668733e325b033
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117675566"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a>\_IAnalysisProxyEvents::ContextNodeDeleting-Ereignis

Tritt ein, bevor [**IInkAnalyzer**](iinkanalyzer.md) ein [**IContextNode-Objekt**](icontextnode.md) löscht.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInkAnalyzer* \[ In\]
</dt> <dd>

Das [**IInkAnalyzer-Objekt,**](iinkanalyzer.md) das das [**IContextNode-Objekt**](icontextnode.md) löscht.

</dd> <dt>

*pContextNodeToBeDeleted* \[ In\]
</dt> <dd>

Das zu löschende [**IContextNode-Objekt.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der des [**IInkAnalyzer**](iinkanalyzer.md)synchronisiert wird. Dieses Ereignis tritt während der Abstimmungsphase der Ink-Analyse oder als Reaktion auf eine Ink-Analysemethode auf, die einen [**IContextNode**](icontextnode.md)löscht.

Bevor [**IInkAnalyzer**](iinkanalyzer.md) einen [**IContextNode**](icontextnode.md)löscht, entfernt **IInkAnalyzer** alle Striche aus dem Kontextknoten und entfernt alle Links zu anderen Kontextknoten. Bevor der Kontextknoten entfernt wird, kann **IInkAnalyzer** die folgenden Ereignisse auslösen.

-   Das [**\_ IAnalysisProxyEvents::StrokeReparented-Ereignis,**](-ianalysisproxyevents-strokereparented.md) wenn ein Strich aus dem [**IContextNode**](icontextnode.md)verschoben wird.
-   Das [**\_ IAnalysisProxyEvents::ContextNodeLinkDeleting-Ereignis,**](-ianalysisproxyevents-contextnodelinkdeleting.md) bevor ein [**IContextLink**](icontextlink.md) aus dem [**IContextNode**](icontextnode.md)entfernt wird.
-   Das **\_ IAnalysisProxyEvents::ContextNodeDeleting-Ereignis,** bevor es einen übergeordneten Kontextknoten entfernt, der nicht mehr über untergeordnete Knoten verfügt.

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit [**IInkAnalyzer**](iinkanalyzer.md)finden Sie unter [Datenproxy mit Freihandanalyse.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

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

 

 




