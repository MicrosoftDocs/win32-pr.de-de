---
description: GetIdentityFolder wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: IUserIdentity::GetIdentityFolder-Methode (Msident.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 20357dde27214177a454eb585dcd51182228c247da5aeae5ef887089b73ed85d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720606"
---
# <a name="iuseridentitygetidentityfolder-method"></a>IUserIdentity::GetIdentityFolder-Methode

\[**GetIdentityFolder** wird nicht unterstützt und kann in Zukunft geändert oder nicht mehr verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schnellem Benutzerwechsel und Remotedesktop](fastuserswitching.md).\]

Ruft den Dateiordner ab, der dieser Identität zugeordnet ist.

## <a name="syntax"></a>Syntax


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwFlags* \[ In\]
</dt> <dd>

Typ: **DWORD**

Erforderlich. Ein -Wert, der angibt, ob der dieser Identität zugeordnete Ordner roamingt. Dabei muss es sich um einen der folgenden Werte handeln.

<dt>



 (GIF) \_ \_ROAMINGORDNER)


</dt> <dd>

Der Ordner befindet sich im Roaming.

</dd> <dt>



 (GIF) \_ NICHT \_ \_ ROAMINGORDNER)


</dt> <dd>

Der Ordner ist lokal.

</dd> </dl> </dd> <dt>

*pszPath* \[ In\]
</dt> <dd>

Typ: **WCHAR \***

Ein Zeiger auf eine Breitzeichenzeichenfolge, die den Ordnerpfad empfängt.

</dd> <dt>

*ulBuffSize* \[ In\]
</dt> <dd>

Typ: **ULONG**

Ein -Wert, der die Größe von *pszPath angibt.*

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

[**IUserIdentity::OpenIdentityRegKey**](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




