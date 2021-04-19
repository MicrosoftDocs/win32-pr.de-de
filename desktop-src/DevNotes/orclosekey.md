---
description: Schließt ein Handle für den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.
ms.assetid: 01bb21b1-217b-4716-ae1e-466cf8383155
title: Orclosekey-Funktion (offreg. h)
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
ms.openlocfilehash: df6b8d9176efc1eb1e4ffb4e0453ec665ec19b6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106372694"
---
# <a name="orclosekey-function"></a>Orclosekey-Funktion

Schließt ein Handle für den angegebenen Registrierungsschlüssel in einer Offline Registrierungs Struktur.

## <a name="syntax"></a>Syntax


```C++
DWORD ORCloseKey(
  _In_ ORHKEY Handle
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*Handle* \[ in\]
</dt> <dd>

Ein Handle für einen geöffneten Registrierungsschlüssel in einer Offline Registrierungs Struktur.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Funktion erfolgreich ausgeführt wird, ist der Rückgabewert Fehler \_ erfolgreich.

Wenn die Funktion fehlschlägt, ist der Rückgabewert ein Fehlercode ungleich 0 (null), der in WinError. h definiert ist. Sie können die [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) -Funktion mit dem \_ Flag Format Message \_ from System verwenden \_ , um eine generische Beschreibung des Fehlers zu erhalten.

Wenn der angegebene Schlüssel der Stamm Schlüssel der Registrierungs Struktur ist, schlägt die Funktion mit einem \_ ungültigen \_ Parameter fehl.

## <a name="remarks"></a>Bemerkungen

Das Handle für einen angegebenen Schlüssel sollte nicht verwendet werden, nachdem es geschlossen wurde, da es nicht mehr gültig ist. Schlüssel Handles sollten nicht länger als erforderlich geöffnet bleiben.

Verwenden Sie die [**orclosehive**](orclosehive.md) -Funktion, um eine Offline Registrierungs Struktur zu schließen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------------------|---------------------------------------------------------------------------------------|
| Verteilbare Komponente<br/> | Windows-offline Registrierungs Bibliothek, Version 1,0 oder höher<br/>                      |
| Header<br/>          | <dl> <dt>Offreg. h</dt> </dl>   |
| DLL<br/>             | <dl> <dt>Offreg.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Orclosehive**](orclosehive.md)
</dt> <dt>

[**Orkreatekey**](orcreatekey.md)
</dt> <dt>

[**Ordeletekey**](ordeletekey.md)
</dt> <dt>

[**Oropenkey**](oropenkey.md)
</dt> </dl>

 

 
