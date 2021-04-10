---
description: Um eine Sicherung vollständig zu implementieren, ist die Teilnahme der Schreiber des Systems erforderlich.
ms.assetid: ea504f8e-26d9-499e-b3e9-03515b480a75
title: Unterstützung für Writer-Sicherungs Schema
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593df12f552f206d5d0eedbf8d021b69ef955c6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214615"
---
# <a name="writer-backup-schema-support"></a>Unterstützung für Writer-Sicherungs Schema

Um eine Sicherung vollständig zu implementieren, ist die Teilnahme der Schreiber des Systems erforderlich. Verschiedene Typen von unterstützten Sicherungen werden als Schemas bezeichnet und durch eine Bitmaske (oder ein bitweises OR) von Membern der [**VSS- \_ Sicherungs \_ Schema**](/windows/desktop/api/Vss/ne-vss-vss_backup_schema) -Enumeration angegeben. Die derzeit unterstützten gültigen Schemas umfassen Folgendes:

-   Standard Schema: Full (VSS \_ - \_ undefiniert) – gibt an, dass ein Writer eine Sicherung unterstützt, in der alle Dateien unabhängig vom Zeitpunkt der letzten Sicherung gesichert werden. Der Sicherungs Verlauf der einzelnen Dateien kann von der anfordernden Person aktualisiert werden, und Writer, die den Enumerationswert von VSS-SB-Zeitstempel unterstützen \_ \_ , speichern einen aktualisierten Zeitstempel mit der Anforderer. Dieses Sicherungs Schema kann als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden.

    Zum Wiederherstellen einer vollständigen Sicherung ist nur ein einzelnes Sicherungs Abbild erforderlich.

-   Copy Backup (VSS \_ b \_ Copy) – wie das Schema der \_ vollständigen VSS- \_ Sicherung gibt an, dass ein Writer eine Sicherung unterstützt, in der alle Dateien unabhängig vom Zeitpunkt der letzten Sicherung gesichert werden. Der Sicherungs Verlauf der einzelnen Dateien wird jedoch nicht von Anforderer oder Writer aktualisiert, und diese Art der Sicherung kann nicht als Grundlage für eine inkrementelle oder differenzielle Sicherung verwendet werden.
-   Protokolldatei (VSS \_ - \_ Protokolldatei) – nur die Protokolldateien eines Writers müssen gesichert werden. Hierfür ist es erforderlich, dass ein Writer mindestens eine Datei zu mindestens einer Komponente mithilfe der [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) -Methode hinzugefügt hat. Dieser Sicherungstyp ist spezifisch für VSS.
-   Benutzerdefinierte Wiederherstellungs Speicherorte (VSS- \_ \_ Writer \_ unterstützt \_ neues \_ Ziel) – gibt an, dass die Writer-Unterstützung für eine anfordernde Person, die die Dateien wiederherstellt, bei der Wiederherstellung geändert Dies bedeutet, dass ein Writer so codiert wurde, dass er eine solche Verschiebung prüft (mithilfe von [**IVssComponent:: getnewtarget**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getnewtarget)) und über die Kapazität zum Arbeiten mit verschobenen Dateien verfügt.
-   Restore with Move (VSS \_ b \_ Writer \_ unterstützt \_ Restore \_ with \_ Move) – gibt an, dass der Writer das Ausführen mehrerer Writer-Instanzen mit derselben Klassen-ID unterstützt und dass eine Anforderer unterstützt, dass eine Komponente zum Zeitpunkt der Wiederherstellung in eine andere Writer-Instanz verschoben wird. Die Writer-Instanz wird mithilfe eines permanenten Writer-Instanznamens angegeben, der als *wszschreiterinstancename* -Parameter an die [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) -Methode übergeben wurde. Ein Anforderer kann den Writer-Instanznamen mithilfe von " [**IVssExamineWriterMetadataEx:: getidentityex**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadataex-getidentityex) " abrufen und die Komponenten während der Wiederherstellung mithilfe von [**ivssbackupcomponentsex:: setselectedforrestoreex**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex-setselectedforrestoreex)verschieben.

    **Windows Server 2003 und Windows XP:** Dieser Wert wird bis Windows Server 2003 mit Service Pack 1 (SP1) nicht unterstützt.

-   Inkrementell \_ ( \_ inkrementell) – gibt an, dass der Writer die VSS-API verwendet, um der anfordernden Person zu helfen, sicherzustellen, dass nur Dateien, die seit der letzten vollständigen oder inkrementellen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert

    Zum Wiederherstellen einer inkrementellen Sicherung sind das ursprüngliche Sicherungs Abbild und alle inkrementellen Sicherungs Abbilder seit der ersten Sicherung

-   Differenziell (VSS- \_ b- \_ differenziell) – gibt an, dass der Writer die VSS-API verwendet, um dem Anforderer zu helfen, sicherzustellen, dass nur Dateien, die seit der letzten vollständigen Sicherung geändert oder hinzugefügt wurden, auf ein Speichermedium kopiert werden. alle zwischen Sicherungs Informationen werden ignoriert.

    Zum Wiederherstellen einer differenziellen Sicherung sind das ursprüngliche Sicherungs Image und das letzte differenzielle Sicherungs Abbild erforderlich, das seit der letzten vollständigen Sicherung erstellt wurde.

-   Inkrementell/differenziell: Zeitstempel Unterstützung (VSS-SB-Zeitstempel \_ \_ ) – gibt an, dass ein Writer die Verwendung des VSS-Zeitstempel Mechanismus zum Einschließen von Dateien in inkrementelle oder differenzielle Operationen Bei der Sicherung muss der Writer den Sicherungs Stempel eines [*Datei Satzes*](vssgloss-f.md) mit der [**IVssComponent:: setbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-setbackupstamp) -Methode speichern und bei der Wiederherstellung mit [**IVssComponent:: getpreviousbackupstamp**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-getpreviousbackupstamp)abrufen.
-   Inkrementell/differenziell: Zeit der letzten Änderungs Unterstützung (VSS- \_ \_ bletzte-Änderung \_ ) – gibt an, dass ein Writer bei der Implementierung von inkrementellen oder differenziellen Sicherungen mit differenzierten Dateien die Informationen zur letzten Änderungszeit unabhängig Diese Informationen können einem Anforderer über die [**IVssComponent:: AddDifferencedFilesByLastModifyTime**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscomponent-adddifferencedfilesbylastmodifytime) -Methode bereitgestellt werden.
-   Inkrementell/differenziell: Unterstützungs Beschränkung ( \_ \_ exklusive \_ inkrementelle VSS-Daten \_ ) – gibt die Schreibunterstützung sowohl für differenzielle als auch für inkrementelle Sicherungs Schemas an
-   Unabhängiger Systemstatus (VSS \_ BS \_ Independent \_ System \_ State) – gibt an, dass der Writer das Sichern von Daten unterstützt, die Teil des Systemstatus sind, aber auch unabhängig vom Systemstatus gesichert werden können.

    **Windows Server 2003 und Windows XP:** Dieser Wert wird bis Windows Vista nicht unterstützt.

-   Roll-Forward Restore (VSS-BVSS- \_ \_ rollforwardwiederherstellung \_ ) – gibt an, dass der Writer eine anfordernde Person unterstützt, die einen Roll Forward-Wiederherstellungspunkt mithilfe von " [**IVssBackupComponentsEx2::**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrollforward)*"

    **Windows Server 2003 und Windows XP:** Dieser Wert wird bis Windows Vista nicht unterstützt.

-   Restore Rename (VSS \_ SB \_ Restore \_ Rename) – gibt an, dass der Writer eine anfordernde Person unterstützt, die einen Wiederherstellungs Namen mithilfe von [**IVssBackupComponentsEx2:: Setup StoreName**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setrestorename)festlegt.

    **Windows Server 2003 und Windows XP:** Dieser Wert wird bis Windows Vista nicht unterstützt.

-   Autoritative Wiederherstellung (autorisierende VSS-Speicher- \_ \_ \_ Wiederherstellung) – gibt an, dass der Writer eine anfordernde Person unterstützt, die eine autorisierende Wiederherstellung mithilfe von [**IVssBackupComponentsEx2:: setautorität**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssbackupcomponentsex2-setauthoritativerestore)-

Writer legen ihre Schemas mithilfe der [**ivsscreatewritermetadata:: setbackupschema**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setbackupschema) -Methode fest, und ein Anforderer erhält das Schema jedes Writers durch Aufrufen von [**ivssexaminewritermetadata:: getbackupschema**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getbackupschema).

 

 



