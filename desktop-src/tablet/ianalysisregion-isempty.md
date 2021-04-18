---
description: Ruft einen Wert ab, der angibt, ob ianalysisregion einen leeren Bereich darstellt.
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'Ianalysisregion:: IsEmpty-Methode (iacom. h)'
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
ms.openlocfilehash: c1fb4ebbe487119c65f153f78e192de38e6393fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345740"
---
# <a name="ianalysisregionisempty-method"></a>Ianalysisregion:: IsEmpty-Methode

Ruft einen Wert ab, der angibt, ob [**ianalysisregion**](ianalysisregion.md) einen leeren Bereich darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfimpmpty* \[ vorgenommen\]
</dt> <dd>

**Variant \_ TRUE** , wenn der dargestellte Bereich leer ist. Andernfalls ist der Wert **\_ false**.

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

[**Ianalysisregion**](ianalysisregion.md)
</dt> <dt>

[**Ianalysisregion:: IsInfinite-Methode**](ianalysisregion-isinfinite.md)
</dt> <dt>

[**Ianalysisregion:: MakeEmpty-Methode**](ianalysisregion-makeempty.md)
</dt> <dt>

[**Ianalysisregion:: MakeInfinite-Methode**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




