---
description: GetCookie wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop.
ms.assetid: 4a743d64-9af3-43cf-9a9f-d808676ab337
title: IUserIdentity::GetCookie-Methode (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: e8b4abb13735b2ce370623ad8e5b79a8d9830b34a3d566fb57c0539d6f2c6095
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118220117"
---
# <a name="iuseridentitygetcookie-method"></a>IUserIdentity::GetCookie-Methode

\[**GetCookie** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Ruft das Cookie ab, das zum eindeutigen Identifizieren dieser Benutzeridentität verwendet wird.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetCookie(
  [out] GUID *puidCookie
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*puidCookie* \[ out\]
</dt> <dd>

Typ: **GUID \***

Ein Zeiger auf einen **GUID-Wert,** der das Cookie empfängt, das zum eindeutigen Identifizieren dieser Benutzeridentität verwendet wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ist, wird **S \_ OK zurückgegeben.** Andernfalls wird ein **HRESULT-Fehlercode** zurückgegeben.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**IUserIdentity**](iuseridentity.md)
</dt> <dt>

[**GetOrdinal**](iuseridentity2-getordinal.md)
</dt> </dl>

 

 




