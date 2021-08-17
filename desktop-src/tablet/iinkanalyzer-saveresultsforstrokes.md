---
description: Speichert Analyseergebnisse für die angegebenen Striche, die einem IInkAnalyzer zugeordnet sind.
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: IInkAnalyzer::SaveResultsForStrokes-Methode (IACom.h)
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
ms.openlocfilehash: fd9a95ada1385fdbb6dbc5a1e22cde0ef319156ad7c3cd7782e911d06696af37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091560"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a>IInkAnalyzer::SaveResultsForStrokes-Methode

Speichert Analyseergebnisse für die angegebenen Striche, die einem [**IInkAnalyzer zugeordnet sind.**](iinkanalyzer.md)

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

*ulStrokeIdsCount* \[ In\]
</dt> <dd>

Die Anzahl der Strichbezeichner in **plStrokeIds**.

</dd> <dt>

*plStrokeIds* \[ In\]
</dt> <dd>

Das Array von Strichbezeichnern.

</dd> <dt>

*pulSerializedDataSize* \[ in, out\]
</dt> <dd>

Die Anzahl der Bytes in *ppbSerializedData.*

</dd> <dt>

*ppbSerializedData* \[ out, retval\]
</dt> <dd>

Zeiger auf die serialisierten Analysedaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Arbeitsspeicherverlust zu vermeiden, rufen Sie [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) für \* *ppbSerializedData* auf, wenn Sie die Informationen nicht mehr benötigen.

 

Diese Methode speichert die aktuellen Analyseergebnisse für die angegebenen Striche. Diese Methode speichert die [**IContextNode-Objekte**](icontextnode.md) des Ink-Blatts, die die Striche und alle Vorgänger dieser Kontextknoten enthalten. Mit dieser Methode werden keine Strichdaten- oder Analysehinweisknoten gespeichert. Es liegt in der Verantwortung Ihrer Anwendung, alle Analyseergebnisse und die entsprechenden Strichdaten zu synchronisieren, wenn sie beibehalten werden.

Diese Methode gibt einen Fehlercode zurück, wenn ein zu speichernde [**IContextNode-Objekt**](icontextnode.md) teilweise aufgefüllt wird (siehe [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer::LoadResults-Methode**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**IInkAnalyzer::SaveResults-Methode**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**IInkAnalyzer::SaveResultsForNodes-Methode**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

