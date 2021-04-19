---
description: Tritt auf, wenn die aktuelle zwischen Analysephase abgeschlossen ist.
ms.assetid: 9ade61f4-bcfe-4c49-bda1-b60aaf780935
title: '_IAnalysisEvents:: IntermediateResults-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.IntermediateResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 33430225746ddd1a4099f89112f14f99f2b6da84
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355732"
---
# <a name="_ianalysiseventsintermediateresults-event"></a>\_Ianalysilvents:: IntermediateResults-Ereignis

Tritt auf, wenn die aktuelle zwischen Analysephase abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT IntermediateResults(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinkanalyzer* \[ in\]
</dt> <dd>

Der [**iinkanalyzer**](iinkanalyzer.md) , der die Analyse ausführt.

</dd> <dt>

*panalysisstatus* \[ in\]
</dt> <dd>

Das [**ianalysisstatus**](ianalysisstatus.md) -Objekt, das den Status der Zwischenergebnisse darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Das [**iinkanalyzer**](iinkanalyzer.md) -Ereignis löst dieses Ereignis aus, nachdem es die Zwischenergebnisse für die aktuelle Analysephase abgestimmt hat.

Wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird, weist dieses Ereignis darauf hin, dass der **iinkanalyzer** seine internen Daten für diese Analysephase geändert hat.

Sperren Sie die Datenstruktur, wenn [**iinkanalyzer**](iinkanalyzer.md) das [**\_ ianalysisproxyevents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) -Ereignis auslöst. Änderungen an der Datenstruktur während dieser Analysephase können bei der frei Hand Analyse und-Synchronisierung zu Fehlern führen. Sie können ihre Datenstruktur entsperren, wenn **iinkanalyzer** das **\_ ianalysitsvents:: IntermediateResults** -oder [**\_ ianalysilvents:: results**](-ianalysisevents-results.md) -Ereignis auslöst.

Weitere Informationen zum Synchronisieren von Anwendungsdaten mit [**iinkanalyzer**](iinkanalyzer.md)finden Sie unter [Daten Proxy mit Ink-Analyse](data-proxy-with-ink-analysis.md).

Der [**iinkanalyzer**](iinkanalyzer.md) generiert nur dann Zwischenergebnisse, wenn für den Analysemodus das **AnalysisModes-Flag " \_ IntermediateResults** " festgelegt ist (siehe [**iinkanalyzer:: getanalysismodes-Methode**](iinkanalyzer-getanalysismodes.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**\_Ianalysil Vents**](-ianalysisevents.md)
</dt> <dt>

[**AnalysisModes**](analysismodes.md)
</dt> <dt>

[**\_Ianalysil Vents:: results**](-ianalysisevents-results.md)
</dt> <dt>

[**\_Ianalysisproxyevents**](-ianalysisproxyevents.md)
</dt> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>
