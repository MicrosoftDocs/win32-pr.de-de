---
description: Ruft einen Wert ab, der angibt, ob ianalysisregion einen unendlichen Bereich darstellt.
ms.assetid: b84ec9ec-42d0-4d03-b78b-433e55d04897
title: 'Ianalysisregion:: IsInfinite-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsInfinite
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4f7d284c043f38a681b969f72d751f9acaa954c4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214681"
---
# <a name="ianalysisregionisinfinite-method"></a>Ianalysisregion:: IsInfinite-Methode

Ruft einen Wert ab, der angibt, ob [**ianalysisregion**](ianalysisregion.md) einen unendlichen Bereich darstellt.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsInfinite(
  [out] VARIANT_BOOL *pfIsInfinite
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pfisinfinite* \[ vorgenommen\]
</dt> <dd>

**Variant \_ TRUE** , wenn der dargestellte Bereich unendlich ist. Andernfalls ist der Wert **\_ false**.

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

[**Ianalysisregion:: IsEmpty-Methode**](ianalysisregion-isempty.md)
</dt> <dt>

[**Ianalysisregion:: MakeEmpty-Methode**](ianalysisregion-makeempty.md)
</dt> <dt>

[**Ianalysisregion:: MakeInfinite-Methode**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




