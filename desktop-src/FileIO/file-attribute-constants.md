---
Description: Dateiattribute sind Metadatenwerte, die vom Dateisystem auf dem Datenträger gespeichert werden und vom System verwendet werden und entwicklern über verschiedene Datei-E/A-APIs zur Verfügung stehen.
ms.assetid: ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156
title: Dateiattributkonstanten (WinNT.h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
ms.openlocfilehash: 1dbb3d8e5eb091c47635f78eba9558a0d2262caeb5ce482c7b5bccdc3b237169
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050870"
---
# <a name="file-attribute-constants"></a>Dateiattributskonstanten

Dateiattribute sind Metadatenwerte, die vom Dateisystem auf dem Datenträger gespeichert werden und vom System verwendet werden und entwicklern über verschiedene Datei-E/A-APIs zur Verfügung stehen. Eine Liste der zugehörigen APIs und Themen finden Sie im Abschnitt Siehe auch .

## <a name="example"></a>Beispiel
```cpp


FILE_BASIC_INFO basicInfo;
    BOOL result;

    result = GetFileInformationByHandleEx( hFile,
                                               FileBasicInfo,
                                               &basicInfo,
                                               sizeof(basicInfo));

\\...

printf("  File Attributes: ");
    PrintFileAttributes(basicInfo.FileAttributes);

\\...
VOID
PrintFileAttributes(
    ULONG FileAttributes
    )
{
    
    if (FileAttributes & FILE_ATTRIBUTE_ARCHIVE) {
        printf("Archive ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_DIRECTORY) {
        printf("Directory ");
    }
    if (FileAttributes & FILE_ATTRIBUTE_READONLY) {
        printf("Read-Only ");
    }
}
```

Beispiel aus einem [Windows klassischen Beispiel](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/io/extendedfileapis/ExtendedFileAPIs.cpp) auf GitHub.



| Konstante/Wert                                                                                                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ ARCHIVE**</dt> <dt>32 (0x20)</dt> </dl>                                                       | Eine Datei oder ein Verzeichnis, bei dem es sich um eine Archivdatei oder ein Archivverzeichnis handelt. Anwendungen verwenden dieses Attribut in der Regel, um Dateien zum Sichern oder Entfernen von zu markieren. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="FILE_ATTRIBUTE_COMPRESSED"></span><span id="file_attribute_compressed"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ COMPRESSED**</dt> <dt>2048 (0x800)</dt> </dl>                                           | Eine komprimierte Datei oder ein Komprimiertes Verzeichnis. Bei einer Datei werden alle Daten in der Datei komprimiert. Bei einem Verzeichnis ist die Komprimierung die Standardeinstellung für neu erstellte Dateien und Unterverzeichnisse.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DEVICE"></span><span id="file_attribute_device"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ DEVICE**</dt> <dt>64 (0x40)</dt> </dl>                                                          | Dieser Wert ist für die Systemverwendung reserviert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DIRECTORY"></span><span id="file_attribute_directory"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ DIRECTORY**</dt> <dt>16 (0x10)</dt> </dl>                                                 | Das Handle, das ein Verzeichnis identifiziert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="FILE_ATTRIBUTE_ENCRYPTED"></span><span id="file_attribute_encrypted"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ ENCRYPTED**</dt> <dt>16384 (0x4000)</dt> </dl>                                            | Eine Datei oder ein Verzeichnis, die bzw. das verschlüsselt ist. Bei einer Datei werden alle Datenströme in der Datei verschlüsselt. Bei einem Verzeichnis ist die Verschlüsselung die Standardeinstellung für neu erstellte Dateien und Unterverzeichnisse.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ HIDDEN**</dt> <dt>2 (0x2)</dt> </dl>                                                            | Die Datei oder das Verzeichnis ist ausgeblendet. Sie ist nicht in einer normalen Verzeichnisauflistung enthalten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_INTEGRITY_STREAM"></span><span id="file_attribute_integrity_stream"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ INTEGRITY \_ STREAM**</dt> <dt>32768 (0x8000)</dt> </dl>                      | Das Verzeichnis oder der Benutzerdatenstrom ist mit Integrität konfiguriert (wird nur auf ReFS-Volumes unterstützt). Sie ist nicht in einer normalen Verzeichnisauflistung enthalten. Die Integritätseinstellung bleibt bei der Datei erhalten, wenn sie umbenannt wird. Wenn eine Datei kopiert wird, wird die Integrität der Zieldatei festgelegt, wenn für die Quelldatei oder das Zielverzeichnis die Integrität festgelegt ist.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieses Flag wird erst Windows Server 2012 unterstützt.<br/>                              |
| <span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ NORMAL**</dt> <dt>128 (0x80)</dt> </dl>                                                         | Eine Datei, für die keine anderen Attribute festgelegt sind. Dieses Attribut ist nur gültig, wenn es allein verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></span><span id="file_attribute_not_content_indexed"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ NOT \_ CONTENT \_ INDEXED**</dt> <dt>8192 (0x2000)</dt> </dl>             | Die Datei oder das Verzeichnis darf nicht vom Inhaltsindizierungsdienst indiziert werden.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="FILE_ATTRIBUTE_NO_SCRUB_DATA"></span><span id="file_attribute_no_scrub_data"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ NO \_ SCRUB \_ DATA**</dt> <dt>131072 (0x20000)</dt> </dl>                            | Der Benutzerdatenstrom, der nicht vom Hintergrunddatenintegritätsscanner (Background Data Integrity Scanner, Bereinigung) gelesen werden soll. Bei Festlegung in einem Verzeichnis wird nur vererbt. Dieses Flag wird nur auf Speicherplätze- und ReFS-Volumes unterstützt. Sie ist nicht in einer normalen Verzeichnisauflistung enthalten.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieses Flag wird erst unterstützt, wenn Windows 8 und Windows Server 2012.<br/>                                                                                                    |
| <span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ OFFLINE**</dt> <dt>4096 (0x1000)</dt> </dl>                                                   | Die Daten einer Datei sind nicht sofort verfügbar. Dieses Attribut gibt an, dass die Dateidaten physisch in den Offlinespeicher verschoben werden. Dieses Attribut wird von Remote Storage verwendet, bei dem es sich um die software für die hierarchische Speicherverwaltung handelt. Anwendungen sollten dieses Attribut nicht beliebig ändern.<br/>                                                                                                                                                                                                                                                                         |
| <span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ READONLY**</dt> <dt>1 (0x1)</dt> </dl>                                                      | Eine schreibgeschützte Datei. Anwendungen können die Datei lesen, aber nicht in sie schreiben oder löschen. Dieses Attribut wird in Verzeichnissen nicht berücksichtigt. Weitere Informationen finden Sie unter [You cannot view or change the Read-only or the System attributes of folders in Windows Server 2003, in Windows XP, in Windows Vista oder in Windows 7](https://support.microsoft.com/kb/326549).<br/>                                                                                                                                                                                           |
| <span id="FILE_ATTRIBUTE_RECALL_ON_DATA_ACCESS"></span><span id="file_attribute_recall_on_data_access"></span><dl> <dt>**FILE \_ ATTRIBUTRÜCKRUF BEI 4194304 FÜR \_ \_ DEN \_ \_ DATENZUGRIFF**</dt> <dt>(0x400000)</dt> </dl> | Wenn dieses Attribut festgelegt ist, bedeutet dies, dass die Datei oder das Verzeichnis nicht vollständig lokal vorhanden ist. Für eine Datei bedeutet dies, dass sich nicht alle Daten im lokalen Speicher (z. B. mit einigen Daten, die sich noch im Remotespeicher befindet) befindet. Für ein Verzeichnis bedeutet dies, dass ein Teil des Verzeichnisinhalts von einem anderen Speicherort virtualisiert wird. Das Lesen der Datei bzw. das Auflisten des Verzeichnisses ist teurer als normal. Dies führt z. B. dazu, dass mindestens ein Teil des Datei-/Verzeichnisinhalts aus einem Remotespeicher abgerufen wird. Nur Aufrufer im Kernelmodus können dieses Bit festlegen.<br/> |
| <span id="FILE_ATTRIBUTE_RECALL_ON_OPEN"></span><span id="file_attribute_recall_on_open"></span><dl> <dt>**FILE \_ \_ATTRIBUTRÜCKRUF \_ BEI \_ OPEN**</dt> <dt>262144 (0x40000)</dt> </dl>                         | Dieses Attribut wird nur in Verzeichnisenumerationsklassen (FILE \_ DIRECTORY \_ INFORMATION, FILE \_ BOTH DIR \_ INFORMATION \_ usw.) angezeigt. Wenn dieses Attribut festgelegt ist, bedeutet dies, dass die Datei oder das Verzeichnis keine physische Darstellung auf dem lokalen System hat. das Element ist virtuell. Das Öffnen des Elements ist teurer als normal. Dies führt beispielsweise dazu, dass mindestens ein Teil davon aus einem Remotespeicher abgerufen wird.<br/>                                                                                                                                                                 |
| <span id="FILE_ATTRIBUTE_REPARSE_POINT"></span><span id="file_attribute_reparse_point"></span><dl> <dt>**FILE \_ \_ \_ ATTRIBUTREARSEPUNKT**</dt> <dt>1024 (0x400)</dt> </dl>                                 | Eine Datei oder ein Verzeichnis, dem ein Replikationspunkt zugeordnet ist, oder eine Datei, die eine symbolische Verknüpfung ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FILE_ATTRIBUTE_SPARSE_FILE"></span><span id="file_attribute_sparse_file"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ SPARSE \_ FILE**</dt> <dt>512 (0x200)</dt> </dl>                                        | Eine Datei, die eine Sparsedatei ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ SYSTEM**</dt> <dt>4 (0x4)</dt> </dl>                                                            | Eine Datei oder ein Verzeichnis, von der bzw. das das Betriebssystem einen Teil von oder ausschließlich verwendet.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ TEMPORARY**</dt> <dt>256 (0x100)</dt> </dl>                                               | Eine Datei, die für den temporären Speicher verwendet wird. Dateisysteme vermeiden das Zurückschreiben von Daten in den Massenspeicher, wenn ausreichend Cachespeicher verfügbar ist, da eine Anwendung in der Regel eine temporäre Datei löscht, nachdem das Handle geschlossen wurde. In diesem Szenario kann das System das Schreiben der Daten vollständig vermeiden. Andernfalls werden die Daten geschrieben, nachdem das Handle geschlossen wurde.<br/>                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_VIRTUAL"></span><span id="file_attribute_virtual"></span><dl> <dt>**FILE \_ ATTRIBUTE \_ VIRTUAL**</dt> <dt>65536 (0x10000)</dt> </dl>                                                 | Dieser Wert ist für die Systemverwendung reserviert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur XP-Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2003-Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT.h (include Windows.h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komprimierungsattribut](compression-attribute.md)
</dt> <dt>

[Erstellen und Öffnen von Dateien](creating-and-opening-files.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**CreateFileTransacted**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**GetFileAttributesEx**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**GetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
</dt> <dt>

[**GetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)
</dt> <dt>

[**GetFileInformationByHandleEx**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)
</dt> <dt>

[**SetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**SetFileAttributesTransacted**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)
</dt> <dt>

[**SetFileInformationByHandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)
</dt> </dl>

 

 




