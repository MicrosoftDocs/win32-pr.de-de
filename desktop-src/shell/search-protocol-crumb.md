---
description: Hier erfahren Sie, wie Sie das CRUMB-Argument in der Windows Shell-Benutzeroberfläche verwenden, um den Bereich einer Suche zu steuern.
title: CRUMB-Argument (die Windows Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: 3309f18cbd5a7e2769b264e516b019d9f3ed3b06
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/26/2021
ms.locfileid: "122885436"
---
# <a name="crumb-argument-the-windows-shell"></a>CRUMB-Argument (die Windows Shell)

Das `crumb` -Argument unterstützt vollständige AQS-Anweisungen (Advanced Query Syntax) und ist besonders nützlich, um den Bereich einer Suche zu steuern. Zusätzlich zu AQS-Anweisungen kann das -Argument einen speziellen Parameter für Windows Vista und die Parameter auf Windows XP verwenden, wie weiter unten `crumb` `location` in diesem Thema `kind` `store` beschrieben.

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



Der &lt; &gt; Spaltenteil ist eine beliebige Eigenschaft im Eigenschaftensystem, und der &lt; &gt; Wertteil ist ein gültiger Wert für diese Eigenschaft. Der <label> -Teil ist ein optionaler Alias für die Eigenschaft, die als Benutzeroberflächenhinweis angezeigt wird.

### <a name="general-examples"></a>Allgemeine Beispiele


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Verwenden von Crumb mit Vista (Standort)

Im crumb-Parameter unterstützt Windows Vista die vollständige AQS und auch die -Eigenschaft, die eine spezielle Implementierung nur auf Windows `location` Vista auflistet. Sie können entweder eine AQS-Zeichenfolge oder die -Eigenschaft innerhalb eines `location` einzelnen crumb-Parameters verwenden, aber nicht beide. Wenn der crumb-Parameter AQS enthält, wird alles andere in diesem crumb-Parameter ignoriert.

Mit `location` der -Eigenschaft können Sie einen zu durchsuchenden Pfad angeben. Windows Vista kann den Indexer umgehen und das Verzeichnis direkt durchlaufen, wenn sich der Speicherort außerhalb des Indexer-Durchforstungsbereichs befindet. Folglich sind diese Suchvorgänge möglicherweise langsamer als Suchvorgänge, die den Indexer verwenden.

Wenn Sie eine Eigenschaft `location` angeben, werden zwei zusätzliche Parameter unterstützt und optional:



| Parameter | Werte                  | Beschreibung                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aufnahme | include, exclude        | Gibt an, ob die Abfrage Elemente in diesen Pfad ein- oder ausschließen soll. "Include" ist die Standardeinstellung. Windows Vista unterstützt keine Ausschlüsse ohne Einschlüsse. (Siehe Beispiel) |
| Rekursion | rekursiv, nicht rekursiv | Gibt an, ob bei der Suche alle Unterordner wiederholt werden sollen, beginnend mit dem Wert, der am Speicherort definiert &lt; ist: value &gt; . "Rekursiv" ist die Standardeinstellung.                             |



 

Für den Bereich einer Suche mithilfe des **Protokolls search:** stehen Ihnen je nach Ziel des Bereichs unterschiedliche Optionen zur Verfügung.

Ordner auf einem lokalen Computer:

-   Verwenden Sie AQS (crumb=folder:<URL-codierten Pfad>)
-   Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)

Ordner auf einem Remotecomputer/-netzwerk:

-   Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)

Ordner, auf den über einen Universal Naming Convention (UNC)-Protokollhandler zugegriffen wird:

-   Verwenden Sie AQS (crumb=store: <UNC protocol handler name> ).
-   Verwenden Sie das location-Argument (crumb=location:<URL-codierten Pfad>)

### <a name="vista-examples"></a>Vista-Beispiele


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Im ersten Beispiel wird eine Suche nach "Vacation" ausgeführt, die am Speicherort beginnt (eine spezielle Verknüpfung zum Ordner Eigene Dokumente des Benutzers), einschließlich dieses Ordners und aller `shell://Personal` Unterordner.  Siehe dazu die folgende Tabelle.

Im zweiten Beispiel wird eine Suche in C: \\ Bilder, aber nicht in C: \\ \\ Bilderduplizieren ausgeführt.

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
| APPDATA                     | APPDATA                         | Dateisystemverzeichnis, das als allgemeines Repository für anwendungsspezifische Daten dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ Anwendungsdaten.                      |
| CACHE                       | CACHE                           | Dateisystemverzeichnis, das als allgemeines Repository für temporäre Internetdateien dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername Temporäre \\ \\ Internetdateien.               |
| CD- UND CD-20                  | CD%20 WIE                    | Ordner, der Daten enthält, die auf CD glühen sollen.                                                                                                                                             |
| ALLGEMEINE VERWALTUNGSTOOLS | COMMON%20ADMINISTRATIVE%20TOOLS | Verwaltungstools für alle Benutzer.                                                                                                                                                    |
| ALLGEMEINE APP-DATEN              | COMMON%20APPDATA                | Anwendungsdaten für alle Benutzer. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ Anwendungsdaten aller \\ Benutzer.                                                                             |
| COMMON DESKTOP              | COMMON DESKTOP                  | Microsoft Windows Desktopdaten für alle Benutzer. Virtueller Ordner, der das Stammverzeichnis des Namespace ist.                                                                                        |
| ALLGEMEINE DOKUMENTE            | COMMON%20DOCUMENTS              | Dokumente für alle Benutzer. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Alle Benutzer \\ \\ Eigene Dokumente.                                                                                        |
| ALLGEMEINE PROGRAMME             | COMMON%20PROGRAMS               | Programmgruppen, die allen Benutzern gemeinsam sind. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Alle Benutzer \\ \\ \\ Startmenüprogramme.                                                                     |
| ALLGEMEINES STARTMENÜ           | COMMON%20START%20MENU           | Startmenü elemente, die allen Benutzern gemeinsam sind. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ \\ Startmenü "Alle Benutzer".                                                                             |
| COMMON STARTUP              | COMMON%20STARTUP                | Startprogrammgruppe, die allen Benutzern gemeinsam ist.                                                                                                                                             |
| ALLGEMEINE VORLAGEN            | COMMON%20TEMPLATES              | Dokumentvorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                                |
| COMMONOLO                 | MY%20 WIES                      | Meine Musik Ordnervorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                         |
| COMMONPICTURES              | MY%20PICTURES                   | My Pictures-Ordnervorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                      |
| COMMONVIDEO                 | MY%20VIDEO                      | Meine Videoordnervorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | Ordner, der Die Verbindungsdaten enthält.                                                                                                                                                     |
| SYSTEMSTEUERUNGSORDNER        | CONTROLPANELFOLDER              | Virtueller Ordner, der Symbole für die Systemsteuerung enthält.                                                                                                                    |
| COOKIES                     | COOKIES                         | Dateisystemverzeichnis, das als allgemeines Repository für Internetcookies dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ Cookies.                                        |
| DESKTOP                     | DESKTOP                         | Microsoft Windows Desktop. Virtueller Ordner, der das Stammverzeichnis des Namespace ist.                                                                                                           |
| FAVORITEN                   | FAVORITEN                       | Dateisystemverzeichnis, das als allgemeines Repository für die bevorzugten Elemente des Benutzers dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ \\ Benutzernamensfavoriten.                             |
| SCHRIFTARTEN                       | SCHRIFTARTEN                           | Virtueller Ordner mit installierten Schriftarten. Ein typischer Pfad ist C: \\ \\ WINDOWS-Schriftarten.                                                                                                       |
| VERLAUF                     | VERLAUF                         | Dateisystemverzeichnis, das als allgemeines Repository für Internetverlaufselemente dient.                                                                                                   |
| INTERNETFOLDER              | INTERNETFOLDER                  | Ordner, der Internetdaten enthält.                                                                                                                                                    |
| LOKALE APP-DATEN               | LOCAL%20APPDATA                 | Dateisystemverzeichnis, das als Datenrepository für lokale (nicht roamingbasierte) Anwendungen dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername Local Einstellungen \\ \\ \\ Anwendungsdaten. |
| LOCALIZEDRESOURCEDIR        | LOCALIZEDRESOURCEDIR            | Lokalisiertes Ressourcenverzeichnis.                                                                                                                                                          |
| MYCOMPUTERFOLDER            | MYCOMPUTERFOLDER                | Arbeitsplatz. Virtueller Ordner, der alles auf dem lokalen Computer enthält: Speichergeräte, Drucker und Systemsteuerung. Dieser Ordner kann auch zugeordnete Netzwerklaufwerke enthalten.             |
| MY MUSIC                    | MY%20 WIES                      | Mein Musik Ordner. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername Eigene Dokumente My \\ \\ \\ Musik.                                                                                       |
| MEINE BILDER                 | MY%20PICTURES                   | Ordner "Meine Bilder". Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername Eigene Dokumente Meine \\ \\ \\ Bilder.                                                                                 |
| MEIN VIDEO                    | MY%20VIDEO                      | Mein Videoordner. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen benutzername Eigene Dokumente Mein \\ \\ \\ Video.                                                                                       |
| NETHOOD                     | NETHOOD                         | Virtueller Ordner, der den Stamm der Netzwerknamespacehierarchie darstellt.                                                                                                               |
| ORDNER "NETZWERKSPEICHERORTE"       | NETWORKDPLACESFOLDER            | Ein Dateisystemordner mit den Linkobjekten, die möglicherweise im virtuellen Ordner "Meine Netzwerkorte" vorhanden sind. Es ist nicht identisch mit NETHOOD, das den Netzwerknamespacestamm darstellt.   |
| OEM-LINKS                   | OEM%20LINKS                     | Ordner mit Links zu OEM-Standorten.                                                                                                                                                  |
| PERSONAL                    | PERSONAL                        | Dateisystemverzeichnis, das als allgemeines Repository für die Dokumente eines Benutzers dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ Eigene Dokumente.                                 |
| DRUCKERORDNER             | DRUCKERORDNER                 | Virtueller Ordner mit installierten Druckern.                                                                                                                                          |
| PRINTHOOD                   | PRINTHOOD                       | Dateisystemverzeichnis, das die Linkobjekte enthält, die möglicherweise im virtuellen Ordner Drucker vorhanden sind. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ PrintHood.                 |
| PROGRAMME                    | PROGRAMME                        | Dateisystemverzeichnis, das die Programmgruppen des Benutzers enthält (die auch Dateisystemverzeichnisse sind). Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ \\ Startmenüprogramme.  |
| PROFILE                     | PROFILE                         | Der Profilordner des Benutzers.                                                                                                                                                                 |
| PROGRAMMDATEIEN               | PROGRAM%20FILES                 | Ordner "Programme". Ein typischer Pfad ist C: \\ Programme.                                                                                                                             |
| ALLGEMEINE PROGRAMMDATEIEN        | PROGRAMFILESCOMMON              | Ordner "Programme", der allen Benutzern gemeinsam ist.                                                                                                                                              |
| PROGRAMME COMMON x86    | PROGRAMFILESCOMMONX86           | Ordner "Programme", der allen Benutzern auf x86-Computern gemeinsam ist.                                                                                                                              |
| PROGRAM FILESx86            | PROGRAMFILESx86                 | Ordner "Programme" auf x86-Computern.                                                                                                                                                  |
| ZULETZT VERWENDET                      | ZULETZT VERWENDET                          | Dateisystemverzeichnis, das die zuletzt verwendeten Dokumente des Benutzers enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername Zuletzt \\ \\ verwendet.                                           |
| PAPIERKORBORDNER          | RECYCLEBINFOLDER                | Virtueller Ordner, der die Objekte im Papierkorb des Benutzers enthält.                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | Das Ressourcenverzeichnis.                                                                                                                                                                |
| SENDTO                      | SENDTO                          | Dateisystemverzeichnis, das die Menüelemente Senden an enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ SendTo.                                                                |
| STARTMENÜ                  | START%20MENU                    | Dateisystemverzeichnis, das Startmenü Elemente enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ Startmenü.                                                                 |
| START                     | START                         | Dateisystemverzeichnis, das der Startprogrammgruppe des Benutzers entspricht.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | Systemordner auf x86-Computern.                                                                                                                                                         |
| VORLAGEN                   | VORLAGEN                       | Dateisystemverzeichnis, das als allgemeines Repository für Dokumentvorlagen dient.                                                                                                       |
| SYSTEM                      | SYSTEM                          | Systemordner. Ein typischer Pfad ist C: \\ Windows \\ System.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Windows Verzeichnis oder SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Argumentinformationen



|                              | Wert                                   |
|------------------------------|-----------------------------------------|
| **Mindestbetriebssystem** | Windows Vista mit Service Pack 1 (SP1) |



 

 

 



