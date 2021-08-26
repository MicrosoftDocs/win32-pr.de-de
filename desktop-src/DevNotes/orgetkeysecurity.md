---
description: Ruft eine Kopie der Sicherheitsbeschreibung ab, die den angegebenen offenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur schützt.
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: ORGetKeySecurity-Funktion (Offreg.h)
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
ms.openlocfilehash: 786321db22c513e7698fcd1661d173ccb5fdf76f1b09d9dd3e739ddf3fb2ca47
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984160"
---
# <a name="orgetkeysecurity-function"></a>ORGetKeySecurity-Funktion

Ruft eine Kopie der Sicherheitsbeschreibung ab, die den angegebenen offenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur schützt.

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

*Handle* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

</dd> <dt>

*SecurityInformation* \[ In\]
</dt> <dd>

Ein [SECURITY \_ INFORMATION-Wert,](../secauthz/security-information.md) der die angeforderten Sicherheitsinformationen angibt.

</dd> <dt>

*pSecurityDescriptor* \[ out, optional\]
</dt> <dd>

Ein Zeiger auf einen Puffer, der eine Kopie des angeforderten Sicherheitsdeskriptors empfängt. Dieser Parameter kann **NULL** sein.

</dd> <dt>

*lpcbSecurityDescriptor* \[ in, out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die die Größe des Puffers in Bytes angibt, auf den der *pSecurityDescriptor-Parameter* zeigt. Wenn die Funktion zurückgegeben wird, enthält die Variable die Anzahl der bytes, die in den Puffer geschrieben wurden.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, gibt die Funktion ERROR \_ SUCCESS zurück.

Wenn die Funktion fehlschlägt, wird ein Fehlercode ungleich 0 (null) zurückgegeben, der in "Winerror.h" definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem \_ FORMAT MESSAGE FROM \_ \_ SYSTEM-Flag verwenden, um eine generische Beschreibung des Fehlers abzurufen.

Wenn der vom *pSecurityDescriptor-Parameter* angegebene Puffer zu klein ist, gibt die Funktion ERROR INSUFFICIENT BUFFER zurück, \_ \_ und der *lpcbSecurityDescriptor-Parameter* enthält die Anzahl der Bytes, die für den angeforderten Sicherheitsdeskriptor erforderlich sind.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offline registry library version 1.0 or later (Offlineregistrierungsbibliothek, Version 1.0 oder höher)<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> <dt>

[**ORSetKeySecurity**](orsetkeysecurity.md)
</dt> <dt>

[\_SICHERHEITSINFORMATIONEN](../secauthz/security-information.md)
</dt> </dl>

 

 
