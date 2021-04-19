---
description: Tritt auf, bevor die Analyseergebnisse von iinkanalyzer so synchronisiert werden, dass eine Anwendung Daten mit dem iinkanalyzer synchronisieren kann.
ms.assetid: 9daa8723-5234-40d9-ac41-6dcca988a8b4
title: '_IAnalysisProxyEvents:: InkAnalyzerStateChanging-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisProxyEvents.InkAnalyzerStateChanging
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 92535c34b5d107fb1e435e9abe229df46204f236
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355731"
---
# <a name="_ianalysisproxyeventsinkanalyzerstatechanging-event"></a>\_Ianalysisproxyevents:: InkAnalyzerStateChanging-Ereignis

Tritt auf, bevor die Analyseergebnisse von [**iinkanalyzer**](iinkanalyzer.md) so synchronisiert werden, dass eine Anwendung Daten mit dem **iinkanalyzer** synchronisieren kann.

## <a name="syntax"></a>Syntax


```C++
HRESULT InkAnalyzerStateChanging(
  [in] IInkAnalyzer *pInkAnalyzer
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinkanalyzer* \[ in\]
</dt> <dd>

Der [**iinkanalyzer**](iinkanalyzer.md) , der seine Analyseergebnisse abgleicht.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Verwenden Sie dieses Ereignis, wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird. Wenn das **iinkanalyzer** -Ereignis dieses Ereignis auslöst, sollte Ihre Anwendung die untergeordneten Knoten des Stamm Knotens der Ink Analyzer Auffüllen (siehe [**icontextnode:: getsubnodes**](icontextnode-getsubnodes.md) und [**iinkanalyzer:: GetRootNode-Methode**](iinkanalyzer-getrootnode.md)).

Das [**iinkanalyzer**](iinkanalyzer.md) -Ereignis löst dieses Ereignis aus, nachdem es das [**\_ ianalysitsvents:: leserytoricile**](-ianalysisevents-readytoreconcile.md) -Ereignis ausgelöst hat. Dieses Ereignis wird nur ausgelöst, wenn eine Hintergrundanalyse durchgeführt wird.

Sperren Sie die Datenstruktur, wenn [**iinkanalyzer**](iinkanalyzer.md) das **\_ ianalysisproxyevents:: InkAnalyzerStateChanging** -Ereignis auslöst. Änderungen an der Datenstruktur während dieser Analysephase können bei der frei Hand Analyse und-Synchronisierung zu Fehlern führen. Entsperren Sie Ihre Datenstruktur, wenn **iinkanalyzer** das [**\_ ianalysitsvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) -oder [**\_ ianalysilvents:: results**](-ianalysisevents-results.md) -Ereignis auslöst.

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

 

 




