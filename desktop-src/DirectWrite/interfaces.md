---
title: DirectWrite-Schnittstellen
description: Listet die Schnittstellen auf, die von DirectWrite definiert werden.
ms.assetid: 7075e771-ce34-4426-8c07-13e85ff4d453
keywords:
- DirectWrite, Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0297875bfe4b5f0a0610091f7330a427ed51b822
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/10/2021
ms.locfileid: "106355092"
---
# <a name="directwrite-interfaces"></a>DirectWrite-Schnittstellen

DirectWrite definiert die folgenden Schnittstellen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | BESCHREIBUNG |
|-|-|
| [**Idschreiteasynkresult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) | Stellt das Ergebnis eines asynchronen Vorgangs dar. Ein Client kann die-Schnittstelle verwenden, um auf den Abschluss des Vorgangs zu warten und das Ergebnis zu erhalten.  |
| [**Idschreitebitmaprendertarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) | Kapselt eine geräteunabhängige 32-Bit-Bitmap und einen Gerätekontext, der zum Rendern von Glyphen verwendet werden kann. |
| [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1) | Kapselt eine geräteunabhängige 32-Bit-Bitmap und einen Gerätekontext, der zum Rendern von Symbolen verwendet werden kann. |
| [**IDWriteBitmapRenderTarget2**](./dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2.md) | Kapselt eine geräteunabhängige 32-Bit-Bitmap und einen Gerätekontext, der zum Rendern von Glyphen verwendet werden kann. |
| [**Idschreitecolorglyphrunenumerator**](idwritecolorglyphrunenumerator.md) | Diese Schnittstelle ermöglicht es der Anwendung, die farbglyphe aufzählen. |
| [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) | Enumerator für eine geordnete Auflistung von Farb Glyphe. |
| [**Idschreitefactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) | Wird verwendet, um alle nachfolgenden DirectWrite-Objekte zu erstellen. Diese Schnittstelle ist die stammfactory-Schnittstelle für alle DirectWrite-Objekte. |
| [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) | Die Root Factory-Schnittstelle für alle [DirectWrite](direct-write-portal.md) -Objekte. |
| [**IDWriteFactory2**](idwritefactory2.md) | Die Root Factory-Schnittstelle für alle [DirectWrite](direct-write-portal.md) -Objekte. |
| [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) | Die Root Factory-Schnittstelle für alle [DirectWrite](direct-write-portal.md) -Objekte. |
| [**IDWriteFactory4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4) | Die Root Factory-Schnittstelle für alle DirectWrite-Objekte. |
| [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) | Die Root Factory-Schnittstelle für alle DirectWrite-Objekte. |
| [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) | Dies stellt ein Factoryobjekt dar, von dem alle DirectWrite-Objekte erstellt werden. **IDWriteFactory6** bietet neue Funktionen für die Arbeit mit Schriftarten und Schriftarten Ressourcen. |
| [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) | Diese Schnittstelle stellt ein Factoryobjekt dar, von dem alle DirectWrite-Objekte erstellt werden. **IDWriteFactory7** bietet neue Funktionen zum Arbeiten mit System Schriftarten. |
| [**Idschreiteschriftart**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | Stellt eine physische Schriftart in einer Schriftart Auflistung dar. Diese Schnittstelle wird verwendet, um Schriftart Flächen aus physischen Schriftarten zu erstellen oder um Informationen wie z. b. Schriftart Metriken oder Gesichts Namen aus vorhandenen Schriftarten abzurufen. |
| [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) | Stellt eine physische Schriftart in einer Schriftart Auflistung dar. |
| [**IDWriteFont2**](idwritefont2.md) | Stellt eine physische Schriftart in einer Schriftart Auflistung dar. |
| [**IDWriteFont3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3) | Stellt eine Schriftart in einer Schriftart Auflistung dar. |
| [**Idschreitefontcollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) | Ein Objekt, das einen Satz von Schriftarten kapselt, z. b. den auf dem System installierten Schriftarten oder den Satz von Schriftarten in einem bestimmten Verzeichnis. Die Schriftart Sammlungs-API kann verwendet werden, um zu ermitteln, welche Schriftfamilien und Schriftarten verfügbar sind, und um einige Metadaten über die Schriftarten zu erhalten. |
| [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) | Ein Objekt, das einen Satz von Schriftarten kapselt, z. b. den auf dem System installierten Schriftarten oder den Satz von Schriftarten in einem bestimmten Verzeichnis. Die Schriftart Sammlungs-API kann verwendet werden, um zu ermitteln, welche Schriftfamilien und Schriftarten verfügbar sind, und um einige Metadaten über die Schriftarten zu erhalten. |
| [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) | Diese Schnittstelle kapselt eine Reihe von Schriftarten, z. b. die auf dem System installierten Schriftarten oder den Satz von Schriftarten in einem bestimmten Verzeichnis. |
| [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) | Diese Schnittstelle kapselt eine Reihe von Schriftarten, z. b. die auf dem System installierten Schriftarten oder den Satz von Schriftarten in einem bestimmten Verzeichnis. |
| [**Idschreitefontcollectionloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) | Wird verwendet, um eine Auflistung von Schriftarten mit einem bestimmten Schlüsseltyp zu erstellen.  |
| [**Idschreitefontdownloadlistener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) | Anwendungs definierte Rückruf Schnittstelle, die Benachrichtigungen von der Schriftart Download Warteschlange empfängt ([**idschreitefontdownloadqueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) -Schnittstelle). Rückrufe erfolgen auf dem Download Thread, und Objekte müssen darauf vorbereitet sein, Aufrufe ihrer Methoden von anderen Threads jederzeit zu verarbeiten. |
| [**Idschreitefontdownloadqueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) | Schnittstelle, die Download Anforderungen für Remote Schriftarten, Zeichen, Glyphen und Schriftart Fragmente in die Warteschlange einreiht.  |
| [**Idschreitefontface**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) | Diese Schnittstelle macht verschiedene Schriftart Daten wie z. b. Metriken, Namen und Symbol Gliederungen verfügbar. Sie enthält Schriftart Typen, entsprechende Datei Verweise und Gesichts Identifizierungs Daten. |
| [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) | Enthält den Schriftart-Typ, die entsprechenden Datei Verweise und die Gesichts Identifizierungs Daten.  |
| [**IDWriteFontFace2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2) | Diese Schnittstelle enthält Schriftart Typen, entsprechende Datei Verweise und Gesichts Identifizierungs Daten. Es bietet die Möglichkeit, zu überprüfen, ob möglicherweise ein farbrenderingpfad erforderlich ist.  |
| [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) | Enthält den Schriftart-Typ, die entsprechenden Datei Verweise und die Gesichts Identifizierungs Daten. |
| [**IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4) | Enthält den Schriftart-Typ, die entsprechenden Datei Verweise und die Gesichts Identifizierungs Daten. |
| [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) | Diese Schnittstelle enthält Schriftart Typen, entsprechende Datei Verweise und Gesichts Identifizierungs Daten. Es werden neue Funktionen hinzugefügt, z. b. zwei Schriftart vergleichen, Schriftart Achsen Werte abgerufen und die zugrunde liegende Schriftart Ressource abgerufen. |
| [**Idschreitefontfakereferenzierung**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) | Stellt einen Verweis auf eine Schriftart dar. Ein eindeutig identifizier ender Verweis auf eine Schriftart, aus der Sie ein Schriftart zum Abfragen von Schriftart Metriken und zum Rendern von Schriftarten erstellen können. Ein Verweis auf eine Schriftart besteht aus einer Schriftart Datei, einem Schriftart Index für die Schriftart und einer Simulation der Schriftart. Die Datei Daten sind möglicherweise noch physisch auf dem lokalen Computer vorhanden.  |
| [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) | Stellt einen Verweis auf eine Schriftart dar. Ein eindeutig identifizier ender Verweis auf eine Schriftart, aus der Sie ein Schriftart zum Abfragen von Schriftart Metriken und zum Rendern von Schriftarten erstellen können. |
| [**Idschreitefontfallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback) | Ermöglicht den Zugriff auf Fall Back-Schriftarten aus der Schriftart Liste. |
| [**Idschreitefontfallbackbuilder**](idwritefontfallbackbuilder.md) | Ermöglicht das Erstellen von Unicode-Schriftart-Fall Back-Zuordnungen und das Erstellen eines Schriftart-Fall Back-Objekts aus diesen Zuordnungen. |
| [**Idschreitefontfamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) | Stellt eine Familie verwandter Schriftarten dar. |
| [**IDWriteFontFamily1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily1) | Stellt eine Familie verwandter Schriftarten dar. |
| [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) | Stellt eine Familie verwandter Schriftarten dar. **IDWriteFontFamily2** fügt neue Funktionen hinzu, einschließlich dem Abrufen von Schriftarten nach Schriftart Achsen Werten. |
| [**Idschreitefontfile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) | Stellt eine Schriftart Datei dar. Anwendungen (z. b. Schriftart-Manager oder Schriftart-Viewer) können [**idschreitefontfile:: Analyse**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) aufzurufen, um herauszufinden, ob eine bestimmte Datei eine Schriftart Datei ist, und ob es sich um einen Schriftart Typ handelt, der vom Schriftart System unterstützt wird. |
| [**Idschreitefontfileenumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) | Kapselt eine Auflistung von Schriftart Dateien. Das Schriftart System verwendet diese Schnittstelle, um beim Aufbau einer Schriftart Auflistung Schriftart Dateien aufzulisten. |
| [**Idschreitefontfileloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) | Behandelt das Laden von Schriftart Datei Ressourcen eines bestimmten Typs aus einem Verweis Schlüssel für eine Schriftart Datei in ein Schriftart Datei-Streamobjekt.  |
| [**Idschreitefontfilestream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) | Lädt Schriftart Datei Daten aus einem benutzerdefinierten Schriftart Datei Lade Tool.  |
| [**Idschreitefontlist**](/windows/win32/api/dwrite/nn-dwrite-idwritefontlist) | Stellt eine Liste von Schriftarten dar. |
| [**IDWriteFontList1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1) | Stellt eine Liste von Schriftarten dar. |
| [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) | Stellt eine Liste von Schriftarten dar. **IDWriteFontList2** fügt neue Funktionen hinzu, einschließlich des Abrufens des zugrunde liegenden Schriftart Satzes, der von der Liste verwendet wird. |
| [**Idschreitefontresource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) | NN-dwrite_3-idschreitefontresource |
| [**Idschreitefontset**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) | Stellt einen Schriftart Satz dar. |
| [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) | Stellt einen Schriftart Satz dar. |
| [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) | Stellt einen Schriftart Satz dar. |
| [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) | Stellt einen Schriftart Satz dar. |
| [**Idschreitefontsetbuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) | Enthält Methoden zum Entwickeln eines Schriftart Satzes. |
| [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) | Enthält Methoden zum Entwickeln eines Schriftart Satzes. |
| [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) | Enthält Methoden zum Entwickeln eines Schriftart Satzes. |
| [**Idschreitegdiinterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) | Bietet Interoperabilität mit GDI, z. b. Methoden zum Konvertieren einer Schriftart in eine LOGFONT-Struktur oder zum Konvertieren einer GDI-Schriftart Beschreibung in eine Schriftart. Sie wird auch zum Erstellen von Bitmap-renderzielobjekten verwendet. |
| [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1) | Bietet Interoperabilität mit GDI, z. b. Methoden zum Konvertieren einer Schriftart in eine LOGFONT-Struktur oder zum Konvertieren einer GDI-Schriftart Beschreibung in eine Schriftart. Sie wird auch zum Erstellen von Bitmap-renderzielobjekten verwendet. |
| [**Idschreitegeometrysink**](idwritegeometrysink.md) | [**Idwrite tegeometrysink**](idwritegeometrysink.md) ist eine **typedef** der [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) -Schnittstelle. Weitere Informationen finden Sie auf der [**ID2D1SimplifiedGeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) -Referenzseite. |
| [**Idschreiteglyphrunanalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) | Enthält Informationen auf niedriger Ebene, die zum renderischen Ausführen von Symbolen verwendet werden. |
| [**Idwrite teinlineobject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) | Umschließt eine Anwendungs definierte Inline Grafik und ermöglicht dwrite das Abfragen von Metriken, als ob die Grafik ein Symbol Inline mit dem Text wäre. |
| [**Idschreiteinmemoryfontfileloader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) | Stellt ein Schriftart Datei Lade Tool dar, das auf in-Memory-Schriftarten zugreifen kann. |
| [**Idschreitelocalfontfileloader**](idwritelocalfontfileloader.md) | Eine integrierte Implementierung der [**idschreitefontfileloader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) -Schnittstelle, die mit lokalen Schriftart Dateien arbeitet und lokale Schriftart Dateiinformationen aus dem Schriftart Datei-Verweis Schlüssel verfügbar macht. Verweise auf Schriftart Dateien, [**die mithilfe von**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) "" erstellt wurden, verwenden dieses Schriftart Datei Lade Tool. |
| [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) | Stellt eine Auflistung von Zeichen folgen dar, die nach Gebiets Schema Namen indiziert sind |
| [**Idschreitenrebersubstitution**](./idwritenumbersubstitution.md) | Enthält die entsprechenden Ziffern und numerischen Satzzeichen für ein angegebenes Gebiets Schema. |
| [**Idschreitepixelsnapping**](/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping) | Definiert die Pixel-Ausrichtungs Eigenschaften, z. b. Pixel pro DIP (Geräte unabhängiges Pixel) und die aktuelle Transformationsmatrix eines textrenderers. |
| [**Idschreiteremotefontfileloader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) | Stellt ein Schriftart Datei-Lade Tool dar, das auf Remote Schriftarten (d.h. herunterladbare Dateien) zugreifen kann.  |
| [**Idschreiteremotefontfilestream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) | Stellt einen Schriftart Datei Datenstrom dar, von Teilen, die möglicherweise nicht lokal sind.  |
| [**Idschreiterenderingparameter**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) | Stellt Text Rendering-Einstellungen wie ClearType-Ebene, erweiterten Kontrast und Gammakorrektur für die Glyphe und Filterung von Symbolen dar. Eine Anwendung ruft in der Regel ein renderingparameterobjekt ab, indem die [**idwrite-Factory:: createmonitorrenderingparameams**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) -Methode aufgerufen wird. |
| [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1) | Stellt textrenderingeinstellungen für das Glyphe und Filtern von Symbolen dar. |
| [**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2) | Stellt textrenderingeinstellungen für das Glyphe und Filtern von Symbolen dar. |
| [**IDWriteRenderingParams3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriterenderingparams3) | Stellt textrenderingeinstellungen für das Glyphe und Filtern von Symbolen dar. |
| [**Idschreitestringlist**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist) | Stellt eine Auflistung von Zeichen folgen dar, die nach Zahl indiziert werden. |
| [**Idschreitetextanalysissink**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink) | Diese Schnittstelle wird vom Client der Textanalyse implementiert, um die Ausgabe einer bestimmten Textanalyse zu erhalten.  |
| [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) | Die Schnittstelle, die Sie implementieren, um die Ausgabe der Textanalyse zu erhalten. |
| [**Idschreitetextanalysissource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) | Wird vom Client der Textanalyse implementiert, um dem Analyzer Text bereitzustellen. Dies ermöglicht die Trennung zwischen der logischen Textansicht als kontinuierlichen Datenstrom von Zeichen, die von eindeutigen Textpositionen identifiziert werden können, und dem tatsächlichen Speicher Layout von potenziell diskreten Textblöcken im Sicherungs Speicher des Clients.  |
| [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) | Die Schnittstelle, die Sie implementieren, um erforderliche Informationen für die Textanalyse bereitzustellen, wie z. b. Text und zugehörige Texteigenschaften |
| [**Idschreitetextanalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) | Analysiert verschiedene Texteigenschaften für die komplexe Skript Verarbeitung, z. b. bidirektionale (Bidi) Unterstützung für Sprachen wie Arabisch, Festlegung von Zeilenumbruch Möglichkeiten, Glyphe-Platzierung und Zahlen Ersetzung. |
| [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) | Analysiert verschiedene Texteigenschaften für die Verarbeitung komplexer Skripts. |
| [**IDWriteTextAnalyzer2**](idwritetextanalyzer2.md) | Analysiert verschiedene Texteigenschaften für die Verarbeitung komplexer Skripts. |
| [**Idschreitetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) | Die [**idwrite Test Textformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) -Schnittstelle beschreibt die Schriftart-und Absatz Eigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen.  |
| [**IDWriteTextFormat1**](idwritetextformat1.md) | Beschreibt die Schriftart-und Absatz Eigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen.  |
| [**IDWriteTextFormat2**](idwritetextformat2.md) | Beschreibt die Schriftart-und Absatz Eigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen.  |
| [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) | Beschreibt die Schriftart-und Absatz Eigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebiets Schema Informationen. |
| [**Idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) | Die [**idschreitetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) -Schnittstelle stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde. |
| [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) | Stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde. |
| [**IDWriteTextLayout2**](idwritetextlayout2.md) | Stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde. |
| [**IDWriteTextLayout3**](idwritetextlayout3.md) | Stellt einen TextBlock dar, nachdem er vollständig analysiert und formatiert wurde.  |
| [**Idschreitetextrenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) | Stellt einen Satz von Anwendungs definierten Rückrufen dar, die das Rendering von Text, Inline Objekten und Dekorationen wie unterstrichen ausführen. |
| [**IDWriteTextRenderer1**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1) | Stellt einen Satz von Anwendungs definierten Rückrufen dar, die das Rendering von Text, Inline Objekten und Dekorationen wie unterstrichen ausführen.  |
| [**Idschreitetypografie**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) | Stellt eine Schriftart typografieeinstellung dar. |