---
description: Tritt auf, bevor der iinkanalyzer innerhalb des Bereichs eines teilweise aufgefüllten icontextnode-Objekts eine Analyse ausführt.
ms.assetid: c24e8adb-672f-444a-bccb-1e9e55bea432
title: _IAnalysisProxyEvents::P-Ereignis "opulatecontextnode" (iacom. h)
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
ms.openlocfilehash: e8aebe4ba777d62f90aa00c45ea0f1644e2b8183
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "104219056"
---
# <a name="_ianalysisproxyeventspopulatecontextnode-event"></a>\_Ianalysisproxyevents::P opulatecontextnode-Ereignis

Tritt auf, bevor der [**iinkanalyzer**](iinkanalyzer.md) innerhalb des Bereichs eines teilweise aufgefüllten [**icontextnode**](icontextnode.md) -Objekts eine Analyse ausführt.

## <a name="syntax"></a>Syntax


```C++
HRESULT PopulateContextNode(
  [in] IInkAnalyzer *pInkAnalyzer,
  [in] IContextNode *pContextNodeToPopulate
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinkanalyzer* \[ in\]
</dt> <dd>

Das [**iinkanalyzer**](iinkanalyzer.md) -Objekt, das eine Analyse durchführen soll.

</dd> <dt>

*pcontextnodebug* \[ in\]
</dt> <dd>

Das teilweise aufgefüllte [**icontextnode**](icontextnode.md) -Objekt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Wenn das **iinkanalyzer** -Ereignis dieses Ereignis auslöst, sollte die Anwendung *pcontextnodebug (pcontextnodebug*) auffüllen. Während der Analysephase löst **iinkanalyzer** dieses Ereignis aus, um Informationen für die Bereiche zu erhalten, in denen frei Hand Eingaben analysiert werden.

Wenn das Dokument Links für die *pcontextnodebug-topopulate* enthält, sollte Ihre Anwendung diese Links erstellen und hinzufügen. Dieser Prozess erfordert, dass sowohl der Quell-als auch der Zielknoten (einschließlich seiner Vorgänger) vollständig aufgefüllt werden, bevor der Ereignishandler für dieses Ereignis beendet wird (siehe [**icontextlink:: getsourcenode**](icontextlink-getsourcenode.md) und [**icontextlink:: getdestinationnode**](icontextlink-getdestinationnode.md)).

Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

Während der Hintergrundanalyse löst das [**iinkanalyzer**](iinkanalyzer.md) -Ereignis dieses Ereignis aus, nachdem es das [**\_ ianalysisevents:: leserytoricile**](-ianalysisevents-readytoreconcile.md) -Ereignis ausgelöst hat.

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

 

 




