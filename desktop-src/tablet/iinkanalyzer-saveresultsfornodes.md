---
description: Speichert Analyseergebnisse für eine bestimmte Kontext Knoten Sammlung, die mit einem iinkanalyzer verknüpft ist.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'Iinkanalyzer:: saveresultsfornodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eb628fafb9bf479e6a011137105005e541180aec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129444"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a>Iinkanalyzer:: saveresultsfornodes-Methode

Speichert Analyseergebnisse für eine bestimmte Kontext Knoten Sammlung, die mit einem [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pcontextnodes* \[ in\]
</dt> <dd>

Die [**icontextnode**](icontextnode.md) -Auflistung, für die Analyseergebnisse gespeichert werden sollen.

</dd> <dt>

*pulserializeddatasize* \[ in, out\]
</dt> <dd>

Die Anzahl der Bytes in *ppbserializeddata*.

</dd> <dt>

*ppbserializeddata* \[ vorgenommen\]
</dt> <dd>

Zeiger auf die serialisierten Analysedaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, müssen Sie für ppbserializeddata " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) " aufrufen, \*  Wenn Sie die Informationen nicht mehr benötigen.

 

Diese Methode speichert die aktuellen Analyseergebnisse für die [**icontextnode**](icontextnode.md) -Objekte in *pcontextnodes* und alle deren Vorgänger-und Nachfolger Kontext Knoten. Diese Methode speichert keine Strich Daten. Es liegt in der Verantwortung der Anwendung, alle Analyseergebnisse und die zugehörigen hubdaten zu synchronisieren, falls Sie weiterhin vorhanden sind.

Wenn das zu speichernde [**icontextnode**](icontextnode.md) -Objekt nur teilweise aufgefüllt ist, gibt diese Methode einen Fehlercode zurück (siehe [**icontextnode:: getpartiallygefüllte**](icontextnode-getpartiallypopulated.md)).

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

[**Iinkanalyzer:: saveresultsforstrokes-Methode**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

