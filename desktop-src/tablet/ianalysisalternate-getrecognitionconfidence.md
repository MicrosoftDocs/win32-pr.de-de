---
description: Ruft einen Wert ab, der die Vertrauens Ebene angibt, die der iinkanalyzer in der Genauigkeit von ianalysisalternate hat.
ms.assetid: ac1c68df-2e0c-4633-b7ee-519482a4d67a
title: 'Ianalysisalternate:: getrecognitionconfidence-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetRecognitionConfidence
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: eacaf7e5a8feaddcd437e68cf7acfa4fc5a7fc80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751881"
---
# <a name="ianalysisalternategetrecognitionconfidence-method"></a>Ianalysisalternate:: getrecognitionconfidence-Methode

Ruft einen Wert ab, der die Vertrauens Ebene angibt, die der [**iinkanalyzer**](iinkanalyzer.md) in der Genauigkeit von [**ianalysisalternate**](ianalysisalternate.md)hat.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetRecognitionConfidence(
  [out] RecognitionConfidence *pConfidence
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pconfidence* \[ vorgenommen\]
</dt> <dd>

Ein Zeiger auf eine [**InkRecognitionConfidence-Enumeration**](/windows/desktop/api/msinkaut/ne-msinkaut-inkrecognitionconfidence) , die die Vertrauens Ebene angibt, die von [**iinkanalysiserkenzer**](iinkanalysisrecognizer.md) in der Genauigkeit der Erkennungs Alternativen liegt.

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

[**Iinkanalyzer**](iinkanalyzer.md)
</dt> <dt>

[**Iinkanalysiserkenzer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**Erkentionconfidence**](recognitionconfidence.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




