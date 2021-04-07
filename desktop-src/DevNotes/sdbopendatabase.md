---
description: Öffnet die angegebene Shimdatenbank.
ms.assetid: 148181d7-a20a-467c-984b-e32013960783
title: Sdbopendatabase-Funktion
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
ms.openlocfilehash: ae0bca035f203593c43bb36e70119fbaf3024059
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103747856"
---
# <a name="sdbopendatabase-function"></a>Sdbopendatabase-Funktion

Öffnet die angegebene Shimdatenbank.

## <a name="syntax"></a>Syntax


```C++
PDB WINAPI SdbOpenDatabase(
  _In_ LPCTSTR   pwszPath,
  _In_ PATH_TYPE eType
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwszpath* \[ in\]
</dt> <dd>

Der Daten Bank Pfad. Dieser Parameter darf nicht **null** sein.

</dd> <dt>

*ETYPE* \[ in\]
</dt> <dd>

Der Pfadtyp. Eine Liste der Werte finden Sie unter [**path \_ Type**](path-type.md) .

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt ein Handle für die Shimdatenbank zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbkreatedatabase**](sdbcreatedatabase.md)
</dt> </dl>

 

 




