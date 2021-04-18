---
description: Tritt auf, nachdem der iinkanalyzer eine oder mehrere Eigenschaften eines icontextnode-Objekts aktualisiert hat.
ms.assetid: f626c263-31a4-45ee-ae04-3251eac0d652
title: '_IAnalysisProxyEvents:: contextnodebug-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodePropertiesUpdated
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fa035b89c531f3b2d230ab849ba20b945dd2d25c
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106365238"
---
# <a name="_ianalysisproxyeventscontextnodepropertiesupdated-event"></a>\_Ianalysisproxyevents:: contextnodebug-Ereignis

Tritt auf, nachdem der [**iinkanalyzer**](iinkanalyzer.md) eine oder mehrere Eigenschaften eines [**icontextnode**](icontextnode.md) -Objekts aktualisiert hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContextNodePropertiesUpdated(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeUpdated
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinkanalyzer* \[ in\]
</dt> <dd>

Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das die Eigenschaften aktualisiert.

</dd> <dt>

*pcontextnodebug* \[ in\]
</dt> <dd>

Das [**icontextnode**](icontextnode.md) -Objekt, dessen Eigenschaften aktualisiert werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine Ink Analyzer-Methode auf, die die Eigenschaften eines [**icontextnode**](icontextnode.md) ändert (siehe [**icontextnode:: GetPropertyData**](icontextnode-getpropertydata.md)).

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

[Kontext Knoten Eigenschaften](context-node-properties.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




