---
description: Das Breadcrumb)-Argument unterstützt vollständige Anweisungen der erweiterten Abfrage Syntax (AQS) und ist besonders nützlich, um den Suchbereich zu steuern.
title: Crumb-Argument (die Windows-Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 7d38fff38c14a6b537bde068b92e19cedf53d5d4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104980200"
---
# <a name="crumb-argument-the-windows-shell"></a>Crumb-Argument (die Windows-Shell)

Das `crumb` -Argument unterstützt vollständige Anweisungen der erweiterten Abfrage Syntax (AQS) und ist besonders nützlich, um den Suchbereich zu steuern. Zusätzlich zu den AQS-Anweisungen kann das- `crumb` Argument einen speziellen `location` Parameter für Windows Vista und `kind` -und- `store` Parameter unter Windows XP verwenden, wie weiter unten in diesem Thema beschrieben.

Dieses Thema enthält folgende Abschnitte:

-   [Crumb-Syntax](#crumb-syntax)
    -   [Allgemeine Beispiele](#general-examples)
-   [Verwenden von Breadcrumb) mit Vista (Speicherort)](#using-crumb-with-vista-location)
    -   [Vista-Beispiele](#vista-examples)
    -   [Konstanten für allgemeine Ordner](#constants-for-common-folders)
    -   [Argument Informationen](#argument-information)

## <a name="crumb-syntax"></a>Crumb-Syntax

Die Breadcrumb)-Syntax lautet wie folgt:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



Der <column> Teil ist eine beliebige Eigenschaft im Eigenschaften System, und der <value> "Teil" ist ein gültiger Wert für diese Eigenschaft. Der- <label> Teil ist ein optionaler Alias für die Eigenschaft, die als Benutzeroberflächen Hinweis angezeigt wird.

### <a name="general-examples"></a>Allgemeine Beispiele


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Verwenden von Breadcrumb) mit Vista (Speicherort)

Im Breadcrumb)-Parameter unterstützt Windows Vista vollständige AQS und auch die- `location` Eigenschaft, die über eine spezielle Implementierung verfügt, die nur unter Windows Vista verfügbar ist. Sie können entweder eine AQS-Zeichenfolge oder die- `location` Eigenschaft innerhalb eines einzelnen Breadcrumb)-Parameters verwenden, aber nicht beides. Wenn der Breadcrumb)-Parameter AQS enthält, wird alles andere in diesem Breadcrumb)-Parameter ignoriert.

Mit der- `location` Eigenschaft können Sie einen zu suchenden Pfad angeben. Windows Vista kann den Indexer umgehen und das Verzeichnis direkt durchlaufen, wenn der Speicherort außerhalb des Durchforstungs Bereichs des Indexers liegt. Folglich sind diese Suchvorgänge möglicherweise langsamer als Suchvorgänge, die den Indexer verwenden.

Wenn Sie eine `location` Eigenschaft angeben, werden zwei zusätzliche Parameter unterstützt und optional:



| Parameter | Werte                  | BESCHREIBUNG                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aufnahme | einschließen, ausschließen        | Gibt an, ob die Abfrage Elemente von diesem Pfad einschließen oder ausschließen soll. "Include" ist die Standardeinstellung. Windows Vista unterstützt keine Ausschlüsse ohne Inklusions. (Siehe Beispiel) |
| Rekursion | rekursiv, nicht rekursiv | Gibt an, ob bei der Suche alle Unterordner beginnend mit dem am Speicherort definierten Wert rekursiert werden sollen:<value>. Der Standardwert ist rekursiv.                             |



 

Um einen Bereich für eine Suche mit dem **Search:** -Protokoll zu verwenden, haben Sie je nach Ziel des Bereichs unterschiedliche Optionen.

Ordner auf einem lokalen Computer:

-   Verwenden Sie AQS (Crumb = Ordner: <URL-codierter Pfad>).
-   Use Location-Argument (Crumb = Speicherort: <URL-codierter Pfad>)

Ordner auf einem Remote Computer/Netzwerk:

-   Use Location-Argument (Crumb = Speicherort: <URL-codierter Pfad>)

Ordner, auf den über einen bekannten Universal Naming Convention (UNC)-Protokollhandler zugegriffen wird:

-   Verwenden Sie AQS (Crumb = Store: <UNC protocol handler name> ).
-   Use Location-Argument (Crumb = Speicherort: <URL-codierter Pfad>)

### <a name="vista-examples"></a>Vista-Beispiele


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Im ersten Beispiel wird eine Suche nach "Vacation" gestartet, die an der `shell://Personal` Stelle beginnt (eine besondere Verknüpfung zum Ordner " **eigene** Dateien" des Benutzers), einschließlich dieses Ordners und aller Unterordner. Siehe dazu die folgende Tabelle.

Im zweiten Beispiel wird eine Suche in c:- \\ Bildern ausgeführt, aber nicht in c: \\ Bilder \\ Duplikaten.

Im dritten Beispiel wird eine Suche in C: \\ Documents ausgeführt, die auf Dateien beschränkt ist, deren- `kind` Eigenschaft auf "Fotos" festgelegt ist.

### <a name="constants-for-common-folders"></a>Konstanten für allgemeine Ordner

Windows Vista ermöglicht die Verwendung von CSIDL-Werten, die eine eindeutige, systemunabhängige Möglichkeit zur Identifizierung spezieller Ordner bieten, die häufig von Anwendungen verwendet werden, aber nicht denselben Namen oder Speicherort auf einem beliebigen System haben. Der Systemordner kann z. b. "c: \\ Windows" auf einem System und "c: \\ Winnt" auf einem anderen System sein.

Verwenden Sie diese Speicherorte mit der folgenden Syntax:


```
crumb=location:shell%3a<LocationName>&
```



In der folgenden Tabelle sind die CSIDL-Werte aufgeführt. Weitere Informationen finden Sie unter [**shellspecialfolderconstants**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants) .



| Name                        | Such Zeichenfolge                   | BESCHREIBUNG                                                                                                                                                                            |
|-----------------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Verwaltungs Tools        | Verwaltungs Tools% 20tools          | Dateisystem Verzeichnis, das als Repository für Verwaltungs Tools dient.                                                                                                            |
| APPDATA                     | APPDATA                         | Das Dateisystem Verzeichnis, das als gängiges Repository für anwendungsspezifische Daten fungiert. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ Anwendungsdaten.                      |
| CACHE                       | CACHE                           | Das Dateisystem Verzeichnis, das als gängiges Repository für temporäre Internet Dateien fungiert. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ temporäres Internet Dateien.               |
| CD-brennen                  | CD% 20brennen                    | Ordner, der die Daten enthält, die auf CD gebrannt werden sollen.                                                                                                                                             |
| allgemeine Verwaltungs Tools | Allgemeine %20 administrative% 20tools | Verwaltungs Tools für alle Benutzer.                                                                                                                                                    |
| Allgemeine APPDATA              | Allgemeine% 20appdata                | Anwendungsdaten für alle Benutzer. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ alle Benutzer \\ Anwendungsdaten.                                                                             |
| allgemeiner Desktop              | allgemeiner Desktop                  | Microsoft Windows-Desktop Daten für alle Benutzer. Der virtuelle Ordner, der das Stammverzeichnis des-Namespace ist.                                                                                        |
| Allgemeine Dokumente            | Allgemeine% 20Dokumente              | Dokumente für alle Benutzer. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ alle Benutzer \\ Eigene Dokumente.                                                                                        |
| allgemeine Programme             | Allgemeine% 20programme               | Programm Gruppen, die allen Benutzern gemeinsam sind. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ alle Benutzer \\ Start Menü \\ Programme.                                                                     |
| gemeinsames Startmenü           | Häufiges %20-Start-%20-Menü           | Startmenü Elemente, die allen Benutzern gemeinsam sind. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ alle Benutzer \\ Startmenü.                                                                             |
| gemeinsamer Start              | Gemeinsamer% 20start                | Start Programmgruppe, die allen Benutzern gemeinsam ist.                                                                                                                                             |
| Allgemeine Vorlagen            | Allgemeine% 20vorlagen              | Dokumentvorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                                |
| Commonmusic                 | Meine% 20musik                      | Meine Musik Ordner Vorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                         |
| Commonpictures              | Meine% 20abbildungen                   | Meine Bilder Ordner Vorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                      |
| Commonvideo                 | Mein% 20video                      | Meine Video Ordner Vorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                         |
| ConnectionsFolder           | ConnectionsFolder               | Ordner mit Verbindungsdaten.                                                                                                                                                     |
| Ordner der Systemsteuerung        | ControlPanelFolder              | Virtueller Ordner, der Symbole für die System Steuerungsanwendungen enthält.                                                                                                                    |
| KS                     | KS                         | Das Dateisystem Verzeichnis, das als gängiges Repository für Internet Cookies fungiert. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ Cookies.                                        |
| DESKTOP                     | DESKTOP                         | Microsoft Windows-Desktop. Der virtuelle Ordner, der das Stammverzeichnis des-Namespace ist.                                                                                                           |
| FAVORITEN                   | FAVORITEN                       | Das Dateisystem Verzeichnis, das als gängiges Repository für die bevorzugten Elemente des Benutzers fungiert. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ Favoriten.                             |
| Schrift                       | Schrift                           | Der virtuelle Ordner mit den installierten Schriftarten. Ein typischer Pfad ist C: \\ Windows- \\ Schriftarten.                                                                                                       |
| VERLAUF                     | VERLAUF                         | Dateisystem Verzeichnis, das als gemeinsames Repository für Internet Verlaufs Elemente dient.                                                                                                   |
| Internet Ordner              | Internet Ordner                  | Ordner, der Internet Daten enthält.                                                                                                                                                    |
| lokale APPDATA               | Lokal% 20appdata                 | Dateisystem Verzeichnis, das als Datenrepository für lokale (nicht roamende) Anwendungen fungiert. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ lokale Einstellungen \\ Anwendungsdaten. |
| Localizedresourcedir        | Localizedresourcedir            | Lokalisiertes Ressourcenverzeichnis.                                                                                                                                                          |
| Ordner "MyComputer"            | Ordner "MyComputer"                | Arbeitsplatz. Virtueller Ordner, der alles auf dem lokalen Computer enthält: Speichergeräte, Drucker und Systemsteuerung. Dieser Ordner kann auch zugeordnete Netzwerklaufwerke enthalten.             |
| meine Musik                    | Meine% 20musik                      | Mein Musik Ordner. Ein typischer Pfad ist "C: \\ Dokumente und Einstellungen \\ Benutzername \\ meine eigene Musik" \\ .                                                                                       |
| meine Bilder                 | Meine% 20abbildungen                   | Ordner "eigene Bilder". Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ meine Dokumente meine \\ Bilder.                                                                                 |
| Mein Video                    | Mein% 20video                      | Mein Video Ordner. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ My Documents \\ My Video.                                                                                       |
| Nicht mehr                     | Nicht mehr                         | Der virtuelle Ordner, der den Stamm der Netzwerk-Namespace Hierarchie darstellt.                                                                                                               |
| Ordner "Netzwerk Orte"       | "Networkdplacesfolder"            | Ein Dateisystem Ordner, der die Link Objekte enthält, die möglicherweise im virtuellen Ordner "Mein Netzwerk" vorhanden sind. Es ist nicht identisch mit dem-Element, das den Netzwerk Namespace Stamm darstellt.   |
| OEM-Links                   | OEM-Verbindungen (%20)                     | Ordner mit Links zu OEM-Websites.                                                                                                                                                  |
| PERSONAL                    | PERSONAL                        | Das Dateisystem Verzeichnis, das als gängiges Repository für die Dokumente eines Benutzers fungiert. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ meine Dokumente.                                 |
| Ordner "Drucker"             | Ordner "Drucker"                 | Ein virtueller Ordner, der installierte Drucker enthält.                                                                                                                                          |
| Printhood                   | Printhood                       | Das Dateisystem Verzeichnis, das die Link Objekte enthält, die möglicherweise im virtuellen Ordner Drucker vorhanden sind. Ein typischer Pfad ist C: \\ Documents und Settings \\ username \\ printhood.                 |
| PROGRAMME                    | PROGRAMME                        | Dateisystem Verzeichnis, das die Programm Gruppen des Benutzers (auch Dateisystem Verzeichnisse) enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ Startmenü \\ Programme.  |
| PROFILE                     | PROFILE                         | Der Profilordner des Benutzers.                                                                                                                                                                 |
| Programmdateien               | Programm% 20dateien                 | Ordner "Programme". Ein typischer Pfad ist C: \\ Program Files.                                                                                                                             |
| Allgemeine Programmdateien        | Programfilescommon              | Ordner "Programme", der allen Benutzern gemeinsam ist.                                                                                                                                              |
| Programmdateien Common x86    | PROGRAMFILESCOMMONX86           | Ordner "Programme", der allen Benutzern auf x86-Computern gemeinsam ist.                                                                                                                              |
| Programm FILESx86            | PROGRAMFILESx86                 | Ordner "Programme" auf x86-Computern.                                                                                                                                                  |
| ZULETZT VERWENDET                      | ZULETZT VERWENDET                          | Das Dateisystem Verzeichnis, das die zuletzt verwendeten Dokumente des Benutzers enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ zuletzt.                                           |
| Papierkorb Ordner          | Recyclebinfolder                | Der virtuelle Ordner, der die Objekte im Papierkorb des Benutzers enthält.                                                                                                                       |
| ResourceDir                 | ResourceDir                     | Das Ressourcenverzeichnis.                                                                                                                                                                |
| SENDTO                      | SENDTO                          | Das Dateisystem Verzeichnis, das "an Menü Elemente senden" enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ SendTo.                                                                |
| Startmenü                  | Menü "%20" starten                    | Das Dateisystem Verzeichnis, das Start Menü Elemente enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Benutzername \\ Startmenü.                                                                 |
| Starts                     | Starts                         | Das Dateisystem Verzeichnis, das der Start Programmgruppe des Benutzers entspricht.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | System Ordner auf x86-Computern.                                                                                                                                                         |
| VORLAGEN                   | VORLAGEN                       | Das Dateisystem Verzeichnis, das als gängiges Repository für Dokumentvorlagen fungiert.                                                                                                       |
| SYSTEM                      | SYSTEM                          | System Ordner. Ein typischer Pfad ist C: \\ Windows- \\ System.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Windows-Verzeichnis oder SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Argument Informationen



|                          |                                         |
|--------------------------|-----------------------------------------|
| Mindestens Betriebs System | Windows Vista mit Service Pack 1 (SP1) |



 

 

 



