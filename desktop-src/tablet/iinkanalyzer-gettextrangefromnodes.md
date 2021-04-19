---
description: Sucht den Textbereich in der erkannten Zeichenfolge, der einer Auflistung von icontextnode-Objekten entspricht.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: 'Iinkanalyzer:: GetTextRangeFromNodes-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.GetTextRangeFromNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da27206a33ca58cebd10192393c4cf2efd1d5919
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106350454"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a>Iinkanalyzer:: GetTextRangeFromNodes-Methode

Sucht den Textbereich in der erkannten Zeichenfolge, der einer Auflistung von [**icontextnode**](icontextnode.md) -Objekten entspricht.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetTextRangeFromNodes(
  [out] LONG          *plStart,
  [out] LONG          *plLength,
  [in]  IContextNodes *pNodesToSearch
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*plstart* \[ vorgenommen\]
</dt> <dd>

Eine 32-Bit-Ganzzahl mit Vorzeichen, die den Anfang des Text Bereichs angibt. Dieser Parameter wird nicht initialisiert übergeben.

</dd> <dt>

*pllength* \[ vorgenommen\]
</dt> <dd>

Eine 32-Bit-Ganzzahl mit Vorzeichen, die die Länge des Text Bereichs angibt. Dieser Parameter wird nicht initialisiert übergeben.

</dd> <dt>

*pnodebug Search* \[ in\]
</dt> <dd>

Die Auflistung von [**icontextnode**](icontextnode.md) -Objekten, für die der Textbereich gesucht werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Wenn *pnodestosearch* [**icontextnode**](icontextnode.md) -Objekte enthält, die nicht angrenzenden sind, gibt diese Methode den kleinsten Textbereich zurück, der alle **icontextnode** -Objekte abdeckt.

Diese Methode löst eine E \_ invalidArg-Ausnahme aus, wenn *pnodestosearch* einen [**icontextnode**](icontextnode.md) enthält, der nicht mit [**iinkanalyzer**](iinkanalyzer.md)verknüpft ist.

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
</dt> </dl>

 

 




