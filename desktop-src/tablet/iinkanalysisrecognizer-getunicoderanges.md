---
description: Ruft ein Array von Zeichenbereichen ab, die die unterstützten Unicode-Zeichenbereiche darstellen.
ms.assetid: 334cf545-832a-4e8a-8fe6-76a173676be7
title: IInkAnalysisRecognizer::GetUnicodeRanges-Methode (IACom.h)
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
ms.openlocfilehash: cf8c0fe75d2eff0cdd8f2f9d3eb5366f6bab4dd4588c854455804ce4196971bc
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008400"
---
# <a name="iinkanalysisrecognizergetunicoderanges-method"></a>IInkAnalysisRecognizer::GetUnicodeRanges-Methode

Ruft ein Array von Zeichenbereichen ab, die die unterstützten Unicode-Zeichenbereiche darstellen.

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

*pulNumberOfRanges* \[ in, out\]
</dt> <dd>

Die Anzahl der Zeichenbereiche, auf die *ppulLowUnicode* zeigt.

</dd> <dt>

*ppulLowUnicode* \[ out\]
</dt> <dd>

Zeiger auf ein Array von Zeichenbereichen, das die unterstützten Unicode-Zeichenbereiche darstellt.

</dd> <dt>

*ppusUnicodeRangeLength* \[ out\]
</dt> <dd>

Zeiger auf ein Array von -Werten, das die Länge jedes Arrays angibt, auf das *ppulLowUnicode* zeigt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> </dl>

 

 




