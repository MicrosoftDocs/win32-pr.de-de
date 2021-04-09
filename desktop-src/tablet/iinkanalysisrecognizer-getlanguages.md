---
description: Ruft die Bezeichner für die Gebiets Schemas ab, die von diesem iinkanalysiserkenzer unterstützt werden.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: 'Iinkanalysiserkenzer:: GetLanguages-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer.GetLanguages
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 1e2b9792957b2de02daf45f8b662cfcb1174be72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862708"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a>Iinkanalysiserkenzer:: GetLanguages-Methode

Ruft die Bezeichner für die Gebiets Schemas ab, die von diesem [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pullanguagescount* \[ in, out\]
</dt> <dd>

Die Anzahl der Bezeichner in *ppullanguages*.

</dd> <dt>

*ppullanguages* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf die Bezeichner für die Gebiets Schemas, die von diesem [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) unterstützt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

> [!Caution]  
> Um einen Speicherplatz zu vermeiden, verwenden Sie " [**CoTaskMemFree**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) ", um den Arbeitsspeicher von \* *ppullanguages* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

Diese Methode gibt ein leeres Array für Objekt-und Gesten Erkennungs Tools zurück.

Weitere Informationen zu sprach Bezeichnern finden Sie unter [sprach Bezeichner-Konstanten und-](/windows/desktop/Intl/language-identifier-constants-and-strings)Zeichen folgen.

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
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

