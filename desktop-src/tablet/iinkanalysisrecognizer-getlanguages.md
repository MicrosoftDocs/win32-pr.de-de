---
description: Ruft die Bezeichner für die Gebietsschemas ab, die von IInkAnalysisRecognizer unterstützt werden.
ms.assetid: 14c91ad0-f49e-43e7-848c-abc96b0dffa8
title: IInkAnalysisRecognizer::GetLanguages-Methode (IACom.h)
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
ms.openlocfilehash: 8a94b85dfe9a6b5dbbd755ff1e0a4cf2d68dccd5178da6d0578d6f50e8b48936
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350970"
---
# <a name="iinkanalysisrecognizergetlanguages-method"></a>IInkAnalysisRecognizer::GetLanguages-Methode

Ruft die Bezeichner für die Gebietsschemas ab, die von [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) unterstützt werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetLanguages(
  [in, out] ULONG *pulLanguagesCount,
  [out]     ULONG **ppulLanguages
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulLanguagesCount* \[ in, out\]
</dt> <dd>

Die Anzahl der Bezeichner in *ppulLanguages*.

</dd> <dt>

*ppulLanguages* \[ out\]
</dt> <dd>

Ein Zeiger auf die Bezeichner für die Gebietsschemas, die von [**diesem IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) unterstützt werden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter Klassen und Schnittstellen – [Ink-Analyse.](classes-and-interfaces---ink-analysis.md)

## <a name="remarks"></a>Hinweise

> [!Caution]  
> Um einen Speicherverlust zu vermeiden, verwenden Sie [**CoTaskMemFree,**](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) um den Arbeitsspeicher von \* *ppulLanguages* freizugeben, wenn Sie die Informationen nicht mehr benötigen.

 

Diese Methode gibt ein leeres Array für die Objekt- und Gestenerkennung zurück.

Weitere Informationen zu Sprachbezeichnern finden Sie unter [Sprachbezeichnerkonstanten und Zeichenfolgen.](/windows/desktop/Intl/language-identifier-constants-and-strings)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

