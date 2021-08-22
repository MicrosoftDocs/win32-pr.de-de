---
description: Öffnet die angegebene Apphelp-Detaildatenbank.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: SdbOpenApphelpDetailsDatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbOpenApphelpDetailsDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: d6bd0bc7cbd1404c3bcf5459254f53e62a777d0936b89a0f7a282dd8d0094227
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120045160"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a>SdbOpenApphelpDetailsDatabase-Funktion

Öffnet die angegebene Apphelp-Detaildatenbank.

## <a name="syntax"></a>Syntax


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwsDetailsDatabasePath* \[ in, optional\]
</dt> <dd>

Der Datenbankpfad. Wenn dieser Parameter **NULL** ist, wird die lokale Systemdatenbank geöffnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die Funktion gibt ein Handle für die Apphelp-Detaildatenbank zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




