---
title: SisFreeRestoreStructure-Funktion (Sisbkup.h)
description: Gibt den für die angegebene SIS-Wiederherstellungsstruktur zugeordneten Arbeitsspeicher frei und führt Aufgaben aus, die den SIS-Filter für die ordnungsgemäße Einrichtung der während des Wiederherstellungsvorgang erstellten Links vorbereiten.
ms.assetid: dbdccb53-b38e-465d-a6d0-ee86923a5879
keywords:
- SisFreeRestoreStructure-Funktionssicherung
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
ms.openlocfilehash: a787283f933ae4ccd2d8100c39e6118b40c545c030bb236a27a2f1598417742e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117835548"
---
# <a name="sisfreerestorestructure-function"></a>SisFreeRestoreStructure-Funktion

Die **SisFreeRestoreStructure-Funktion** gibt den für die angegebene SIS-Wiederherstellungsstruktur zugeordneten Arbeitsspeicher frei und führt Aufgaben aus, die den SIS-Filter für die ordnungsgemäße Einrichtung der während des Wiederherstellungsvorgang erstellten Links vorbereiten.

## <a name="syntax"></a>Syntax


```C++
BOOL SisFreeRestoreStructure(
  _In_ PVOID sisRestoreStructure
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sisRestoreStructure* \[ In\]
</dt> <dd>

Zeiger auf eine SIS-Wiederherstellungsstruktur, die von [**SisCreateRestoreStructure zurückgegeben wird.**](siscreaterestorestructure.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **TRUE zurück,** wenn sie erfolgreich abgeschlossen wurde, andernfalls **FALSE.** Rufen [**Sie GetLastError auf,**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) um weitere Informationen zum Grund für den Fehler des Aufrufs zu erhalten.

## <a name="remarks"></a>Hinweise

Der Zugriff auf die SIS-Links, bevor der Aufruf dieser Funktion abgeschlossen ist, kann zu einer Volumeüberprüfung oder einem teiliellen Lesen des Linksinhalts führen.

Beachten Sie, dass es nicht sicher ist, davon auszugehen, dass dadurch nur Arbeitsspeicher zugewiesen wird. Diese Funktion kann beispielsweise auch zusätzliche Verwaltungsvorgänge für die SIS-Architektur ausführen. Rufen Sie diese Funktion daher auch dann auf, wenn der Wiederherstellungsvorgang unmittelbar danach beendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ XP-Desktop-Apps\]<br/>                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                   |
| Header<br/>                   | <dl> <dt>Sisbkup.h</dt> </dl>   |
| Bibliothek<br/>                  | <dl> <dt>Sisbkup.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Sisbkup.dll</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**SisCreateRestoreStructure**](siscreaterestorestructure.md)
</dt> </dl>

 

