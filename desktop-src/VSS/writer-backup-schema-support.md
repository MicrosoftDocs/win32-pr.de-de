---
description: Um eine Sicherung vollständig zu implementieren, ist die Beteiligung der Writer des Systems erforderlich.
ms.assetid: ea504f8e-26d9-499e-b3e9-03515b480a75
title: Unterstützung des Writersicherungsschemas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b037591d6deda2657acdfe4f4e4755fef96b52bafc92e4cc51e4ef7119de1f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118344243"
---
# <a name="writer-backup-schema-support"></a>Unterstützung des Writersicherungsschemas

Um eine Sicherung vollständig zu implementieren, ist die Beteiligung der Writer des Systems erforderlich. Verschiedene Unterstützte Sicherungstypen werden als Schemas bezeichnet und durch eine Bitmaske (oder bitweises OR) von Membern der [**VSS \_ BACKUP \_ SCHEMA-Enumeration**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) angegeben. Die derzeit unterstützten gültigen Schemas umfassen Folgendes:

-   Standardschema: Vollständig \_ (VSS BS UNDEFINED) – gibt an, dass ein Writer eine Sicherung unterstützt, bei der alle Dateien unabhängig vom letzten Sicherungsdatum \_ gesichert werden. Der Sicherungsverlauf jeder Datei kann vom Anfordernden aktualisiert werden, und Writer, die den \_ VSS BS TIMESTAMPED-Enumerationswert unterstützen, speichern einen aktualisierten Zeitstempel mit dem \_ Anfordernden. Dieses Sicherungsschema kann als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden.

    Zum Wiederherstellen einer vollständigen Sicherung ist nur ein einzelnes Sicherungsimage erforderlich.

-   Kopiesicherung (VSS BS COPY) – wie das \_ \_ VSS BS FULL-Sicherungsschema – gibt an, dass ein Writer eine Sicherung unterstützt, bei der alle Dateien unabhängig vom letzten Sicherungsdatum gesichert \_ \_ werden. Der Sicherungsverlauf jeder Datei wird jedoch weder von der Anfordernden noch vom Writer aktualisiert, und diese Art von Sicherung kann nicht als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden.
-   Protokolldatei (VSS BS LOG): Nur die Protokolldateien eines \_ \_ Writers müssen sichern. Dies erfordert, dass ein Writer mindestens einer Komponente mithilfe der [**IVssCreateWriterMetadata::AddDatabaseLogFiles-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) mindestens eine Datei hinzugefügt hat. Dieser Sicherungstyp ist für VSS spezifisch.
-   Benutzerdefinierte Wiederherstellungsstandorte (VSS BS WRITER UNTERSTÜTZT NEUES ZIEL) – gibt die Writerunterstützung für einen Anfordernden an, der zum Zeitpunkt der Wiederherstellung angibt, wo seine Dateien \_ \_ \_ \_ \_ wiederhergestellt werden. Dies bedeutet, dass ein Writer so codiert wurde, dass er auf eine solche Verschiebung überprüft (mithilfe von [**IVssComponent::GetNewTarget)**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)und über die Kapazität zum Arbeiten mit verschobenen Dateien verfügt.
-   Wiederherstellung mit Move (VSS \_ BS WRITER UNTERSTÜTZT RESTORE WITH MOVE) – gibt an, dass der Writer die Ausführung mehrerer Writerinstanzen mit der gleichen Klassen-ID unterstützt und dass ein Anfordernder eine Komponente zur Wiederherstellungszeit in eine andere Writerinstanz verschieben \_ \_ \_ \_ \_ kann. Die Writerinstanz wird mithilfe eines persistenten Writerinstanznamens angegeben, der als *wszWriterInstanceName-Parameter* an die [**CVssWriter::Initialize-Methode übergeben**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) wurde. Eine Anfordernde kann den Namen der Writerinstanz mithilfe von [**IVssExerklärwriterMetadataEx::GetIdentityEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex) abrufen und Komponenten während der Wiederherstellung mithilfe von [**IVssBackupComponentsEx::SetSelectedForRestoreEx**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)verschieben.

    **Windows Server 2003 und Windows XP:** Dieser Wert wird erst ab Windows Server 2003 mit Service Pack 1 (SP1) unterstützt.

-   Inkrementell (VSS BS INCREMENTAL): Gibt an, dass der Writer die \_ VSS-API verwendet, um dem Anfordernden zu helfen. So wird sichergestellt, dass nur Dateien, die seit der letzten vollständigen oder inkrementellen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert \_ werden.

    Das Wiederherstellen einer inkrementellen Sicherung erfordert das ursprüngliche Sicherungsimage und alle inkrementellen Sicherungsimages, die seit der ersten Sicherung erstellt wurden.

-   Differenziell (VSS BS DIFFERENTIAL): Gibt an, dass der Writer die \_ VSS-API verwendet, um dem Anfordernden zu helfen sicherzustellen, dass nur Dateien, die seit der letzten vollständigen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden sollen. Alle Zwischensicherungsinformationen werden \_ ignoriert.

    Das Wiederherstellen einer differenziellen Sicherung erfordert das ursprüngliche Sicherungsimage und das letzte differenzielle Sicherungsimage, das seit der letzten vollständigen Sicherung erstellt wurde.

-   Inkrementell/differenziell: Zeitstempelunterstützung (VSS BS TIMESTAMPED) – gibt an, dass ein Writer die Verwendung des VSS-Zeitstempelmechanismus unterstützt, um Dateien in inkrementelle oder differenzielle Vorgänge \_ \_ ein schließen zu können. Bei der Sicherung muss [](vssgloss-f.md) der Writer den Sicherungsstempel eines Dateisets mit der [**IVssComponent::SetBackupStamp-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) speichern und bei der Wiederherstellung mit [**IVssComponent::GetPreviousBackupStamp abrufen.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)
-   Inkrementell/differenziell: Unterstützung der letzten Änderung (VSS BS LAST MODIFY) – gibt an, dass ein Writer bei der Implementierung inkrementeller oder differenzieller Sicherungen mit differenzierten Dateien informationen zum Zeitpunkt der letzten Änderung unabhängig bereitstellen \_ \_ \_ kann. Diese Informationen können einem Anfordernden über die [**IVssComponent::AddDifferencedFilesByLastModifyTime-Methode bereitgestellt**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) werden.
-   Inkrementell/differenziell: Die Unterstützungsbeschränkung (VSS BS EXCLUSIVE INCREMENTAL DIFFERENTIAL) gibt an, dass Writer sowohl differenzielle als auch inkrementelle \_ \_ \_ Sicherungsschemas unterstützen, aber nur exklusiv: Beispielsweise können Sie einer inkrementellen Sicherung mit einer differenziellen Sicherung nicht \_ folgen.
-   Unabhängiger Systemstatus (VSS BS INDEPENDENT SYSTEM STATE) – gibt an, dass der Writer das Sichern von Daten unterstützt, die Teil des Systemstatus sind, aber auch unabhängig vom Systemstatus sichern \_ \_ \_ \_ können.

    **Windows Server 2003 und Windows XP:** Dieser Wert wird erst nach der Windows Vista unterstützt.

-   Roll-Forward Restore (VSS BS ROLLFORWARD RESTORE) – gibt an, dass der Writer das Festlegen eines \_ \_ \_ Rollforward-Wiederherstellungspunkts mithilfe von [**IVssBackupComponentsEx2::SetRollForward unterstützt.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward)

    **Windows Server 2003 und Windows XP:** Dieser Wert wird erst nach der Windows Vista unterstützt.

-   Umbenennen wiederherstellen (VSS BS RESTORE RENAME) – gibt an, dass der Writer das Festlegen eines Wiederherstellungsnamens durch einen Anfordernden mithilfe von \_ \_ \_ [**IVssBackupComponentsEx2::SetRestoreName unterstützt.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename)

    **Windows Server 2003 und Windows XP:** Dieser Wert wird erst nach der Windows Vista unterstützt.

-   Autoritative Wiederherstellung (VSS BS AUTHORITATIVE RESTORE): Gibt an, dass der Writer eine anfordernde Einstellung für die autoritative Wiederherstellung mithilfe von \_ \_ \_ [**IVssBackupComponentsEx2::SetAuthoritativeRestore unterstützt.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore)

Writer legen ihre Schemas mithilfe der [**IVssCreateWriterMetadata::SetBackupSchema-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) fest, und eine Anfordernde ruft das Schema jedes Writers ab, indem sie [**IVssExkatWriterMetadata::GetBackupSchema aufruft.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema)

 

 



