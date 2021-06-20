---
title: Windows Desktop Search 2.x
description: Informationen zur Windows-Desktopsuche 2.x. Verwenden Sie für Windows-Releases, die höher als Windows XP und Windows Server 2003 sind, Windows Search.
ms.assetid: 3d73f850-58b8-4a41-8863-e2914661d4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1ff43f827458d295e54b71b3f39c7aa471c058d
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408123"
---
# <a name="windows-desktop-search-2x"></a>Windows Desktop Search 2.x

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)

Die Verwendung von und entwicklung für die 2.x-Versionen von Microsoft Windows Desktop Search (WDS) wird dringend zugunsten von [Windows Search.](../search/-search-3x-wds-overview.md)

WDS ist ein Indizierungsdienst und eine Plattform, die eine schnelle Suche nach Dateien und Daten über verschiedene Datenquellen und Speicherorte hinweg ermöglicht. WDS hilft Benutzern und anderen Anwendungen, fast alles auf ihren Computern, E-Mail-Nachrichten, Kalenderterminen, Fotos, Dokumenten und mehr zu finden. Darüber hinaus kann WDS Ergebnisse aus mehreren Datenquellen in einer Windows-Explorer-Umgebung zurückgeben, damit Ihre Benutzer schnell eine Vorschau anzeigen, filtern und auf Suchergebnisse reagieren können.

WDS indiziert Daten innerhalb eines bestimmten Durchforstungsbereichs, der angegebenen Speicherorte innerhalb eines lokalen Computers und freigegebenen Netzwerks, die der Indexer durchforsten soll. Dieser Durchforstungsbereich kann durch Benutzergruppenoptionen, Verwaltungs-APIs und Gruppenrichtlinien gesteuert werden, die Netzwerkadministratoren konfigurieren können, um Benutzerzugriffsberechtigungen und Indizierungseinstellungen zu steuern. Gruppenrichtlinien können den Zugriff auf bestimmte Netzwerkressourcen einschränken und zu indizierende Ressourcen definieren.

Dieser Abschnitt enthält die folgenden Themen:

-   [Übersicht](#windows-desktop-search-2x)
    -   [Informationen zum WDS-Indexer](#about-the-wds-indexer)
    -   [Informationen zum WDS-Katalog](#about-the-wds-catalog)
    -   [Informationen zur Suchmaschine und den Ergebnissen](#about-the-search-engine-and-results)
-   [Entwickeln mit WDS](#developing-with-wds)
    -   [Hinzufügen von Daten zum Index mit Add-Ins](#adding-data-to-the-index-with-add-ins)
    -   [Abfragen des Index](#querying-the-index)
-   [Kompatibilitätsanforderungen](#compatibility-requirements)
    -   [Systemanforderungen](#system-requirements)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Übersicht

### <a name="about-the-wds-indexer"></a>Informationen zum WDS-Indexer

Bei der ersten Installation durchforstung der Indexer die gängigsten benutzerorientierten Dateien im Ordner Eigene Dokumente, in den E-Mail-Ordnern Microsoft Outlook und Microsoft Outlook Express sowie an den in Gruppenrichtlinie. Benutzer können auch neue Dateien und Speicherorte für den Indexer angeben, die in aufeinander folgende Durchforstungen aufgenommen (oder ausgeschlossen) werden. Jeder enthaltene Speicherort wird durch eine URL identifiziert, und der Indexer beginnt bei dieser URL und durchlädt rekursiv alle Unterordner oder Speicherorte, bis alle Elemente indiziert wurden. Ein Bereich ist ein Satz von URLs. Die Verwaltungs-APIs können von benutzerdefinierten Anwendungen verwendet werden, um ihren Durchforstungsbereich zu definieren, eine Reihe von URLs, die auf Pfade innerhalb eines Protokolls verweisen, z. B. für Ordner auf einem Laufwerk oder `file://` für MAPI-E-Mail-Speicher wie `mapi:// ` Outlook. WDS verwendet Protokollhandler für den Zugriff auf die Datenspeicher und Filter, um den Text und die Eigenschaften der Elemente zu analysieren und zu indizieren. Diese Daten werden dann im Katalog gespeichert.

### <a name="about-the-wds-catalog"></a>Informationen zum WDS-Katalog

Der WDS-Katalog ist ein Index von Text und Eigenschaften, die von Elementen in angegebenen E-Mails, lokalen Laufwerken, Netzwerkressourcen und anderen lokalen Datenspeichern gesammelt wurden. Der Inhalt des Katalogs basiert auf Optionen und Regeln, die von WDS, auf der WDS-Plattform erstellten Anwendungen, Benutzereinstellungen und Gruppenrichtlinien festgelegt werden. Für jedes indizierte Element sind über 200 Eigenschaften verfügbar, z. B. Erstellungsdatum, Größe und typspezifische Eigenschaften ("From" für E-Mail-Nachrichten). Eine Liste dieser Eigenschaften finden Sie in der [WDS-Schemareferenz.](-search-2x-wds-schematable.md)

### <a name="about-the-search-engine-and-results"></a>Informationen zur Suchmaschine und den Ergebnissen

Über die WDS-Deskleiste oder Windows-Explorer können Benutzer die Volltextinhalts- und Eigenschaftsmetadaten indizierter Elemente durchsuchen. Die gleichen Suchvorgänge können auch über die Befehlszeile, über eine Webseite oder über eine benutzerdefinierte Anwendung initiiert werden. Die WDS-Suchmaschine sucht Nach Elementen, die den Suchkriterien entsprechen, und gibt sie als Microsoft ActiveX Data Objects(ADO)-ResultSets zurück. WDS zeigt Elemente an, die den Suchkriterien entsprechen, und kann eine umfassende Vorschau des Elements anzeigen. Sie können Anwendungen erstellen, um die Suchabfrage abzufangen, die Suche durchzuführen und/oder das Ergebnisset anzuzeigen.

## <a name="developing-with-wds"></a>Entwickeln mit WDS

Es gibt zwei Haupttypen der Integration in WDS: das Hinzufügen von Daten zum Index und das Abfragen des Indexinhalts, um Datensätze abzurufen, die den Suchkriterien entsprechen.

### <a name="adding-data-to-the-index-with-add-ins"></a>Hinzufügen von Daten zum Index mit Add-Ins

Es gibt im Grunde zwei Arten von Datenquellen: Dateisystemspeicher und Nichtdateisystemspeicher. Eine Gruppe von Dateien in Eigene Dokumente ist ein einfacher Dateisystemspeicher. WDS kann Informationen in den Dateien durchsuchen, die in einem solchen Dateisystem gespeichert sind, wenn ein Filter für den Dateityp gefunden werden kann. Sie können WDS aktivieren, um einen neuen proprietären Dateityp zu indizieren, wenn Sie eine Implementierung der [**IFilter-Schnittstelle**](/windows/desktop/api/filter/nn-filter-ifilter)für diesen Dateityp bereitstellen.

Ein Nichtdateisystemspeicher wie eine Datenbank erfordert einen Protokollhandler, um WDS das Navigieren durch und Indizieren von Daten innerhalb des Datenspeichers zu ermöglichen. Wenn Sie beispielsweise über einen E-Mail-Client verfügen, der die Liste der empfangenen E-Mails in einer eigenen Datei speichert (z. B. PST-Dateien in Outlook), können Sie einen Protokollhandler bereitstellen, um jede einzelne E-Mail zu indizieren und zu durchsuchen, indem Sie einen Protokollhandler bereitstellen. Wenn der Datenspeicher hierarchisch ist, müssen Sie auch eine [**IFilter-Schnittstelle**](/windows/desktop/api/filter/nn-filter-ifilter)implementieren, um die Elemente im Speicher aufzuzählen. Für eine bessere Benutzererfahrung können Sie eine Shellerweiterung implementieren, um Kontextmenüs und Symbole aus der Ergebnisansicht zur Verfügung zu stellen.

Derzeit enthält WDS Filter für mehr als 200 Elementtypen (einschließlich Klartextelementen wie HTML-, XML- und Quellcodedateien) und verwendet die gleiche [**IFilter-**](/windows/desktop/api/filter/nn-filter-ifilter)und Protokollhandlertechnologie wie SharePoint Services. Wenn Sie bereits Filter für proprietäre Dateitypen installiert haben, kann WDS die vorhandenen Filterschnittstellen verwenden, um diese Daten zu indizieren.

### <a name="querying-the-index"></a>Abfragen des Index

WDS stellt Anwendungen benutzerdefinierte Datensätze aus dem Index bereit, die auf einem der verfügbaren Schemawerte basieren. Ergebnisse werden als ADO-Eintragssätze zurückgegeben. Es gibt vier Möglichkeiten, WDS-Abfragen in eine Anwendung zu integrieren, die jeweils verschiedene Anpassungs- und Stabilitätsebenen bieten.

-   ISearchDesktop-Schnittstelle: APIs in dieser Schnittstelle werden zum programmgesteuerten Aufrufen von WDS verwendet, indem eine Abfragezeichenfolge, eine Liste der zurücksenden Spalten, Bereichseinschränkungen ähnlich einer Structured Query Language (SQL)-WHERE-Klausel und der Name der Spalte angegeben werden, nach der sortiert werden soll. Diese APIs sind für nativen und verwalteten Code verfügbar.
-   WDS-ActiveX-Steuerelement: Dieses Steuerelement zeichnet die WDS-Suchschnittstelle und verwaltet das Suchen und Anzeigen von Ergebnissen. Diese Methode ist einfacher als die Verwendung der APIs, aber weniger flexibel. Um dieses Steuerelement in einer Microsoft Visual Studio-Anwendung zu verwenden, wechseln Sie im Menü **Extras** zum Dialogfeld **Toolboxelemente** auswählen, und fügen Sie der **Toolbox** auf der Registerkarte **COM-Komponenten** "Windows Desktop Search - Results Viewer" hinzu. Fügen Sie dann das Steuerelement dem Formular hinzu, in dem Sie es enthalten möchten. Das WDS ActiveX-Steuerelement ist nur unter Windows XP mit WDS 2.x und 3.x kompatibel.
-   Befehlszeilenparameter: Anwendungen können die ausführbare WDS-Datei mit verschiedenen Parametern aufrufen, um Ergebnisse zu suchen und anzuzeigen. Dadurch wird ein WDS-Fenster geöffnet, in dem die Ergebnisse angezeigt werden. Dies ist die einfachste Möglichkeit, einer Anwendung eine Suche hinzuzufügen, gibt jedoch keine Informationen darüber zurück, was der Benutzer im WDS-Fenster tut.
-   WDS-Browser-Hilfsobjekt (BHO): Auf ähnliche Weise können Webseiten den BHO verwenden, um Abfragen an WDS oder die registrierte Suchanwendung zu senden. Nach dem Überprüfen der Webseiten-URL anhand der liste mit den WDS-Domänensicheren führt WDS entweder die Abfrage aus und zeigt die Ergebnisse über die Standardsuchschnittstelle an, oder die Abfrage wird an die registrierte Suchanwendung übergeben.

Benutzer können erweiterte [Abfragesyntax verwenden,](-search-2x-wds-aqsreference.md) um den Katalog leistungsfähiger zu abfragen, indem sie den Suchbereich steuern und Suchparameter mit booleschen Operatoren kombinieren. Beispielsweise könnte ein Benutzer in einer E-Mail von John nach einer Anlage suchen, die entweder "Projektzeitplan" oder "Projektplan" mit einer Abfrage wie der folgenden enthält: `from:John isattachment:true "project schedule" OR "project plan"` .

## <a name="compatibility-requirements"></a>Kompatibilitätsanforderungen

WDS 2.6.5 ist nur für Windows 2000, Windows Server 2003 und Windows XP verfügbar. WDS ist ein separater Download, der von Microsoft kostenlos für den privaten und geschäftlichen Gebrauch zur Verfügung steht. Sie muss installiert sein und für die Indizierung des Benutzerkontos verwendet werden, bevor anwendungen, die für WDS 2.6.5 erstellt wurden, funktionieren.

### <a name="system-requirements"></a>Systemanforderungen

Für die Verwendung der Windows-Desktopsuche ist Folgendes erforderlich:

-   Windows Internet Explorer oder höher.
-   Um Ihre E-Mail-Nachrichten in den Katalog einfingen zu können, müssen Sie microsoft Microsoft Outlook 2000 oder höher oder Microsoft Outlook Express 6.0 oder höher verwenden.
-   Die vollständige Vorschau von Microsoft Microsoft Office in der Ergebnisansicht erfordert Office XP oder höher.
-   Mindestens ein Pentium-Prozessor mit 500 MHz (1 GHz empfohlen).
-   Windows XP, Windows 2000 SP4 oder höher oder Windows Server 2003 Service Pack 1.
-   Mindestens 128 MB RAM (256 MB empfohlen).
-   500 MB freier Festplattenspeicher empfohlen. Die Größe des Index hängt davon ab, wie viel Inhalt Sie indiziert haben.
-   1024 x 768 Bildschirmauflösung empfohlen.

## <a name="related-topics"></a>Verwandte Themen

1.  Abfragen des Index

    -   [Programmgesteuertes Aufrufen von WDS (über ISearchDesktop)](-search-2x-wds-callingwdsprogrammatically.md)
    -   [Aufrufen von WDS über Webseiten](-search-2x-wds-browserhelpobject.md)
    -   [Aufrufen von WDS über die Befehlszeile](-search-2x-wds-fromcommandline.md)

2.  [Erweitern des Indexes (Übersicht)](-search-2x-wds-extendingtheindex.md)

    -   [Entwickeln von IFilter-Add-Ins](-search-2x-wds-ifilteraddins.md)
    -   [Entwickeln von Protokollhandlern](-search-2x-wds-phaddins.md)

3.  Allgemeine Verweise

    -   [WDS-Schema](-search-2x-wds-schematable.md)
    -   [Erweiterte Abfragesyntax](-search-2x-wds-aqsreference.md)
    -   [Von WDS wahrgenommene Typen](-search-2x-wds-perceivedtype.md)

 

 