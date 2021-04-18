---
description: Tritt auf, bevor das iinkanalyzer-Objekt ein icontextnode-Objekt löscht.
ms.assetid: 9c89198e-cc64-4041-b7a3-457f94c4aeaf
title: '_IAnalysisProxyEvents:: contextnodebug-Ereignis (iacom. h)'
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
ms.openlocfilehash: 26488c5657b6d2765534f82b6eacae774adcf561
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106354290"
---
# <a name="_ianalysisproxyeventscontextnodedeleting-event"></a>\_Ianalysisproxyevents:: contextnodebug-Ereignis

Tritt auf, bevor das [**iinkanalyzer**](iinkanalyzer.md) -Objekt ein [**icontextnode**](icontextnode.md) -Objekt löscht.

## <a name="syntax"></a>Syntax


```C++
HRESULT ContextNodeDeleting(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToBeDeleted
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinkanalyzer* \[ in\]
</dt> <dd>

Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das das [**icontextnode**](icontextnode.md) -Objekt löscht.

</dd> <dt>

*pcontextnodebug* \[ in\]
</dt> <dd>

Das [**icontextnode**](icontextnode.md) -Objekt, das gelöscht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Dieses Ereignis tritt während der ababstimmungs Phase der frei Hand Analyse oder als Reaktion auf eine Ink Analyzer-Methode auf, die einen [**icontextnode**](icontextnode.md)löscht.

Bevor [**iinkanalyzer**](iinkanalyzer.md) einen [**icontextnode**](icontextnode.md)löscht, entfernt **iinkanalyzer** alle Striche aus dem Kontext Knoten und entfernt alle Verknüpfungen zu anderen Kontext Knoten. Vor dem Entfernen des Kontext Knotens kann **iinkanalyzer** die folgenden Ereignisse hervorrufen.

-   Das [**\_ ianalysisproxyevents:: strokereprodent**](-ianalysisproxyevents-strokereparented.md) -Ereignis, wenn es einen Strich aus dem [**icontextnode**](icontextnode.md)verschiebt.
-   Das [**\_ ianalysisproxyevents:: contextnodelinklösch**](-ianalysisproxyevents-contextnodelinkdeleting.md) -Ereignis, bevor ein [**icontextlink**](icontextlink.md) aus dem [**icontextnode**](icontextnode.md)entfernt wird.
-   Das **\_ ianalysisproxyevents:: contextnodelösch** -Ereignis, bevor ein übergeordneter Kontext Knoten entfernt wird, der keine untergeordneten Knoten mehr aufweist.

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

 

 




