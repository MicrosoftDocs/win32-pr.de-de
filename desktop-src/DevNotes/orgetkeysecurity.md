---
description: Ruft eine Kopie der Sicherheits Beschreibung ab, die den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur schützt.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: Orgetkeysecurity-Funktion (offreg. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372644"
---
# <a name="orgetkeysecurity-function"></a>Orgetkeysecurity-Funktion

Ruft eine Kopie der Sicherheits Beschreibung ab, die den angegebenen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur schützt.

## <a name="syntax"></a>Syntax


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
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

Ein [Sicherheits \_ Informations](../secauthz/security-information.md) Wert, der die angeforderten Sicherheitsinformationen angibt.

</dd> <dt>

*psecuritydescriptor* \[ Out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine Kopie der angeforderten Sicherheits Beschreibung empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpcbsecuritydescriptor* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Puffers in Bytes angibt, auf den der *psecuritydescriptor* -Parameter verweist. Wenn die Funktion zurückgibt, enthält die Variable die Anzahl der in den Puffer geschriebenen Bytes.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, gibt die Funktion den Fehler \_ Erfolg zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlercode ungleich NULL zurückgegeben, der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

Wenn der durch den *psecuritydescriptor* -Parameter angegebene Puffer zu klein ist, gibt die Funktion Fehler \_ unzureichenden Puffer zurück, \_ und der *lpcbsecuritydescriptor* -Parameter enthält die Anzahl der Bytes, die für die angeforderte Sicherheits Beschreibung benötigt werden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Ordeletekey**](ordeletekey.md)
</dt> <dt>

[**Oropenkey**](oropenkey.md)
</dt> <dt>

[**Orsetkeysecurity**](orsetkeysecurity.md)
</dt> <dt>

[Sicherheits \_ Informationen](../secauthz/security-information.md)
</dt> </dl>

 

 
