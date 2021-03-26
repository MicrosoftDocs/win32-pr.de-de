---
description: "\"GetCount\" wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop."
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: 'Ienumumuseridentity:: GetCount-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 43355a9585fc4099c8649f7df506ff3495a53944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345388"
---
# <a name="ienumuseridentitygetcount-method"></a>Ienumumuseridentity:: GetCount-Methode

\[" **GetCount** " wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Ruft die Anzahl der Benutzer Identitäten ab, die sich zurzeit im System befinden.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pnCount* \[ vorgenommen\]
</dt> <dd>

Typ: **ulong \** _

Zeiger auf ein _ *ulong**-Wert, der die Anzahl empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Wenn die Unterstützung für mehrere Benutzer Identitäten deaktiviert ist, erhält *pnCount* den Wert 1.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows XP<br/>                                                                  |
| Ende des Supports (Server)<br/>    | Windows Server 2003<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iumumuseridentity**](ienumuseridentity.md)
</dt> <dt>

[**Iendumuseridentity:: Skip**](ienumuseridentity-skip.md)
</dt> <dt>

[**Ienumumuseridentity:: Reset**](ienumuseridentity-reset.md)
</dt> <dt>

[**Ienumumuseridentity:: Next**](ienumuseridentity-next.md)
</dt> </dl>

 

 




