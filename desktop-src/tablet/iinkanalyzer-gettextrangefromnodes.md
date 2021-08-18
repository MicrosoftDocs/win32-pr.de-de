---
description: Sucht den Textbereich in der erkannten Zeichenfolge, der einer Auflistung von IContextNode-Objekten entspricht.
ms.assetid: 2c5bc4a1-08de-4872-b552-6d22924ce2a8
title: IInkAnalyzer::GetTextRangeFromNodes-Methode (IACom.h)
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
ms.openlocfilehash: 147877ef8871f7b07e2aa501a107c1e40bd75e80009e5bee97dca03346bb853a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092130"
---
# <a name="iinkanalyzergettextrangefromnodes-method"></a>IInkAnalyzer::GetTextRangeFromNodes-Methode

Sucht den Textbereich in der erkannten Zeichenfolge, der einer Auflistung von [**IContextNode-Objekten**](icontextnode.md) entspricht.

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

*plStart* \[ out\]
</dt> <dd>

Eine 32-Bit-Ganzzahl mit Vorzeichen, die den Anfang des Textbereichs angibt. Dieser Parameter wird nicht initialisiert übergeben.

</dd> <dt>

*plLength* \[ out\]
</dt> <dd>

Eine 32-Bit-Ganzzahl mit Vorzeichen, die die Länge des Textbereichs angibt. Dieser Parameter wird nicht initialisiert übergeben.

</dd> <dt>

*pNodesToSearch* \[ In\]
</dt> <dd>

Die Auflistung von [**IContextNode-Objekten,**](icontextnode.md) für die der Textbereich gefunden werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Wenn *pNodesToSearch* [**IContextNode-Objekte**](icontextnode.md) enthält, die nicht nebeneinander liegen, gibt diese Methode den kleinsten Textbereich zurück, der alle **IContextNode-Objekte** abdeckt.

Diese Methode löst eine E INVALIDARG-Ausnahme aus, wenn \_ *pNodesToSearch* einen [**IContextNode**](icontextnode.md) enthält, der nicht dem [**IInkAnalyzer zugeordnet ist.**](iinkanalyzer.md)

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
</dt> </dl>

 

 




