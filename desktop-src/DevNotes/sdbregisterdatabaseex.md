---
description: Registriert die angegebene Datenbank.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: SdbRegisterDatabaseEx-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbRegisterDatabaseEx
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 512e180549c246a5504bc14675d61082c68904aa767d98deca5111d9a275dc60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119984100"
---
# <a name="sdbregisterdatabaseex-function"></a>SdbRegisterDatabaseEx-Funktion

Registriert die angegebene Datenbank.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbRegisterDatabaseEx(
  _In_     LPCTSTR    pszDatabasePath,
  _In_     DWORD      dwDatabaseType,
  _In_opt_ PULONGLONG pTimeStamp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pszDatabasePath* \[ In\]
</dt> <dd>

Der Datenbankpfad. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*dwDatabaseType* \[ In\]
</dt> <dd>

Der Datenbanktyp. Eine Liste der Werte finden Sie unter [Shim-Datenbanktypen.](shim-database-types.md)

</dd> <dt>

*pTimeStamp* \[ in, optional\]
</dt> <dd>

Der Zeitstempel für die Datenbank. Wenn dieser Parameter **NULL** ist, wird die Systemzeit verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt **TRUE** bei Erfolg oder **FALSE** bei Einem Fehler zurück.

## <a name="remarks"></a>Hinweise

Eine Datenbank muss registriert werden, bevor Sie andere SDB-Funktionen verwenden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbUnregisterDatabase**](sdbunregisterdatabase.md)
</dt> </dl>

 

 




