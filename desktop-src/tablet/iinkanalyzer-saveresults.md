---
description: Speichert alle Analyseergebnisse für einen IInkAnalyzer.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: IInkAnalyzer::SaveResults-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 216f238776cf88a24d10f57671aa4f03c71d07962ff480d5b219653a5c9d338e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091990"
---
# <a name="iinkanalyzersaveresults-method"></a>IInkAnalyzer::SaveResults-Methode

Speichert alle Analyseergebnisse für einen [**IInkAnalyzer.**](iinkanalyzer.md)

## <a name="syntax"></a>Syntax


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulSerializedDataSize* \[ out\]
</dt> <dd>

Die Anzahl der Bytes in *ppbSerializedData*.

</dd> <dt>

*ppbSerializedData* \[ out\]
</dt> <dd>

Ein Array, das die gespeicherten Analyseergebnisse enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, verwenden Sie [**CoTaskMemFree,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um den Arbeitsspeicher von \* *ppbSerializedData* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

Diese Methode speichert alle aktuellen Analyseergebnisse, die aktuelle Analysehinweise und benutzerdefinierte Erkennungsknoten enthalten (siehe [**IContextNode::GetType**](icontextnode-gettype.md)). Diese Methode speichert keine Strichdaten. Es liegt in der Verantwortung Ihrer Anwendung, alle Analyseergebnisse und die entsprechenden Striche zu synchronisieren, wenn daten beibehalten werden.

Diese Methode gibt einen Fehlercode zurück, wenn ein zu speicherndes [**IContextNode-Objekt**](icontextnode.md) teilweise aufgefüllt wird (siehe [**IContextNode::GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)).

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

[**IInkAnalyzer::SaveResultsForNodes-Methode**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IInkAnalyzer::SaveResultsForStrokes-Methode**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

