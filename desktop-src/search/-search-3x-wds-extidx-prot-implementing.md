---
description: Einige Anwendungen speichern ihre Elemente in Datenbanken oder benutzerdefinierten Dateitypen.
ms.assetid: 0e2b7b4b-ae87-4092-b924-6191cdf42c9b
title: Grundlegendes zu Protokoll Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 28c171c5790e47bbf624d9107a5ca5b3dc0b9fd4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343244"
---
# <a name="understanding-protocol-handlers"></a>Grundlegendes zu Protokoll Handlern

Einige Anwendungen speichern ihre Elemente in Datenbanken oder benutzerdefinierten Dateitypen. Obwohl der Name und die Eigenschaften der Datei in Windows Search indiziert werden können, hat Windows keine Kenntnis über den Inhalt der Datei. Folglich können solche Elemente in der Windows-Shell nicht indiziert oder verfügbar gemacht werden. Durch Erstellen eines Protokoll Handlers können Sie diese Elemente für die Indizierung verfügbar machen. Sie können auch ein zusammengesetztes Dateiformat, z. b. eine ZIP-Datei, indizieren.

Dieses Thema ist wie folgt organisiert:

-   [Indizieren von Daten speichern mit Protokoll Handlern](#indexing-data-stores-with-protocol-handlers)
    -   [Shelldatenspeicher](#shell-data-stores)
    -   [Protokollhandler](#protocol-handlers)
    -   [Filter und Protokollhandler](#filters-and-protocol-handlers)
-   [Indizieren eines zusammengesetzten Datei Formats](#indexing-a-compound-file-format)
-   [Zugehörige Themen](#related-topics)

## <a name="indexing-data-stores-with-protocol-handlers"></a>Indizieren von Daten speichern mit Protokoll Handlern

Wenn Benutzer Legacy Datenbanken, e-Mail-Speicher oder andere Datenstrukturen durchsuchen müssen, die nicht von Windows Search unterstützt werden, sollten Sie zunächst feststellen, ob ein Protokollhandler für diesen Datenspeicher bereits vorhanden ist, z. b. für die Verwendung mit einer anderen Anwendung wie SharePoint Server. Wenn dies der Fall ist, können Sie diesen Protokollhandler auf dem System installieren. Windows Search-Protokollhandler verwenden Designspezifikationen ähnlich wie SharePoint Server, und Sie können häufig austauschbar verwendet werden.

Weitere Informationen zur Bereitstellung von Search Server 2008 mit Office SharePoint Server 2007 finden Sie unter [Federated Search \[ Search \] Server 2008](/previous-versions/office/bb931109(v=office.14)).

### <a name="shell-data-stores"></a>Shelldatenspeicher

Bevor Entwickler neuer Dateiformate und Datenspeicher von Drittanbietern diese Formate und Speicher in den Abfrage Ergebnissen in Windows-Explorer anzeigen können, muss der Entwickler eine shelldatenquelle implementieren. Eine shelldatenquelle ist eine Komponente, die verwendet wird, um den Shellnamespace zu erweitern und Elemente in einem Datenspeicher verfügbar zu machen. Ein Datenspeicher ist ein Repository mit Daten. Ein Datenspeicher kann für das shellprogrammierungs Modell als Container verfügbar gemacht werden, der eine shelldatenquelle verwendet. Die Elemente in einem Datenspeicher können vom Windows-Suchsystem mithilfe eines Protokoll Handlers indiziert werden. Der Protokollhandler implementiert das Protokoll für den Zugriff auf eine Inhaltsquelle im systemeigenen Format. Die [**isearchprotocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) -und [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) -Schnittstellen werden verwendet, um einen benutzerdefinierten Protokollhandler zu implementieren, um die Datenquellen zu erweitern, die indiziert werden können.

Wenn Sie möchten, dass die Abfrageergebnisse in Windows-Explorer angezeigt werden, müssen Sie eine Shell-Datenquelle implementieren, bevor Sie einen Protokollhandler zum Erweitern des Indexes erstellen können. Wenn allerdings alle Abfragen Programm gesteuert werden (z. b. über OLE DB) und vom Code der Anwendung anstelle der Shell interpretiert werden, ist ein Shellnamespace, der weiterhin bevorzugt wird, nicht unbedingt erforderlich.

> [!Note]  
> Eine shelldatenquelle wird manchmal als Shellnamespace Erweiterung bezeichnet. Ein Handler wird manchmal als Shellerweiterung oder Shellerweiterungs Handler bezeichnet.

 

Wenn Sie möchten, dass Benutzer Ihre Suchergebnisse innerhalb von Windows-Explorer anzeigen, müssen Sie einen Protokollhandler und mindestens eines der folgenden Add-Ins erstellen:

-   Kontextmenü Handler
-   Symbol Handler
-   Ein anderer Dateityp des Datei Handlers

Eine Liste der Handler, die von dem Entwickler Szenario identifiziert werden, das Sie zu erreichen versuchen, finden Sie unter "Übersicht über Handler" in der [Windows-Suche als Entwicklungsplattform](-search-3x-wds-development-ovr.md). Weitere Informationen zum Erstellen von Handlern finden Sie unter [Registrieren von Shellerweiterungen](../shell/reg-shell-exts.md), [Kontextmenüs](/previous-versions/windows/desktop/legacy/cc144169(v=vs.85))und [Dateityp Handlern](../shell/fa-file-extensions.md).

### <a name="protocol-handlers"></a>Protokollhandler

Wenn es sich bei dem Datenspeicher ebenfalls um einen Container handelt (z. b. um einen Dateisystem Ordner), müssen Sie einen Filter implementieren, um die URLs im Container aufzuzählen. Wenn der Datenspeicher Daten oder andere Dateitypen als einen der von Windows Search unterstützten 200-Dateitypen enthält, müssen Sie einen Filter implementieren, um auf den Inhalt von Elementen im Speicher zuzugreifen und ihn zu indizieren. Windows Search verwendet die Protokollhandler-und [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Technologie, die der von SharePoint Server verwendeten ähnelt. Wenn Sie bereits Filter für einen bestimmten Speicher und Dateityp auf dem zu indizierenden System installiert haben, kann Windows Search die vorhandenen Schnittstellen verwenden, um diese Daten zu indizieren.

Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md). Konzeptionelle Informationen zu Filter Handlern finden Sie unter [entwickeln von Filter Handlern](-search-ifilter-conceptual.md).

### <a name="filters-and-protocol-handlers"></a>Filter und Protokollhandler

Protokollhandler ermöglichen dem Windows Search-Indexer Zugriff auf Datenspeicher, sodass der Indexer die Knoten eines Datenspeichers durchforsten und relevante Informationen in den Index extrahieren kann. Windows Search ist beispielsweise mit Protokoll Handlern für Dateisystem Speicher und einigen Versionen von Microsoft Outlook-Daten speichern ausgeliefert. Beim Indizieren von Outlook-e-Mails durchsucht der Protokollhandler alle Nachrichten in einem Satz von Outlook-Ordnern und extrahiert Informationen aus jeder Nachricht und Anlage. Diese Informationen werden an den Indexer für die Einbindung in den Windows Search-Katalog übermittelt.

Informationen zu Übersichten des Katalog-Managers und des Crawl Scope-Managers (CSM) finden [Sie unter Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md) und [Verwenden des Crawl Scope-Managers](-search-3x-wds-extidx-csm.md).

## <a name="indexing-a-compound-file-format"></a>Indizieren eines zusammengesetzten Datei Formats

Ein zusammengesetztes Dateiformat kann indiziert werden, damit einzelne Elemente in der Datei als einzelne Ergebnisse zurückgegeben werden können. Bei einem Verbund Dateiformat, z. b. einer komprimierten Datei mit der Dateinamenerweiterung ". zip", handelt es sich im Wesentlichen um einen Datenspeicher, der für Indizierungs Zwecke als solche Im folgenden Beispiel wird eine ZIP-Datei im Dateisystem-Namespace (file://c:/Test/test.zip) angezeigt, in der Unterordner und einzelne Elemente vorhanden sind.

``` syntax
Test.zip 

    |-folder1 

    |    |-folder2 

    |           |- FileX.txt 

    |- FileY.doc
```

Der Datei Protokollhandler ermittelt, ob test.zip file://c:/Test/durch Überwachen von Dateisystem-Änderungs Protokollen geändert wird, und Ruft einen [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) auf, der für ZIP-Dateien in dieser Datei registriert ist, wenn sich die Datei ändert, aber keine Kenntnis der internen Struktur der ZIP-Datei selbst hat.

Sie müssen den Indexer darüber informieren, dass das Verbund Dateiformat ein Datenspeicher ist. Dies ist erforderlich, damit einzelne Elemente indiziert und als eindeutige Entitäten abgerufen werden. Nachdem Sie eine shelldatenquelle implementiert und die folgenden Schritte ausgeführt haben, verfügen Sie über einen Protokollhandler, der die Daten aus einem Verbund Dateiformat (ZIP-Datei) verarbeiten und als einzelne Elemente verfügbar machen kann.

**So informieren Sie den Indexer, dass eine Verbund Datei ein Datenspeicher ist:**

1.  Erstellen Sie einen Protokollhandler (mit [**isearchprotocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) oder [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2)) für ZIP-Dateien, die die Möglichkeit haben, eine Bindung an die Quelldatei herzustellen. Weitere Informationen finden Sie unter [Installieren und Registrieren von Protokoll Handlern](-search-3x-wds-ph-install-registration.md).

    Beispielsweise können Sie einen escapepfad zur ZIP-Datei als Stamm Ordnernamen verwenden und dann eine Hierarchie Syntax wie jedes andere Dateiformat verwenden.

    ``` syntax
    .zip:///escapedPathTo.zipFile/.zipfolder/.../.zipfile
    ```

    Wenn Sie die obigen Beispiel Daten für c: \\ Test \\test.zip verwenden, lauten die eindeutigen URLs wie folgt. Mit diesen URLs verfügt der Protokollhandler über die erforderlichen Informationen, um die ZIP-Datei zu binden und die untergeordneten URLs einschließlich der inneren Dateien aufzulisten, damit Sie an die Filter ". doc" und ". txt" gebunden und indiziert werden können.

    ``` syntax
      

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/ 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/FileY.Doc 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2 

    .zip:///FILE:%2f%2f%2fc:%2ftest%2ftest.zip/folder1/folder2/FileX.txt
    ```

2.  Stellen Sie sicher, dass der Protokollhandler die folgenden beiden Bedingungen erfüllt:
    -   Die Stamm-URLs für eine ZIP-Datei sollten die pkey- \_ Suche " \_ iscloseddirectory" ([System. search. iscloseddirectory](../properties/props-system-search-iscloseddirectory.md)) in den URLs ausgeben, bei denen es sich um die URLs der Stamm-ZIP-Datei handelt. Beispiel:. zip:///file:%2F%2F%2fc:%2ftest% 2ftest.zip/sollte iscloseddirectory = **true** ausgeben. Dies weist den Indexer darauf hin, dass das Datum, an dem diese URL nicht geändert wurde, keine der untergeordneten URLs verarbeiten muss.
    -   Jede untergeordnete URL für diese URL sollte die pkey- \_ Suche " \_ isfullyall" ([System. search. isfullyenthaltige](../properties/props-system-search-isfullycontained.md)) für die untergeordneten URLs der URL "root. zip" ausgeben. Normalerweise behandelt der Indexer am Ende eines inkrementellen Crawls alle nicht besuchten URLs als Elemente, die gelöscht werden sollen. Die Stamm-URL sollte jedoch nicht von der root. zip-Datei verarbeitet werden, da sich nichts geändert hat. Wenn diese Eigenschaft als **true** ausgegeben wird, wird dem Indexer mitgeteilt, dass diese URL nicht gelöscht werden sollte, wenn diese URL nicht am Ende eines inkrementellen Crawls verarbeitet wurde. Sie wird nur gelöscht, wenn sich das Stamm Element geändert hat und es nicht besucht wird.

Für Windows Search ist eine Startseite für ein Protokoll erforderlich, um zu wissen, welche URLs inkrementell durchsucht werden sollen und welche URLs ignoriert werden sollen, wenn Sie gefunden werden. Wir können jedoch nicht mit einer URL für jede Zip-Datei beginnen, da wir nicht wissen, wo sich die einzelnen ZIP-Dateien befinden. Daher muss die URL der Startseite des ZIP-Protokoll Handlers alle Elemente im Stammverzeichnis der escapepfade aller ZIP-Dateien aufzählen können. Diese ZIP-Dateien sind nicht notwendigerweise in der Datei: Namespace und könnten eine MAPI-Typ-URL sein, die auf eine ZIP-Datei als Anlage zeigt, z. b..

**So registrieren Sie einen Stamm als Startseite:**

1.  Registrieren Sie einen Stamm, z. b.. zip:///, als Startseite, sodass alle ZIP-Dateien dort gestartet werden. Bei der Verarbeitung der root. zip:-URL sollte der Protokollhandler die Liste der untergeordneten URLs generieren, die durch Abfragen von Windows Search nach allen URLs mit System. File Extension = ". zip" ausgegeben werden.
2.  Versehen Sie diese URLs, um die Schrägstriche zu entfernen und Sie als untergeordnete URLs zurückzugeben. Eine Beispiel Abfrage zum Abrufen der gewünschten Typen könnte wie folgt aussehen.

    ``` syntax
    SELECT system.itemurl, System.DateModified FROM SystemIndex 
    WHERE System.FileExtension='.zip' OR System.MimeType='mimetypefor.zip'
    ```

3.  Wenn die Windows-Suche in regelmäßigen Abständen eine inkrementelle durch Forstung für Ihre ZIP:///-Stamm-URL durchläuft, müssen Sie die Liste der URLs, die von Windows Search bereits gewartet werden, als ZIP-URLs Wenn im systemeigenen Speicher, in dem die ZIP-Datei gespeichert wird, eine Löschung erkannt wird, wird Sie nicht in der Enumeration angezeigt, und dieser Branch der Struktur in der ZIP-Datei wird entfernt.
4.  Um eine Bindung an die ZIP-Daten eines anderen Protokoll Handlers zu erhalten, sollten Sie idealerweise den [IShellFolder](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) für diese URL durchlaufen, um die Bindung an den Speicher des Objekts herzustellen, und nicht davon ausgehen, dass es sich immer um eine Datei handelt. Auf diese Weise haben Sie die Flexibilität, mit Anlagen in e-Mail-Stores zu arbeiten, z. b..
5.  Beim Ausgeben von untergeordneten URLs für jede. zip-Datei: Verwenden Sie die pkey- \_ Suche \_ urltoindexwithmodificationtime ([System. search. urltoindexwithmodificationtime](../properties/props-system-search-urltoindexwithmodificationtime.md)), um pkey \_ DateModified ([System. DateChanged](../properties/props-system-datemodified.md)) der eigentlichen ZIP-Datei zu übergeben, sodass der Indexer die ZIP-Datei nur dann durchläuft, wenn Sie geändert wurde.

Damit Ihre ZIP-URLs sofort nach dem Erstellen oder ändern indiziert werden und nicht auf eine inkrementelle durch Forstung warten müssen, um den neuen Zustand zu ermitteln, können Sie das Dateisystem selbst für ZIP-Dateiänderungen überwachen. Ein solcher Ansatz funktioniert jedoch nicht für andere Datenspeicher, z. b. MAPI.

**So werden Ihre ZIP-URLs indiziert, wenn Sie erstellt oder geändert werden:**

1.  Erstellen Sie einen Filter (und die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle) für den ZIP-Dateityp. Weitere Informationen finden Sie unter [entwickeln von Eigenschaften Handlern für Windows Search](-search-3x-wds-extidx-propertyhandlers.md).
2.  Wenn Ihre [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Implementierung aufgerufen wird, liegt dies daran, dass diese URL erkannt oder geändert wurde. Generieren Sie dann ein Ereignis für die ZIP-URL, die für die Quell-URL geeignet ist, über die [**igathernotifyinline**](/previous-versions/windows/desktop/legacy/bb231470(v=vs.85)) -Schnittstelle. Dadurch haben Sie die Möglichkeit, dem Indexer sofort mitzuteilen, dass neue Daten indiziert werden müssen, ohne auf die inkrementelle durch Forstung warten zu müssen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Entwickeln von Protokoll Handlern](-search-3x-wds-phaddins.md)
</dt> <dt>

[Installieren und Registrieren von Protokoll Handlern](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Benachrichtigen des Index von Änderungen](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Hinzufügen von Symbolen und Kontextmenüs](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Code Beispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Installieren und Registrieren von Protokoll Handlern](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[Erstellen eines Suchconnector für einen Protokoll Handler](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Debuggen von Protokoll Handlern](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
