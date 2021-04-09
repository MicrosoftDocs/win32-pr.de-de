---
title: Siscreaterestorestruktur-Funktion (Sisbkup. h)
description: Erstellt basierend auf den angegebenen Informationen eine SIS-Wiederherstellungs Struktur.
ms.assetid: acdd4258-813d-42af-a2e1-e59a1426f86c
keywords:
- Siscreaterestorestruktur-Funktions Sicherung
topic_type:
- apiref
api_name:
- SisCreateRestoreStructure
api_location:
- Sisbkup.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b83ebcdd609b00fdec19666a6915926692a2048
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858761"
---
# <a name="siscreaterestorestructure-function"></a>Siscreaterestorestruktur-Funktion

Die **siscreaterestorestruktur** -Funktion erstellt basierend auf den angegebenen Informationen eine SIS-Wiederherstellungs Struktur.

## <a name="syntax"></a>Syntax


```C++
BOOL SisCreateRestoreStructure(
  _In_  PWCHAR volumeRoot,
  _Out_ PVOID  *sisRestoreStructure,
  _Out_ PWCHAR *commonStoreRootPathname,
  _Out_ PULONG countOfCommonStoreFilesToRestore,
  _Out_ PWCHAR **commonStoreFilesToRestore
);
```



## <a name="parameters"></a>Parameter

<dl> <dt>

*volumeroot* \[ in\]
</dt> <dd>

Der Dateiname des volumestamms ohne nachfolgenden umgekehrten Schrägstrich des zu sichernden Volumes. Geben Sie z. b. "c:" und nicht "c:" an \\ . Das Volume kann nicht das System-oder Start Volume sein.

</dd> <dt>

*sisrestorestruktur* \[ vorgenommen\]
</dt> <dd>

Zurückgegebene SIS-Wiederherstellungs Struktur. Diese Struktur sollte vom Aufrufer als nicht transparent behandelt werden.

</dd> <dt>

*commonstorerootpathname* \[ vorgenommen\]
</dt> <dd>

Der voll qualifizierte Pfadname des allgemeinen Speicher des angegebenen Volumes. Beispiel: "c: \\ SIS Common Store".

</dd> <dt>

" *frajeficommonstorefilestorestore* \[ " vorgenommen\]
</dt> <dd>

Anzahl der Dateien, die im *commonstorefilestorestore* -Parameter aufgeführt sind.

</dd> <dt>

*commonstorefilestorestore* \[ vorgenommen\]
</dt> <dd>

Zeiger auf ein Array von Dateinamen, das die Liste der internen Dateien angibt, die von SIS zum Verwalten des angegebenen Volumes verwendet werden. Diese Dateien müssen gleichzeitig und auf die gleiche Weise wieder hergestellt werden wie die von [**siscsfilestobackupforlink**](siscsfilestobackupforlink.md)angeforderten Dateien des Common Stores.

</dd> </dl>

## <a name="return-value"></a>Rückgabewert

Diese Funktion gibt **true** zurück, wenn Sie erfolgreich abgeschlossen wurde, andernfalls **false** . Aufrufen von [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) zum Abrufen von weiteren Informationen über den Grund, warum der Fehler aufgetreten ist.

## <a name="remarks"></a>Bemerkungen

Diese Funktion legt die Wiederherstellungs Umgebung auf dem angegebenen Volume so fest, wie [**siscreatebackupstructure**](siscreatebackupstructure.md) die Sicherungs Umgebung auf dem angegebenen Volume festlegt.

Beachten Sie, dass diese Funktion nicht notwendigerweise die Common-Store-Datei oder die Dateien identifiziert, die einem Satz von SIS-Links auf dem Sicherungsmedium entsprechen, wenn diese gemeinsamen Speicherdateien oder Dateien noch auf dem Datenträger vorhanden sind. Der Inhalt des Datenstroms einer Datei der Common Store-Datei ändert sich nie, nachdem Sie erstellt wurde. wenn die Datei auf dem Datenträger bereits vorhanden ist, muss Sie daher nicht wieder hergestellt werden.

Dateinamen im allgemeinen Speicher sind global eindeutig, um die Integrität des Wiederherstellungs Vorgangs zu gewährleisten, auch wenn er nicht auf dem gleichen SIS-fähigen Volume auftritt, auf das der Sicherungs Vorgang zugegriffen hat.

Nachdem der Wiederherstellungs Vorgang beendet wurde, müssen Sie die Zuordnung des vom *commonstorefilestorestore* -Array von Zeichen folgen verwendeten Speichers durch Aufrufen von [**sisfrealloeredmemory**](sisfreeallocatedmemory.md)aufgehoben.

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
</dt> <dt>

[**Siscsfilestobackupforlink**](siscsfilestobackupforlink.md)
</dt> <dt>

[**Sisfrezuden Speicher**](sisfreeallocatedmemory.md)
</dt> <dt>

[**Sisfrebackupstructure**](sisfreebackupstructure.md)
</dt> </dl>

 

