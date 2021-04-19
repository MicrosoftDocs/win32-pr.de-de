---
description: Tritt auf, bevor das iinkanalyzer-Objekt ein icontextnode-Objekt an eine neue Position in der Auflistung der untergeordneten Knoten des übergeordneten Knotens verschiebt.
ms.assetid: c7a5956e-ffc4-4205-9de3-e8b7d672156d
title: '_IAnalysisProxyEvents:: ContextNodeMovingToPosition-Ereignis (iacom. h)'
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
ms.openlocfilehash: 462e7428fb43fd998d769dd152e19f8109b04158
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106353268"
---
# <a name="_ianalysisproxyeventscontextnodemovingtoposition-event"></a>\_Ianalysisproxyevents:: ContextNodeMovingToPosition-Ereignis

Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) -Objekt ein [**icontextnode**](icontextnode.md) -Objekt an eine neue Position in der Auflistung der untergeordneten Knoten des übergeordneten Knotens verschiebt.

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

*pinkanalyzer* \[ in\]
</dt> <dd>

Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das das [**icontextnode**](icontextnode.md) -Objekt verschiebt.

</dd> <dt>

*pisubnoabtomove* \[ in\]
</dt> <dd>

Das [**icontextnode**](icontextnode.md) -Objekt, das verschoben werden soll.

</dd> <dt>

*pparameentcontextnode* \[ in\]
</dt> <dd>

Das übergeordnete [**icontextnode**](icontextnode.md) -Objekt von *pisubnodecotomove*.

</dd> <dt>

*ulnetwindex* \[ in\]
</dt> <dd>

Die neue Position von *pisubnodetomove* in der Auflistung der untergeordneten Knoten des übergeordneten Knotens.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Dieses Ereignis tritt während der Abstimmungsphase der frei Hand Analyse oder als Reaktion auf eine Ink Analyzer-Methode auf, die einen [**icontextnode**](icontextnode.md) in der Auflistung der untergeordneten Knoten des übergeordneten Knotens verschiebt (siehe [**icontextnode:: gettientnode**](icontextnode-getparentnode.md) und [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)).

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

[**Icontextnode:: getparameentnode**](icontextnode-getparentnode.md)
</dt> <dt>

[**Icontextnode:: getsubnodes**](icontextnode-getsubnodes.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




