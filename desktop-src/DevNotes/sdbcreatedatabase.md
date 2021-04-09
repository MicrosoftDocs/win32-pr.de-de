---
description: Erstellt eine neue Shimdatenbank.
ms.assetid: 91fb180d-1a21-4011-821d-ea0fc999dc76
title: Sdbkreatedatabase-Funktion
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
ms.openlocfilehash: 1ab8b8071cc210f6129545985d2d2e089680f0f2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958364"
---
# <a name="sdbcreatedatabase-function"></a>Sdbkreatedatabase-Funktion

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

*pwszpath* \[ in\]
</dt> <dd>

Der Pfad, in dem die Datenbank gespeichert werden soll. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*ETYPE* \[ in\]
</dt> <dd>

Der Pfadtyp. Eine Liste der Werte finden Sie unter [**path \_ Type**](path-type.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt ein Handle für die Shimdatenbank oder **null** bei einem Fehler zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                         |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbopendatabase**](sdbopendatabase.md)
</dt> </dl>

 

 




