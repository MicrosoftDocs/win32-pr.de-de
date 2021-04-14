---
description: Registriert die angegebene Datenbank.
ms.assetid: 65eceb1a-9ce1-4b97-98d7-731932797794
title: Sdbregisterdatabaseex-Funktion
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
ms.openlocfilehash: 74872f8895032abe02b024396fda12c43dc1611d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104523344"
---
# <a name="sdbregisterdatabaseex-function"></a>Sdbregisterdatabaseex-Funktion

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

*pszdatabasepath* \[ in\]
</dt> <dd>

Der Daten Bank Pfad. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*dwdatabasetype* \[ in\]
</dt> <dd>

Der Datenbanktyp. Eine Liste der Werte finden Sie unter [Shim-Datenbanktypen](shim-database-types.md) .

</dd> <dt>

*ptimestamp* \[ in, optional\]
</dt> <dd>

Der Zeitstempel für die Datenbank. Wenn dieser Parameter **null** ist, wird die Systemzeit verwendet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="remarks"></a>Bemerkungen

Eine Datenbank muss registriert werden, bevor Sie andere SDB-Funktionen verwenden können.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbunregisterdatabase**](sdbunregisterdatabase.md)
</dt> </dl>

 

 




