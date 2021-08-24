---
description: 'Das Writer Metadata Document enthält drei Sätze von Daten: Informationen zur Identifizierung und Klassifizierung von Writern, Spezifikationen auf Writerebene und Komponentendaten.'
ms.assetid: 1a84790a-8f46-4e1b-8e45-5036830e8fee
title: Inhalt des Writermetadatendokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fbdb8cf4c2313d17cfd9059626f97356f27ba9168f9e19e4a796fae8797728d5
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119905050"
---
# <a name="writer-metadata-document-contents"></a>Inhalt des Writermetadatendokuments

Das Writer Metadata Document enthält drei Sätze von Daten: Informationen zur Identifizierung und Klassifizierung von Writern, Spezifikationen auf Writerebene und Komponentendaten.

## <a name="writer-identification-information"></a>Writer Identification Information (Informationen, die den Writer identifizieren)

Die Schreiberidentifikations- und Klassifizierungsinformationen umfassen Folgendes:

-   Writername
-   [*Writer-Klassen-ID*](vssgloss-w.md)
-   [*Writer-Instanz*](vssgloss-w.md)
-   Wie die vom Writer verwalteten Daten auf dem Hostsystem verwendet werden (siehe [**VSS \_ USAGE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Der Typ der vom Writer verwalteten Daten (siehe [**VSS \_ SOURCE \_ TYPE**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Mit Ausnahme der Writer-Instanz, die eindeutig ist und vom System generiert wird, wenn ein [**CVssWriter-Objekt**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) initialisiert wird, werden alle diese Werte von einem Writer festgelegt, wenn sie [**CVssWriter::Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) aufruft, und stehen einem Anfordernden durch Aufrufen von [**IVssExkatWriterMetadata::GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity)zur Verfügung.

Da die Writerinstanz eindeutig generiert wird, ist eine gespeicherte Writerinstanz, die aus einem gespeicherten Writer-Metadatendokument abgerufen wird, wahrscheinlich nicht nützlich.

Durch Überprüfen [**des VSS-VERWENDUNGSTYPs \_ \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)kann eine Anwendung bestimmen, ob ein Writer allgemeine Anwendungsdaten verwalten oder ob die Dateien, mit der sie arbeitet, Teil des Systemstartstatus sind oder von einem Systemdienst verwendet werden. Beim Sichern und Wiederherstellen von Anwendungen müssen Nutzungstypen beachtet werden, um die Systemstabilität zu gewährleisten.

Das [**VSS \_ SOURCE \_ TYPE-Flag**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type) gibt an, welche Art von Anwendung der Writer, der die zu sichernden Daten verwalten soll, während des normalen Betriebs ausführt.

Derzeit ist der Unterschied auf die Angabe beschränkt, ob der Writer Dateien im Rahmen transaktionaler oder nicht transaktionaler Datenbankvorgänge erzeugt oder ob die Dateien das Ergebnis eines allgemeineren Aktivitätstyps sind. Diese Liste kann im Laufe der Zeit zunehmen. Diese Informationen können nützlich sein, um die normale Aktivitätsebene zu bestimmen, die in den Dateien eines Writers erwartet wird.

## <a name="writer-level-specification"></a>Writer-Level Spezifikation

Spezifikationen auf Writer-Ebene enthalten Informationen, die in ihrem Bereich writerweit sind und auf alle Daten anwenden, unabhängig davon, welche Komponente sie verwaltet.

Ein Writer muss immer [*Wiederherstellungsmethoden angeben.*](vssgloss-r.md)

Optional kann Folgendes angegeben werden:

-   Liste "Datei ausschließen"
-   [*Zuordnungen alternativer Speicherorte für*](vssgloss-a.md) die Wiederherstellung

Die Include- und Exclude-Dateilisten enthalten Dateiinformationen, die über die in den Komponenten hinausgehen, und ihre Spezifikation ersetzt die Komponentenspezifikation.

## <a name="restore-method-specification"></a>Spezifikation der Wiederherstellungsmethode

Die [*Wiederherstellungsmethode*](vssgloss-r.md) wird im Writer-Metadatendokument von [**IVssCreateWriterMetadata::SetRestoreMethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) festgelegt und von einem Anfinger mit [**IVssExerklärWriterMetadata::GetRestoreMethod abgerufen.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)

Beim Festlegen einer Wiederherstellungsmethode gibt ein Writer für alle dateien, die von einem Writer verwaltet werden, die bevorzugte Art der Dateiwiederherstellung an, die auch als ursprüngliches Wiederherstellungsziel bezeichnet wird. Die Wiederherstellungsmethode gibt beispielsweise an, ob alle dateien, die von einem Writer verwaltet werden, Dateien, die derzeit auf dem Datenträger gespeichert sind, überschreiben dürfen. (Weitere Informationen finden Sie unter [VSS-Wiederherstellungskonfigurationen](vss-restore-configurations.md) und [**VSS \_ RESTOREMETHOD \_ ENUM.)**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum)

## <a name="exclude-file-list-specification"></a>Spezifikation der Ausschlussdateiliste

Die Ausschlussliste ermöglicht die Feinabstimmung von Platzhalterspezifikationen in Komponenten, indem explizit verhindert wird, dass bestimmte Dateien in einen Sicherungssatz eingeschlossen werden.

Eine Komponente kann z. B. über einen [*Dateisatz*](vssgloss-f.md) verfügen, der die Dateispezifikation c: \\ Database \\ \* . \* Obwohl dies eine praktische Definition ist, werden gelegentlich temporäre Dateien generiert (möglicherweise im TMP-Formular), und der Writer möchte deren Sicherung \* immer verhindern.

In diesem Fall würde ein Writer \* .tmp mithilfe von [**IVssCreateWriterMetadata::AddExcludeFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles)zu seiner Ausschlussliste hinzufügen. Diese Spezifikation kann rekursiv sein.

Ein Anfrager würde diese Informationen mithilfe von [**IVssExerklärwriterMetadata::GetExcludeFile abfragen.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)

Die Ausschlussdateiliste hat Vorrang vor Komponentendateienlisten.

Daher besteht die Liste der dateien, die für die Sicherung in [](vssgloss-e.md) einem Writer-Metadatendokument [](vssgloss-i.md) angegeben sind, aus allen Dateien, die in den explizit eingeschlossenen Komponenten angegeben sind, und den implizit eingeschlossenen Komponenten und nicht aus allen ausgeschlossenen Dateien.

## <a name="alternate-location-mappings-specification"></a>Spezifikation für alternative Speicherortzuordnungen

Alternative Speicherortzuordnungen werden anfänglich während der Erstellung eines Writer-Metadatendokuments festgelegt und geben einen Speicherort auf dem Datenträger an, auf dem Dateien wiederhergestellt werden können, wenn die Wiederherstellung einer Datei am ursprünglichen Speicherort nicht möglich ist.

Die Informationen werden mit [**IVssCreateWriterMetadata::AddAlternateLocationMapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) als auf NULL terminierte Breitzeichenfolge hinzugefügt und von [**IVssExwordWriterMetadata::GetAlternateLocationMapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping)als [**IVssWMFiledesc-Objekt**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) abgerufen.

Obwohl alternative Speicherortzuordnungen mithilfe der Schnittstellen auf Writerebene [**(IVssCreateWriterMetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) und [**IVssExassoWriterMetadata)**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)angegeben und untersucht werden, werden sie als Dateisätze [*angegeben.*](vssgloss-f.md) Der Dateisatz, der zum Angeben einer alternativen Speicherortzuordnung (Pfad, Dateispezifikation und Rekursionsflag) verwendet wird, muss mit einem der Dateisätze übereinstimmen, die bereits einer der Komponenten des Writers hinzugefügt wurden (siehe [Hinzufügen](definition-of-components-by-writers.md)von Dateien zu Komponenten ).

Weitere Informationen finden Sie unter [Nicht standardmäßige Sicherungs- und Wiederherstellungsspeicherorte.](non-default-backup-and-restore-locations.md)

## <a name="component-level-information"></a>Component-Level Information

[*Komponenten*](vssgloss-c.md) sind Sammlungen von Dateien, die zu Sicherungs- und Wiederherstellungszwecken eine logische Einheit bilden. Alle Dateien in einer Komponente (mit Ausnahme der explizit ausgeschlossenen Dateien) müssen als Einheit sichern und wiederhergestellt werden.

Writer fügen Komponenten [**mithilfe von IVssCreateWriterMetadata::AddComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)hinzu und geben dabei die folgenden Komponenteninformationen an:

-   type
-   Name
-   Logischer Pfad (falls noch)
-   Unterstützte Funktion
-   [*Auswählbarkeit*](vssgloss-s.md)
-   Metadaten, die vom Writer während der Wiederherstellung verwendet werden sollen
-   Anzeigen von Informationen
-   Benachrichtigungsinformationen

[*Die Auswählbarkeit*](vssgloss-s.md) der Sicherung und die Auswählbarkeit für die Wiederherstellung sind vollständig voneinander unabhängig, und ein Writer verwendet sie in Verbindung mit logischen Pfaden, um Beziehungen zwischen den verschiedenen von ihm verwalteten Komponenten anzugeben. [](vssgloss-s.md) Writer können angeben, welche Komponenten explizit eingeschlossen werden [*müssen*](vssgloss-e.md) (solche, die möglicherweise explizit im Ermessen eines Anfordernden eingeschlossen werden) und diejenigen, die nur implizit eingeschlossen [*werden können.*](vssgloss-i.md) (Weitere Informationen [finden Sie unter Arbeiten mit Auswählbarkeit und logischen Pfaden.)](working-with-selectability-and-logical-paths.md)

Dateien werden einer bestimmten Komponente entweder mit [**IVssCreateWriterMetadata::AddFilesToFileGroup,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) [**IVssCreateWriterMetadata::AddDatabaseFiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**IVssCreateWriterMetadata::AddDatabaseLogFiles hinzugefügt.**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) (Siehe [Hinzufügen von Dateien zu Komponenten](definition-of-components-by-writers.md).)

Beim Hinzufügen von Dateien zu einer Komponente während der Sicherung muss ein Writer einen Dateisatz (einen Pfad, eine Dateispezifikation und ein Rekursionsflag) angeben, der die zu sichernden Dateien definiert.

Writer können auch einen alternativen [*Pfad für die*](vssgloss-a.md) Sicherung angeben, der nicht mit den zuvor erwähnten alternativen [*Speicherortzuordnungen*](vssgloss-a.md) verwechselt werden sollte. Dieser alternative Pfad gibt einen nicht standardmäßigen Speicherort an, von dem Dateien beim Sichern eines Volumes kopiert werden sollen.

Informationen zu einer bestimmten Komponente im Writer-Metadatendokument können über eine [**IVssWMComponent-Schnittstelle**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) erhalten werden, die von [**IVssExerklärwriterMetadata::GetComponent zurückgegeben wird.**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent)

Die Dateien und Pfade werden in [**IVssWMComponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) als [**IVssWMFiledesc-Objekte zurückgegeben.**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc)

Die Komponenteninformationen eines Writers werden unter [Definition of Components by Writers ausführlich erläutert.](definition-of-components-by-writers.md)

 

 



