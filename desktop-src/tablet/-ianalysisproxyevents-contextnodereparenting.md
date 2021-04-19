---
description: Tritt auf, bevor das iinkanalyzer-Objekt durch Ändern des übergeordneten Knotens verschoben wird.
ms.assetid: 91261270-aa7c-4f0a-a790-1b2bf322a3ad
title: '_IAnalysisProxyEvents:: contextnoderethenting-Ereignis (iacom. h)'
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
ms.openlocfilehash: 084f971edc5adce0845fc7e1c3ea6ea59a066bb0
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363047"
---
# <a name="_ianalysisproxyeventscontextnodereparenting-event"></a>\_Ianalysisproxyevents:: contextnoderesienting-Ereignis

Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) [**-Objekt durch**](icontextnode.md) Ändern des übergeordneten Knotens verschoben wird.

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

*pinkanalyzer* \[ in\]
</dt> <dd>

Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das das [**icontextnode**](icontextnode.md) -Objekt verschiebt.

</dd> <dt>

*pnewparameentcontextnode* \[ in\]
</dt> <dd>

Das neue übergeordnete [**icontextnode**](icontextnode.md) -Objekt.

</dd> <dt>

*pcontextnodebug* \[ in\]
</dt> <dd>

Das [**icontextnode**](icontextnode.md) -Objekt, das verschoben werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine Methode auf, die einen [**icontextnode**](icontextnode.md) aus einer Auflistung von untergeordneten Knoten zu einem anderen verschiebt (siehe [**icontextnode:: gettientnode**](icontextnode-getparentnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)).

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

[**Icontextnode:: getparameentnode**](icontextnode-getparentnode.md)
</dt> <dt>

[**Icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




