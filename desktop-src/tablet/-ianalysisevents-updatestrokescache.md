---
description: Tritt ein, bevor IInkAnalyzer auf Strichdaten zugreift.
ms.assetid: fed46476-4531-4516-9375-d7b654efb3be
title: _IAnalysisEvents::UpdateStrokesCache-Ereignis (IACom.h)
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
ms.openlocfilehash: 9a5854c8061a12dc558a2ca20ebd893880f899b2113065abd9b8122c53812aa0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118047372"
---
# <a name="_ianalysiseventsupdatestrokescache-event"></a>\_IAnalysisEvents::UpdateStrokesCache-Ereignis

Tritt ein, bevor [**IInkAnalyzer**](iinkanalyzer.md) auf Strichdaten zugreift.

## <a name="syntax"></a>Syntax


```C++
HRESULT UpdateStrokesCache(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulStrokeIdsCount* \[ In\]
</dt> <dd>

Die Anzahl der Strichbezeichner in *plStrokeIds*.

</dd> <dt>

*plStrokeIds* \[ In\]
</dt> <dd>

Die Bezeichner der Striche, deren Paketdaten gelöscht wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

Der [**IInkAnalyzer**](iinkanalyzer.md) löst dieses Ereignis während der Freihandanalyse aus, wenn er auf einen oder mehrere Striche zugreift, für die die Paketdaten gelöscht wurden. Um die Strichpaketdaten zu aktualisieren, verwenden Sie die [**IInkAnalyzer::UpdateStrokesData-Methode.**](iinkanalyzer-updatestrokesdata.md)

Der [**IInkAnalyzer**](iinkanalyzer.md) gibt dieses Ereignis nicht aus, wenn auf einen teilweise aufgefüllten Freihandblattknoten zugegriffen wird, wenn die Position des Knotens nicht vom **IInkAnalyzer** festgelegt wurde.

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

[**\_IAnalysisEvents**](-ianalysisevents.md)
</dt> <dt>

[**\_IAnalysisProxyEvents**](-ianalysisproxyevents.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::Analyze-Methode**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer::BackgroundAnalyze-Methode**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer::UpdateStrokesData-Methode**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[**IContextNode::CreatePartiallyPopulatedSubNode**](icontextnode-createpartiallypopulatedsubnode.md)
</dt> <dt>

[**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




