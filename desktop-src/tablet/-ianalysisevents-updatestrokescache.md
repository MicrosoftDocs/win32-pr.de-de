---
description: Tritt auf, bevor der iinkanalyzer auf Stroke-Daten zugreift.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: '_IAnalysisEvents:: updatestrokescache-Ereignis (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- _IAnalysisEvents.UpdateStrokesCache
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 5d16011d8c5fe571d228b632fecb7a973bafcbf5
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/05/2021
ms.locfileid: "106363045"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a>\_Ianalysil Vents:: updatestrokescache-Ereignis

Tritt auf, bevor der [**iinkanalyzer**](iinkanalyzer.md) auf Stroke-Daten zugreift.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulstrokeidscount* \[ in\]
</dt> <dd>

Die Anzahl der Stroke-IDs in *plstrokeids*.

</dd> <dt>

*plstrokeids* \[ in\]
</dt> <dd>

Die Bezeichner der Striche, deren Paketdaten gelöscht wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Der [**iinkanalyzer**](iinkanalyzer.md) löst dieses Ereignis während der Handschrift Analyse aus, wenn er auf einen oder mehrere Striche zugreift, für die die Paketdaten gelöscht wurden. Verwenden Sie die [**Methode iinkanalyzer:: UpdateStrokesData**](iinkanalyzer-updatestrokesdata.md) , um die Daten des Stroke-Pakets zu aktualisieren.

Der [**iinkanalyzer**](iinkanalyzer.md) gibt dieses Ereignis nicht aus, wenn er auf einen teilweise gefüllten frei Hand Blattknoten zugreift, wenn die Position des Knotens nicht durch **iinkanalyzer** festgelegt wurde.

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

[**Iinkanalyzer:: UpdateStrokesData-Methode**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[**Icontextnode:: kreatepartiallypopulatedsubnode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**Icontextnode:: getpartiallyaufgefüllt**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




