---
title: CB_DIR (Winuser.h)
description: Fügt der Liste, die im Kombinationsfeld angezeigt wird, Namen hinzu. Die Meldung fügt die Namen von Verzeichnissen und Dateien hinzu, die mit einer angegebenen Zeichenfolge und einem Satz von Dateiattributen übereinstimmen. CB \_ DIR kann der Liste auch zugeordnete Laufwerkbuchstaben hinzufügen.
ms.assetid: 6082d12c-0af4-4a99-98c0-6a98d171f4d8
keywords:
- CB_DIR von Windows-Steuerelementen
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
ms.openlocfilehash: defa19ffdebfb448e1a89c141da0b275c1df1bffdcfa9e3914293400d706b7ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119577120"
---
# <a name="cb_dir-message"></a>CB \_ DIR-Nachricht

Fügt der Liste, die im Kombinationsfeld angezeigt wird, Namen hinzu. Die Meldung fügt die Namen von Verzeichnissen und Dateien hinzu, die mit einer angegebenen Zeichenfolge und einem Satz von Dateiattributen übereinstimmen. **CB \_ DIR** kann der Liste auch zugeordnete Laufwerkbuchstaben hinzufügen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Attribute der Dateien oder Verzeichnisse, die dem Kombinationsfeld hinzugefügt werden sollen. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                         | Bedeutung                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**DDL \_ ARCHIVE**</dt> </dl>       | Schließt archivierte Dateien ein.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**\_DDL-VERZEICHNIS**</dt> </dl> | Schließt Unterverzeichnisse ein, die in eckige Klammern () eingeschlossen \[ \] sind.<br/>                                                             |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**\_DDL-LAUFWERKE**</dt> </dl>          | Alle zugeordneten Laufwerke werden der Liste hinzugefügt. Laufwerke werden im Formular \[ - *x* - \] aufgeführt, wobei *x* der Laufwerkbuchstaben ist.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DDL \_ EXCLUSIVE**</dt> </dl> | Schließt nur Dateien mit den angegebenen Attributen ein. Standardmäßig werden Lese-/Schreibdateien auch dann aufgelistet, wenn DDL \_ READWRITE nicht angegeben ist.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ HIDDEN**</dt> </dl>          | Schließt ausgeblendete Dateien ein.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL \_ READONLY**</dt> </dl>    | Schließt schreibgeschützte Dateien ein.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**DDL \_ READWRITE**</dt> </dl> | Schließt Lese-/Schreibdateien ohne zusätzliche Attribute ein. Dies ist die Standardoption.<br/>                                                       |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**\_DDL-SYSTEM**</dt> </dl>          | Schließt Systemdateien ein.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein **LPCTSTR-Zeiger** auf eine auf NULL beendete Zeichenfolge, die einen absoluten Pfad, relativen Pfad oder Dateinamen angibt. Ein absoluter Pfad kann mit einem Laufwerkbuchstaben beginnen (z. B. d: oder einem UNC-Namen (z. B. \) \\ \\ *machinename* \\ *sharename).* Wenn die Zeichenfolge einen Dateinamen oder ein Verzeichnis mit den attributen angibt, die vom *wParam-Parameter* angegeben werden, wird der Dateiname oder das Verzeichnis der Liste hinzugefügt. Wenn der Datei- oder Verzeichnisname Platzhalterzeichen enthält (? oder ), werden alle Dateien oder Verzeichnisse, die mit dem Platzhalterausdruck übereinstimmen und über die vom \* *wParam-Parameter* angegebenen Attribute verfügen, der im Kombinationsfeld angezeigten Liste hinzugefügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert der nullbasierte Index des Nachnamens, der der Liste hinzugefügt wurde.

Wenn ein Fehler auftritt, ist der Rückgabewert CB \_ ERR. Wenn nicht genügend Speicherplatz zum Speichern der neuen Zeichenfolgen verfügbar ist, ist der Rückgabewert CB \_ ERRSPACE.

## <a name="remarks"></a>Hinweise

Wenn *wParam* das DDL DIRECTORY-Flag enthält und lParam alle Unterverzeichnisse eines Verzeichnisses der ersten Ebene angibt, z. B. C: TEMP, enthält das Listenfeld immer einen \_ Eintrag  \\ \\ \* ".." für das Stammverzeichnis. Dies gilt auch, wenn das Stammverzeichnis über ausgeblendete Attribute oder Systemattribute verfügt und die Flags DDL HIDDEN und \_ DDL \_ SYSTEM nicht angegeben sind. Das Stammverzeichnis eines NTFS-Volumes verfügt über ausgeblendete - und -Systemattribute.

In der Liste werden lange Dateinamen (sofern verfügbar) angezeigt.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

**Referenz**
</dt> <dt>

[**CB \_ ADDSTRING**](cb-addstring.md)
</dt> <dt>

[**CB \_ INSERTSTRING**](cb-insertstring.md)
</dt> <dt>

[**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)
</dt> </dl>

 

 





