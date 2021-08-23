---
description: Speichert Analyseergebnisse für eine bestimmte Kontextknotenauflistung, die einem IInkAnalyzer zugeordnet ist.
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: IInkAnalyzer::SaveResultsForNodes-Methode (IACom.h)
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
ms.openlocfilehash: 4386f9b051bf1cfcda6ee55d7b83728b096dc6f69de4d87745ce564f19249565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091569"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a>IInkAnalyzer::SaveResultsForNodes-Methode

Speichert Analyseergebnisse für eine bestimmte Kontextknotenauflistung, die einem [**IInkAnalyzer**](iinkanalyzer.md)zugeordnet ist.

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

*pContextNodes* \[ In\]
</dt> <dd>

Die [**IContextNode-Auflistung,**](icontextnode.md) für die Analyseergebnisse gespeichert werden sollen.

</dd> <dt>

*pulSerializedDataSize* \[ in, out\]
</dt> <dd>

Die Anzahl der Bytes in *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ out\]
</dt> <dd>

Zeiger auf die serialisierten Analysedaten.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, rufen Sie [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) für \* *ppbSerializedData* auf, wenn Sie die Informationen nicht mehr benötigen.

 

Diese Methode speichert die aktuellen Analyseergebnisse für die [**IContextNode-Objekte**](icontextnode.md) in *pContextNodes* und all ihren Vorgänger- und Nachfolgerkontextknoten. Diese Methode speichert keine Strichdaten. Es liegt in der Verantwortung Ihrer Anwendung, alle Analyseergebnisse und die entsprechenden Strichdaten zu synchronisieren, sofern sie beibehalten werden.

Wenn das zu speichernde [**IContextNode-Objekt**](icontextnode.md) nur teilweise aufgefüllt wird, gibt diese Methode einen Fehlercode zurück (siehe [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

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

[**IInkAnalyzer::SaveResultsForStrokes-Methode**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

