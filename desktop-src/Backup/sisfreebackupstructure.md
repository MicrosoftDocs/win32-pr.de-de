---
title: SisFreeBackupStructure-Funktion (Sisbkup.h)
description: Gibt die angegebene SIS-Sicherungsstruktur frei.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Sicherung der SisFreeBackupStructure-Funktion
topic_type:
- apiref
api_name:
- SisFreeBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1e506881110ad9fbb60ea12479c64f8ef8024f8e0f9ddee753813795d31f3dd6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119021358"
---
# <a name="sisfreebackupstructure-function"></a>SisFreeBackupStructure-Funktion

Die **SisFreeBackupStructure-Funktion** gibt die angegebene SIS-Sicherungsstruktur frei.

## <a name="syntax"></a>Syntax


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sisBackupStructure* \[ In\]
</dt> <dd>

Zeiger auf die SIS-Sicherungsstruktur, die von [**SisCreateBackupStructure**](siscreatebackupstructure.md)zurückgegeben wird.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE** zurück, wenn sie erfolgreich abgeschlossen wurde, andernfalls **FALSE.** Rufen [**Sie GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) auf, um weitere Informationen zur Ursache des Fehlers beim Aufruf zu erhalten.

## <a name="remarks"></a>Hinweise

Diese Funktion sollte aufgerufen werden, nachdem der Sicherungsvorgang für das Volume abgeschlossen wurde, das durch den Wert des *parameters sisBackupStructure* identifiziert wird.

Beachten Sie, dass es nicht sicher ist, davon auszugehen, dass dadurch nur der Arbeitsspeicher freigegeben wird. Diese Funktion kann beispielsweise auch zusätzliche Verwaltungsvorgänge für die SIS-Architektur ausführen. Rufen Sie diese Funktion daher auch dann auf, wenn Der Sicherungsvorgang unmittelbar danach beendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SisCreateBackupStructure**](siscreatebackupstructure.md)
</dt> </dl>

 

