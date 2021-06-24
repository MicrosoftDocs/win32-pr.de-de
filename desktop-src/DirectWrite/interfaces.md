---
title: DirectWrite-Schnittstellen
description: Listet die von DirectWrite definierten Schnittstellen auf.
ms.assetid: 7075e771-ce34-4426-8c07-13e85ff4d453
keywords:
- DirectWrite,Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ff423289eb76a3506edb3537875a99a364be457
ms.sourcegitcommit: 749dea42142dec076d41a8f26cb57ae8db46e848
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/24/2021
ms.locfileid: "112588039"
---
# <a name="directwrite-interfaces"></a>DirectWrite-Schnittstellen

DirectWrite definiert die folgenden Schnittstellen.

## <a name="in-this-section"></a>In diesem Abschnitt

| Thema | Beschreibung |
|-|-|
| [**IDWriteAsyncResult**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteasyncresult) | Stellt das Ergebnis eines asynchronen Vorgangs dar. Ein Client kann die -Schnittstelle verwenden, um auf den Abschluss des Vorgangs zu warten und das Ergebnis zu erhalten.  |
| [**IDWriteBitmapRenderTarget**](/windows/win32/api/dwrite/nn-dwrite-idwritebitmaprendertarget) | Kapselt eine geräteunabhängige 32-Bit-Bitmap und einen Gerätekontext, der zum Rendern von Glyphen verwendet werden kann. |
| [**IDWriteBitmapRenderTarget1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritebitmaprendertarget1) | Kapselt eine geräteunabhängige 32-Bit-Bitmap und einen Gerätekontext, die Sie zum Rendern von Glyphen verwenden können. |
| [**IDWriteBitmapRenderTarget2**](/windows/windows-app-sdk/api/win32/dwrite_3/nn-dwrite_3-idwritebitmaprendertarget2) | Kapselt eine geräteunabhängige 32-Bit-Bitmap und einen Gerätekontext, der zum Rendern von Glyphen verwendet werden kann. |
| [**IDWriteColorGlyphRunEnumerator**](idwritecolorglyphrunenumerator.md) | Mit dieser Schnittstelle kann die Anwendung die Farbglyphenläufe aufzählen. |
| [**IDWriteColorGlyphRunEnumerator1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritecolorglyphrunenumerator1) | Enumerator für eine geordnete Auflistung von Farbglyphenläufen. |
| [**IDWriteFactory**](/windows/win32/api/dwrite/nn-dwrite-idwritefactory) | Wird verwendet, um alle nachfolgenden DirectWrite-Objekte zu erstellen. Diese Schnittstelle ist die Stamm-Factoryschnittstelle für alle DirectWrite-Objekte. |
| [**IDWriteFactory1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefactory1) | Die Stamm-Factoryschnittstelle für alle [DirectWrite-Objekte.](direct-write-portal.md) |
| [**IDWriteFactory2**](idwritefactory2.md) | Die Stamm-Factoryschnittstelle für alle [DirectWrite-Objekte.](direct-write-portal.md) |
| [**IDWriteFactory3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory3) | Die Stamm-Factoryschnittstelle für alle [DirectWrite-Objekte.](direct-write-portal.md) |
| [**IDWriteFactory4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory4) | Die Stamm-Factoryschnittstelle für alle DirectWrite-Objekte. |
| [**IDWriteFactory5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory5) | Die Stamm-Factoryschnittstelle für alle DirectWrite-Objekte. |
| [**IDWriteFactory6**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory6) | Dies stellt ein Factoryobjekt dar, aus dem alle DirectWrite-Objekte erstellt werden. **IDWriteFactory6 fügt** neue Funktionen für die Arbeit mit Schriftarten und Schriftartressourcen hinzu. |
| [**IDWriteFactory7**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefactory7) | Diese Schnittstelle stellt ein Factoryobjekt dar, aus dem alle DirectWrite-Objekte erstellt werden. **IDWriteFactory7 fügt** neue Funktionen für die Arbeit mit Systemschriftarten hinzu. |
| [**IDWriteFont**](/windows/win32/api/dwrite/nn-dwrite-idwritefont) | Stellt eine physische Schriftart in einer Schriftartauf auflistung dar. Diese Schnittstelle wird verwendet, um Schriftartgesichter aus physischen Schriftarten zu erstellen oder Informationen wie Schriftartmetriken oder Gesichtsnamen aus vorhandenen Schriftartgesichtern abzurufen. |
| [**IDWriteFont1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefont1) | Stellt eine physische Schriftart in einer Schriftartauf auflistung dar. |
| [**IDWriteFont2**](idwritefont2.md) | Stellt eine physische Schriftart in einer Schriftartauf auflistung dar. |
| [**IDWriteFont3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefont3) | Stellt eine Schriftart in einer Schriftartauf auflistung dar. |
| [**IDWriteFontCollection**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollection) | Ein Objekt, das eine Gruppe von Schriftarten kapselt, z. B. den Satz von Schriftarten, die auf dem System installiert sind, oder den Satz von Schriftarten in einem bestimmten Verzeichnis. Die Api für die Schriftartsammlung kann verwendet werden, um zu entdecken, welche Schriftfamilien und Schriftarten verfügbar sind, und um einige Metadaten zu den Schriftarten zu erhalten. |
| [**IDWriteFontCollection1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection1) | Ein Objekt, das eine Gruppe von Schriftarten kapselt, z. B. den Satz von Schriftarten, die auf dem System installiert sind, oder den Satz von Schriftarten in einem bestimmten Verzeichnis. Die Api für die Schriftartsammlung kann verwendet werden, um zu entdecken, welche Schriftfamilien und Schriftarten verfügbar sind, und um einige Metadaten zu den Schriftarten zu erhalten. |
| [**IDWriteFontCollection2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection2) | Diese Schnittstelle kapselt eine Reihe von Schriftarten, z. B. den Satz von Schriftarten, die auf dem System installiert sind, oder den Satz von Schriftarten in einem bestimmten Verzeichnis. |
| [**IDWriteFontCollection3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontcollection3) | Diese Schnittstelle kapselt eine Reihe von Schriftarten, z. B. den Satz von Schriftarten, die auf dem System installiert sind, oder den Satz von Schriftarten in einem bestimmten Verzeichnis. |
| [**IDWriteFontCollectionLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontcollectionloader) | Wird verwendet, um eine Auflistung von Schriftarten mit einem bestimmten Schlüsseltyp zu erstellen.  |
| [**IDWriteFontDownloadListener**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadlistener) | Anwendungsdefinierte Rückrufschnittstelle, die Benachrichtigungen von der Downloadwarteschlange für Schriftarten empfängt [**(IDWriteFontDownloadQueue-Schnittstelle).**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) Rückrufe werden für den herunterladenden Thread ausgeführt, und -Objekte müssen jederzeit für die Behandlung von Aufrufen ihrer Methoden aus anderen Threads vorbereitet werden. |
| [**IDWriteFontDownloadQueue**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontdownloadqueue) | Schnittstelle, die Downloadanforderungen für Remoteschriftarten, Zeichen, Glyphen und Schriftartfragmente in die Queue einträgt.  |
| [**IDWriteFontFace**](/windows/win32/api/dwrite/nn-dwrite-idwritefontface) | Diese Schnittstelle macht verschiedene Schriftartdaten verfügbar, z. B. Metriken, Namen und Glyphengliederungen. Sie enthält Schriftarttyp, entsprechende Dateiverweise und Gesichtsidentifikationsdaten. |
| [**IDWriteFontFace1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritefontface1) | Enthält Schriftarttyp, entsprechende Dateiverweise und Gesichtsidentifikationsdaten.  |
| [**IDWriteFontFace2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontface2) | Diese Schnittstelle enthält schriftartengesichtige Typen, entsprechende Dateiverweise und Gesichtsidentifikationsdaten. Sie bietet die Möglichkeit, zu überprüfen, ob ein Farbrenderingpfad potenziell erforderlich ist.  |
| [**IDWriteFontFace3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface3) | Enthält Schriftarttyp, entsprechende Dateiverweise und Gesichtsidentifikationsdaten. |
| [**IDWriteFontFace4**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface4) | Enthält Schriftarttyp, entsprechende Dateiverweise und Gesichtsidentifikationsdaten. |
| [**IDWriteFontFace5**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontface5) | Diese Schnittstelle enthält schriftartengesichtige Typen, entsprechende Dateiverweise und Gesichtsidentifikationsdaten. Es werden neue Funktionen wie das Vergleichen von zwei Schriftartgesichtern, das Abrufen von Schriftartachsenwerten und das Abrufen der zugrunde liegenden Schriftartressource hinzufügt. |
| [**IDWriteFontFaceReference**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference) | Stellt einen Verweis auf ein Schriftartgesicht dar. Ein eindeutig identifizierenden Verweis auf eine Schriftart, aus der Sie ein Schriftartgesicht erstellen können, um Schriftartmetriken und für das Rendering zu abfragen. Ein Schriftartverweis besteht aus einer Schriftartdatei, einem Schriftartenindex und einer Schriftarten-Gesichtssimulation. Die Dateidaten sind möglicherweise noch physisch auf dem lokalen Computer vorhanden.  |
| [**IDWriteFontFaceReference1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfacereference1) | Stellt einen Verweis auf ein Schriftartgesicht dar. Ein eindeutig identifizierenden Verweis auf eine Schriftart, aus der Sie ein Schriftartgesicht erstellen können, um Schriftartmetriken und für das Rendering zu abfragen. |
| [**IDWriteFontFallback**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritefontfallback) | Ermöglicht den Zugriff auf Fallbackschriftarten aus der Schriftartliste. |
| [**IDWriteFontFallbackBuilder**](idwritefontfallbackbuilder.md) | Ermöglicht ihnen das Erstellen von Unicode-Schriftartfallbackzuordnungen und das Erstellen eines Schriftartfallbackobjekts aus diesen Zuordnungen. |
| [**IDWriteFontFamily**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfamily) | Stellt eine Familie verwandter Schriftarten dar. |
| [**IDWriteFontFamily1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily1) | Stellt eine Familie verwandter Schriftarten dar. |
| [**IDWriteFontFamily2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontfamily2) | Stellt eine Familie verwandter Schriftarten dar. **IDWriteFontFamily2 fügt** neue Funktionen hinzu, einschließlich des Abrufens von Schriftarten nach Schriftartachsenwerten. |
| [**IDWriteFontFile**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfile) | Stellt eine Schriftartdatei dar. Anwendungen wie Schriftart-Manager oder Schriftart-Viewer können [**IDWriteFontFile::Analyze**](/windows/win32/api/dwrite/nf-dwrite-idwritefontfile-analyze) aufrufen, um herauszufinden, ob eine bestimmte Datei eine Schriftartdatei ist und ob es sich um einen Schriftarttyp handelt, der vom Schriftartsystem unterstützt wird. |
| [**IDWriteFontFileEnumerator**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileenumerator) | Kapselt eine Auflistung von Schriftartdateien. Das Schriftartsystem verwendet diese Schnittstelle, um Schriftartdateien aufzuzählen, wenn eine Schriftartauflistung erstellen wird. |
| [**IDWriteFontFileLoader**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) | Behandelt das Laden von Schriftartdateiressourcen eines bestimmten Typs aus einem Schriftartdatei-Verweisschlüssel in ein Schriftartdateistreamobjekt.  |
| [**IDWriteFontFileStream**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfilestream) | Lädt Schriftartdateidaten aus einem benutzerdefinierten Schriftartdateiladeprogramm.  |
| [**IDWriteFontList**](/windows/win32/api/dwrite/nn-dwrite-idwritefontlist) | Stellt eine Liste von Schriftarten dar. |
| [**IDWriteFontList1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist1) | Stellt eine Liste von Schriftarten dar. |
| [**IDWriteFontList2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontlist2) | Stellt eine Liste von Schriftarten dar. **IDWriteFontList2** fügt neue Funktionen hinzu, einschließlich des Abrufens des zugrunde liegenden Schriftartsatzes, der von der Liste verwendet wird. |
| [**IDWriteFontResource**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontresource) | nn-dwrite_3-idwritefontresource |
| [**IDWriteFontSet**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset) | Stellt einen Schriftartsatz dar. |
| [**IDWriteFontSet1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset1) | Stellt einen Schriftartsatz dar. |
| [**IDWriteFontSet2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset2) | Stellt einen Schriftartsatz dar. |
| [**IDWriteFontSet3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontset3) | Stellt einen Schriftartsatz dar. |
| [**IDWriteFontSetBuilder**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder) | Enthält Methoden zum Erstellen eines Schriftartsatzes. |
| [**IDWriteFontSetBuilder1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder1) | Enthält Methoden zum Erstellen eines Schriftartsatzes. |
| [**IDWriteFontSetBuilder2**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritefontsetbuilder2) | Enthält Methoden zum Erstellen eines Schriftartsatzes. |
| [**IDWriteGdiInterop**](/windows/win32/api/dwrite/nn-dwrite-idwritegdiinterop) | Stellt Interoperabilität mit GDI bereit, z. B. Methoden zum Konvertieren einer Schriftart in eine LOGFONT-Struktur oder zum Konvertieren einer GDI-Schriftartbeschreibung in ein Schriftartenbild. Es wird auch verwendet, um Bitmap-Renderzielobjekte zu erstellen. |
| [**IDWriteGdiInterop1**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritegdiinterop1) | Stellt Interoperabilität mit GDI bereit, z. B. Methoden zum Konvertieren einer Schriftart in eine LOGFONT-Struktur oder zum Konvertieren einer GDI-Schriftartbeschreibung in ein Schriftartenbild. Es wird auch verwendet, um Bitmap-Renderzielobjekte zu erstellen. |
| [**IDWriteGeometrySink**](idwritegeometrysink.md) | [**IDWriteGeometrySink**](idwritegeometrysink.md) ist eine **Typedef** der [**ID2D1SimplifiedGeometrySink-Schnittstelle.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) Weitere Informationen finden Sie auf der Referenzseite [**id2D1SimplifiedGeometrySink.**](/windows/win32/api/d2d1/nn-d2d1-id2d1simplifiedgeometrysink) |
| [**IDWriteGlyphRunAnalysis**](/windows/win32/api/dwrite/nn-dwrite-idwriteglyphrunanalysis) | Enthält Informationen auf niedriger Ebene, die zum Rendern einer Glyphen-Ausführung verwendet werden. |
| [**IDWriteInlineObject**](/windows/win32/api/dwrite/nn-dwrite-idwriteinlineobject) | Umschließt eine anwendungsdefinierte Inlinegrafik, sodass DWrite Metriken abfragen kann, als wäre die Grafik ein Glyphen inline mit dem Text. |
| [**IDWriteInMemoryFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteinmemoryfontfileloader) | Stellt ein Schriftartdateiladeprogramm dar, das auf In-Memory-Schriftarten zugreifen kann. |
| [**IDWriteLocalFontFileLoader**](idwritelocalfontfileloader.md) | Eine integrierte Implementierung der [**IDWriteFontFileLoader-Schnittstelle,**](/windows/win32/api/dwrite/nn-dwrite-idwritefontfileloader) die lokale Schriftartdateien verwendet und lokale Schriftartdateiinformationen aus dem Referenzschlüssel der Schriftartdatei verfügbar macht. Schriftartdateiverweise, die mit [**CreateFontFileReference**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createfontfilereference) erstellt wurden, verwenden dieses Schriftartdateiladeprogramm. |
| [**IDWriteLocalizedStrings**](/windows/win32/api/dwrite/nn-dwrite-idwritelocalizedstrings) | Stellt eine Auflistung von Zeichenfolgen dar, die anhand des Gebietsschemanamens indiziert sind. |
| [**IDWriteNumberSubsierung**](./idwritenumbersubstitution.md) | Enthält die entsprechenden Ziffern und numerische Interpunktion für ein angegebenes Gebietsschema. |
| [**IDWritePixelSnapping**](/windows/win32/api/dwrite/nn-dwrite-idwritepixelsnapping) | Definiert die Pixel-Ausrichtungseigenschaften wie Pixel pro DIP (geräteunabhängiges Pixel) und die aktuelle Transformationsmatrix eines Textrenderers. |
| [**IDWriteRemoteFontFileLoader**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfileloader) | Stellt ein Schriftartdateiladeprogramm dar, das auf Remoteschriftarten (d. h. herunterladbare Schriftarten) zugreifen kann.  |
| [**IDWriteRemoteFontFileStream**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriteremotefontfilestream) | Stellt einen Schriftartdateistream dar, dessen Teile möglicherweise nicht lokal sind.  |
| [**IDWriteRenderingParams**](/windows/win32/api/dwrite/nn-dwrite-idwriterenderingparams) | Stellt Textrenderingeinstellungen wie ClearType-Ebene, verbesserten Kontrast und Gammakorrektur für die Rasterung und Filterung von Glyphen dar. Eine Anwendung ruft in der Regel ein Renderingparameterobjekt ab, indem sie die [**IDWriteFactory::CreateMonitorRenderingParams-Methode**](/windows/win32/api/dwrite/nf-dwrite-idwritefactory-createmonitorrenderingparams) aufruft. |
| [**IDWriteRenderingParams1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwriterenderingparams1) | Stellt Textrenderingeinstellungen für die Rasterung und Filterung von Glyphen dar. |
| [**IDWriteRenderingParams2**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwriterenderingparams2) | Stellt Textrenderingeinstellungen für die Rasterung und Filterung von Glyphen dar. |
| [**IDWriteRenderingParams3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwriterenderingparams3) | Stellt Textrenderingeinstellungen für die Rasterung und Filterung von Glyphen dar. |
| [**IDWriteStringList**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritestringlist) | Stellt eine Auflistung von Zeichenfolgen dar, die nach Zahl indiziert sind. |
| [**IDWriteTextAnalysisSink**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissink) | Diese Schnittstelle wird vom Client des Textanalysetools implementiert, um die Ausgabe einer bestimmten Textanalyse zu empfangen.  |
| [**IDWriteTextAnalysisSink1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissink1) | Die Schnittstelle, die Sie implementieren, um die Ausgabe der Textanalysetools zu empfangen. |
| [**IDWriteTextAnalysisSource**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalysissource) | Wird vom Client der Textanalyse implementiert, um Text für das Analyseprogramm bereitzustellen. Sie ermöglicht die Trennung zwischen der logischen Textansicht als fortlaufendem Zeichenstrom, der durch eindeutige Textpositionen identifiziert wird, und dem tatsächlichen Speicherlayout potenziell diskreter Textblöcke im Sicherungsspeicher des Clients.  |
| [**IDWriteTextAnalysisSource1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalysissource1) | Die Schnittstelle, die Sie implementieren, um dem Textanalyseprogramm die erforderlichen Informationen bereitzustellen, z. B. den Text und die zugehörigen Texteigenschaften. |
| [**IDWriteTextAnalyzer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextanalyzer) | Analysiert verschiedene Texteigenschaften für die komplexe Skriptverarbeitung, z. B. bidirektionale Unterstützung (bidi) für Sprachen wie Arabisch, Bestimmung von Zeilenumbruchmöglichkeiten, Glyphenplatzierung und Zahlenersetzung. |
| [**IDWriteTextAnalyzer1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextanalyzer1) | Analysiert verschiedene Texteigenschaften für die komplexe Skriptverarbeitung. |
| [**IDWriteTextAnalyzer2**](idwritetextanalyzer2.md) | Analysiert verschiedene Texteigenschaften für die komplexe Skriptverarbeitung. |
| [**Idwritetextformat**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) | Die [**IDWriteTextFormat-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextformat) beschreibt die Schriftart- und Absatzeigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebietsschemainformationen.  |
| [**IDWriteTextFormat1**](idwritetextformat1.md) | Beschreibt die Schriftart- und Absatzeigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebietsschemainformationen.  |
| [**IDWriteTextFormat2**](idwritetextformat2.md) | Beschreibt die Schriftart- und Absatzeigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebietsschemainformationen.  |
| [**IDWriteTextFormat3**](/windows/win32/api/dwrite_3/nn-dwrite_3-idwritetextformat3) | Beschreibt die Schriftart- und Absatzeigenschaften, die zum Formatieren von Text verwendet werden, und beschreibt Gebietsschemainformationen. |
| [**Idwritetextlayout**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) | Die [**IDWriteTextLayout-Schnittstelle**](/windows/win32/api/dwrite/nn-dwrite-idwritetextlayout) stellt einen Textblock dar, nachdem er vollständig analysiert und formatiert wurde. |
| [**IDWriteTextLayout1**](/windows/win32/api/dwrite_1/nn-dwrite_1-idwritetextlayout1) | Stellt einen Textblock dar, nachdem er vollständig analysiert und formatiert wurde. |
| [**IDWriteTextLayout2**](idwritetextlayout2.md) | Stellt einen Textblock dar, nachdem er vollständig analysiert und formatiert wurde. |
| [**IDWriteTextLayout3**](idwritetextlayout3.md) | Stellt einen Textblock dar, nachdem er vollständig analysiert und formatiert wurde.  |
| [**IDWriteTextRenderer**](/windows/win32/api/dwrite/nn-dwrite-idwritetextrenderer) | Stellt eine Reihe von anwendungsdefinierte Rückrufen dar, die das Rendern von Text, Inlineobjekten und Verzierungen wie Unterstreichungen ausführen. |
| [**IDWriteTextRenderer1**](/windows/win32/api/dwrite_2/nn-dwrite_2-idwritetextrenderer1) | Stellt eine Reihe von anwendungsdefinierte Rückrufen dar, die das Rendern von Text, Inlineobjekten und Verzierungen wie Unterstreichungen ausführen.  |
| [**IDWriteTypography**](/windows/win32/api/dwrite/nn-dwrite-idwritetypography) | Stellt eine Schriftarttypografieeinstellung dar. |