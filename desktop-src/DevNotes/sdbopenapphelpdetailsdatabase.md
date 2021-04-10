---
description: Öffnet die angegebene AppHelp-Detail Datenbank.
ms.assetid: c3b07c00-a3c6-419c-94c6-34c573a04d6d
title: Sdbopenapphelpdetailsdatabase-Funktion
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
ms.openlocfilehash: 2810b0bbe1f10f013f39570aecda448a4ceeea6c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104125623"
---
# <a name="sdbopenapphelpdetailsdatabase-function"></a>Sdbopenapphelpdetailsdatabase-Funktion

Öffnet die angegebene AppHelp-Detail Datenbank.

## <a name="syntax"></a>Syntax


```C++
PDB WINAPI SdbOpenApphelpDetailsDatabase(
  _In_opt_ LPCWSTR pwsDetailsDatabasePath
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pwsdetailsdatabasepath* \[ in, optional\]
</dt> <dd>

Der Daten Bank Pfad. Wenn dieser Parameter **null** ist, wird die lokale Systemdatenbank geöffnet.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Die-Funktion gibt ein Handle für die AppHelp-Detail Datenbank zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



 

 




