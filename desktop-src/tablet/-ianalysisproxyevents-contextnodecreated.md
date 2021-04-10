---
description: Tritt auf, nachdem iinkanalyzer ein icontextnode-Objekt erstellt hat.
ms.assetid: b4ba0d3b-da91-4cc7-b071-240155687b83
title: '_IAnalysisProxyEvents:: contextnoentcreated-Ereignis (iacom. h)'
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
ms.openlocfilehash: ac06a7fc45604e93408b1bb144ee7e884efd351e
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "103961241"
---
# <a name="_ianalysisproxyeventscontextnodecreated-event"></a>\_Ianalysisproxyevents:: contextnoentcreated-Ereignis

Tritt auf, nachdem [**iinkanalyzer**](iinkanalyzer.md) ein [**icontextnode**](icontextnode.md) -Objekt erstellt hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContextNodeCreated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeCreated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinkanalyzer* \[ in\]
</dt> <dd>

Der [**iinkanalyzer**](iinkanalyzer.md) , der das [**icontextnode**](icontextnode.md) -Objekt erstellt.

</dd> <dt>

*pcontextnode erstellt* \[ in\]
</dt> <dd>

Das neue [**icontextnode**](icontextnode.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine Ink Analyzer-Methode auf, die einen [**icontextnode**](icontextnode.md)erstellt.

Wenn [**iinkanalyzer**](iinkanalyzer.md) einen [**icontextnode**](icontextnode.md)erstellt, enthält der neue **icontextnode** keine Striche, enthält keine Links zu anderen **icontextnode** -Objekten, und möglicherweise sind nicht alle zugehörigen Eigenschaften festgelegt. Außerdem wird der neue **icontextnode** am Ende der Auflistung der untergeordneten Knoten des übergeordneten Knotens hinzugefügt (siehe [**icontextnode:: gettientnode**](icontextnode-getparentnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)). Nach diesem Ereignis kann der **iinkanalyzer** die folgenden Ereignisse aufwecken.

-   Das [**\_ ianalysisproxyevents:: strokereprodent**](-ianalysisproxyevents-strokereparented.md) -Ereignis, wenn ein Strich von einem Kontext Knoten zu einem anderen verschoben wird.
-   Das [**\_ ianalysisproxyevents:: contextnodelta inkadditions**](-ianalysisproxyevents-contextnodelinkadding.md) -Ereignis, wenn einem [**icontextnode**](icontextnode.md)ein [**icontextlink**](icontextlink.md) hinzugefügt wird.
-   Das [**\_ ianalysisproxyevents:: ContextNodeMovingToPosition**](-ianalysisproxyevents-contextnodemovingtoposition.md) -Ereignis, wenn die Reihenfolge eines [**icontextnode**](icontextnode.md) in der Auflistung von untergeordneten Knoten des übergeordneten Knotens geändert wird.
-   Der [**iinkanalyzer**](iinkanalyzer.md) löst das [**\_ ianalysisproxyevents:: contextnodebug**](-ianalysisproxyevents-contextnodepropertiesupdated.md) -Ereignis aus, nachdem der Zustand von [**icontextnode**](icontextnode.md) für diese Analysephase aufgelöst wurde.

Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_Ianalysisproxyevents**](-ianalysisproxyevents.md)
</dt> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




