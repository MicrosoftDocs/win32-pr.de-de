---
title: LB_DIR (Winuser.h)
description: Fügt der Liste, die von einem Listenfeld angezeigt wird, Namen hinzu. Die Meldung fügt die Namen von Verzeichnissen und Dateien hinzu, die mit einer angegebenen Zeichenfolge und einem Satz von Dateiattributen übereinstimmen. LB DIR kann dem Listenfeld auch zugeordnete \_ Laufwerkbuchstaben hinzufügen.
ms.assetid: 5ec134e9-fe42-4cc0-bdea-fa5e66c218f6
keywords:
- LB_DIR meldungssteuerelemente Windows
topic_type:
- apiref
api_name:
- LB_DIR
api_location:
- Winuser.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f3add3c0ea14c637e0240ab296095bcc720aff9efb4c3e8e99a2f3de7019a711
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118671666"
---
# <a name="lb_dir-message"></a>LB \_ DIR-Nachricht

Fügt der Liste, die von einem Listenfeld angezeigt wird, Namen hinzu. Die Meldung fügt die Namen von Verzeichnissen und Dateien hinzu, die mit einer angegebenen Zeichenfolge und einem Satz von Dateiattributen übereinstimmen. **LB \_ DIR** kann dem Listenfeld auch zugeordnete Laufwerkbuchstaben hinzufügen.

## <a name="parameters"></a>Parameter

<dl> <dt>

*wParam* 
</dt> <dd>

Die Attribute der Dateien oder Verzeichnisse, die dem Listenfeld hinzugefügt werden sollen. Dieser Parameter kann einen oder mehrere der folgenden Werte sein.



| Wert                                                                                                                                                         | Bedeutung                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="DDL_ARCHIVE"></span><span id="ddl_archive"></span><dl> <dt>**DDL \_ ARCHIVE**</dt> </dl>       | Schließt archivierte Dateien ein.<br/>                                                                                                            |
| <span id="DDL_DIRECTORY"></span><span id="ddl_directory"></span><dl> <dt>**\_DDL-VERZEICHNIS**</dt> </dl> | Schließt Unterverzeichnisse ein. Unterverzeichnisnamen werden in eckige Klammern () \[ \] eingeschlossen.<br/>                                                |
| <span id="DDL_DRIVES"></span><span id="ddl_drives"></span><dl> <dt>**\_DDL-LAUFWERKE**</dt> </dl>          | Alle zugeordneten Laufwerke werden der Liste hinzugefügt. Laufwerke werden im Formular \[ - *x* - \] aufgeführt, wobei *x* der Laufwerkbuchstaben ist.<br/>                    |
| <span id="DDL_EXCLUSIVE"></span><span id="ddl_exclusive"></span><dl> <dt>**DDL \_ EXCLUSIVE**</dt> </dl> | Schließt nur Dateien mit den angegebenen Attributen ein. Standardmäßig werden Lese-/Schreibdateien auch dann aufgelistet, wenn DDL \_ READWRITE nicht angegeben ist.<br/> |
| <span id="DDL_HIDDEN"></span><span id="ddl_hidden"></span><dl> <dt>**DDL \_ HIDDEN**</dt> </dl>          | Schließt ausgeblendete Dateien ein.<br/>                                                                                                              |
| <span id="DDL_READONLY"></span><span id="ddl_readonly"></span><dl> <dt>**DDL \_ READONLY**</dt> </dl>    | Schließt schreibgeschützte Dateien ein.<br/>                                                                                                           |
| <span id="DDL_READWRITE"></span><span id="ddl_readwrite"></span><dl> <dt>**DDL \_ READWRITE**</dt> </dl> | Schließt Lese-/Schreibdateien ohne zusätzliche Attribute ein. Dies ist die Standardeinstellung.<br/>                                               |
| <span id="DDL_SYSTEM"></span><span id="ddl_system"></span><dl> <dt>**\_DDL-SYSTEM**</dt> </dl>          | Schließt Systemdateien ein.<br/>                                                                                                              |



 

</dd> <dt>

*lParam* 
</dt> <dd>

Ein Zeiger auf die auf NULL beendete Zeichenfolge, die einen absoluten Pfad, relativen Pfad oder Dateinamen angibt. Ein absoluter Pfad kann mit einem Laufwerkbuchstaben beginnen (z. B. d: oder einem UNC-Namen (z. B. \) \\ \\ *machinename* \\ *sharename).*

Wenn die Zeichenfolge einen Dateinamen oder ein Verzeichnis mit den attributen angibt, die vom *wParam-Parameter* angegeben werden, wird der Dateiname oder das Verzeichnis der Liste hinzugefügt. Wenn der Dateiname oder Verzeichnisname Platzhalterzeichen enthält (? oder ), werden alle Dateien oder Verzeichnisse, die mit dem Platzhalterausdruck übereinstimmen und über die vom \* *wParam-Parameter* angegebenen Attribute verfügen, der Liste hinzugefügt.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Wenn die Nachricht erfolgreich ist, ist der Rückgabewert der nullbasierte Index des Nachnamens, der der Liste hinzugefügt wurde.

Wenn ein Fehler auftritt, ist der Rückgabewert LB \_ ERR. Wenn nicht genügend Speicherplatz zum Speichern der neuen Zeichenfolgen verfügbar ist, ist der Rückgabewert LB \_ ERRSPACE.

## <a name="remarks"></a>Hinweise

Die [**LB \_ INITSTORAGE-Nachricht**](lb-initstorage.md) beschleunigt die Initialisierung von Listenfeldern mit einer großen Anzahl von Elementen (mehr als 100). Die angegebene Arbeitsspeichermenge wird reserviert, sodass nachfolgende **LB \_ DIR-Nachrichten** so kurz wie möglich dauern. Sie können Schätzungen für die *Parameter wParam* und *lParam* verwenden. Wenn Sie überschätzen, wird der zusätzliche Arbeitsspeicher zugeordnet. Wenn Sie zu viele Überschreitungen haben, wird die normale Zuordnung für Elemente verwendet, die den angeforderten Betrag überschreiten.

Wenn *wParam* das DDL DIRECTORY-Flag enthält und lParam alle Unterverzeichnisse eines Verzeichnisses der ersten Ebene angibt, z. B. C: TEMP, enthält das Listenfeld immer einen \_ Eintrag  \\ \\ \* ".." für das Stammverzeichnis. Dies gilt auch, wenn das Stammverzeichnis über ausgeblendete Attribute oder Systemattribute verfügt und die Flags DDL HIDDEN und \_ DDL \_ SYSTEM nicht angegeben sind. Das Stammverzeichnis eines NTFS-Volumes verfügt über ausgeblendete - und -Systemattribute.

In der Liste werden lange Dateinamen (sofern verfügbar) angezeigt.

Bei einer ANSI-Anwendung konvertiert das System den Text in einem Listenfeld mithilfe von CP ACP in \_ Unicode. Dies kann zu Problemen führen. Beispielsweise werden akzentierte romanische Zeichen in einem Nicht-Unicode-Listenfeld auf japanisch Windows geschachtelt angezeigt. Kompilieren Sie die Anwendung entweder als Unicode, oder verwenden Sie ein vom Besitzer gezeichnetes Listenfeld, um dieses Problem zu beheben.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                                           |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                     |
| Header<br/>                   | <dl> <dt>Winuser.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[**DlgDirList**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlista)
</dt> </dl>

 

 





