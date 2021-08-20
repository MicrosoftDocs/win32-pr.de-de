---
description: Tritt ein, wenn der IInkAnalyzer einen Strich von einem IContextNode-Objekt in ein anderes verschiebt.
ms.assetid: a90214af-c3ea-4e2a-94b4-bb5746a2b476
title: _IAnalysisProxyEvents::StrokeReparented-Ereignis (IACom.h)
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
ms.openlocfilehash: 1e9262eb7b4ce2b323669eeb084abb597b5fe00488df90fc5fde0b2876b7e953
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967869"
---
# <a name="_ianalysisproxyeventsstrokereparented-event"></a>\_IAnalysisProxyEvents::StrokeReparented-Ereignis

Tritt ein, wenn [**der IInkAnalyzer**](iinkanalyzer.md) einen Strich von einem [**IContextNode-Objekt**](icontextnode.md) in ein anderes verschiebt.

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

*pInkAnalyzer* \[ In\]
</dt> <dd>

Das [**IInkAnalyzer-Objekt,**](iinkanalyzer.md) das den Strich bewegt.

</dd> <dt>

*lStrokeIdToMove* \[ In\]
</dt> <dd>

Der Bezeichner des zu verschiebenden Strichs.

</dd> <dt>

*pSourceContextNode* \[ In\]
</dt> <dd>

Das [**IContextNode-Objekt,**](icontextnode.md) aus dem der Strich verschoben wird.

</dd> <dt>

*pDestinationContextNode* \[ In\]
</dt> <dd>

Das [**IContextNode-Objekt,**](icontextnode.md) in das der Strich verschoben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der des [**IInkAnalyzer**](iinkanalyzer.md)synchronisiert wird. Dieses Ereignis tritt während der Abstimmungsphase der Freihandanalyse oder als Reaktion auf eine **IInkAnalyzer-Methode** auf, die Strichdaten von einem [**IContextNode**](icontextnode.md) in einen anderen verschiebt.

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

 

 




