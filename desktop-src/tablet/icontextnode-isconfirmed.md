---
description: Ruft einen Wert ab, der angibt, ob der an diese Methode übergebene ConfirmationType für diesen IContextNode festgelegt wurde.
ms.assetid: 4a96bc46-b627-4784-ad1d-1079f49592e5
title: IContextNode::IsConfirmed-Methode (IACom.h)
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
ms.openlocfilehash: 2e378aaf344e177514115c82b1179f8d1ebe25faefa0d5d840d5a0af62ff1c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118967359"
---
# <a name="icontextnodeisconfirmed-method"></a>IContextNode::IsConfirmed-Methode

Ruft einen Wert ab, der angibt, ob der an diese Methode übergebene ConfirmationType für diesen IContextNode festgelegt wurde.

## <a name="syntax"></a>Syntax


```C++
HRESULT IsConfirmed(
  [in]  ConfirmationType confirmedType,
  [out] VARIANT_BOOL     *pfTypeConfirmed
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*confirmedType* \[ In\]
</dt> <dd>

Der Bestätigungstyp, auf den getestet wird.

</dd> <dt>

*pfTypeConfirmed* \[ out\]
</dt> <dd>

**VARIANT \_ TRUE,** wenn der in confirmedType übergebene Typ für dieses [**IContextNode-Objekt festgelegt**](icontextnode.md) wurde. andernfalls **VARIANT \_ FALSE**.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Eine Beschreibung der Rückgabewerte finden Sie unter [Klassen und Schnittstellen – Ink-Analyse](classes-and-interfaces---ink-analysis.md).

## <a name="remarks"></a>Hinweise

Dieser Wert wird von der [**IContextNode::Confirm-Methode**](icontextnode-confirm.md) festgelegt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur Desktop-Apps der XP Tablet PC Edition \[\]<br/>                                                 |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                                     |
| Header<br/>                   | <dl> <dt>IACom.h (erfordert auch IACom \_ i.c)</dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**IContextNode**](icontextnode.md)
</dt> <dt>

[**IContextNode::Confirm**](icontextnode-confirm.md)
</dt> <dt>

[Referenz zur Ink-Analyse](ink-analysis-reference.md)
</dt> </dl>

 

 




