---
description: Getidentityfolder wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: 'Iuseridentity:: getidentityfolder-Methode (Msident. h)'
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
ms.openlocfilehash: 9f2644570bb7ccc2ae5bee8a37d4471ffb65861a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977904"
---
# <a name="iuseridentitygetidentityfolder-method"></a>Iuseridentity:: getidentityfolder-Methode

\[**Getidentityfolder** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein. Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]

Ruft den Datei Ordner ab, der dieser Identität zugeordnet ist.

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

*dwFlags* \[ in\]
</dt> <dd>

Typ: **DWORD**

Erforderlich. Ein-Wert, der angibt, ob der dieser Identität zugeordnete Ordner roamingbasiert. Muss einen der folgenden Werte aufweisen.

<dt>



 (GIF \_ \_roamingordner)


</dt> <dd>

Der Ordner ist Roaming.

</dd> <dt>



 (GIF \_ nicht \_ \_ roamingordner)


</dt> <dd>

Der Ordner ist "local".

</dd> </dl> </dd> <dt>

*pszpath* \[ in\]
</dt> <dd>

Typ: **WCHAR \** _

Ein Zeiger auf eine breit Zeichen-Zeichenfolge, die den Ordner Pfad empfängt.

</dd> <dt>

_ulBuffSize * \[ in\]
</dt> <dd>

Typ: **ulong**

Ein-Wert, der die Größe von *pszpath* angibt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Typ: **HRESULT**

Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück. Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.

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



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iuseridentity**](iuseridentity.md)
</dt> <dt>

[**Iuseridentity:: openidentityregkey**](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




