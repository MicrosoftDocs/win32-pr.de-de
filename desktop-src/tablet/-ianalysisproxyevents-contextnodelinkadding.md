---
description: Tritt ein, bevor das Ink-Analyseprogramm ein IContextLink-Objekt zwischen zwei IContextNode-Objekten hinzufügt.
ms.assetid: ec56cb8e-5154-45ee-911d-e2a240d19dc3
title: _IAnalysisProxyEvents::ContextNodeLinkAdding-Ereignis (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkAdding
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1d100d4ecb4caa6fb7230afd3d4ae6572466ae86855ac9bd28155b6b181cdd5a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452155"
---
# <a name="_ianalysisproxyeventscontextnodelinkadding-event"></a>\_IAnalysisProxyEvents::ContextNodeLinkAdding-Ereignis

Tritt ein, bevor das Ink-Analyseprogramm ein [**IContextLink-Objekt**](icontextlink.md) zwischen zwei [**IContextNode-Objekten**](icontextnode.md) hinzufügt.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContextNodeLinkAdding(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeAdded
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInkAnalyzer* \[ In\]
</dt> <dd>

Der [**IInkAnalyzer,**](iinkanalyzer.md) der den Link hinzufügt.

</dd> <dt>

*pContextLinkToBeAdded* \[ In\]
</dt> <dd>

Das [**hinzuzufügende IContextLink-Objekt.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der des [**IInkAnalyzer**](iinkanalyzer.md)synchronisiert wird. Dieses Ereignis tritt während der Abstimmungsphase der Ink-Analyse oder als Reaktion auf eine Ink-Analysemethode auf, die einem [**IContextNode**](icontextnode.md)einen neuen [**IContextLink**](icontextlink.md) hinzufügt.

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit [**IInkAnalyzer**](iinkanalyzer.md)finden Sie unter [Datenproxy mit Freihandanalyse.](data-proxy-with-ink-analysis.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen:

<dl> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




