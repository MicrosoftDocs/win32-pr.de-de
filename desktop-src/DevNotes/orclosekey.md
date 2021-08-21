---
description: Schließt ein Handle für den angegebenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur.
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: ORCloseKey-Funktion (Offreg.h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORCloseKey
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 28f93c2bb1de61da072d7fde6d811463106be0c56f049b3ebf7e74f79ef740fc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119572110"
---
# <a name="orclosekey-function"></a>ORCloseKey-Funktion

Schließt ein Handle für den angegebenen Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

## <a name="syntax"></a>Syntax


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ In\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offlineregistrierungsstruktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, lautet der Rückgabewert ERROR \_ SUCCESS.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in Winerror.h definiert ist. Sie können die [FormatMessage-Funktion](/windows/win32/api/winbase/nf-winbase-formatmessage) mit dem \_ FORMAT MESSAGE FROM \_ \_ SYSTEM-Flag verwenden, um eine generische Beschreibung des Fehlers abzurufen.

Wenn der angegebene Schlüssel der Stammschlüssel der Registrierungsstruktur ist, schlägt die Funktion mit ERROR \_ INVALID \_ PARAMETER fehl.

## <a name="remarks"></a>Hinweise

Das Handle für einen angegebenen Schlüssel sollte nach dem Schließen nicht mehr verwendet werden, da es nicht mehr gültig ist. Schlüsselhandles sollten nicht länger als nötig geöffnet bleiben.

Verwenden Sie die [**ORCloseHive-Funktion,**](orclosehive.md) um eine Offlineregistrierungsstruktur zu schließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows Offline registry library version 1.0 or later (Offlineregistrierungsbibliothek, Version 1.0 oder höher)<br/>                      |
| Header<br/>          | <dl> <dt>Offreg.h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**ORCloseHive**](orclosehive.md)
</dt> <dt>

[**ORCreateKey**](orcreatekey.md)
</dt> <dt>

[**ORDeleteKey**](ordeletekey.md)
</dt> <dt>

[**OROpenKey**](oropenkey.md)
</dt> </dl>

 

 
