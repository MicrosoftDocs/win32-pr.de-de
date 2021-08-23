---
description: Löscht einen Unterschlüssel und seine Werte aus einer Offlineregistrierungsstruktur.
ms.assetid: 651795d3-4328-4281-9a7f-ba75b4ec4da1
title: ORDeleteKey-Funktion (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORDeleteKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 9f3be934eca97d88f4dfeb1b1576d9fcd06f5681351a2e85d8ae7f6ba31e8860
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119571930"
---
# <a name="ordeletekey-function"></a>ORDeleteKey-Funktion

Löscht einen Unterschlüssel und seine Werte aus einer Offlineregistrierungsstruktur.

## <a name="syntax"></a>Syntax


```C++
DWORD ORDeleteKey(
  _In_     ORHKEY Handle,
  _In_opt_ PCWSTR lpSubKey
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur. Dieses Handle wird von der [**ORCreateKey-**](orcreatekey.md) oder [**OROpenKey-Funktion**](oropenkey.md) zurückgegeben.

</dd> <dt>

*lpSubKey* \[ in, optional\]
</dt> <dd>

Der Name des zu löschenden Schlüssels. Er muss ein Unterschlüssel des Schlüssels sein, der *von Handle* identifiziert wird, darf jedoch keine Unterschlüssel haben.

Wenn der Unterschlüssel nicht vorhanden ist, gibt die Funktion ERROR \_ NOT \_ FOUND zurück.

Wenn dieser Parameter **NULL ist,** löscht die Funktion den durch den *Handle-Parameter angegebenen* Schlüssel. Wenn der durch den *Handle-Parameter angegebene* Schlüssel der Stammschlüssel der Struktur ist, gibt die Funktion ERROR INVALID \_ PARAMETER \_ zurück.

Bei Schlüsselnamen wird die Schreibung nicht beachtet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ist, ist der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein fehlerfreier Code, der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem Flag FORMAT MESSAGE FROM SYSTEM verwenden, \_ um eine generische Beschreibung des \_ \_ Fehlers zu erhalten. Mögliche Fehlercodes:

-   Wenn der angegebene Unterschlüssel nicht vorhanden ist, gibt die Funktion ERROR \_ FILE \_ NOT FOUND \_ zurück.
-   Wenn der angegebene Unterschlüssel der Stammschlüssel der Registrierungsstruktur ist, gibt die Funktion ERROR \_ INVALID \_ PARAMETER zurück.
-   Wenn der angegebene Unterschlüssel Unterschlüssel hat, gibt die Funktion ERROR \_ KEY \_ HAS CHILDREN \_ zurück.

## <a name="remarks"></a>Hinweise

Wenn der angegebene Registrierungsschlüssel vorhanden ist, wird er als gelöscht markiert. Ein gelöschter Schlüssel wird erst entfernt, wenn das letzte Handle geschlossen wurde.

Der zu löschende Schlüssel darf keine Unterschlüssel haben. Um einen Schlüssel und alle seine Unterschlüssel zu löschen, verwenden Sie die [**OREnumKey-Funktion,**](orenumkey.md) um die Unterschlüssel zu aufzählen und einzeln zu löschen.

Nur die [**ORCloseKey-Funktion**](orclosekey.md) kann für einen gelöschten Schlüssel aufgerufen werden. Alle anderen Offlineregistrierungsvorgänge sind nicht möglich. Wenn der gelöschte Schlüssel explizit durch Aufrufen von [**ORCreateKey**](orcreatekey.md)erstellt wurde, werden ressourcen, die dem Schlüssel zugeordnet sind, freigegeben, wenn das letzte Handle für den gelöschten Schlüssel geschlossen wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offlineregistrierungsbibliothek, Version 1.0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**OREnumKey**](orenumkey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
