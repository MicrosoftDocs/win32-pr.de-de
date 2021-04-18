---
title: Siscsfilestobackupforlink-Funktion (Sisbkup. h)
description: Gibt Informationen zurück, die die gemeinsamen Speicherdateien beschreiben, auf die der angegebene SIS-Link verweist.
ms.assetid: 0580c34e-195a-4a2c-893f-bc339dcc88d7
keywords:
- Siscsfilestobackupforlink-Funktions Sicherung
topic_type:
- apiref
api_name:
- SisCSFilesToBackupForLink
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27d4f52728d662f43efed85d662874bd4b008947
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106340989"
---
# <a name="siscsfilestobackupforlink-function"></a>Siscsfilestobackupforlink-Funktion

Die **siscsfilestobackupforlink** -Funktion gibt Informationen zurück, die die gemeinsamen Speicherdateien beschreiben, auf die der angegebene SIS-Link verweist.

## <a name="syntax"></a>Syntax


```C++
BOOL SisCSFilesToBackupForLink(
  _In_  PVOID  sisBackupStructure,
  _In_  PVOID  reparseData,
  _In_  ULONG  reparseDataSize,
  _Out_ PVOID  thisFileContext,
  _Out_ PVOID  *matchingFileContext,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*sisbackupstructure* \[ in\]
</dt> <dd>

Ein Zeiger auf die SIS-Sicherungs Struktur, die von [**siscreatebackupstructure**](siscreatebackupstructure.md)zurückgegeben wurde.

</dd> <dt>

*Analysedaten* \[ in\]
</dt> <dd>

Zeiger auf den Inhalt des SIS-Analyse Punkts. Dieser Analyse Punkt enthält Daten, die einen SIS-Link beschreiben. Um die Analyse Punktdaten für eine Datei abzurufen, verwenden Sie den [**FSCTL \_ Get Analyse \_ \_ Point**](/windows/desktop/api/winioctl/ni-winioctl-fsctl_get_reparse_point) -Steuerungs Code.

</dd> <dt>

*Analyse DataSize* \[ in\]
</dt> <dd>

Größe des Inhalts des SIS-Analyse Punkts, auf den von Analyse *Daten* verwiesen wird (in Bytes).

</dd> <dt>

*thisfilecontext* \[ vorgenommen\]
</dt> <dd>

Zeiger auf eine von der Sicherungs Anwendung bereitgestellte Kontext Zeichenfolge, die diese Funktion aufgerufen hat. Der Inhalt dieser Inhalts Zeichenfolge wird von dieser Sicherungs Anwendung vollständig bestimmt und nicht von der SIS-Sicherungs-API interpretiert. Dieser Parameter ist optional. Wenn Sie nicht verwendet wird, legen Sie den Wert dieses Parameters auf **null** fest. Der Wert dieses Parameters wird in diesem Fall nicht verarbeitet.

</dd> <dt>

*matchingfilecontext* \[ vorgenommen\]
</dt> <dd>

Doppelter indirekter Zeiger auf die Kontext Zeichenfolge des SIS-Links, der durch die Informationen identifiziert wird, die in den ersten vier Parametern dieser Funktion übermittelt wurden. Dieser Parameter ist optional. Wenn keine Kontext Zeichenfolge als Wert des *thisfilecontext* -Parameters angegeben wird, legen Sie den Wert dieses Parameters auf **null** fest. Der Wert dieses Parameters wird in diesem Fall nicht verarbeitet.

</dd> <dt>

"count" für " *Anf. commonstorefilestobackup* \[ vorgenommen\]
</dt> <dd>

Anzahl der Dateien, die im Parameter " *commonstorefilestobackup* " aufgelistet sind.

</dd> <dt>

*commonstorefilestobackup* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Array von Dateinamen. Diese Dateien müssen gleichzeitig und auf die gleiche Weise gesichert werden wie die von [**siscreatebackupstructure**](siscreatebackupstructure.md)angeforderten Dateien des Common Stores.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** . Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Die Sicherungs Anwendung sollte diese Funktion für jede zu sichernde SIS-Linkdatei nur einmal aufzurufen.

Die Sicherungs Anwendung kann einen SIS-Analyse Punkt anhand ihres Tags, e/a- \_ \_ Analyse Tags, identifizieren \_ . Dieses Tag wird in "Winnt. h" definiert.

Wenn dieser Analyse Punkt, der durch den Wert des Parameters " *paramesedata* " identifiziert wird, die erste Instanz einer zu sichernden Datei beschreibt, gibt diese Funktion **null** als Wert des *matchingfilecontext* -Parameters zurück und initialisiert den Wert des *commonstorefilestobackup* -Arrays von Zeichen folgen mit den Namen der zu sichernden Datei im allgemeinen Speicher. Andernfalls legt diese Funktion den Wert des *matchingfilecontext* -Parameters auf die Kontext Zeichenfolge fest, die der ersten Instanz der angegebenen Datei entspricht, und legt den Wert des Parameters " *zähltofcommonstorefilestobackup* " auf "0" fest. Wenn mehrere Common-Store-Dateien vorhanden sind, die dem angegebenen Link entsprechen, entspricht der Wert des *thisfilecontext* -Parameters der Kontext Zeichenfolge, die der ersten Common-Store-Datei entspricht, die im-Array mit commonstorefilestobackup 0 zurückgegeben wird \[ \] .

Die aktuelle Version dieser Funktion gibt höchstens eine Common-Store-Datei zurück. es ist jedoch möglich, dass in zukünftigen Versionen ein einzelner Link durch mehrere Dateien im allgemeinen Speicher gestützt wird, z. b. für jeden Stream in der Datei, damit die Sicherungs Anwendung mehrere Dateien in jedem aufrufungs Vorgang unterstützt. In jedem Fall wird jede Common Store-Datei für jeden Sicherungs Durchlauf höchstens einmal zurückgegeben.

Die Sicherungs Anwendung sollte die Datei "Common-Store", die durch den Dateinamen oder die Dateinamen identifiziert wird, die im Parameter " *commonstorefilestobackup* " zurückgegeben werden, sichern oder wiederherstellen. Unabhängig davon, ob es eine entsprechende Datei mit dem gemeinsamen Speicher gibt, sollte die Sicherungs Anwendung die SIS-Verknüpfungs Datei wie auf dem Datenträger sichern, z. b. als Analyse Punkt und als sparsesdatei, und höchstwahrscheinlich ohne eingefüge Bereiche. Die Sicherungs Anwendung kann die Datei oder Dateien des Common Stores sofort sichern oder wiederherstellen, die Sicherung verzögern oder Sie nach Bedarf miteinander vermischen.

Nachdem der Sicherungs Vorgang beendet wurde, müssen Sie die Zuordnung des vom *commonstorefilestobackup* -Array von Zeichen folgen verwendeten Speichers durch Aufrufen von [**sisfrealloeredmemory**](sisfreeallocatedmemory.md)aufgehoben.

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

[**Sisfrezuden Speicher**](sisfreeallocatedmemory.md)
</dt> <dt>

[**Siscreatebackupstructure**](siscreatebackupstructure.md)
</dt> </dl>

 

