---
description: Öffnet die angegebene Shim-Datenbank.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: SdbOpenDatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: df0081d7373bf67d3df1723be7d5beb272ef7ee4c77c54da8a6985dfe250d7c2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161193"
---
# <a name="sdbopendatabase-function"></a>SdbOpenDatabase-Funktion

Öffnet die angegebene Shim-Datenbank.

## <a name="syntax"></a>Syntax


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszPath* \[ In\]
</dt> <dd>

Der Datenbankpfad. Dieser Parameter darf nicht **NULL sein.**

</dd> <dt>

*eType* \[ In\]
</dt> <dd>

Der Pfadtyp. Eine Liste der Werte finden Sie unter [**PATH \_ TYPE.**](path-type.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt ein Handle an die Shimdatenbank zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbCreateDatabase**](sdbcreatedatabase.md)
</dt> </dl>

 

 




