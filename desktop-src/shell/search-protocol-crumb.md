---
description: Hier erfahren Sie, wie Sie das ARGUMENTS in der Windows Shell-Benutzeroberfläche verwenden, um den Bereich einer Suche zu steuern.
title: ARGUMENTS-Argument (die Windows Shell)
ms.topic: article
ms.date: 05/31/2018
ms.assetid: 8f87a2b7-7f5a-4629-b881-44bf418b2df0
api_name: ''
api_type: ''
api_location: ''
topic_type:
- kbArticle
ms.openlocfilehash: b93764f8014a5d9446811ef622f7c5afc20acbc6193d938c98642afaae5392fa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118452876"
---
# <a name="crumb-argument-the-windows-shell"></a>ARGUMENTS-Argument (die Windows Shell)

Das `crumb` -Argument unterstützt vollständige AQS-Anweisungen (Advanced Query Syntax) und ist besonders nützlich, um den Bereich einer Suche zu steuern. Zusätzlich zu AQS-Anweisungen kann das `crumb` Argument einen speziellen Parameter für Windows Vista und parameter für Windows XP `location` `kind` `store` verwenden, wie weiter unten in diesem Thema beschrieben.

Dieses Thema enthält folgende Abschnitte:

-   [Syntax der Verrenkung](#crumb-syntax)
    -   [Allgemeine Beispiele](#general-examples)
-   [Verwenden von "vererbte" mit Vista (Standort)](#using-crumb-with-vista-location)
    -   [Vista-Beispiele](#vista-examples)
    -   [Konstanten für allgemeine Ordner](#constants-for-common-folders)
    -   [Argumentinformationen](#argument-information)

## <a name="crumb-syntax"></a>Syntax der Verrenkung

Die Syntax für die Unbrütlichung lautet wie folgt:


```
crumb=<column>:<value>[,<label>][,<column>:<value>[,<label>]]& 
```



Der <column> Teil ist eine beliebige Eigenschaft im Eigenschaftensystem, und der <value> -Teil ist ein gültiger Wert für diese Eigenschaft. Der <label> -Teil ist ein optionaler Alias für die Eigenschaft, die als Benutzeroberflächenhinweis angezeigt wird.

### <a name="general-examples"></a>Allgemeine Beispiele


```
crumb=System.Author:paolo&
crumb=store:mapi&
crumb=location:c%3a%5cMyVacationPix,Vacation&
```



## <a name="using-crumb-with-vista-location"></a>Verwenden von "vererbte" mit Vista (Standort)

Im Parameters "vista" unterstützt Windows Vista vollständige AQS-Funktionen und auch die `location` -Eigenschaft, die nur auf Windows Vista über eine spezielle Implementierung verfügt. Sie können entweder eine AQS-Zeichenfolge oder die `location` -Eigenschaft innerhalb eines einzigen Vererbeparameters verwenden, aber nicht beides. Wenn der Parameters zum Überschließen AQS enthält, wird alles andere in diesem Parameter ignoriert.

Mit `location` der -Eigenschaft können Sie einen Pfad für die Suche angeben. Windows Vista kann den Indexer umgehen und das Verzeichnis direkt durchlaufen, wenn sich der Speicherort außerhalb des Durchforstungsbereichs des Indexers befindet. Folglich sind diese Suchvorgänge möglicherweise langsamer als Suchvorgänge, die den Indexer verwenden.

Wenn Sie eine `location` Eigenschaft angeben, werden zwei zusätzliche Parameter unterstützt und optional:



| Parameter | Werte                  | Beschreibung                                                                                                                                                                       |
|-----------|-------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Aufnahme | Include, Exclude        | Gibt an, ob die Abfrage Elemente in diesen Pfad einschließen oder davon ausschließen soll. "Include" ist die Standardeinstellung. Windows Vista unterstützt keine Ausschlüsse ohne Einschlüsse. (Siehe Beispiel) |
| Rekursion | rekursiv, nicht rekursiv | Gibt an, ob bei der Suche alle Unterordner beginnend mit dem am Speicherort definierten Wert wiederholt werden sollen:<value>. "Rekursiv" ist die Standardeinstellung.                             |



 

Sie haben je nach Ziel des Bereichs unterschiedliche Optionen, um eine Suche mithilfe des **Protokolls search:** zu ermöglichen.

Ordner auf einem lokalen Computer:

-   Verwenden Sie AQS (folder=folder:<URL-codierter Pfad>)
-   Verwenden Sie das Location-Argument (vererb=location:<URL-codierter Pfad>)

Ordner auf einem Remotecomputer/Netzwerk:

-   Verwenden Sie das Location-Argument (vererb=location:<URL-codierter Pfad>)

Ordner, auf den über einen bekannten UNC-Protokollhandler (Universal Naming Convention) zugegriffen wird:

-   Verwenden Sie AQS (vererb=store: <UNC protocol handler name> ).
-   Verwenden Sie das Location-Argument (vererb=location:<URL-codierter Pfad>)

### <a name="vista-examples"></a>Vista-Beispiele


```
search:query=vacation&crumb=location:shell%3aPersonal,include,recursive&
    
search:crumb=location:c%3a%5cPictures&crumb=location:c%3a%5cPictures%5cDuplicates,,exclude& 
    
search:crumb=location:c%3a%5cDocuments&crumb=kind:pics&
```



Im ersten Beispiel wird eine Suche nach "Vacation" am Standort (eine spezielle Verknüpfung zum ordner Eigene Dokumente des Benutzers) ausgeführt, `shell://Personal` einschließlich dieses Ordners und aller Unterordner.  Siehe dazu die folgende Tabelle.

Im zweiten Beispiel wird eine Suche in C: \\ Bilder ausgeführt, jedoch nicht in C: \\ \\ Bildduplikate.

Im dritten Beispiel wird eine Suche in C: \\ Dokumente ausgeführt, die auf Dateien beschränkt ist, `kind` deren -Eigenschaft auf Bilder festgelegt ist.

### <a name="constants-for-common-folders"></a>Konstanten für allgemeine Ordner

Windows Vista ermöglicht die Verwendung von CSIDL-Werten, die eine eindeutige systemunabhängige Möglichkeit bieten, spezielle Ordner zu identifizieren, die häufig von Anwendungen verwendet werden, aber möglicherweise nicht den gleichen Namen oder Speicherort auf einem bestimmten System aufweisen. Beispielsweise kann der Systemordner auf einem System "C: \\ Windows" und auf einem anderen "C: \\ Winnt" sein.

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
| CD-AKTUSER                  | CD%20 VERARBEITUNG                    | Ordner, der Daten enthält, die auf CD 1000000000000000000000                                                                                                                                             |
| ALLGEMEINE VERWALTUNGSTOOLS | COMMON%20ADMINISTRATIVE%20TOOLS | Verwaltungstools für alle Benutzer.                                                                                                                                                    |
| ALLGEMEINE APPDATA              | COMMON%20APPDATA                | Anwendungsdaten für alle Benutzer. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Alle \\ \\ Benutzeranwendungsdaten.                                                                             |
| COMMON DESKTOP              | COMMON DESKTOP                  | Microsoft Windows Desktop-Daten für alle Benutzer. Virtueller Ordner, der das Stammverzeichnis des Namespaces ist.                                                                                        |
| ALLGEMEINE DOKUMENTE            | COMMON%20DOCUMENTS              | Dokumente für alle Benutzer. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Alle Benutzer \\ \\ Eigene Dokumente.                                                                                        |
| ALLGEMEINE PROGRAMME             | COMMON%20PROGRAMS               | Programmgruppen, die allen Benutzern gemeinsam sind. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Alle Benutzer \\ \\ \\ Startmenüprogramme.                                                                     |
| ALLGEMEINES STARTMENÜ           | COMMON%20START%20MENU           | Startmenü Elemente, die allen Benutzern gemeinsam sind. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Alle Benutzer \\ \\ Startmenü.                                                                             |
| ALLGEMEINER START              | COMMON%20STARTUP                | Startprogrammgruppe, die allen Benutzern gemeinsam ist.                                                                                                                                             |
| ALLGEMEINE VORLAGEN            | COMMON%20TEMPLATES              | Dokumentvorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                                |
| COMMONOLO                 | MY%20 WIES                      | Meine Musik Ordnervorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                         |
| COMMONPICTURES              | MY%20PICTURES                   | My Pictures-Ordnervorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                      |
| COMMONVIDEO                 | MY%20VIDEO                      | Meine Videoordnervorlagen, die allen Benutzern gemeinsam sind.                                                                                                                                         |
| CONNECTIONSFOLDER           | CONNECTIONSFOLDER               | Ordner, der Die Verbindungsdaten enthält.                                                                                                                                                     |
| SYSTEMSTEUERUNGSORDNER        | CONTROLPANELFOLDER              | Virtueller Ordner, der Symbole für die Systemsteuerung enthält.                                                                                                                    |
| Cookies                     | Cookies                         | Dateisystemverzeichnis, das als allgemeines Repository für Internetcookies dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ Cookies.                                        |
| DESKTOP                     | DESKTOP                         | Microsoft Windows Desktop. Virtueller Ordner, der das Stammverzeichnis des Namespaces ist.                                                                                                           |
| FAVORITEN                   | FAVORITEN                       | Dateisystemverzeichnis, das als allgemeines Repository für die bevorzugten Elemente des Benutzers dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ \\ Favoriten für Benutzernamen.                             |
| Schriftarten                       | Schriftarten                           | Virtueller Ordner mit installierten Schriftarten. Ein typischer Pfad ist C: \\ \\ WINDOWS-Schriftarten.                                                                                                       |
| VERLAUF                     | VERLAUF                         | Dateisystemverzeichnis, das als allgemeines Repository für Internetverlaufselemente dient.                                                                                                   |
| INTERNETFOLDER              | INTERNETFOLDER                  | Ordner, der Internetdaten enthält.                                                                                                                                                    |
| LOKALE APPDATA               | LOCAL%20APPDATA                 | Dateisystemverzeichnis, das als Datenrepository für lokale (nicht roamingbasierte) Anwendungen dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername Local Einstellungen \\ \\ \\ Anwendungsdaten. |
| LOCALIZEDRESOURCEDIR        | LOCALIZEDRESOURCEDIR            | Lokalisiertes Ressourcenverzeichnis.                                                                                                                                                          |
| MYCOMPUTERFOLDER            | MYCOMPUTERFOLDER                | Arbeitsplatz. Virtueller Ordner, der alles auf dem lokalen Computer enthält: Speichergeräte, Drucker und Systemsteuerung. Dieser Ordner kann auch zugeordnete Netzwerklaufwerke enthalten.             |
| MY MUSIC                    | MY%20 WIES                      | Mein Musik Ordner. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername Eigene Dokumente My \\ \\ \\ Musik.                                                                                       |
| MEINE BILDER                 | MY%20PICTURES                   | Ordner "Meine Bilder". Ein typischer Pfad ist C: \\ Dokumente und Einstellungen benutzername Eigene Dokumente Meine \\ \\ \\ Bilder.                                                                                 |
| MEIN VIDEO                    | MY%20VIDEO                      | Mein Videoordner. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername Eigene Dokumente Mein \\ \\ \\ Video.                                                                                       |
| NETHOOD                     | NETHOOD                         | Virtueller Ordner, der den Stamm der Netzwerknamespacehierarchie darstellt.                                                                                                               |
| ORDNER "NETZWERKSPEICHERORTE"       | NETWORKDPLACESFOLDER            | Ein Dateisystemordner mit den Linkobjekten, die möglicherweise im virtuellen Ordner "Meine Netzwerkorte" vorhanden sind. Es ist nicht identisch mit NETHOOD, das den Netzwerknamespacestamm darstellt.   |
| OEM-LINKS                   | OEM%20LINKS                     | Ordner mit Links zu OEM-Standorten.                                                                                                                                                  |
| PERSONAL                    | PERSONAL                        | Dateisystemverzeichnis, das als allgemeines Repository für die Dokumente eines Benutzers dient. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ Eigene Dokumente.                                 |
| DRUCKERORDNER             | DRUCKERORDNER                 | Virtueller Ordner mit installierten Druckern.                                                                                                                                          |
| PRINTHOOD                   | PRINTHOOD                       | Dateisystemverzeichnis, das die Linkobjekte enthält, die möglicherweise im virtuellen Ordner Drucker vorhanden sind. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ \\ PrintHood.                 |
| PROGRAMME                    | PROGRAMME                        | Dateisystemverzeichnis, das die Programmgruppen des Benutzers enthält (die auch Dateisystemverzeichnisse sind). Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ \\ \\ Startmenüprogramme.  |
| PROFILE                     | PROFILE                         | Der Profilordner des Benutzers.                                                                                                                                                                 |
| PROGRAMMDATEIEN               | PROGRAM%20FILES                 | Ordner "Programme". Ein typischer Pfad ist C: \\ Programme.                                                                                                                             |
| ALLGEMEINE PROGRAMMDATEIEN        | PROGRAMFILESCOMMON              | Ordner "Programme", der allen Benutzern gemeinsam ist.                                                                                                                                              |
| PROGRAMME COMMON x86    | PROGRAMFILESCOMMONX86           | Ordner "Programme", der allen Benutzern auf x86-Computern gemeinsam ist.                                                                                                                              |
| PROGRAM FILESx86            | PROGRAMFILESx86                 | Ordner "Programme" auf x86-Computern.                                                                                                                                                  |
| ZULETZT VERWENDET                      | ZULETZT VERWENDET                          | Dateisystemverzeichnis, das die zuletzt verwendeten Dokumente des Benutzers enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen Benutzername \\ \\ Zuletzt.                                           |
| ORDNER "PAPIERKORB"          | RECYCLEBINFOLDER                | Virtueller Ordner, der die Objekte im Benutzerordner Papierkorb.                                                                                                                       |
| RESOURCEDIR                 | RESOURCEDIR                     | Das Ressourcenverzeichnis.                                                                                                                                                                |
| Sendto                      | Sendto                          | Dateisystemverzeichnis, das Menüelemente an senden enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ \\ SendTo.                                                                |
| STARTMENÜ                  | START%20MENU                    | Dateisystemverzeichnis, das Startmenü enthält. Ein typischer Pfad ist C: \\ Dokumente und Einstellungen \\ \\ Startmenü des Benutzernamens.                                                                 |
| Start                     | Start                         | Dateisystemverzeichnis, das der Startprogrammgruppe des Benutzers entspricht.                                                                                                            |
| SYSTEMx86                   | SYSTEMx86                       | Systemordner auf x86-Computern.                                                                                                                                                         |
| VORLAGEN                   | VORLAGEN                       | Dateisystemverzeichnis, das als allgemeines Repository für Dokumentvorlagen dient.                                                                                                       |
| SYSTEM                      | SYSTEM                          | Systemordner. Ein typischer Pfad ist C: \\ Windows \\ System.                                                                                                                                  |
| WINDOWS                     | WINDOWS                         | Windows oder SYSROOT.                                                                                                                                                          |



 

### <a name="argument-information"></a>Argumentinformationen



|                              | Wert                                   |
|------------------------------|-----------------------------------------|
| **Mindestbetriebssystem** | Windows Vista mit Service Pack 1 (SP1) |



 

 

 



