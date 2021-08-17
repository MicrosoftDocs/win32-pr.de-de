---
description: Tritt ein, bevor IInkAnalyzer eine Analyse im Bereich eines teilweise aufgefüllten IContextNode-Objekts ausführt.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents::P opulateContextNode-Ereignis (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.PopulateContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ff6378f7ecf3ff597f4c02740e30544ff65651d0a7fcd6d6d490ebabf2161ef7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967929"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a>\_IAnalysisProxyEvents::P opulateContextNode-Ereignis

Tritt ein, bevor [**IInkAnalyzer**](iinkanalyzer.md) eine Analyse im Bereich eines teilweise aufgefüllten [**IContextNode-Objekts**](icontextnode.md) ausführt.

## <a name="syntax"></a>Syntax


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pInkAnalyzer* \[ In\]
</dt> <dd>

Das [**IInkAnalyzer-Objekt,**](iinkanalyzer.md) das eine Analyse durchführen soll.

</dd> <dt>

*pContextNodeToPopulate* \[ In\]
</dt> <dd>

Das teilweise [**aufgefüllte IContextNode-Objekt.**](icontextnode.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur bei behält, die mit der von [**IInkAnalyzer synchronisiert wird.**](iinkanalyzer.md) Wenn **der IInkAnalyzer dieses** Ereignis löst, sollte Ihre Anwendung *den pContextNodeToPopulate auffüllen.* Während der Analysephase löst **der IInkAnalyzer** dieses Ereignis aus, um Informationen zu Bereichen zu erhalten, in denen die Ink-Analyse durchgeführt wird.

Wenn das Dokument Links für *pContextNodeToPopulate* enthält, sollte Ihre Anwendung diese Links erstellen und hinzufügen. Dieser Prozess erfordert, dass sowohl die Quell- als auch die Zielknoten einschließlich ihrer Vorgänger vollständig aufgefüllt werden, bevor der Ereignishandler für dieses Ereignis beendet wird (siehe [**IContextLink::GetSourceNode**](icontextlink-getsourcenode.md) und [**IContextLink::GetDestinationNode**](icontextlink-getdestinationnode.md)).

Weitere Informationen zum Synchronisieren Ihrer Anwendungsdaten mit [**IInkAnalyzer**](iinkanalyzer.md)finden Sie unter [Datenproxy mit Ink-Analyse.](data-proxy-with-ink-analysis.md)

Während der Hintergrundanalyse löst [**der IInkAnalyzer**](iinkanalyzer.md) dieses Ereignis aus, nachdem es das [**\_ IAnalysisEvents::ReadyToReconcile-Ereignis ausgelöst**](-ianalysisevents-readytoreconcile.md) hat.

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

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




