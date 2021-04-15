---
description: Filter Handler, bei denen es sich um Implementierungen der IFilter-Schnittstelle handelt, Scannen Dokumente nach Text und Eigenschaften.
ms.assetid: 2ee9ea19-ae03-4f14-8f06-f8aa670e204e
title: Grundlegendes zu Filter Handlern in Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e49cc1d3e479ae03645665618c60a33bdcfe19ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525520"
---
# <a name="understanding-filter-handlers-in-windows-search"></a>Grundlegendes zu Filter Handlern in Windows Search

Filter Handler, bei denen es sich um Implementierungen der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle handelt, Scannen Dokumente nach Text und Eigenschaften. Filter Handler extrahieren Textabschnitte aus diesen Elementen, Filtern eingebettete Formatierungen und behalten Informationen zur Position des Texts bei. Sie extrahieren auch Blöcke von Werten, die Dokumenteigenschaften sind. **IFilter** ist die Grundlage für das Entwickeln von Anwendungen höherer Ebene, z. b. dokumentindexer und Anwendungs unabhängige Viewer.

Dieses Thema ist wie folgt organisiert:

- [Informationen zur IFilter-Schnittstelle](#about-the-ifilter-interface)
  - [Isolations Prozess](#isolation-process)
  - [IFilter-DLLs](#ifilter-dlls)
  - [IFilter-Struktur](#ifilter-structure)
  - [Nativer Code](#native-code)
- [Suchen des IFilter-Klassen Bezeichners](#finding-the-ifilter-class-identifier)
  - [IFilter:: GetChunk-und locale-Code Bezeichner](#ifiltergetchunk-and-locale-code-identifiers)
- [Weitere Ressourcen](#additional-resources)
- [Zugehörige Themen](#related-topics)

## <a name="about-the-ifilter-interface"></a>Informationen zur IFilter-Schnittstelle

Microsoft Windows Search verwendet Filter zum Extrahieren des Inhalts von Elementen für die Aufnahme in einen Volltextindex. Sie können Windows Search erweitern, um neue oder proprietäre Dateitypen zu indizieren, indem Sie Filter zum Extrahieren des Inhalts schreiben und Eigenschaften Handler, um die Eigenschaften von Dateien zu extrahieren.

Die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle ist so konzipiert, dass Sie den spezifischen Anforderungen der Volltext-Suchmaschinen entspricht. Volltext-Suchmaschinen wie Windows Search nennen die **IFilter** -Methoden, um Text-und Eigenschafts Informationen zu extrahieren und Sie einem Index hinzuzufügen. Windows Search unterbricht die Ergebnisse der zurückgegebenen [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext) -Methode in Wörter, normalisiert Sie und speichert Sie in einem Index. Falls verfügbar, verwendet die Suchmaschine den Sprachcode Bezeichner (Language Code Identifier, LCID) eines Text Abschnitts, um die sprachspezifische Wörter Trennung und-Normalisierung auszuführen.

Windows Search verwendet drei Funktionen, die in der folgenden Tabelle beschrieben werden, um auf registrierte Filter Handler (Implementierungen der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle) zuzugreifen. Diese Funktionen sind besonders nützlich, wenn der Filter Handler eines eingebetteten Objekts geladen und gebunden wird.

| Funktion               | BESCHREIBUNG                                                                                                                                                                                               |
|------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Loadifilter            | Ruft einen Zeiger auf den [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ab, der für den angegebenen Inhaltstyp am besten geeignet ist.                                                                                            |
| Bindifilterfromstorage | Ruft einen Zeiger auf den [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ab, der sich am besten für den Inhalt eignet, der in einem [IStorage-Schnittstellen](/windows/win32/api/objidl/nn-objidl-istorage) Objekt enthalten ist. |
| Bindifilterfromstream  | Ruft einen Zeiger auf den [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ab, der am besten für eine angegebene Klassen-ID (CLSID) geeignet ist, die aus einer Datenstrom Variablen abgerufen wurde.                                                 |

Die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle verfügt über fünf Methoden, die in der folgenden Tabelle beschrieben werden.

| Methode                                                    | BESCHREIBUNG                                                                                                        |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| [**IFilter:: init**](/windows/win32/api/filter/nf-filter-ifilter-init)          | Initialisiert eine Filter Sitzung.                                                                                   |
| [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk)     | Positioniert [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) am Anfang des ersten oder nächsten Blocks und gibt einen Deskriptor zurück. |
| [**IFilter:: gettext**](/windows/win32/api/filter/nf-filter-ifilter-gettext)       | Ruft Text aus dem aktuellen Segment ab.                                                                             |
| [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue)     | Ruft Werte aus dem aktuellen Segment ab.                                                                           |
| [**IFilter:: BindRegion**](/windows/win32/api/filter/nf-filter-ifilter-bindregion) | Ruft eine Schnittstelle ab, die den angegebenen Teil des Objekts darstellt. Für die zukünftige Verwendung reserviert.                      |

### <a name="isolation-process"></a>Isolations Prozess

Die Windows-Suche führt IFilters im Sicherheitskontext des lokalen Systems mit eingeschränkten Rechten aus. In diesem [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) Host-Isolations Prozess werden eine Reihe von rechten entfernt:

- Eingeschränkter Code
- Jeder
- Lokal
- Interactive
- Authentifizierte Benutzer
- Integrierte Benutzer
- Sicherheits-ID (SID) des Benutzers

Das Entfernen dieser Rechte bedeutet, dass die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle keinen Zugriff auf das Datenträger System oder das Netzwerk oder auf eine Benutzeroberfläche oder Zwischenablage Funktionen hat. Außerdem wird der Isolations Prozess unter einem Job-Objekt ausgeführt, das verhindert, dass untergeordnete Prozesse erstellt werden, und es wird ein Grenzwert von 100 MB für das Workingset erzwungen. der Host Isolations Prozess der **IFilter** -Schnittstelle erhöht die Stabilität der Indizierungs Plattform, weil falsch implementierte Filter von Drittanbietern möglich sind.

> [!NOTE]  
> Filter Handler müssen geschrieben werden, um Puffer zu verwalten und ordnungsgemäß Stapel zu stellen. Alle Zeichen folgen Kopien müssen über explizite Überprüfungen zum Schutz vor Pufferüberläufen verfügen. Sie sollten immer die zugeordnete Größe des Puffers überprüfen. Sie sollten immer die Größe der Daten mit der Größe des Puffers testen.

### <a name="ifilter-dlls"></a>IFilter-DLLs

[**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) DLLs implementieren die **IFilter** -Schnittstelle, um es einem Client zu ermöglichen, Text-und Eigenschafts Wert Informationen aus einem Dateityp, einer Klasse oder einem erkannten Typ zu extrahieren. Der Windows Search-Filterprozess **SearchFilterHost.exe** an den **IFilter** gebunden, der für die Klasse, den wahrgenommenen Typ oder die Namenserweiterung des Elements registriert ist.

### <a name="ifilter-structure"></a>IFilter-Struktur

Jeder [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ist eine DLL-Datei, die einen in-Process-Component Object Model (com)-Server implementiert, um die angegebenen Filterfunktionen bereitzustellen. In der folgenden Abbildung wird die Gesamtstruktur einer typischen **IFilter** -DLLs veranschaulicht. Ein komplexeres Beispiel könnte mehr als eine **IFilter** -Klasse implementieren.

![Diagramm der Struktur einer typischen IFilter-DLL](images/ifilter-structure.png)

### <a name="native-code"></a>nativer Code

Filter müssen in nativem Code geschrieben werden, da bei dem Prozess, in dem mehrere Add-Ins ausgeführt werden, mögliche Common Language Runtime (CLR)-Versions Probleme aufgetreten sind. In Windows 7 und höher und höher werden in verwaltetem Code geschriebene Filter explizit blockiert.

## <a name="finding-the-ifilter-class-identifier"></a>Suchen des IFilter-Klassen Bezeichners

Die Klasse der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -dll wird unter dem PersistentHandler-Registrierungsschlüssel registriert. Im folgenden Beispiel wird für HTML-Dateien veranschaulicht, wie die **IFilter** -dll für ein HTML-Dokument gefunden wird. In diesem Beispiel wird die Logik befolgt, ähnlich der, die vom System verwendet wird, um den einem Element zugeordneten **IFilter** zu suchen.

1. Überprüfen Sie, ob die Erweiterung für den Typ der Dateien, die die dll filtert, über einen PersistentHandler verfügt, der unter dem Registrierungs Eintrag \\ HKEY Local Machine Machines registriert ist \_ \_ \\ \\ . Lassen Sie uns diesen Schlüssel verwenden `Value1` . Wenn dieser Eintrag bereits vorhanden ist, fahren Sie mit Schritt 4 dieses Verfahrens fort, und verwenden Sie diesen `Value1` Schlüssel. Die Werte sind vom Typ reg \_ SZ.

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             .htm
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

2. Wenn kein PersistentHandler für die Erweiterung registriert ist, suchen Sie die CLSID, die dem Dokumenttyp zugeordnet ist, unter dem Registrierungs Eintrag \\ HKEY \_ local \_ Machine \\ Machines \\ . Lassen Sie uns diesen Schlüssel verwenden `Value2` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                CLSID
                   {25336920-03F9-11CF-8FD0-00AA00686F13}
```

3. Bestimmen Sie, ob ein PersistentHandler für die CLSID registriert ist. `Value2`Suchen Sie die in Schritt 2 festgelegte Verwendung von PersistentHandler für den \\ HKEY \_ local \_ Machine \\ \\ Classes \\ CLSID \\ value2 Entry. Lassen Sie uns diesen Schlüssel verwenden `Value3` .

```
    \HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             htmlfile
                 = Class for WWW HTML files
                PersistentHandler
                   {EEC97550-47A9-11CF-B952-00AA0051FE20}
```

4. Bestimmen Sie die GUID des persistenten [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Handlers. Suchen `Value1` Sie `Value3` unter Verwendung von und nach der GUID des beständigen **IFilter** -Handlers für den Dokumenttyp. Der Wert unter dem Registrierungs Eintrag \\ HKEY \_ local \_ Machine \\ \\ Classes \\ CLSID \\ value1 oder 3 \\ persistentaddinsregistered \\ 89bcb740-6119-101A-bcb7-00dd010655af "/> gibt die **IFilter** PersistentHandler-GUID für diesen Dokumenttyp aus. Lassen Sie uns diesen Schlüssel verwenden `Value4` . In diesem Beispiel lautet die GUID der **IFilter** -Schnittstelle 89bcb740-6119-101A-bcb7-00dd010655af.

```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Classes
             {EEC97550-47A9-11CF-B952-00AA0051FE20}
                 = HTML File Persistent Handler
                    Data type         REG_SZ
                        PersistentAddinsRegistered
                        {89BCB740-6119-101A-BCB7-00DD010655AF}

                    Data type         REG_SZ
                        default = {E0CA5340-4534-11CF-B952-00AA0051FE20}
```

> [!NOTE]  
> In diesem Beispiel wird die [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -dll für HTML-Dokumente nlhtml.dll.

### <a name="ifiltergetchunk-and-locale-code-identifiers"></a>IFilter:: GetChunk-und locale-Code Bezeichner

Die LCID von Text kann innerhalb einer einzelnen Datei geändert werden. Beispielsweise kann der Text eines Anweisungs Handbuchs zwischen Englisch (en-US) und Spanisch (es) wechseln, oder der Text kann ein einzelnes Wort in einer anderen Sprache als der Primärsprache enthalten. In jedem Fall muss Ihr [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) jedes Mal, wenn die LCID geändert wird, einen neuen Block starten. Da die LCID verwendet wird, um eine geeignete Wörter Trennung auszuwählen, ist es sehr wichtig, dass Sie diese ordnungsgemäß identifizieren. Wenn der **IFilter** das Gebiets Schema des Texts nicht ermitteln kann, sollte er eine LCID von 0 (null) mit dem Block zurückgeben. Wenn eine LCID 0 (null) zurückgegeben wird, verwendet die Windows-Suche die Technologie zur automatischen Erkennung von Sprachen (LAD), um die Gebiets Schema-ID des Blocks zu ermitteln. Wenn die Windows-Suche keine Entsprechung findet, wird standardmäßig das Standard Gebiets Schema des Systems (durch Aufrufen der [getsystemdefaultlocalename-Funktions](/windows/win32/api/winnls/nf-winnls-getsystemdefaultlocalename) Funktion) verwendet. Weitere Informationen finden Sie unter [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk), [**Chunk \_ breaktype**](/windows/win32/api/filter/ne-filter-chunk_breaktype), [**chunkstate**](/windows/win32/api/filter/ne-filter-chunkstate)und [**stat Block \_**](/windows/win32/api/filter/ns-filter-stat_chunk).

Wenn Sie das Dateiformat Steuern und es derzeit keine Gebiets Schema Informationen enthält, sollten Sie eine Benutzerfunktion hinzufügen, um die ordnungsgemäße Gebiets Schema Identifizierung zu aktivieren. Wenn eine nicht übereinstimmende Wörter Trennung verwendet wird, kann dies zu einer schlechten Abfrageleistung für den Benutzer führen. Weitere Informationen finden Sie unter [**iwordbreaker**](/windows/desktop/api/Indexsrv/nn-indexsrv-iwordbreaker).

> [!NOTE]  
> Filter sind Dateitypen zugeordnet, die durch Dateinamen Erweiterungen, MIME-Typen oder CLSIDs bezeichnet werden. Obwohl ein Filter mehrere Dateitypen verarbeiten kann, kann jeder Typ nur mit einem einzigen Filter verwendet werden.

## <a name="additional-resources"></a>Weitere Ressourcen

- Das in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample7)verfügbare [ifiltersample](-search-sample-ifiltersample.md) -Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.
- Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).
- Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).
- Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".

## <a name="related-topics"></a>Zugehörige Themen

[Entwickeln von Filter Handlern](-search-ifilter-conceptual.md)

[Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search](-search-3x-wds-extidx-filters.md)

[Zurückgeben von Eigenschaften aus einem Filter Handler](-search-ifilter-property-filtering.md)

[Filtern von Handlern, die mit Windows ausgeliefert werden](-search-ifilter-implementations.md)

[Implementieren von Filter Handlern in Windows Search](-search-ifilter-constructing-filters.md)

[Registrieren von Filter Handlern](-search-ifilter-registering-filters.md)

[Testen von Filter Handlern](-search-ifilter-testing-filters.md)
