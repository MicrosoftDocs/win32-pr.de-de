---
description: Veraltet. Ruft den Schlüssel in der Registrierung ab, der dieser Benutzeridentität entspricht.
ms.assetid: eecf8b73-e86a-4274-8d9c-c601153f81db
title: 'Iuseridentity:: openidentityregkey-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.OpenIdentityRegKey
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f1d67918f4a9802e63682e0663994c1ea6a06200
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977896"
---
# <a name="iuseridentityopenidentityregkey-method"></a>Iuseridentity:: openidentityregkey-Methode

\[Die **iuseridentity:: openidentityregkey** -Methode ist für die Verwendung in Windows 2000 verfügbar. In Windows XP wurde diese Funktion durch [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md)abgelöst und kann in nachfolgenden Versionen geändert oder nicht verfügbar sein.\]

Veraltet. Ruft den Schlüssel in der Registrierung ab, der dieser Benutzeridentität entspricht.

## <a name="syntax"></a>Syntax


```C++
HRESULT OpenIdentityRegKey(
  [in]  DWORD dwDesiredAccess,
  [out] HKEY  *phKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*dwDesiredAccess* \[ in\]
</dt> <dd>

Typ: **DWORD**

Ein-Wert, der die angeforderte Zugriffsebene für den Registrierungsschlüssel beschreibt.

</dd> <dt>

*phkey* \[ vorgenommen\]
</dt> <dd>

Geben Sie Folgendes ein: **HKEY \** _

Ein Zeiger, der den Registrierungsschlüssel empfängt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Type: _ *HRESULT**

Das Ergebnis der Registrierungs Anforderung. Bei erfolgreicher Ausführung wird **S \_ OK** zurückgegeben. Andernfalls wird einer der folgenden Fehlercodes zurückgegeben.



| Rückgabecode                                                                                            | Beschreibung                                                        |
|--------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------|
| <dl> <dt>**E- \_ Identität \_ nicht \_ gefunden**</dt> </dl> | Diese Identität weist keinen zugeordneten Registrierungsschlüssel auf.<br/> |
| <dl> <dt>**E \_ fehlschlagen**</dt> </dl>                 | Der Zugriff auf den Registrierungsschlüssel war nicht möglich.<br/>             |



 

## <a name="remarks"></a>Bemerkungen

Der *dwDesiredAccess* -Parameter ist eine standardmäßige Registrierungs Zugriffs-Sicherheits Beschreibung, die den Zugriff beschreibt, den Sie für den Registrierungsschlüssel gewinnen möchten. Weitere Informationen zur Registrierungs Sicherheit, einschließlich einer Liste zulässiger Werte für diesen Parameter, finden Sie unter [Sicherheit und Zugriffsrechte für den Registrierungsschlüssel](../sysinfo/registry-key-security-and-access-rights.md).

## <a name="requirements"></a>Requirements (Anforderungen)



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 2000 Professional \[nur Desktop-Apps\]<br/>                             |
| Unterstützte Mindestversion (Server)<br/> | Windows 2000 Server \[nur Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Msident. h</dt> </dl>   |
| IDL<br/>                      | <dl> <dt>Msident. idl</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Msident.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**Iuseridentity**](iuseridentity.md)
</dt> <dt>

[**Iuseridentity:: getidentityfolder**](iuseridentity-getidentityfolder.md)
</dt> </dl>

 

 
