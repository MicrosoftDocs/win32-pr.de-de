---
title: Sisfrebackupstructure-Funktion (Sisbkup. h)
description: Gibt die angegebene SIS-Sicherungs Struktur frei.
ms.assetid: 34d5e919-e4bf-4105-ac15-a2ff5adfbdee
keywords:
- Sisfrebackupstructure-Funktions Sicherung
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
ms.openlocfilehash: d3a135c4787ff116ec10efd61fa1492033393c88
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103740696"
---
# <a name="sisfreebackupstructure-function"></a>Sisfrebackupstructure-Funktion

Die **sisfrebackupstructure** -Funktion gibt die angegebene SIS-Sicherungs Struktur frei.

## <a name="syntax"></a>Syntax


```C++
BOOL SisFreeBackupStructure(
  _In_ PVOID sisBackupStructure
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sisbackupstructure* \[ in\]
</dt> <dd>

Ein Zeiger auf die SIS-Sicherungs Struktur, die von [**siscreatebackupstructure**](siscreatebackupstructure.md)zurückgegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** . Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion sollte aufgerufen werden, nachdem der Sicherungs Vorgang für das durch den Wert des Parameters *sisbackupstructure* identifizierte Volume abgeschlossen wurde.

Beachten Sie, dass es nicht sicher geht, dass dies nur den Arbeitsspeicher zuweist. Diese Funktion kann z. b. auch zusätzliche administrative Vorgänge für die SIS-Architektur ausführen. Daher wird diese Funktion auch dann aufgerufen, wenn der Sicherungs Vorgang sofort danach beendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup. h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Sisbkup. lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Siscreatebackupstructure**](siscreatebackupstructure.md)
</dt> </dl>

 

