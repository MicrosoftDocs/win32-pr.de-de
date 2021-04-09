---
description: Bestimmt, ob der angegebene ianalysisregion denselben Wert wie das aktuelle ianalysisregion-Objekt enthält.
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'Ianalysisregion:: equalsregion-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129524"
---
# <a name="ianalysisregionequalsregion-method"></a>Ianalysisregion:: equalsregion-Methode

Bestimmt, ob der angegebene [**ianalysisregion**](ianalysisregion.md) denselben Wert wie das aktuelle **ianalysisregion** -Objekt enthält.

## <a name="syntax"></a>Syntax


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*potherregion* \[ in\]
</dt> <dd>

Das [**ianalysisregion**](ianalysisregion.md) -Objekt, das mit dem aktuellen **ianalysisregion** verglichen werden soll.

</dd> <dt>

*pfregionsequal* \[ vorgenommen\]
</dt> <dd>

**Variant \_ TRUE** , wenn der angegebene [**ianalysisregion**](ianalysisregion.md) denselben Wert wie der aktuelle ianalysisregion enthält. Andernfalls ist der Wert **\_ false**.

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
</dt> </dl>

 

 




