---
description: Gibt die Anzahl der von diesem Enumerator gespeicherten Elemente zurück.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: IEnumWiaItem2::GetCount-Methode (Wia.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumWiaItem2.GetCount
api_type:
- COM
api_location:
- Wia.h
ms.openlocfilehash: 0a64a7c015f7c21ff19a736570aa104f0b229bc1b6561001b612045824f9a31d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119882420"
---
# <a name="ienumwiaitem2getcount-method"></a>IEnumWiaItem2::GetCount-Methode

Gibt die Anzahl der von diesem Enumerator gespeicherten Elemente zurück.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*cElt* \[ out\]
</dt> <dd>

Typ: **ULONG \***

Empfängt einen Zeiger auf ein **ULONG-Element,** das die Anzahl der Elemente in der -Enumeration empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>Wia.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Wia.idl</dt> </dl> |



 

 




