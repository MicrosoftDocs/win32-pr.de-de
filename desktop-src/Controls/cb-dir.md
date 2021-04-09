---
title: CB_DIR Meldung (Winuser. h)
description: Fügt der Liste Namen hinzu, die im Kombinations Feld angezeigt werden. In der Meldung werden die Namen von Verzeichnissen und Dateien hinzugefügt, die einer angegebenen Zeichenfolge und einem Satz von Dateiattributen entsprechen. CB \_ dir kann auch zugeordnete Laufwerk Buchstaben zur Liste hinzufügen.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- Windows-Steuerelemente für CB_DIR Meldung
topic_type:
- apiref
api_name:
- CB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 98cbea5bb88614d5606dd3d5cb165be59f632556
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858896"
---
# <a name="cb_dir-message"></a>CB- \_ dir-Nachricht

Fügt der Liste Namen hinzu, die im Kombinations Feld angezeigt werden. In der Meldung werden die Namen von Verzeichnissen und Dateien hinzugefügt, die einer angegebenen Zeichenfolge und einem Satz von Dateiattributen entsprechen. **CB \_ DIR** können auch zugeordnete Laufwerk Buchstaben zur Liste hinzugefügt werden.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Attribute der Dateien oder Verzeichnisse, die dem Kombinations Feld hinzugefügt werden sollen. Dieser Parameter kann einen oder mehrere der folgenden Werte aufweisen.



| Wert                                                                                                                                                         | Bedeutung                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**DDL- \_ Archiv**</dt> </dl>       | Schließt archivierte Dateien ein.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**DDL- \_ Verzeichnis**</dt> </dl> | Schließt Unterverzeichnisse ein, die in eckigen Klammern () eingeschlossen sind \[ \] .<br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**DDL- \_ Laufwerke**</dt> </dl>          | Alle zugeordneten Laufwerke werden der Liste hinzugefügt. Laufwerke werden im Format x aufgelistet \[ -  - \] , wobei *x* für den Laufwerk Buchstaben steht.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DDL \_ exklusiv**</dt> </dl> | Schließt nur Dateien mit den angegebenen Attributen ein. Standardmäßig werden Lese-/schreibdateien aufgelistet, auch wenn DDL- \_ Schreibweise nicht angegeben ist.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ ausgeblendet**</dt> </dl>          | Schließt verborgene Dateien ein.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL-schreibgeschützt \_**</dt> </dl>    | Schließt schreibgeschützte Dateien ein.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**DDL- \_ Lesevorgang**</dt> </dl> | Umfasst Dateien mit Lese-/Schreibzugriff ohne zusätzliche Attribute. Dies ist die Standardoption.<br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**DDL- \_ System**</dt> </dl>          | Schließt Systemdateien ein.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **LPCTSTR** -Zeiger auf eine NULL-terminierte Zeichenfolge, die einen absoluten Pfad, einen relativen Pfad oder einen Dateinamen angibt. Ein absoluter Pfad kann mit einem Laufwerk Buchstaben (z. b. "d:" \) oder einem UNC-Namen (z. b. " \\ \\ *MachineName* \\ *ShareName*") beginnen. Wenn die Zeichenfolge einen Dateinamen oder ein Verzeichnis angibt, das über die vom *wParam* -Parameter angegebenen Attribute verfügt, wird der Dateiname oder das Verzeichnis der Liste hinzugefügt. Wenn der Dateiname oder der Verzeichnisname Platzhalter Zeichen enthält (? oder \* ), werden alle Dateien oder Verzeichnisse, die dem Platzhalter Ausdruck entsprechen und die vom *wParam* -Parameter angegebenen Attribute aufweisen, der im Kombinations Feld angezeigten Liste hinzugefügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert der null basierte Index des letzten namens, der der Liste hinzugefügt wird.

Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ Err. Wenn nicht genügend Speicherplatz zum Speichern der neuen Zeichen folgen verfügbar ist, ist der Rückgabewert CB \_ errspace.

## <a name="remarks"></a>Bemerkungen

Wenn *wParam* das DDL \_ -verzeichnisflag enthält und *LPARAM* alle Unterverzeichnisse eines Verzeichnisses der ersten Ebene (z. b. C: Temp) angibt \\ \\ \* , enthält das Listenfeld immer einen ".."-Eintrag für das Stammverzeichnis. Dies gilt auch, wenn das Stammverzeichnis ausgeblendete oder Systemattribute aufweist und die DDL-ausgeblendeten \_ und DDL- \_ systemFlags nicht angegeben werden. Das Stammverzeichnis eines NTFS-Volumes verfügt über verborgene Attribute und Systemattribute.

In der Liste werden lange Dateinamen angezeigt, sofern vorhanden.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser. h (Windows. h einschließen)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Verweis**
</dt> <dt>

[**CB \_ AddString**](cb-addstring.md)
</dt> <dt>

[**CB \_ InsertString**](cb-insertstring.md)
</dt> <dt>

[**Dlgdirlistcombobox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





