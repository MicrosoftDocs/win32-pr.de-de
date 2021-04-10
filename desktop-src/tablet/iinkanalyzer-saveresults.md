---
description: Speichert alle Analyseergebnisse für einen iinkanalyzer.
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'Iinkanalyzer:: SaveResults-Methode (iacom. h)'
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
ms.openlocfilehash: a07351662512ad3234dfe6847cd8c4300bd035e5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343679"
---
# <a name="iinkanalyzersaveresults-method"></a>Iinkanalyzer:: SaveResults-Methode

Speichert alle Analyseergebnisse für einen [**iinkanalyzer**](iinkanalyzer.md).

## <a name="syntax"></a>Syntax


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulserializeddatasize* \[ vorgenommen\]
</dt> <dd>

Die Anzahl der Bytes in *ppbserializeddata*.

</dd> <dt>

*ppbserializeddata* \[ vorgenommen\]
</dt> <dd>

Ein Array, das die gespeicherten Analyseergebnisse enthält.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppbserializeddata* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

Diese Methode speichert alle aktuellen Analyseergebnisse, einschließlich aktueller Analyse Hinweis und benutzerdefinierter Erkennungs Knoten (siehe [**icontextnode:: GetType**](icontextnode-gettype.md)). Diese Methode speichert keine Strich Daten. Es liegt in der Verantwortung der Anwendung, Analyseergebnisse und entsprechende Striche zu synchronisieren, wenn Sie Daten beibehalten.

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

[**Iinkanalyzer:: saveresultsfornodes-Methode**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**Iinkanalyzer:: saveresultsforstrokes-Methode**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

