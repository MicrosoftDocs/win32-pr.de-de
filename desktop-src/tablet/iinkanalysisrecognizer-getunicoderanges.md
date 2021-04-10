---
description: Ruft ein Array von Zeichen Bereichen ab, die die unterstützten Unicode-Zeichen Bereiche darstellen.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: 'Iinkanalysiserkenzer:: GetUnicodeRanges-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetUnicodeRanges
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 939c2d5bf45c5dfbf0f1866cb6d0c7a58c38320f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862707"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a>Iinkanalysiserkenzer:: GetUnicodeRanges-Methode

Ruft ein Array von Zeichen Bereichen ab, die die unterstützten Unicode-Zeichen Bereiche darstellen.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetUnicodeRanges(
  [in, out] ULONG  *pulNumberOfRanges,
  [out]     WCHAR  **ppulLowUnicode,
  [out]     USHORT **ppusUnicodeRangeLength
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulnummeriofranges* \[ in, out\]
</dt> <dd>

Die Anzahl der Zeichen Bereiche, auf die von *ppullowunicode* verwiesen wird.

</dd> <dt>

*ppullowunicode* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von Zeichen Bereichen, die die unterstützten Unicode-Zeichen Bereiche darstellen.

</dd> <dt>

*ppusunicoderangelength* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf ein Array von-Werten, das die Länge der einzelnen Array Punkte von *ppullowunicode* angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Iinkanalysiserkenzer**](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




