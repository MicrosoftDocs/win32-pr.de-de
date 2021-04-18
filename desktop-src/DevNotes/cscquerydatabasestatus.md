---
description: Ruft den Status des Offlinedateien Caches ab.
ms.assetid: a8cc0dbb-0005-4e74-892e-898e2ebe0465
title: Cscquerydatabasestatus-Funktion
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
ms.openlocfilehash: badd869306290609ccadeba80e6ea67ca3479be8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106365601"
---
# <a name="cscquerydatabasestatus-function"></a>Cscquerydatabasestatus-Funktion

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

*pulstatus* 
</dt> <dd>

Der Status. Dieser Parameter kann einen der folgenden Werte annehmen.



| Wert                                                                                                                                                                                                                                                                                                               | Bedeutung                                                                                                |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <span id="FLAG_DATABASESTATUS_ENCRYPTED"></span><span id="flag_databasestatus_encrypted"></span><dl> <dt>**Flag \_ Databasestatus \_ verschlüsselt**</dt> <dt>0x00000002</dt> </dl>                                      | Der Cache ist für die Verschlüsselung markiert, und alle Dateien im Cache werden verschlüsselt.<br/>                |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_ENCRYPTED"></span><span id="flag_databasestatus_partially_encrypted"></span><dl> <dt>**Flag \_ Databasestatus \_ teilweise \_ verschlüsselt**</dt> <dt>0x00000004</dt> </dl>       | Der Cache ist für die Verschlüsselung gekennzeichnet, einige Dateien im Cache werden jedoch nicht verschlüsselt.<br/>          |
| <span id="FLAG_DATABASESTATUS_PARTIALLY_UNENCRYPTED"></span><span id="flag_databasestatus_partially_unencrypted"></span><dl> <dt>**Flag \_ Databasestatus \_ teilweise \_ unverschlüsselt**</dt> <dt>0x00000004</dt> </dl> | Der Cache ist nicht für die Verschlüsselung gekennzeichnet, aber nicht alle Dateien im Cache wurden entschlüsselt.<br/> |
| <span id="FLAG_DATABASESTATUS_UNENCRYPTED"></span><span id="flag_databasestatus_unencrypted"></span><dl> <dt>**Flag \_ Databasestatus \_ unverschlüsselt**</dt> <dt>0x00000000</dt> </dl>                                | Der Cache ist nicht für die Verschlüsselung markiert, und alle Dateien im Cache wurden entschlüsselt.<br/>      |



 

</dd> <dt>

*pulerrors* 
</dt> <dd>

Dieser Parameter ist ein Wert ungleich 0 (null), wenn ein interner Datenbankfehler vorliegt oder andernfalls 0.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich ist. Andernfalls wird **false** zurückgegeben.

## <a name="remarks"></a>Bemerkungen

Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|----------------|---------------------------------------------------------------------------------------|
| DLL<br/> | <dl> <dt>Cscmig.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Csciscscenabled**](csciscscenabled.md)
</dt> </dl>

 

 
