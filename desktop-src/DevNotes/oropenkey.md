---
description: Öffnet den angegebenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur.
ms.assetid: 4a4afbef-5107-4006-bd67-aecb5d3b5112
title: OROpenKey-Funktion (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OROpenKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 4c0f641925fbc35fba6072ee395f67fad540dcd2ec5198b945ad658a723238b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118667095"
---
# <a name="oropenkey-function"></a>OROpenKey-Funktion

Öffnet den angegebenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

## <a name="syntax"></a>Syntax


```C++
DWORD OROpenKey(
  _In_     ORHKEY  Handle,
  _In_opt_ PCWSTR  lpSubKeyName,
  _Out_    PORHKEY phkResult
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

</dd> <dt>

*lpSubKeyName* \[ in, optional\]
</dt> <dd>

Ein Zeiger auf eine UNICODE-Zeichenfolge, die den Namen des zu öffnenden Registrierungsschlüssels enthält. Dieser Schlüssel muss ein Unterschlüssel des Schlüssels sein, der durch den *Handle-Parameter* identifiziert wird.

Bei Schlüsselnamen wird die Groß-/Kleinschreibung nicht beachtet.

Wenn dieser Parameter **NULL** oder ein Zeiger auf eine leere Zeichenfolge ist, gibt die Funktion das gleiche Handle zurück, das übergeben wurde. Wenn der vom *Handle-Parameter* angegebene Schlüssel der Stammschlüssel der Struktur ist, gibt die Funktion ERROR \_ INVALID PARAMETER \_ zurück.

Weitere Informationen finden Sie unter [Größenbeschränkungen für Registrierungselemente.](../sysinfo/registry-element-size-limits.md)

</dd> <dt>

*phkResult* \[ out\]
</dt> <dd>

Ein Zeiger auf eine Variable, die ein Handle für den geöffneten Schlüssel empfängt. Verwenden Sie die [**ORCloseKey-Funktion,**](orclosekey.md) um den Schlüssel zu schließen, nachdem Sie das Handle verwendet haben.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem \_ FORMAT MESSAGE FROM \_ \_ SYSTEM-Flag verwenden, um eine generische Beschreibung des Fehlers abzurufen.

Wenn das zurückzugebende Handle ein Handle für den Stammschlüssel der Struktur wäre, gibt die Funktion ERROR \_ INVALID \_ PARAMETER zurück.

Wenn der angegebene Schlüssel als gelöscht markiert wurde, gibt diese Funktion ERROR \_ KEY \_ DELETED zurück.

## <a name="remarks"></a>Hinweise

Die **OROpenKey-Funktion** kann nicht verwendet werden, um den Stammschlüssel in einer Offlineregistrierungsstruktur zu öffnen. Um ein Handle für den Stammschlüssel einer Struktur abzurufen, verwenden Sie die [**OROpenHive-Funktion,**](oropenhive.md) um die Struktur in den Arbeitsspeicher zu laden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offline registry library version 1.0 or later (Offlineregistrierungsbibliothek, Version 1.0 oder höher)<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**ORCloseKey**](orclosekey.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenHive**](oropenhive.md)
</dt> </dl>

 

 
