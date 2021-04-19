---
description: Logischer Pfad wird verwendet, um die von einem Writer verwalteten Komponenten in klar definierte Gruppen zu organisieren.
ms.assetid: 663c8ca9-8f5b-48bd-af2d-b2d90de9e492
title: Logische Komponente von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9a591f3eec0e00257740dbbd24ab7c609c53c27a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106349786"
---
# <a name="logical-pathing-of-components"></a>Logische Komponente von Komponenten

[*Logischer*](vssgloss-l.md) Pfad wird verwendet, um die von einem Writer verwalteten Komponenten in klar definierte Gruppen zu organisieren.

Der logische Pfad ist analog zur Struktur mit herkömmlichem Dateipfad und verwendet den umgekehrten Schrägstrich " \\ ", um Elemente im Pfad zu trennen. Anders als bei Dateipfaden ist der Stamm eines logischen Pfades **null**, anstelle von " \\ ".

Der logische Pfad wird als **null**-terminierte Zeichenfolge ausgedrückt, und die Zeichen, die der Pfad enthalten kann, haben keine weiteren Einschränkungen.

Die wichtigste Verwendung von logischem Pfad ist das Definieren von [*Komponenten Sätzen*](vssgloss-c.md), bei denen die [*explizite Komponenten Einbindung*](vssgloss-e.md) in einen Sicherungs-oder Wiederherstellungs Vorgang einer auswählbaren Komponente die Einbeziehung einer Reihe anderer Komponenten ([*Unterkomponente*](vssgloss-s.md)) erfordert. Der logische Pfad der definierenden Komponente eines Komponenten Satzes ist ein übergeordnetes Element der logischen Pfade der zugehörigen unter Komponenten und:

-   Unter Komponenten müssen als Stammpfad den logischen Pfad der auswählbaren Komponente freigeben, die den Komponenten Satz definiert.
-   Ein Stammpfad von **null** ist gültig.
-   Der Name der definierenden auswählbaren Komponente muss das erste logische Pfad Element hinter dem Stammpfad für jede nicht auswählbare Unterkomponente des Komponenten Satzes sein.
-   Komponenten Sätze können eingebettet werden.
-   Die Kombination aus logischem Pfad und Komponenten Name muss in allen Instanzen einer [*Writer-Klasse*](vssgloss-w.md)eindeutig sein.

Das hypothetische Beispiel eines Writers *myWriter* mit einer logischen Pfad Struktur, die unten definiert ist, veranschaulicht logische Pfade.



| Komponentenname | Logischer Pfad            | Für Sicherung auswählbar |
|----------------|-------------------------|-----------------------|
| Ausführbare Dateien  | ""                      | N                     |
| "Configfiles"  | Ausführbare Dateien           | N                     |
| "Licenseingefo"  | ""                      | J                     |
| "Security"     | ""                      | J                     |
| UserInfo     | "Security"              | N                     |
| Abschluss | "Security"              | N                     |
| "beschreibdaten"   | ""                      | J                     |
| Set1         | "beschreibdaten"            | N                     |
| Jan          | "Schreibdaten \\ set1"      | N                     |
| 31.12.2012          | "Schreibdaten \\ set1"      | N                     |
| Set2         | "beschreibdaten"            | N                     |
| Jan          | "Schreibdaten \\ set2"      | N                     |
| 31.12.2012          | "Schreibdaten \\ set2"      | N                     |
| Such        | "Write Data \\ querylogs" | N                     |
| Ungs        | "beschreibdaten"            | J                     |
| Jan          | "Verwendung von" Schreib Daten \\ "     | N                     |
| 31.12.2012          | "Verwendung von" Schreib Daten \\ "     | N                     |



 

Beachten Sie, dass die Komponenten "Executables" und "configfile" über eine über-/Unterordnungsbeziehung verfügen, beide jedoch nicht auswählbar sind. Daher bilden Sie keinen Komponenten Satz. Jedes Mal, wenn der Writer *myWriter* gesichert oder wieder hergestellt wird, müssen diese beiden Komponenten [*explizit*](vssgloss-e.md) in den Vorgang eingeschlossen werden.

Die%% amp; quot; licenseingefo-Komponente ist weder für Vorgänger noch als Nachfolger ausgewählt. Sie kann in einem Sicherungs-oder Wiederherstellungs Vorgang in einem Sicherungs-oder Wiederherstellungs Vorgang nach dem Ermessen des Anforderers explizit eingeschlossen werden.

Die Komponente "Sicherheit" definiert einen einfachen Komponenten Satz, der keine Komponenten Gruppen enthält.

Die Komponente "Beschreibungsdaten" definiert einen Komponenten Satz, der eine komplexe Auflistung von Komponenten mit mehreren wohl definierten logischen Pfad Hierarchien darunter enthält.

Eine Unterkomponente, "Usage", ist auswählbar und definiert einen Komponenten Satz.

Mehrere Komponenten haben denselben Namen und werden durch ihre logischen Pfade unterschieden. Instanzen der nicht auswählbaren Komponenten "Dec" und "Jan" sind unter den Komponenten nicht auswählbare Komponenten "set1" und "set2" und unter der auswählbaren Unterkomponente "Usage" vorhanden.

Wenn die Komponente "schreibdata" explizit in eine Sicherung oder Wiederherstellung eingeschlossen wird, werden alle zugehörigen unter Komponenten – auch diejenigen in dem durch "Verwendung" definierten durch "Verwendung" [*– implizit implizit*](vssgloss-e.md)[*in den Vorgang eingeschlossen.*](vssgloss-i.md)

Wenn der durch "Write Data" definierte Komponenten Satz nicht explizit in eine Sicherung oder Wiederherstellung eingeschlossen wird, werden die Komponenten "set1", "set2" und "querylogs" (und Ihre Instanzen der unter Komponenten "Dec" und "Jan") nicht implizit in den Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen.

Auch wenn "Write Data" nicht im Vorgang enthalten ist, ist die Komponente "Usage" weiterhin auswählbar und kann weiterhin explizit in einen Sicherungs-oder Wiederherstellungs Vorgang eingeschlossen werden. Wenn dies der Fall ist, werden die zugehörigen unter Komponenten "Jan" und "Dec" implizit eingeschlossen.

Andere Punkte, die beachtet werden sollten:

-   Die auswählbaren Komponenten "LicenseInfo" und "Write Data" und die nicht auswählbare Komponente "Executables" befinden sich auf derselben Ebene in der logischen Pfad Hierarchie von *myWriter*: alle haben denselben logischen Pfad von **null** oder "", dem logischen Stamm Pfad.
-   Die auswählbare Komponente "Usage" sollte nie explizit in eine Sicherung eingeschlossen werden, wenn Ihr auswählbares übergeordnetes Element ("Write Data") explizit in einem Sicherungs-oder Wiederherstellungs Vorgang enthalten ist.
-   Komponenten, die Komponenten Sätze definieren, können einfach aus organisatorischen Gründen vorhanden sein. Beispielsweise kann entweder die "Write Data"-oder "Usage"-Komponente oder beides leer sein. Das heißt, dass keinen [*Datei Satz*](vssgloss-f.md) mithilfe der [**ivssdeateschreitermetadata:: addfilestofilegroup**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup)-, [**ivsskreateschreitermetadata:: adddatabasefiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) -Methode oder der [**ivsskreateschreitermetadata:: adddatabaselogfiles**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) -Methode hinzugefügt wurden. Die Komponenten definieren weiterhin einen Komponenten Satz.

 

 



