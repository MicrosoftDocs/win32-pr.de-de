---
description: ChangePassword wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: bc8813a0-9b40-481f-9ab3-cf6a9a0796d2
title: 'IUserIdentity2:: ChangePassword-Methode (Msident. h)'
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
ms.openlocfilehash: dd4b858924e4b042b3d7a0636d90eb582e9506df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977889"
---
# <a name="iuseridentity2changepassword-method"></a>IUserIdentity2:: ChangePassword-Methode

\[**ChangePassword** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

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

*szoldpass* \[ in\]
</dt> <dd>

Typ: **WCHAR \** _

Die Zeichenfolge mit breit Zeichen, die das Kennwort enthält, das derzeit der Identität zugeordnet ist.

</dd> <dt>

_szNewPass * \[ in\]
</dt> <dd>

Typ: **WCHAR \** _

Die Zeichenfolge mit breit Zeichen, die das neue Kennwort enthält, das der Identität zugeordnet werden soll.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Der Wert von *szoldpass* muss mit dem aktuellen Kennwort der Identität für den anzuwendenden *sznewpass* -Wert identisch sein. Ein falscher Wert von *szoldpass* führt zu einem Rückgabewert von E \_ Fail.

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Ende des Supports (Client)<br/>    | Windows 2000 Professional<br/>                                                   |
| Ende des Supports (Server)<br/>    | Windows 2000 Server<br/>                                                         |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



 

 




