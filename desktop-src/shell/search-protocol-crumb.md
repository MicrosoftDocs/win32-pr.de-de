---
description: Hier erfahren Sie, wie Sie das CRUMB-Argument in der Windows Shell-Benutzeroberfläche verwenden, um den Bereich einer Suche zu steuern.
title: CRUMB-Argument (Die Windows-Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 543bc90647bbe1daed1a3a6d1f7bc54a4713a8ed
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112403603"
---
# <a name="crumb-argument-the-windows-shell"></a>CRUMB-Argument (Die Windows-Shell)

Das `crumb` -Argument unterstützt vollständige AQS-Anweisungen (Advanced Query Syntax) und ist besonders nützlich, um den Bereich einer Suche zu steuern. Zusätzlich zu AQS-Anweisungen kann das -Argument einen speziellen Parameter unter Windows Vista und parameter unter Windows XP verwenden, wie weiter unten `crumb` `location` in diesem Thema `kind` `store` beschrieben.

Dieses Thema enthält folgende Abschnitte:

-   [Crumb-Syntax](#crumb-syntax)
    -   [Allgemeine Beispiele](#general-examples)
-   [Verwenden von Crumb mit Vista (Standort)](#using-crumb-with-vista-location)
    -   [Vista-Beispiele](#vista-examples)
    -   [Konstanten für allgemeine Ordner](#constants-for-common-folders)
    -   [Argumentinformationen](#argument-information)

## <a name="crumb-syntax"></a>Crumb-Syntax

Die Crumb-Syntax lautet wie folgt:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



Der <column> -Teil ist eine beliebige Eigenschaft im Eigenschaftensystem, und <value> portion ist ein gültiger Wert für diese Eigenschaft. Der <label> -Teil ist ein optionaler Alias für die Eigenschaft, die als Benutzeroberflächenhinweis angezeigt wird.

### <a name="general-examples"></a>Allgemeine Beispiele


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Verwenden von Crumb mit Vista (Standort)

Im crumb-Parameter unterstützt Windows Vista die vollständige AQS-Version sowie die -Eigenschaft, die nur unter Windows Vista über eine spezielle Implementierung `location` verfügt. Sie können entweder eine AQS-Zeichenfolge oder die -Eigenschaft innerhalb eines `location` einzelnen crumb-Parameters verwenden, aber nicht beide. Wenn der crumb-Parameter AQS enthält, wird alles andere in diesem crumb-Parameter ignoriert.

Mit `location` der -Eigenschaft können Sie einen zu durchsuchenden Pfad angeben. Windows Vista kann den Indexer umgehen und das Verzeichnis direkt durchlaufen, wenn sich der Speicherort außerhalb des Indexer-Durchforstungsbereichs befindet. Folglich sind diese Suchvorgänge möglicherweise langsamer als Suchvorgänge, die den Indexer verwenden.

Wenn Sie eine Eigenschaft `location` angeben, werden zwei zusätzliche Parameter unterstützt und optional:



| Parameter | Werte                  | Beschreibung                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aufnahme | include, exclude        | Gibt an, ob die Abfrage Elemente in diesen Pfad ein- oder ausschließen soll. "Include" ist die Standardeinstellung. Windows Vista unterstützt keine Ausschlüsse ohne Einschlüsse. (Siehe Beispiel) |
| Rekursion | rekursiv, nicht rekursiv | Gibt an, ob bei der Suche alle Unterordner beginnend mit dem am Speicherort definierten Wert erneut wiederholt werden sollen:<value>. "Rekursiv" ist die Standardeinstellung.                             |



 

Für den Bereich einer Suche mithilfe des **Protokolls search:** stehen Ihnen je nach Ziel des Bereichs unterschiedliche Optionen zur Verfügung.

Ordner auf einem lokalen Computer:

-   Verwenden Sie AQS (crumb=folder:<URL-codierten Pfad>)
-   Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)

Ordner auf einem Remotecomputer/-netzwerk:

-   Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)

Ordner, auf den über einen bekannten UNIVERSAL NAMING CONVENTION(UNC)-Protokollhandler zugegriffen wird:

-   Verwenden Sie AQS (crumb=store: <UNC protocol handler name> ).
-   Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)

### <a name="vista-examples"></a>Vista-Beispiele


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Im ersten Beispiel wird eine Suche nach "Vacation" ausgeführt, die am Speicherort beginnt (eine spezielle Verknüpfung zum Ordner Eigene Dokumente des Benutzers), einschließlich dieses Ordners und aller `shell://Personal` Unterordner.  Siehe dazu die folgende Tabelle.

Im zweiten Beispiel wird eine Suche in C: \\ Bilder ausgeführt, jedoch nicht in C: \\ \\ Bildduplizieren.

Im dritten Beispiel wird eine Suche in C: Dokumente ausgeführt, die auf Dateien beschränkt ist, bei der \\ `kind` die -Eigenschaft auf Pics festgelegt ist.

### <a name="constants-for-common-folders"></a>Konstanten für allgemeine Ordner

Windows Vista ermöglicht die Verwendung von CSIDL-Werten, die eine eindeutige systemunabhängige Möglichkeit bieten, spezielle Ordner zu identifizieren, die häufig von Anwendungen verwendet werden, aber möglicherweise nicht denselben Namen oder Speicherort auf einem bestimmten System haben. Der Systemordner kann beispielsweise "C: Windows" auf einem System und \\ "C: \\ Winnt" auf einem anderen System sein.

Verwenden Sie diese Speicherorte mit dieser Syntax:


```
crumb=location:shell%3a<LocationName>&
```



In der folgenden Tabelle sind die CSIDL-Werte aufgeführt. Weitere Informationen finden Sie unter [**ShellSpecialFolderConstants.**](/windows/desktop/api/Shldisp/ne-shldisp-shellspecialfolderconstants)



| Name                        | Suchzeichenfolge                   | Beschreibung                                                                                                                                                                            |
|-----------------------------|---------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| VERWALTUNGSTOOLS        | ADMINISTRATIVE%20TOOLS          | Dateisystemverzeichnis, das als Repository für Verwaltungstools dient.                                                                                                            |
| APPDATA                     | APPDATA                         | Dateisystemverzeichnis, das als allgemeines Repository für anwendungsspezifische Daten dient. Ein typischer Pfad ist C: Dokumente und Einstellungen Benutzername \\ \\ \\ Anwendungsdaten.                      |
| CACHE                       | CACHE                           | Dateisystemverzeichnis, das als allgemeines Repository für temporäre Internetdateien dient. Ein typischer Pfad ist C: \\ Benutzername für Dokumente und Einstellungen Temporäre \\ \\ Internetdateien.               |
| CD- UND CD-20                  | CD%20 WIE                    | Ordner, der Daten enthält, die auf CD glühen sollen.                                                                                                                                             |
| ALLGEMEINE VERWALTUNGSTOOLS | COMMON%20ADMINISTRATIVE%20TOOLS | Verwaltungstools für alle Benutzer.                                                                                                                                                    |
| ALLGEMEINE APP-DATEN              | COMMON%20APPDATA                | Anwendungsdaten für alle Benutzer. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Alle \\ \\ Benutzeranwendungsdaten.                                                                             |
| COMMON DESKTOP              | COMMON DESKTOP                  | Microsoft Windows Desktop-Daten für alle Benutzer. Virtueller Ordner, der das Stammverzeichnis des Namespaces ist.                                                                                        |
| ALLGEMEINE DOKUMENTE            | COMMON%20DOCUMENTS              | Dokumente für alle Benutzer. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Alle Benutzer \\ \\ Eigene Dokumente.                                                                                        |
| ALLGEMEINE PROGRAMME             | COMMON%20PROGRAMS               | Programmgruppen, die allen Benutzern gemeinsam sind. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Alle Benutzer \\ \\ \\ Startmenüprogramme.                                                                     |
| ALLGEMEINES STARTMENÜ           | COMMON%20START%20MENU           | Startmenü elemente, die allen Benutzern gemeinsam sind. Ein typischer Pfad ist C: \\ Startmenü "Dokumente und \\ Einstellungen für alle \\ Benutzer".                                                                             |
| COMMON STARTUP              | COMMON%20STARTUP                | Startprogrammgruppe, die allen Benutzern gemeinsam ist.                                                                                                                                             |
| ALLGEMEINE VORLAGEN            | COMMON%20TEMPLATES              | Dokumentvorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                                |
| COMMONLÄUFIGKEIT                 | MY%20BIRD                      | Meine Ordnervorlagen für Musik, die allen Benutzern gemeinsam sind.                                                                                                                                         |
| COMMONPICTURES              | MY%20PICTURES                   | Ordnervorlagen "Meine Bilder", die allen Benutzern gemeinsam sind.                                                                                                                                      |
| COMMONVIDEO                 | MY%20VIDEO                      | Meine Videoordnervorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | Ordner, der Verbindungsdaten enthält.                                                                                                                                                     |
| ORDNER "SYSTEMSTEUERUNG"        | CONTROLPANELFOLDER              | Virtueller Ordner mit Symbolen für die Systemsteuerung Anwendungen.                                                                                                                    |
| Cookies                     | Cookies                         | Dateisystemverzeichnis, das als allgemeines Repository für Internetcookies dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ Cookies.                                        |
| DESKTOP                     | DESKTOP                         | Microsoft Windows Desktop. Virtueller Ordner, der das Stammverzeichnis des Namespaces ist.                                                                                                           |
| FAVORITEN                   | FAVORITEN                       | Dateisystemverzeichnis, das als allgemeines Repository für die favoriten Elemente des Benutzers dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ Favoriten.                             |
| Schriftarten                       | Schriftarten                           | Virtueller Ordner, der installierte Schriftarten enthält. Ein typischer Pfad ist C: \\ \\ WINDOWS-Schriftarten.                                                                                                       |
| VERLAUF                     | VERLAUF                         | Dateisystemverzeichnis, das als allgemeines Repository für Internetverlaufselemente dient.                                                                                                   |
| INTERNETFOLDER              | INTERNETFOLDER                  | Ordner, der Internetdaten enthält.                                                                                                                                                    |
| LOKALE APPDATA               | LOCAL%20APPDATA                 | Dateisystemverzeichnis, das als Daten-Repository für lokale Anwendungen (ohne Roaming) dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername Lokale Einstellungen \\ \\ \\ Anwendungsdaten. |
| LOCALIZEDRESOURCEDIR        | LOCALIZEDRESOURCEDIR            | Lokalisiertes Ressourcenverzeichnis.                                                                                                                                                          |
| MYCOMPUTERFOLDER            | MYCOMPUTERFOLDER                | Arbeitsplatz. Virtueller Ordner, der alles auf dem lokalen Computer enthält: Speichergeräte, Drucker und Systemsteuerung. Dieser Ordner kann auch zugeordnete Netzwerklaufwerke enthalten.             |
| MEINE MUSIK                    | MY%20BIRD                      | Ordner "Meine Musik". Ein typischer Pfad ist C: \\ Benutzername für Dokumente und Einstellungen Eigene Dokumente My \\ \\ \\ Music.                                                                                       |
| MEINE BILDER                 | MY%20PICTURES                   | Ordner "Meine Bilder". Ein typischer Pfad ist C: \\ Benutzername für Dokumente und Einstellungen Eigene Dokumente Meine \\ \\ \\ Bilder.                                                                                 |
| MEIN VIDEO                    | MY%20VIDEO                      | Ordner "Mein Video". Ein typischer Pfad ist C: Benutzername für \\ Dokumente und Einstellungen Eigene Dokumente Mein \\ \\ \\ Video.                                                                                       |
| NETHOOD                     | NETHOOD                         | Virtueller Ordner, der den Stamm der Netzwerknamespacehierarchie darstellt.                                                                                                               |
| ORDNER "NETZWERKSPEICHERORTE"       | NETWORKDPLACESFOLDER            | Ein Dateisystemordner, der die Linkobjekte enthält, die möglicherweise im virtuellen Ordner Meine Netzwerkplätze vorhanden sind. Es ist nicht identisch mit NETHOOD, das den Stamm des Netzwerknamespace darstellt.   |
| OEM-LINKS                   | OEM%20LINKS                     | Ordner mit Links zu OEM-Standorten.                                                                                                                                                  |
| PERSONAL                    | PERSONAL                        | Dateisystemverzeichnis, das als allgemeines Repository für die Dokumente eines Benutzers dient. Ein typischer Pfad ist C: Benutzername für \\ Dokumente und Einstellungen \\ \\ Eigene Dokumente.                                 |
| ORDNER "DRUCKER"             | ORDNER "DRUCKER"                 | Virtueller Ordner mit installierten Druckern.                                                                                                                                          |
| PRINTHOOD                   | PRINTHOOD                       | Dateisystemverzeichnis, das die Linkobjekte enthält, die möglicherweise im virtuellen Ordner Drucker vorhanden sind. Ein typischer Pfad ist "C: \\ Documents and Settings username \\ \\ PrintHood".                 |
| PROGRAMME                    | PROGRAMME                        | Dateisystemverzeichnis, das die Programmgruppen des Benutzers enthält (die auch Dateisystemverzeichnisse sind). Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ \\ Startmenüprogramme.  |
| PROFILE                     | PROFILE                         | Der Profilordner des Benutzers.                                                                                                                                                                 |
| PROGRAMMDATEIEN               | PROGRAM%20FILES                 | Ordner "Programme". Ein typischer Pfad ist C: \\ Programme.                                                                                                                             |
| PROGRAMMDATEIEN ( COMMON)        | PROGRAMFILESCOMMON              | Der Ordner "Programme" ist für alle Benutzer gleich.                                                                                                                                              |
| PROGRAMME COMMON x86    | PROGRAMFILESCOMMONX86           | Ordner "Programme", der allen Benutzern auf x86-Computern gemeinsam ist.                                                                                                                              |
| PROGRAM FILESx86            | PROGRAMFILESx86                 | Ordner "Programme" auf x86-Computern.                                                                                                                                                  |
| ZULETZT VERWENDET                      | ZULETZT VERWENDET                          | Dateisystemverzeichnis, das die zuletzt verwendeten Dokumente des Benutzers enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername Zuletzt \\ \\ verwendet.                                           |
| PAPIERKORBORDNER          | RECYCLEBINFOLDER                | Virtueller Ordner, der die Objekte im Papierkorb des Benutzers enthält.                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | Das Ressourcenverzeichnis.                                                                                                                                                                |
| Sendto                      | Sendto                          | Dateisystemverzeichnis, das die Menüelemente Senden an enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ SendTo.                                                                |
| STARTMENÜ                  | START%20MENU                    | Dateisystemverzeichnis, das Startmenü Elemente enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ Startmenü.                                                                 |
| Start                     | Start                         | Dateisystemverzeichnis, das der Startprogrammgruppe des Benutzers entspricht.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | Systemordner auf x86-Computern.                                                                                                                                                         |
| VORLAGEN                   | VORLAGEN                       | Dateisystemverzeichnis, das als allgemeines Repository für Dokumentvorlagen dient.                                                                                                       |
| SYSTEM                      | SYSTEM                          | Systemordner. Ein typischer Pfad ist C: \\ \\ Windows-System.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Windows-Verzeichnis oder SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Argumentinformationen



|                              | Wert                                   |
|------------------------------|-----------------------------------------|
| **Mindestbetriebssystem** | Windows Vista mit Service Pack 1 (SP1) |



 

 

 



