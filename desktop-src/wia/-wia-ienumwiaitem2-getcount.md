---
description: Gibt die Anzahl von Elementen zurück, die von diesem Enumerator gespeichert werden.
ms.assetid: d374ec81-0bd5-4b5d-8002-e3b53476421a
title: 'IEnumWiaItem2:: GetCount-Methode (WIA. h)'
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
ms.openlocfilehash: 23c067b8e4da93d678f641890a85e2535b3ca50d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041839"
---
# <a name="ienumwiaitem2getcount-method"></a>IEnumWiaItem2:: GetCount-Methode

Gibt die Anzahl von Elementen zurück, die von diesem Enumerator gespeichert werden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [out] ULONG *cElt
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*celt* \[ vorgenommen\]
</dt> <dd>

Typ: **ulong \** _

Empfängt einen Zeiger auf ein _ *ulong**-Element, das die Anzahl der Elemente in der-Enumeration empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                     |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                               |
| Header<br/>                   | <dl> <dt>WIA. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>WIA. idl</dt> </dl> |



 

 




