---
description: Erstellt eine neue Shimdatenbank.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: SdbCreateDatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbCreateDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 6c7ac5d30c9c5a0154d770266410d278c5c3f31a65166515078a5384b1b8b55d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118161556"
---
# <a name="sdbcreatedatabase-function"></a>SdbCreateDatabase-Funktion

Erstellt eine neue Shimdatenbank.

## <a name="syntax"></a>Syntax


```C++
PDB WINAPI SdbCreateDatabase(
  _In_ LPCWSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszPath* \[ In\]
</dt> <dd>

Der Pfad, in dem die Datenbank gespeichert werden soll. Dieser Parameter darf nicht **NULL** sein.

</dd> <dt>

*eType* \[ In\]
</dt> <dd>

Der Pfadtyp. Eine Liste der Werte finden Sie unter [**PATH \_ TYPE.**](path-type.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt bei einem Fehler ein Handle für die Shimdatenbank oder **NULL** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**SdbOpenDatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




