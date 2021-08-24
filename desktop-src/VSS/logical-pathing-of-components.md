---
description: Logisches Pfading wird verwendet, um komponenten, die von einem Writer verwaltet werden, in klar definierte Gruppen zu organisieren.
ms.assetid: 663c8ca9-8f5b-48bd-af2d-b2d90de9e492
title: Logisches Pfadieren von Komponenten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2ce4feeeb2147a7be736547eb69cbbb1a254c5940b18e904bc3be3290a2c79b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767750"
---
# <a name="logical-pathing-of-components"></a>Logisches Pfadieren von Komponenten

[*Logisches Pfading*](vssgloss-l.md) wird verwendet, um komponenten, die von einem Writer verwaltet werden, in klar definierte Gruppen zu organisieren.

Der logische Pfad entspricht in der Struktur dem herkömmlichen Dateipfad, indem der schräge Schrägstrich " " verwendet wird, um Elemente \\ im Pfad zu trennen. Im Gegensatz zu Dateipfaden ist der Stamm eines logischen Pfads **NULL** anstelle von " \\ ".

Der logische Pfad wird als mit **NULL** beendete Zeichenfolge ausgedrückt, und es gibt keine anderen Einschränkungen für die Zeichen, die der Pfad enthalten kann.

Die wichtigste Verwendung der logischen Pfadierung ist das Definieren von [*Komponentensätzen,*](vssgloss-c.md)wobei der explizite Komponenteneinschluss [*in*](vssgloss-e.md) einen Sicherungs- oder Wiederherstellungsvorgang einer auswählbaren Komponente die Einbeziehung einer Reihe anderer Komponenten (Unterkomponente)[*erfordert.*](vssgloss-s.md) Der logische Pfad der definierenden Komponente eines Komponentensets ist den logischen Pfaden seiner Unterkomponenten über- und:

-   Unterkomponenten müssen den logischen Pfad der auswählbaren Komponente, die den Komponentensatz definiert, als Stammpfad gemeinsam verwenden.
-   Der Stammpfad **NULL ist** gültig.
-   Der Name der definierenden auswählbaren Komponente muss das erste logische Pfadelement nach dem Stammpfad für jede nicht auswählbare Unterkomponente des Komponentensets sein.
-   Komponentensätze können geschachtelt werden.
-   Die Kombination aus logischem Pfad und Komponentenname muss für alle Instanzen einer Writerklasse [*eindeutig sein.*](vssgloss-w.md)

Das hypothetische Beispiel für einen Writer *MyWriter* mit einer unten definierten logischen Pfadstruktur veranschaulicht das logische Pfading.



| Komponentenname | Logischer Pfad            | Für die Sicherung auswählbar |
|----------------|-------------------------|-----------------------|
| "Ausführbare Dateien"  | ""                      | N                     |
| "ConfigFiles"  | "Ausführbare Dateien"           | N                     |
| "LicenseInfo"  | ""                      | J                     |
| "Security"     | ""                      | J                     |
| "UserInfo"     | "Security"              | N                     |
| "Zertifikate" | "Security"              | N                     |
| "writerData"   | ""                      | J                     |
| "Set1"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set1"      | N                     |
| "Dec"          | "writerData \\ Set1"      | N                     |
| "Set2"         | "writerData"            | N                     |
| "Jan"          | "writerData \\ Set2"      | N                     |
| "Dec"          | "writerData \\ Set2"      | N                     |
| "Abfrage"        | "writerData \\ QueryLogs" | N                     |
| "Nutzung"        | "writerData"            | J                     |
| "Jan"          | "writerData \\ Usage"     | N                     |
| "Dec"          | "writerData \\ Usage"     | N                     |



 

Beachten Sie, dass die Komponenten "Executables" und "ConfigFile" über eine über- und untergeordnete Beziehung verfügen, aber beide nicht ausgewählt werden können. Daher bilden sie keinen Komponentensatz. Wenn der *Writer MyWriter* sichern oder wiederhergestellt wird, müssen diese beiden Komponenten explizit [*in*](vssgloss-e.md) den Vorgang eingeschlossen werden.

Die Komponente "LicenseInfo" kann weder mit Vorgänger noch mit Nachfolger ausgewählt werden. Sie kann explizit in einen Sicherungs- oder Wiederherstellungsvorgang eingeschlossen oder nicht in den Ermessen des Anfordernden eingeschlossen werden.

Die Komponente "Sicherheit" definiert einen einfachen Komponentensatz, der keine Komponentensätze darunter enthält.

Die Komponente "writerData" definiert einen Komponentensatz, der eine komplexe Auflistung von Komponenten mit mehreren klar definierten logischen Pfadhierarchien darunter enthält.

Eine Unterkomponente, "Usage", ist auswählbar und definiert einen Komponentensatz.

Mehrere Komponenten haben denselben Namen und werden durch ihre logischen Pfade unterschieden. Instanzen der nicht auswählbaren Komponenten "Dec" und "Jan" sind unter den nicht auswählbaren Komponenten "Set1" und "Set2" und unter der auswählbaren Unterkomponenten "Usage" vorhanden.

Wenn die Komponente "writerData" explizit in einer Sicherung oder Wiederherstellung enthalten ist, werden alle ihre Unterkomponenten – auch diejenigen [](vssgloss-e.md)in der geschachtelten Komponente, die durch "Usage" definiert ist – implizit [*in*](vssgloss-i.md) den Vorgang eingeschlossen.

Wenn der von "writerData" definierte Komponentensatz nicht explizit in einer Sicherung oder Wiederherstellung enthalten ist, werden die Komponenten "Set1", "Set2" und "QueryLogs" (und ihre Instanzen der Unterkomponenten "Dec" und "Jan") nicht implizit in den Sicherungs- oder Wiederherstellungsvorgang einbezogen.

Auch wenn "writerData" nicht im Vorgang enthalten ist, ist die Komponente "Usage" weiterhin auswählbar und kann weiterhin explizit in einen Sicherungs- oder Wiederherstellungsvorgang eingeschlossen werden. Wenn ja, werden die Unterkomponenten "Jan" und "Dec" implizit eingeschlossen.

Weitere Punkte, die zu beachten sind:

-   Die auswählbaren Komponenten "LicenseInfo" und "writerData" und die nicht auswählbare Komponente "Executables" befinden sich alle auf derselben Ebene in der logischen Pfadhierarchie von *MyWriter:* Alle haben den gleichen logischen Pfad von **NULL** oder "", dem logischen Stammpfad.
-   Die auswählbare Komponente "Usage" sollte nie explizit in eine Sicherung eingeschlossen werden, wenn das auswählbare übergeordnete Element ("writerData") explizit in einen Sicherungs- oder Wiederherstellungsvorgang eingeschlossen ist.
-   Komponenten, die Komponentensätze definieren, können einfach aus organisatorischen Gründen vorhanden sein. Beispielsweise kann entweder die Komponente "writerData" oder die Komponente "Usage" oder beides leer sein. Das bedeutet, [](vssgloss-f.md) dass ihnen keine Dateisätze mithilfe der [**IVssCreateWriterMetadata::AddFilesToFileGroup-,**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-addfilestofilegroup) [**IVssCreateWriterMetadata::AddDatabaseFiles-**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabasefiles) oder [**IVssCreateWriterMetadata::AddDatabaseLogFiles-Methode**](/windows/desktop/api/VsWriter/nf-vswriter-ivsscreatewritermetadata-adddatabaselogfiles) hinzugefügt wurden. Die Komponenten definieren weiterhin einen Komponentensatz.

 

 



