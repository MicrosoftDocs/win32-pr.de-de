---
description: Ruft den erkannten Zeichenfolgenwert des IAnalysisAlternate-Objekts ab.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: IAnalysisAlternate::GetRecognizedString-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognizedString
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 79d0967d2653a68145a9a50c34134d176d78674c5ea5729230035edd65a5e6b3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008490"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a>IAnalysisAlternate::GetRecognizedString-Methode

Ruft den erkannten [**Zeichenfolgenwert des IAnalysisAlternate-Objekts**](ianalysisalternate.md) ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstrRecognizedString* \[ out\]
</dt> <dd>

Ein Zeiger auf den **BSTR,** der auf den erkannten Zeichenfolgenwert festgelegt ist.

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer::GetRecognizedString-Methode**](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




