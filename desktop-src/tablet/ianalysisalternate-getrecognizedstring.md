---
description: Ruft den erkannten Zeichen folgen Wert des ianalysisalternate-Objekts ab.
ms.assetid: cdf41824-77a4-4c71-8712-f380a6cbf4c5
title: 'Ianalysisalternate:: GetRecognizedString-Methode (iacom. h)'
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
ms.openlocfilehash: 5489773b29ade35d4b7297065c1104bfecefa117
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526570"
---
# <a name="ianalysisalternategetrecognizedstring-method"></a>Ianalysisalternate:: GetRecognizedString-Methode

Ruft den erkannten Zeichen folgen Wert des [**ianalysisalternate**](ianalysisalternate.md) -Objekts ab.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRecognizedString(
  [out] BSTR *pbstrRecognizedString
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pbstrauerkenzedstring* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf den **BSTR** -Wert, der auf den erkannten Zeichen folgen Wert festgelegt ist.

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

[**Ianalysisalternate**](ianalysisalternate.md)
</dt> <dt>

[**Iinkanalyzer:: GetRecognizedString-Methode**](iinkanalyzer-getrecognizedstring.md)
</dt> </dl>

 

 




