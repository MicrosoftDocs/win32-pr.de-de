---
description: Wichtig für die Organisation der zu sichernden oder wiederherzustellenden Dateien ist das Konzept einer Komponente.
ms.assetid: 5f85bd0e-31bb-45aa-af7c-15299ed31b26
title: VSS-Metadatenkomponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c913262158d59a69de21a6e0d49e31979c1a0cae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106372823"
---
# <a name="vss-metadata-components"></a>VSS-Metadatenkomponenten

Wichtig für die Organisation der zu sichernden oder wiederherzustellenden Dateien ist das Konzept einer [*Komponente*](vssgloss-c.md).

Mit-Komponenten kann ein Writer einem Sicherungs Modul zeigen, wie seine Dateien organisiert werden sollen, Abhängigkeiten zwischen Dateien und welchen Datentyp diese Dateien enthalten können. Dadurch kann eine Sicherungs-Engine entscheiden, wie Dateien für maximale Effizienz gespeichert werden sollen.

Außerdem verwenden VSS-basierte Anwendungen Komponenten als Bausteine für Ihre Metadaten und das Medium für die Kommunikation zwischen Writer und Anforderer.

Writer und Anforderer speichert Informationen zu Komponenten separat – im Writer-Metadatendokument und in den Sicherungs Komponenten Dokumenten bzw. –, und die Informationen unterscheiden sich in den einzelnen Darstellungen.

Zu den Komponenten Informationen in Writer-Metadatendokumenten zählen die folgenden:

-   Informationen aus nur einem Writer in jedem Dokument
-   Alle diese Writer-Komponenten, unabhängig davon, ob Sie [*explizit eingeschlossen*](vssgloss-e.md) werden können oder [*implizit*](vssgloss-i.md) in einen Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen werden müssen
-   [*Logische Pfad*](vssgloss-l.md) Informationen, die verwendet werden, um eine wählbare für Sicherungs Komponente mit bestimmten nicht auswählbaren Sicherungs Komponenten zuzuordnen und so einen Komponenten Satz zu bilden.
-   Die [*Datei Satz*](vssgloss-f.md) Informationen – Pfad, Datei Angabe und Rekursions Flag – werden für jede Komponente verwaltet.

Writer-Metadatendokumente enthalten außerdem Metadateninformationen auf Schreib Ebene, z. b. Wiederherstellungsmethoden und Alternative Speicherort Zuordnungen für die Wiederherstellung. Writer-Metadatendokumente sind schreibgeschützt. Die Schnittstelle zur Untersuchung dieser Informationen ist [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent).

Die Komponenten Informationen in den Dokumenten der Sicherungs Komponenten umfassen Folgendes:

-   Nur Informationen zu explizit enthaltenen Komponenten
-   Metadateninformationen auf Writer-Ebene, z. b. Alternative Speicherort Zuordnungen und Wiederherstellung
-   Zustandsinformationen, die einen Sicherungs-oder Wiederherstellungs Vorgang beschreiben

Sicherungs Komponenten Dokumente enthalten keine Informationen über die [*Dateigruppen*](vssgloss-f.md)der Komponenten. Sicherungs Komponenten Dokumente sind nicht schreibgeschützt und können vom Writer geändert werden. Die Schnittstelle für den Zugriff auf diese Informationen ist [**IVssComponent**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscomponent).

Der Lebenszyklus und die Beziehung zwischen den beiden Ausdrücken einer Komponente können wie folgt interpretiert werden:

-   Writer sind für die anfänglichen Definitionen von Komponenten verantwortlich.
-   Ein Anforderer überprüft die Metadaten aller Writer und deren Komponenten.
-   Aus der selekabilität und den logischen Pfadinformationen der Komponenten bestimmt ein Anforderer, welche Komponenten explizit eingeschlossen werden müssen. diese sind möglicherweise explizit eingeschlossen, wodurch Komponenten Sätze definiert werden und die Mitglieder von Komponenten Sätzen sind.
-   Ein Anforderer fügt die Komponenten hinzu, die eine explizite Einbindung erfordern, und umfasst implizit unter Komponenten in [*Komponenten Sätze*](/windows) (deren Informationen sich nicht im Dokument mit den Sicherungs Komponenten befinden).
-   Bei der Ereignis Behandlung können Writer und Anforderer die im Dokument der Sicherungs Komponenten gespeicherten Komponenten Informationen ändern und untersuchen, um deren Aktivität zu koordinieren.

Zum ordnungsgemäßen Ausführen von Sicherungs-und Wiederherstellungs Vorgängen sind sowohl die Writer-als auch die RequestVersion-Komponenten Informationen erforderlich, und beide müssen mit allen gesicherten Daten gespeichert werden:

-   [Komponenten Typen](component-types.md)
-   [Definition von Komponenten durch Writer](definition-of-components-by-writers.md)
-   [Verwendung von Komponenten durch den Anforderer](use-of-components-by-the-requestor.md)

 

 
