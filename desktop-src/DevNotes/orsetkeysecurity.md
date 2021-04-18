---
description: Legt die Sicherheit eines geöffneten Registrierungsschlüssels in einer Offline Registrierungs Struktur fest.
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: Orsetkeysecurity-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365179"
---
# <a name="orsetkeysecurity-function"></a>Orsetkeysecurity-Funktion

Legt die Sicherheit eines geöffneten Registrierungsschlüssels in einer Offline Registrierungs Struktur fest.

## <a name="syntax"></a>Syntax


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.

</dd> <dt>

*Securityinformation* \[ in\]
</dt> <dd>

Bitflags, die den Typ der festzulegenden Sicherheitsinformationen angeben. Dieser Parameter kann eine Kombination der [ \_ Sicherheitsinformations](../secauthz/security-information.md) -Bitflags sein.

</dd> <dt>

*psecuritydescriptor* \[ in\]
</dt> <dd>

Ein Zeiger auf eine [Sicherheits \_ deskriptorstruktur](/windows/win32/api/winnt/ns-winnt-security_descriptor) , die die Sicherheits Attribute angibt, die für den angegebenen Schlüssel festgelegt werden sollen.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion den Fehler \_ Erfolg zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlercode ungleich NULL zurückgegeben, der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Orclosekey**](orclosekey.md)
</dt> <dt>

[**Ordeletekey**](ordeletekey.md)
</dt> <dt>

[**Oropenkey**](oropenkey.md)
</dt> <dt>

[**Orgetkeysecurity**](orgetkeysecurity.md)
</dt> <dt>

[Sicherheits \_ Beschreibung](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[Sicherheits \_ Informationen](../secauthz/security-information.md)
</dt> </dl>

 

 
