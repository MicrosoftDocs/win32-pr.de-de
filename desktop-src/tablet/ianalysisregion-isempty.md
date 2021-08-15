---
description: Ruft einen Wert ab, der angibt, ob IAnalysisRegion einen leeren Bereich darstellt.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: IAnalysisRegion::IsEmpty-Methode (IACom.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a599d88371a1a6726ed2ec4ee217c36b3ea3cd71d6117305a59860cb9a8bf09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092321"
---
# <a name="ianalysisregionisempty-method"></a>IAnalysisRegion::IsEmpty-Methode

Ruft einen Wert ab, der angibt, ob [**IAnalysisRegion**](ianalysisregion.md) einen leeren Bereich darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfIsEmpty* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn der dargestellte Bereich leer ist; Andernfalls **VARIANT \_ FALSE**.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion::IsInfinite-Methode**](ianalysisregion-isinfinite.md)
</dt> <dt>

[**IAnalysisRegion::MakeEmpty-Methode**](ianalysisregion-makeempty.md)
</dt> <dt>

[**IAnalysisRegion::MakeInfinite-Methode**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




