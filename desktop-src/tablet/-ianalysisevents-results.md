---
description: Tritt auf, wenn die abschließende Analysephase abgeschlossen ist.
ms.assetid: 97318c2d-980e-436c-b97d-e064bace5bf0
title: '_IAnalysisEvents:: results-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.Results
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: bd52a5ce4563827fb22a00f79113fe1e80e852b3
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106355112"
---
# <a name="_ianalysiseventsresults-event"></a>\_Ianalysil Vents:: results-Ereignis

Tritt auf, wenn die abschließende Analysephase abgeschlossen ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT Results(
  [in] IInkAnalyzer    *pInkAnalyzer,
  [in] IAnalysisStatus *pAnalysisStatus
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pinkanalyzer* \[ in\]
</dt> <dd>

Der [**iinkanalyzer**](iinkanalyzer.md) , der die Analyseergebnisse erzeugt.

</dd> <dt>

*panalysisstatus* \[ in\]
</dt> <dd>

Das [**ianalysisstatus**](ianalysisstatus.md) -Objekt, das den Status der Analyse darstellt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Das [**iinkanalyzer**](iinkanalyzer.md) -Ereignis löst dieses Ereignis aus, nachdem es die Ergebnisse für die abschließende Analysephase abgestimmt hat.

Wenn Ihre Anwendung die [**iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)aufruft, signalisiert dieses Ereignis, wann die Analyseergebnisse bereit sind.

Wenn Ihre Anwendung ihre eigene Datenstruktur verwaltet, die mit der von [**iinkanalyzer**](iinkanalyzer.md)synchronisiert wird, weist dieses Ereignis darauf hin, dass der **iinkanalyzer** seine internen Daten für diese Analysephase geändert hat.

Sperren Sie die Datenstruktur, wenn [**iinkanalyzer**](iinkanalyzer.md) das [**\_ ianalysisproxyevents:: InkAnalyzerStateChanging**](-ianalysisproxyevents-inkanalyzerstatechanging.md) -Ereignis auslöst. Änderungen an der Datenstruktur während dieser Analysephase können bei der frei Hand Analyse und-Synchronisierung zu Fehlern führen. Entsperren Sie Ihre Datenstruktur, wenn **iinkanalyzer** das [**\_ ianalysitsvents:: IntermediateResults**](-ianalysisevents-intermediateresults.md) -oder **\_ ianalysilvents:: results** -Ereignis auslöst.

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

[**\_Ianalysil Vents**](-ianalysisevents.md)
</dt> <dt>

[**\_Ianalysisproxyevents**](-ianalysisproxyevents.md)
</dt> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalyzer:: analysierungsmethode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**Iinkanalyzer:: BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**Ianalysisstatus**](ianalysisstatus.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




