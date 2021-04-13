---
description: Hebt die Registrierung der angegebenen Datenbank auf, sodass Sie nicht mehr verfügbar ist.
ms.assetid: 7e6c50f4-85f6-4b33-b639-d8fda143e5e7
title: Sdbunregisterdatabase-Funktion
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbUnregisterDatabase
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 72171e1f9ae20ac2213a285046b2499093be4313
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104483118"
---
# <a name="sdbunregisterdatabase-function"></a>Sdbunregisterdatabase-Funktion

Hebt die Registrierung der angegebenen Datenbank auf, sodass Sie nicht mehr verfügbar ist.

## <a name="syntax"></a>Syntax


```C++
BOOL WINAPI SdbUnregisterDatabase(
  _In_ GUID *pguidDB
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*pguiddb* \[ in\]
</dt> <dd>

Die GUID der Datenbank. Dieser Parameter darf nicht **null** sein.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Bei einem Fehler gibt die Funktion **true** oder **false** zurück.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| DLL<br/>                      | <dl> <dt>Apphelp.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Sdbregisterdatabaseex**](sdbregisterdatabaseex.md)
</dt> </dl>

 

 




