---
description: Tritt auf, wenn der iinkanalyzer einen Strich von einem icontextnode-Objekt zu einem anderen verschiebt.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: '_IAnalysisProxyEvents:: strokereparame-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.StrokeReparented
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a587acb6534641d5d64981ab25247b0e23e4f347
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106361130"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a>\_Ianalysisproxyevents:: strokereproented-Ereignis

Tritt auf, wenn der [**iinkanalyzer**](iinkanalyzer.md) einen Strich von einem [**icontextnode**](icontextnode.md) -Objekt zu einem anderen verschiebt.

## <a name="syntax"></a>Syntax


```C++
HRESULT StrokeReparented(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] LONG         lStrokeIdToMove,
  [in] IContextNode *pSourceContextNode,
  [in] IContextNode *pDestinationContextNode
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinkanalyzer* \[ in\]
</dt> <dd>

Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das den Strich verschiebt.

</dd> <dt>

*lstrokeidtomove* \[ in\]
</dt> <dd>

Der Bezeichner des zu verschiebenden Strichs.

</dd> <dt>

*psourcecontextnode* \[ in\]
</dt> <dd>

Das [**icontextnode**](icontextnode.md) -Objekt, aus dem der Strich verschoben wird.

</dd> <dt>

*pdestinationcontextnode* \[ in\]
</dt> <dd>

Das [**icontextnode**](icontextnode.md) -Objekt, in das der Strich verschoben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine **iinkanalyzer** -Methode auf, die Strich Daten von einem [**icontextnode**](icontextnode.md) zu einem anderen verschiebt.

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

 

 




