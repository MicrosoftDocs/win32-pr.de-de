---
title: Sisfreerestorestruktur-Funktion (Sisbkup. h)
description: Gibt den für die angegebene SIS-Wiederherstellungs Struktur zugeordneten Arbeitsspeicher frei und führt Tasks aus, die den SIS-Filter vorbereiten, um die während des Wiederherstellungs Vorgangs erstellten Links ordnungsgemäß einzurichten.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- Sicherung der sisfreerestorestruktur-Funktion
topic_type:
- apiref
api_name:
- SisFreeRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7293514d798fe65c82863a83549039b05ec8eb3e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104478729"
---
# <a name="sisfreerestorestructure-function"></a>Sisfreerestorestruktur-Funktion

Die **sisfreerestorestruktur** -Funktion gibt den für die angegebene SIS-Wiederherstellungs Struktur zugeordneten Arbeitsspeicher frei und führt Tasks aus, die den SIS-Filter für die ordnungsgemäße Einrichtung der während des Wiederherstellungs Vorgangs erstellten Verknüpfungen vorbereiten.

## <a name="syntax"></a>Syntax


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sisrestorestruktur* \[ in\]
</dt> <dd>

Zeiger auf eine SIS-Wiederherstellungs Struktur, die von [**siscreaterestorestruktur**](siscreaterestorestructure.md)zurückgegeben wurde.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** . Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Der Zugriff auf die SIS-Links, bevor der Aufrufen dieser Funktion abgeschlossen wird, kann zu einer Volumeüberprüfung oder einem partiellen Lesevorgang für den Inhalt des Links führen.

Beachten Sie, dass es nicht sicher geht, dass dies nur den Arbeitsspeicher zuweist. Diese Funktion kann z. b. auch zusätzliche administrative Vorgänge für die SIS-Architektur ausführen. Daher wird diese Funktion auch dann aufgerufen, wenn der Wiederherstellungs Vorgang sofort beendet wird.

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

[**Siscreaterestorestruktur**](siscreaterestorestructure.md)
</dt> </dl>

 

