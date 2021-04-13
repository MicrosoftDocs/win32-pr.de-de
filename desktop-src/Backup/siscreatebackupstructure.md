---
title: Siscreatebackupstructure-Funktion (Sisbkup. h)
description: Erstellt basierend auf den angegebenen Informationen eine SIS-Sicherungs Struktur.
ms.assetid: a8c48961-fa24-4eb6-92cd-1b9bc83cec41
keywords:
- Siscreatebackupstructure-Funktions Sicherung
topic_type:
- apiref
api_name:
- SisCreateBackupStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ad432095f9d264e124df1d84070056fc827c625e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475927"
---
# <a name="siscreatebackupstructure-function"></a>Siscreatebackupstructure-Funktion

Die Funktion **siscreatebackupstructure** erstellt basierend auf den angegebenen Informationen eine SIS-Sicherungs Struktur.

## <a name="syntax"></a>Syntax


```C++
BOOL SisCreateBackupStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisBackupStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToBackUp,
  _Out_ PWCHAR **commonStoreFilesToBackUp
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*volumeroot* \[ in\]
</dt> <dd>

Der Dateiname des volumestamms ohne nachfolgenden umgekehrten Schrägstrich des zu sichernden Volumes. Geben Sie z. b. "c:" und nicht "c:" an \\ .

</dd> <dt>

*sisbackupstructure* \[ vorgenommen\]
</dt> <dd>

SIS-Sicherungs Struktur zurückgegeben.

</dd> <dt>

*commonstorerootpathname* \[ vorgenommen\]
</dt> <dd>

Der voll qualifizierte Pfadname des allgemeinen Speicher des angegebenen Volumes. Beispiel: "c: \\ SIS Common Store".

</dd> <dt>

"count" für " *Anf. commonstorefilestobackup* \[ vorgenommen\]
</dt> <dd>

Anzahl der Dateien, die im Parameter " *commonstorefilestobackup* " aufgelistet sind.

</dd> <dt>

*commonstorefilestobackup* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Array von Dateinamen, das eine Liste interner Dateien angibt, die von SIS zum Verwalten des angegebenen Volumes verwendet werden. Diese Dateien müssen gleichzeitig und auf die gleiche Weise gesichert werden wie die von [ **siscsfilestobackupforlink** angeforderten Dateien des Common Stores.](siscsfilestobackupforlink.md)

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** . Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion erstellt eine SIS-Sicherungs Struktur, die von der SIS Backup-API verwendet wird, um eine Liste der Datei Verknüpfungen auf dem Volume und die ursprünglichen Dateien, auf die die Verknüpfungen verweisen, zu erstellen und zu verwalten. Diese Funktion sollte nur einmal für jedes zu sichernde SIS-fähige Volume aufgerufen werden. Alle Dateien innerhalb des angegebenen Volumes sollten als Dateien für den gemeinsamen Speicher behandelt und nur gesichert werden, wenn SIS angibt, dass dies der Fall sein sollte.

Die Parameter " *thestof commonstorefilestobackup* " und " *commonstorefilestobackup* " geben eine Liste der Dateien zurück, die unabhängig von den gesicherten Links gesichert werden müssen.

Wenn der Wert für " *Anf commonstorefilestobackup* " 0 ist, kann " *commonstorefilestobackup* " ein **null** -Zeiger sein. Der Wert des *commonstorefilestobackup* -Parameters sollte ignoriert werden.

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

[**Siscreaterestorestruktur**](siscreaterestorestructure.md)
</dt> <dt>

[**Siscsfilestobackupforlink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**Sisfrezuden Speicher**](sisfreeallocatedmemory.md)
</dt> </dl>

 

