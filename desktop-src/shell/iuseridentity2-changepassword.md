---
description: ChangePassword wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: IUserIdentity2::ChangePassword-Methode (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.ChangePassword
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d892fd3f676183864d72d905b72cea2f01643211314fc293b1cd76e5d70fc237
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092697"
---
# <a name="iuseridentity2changepassword-method"></a>IUserIdentity2::ChangePassword-Methode

\[**ChangePassword** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Legt ein neues Kennwort für die Identität fest.

## <a name="syntax"></a>Syntax


```C++
HRESULT ChangePassword(
  [in] WCHAR *szOldPass,
  [in] WCHAR *szNewPass
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*szOldPass* \[ In\]
</dt> <dd>

Typ: **WCHAR \***

Die Breitzeichenzeichenfolge, die das kennwort enthält, das der Identität derzeit zugeordnet ist.

</dd> <dt>

*szNewPass* \[ In\]
</dt> <dd>

Typ: **WCHAR \***

Die Breitzeichenzeichenfolge, die das neue Kennwort enthält, das der Identität zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK** zurückgegeben. Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

## <a name="remarks"></a>Hinweise

Der Wert von *szOldPass* muss mit dem aktuellen Kennwort der Identität übereinstimmen, damit *szNewPass* angewendet werden kann. Ein falscher Wert von *szOldPass* führt zu einem Rückgabewert von E \_ FAIL.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident.h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Msident.idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



 

 




