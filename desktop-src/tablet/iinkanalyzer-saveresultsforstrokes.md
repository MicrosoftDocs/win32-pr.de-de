---
description: Speichert Analyseergebnisse für die angegebenen Striche, die einem iinkanalyzer zugeordnet sind.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'Iinkanalyzer:: saveresultsforstrokes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1371b056cf01beba75fdcbd427c526ed29d20c55
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343678"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a>Iinkanalyzer:: saveresultsforstrokes-Methode

Speichert Analyseergebnisse für die angegebenen Striche, die einem [**iinkanalyzer**](iinkanalyzer.md)zugeordnet sind.

## <a name="syntax"></a>Syntax


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*ulstrokeidscount* \[ in\]
</dt> <dd>

Die Anzahl der Stroke-IDs in **plstrokeids**.

</dd> <dt>

*plstrokeids* \[ in\]
</dt> <dd>

Das Array von Strich bezeichlern.

</dd> <dt>

*pulserializeddatasize* \[ in, out\]
</dt> <dd>

Die Anzahl der Bytes in *ppbserializeddata*.

</dd> <dt>

*ppbserializeddata* \[ Out, retval\]
</dt> <dd>

Zeiger auf die serialisierten Analysedaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, müssen Sie für ppbserializeddata " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, \*  Wenn Sie die Informationen nicht mehr benötigen.

 

Diese Methode speichert die aktuellen Analyseergebnisse für die angegebenen Striche. Diese Methode speichert die frei Hand Blatt- [**icontextnode**](icontextnode.md) -Objekte, die die Striche und alle übergeordneten Knoten dieser Kontext Knoten enthalten. Diese Methode speichert keine Stroke-Daten oder Analyse Hinweis Knoten. Es liegt in der Verantwortung der Anwendung, alle Analyseergebnisse und die zugehörigen hubdaten zu synchronisieren, falls Sie weiterhin vorhanden sind.

Diese Methode gibt einen Fehlercode zurück, wenn ein [**icontextnode**](icontextnode.md) -Objekt zum Speichern teilweise aufgefüllt wird (siehe [**icontextnode:: getpartiallyaufgefüllt**](icontextnode-getpartiallypopulated.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalyzer:: loadresults-Methode**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**Iinkanalyzer:: SaveResults-Methode**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**Iinkanalyzer:: saveresultsfornodes-Methode**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

