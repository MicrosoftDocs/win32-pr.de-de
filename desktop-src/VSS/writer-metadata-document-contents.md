---
description: 'Das Writer-Metadatendokument enthält drei Datensätze: Writer-Identifizierungs-und Klassifizierungs Informationen, Spezifikationen auf Writer-Ebene und Komponenten Daten.'
ms.assetid: 1a84790a-8f46-4e1b-8e45-5036830e8fee
title: Inhalt des Writer-Metadatendokuments
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f222977f1c8d785e6f69613f219545dc3402af7f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041740"
---
# <a name="writer-metadata-document-contents"></a>Inhalt des Writer-Metadatendokuments

Das Writer-Metadatendokument enthält drei Datensätze: Writer-Identifizierungs-und Klassifizierungs Informationen, Spezifikationen auf Writer-Ebene und Komponenten Daten.

## <a name="writer-identification-information"></a>Writer Identification Information (Informationen, die den Writer identifizieren)

Die Writer-Identifikations-und-Klassifizierungs Informationen umfassen Folgendes:

-   Writer-Name
-   [*Writer-Klassen-ID*](vssgloss-w.md)
-   [*Writer-Instanz*](vssgloss-w.md)
-   Wie die vom Writer verwalteten Daten auf dem Host System verwendet werden (siehe [**VSS- \_ \_ Verwendungstyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type))
-   Der Typ der vom Writer verwalteten Daten (siehe [**VSS- \_ \_ Quelltyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type))

Mit Ausnahme der Writer-Instanz, die eindeutig ist und vom System generiert wird, wenn ein [**CVssWriter**](/windows/desktop/api/VsWriter/nl-vswriter-cvsswriter) -Objekt initialisiert wird, werden alle diese Werte von einem Writer festgelegt, wenn Sie [**CVssWriter:: Initialize**](/windows/desktop/api/VsWriter/nf-vswriter-cvsswriter-initialize) aufruft und für eine Anforderer durch Aufrufen von [**ivssexamineschreitermetadata:: GetIdentity**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getidentity)aufgerufen werden.

Da die Writer-Instanz eindeutig generiert wird, ist eine gespeicherte Writer-Instanz, die aus einem gespeicherten Writer-Metadatendokument abgerufen wurde, wahrscheinlich nicht nützlich.

Durch das Überprüfen des [**VSS- \_ Verwendungs \_ Typs**](/windows/desktop/api/VsWriter/ne-vswriter-vss_usage_type)kann eine Anwendung ermitteln, ob ein Writer allgemeine Anwendungsdaten verwaltet, oder ob die Dateien, mit denen Sie arbeiten, Teil des Systemstart Zustands sind oder von einem Systemdienst verwendet werden. Sicherungs-und Wiederherstellungs Anwendungen müssen Verwendungs Typen beachten, um die Stabilität des Systems zu gewährleisten.

Das Flag für den [**VSS- \_ \_ Quelltyp**](/windows/desktop/api/VsWriter/ne-vswriter-vss_source_type) gibt an, welche Art von Anwendung der Writer, der die zu sichernden Daten verwaltet, während des normalen Vorgangs ausführt.

Derzeit ist der Unterschied darauf beschränkt, anzugeben, ob der Writer Dateien als Teil von transaktionalen oder nicht transaktionalen Daten Bank Vorgängen erzeugt oder ob die Dateien das Ergebnis einer allgemeineren Art von Aktivität sind. Diese Liste kann im Laufe der Zeit zunehmen. Diese Informationen können hilfreich sein, um die normale Aktivitätsstufe zu ermitteln, die in den Dateien eines Writers erwartet wird.

## <a name="writer-level-specification"></a>Writer-Level Spezifikation

Spezifikationen auf Writer-Ebene enthalten Informationen, die in Ihrem Bereich Writer-weit sind und auf alle Daten angewendet werden, unabhängig davon, welche Komponente Sie verwaltet.

Ein Writer muss immer [*Restore-Methoden*](vssgloss-r.md)angeben.

Optional können Sie Folgendes angeben:

-   Datei Liste ausschließen
-   [*Alternative Speicherort*](vssgloss-a.md) Zuordnungen für die Wiederherstellung

Die Listen "include" und "Exclude file" enthalten Dateiinformationen, die in den-Komponenten überschritten werden, und ihre Spezifikation ersetzt die Komponenten Spezifikation.

## <a name="restore-method-specification"></a>Restore-Methoden Spezifikation

Die [*Restore-Methode*](vssgloss-r.md) wird im Writer-Metadatendokument von [**ivsskreateschreitermetadata:: setrestoremethod**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-setrestoremethod) festgelegt und von einem Anforderer mit [**ivssexamineschreitermetadata:: getrestoremethod**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getrestoremethod)abgerufen.

Beim Festlegen einer Wiederherstellungsmethode gibt ein Writer die bevorzugte Art der Dateiwiederherstellung (auch als ursprüngliches Wiederherstellungs Ziel bezeichnet) für alle Dateien an, die von einem Writer verwaltet werden. Die Restore-Methode gibt beispielsweise an, ob alle Dateien, die von einem Writer verwaltet werden, Dateien überschreiben dürfen, die derzeit auf dem Datenträger gespeichert sind (Weitere Informationen finden Sie unter [VSS-Wiederherstellungs Konfigurationen](vss-restore-configurations.md) und [**VSS \_ restoremethod \_**](/windows/desktop/api/VsWriter/ne-vswriter-vss_restoremethod_enum) -Aufzählung.)

## <a name="exclude-file-list-specification"></a>Dateilisten Spezifikation ausschließen

Die Ausschlussliste ermöglicht die Feinabstimmung von Platzhalter Spezifikationen in-Komponenten, indem explizit verhindert wird, dass bestimmte Dateien in einem Sicherungs Satz enthalten sind.

Beispielsweise kann eine Komponente über einen [*Dateisatz*](vssgloss-f.md) verfügen, der die Datei Spezifikation "c: Database" enthält. \\ \\ \* \* Obwohl es sich hierbei um eine bequeme Definition handelt, kann es vorkommen, dass gelegentlich temporäre Dateien generiert werden (möglicherweise in der Form \* . tmp) und der Writer die Sicherung immer verhindern möchte.

In diesem Fall würde ein Writer \* . tmp mithilfe von [**ivsskreateschreitermetadata:: addexcludefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addexcludefiles)zu seiner Ausschlussliste hinzufügen. Diese Spezifikation könnte rekursiv sein.

Ein Anforderer würde diese Informationen mithilfe von [**ivssexamineschreitermetadata:: getexcludefile**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getexcludefile)Abfragen.

Die Liste Datei ausschließen hat Vorrang vor Komponenten Dateilisten.

Die Liste der Dateien, die für die Sicherung in einem Writer-Metadatendokument angegeben werden, besteht daher aus allen Dateien, die in den [*explizit enthaltenen*](vssgloss-e.md) Komponenten und den [*implizit enthaltenen*](vssgloss-i.md) Komponenten angegeben sind, weniger alle ausgeschlossenen Dateien.

## <a name="alternate-location-mappings-specification"></a>Spezifikation der Zuordnungen alternativer Orte

Alternative Speicherort Zuordnungen werden anfänglich bei der Erstellung eines Writer-Metadatendokuments festgelegt und geben einen Speicherort auf dem Datenträger an, auf dem Dateien wieder hergestellt werden können, wenn die Wiederherstellung einer Datei am ursprünglichen Speicherort nicht möglich ist.

Die Informationen werden als NULL-terminierte breit Zeichen Zeichenfolgen mit [**ivssdeateschreitermetadata:: addtexelocationmapping**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addalternatelocationmapping) hinzugefügt und durch [**ivssexamineschreibmetadata:: getalternatelocationmapping**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getalternatelocationmapping)als [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Objekt abgerufen.

Trotz der Tatsache, dass alternative Speicherort Zuordnungen angegeben und mithilfe der Schnittstellen auf Writer-Ebene ([**ivsskreateschreitermetadata**](/windows/desktop/api/VsWriter/nl-vswriter-ivsscreatewritermetadata) und [**ivssexaminewrite Metadata**](/windows/desktop/api/VsBackup/nl-vsbackup-ivssexaminewritermetadata)) überprüft werden, werden Sie in Form von [*Datei Sätzen*](vssgloss-f.md)angegeben. Der zum Angeben einer alternativen Speicherort Zuordnung verwendete Dateisatz (Pfad, Datei Angabe und Rekursions Flag) muss mit einem der Datei Sätze identisch sein, die bereits einer der Komponenten des Writers hinzugefügt wurden (siehe [Hinzufügen von Dateien zu Komponenten](definition-of-components-by-writers.md)).

Weitere Informationen finden Sie unter [nicht standardmäßige Sicherungs-und Wiederherstellungs Speicherorte](non-default-backup-and-restore-locations.md).

## <a name="component-level-information"></a>Component-Level Informationen

[*Komponenten*](vssgloss-c.md) sind Sammlungen von Dateien, die eine logische Einheit für die Sicherung und Wiederherstellung bilden. Alle Dateien in einer Komponente (außer den explizit ausgeschlossenen) müssen als Einheit gesichert und wieder hergestellt werden.

Writer fügen mithilfe von [**ivsskreatewritermetadata:: addComponent**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addcomponent)Komponenten hinzu, wobei die folgenden Komponenten Informationen angegeben werden:

-   type
-   Name
-   Logischer Pfad (falls vorhanden)
-   Unterstützte Funktion
-   [*Selektbarkeit*](vssgloss-s.md)
-   Metadaten, die vom Writer während der Wiederherstellung verwendet werden
-   Anzeigeinformationen
-   Benachrichtigungs Informationen

Die [*Auswahlmöglichkeiten für*](vssgloss-s.md) die [*Wiederherstellung*](vssgloss-s.md) von Sicherungs-und Auswahlmöglichkeiten sind vollständig voneinander unabhängig, und ein Writer verwendet diese zusammen mit logischen Pfaden, um die Beziehungen zwischen den verschiedenen verwalteten Komponenten anzugeben. Writer können angeben, welche Komponenten für [*explizit eingeschlossen*](vssgloss-e.md) werden sollen (solche, die möglicherweise explizit in den Ermessen eines Anforderers eingeschlossen werden), und diejenigen, die nur [*implizit eingeschlossen*](vssgloss-i.md)werden können. (Weitere Informationen finden Sie [unter Arbeiten mit selekabilität und logischen Pfaden](working-with-selectability-and-logical-paths.md).)

Dateien werden einer bestimmten Komponente mithilfe von [**ivsskreateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup), [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles)oder [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles)hinzugefügt. (Siehe [Hinzufügen von Dateien zu Komponenten](definition-of-components-by-writers.md).)

Beim Hinzufügen von Dateien zu einer Komponente während der Sicherung muss ein Writer einen Datei Satz angeben (Pfad, Datei Angabe und Rekursions Kennzeichen), der die zu sichernden Dateien definiert.

Writer können auch einen [*alternativen Pfad*](vssgloss-a.md) für die Sicherung angeben, der nicht mit den zuvor erwähnten [*Alternativen Orts*](vssgloss-a.md) Zuordnungen verwechselt werden sollte. Dieser Alternative Pfad gibt einen nicht standardmäßigen Speicherort an, von dem Dateien kopiert werden sollen, wenn ein Volume gesichert wird.

Informationen zu einer bestimmten Komponente im Writer-Metadatendokument können über eine [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) -Schnittstelle abgerufen werden, die von [**ivssexamineschreitermetadata:: getComponent**](/windows/desktop/api/VsBackup/nf-vsbackup-ivssexaminewritermetadata-getcomponent)zurückgegeben wird.

Die Dateien und Pfade werden in [**ivsswmcomponent**](/windows/desktop/api/VsBackup/nl-vsbackup-ivsswmcomponent) als [**ivsswmfiledesc**](/windows/desktop/api/VsWriter/nl-vswriter-ivsswmfiledesc) -Objekte zurückgegeben.

Die Komponenten Informationen eines Writers werden ausführlich in [der Definition von Komponenten durch Writer](definition-of-components-by-writers.md)erläutert.

 

 



