---
title: Windows-Desktop Suche 2. x
description: Die Verwendung der-und-Entwicklung für die 2. x-Versionen von Microsoft Windows Desktop Search (WDS) wird zugunsten von Windows Search dringend empfohlen.
ms.assetid: 3d73f850-58b8-4a41-8863-e2914661d4b9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e5131fe700b7b049371625249768b0073d009a87
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337429"
---
# <a name="windows-desktop-search-2x"></a>Windows-Desktop Suche 2. x

> [!NOTE]
> Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .

Die Verwendung der-und-Entwicklung für die 2. x-Versionen von Microsoft Windows Desktop Search (WDS) wird zugunsten von [Windows Search](../search/-search-3x-wds-overview.md)dringend empfohlen.

Bei WDS handelt es sich um einen Indizierungs Dienst und eine Plattform, die eine schnelle Suche von Dateien und Daten über verschiedene Datenquellen und Standorte hinweg ermöglicht. WDS unterstützt Benutzer und andere Anwendungen dabei, fast alles auf ihren Computern, e-Mail-Nachrichten, Kalender Terminen, Fotos, Dokumente und mehr zu finden. Darüber hinaus können WDS Ergebnisse aus mehreren Datenquellen in einer Windows-Explorer-Umgebung zurückgeben, damit Ihre Benutzer schnell eine Vorschau, eine Filterung und einen Suchvorgang für Suchergebnisse durchführen können.

WDS indiziert Daten innerhalb eines bestimmten Durchforstungs Bereichs, die angegebenen Speicherorte auf einem lokalen Computer und das freigegebene Netzwerk, das der Indexer durchforsten soll. Dieser Crawl Bereich kann durch Benutzer Satz Optionen, Verwaltungs-APIs und Gruppenrichtlinien gesteuert werden, die Netzwerkadministratoren so konfigurieren können, dass Benutzer Zugriffsberechtigungen und Indizierungs Einstellungen gesteuert werden. Gruppenrichtlinien können den Zugriff auf bestimmte Netzwerkressourcen einschränken und die zu indizierenden Ressourcen definieren.

Dieser Abschnitt enthält die folgenden Themen:

-   [Übersicht](#windows-desktop-search-2x)
    -   [Informationen zum WDS-Indexer](#about-the-wds-indexer)
    -   [Informationen zum WDS-Katalog](#about-the-wds-catalog)
    -   [Informationen zur Suchmaschine und zu Ergebnissen](#about-the-search-engine-and-results)
-   [Entwickeln mit WDS](#developing-with-wds)
    -   [Hinzufügen von Daten zum Index mit Add-ins](#adding-data-to-the-index-with-add-ins)
    -   [Abfragen des Indexes](#querying-the-index)
-   [Kompatibilitätsanforderungen](#compatibility-requirements)
    -   [Systemanforderungen](#system-requirements)
-   [Verwandte Themen](#related-topics)

## <a name="overview"></a>Übersicht

### <a name="about-the-wds-indexer"></a>Informationen zum WDS-Indexer

Bei der Erstinstallation durchsucht der Indexer die gängigsten Benutzer seitigen Dateien im Ordner "eigene Dateien", in Microsoft Outlook und in Microsoft Outlook Express-e-Mail-Ordnern und in Gruppenrichtlinie angegebene Standorte. Benutzer können auch neue Dateien und Speicherorte angeben, die der Indexer in nachfolgende Crawls einschließen (oder ausschließen) soll. Jeder enthaltene Speicherort wird durch die URL identifiziert, und der Indexer beginnt bei dieser URL und durchläuft rekursiv alle Unterordner oder Speicherorte, bis alle Elemente indiziert wurden. Ein Bereich ist ein Satz von URLs. Die Verwaltungs-APIs können von benutzerdefinierten Anwendungen verwendet werden, um Ihren Crawl Bereich zu definieren, eine Gruppe von URLs, die auf Pfade innerhalb eines Protokolls verweisen, z `file://` . b. für Ordner auf einem Laufwerk oder `mapi:// ` für MAPI-e-Mail-Speicher wie Outlook. WDS verwendet Protokollhandler, um auf die Datenspeicher und Filter zuzugreifen, um den Text und die Eigenschaften der Elemente zu analysieren und zu indizieren. Diese Daten werden dann im-Katalog gespeichert.

### <a name="about-the-wds-catalog"></a>Informationen zum WDS-Katalog

Beim WDS-Katalog handelt es sich um einen Index von Text und Eigenschaften, die von Elementen in der angegebenen e-Mail, von lokalen Laufwerken, Netzwerkressourcen und anderen lokalen Daten speichern gesammelt werden. Der Inhalt des Katalogs basiert auf von WDS festgelegten Optionen und Regeln, auf der WDS-Plattform basierende Anwendungen, Benutzereinstellungen und Gruppenrichtlinien. Es sind mehr als 200 Eigenschaften für jedes indizierte Element verfügbar, wie z. b. Erstellungsdatum, Größe und typspezifische Eigenschaften ("from" für e-Mail-Nachrichten). Eine Liste dieser Eigenschaften finden Sie in der WDS- [Schema Referenz](-search-2x-wds-schematable.md).

### <a name="about-the-search-engine-and-results"></a>Informationen zur Suchmaschine und zu Ergebnissen

Auf der WDS-Desktop Leiste oder im Windows-Explorer können Benutzer den voll Text Inhalt und die Eigenschafts Metadaten von indizierten Elementen durchsuchen. Die gleichen Arten von Such Vorgängen können auch über die Befehlszeile, über eine Webseite oder über eine benutzerdefinierte Anwendung initiiert werden. Das WDS-Suchmodul sucht nach Elementen, die mit den Suchkriterien übereinstimmen, und gibt diese als ADO-Resultsets (Microsoft ActiveX Data Objects) zurück. WDS zeigt Elemente an, die mit den Suchkriterien übereinstimmen, und kann eine umfangreiche Vorschau des Elements darstellen. Sie können Anwendungen erstellen, um die Suchabfrage abzufangen, die Suche durchzuführen und/oder das Resultset anzuzeigen.

## <a name="developing-with-wds"></a>Entwickeln mit WDS

Es gibt zwei primäre Arten der Integration in WDS: das Hinzufügen von Daten zum Index und das Abfragen des Index Inhalts zum Abrufen von Datensätzen, die den Suchkriterien entsprechen.

### <a name="adding-data-to-the-index-with-add-ins"></a>Hinzufügen von Daten zum Index mit Add-Ins

Es gibt im Grunde zwei Arten von Datenquellen: Dateisystem Speicher und nicht-Dateisystem Speicher. Eine Gruppe von Dateien in "eigene Dokumente" ist ein einfacher Dateisystem Speicher. WDS kann Informationen in den in einem solchen Dateisystem gespeicherten Dateien durchsuchen, wenn ein Filter für den Dateityp gefunden werden kann. Sie können WDS aktivieren, um einen neuen proprietären Dateityp zu indizieren, wenn Sie eine Implementierung der [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Schnittstelle für diesen Dateityp bereitstellen.

Ein nicht-Dateisystem Speicher, wie z. b. eine Datenbank, erfordert einen Protokollhandler, um WDS die Navigation innerhalb und Indizierung von Daten im Datenspeicher zu ermöglichen. Wenn Sie z. b. einen e-Mail-Client haben, in dem die Liste der empfangenen e-Mails in einer eigenen Datei gespeichert ist (z. b. PST-Dateien in Outlook), können Sie einen Protokollhandler zum Indizieren und Durchsuchen jeder einzelnen e-Mail bereitstellen, indem Sie einen Protokollhandler angeben Wenn der Datenspeicher hierarchisch ist, müssen Sie auch eine [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Schnittstelle implementieren, um die Elemente im Speicher aufzuzählen. Um eine bessere Benutzer Leistung zu erzielen, können Sie eine Shellerweiterung implementieren, um Kontextmenüs und-Symbole in der Ergebnis Ansicht bereitzustellen.

Derzeit enthält WDS Filter für mehr als 200 Typen von Elementen (einschließlich Klartext-Elemente wie HTML-, XML-und Quell Code Dateien) und verwendet dieselbe [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-und protokollhandlertechnologie wie SharePoint Services. Wenn Sie bereits Filter für proprietäre Dateitypen installiert haben, kann WDS die vorhandenen Filter Schnittstellen verwenden, um diese Daten zu indizieren.

### <a name="querying-the-index"></a>Abfragen des Indexes

WDS stellt Anwendungen mit angepassten Resultsets von Daten aus dem Index auf der Grundlage der verfügbaren Schema Werte bereit. Die Ergebnisse werden als ADO-Daten Satz Gruppen zurückgegeben. Es gibt vier Möglichkeiten, um WDS-Abfragen in eine Anwendung einzubinden, die jeweils verschiedene Anpassungs-und Stabilitäts Stufen bieten.

-   ISearchDesktop Interface: APIs in dieser Schnittstelle werden verwendet, um WDS Programm gesteuert aufzurufen, indem Sie eine Abfrage Zeichenfolge, eine Liste der zurück zugebende Spalten, Bereichs Einschränkungen ähnlich einer Structured Query Language (SQL) WHERE-Klausel und den Namen der Spalte angeben, nach der sortiert werden soll. Diese APIs sind für nativen und verwalteten Code verfügbar.
-   WDS-ActiveX-Steuerelement: dieses Steuerelement zeichnet die WDS-Suchschnittstelle und verwaltet das Suchen und Anzeigen von Ergebnissen. Diese Methode ist einfacher als die Verwendung der APIs, aber weniger flexibel. Um dieses Steuerelement in einer Microsoft Visual Studio Anwendung zu verwenden, navigieren Sie **im Menü Extras** zum Dialogfeld **Toolbox Elemente auswählen** , und fügen Sie der **Toolbox** auf der Registerkarte **com-Komponenten** "Windows Desktop Search-results Viewer" hinzu. Fügen Sie dann das Steuerelement dem Formular hinzu, in das Sie es einschließen möchten. Das WDS-ActiveX-Steuerelement ist nur mit WDS 2. x und 3. x unter Windows XP kompatibel.
-   Befehlszeilenparameter: Anwendungen können die ausführbare WDS-Datei mit verschiedenen Parametern aufrufen, um Ergebnisse zu suchen und anzuzeigen. Dadurch wird ein WDS-Fenster mit den angezeigten Ergebnissen geöffnet. Dies ist die einfachste Möglichkeit zum Hinzufügen von Suchfunktionen zu einer Anwendung, jedoch nicht zur aufrufenden Anwendung, um Informationen darüber zu erfahren, was der Benutzer innerhalb des WDS-Fensters vornimmt.
-   WDS-Browserhilfsobjekt (BHO): ähnlich können Webseiten das BHO verwenden, um Abfragen an WDS oder die registrierte Suchanwendung zu senden. Nach der Überprüfung der Webseiten-URL anhand der WDS-Domänen sicheren Liste führt WDS entweder die Abfrage aus und zeigt die Ergebnisse mit der Standard Suchschnittstelle an oder übergibt die Abfrage an die registrierte Suchanwendung.

Benutzer können die [Erweiterte Abfrage Syntax](-search-2x-wds-aqsreference.md) verwenden, um den Katalog effektiver abzufragen, indem Sie den Suchbereich Steuern und Suchparameter mit booleschen Operatoren kombinieren. Ein Benutzer könnte z. b. eine Anlage in einer e-Mail von John suchen, die entweder "Project Schedule" oder "Project Plan" mit einer Abfrage wie der folgenden enthält: `from:John isattachment:true "project schedule" OR "project plan"` .

## <a name="compatibility-requirements"></a>Kompatibilitätsanforderungen

WDS 2.6.5 ist nur für Windows 2000, Windows Server 2003 und Windows XP verfügbar. Bei WDS handelt es sich um einen separaten Download, der von Microsoft kostenlos zur Verfügung gestellt wird. Sie muss installiert und für die Indizierung des Benutzerkontos verwendet werden, bevor die für WDS 2.6.5 erstellten Anwendungen funktionieren.

### <a name="system-requirements"></a>Systemanforderungen

Folgendes ist erforderlich, um die Windows-Desktop Suche zu verwenden:

-   Windows Internet Explorer oder höher.
-   Wenn Sie Ihre e-Mail-Nachrichten in den Katalog einschließen möchten, müssen Sie entweder Microsoft Microsoft Outlook 2000 oder höher oder Microsoft Outlook Express 6,0 oder höher haben.
-   Für die vollständige Vorschau von Microsoft Microsoft Office-Dokumenten in der Ergebnis Ansicht ist Office XP oder höher erforderlich.
-   Minimaler Pentium 500 MHz-Prozessor (1 GHz empfohlen).
-   Windows XP, Windows 2000 SP4 oder höher oder Windows Server 2003 Service Pack 1.
-   Mindestens 128 MB RAM (256 MB empfohlen).
-   500 MB freier Festplattenspeicher empfohlen. Die Größe des Indexes hängt davon ab, wie viel Inhalt indiziert wurde.
-   1024 x 768 Bildschirmauflösung empfohlen.

## <a name="related-topics"></a>Verwandte Themen

1.  Abfragen des Indexes

    -   [Programm gesteuertes Aufrufen von WDS (über ISearchDesktop)](-search-2x-wds-callingwdsprogrammatically.md)
    -   [Aufrufen von WDS von Webseiten](-search-2x-wds-browserhelpobject.md)
    -   [Aufrufen von WDS über die Befehlszeile](-search-2x-wds-fromcommandline.md)

2.  [Erweitern des Indexes (Übersicht)](-search-2x-wds-extendingtheindex.md)

    -   [Entwickeln von IFilter-Add-ins](-search-2x-wds-ifilteraddins.md)
    -   [Entwickeln von Protokoll Handlern](-search-2x-wds-phaddins.md)

3.  Allgemeine Verweise

    -   [WDS-Schema](-search-2x-wds-schematable.md)
    -   [Erweiterte Abfragesyntax](-search-2x-wds-aqsreference.md)
    -   [Von WDS erkannte Typen](-search-2x-wds-perceivedtype.md)

 

 