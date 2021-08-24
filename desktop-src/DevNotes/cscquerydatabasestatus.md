---
description: Ruft den Status des Offlinedateien Caches ab.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: CSCQueryDatabaseStatus-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSCQueryDatabaseStatus
api_type:
- DllExport
api_location:
- Cscmig.dll
ms.openlocfilehash: 312a1cfadcc38b4f76cd0dd488de07377e6fd68b9875a1ed6d39ed674b581b35
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119331830"
---
# <a name="cscquerydatabasestatus-function"></a>CSCQueryDatabaseStatus-Funktion

\[Diese Funktion wird nicht unterstützt und sollte nicht verwendet werden.\]

Ruft den Status des Offlinedateien Caches ab.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI CSCQueryDatabaseStatus(
   ULONG *pulStatus,
   ULONG *pulErrors
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pulStatus* 
</dt> <dd>

Der Status. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <dt>**FLAG \_ DATABASESTATUS \_ ENCRYPTED**</dt> <dt>0x00000002</dt> </dl>                                      | Der Cache ist für die Verschlüsselung markiert, und alle Dateien im Cache werden verschlüsselt.<br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <dt>**FLAG \_ DATABASESTATUS \_ PARTIALLY \_ ENCRYPTED**</dt> <dt>0x00000004</dt> </dl>       | Der Cache ist für die Verschlüsselung markiert, einige Dateien im Cache sind jedoch nicht verschlüsselt.<br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <dt>**FLAG \_ DATABASESTATUS \_ TEILWEISE \_ UNVERSCHLÜSSELTE**</dt> <dt>0x00000004</dt> </dl> | Der Cache ist nicht für die Verschlüsselung markiert, aber nicht alle Dateien im Cache wurden entschlüsselt.<br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <dt>**FLAG \_ \_DATABASESTATUS UNENCRYPTED**</dt> <dt>0x00000000</dt> </dl>                                | Der Cache ist nicht für die Verschlüsselung markiert, und alle Dateien im Cache wurden entschlüsselt.<br/>      |



 

</dd> <dt>

*pulErrors* 
</dt> <dd>

Dieser Parameter ist ein Wert ungleich 0 (null), wenn ein interner Datenbankfehler vorliegt, andernfalls 0 .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE** zurück, wenn sie erfolgreich ist. Andernfalls wird **FALSE** zurückgegeben.

## <a name="remarks"></a>Hinweise

Dieser Funktion ist keine Importbibliothek oder Headerdatei zugeordnet. Sie müssen sie mithilfe der [**Funktionen LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) und [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**CSCIsCSCEnabled**](csciscscenabled.md)
</dt> </dl>

 

 
