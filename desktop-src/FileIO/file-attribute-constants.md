---
Description: Dateiattribute sind Metadatenwerte, die vom Dateisystem auf dem Datenträger gespeichert werden und vom System verwendet werden und Entwicklern über verschiedene Datei-e/a-APIs zur Verfügung gestellt werden.
ms.assetid: ed9a73d2-7fb6-4fb7-97f6-4dbf89e2f156
title: Datei Attribut Konstanten (WinNT. h)
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/23/2020
ms.openlocfilehash: eae376462ae6c633be96e4434fbb782fa41c802f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357318"
---
# <a name="file-attribute-constants"></a>Dateiattributskonstanten

Dateiattribute sind Metadatenwerte, die vom Dateisystem auf dem Datenträger gespeichert werden und vom System verwendet werden und Entwicklern über verschiedene Datei-e/a-APIs zur Verfügung gestellt werden. Eine Liste verwandter APIs und Themen finden Sie im Abschnitt "Siehe auch".

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

Beispiel für ein [klassisches Windows](https://github.com/microsoft/Windows-classic-samples/blob/1d363ff4bd17d8e20415b92e2ee989d615cc0d91/Samples/Win7Samples/winbase/io/extendedfileapis/ExtendedFileAPIs.cpp) -Beispiel auf GitHub.



| Konstante/Wert                                                                                                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="FILE_ATTRIBUTE_ARCHIVE"></span><span id="file_attribute_archive"></span><dl> <dt>**Datei \_ Attribut \_ Archiv**</dt> <dt>32 (0x20)</dt> </dl>                                                       | Eine Datei oder ein Verzeichnis, das eine Archivdatei oder ein Archiv Verzeichnis ist. Anwendungen verwenden dieses Attribut in der Regel, um Dateien für die Sicherung oder Entfernung zu markieren. <br/>                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span id="FILE_ATTRIBUTE_COMPRESSED"></span><span id="file_attribute_compressed"></span><dl> <dt>**Datei \_ \_Komprimiertes Attribut**</dt> <dt>2048 (0x800)</dt> </dl>                                           | Eine komprimierte Datei oder ein Verzeichnis. Für eine Datei werden alle Daten in der Datei komprimiert. Für ein Verzeichnis ist die Komprimierung der Standardwert für neu erstellte Dateien und Unterverzeichnisse.<br/>                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DEVICE"></span><span id="file_attribute_device"></span><dl> <dt>**Datei \_ Attribut \_ Gerät**</dt> <dt>64 (0x40)</dt> </dl>                                                          | Dieser Wert ist für die Verwendung durch das System reserviert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span id="FILE_ATTRIBUTE_DIRECTORY"></span><span id="file_attribute_directory"></span><dl> <dt>**Datei \_ Attribut \_ Verzeichnis**</dt> <dt>16 (0x10)</dt> </dl>                                                 | Das Handle, das ein Verzeichnis identifiziert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| <span id="FILE_ATTRIBUTE_ENCRYPTED"></span><span id="file_attribute_encrypted"></span><dl> <dt>**Datei \_ \_Verschlüsseltes Attribut**</dt> <dt>16384 (0x4000)</dt> </dl>                                            | Eine Datei oder ein Verzeichnis, das verschlüsselt ist. Für eine Datei werden alle Datenströme in der Datei verschlüsselt. Für ein Verzeichnis ist die Verschlüsselung der Standardwert für neu erstellte Dateien und Unterverzeichnisse.<br/>                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_HIDDEN"></span><span id="file_attribute_hidden"></span><dl> <dt>**Datei \_ Attribut \_ ausgeblendet**</dt> <dt>2 (0x2)</dt> </dl>                                                            | Die Datei oder das Verzeichnis ist ausgeblendet. Er ist nicht in einer normalen Verzeichnis Auflistung enthalten.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| <span id="FILE_ATTRIBUTE_INTEGRITY_STREAM"></span><span id="file_attribute_integrity_stream"></span><dl> <dt>**Datei \_ Attribut \_ Integritäts Daten \_ Strom**</dt> <dt>32768 (0X8000)</dt> </dl>                      | Das Verzeichnis oder der Benutzerdaten Strom ist mit Integrität konfiguriert (wird nur auf Refs-Volumes unterstützt). Er ist nicht in einer normalen Verzeichnis Auflistung enthalten. Die Integritäts Einstellung bleibt mit der Datei erhalten, wenn Sie umbenannt wird. Wenn eine Datei kopiert wird, wird die Integrität der Zieldatei festgelegt, wenn die Quelldatei oder das Zielverzeichnis Integritäts festgelegt haben.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieses Flag wird bis Windows Server 2012 nicht unterstützt.<br/>                              |
| <span id="FILE_ATTRIBUTE_NORMAL"></span><span id="file_attribute_normal"></span><dl> <dt>**Datei \_ Attribut \_ Normal**</dt> <dt>128 (0x80)</dt> </dl>                                                         | Eine Datei, für die keine anderen Attribute festgelegt sind. Dieses Attribut ist nur gültig, wenn es allein verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_NOT_CONTENT_INDEXED"></span><span id="file_attribute_not_content_indexed"></span><dl> <dt>**Datei \_ Nicht mit dem \_ \_ Inhalt \_ indiziertes Attribut**</dt> <dt>8192 (0x2000)</dt> </dl>             | Die Datei oder das Verzeichnis wird nicht vom Inhalts Indizierungs Dienst indiziert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
| <span id="FILE_ATTRIBUTE_NO_SCRUB_DATA"></span><span id="file_attribute_no_scrub_data"></span><dl> <dt>**Datei \_ Attribute \_ No \_ \_ scrudata**</dt> <dt>131072 (0x20000)</dt> </dl>                            | Der Benutzerdaten Strom, der vom Hintergrunddaten Integritäts Scanner (auch Scrubber) nicht gelesen werden soll. Wenn es für ein Verzeichnis festgelegt ist, stellt es nur Vererbung bereit Dieses Flag wird nur für Speicherplätze und Refs-Volumes unterstützt. Er ist nicht in einer normalen Verzeichnis Auflistung enthalten.<br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008, Windows Vista, Windows Server 2003 und Windows XP:** Dieses Flag wird erst ab Windows 8 und Windows Server 2012 unterstützt.<br/>                                                                                                    |
| <span id="FILE_ATTRIBUTE_OFFLINE"></span><span id="file_attribute_offline"></span><dl> <dt>**Datei \_ Attribut \_ Offline**</dt> <dt>4096 (0x1000)</dt> </dl>                                                   | Die Daten einer Datei sind nicht sofort verfügbar. Dieses Attribut gibt an, dass die Datei Daten physisch in den Offline Speicher verschoben werden. Dieses Attribut wird von Remote Speicher verwendet, bei dem es sich um die hierarchische Speicherverwaltungssoftware handelt. Anwendungen sollten dieses Attribut nicht willkürlich ändern.<br/>                                                                                                                                                                                                                                                                         |
| <span id="FILE_ATTRIBUTE_READONLY"></span><span id="file_attribute_readonly"></span><dl> <dt>**Datei \_ Attribut \_**</dt> schreibgeschützt <dt>1 (0x1)</dt> </dl>                                                      | Eine Datei, die schreibgeschützt ist. Anwendungen können die Datei lesen, aber nicht in diese schreiben oder Sie löschen. Dieses Attribut wird für Verzeichnisse nicht berücksichtigt. Weitere Informationen finden Sie unter [Sie können die schreibgeschützten oder System Attribute von Ordnern in Windows Server 2003, in Windows XP, in Windows Vista oder Windows 7 nicht anzeigen oder ändern](https://support.microsoft.com/kb/326549).<br/>                                                                                                                                                                                           |
| <span id="FILE_ATTRIBUTE_RECALL_ON_DATA_ACCESS"></span><span id="file_attribute_recall_on_data_access"></span><dl> <dt>**Datei \_ Attribut \_ Rückruf \_ für den \_ Daten \_ Zugriff**</dt> <dt>4194304 (0x400000)</dt> </dl> | Wenn dieses Attribut festgelegt ist, bedeutet dies, dass die Datei oder das Verzeichnis nicht vollständig lokal vorhanden ist. Für eine Datei, die bedeutet, dass sich nicht alle Ihre Daten im lokalen Speicher befinden (z. b. geringer Dichte, wenn sich einige Daten noch im Remote Speicher befinden). Für ein Verzeichnis bedeutet dies, dass einige der Verzeichnisinhalte von einem anderen Speicherort aus virtualisiert werden. Das Lesen der Datei/das Auflisten des Verzeichnisses ist teurer als normal, z. b. führt dies dazu, dass zumindest ein Teil des Datei-/Verzeichnisinhalts aus einem Remote Speicher abgerufen wird. Dieses Bit kann nur von Aufrufern im Kernelmodus festgelegt werden<br/> |
| <span id="FILE_ATTRIBUTE_RECALL_ON_OPEN"></span><span id="file_attribute_recall_on_open"></span><dl> <dt>**Datei \_ Attribut \_ Rückruf \_ bei \_ Open**</dt> <dt>262144 (0x40000)</dt> </dl>                         | Dieses Attribut wird nur in verzeichnisenumerationstypen (Datei \_ Verzeichnis \_ Informationen, Datei Verzeichnisinformationen \_ \_ \_ usw.) angezeigt. Wenn dieses Attribut festgelegt ist, bedeutet dies, dass die Datei oder das Verzeichnis keine physische Darstellung auf dem lokalen System hat. das Element ist virtuell. Das Öffnen des Elements ist teurer als normal, weil es z. b. dazu führt, dass zumindest einige davon aus einem Remote Speicher abgerufen werden.<br/>                                                                                                                                                                 |
| <span id="FILE_ATTRIBUTE_REPARSE_POINT"></span><span id="file_attribute_reparse_point"></span><dl> <dt>**Datei \_ Attribut Analyse \_ \_ Punkt**</dt> <dt>1024 (0x400)</dt> </dl>                                 | Eine Datei oder ein Verzeichnis, das über einen zugeordneten Analyse Punkt verfügt, oder eine Datei, die eine symbolische Verknüpfung ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| <span id="FILE_ATTRIBUTE_SPARSE_FILE"></span><span id="file_attribute_sparse_file"></span><dl> <dt>**Datei \_ Attribut \_ \_ sparsedatei**</dt> <dt>512 (0x200)</dt> </dl>                                        | Eine Datei, die eine sparsedatei ist.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                            |
| <span id="FILE_ATTRIBUTE_SYSTEM"></span><span id="file_attribute_system"></span><dl> <dt>**Datei \_ Attribut \_ System**</dt> <dt>4 (0x4)</dt> </dl>                                                            | Eine Datei oder ein Verzeichnis, das vom Betriebssystem oder ausschließlich verwendet wird.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_TEMPORARY"></span><span id="file_attribute_temporary"></span><dl> <dt>**Datei \_ \_Temporäres Attribut**</dt> <dt>256 (0x100)</dt> </dl>                                               | Eine Datei, die für den temporären Speicher verwendet wird. Dateisysteme vermeiden das Schreiben von Daten in den Massenspeicher, wenn ausreichend Cache Arbeitsspeicher verfügbar ist, da eine Anwendung in der Regel eine temporäre Datei löscht, nachdem das Handle geschlossen wurde. In diesem Szenario kann das System das Schreiben der Daten vollständig vermeiden. Andernfalls werden die Daten geschrieben, nachdem das Handle geschlossen wurde.<br/>                                                                                                                                                                                                       |
| <span id="FILE_ATTRIBUTE_VIRTUAL"></span><span id="file_attribute_virtual"></span><dl> <dt>**Datei \_ \_Virtuelles Attribut**</dt> <dt>65536 (0x10000)</dt> </dl>                                                 | Dieser Wert ist für die Verwendung durch das System reserviert.<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |



## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|--------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows XP \[ -Desktop-Apps\]<br/>                                                            |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2003 \[ -Desktop-Apps\]<br/>                                                   |
| Header<br/>                   | <dl> <dt>WinNT. h (Include Windows. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Komprimierungs Attribut](compression-attribute.md)
</dt> <dt>

[Erstellen und Öffnen von Dateien](creating-and-opening-files.md)
</dt> <dt>

[**CreateFile**](/windows/desktop/api/FileAPI/nf-fileapi-createfilea)
</dt> <dt>

[**"Kreatefiletransagiert"**](/windows/desktop/api/WinBase/nf-winbase-createfiletransacteda)
</dt> <dt>

[**GetFileAttributes**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesa)
</dt> <dt>

[**Getfileattributesex**](/windows/desktop/api/FileAPI/nf-fileapi-getfileattributesexa)
</dt> <dt>

[**Getfileattributestransagiert**](/windows/desktop/api/WinBase/nf-winbase-getfileattributestransacteda)
</dt> <dt>

[**Getfileingeformationbyhandle**](/windows/desktop/api/FileAPI/nf-fileapi-getfileinformationbyhandle)
</dt> <dt>

[**Getfileingeformationbylenker Ex**](/windows/desktop/api/WinBase/nf-winbase-getfileinformationbyhandleex)
</dt> <dt>

[**Setfileattribute**](/windows/desktop/api/FileAPI/nf-fileapi-setfileattributesa)
</dt> <dt>

[**Setfileattributestranshandelten**](/windows/desktop/api/WinBase/nf-winbase-setfileattributestransacteda)
</dt> <dt>

[**Setfileingeformationbyhandle**](/windows/desktop/api/FileAPI/nf-fileapi-setfileinformationbyhandle)
</dt> </dl>

 

 




