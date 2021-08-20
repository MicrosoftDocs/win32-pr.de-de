---
description: Tritt ein, bevor IInkAnalyzer ein IContextLink-Objekt zwischen zwei IContextNode-Objekten löscht.
ms.assetid: bc9716b8-8793-4886-aff4-d880024129a6
title: _IAnalysisProxyEvents::ContextNodeLinkDeleting -Ereignis (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.ContextNodeLinkDeleting
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2bf45b8ae900d574bc50151e1bd17f0a124211272d4a83ccb43216ebbf82e2f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452085"
---
# <a name="_ianalysisproxyeventscontextnodelinkdeleting-event"></a>\_IAnalysisProxyEvents::ContextNodeLinkDeleting-Ereignis

Tritt ein, bevor [**IInkAnalyzer**](iinkanalyzer.md) ein [**IContextLink-Objekt**](icontextlink.md) zwischen zwei [**IContextNode-Objekten löscht.**](icontextnode.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT ContextNodeLinkDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextLink *pContextLinkToBeDeleted
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInkAnalyzer* \[ In\]
</dt> <dd>

[**IInkAnalyzer löscht**](iinkanalyzer.md) den Link.

</dd> <dt>

*pContextLinkToBeDeleted* \[ In\]
</dt> <dd>

Das zu löschende [**IContextLink-Objekt.**](icontextlink.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur bei behält, die mit der von [**IInkAnalyzer synchronisiert wird.**](iinkanalyzer.md) Dieses Ereignis tritt während der Abstimmungsphase der Ink-Analyse oder als Reaktion auf eine **IInkAnalyzer-Methode** auf, die einen [**IContextLink**](icontextlink.md) aus einem [**IContextNode entfernt.**](icontextnode.md)

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

[**IContextLink**](icontextlink.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




