---
description: Ruft einen Wert ab, der angibt, ob der an diese Methode weiter gegebene ConfirmationType für diesen icontextnode festgelegt wurde.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: 'Icontextnode:: isconfirmed-Methode (iacom. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.IsConfirmed
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 300e0126b4a1ff55d372ff31deebde0eab686645
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526519"
---
# <a name="icontextnodeisconfirmed-method"></a>Icontextnode:: isconfirmed-Methode

Ruft einen Wert ab, der angibt, ob der an diese Methode weiter gegebene ConfirmationType für diesen icontextnode festgelegt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*confirmedtype* \[ in\]
</dt> <dd>

Der zu testende bestätentyp.

</dd> <dt>

*pftypebestätigt* \[ vorgenommen\]
</dt> <dd>

**Variant \_ TRUE** , wenn der in confirmedtype weiter gegebene Typ für dieses [**icontextnode**](icontextnode.md) -Objekt festgelegt wurde. Andernfalls ist der Wert **\_ false**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen-Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Bemerkungen

Dieser Wert wird durch die [**icontextnode:: Confirm**](icontextnode-confirm.md) -Methode festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>Iacom. h (erfordert auch iacom \_ i. c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Icontextnode**](icontextnode.md)
</dt> <dt>

[**Icontextnode:: Confirm**](icontextnode-confirm.md)
</dt> <dt>

[Ink-Analyse Referenz](ink-analysis-reference.md)
</dt> </dl>

 

 




