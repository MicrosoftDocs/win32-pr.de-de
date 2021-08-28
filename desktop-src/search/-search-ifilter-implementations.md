---
description: Microsoft stellt mehrere Standardfilter mit Windows Search zur Verfügung. Clients rufen diese Filterhandler auf (bei denen es sich um Implementierungen der IFilter-Schnittstelle handelt), um Text und Eigenschaften aus einem Dokument zu extrahieren.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Filterhandler, die mit Windows
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e1a245978482e0334d91e35031aa80186fd2cb32
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122624366"
---
# <a name="filter-handlers-that-ship-with-windows"></a>Filterhandler, die mit Windows

Microsoft stellt mehrere Standardfilter mit Windows Search zur Verfügung. Clients rufen diese Filterhandler auf (bei denen es sich um Implementierungen der [**IFilter-Schnittstelle**](/windows/win32/api/filter/nn-filter-ifilter) handelt), um Text und Eigenschaften aus einem Dokument zu extrahieren.

Dieses Thema ist wie folgt organisiert:

- [Windows Hinweise zur Implementierung der Suche](#windows-search-implementation-notes)
  - [Windows 7- und 10-Implementierung](#windows-7-and-10-implementation)
  - [Windows Vista-Implementierung](#windows-vista-implementation)
  - [Legacyimplementierungen](#legacy-implementation)
- [Windows Suchfilter](#filter-handlers-that-ship-with-windows)
  - [MIME-Filterhandler](#mime-filter-handler)
  - [HTML-Filterhandler](#html-filter-handler)
  - [Dokumentfilterhandler](#document-filter-handler)
  - [Nur-Text-Filterhandler](#plain-text-filter-handler)
  - [Binärer oder NULL-Filterhandler](#binary-or-null-filter-handler)
- [Weitere Ressourcen](#additional-resources)
- [Zugehörige Themen](#related-topics)

## <a name="windows-search-implementation-notes"></a>Windows Hinweise zur Implementierung der Suche

In Windows 7 und höher werden in verwaltetem Code geschriebene Filter explizit blockiert. Filter MÜSSEN aufgrund potenzieller CLR-Versionsprobleme mit dem Prozess, in dem mehrere Add-Ins ausgeführt werden, in nativem Code geschrieben werden.

### <a name="windows-7-and-10-implementation"></a>Windows 7- und 10-Implementierung

In Windows 7 und höher tritt beim Registrieren eines Filterhandlers, Eigenschaftenhandlers oder einer neuen Erweiterung ein neues Verhalten auf. Wenn ein neuer Eigenschaftenhandler und/oder Filterhandler installiert ist, werden Dateien mit den entsprechenden Erweiterungen automatisch neu indiziert.

In Windows 7 und höher wird empfohlen, einen Filterhandler in Verbindung mit den entsprechenden Eigenschaftenhandlern zu installieren und den Filterhandler vor dem Eigenschaftenhandler zu registrieren. Die Registrierung des Eigenschaftenhandlers initiiert die sofortige erneute Indizierung zuvor indizierter Dateien, ohne dass zuerst ein Neustart erforderlich ist, und nutzt alle zuvor registrierten Filterhandler für die Inhaltsindizierung.

Wenn nur ein Filterhandler ohne einen entsprechenden Eigenschaftenhandler installiert wird, erfolgt die automatische erneute Indizierung entweder nach einem Neustart des Indizierungsdiensts oder einem Neustart des Systems.

Spezifische Eigenschaftenbeschreibungsflags für Windows 7 finden Sie in den folgenden Referenzthemen: [GETPROPERTYSTOREFLAGS,](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags) [PROPDESC \_ COLUMNINDEX \_ TYPE](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) und [PROPDESC \_ SEARCHINFO \_ FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).

### <a name="windows-vista-implementation"></a>Windows Vista-Implementierung

In Windows Vista und früheren Versionen initiiert die Installation eines [**IFilter-**](/windows/win32/api/filter/nn-filter-ifilter) oder Eigenschaftenhandlers keine erneute Indizierung vorhandener Elemente, es sei denn, ein unabhängiger Softwarehersteller (Independent Software Vendor, ISV) ruft explizit eine Neuerstellung oder Neuindizierung übereinstimmender URLs auf.

Es gibt zwei wesentliche Unterschiede zwischen Legacyanwendungen wie indexing Service und neueren Anwendungen wie Windows Search, die Sie beim Implementieren von Filtern beachten sollten:

- Verwendung der [IPersistStream-Schnittstelle.](/windows/win32/api/objidl/nn-objidl-ipersiststream)
- Verwendung von Eigenschaftenhandlern.

Zunächst müssen Sie Windows Vista und Windows Search 3.0 und höher [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) aus den folgenden Gründen verwenden:

- Um die Leistung und zukünftige Kompatibilität sicherzustellen.
- Um die Sicherheit zu erhöhen. Filter, die mit [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) implementiert werden, sind sicherer, da der Kontext, in dem der Filter ausgeführt wird, nicht die Rechte zum Öffnen von Dateien auf dem Datenträger oder über das Netzwerk benötigt.

Während Windows Search nur [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)verwendet, können Sie aus Gründen der Abwärtskompatibilität auch implementierungen der [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile) und/oder [der IPersistStorage-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersiststorage) in Ihre Filter einschließen.

Der zweite hauptunterschied besteht darin, dass Windows Vista und Windows Search 3.0 und höher über ein neues [Eigenschaftensystem](../properties/building-property-handlers.md) verfügen, das Eigenschaftenhandler verwendet, um Eigenschaften von Elementen aufzuzählen.

Es gibt jedoch Zeiten, in denen Sie einen Filter implementieren müssen, der sowohl Inhalt als auch Eigenschaften behandelt, um:

- Unterstützung von älteren MSSearch-Implementierungen.
- Durchlaufen Sie Links.
- Beibehalten von Sprachinformationen.
- Filtern Sie eingebettete Elemente rekursiv.

In diesen Situationen benötigen Sie eine vollständige Filterimplementierungen, einschließlich der [**IFilter::GetValue-Methode,**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) um auf Eigenschaftswerte zuzugreifen.

### <a name="legacy-implementation"></a>Legacyimplementierungen

Wie bereits erwähnt, enthalten Windows Vista und Windows Search ein neues Eigenschaftensystem, das die Eigenschaften eines Elements kapselt, die vom Inhalt eines Elements getrennt sind. Dieses Eigenschaftensystem ist in früheren Versionen von Microsoft Windows DesktopSuche (WDS) 2.x nicht vorhanden. Wenn Ihr Filter wie oben beschrieben andere Anwendungen unterstützen muss, muss er möglicherweise sowohl Inhalt als auch Eigenschaften behandeln.

Weitere Informationen zum Entwickeln eines kompatiblen Filters finden Sie in den folgenden Themen: [IFilter (für Legacyanwendungen)](/windows/win32/api/filter/nn-filter-ifilter)und [Entwickeln von Filter-Add-Ins (für Legacyanwendungen).](../lwef/-search-2x-wds-ifilteraddins.md)

## <a name="windows-search-filters"></a>Windows Suchfilter

Microsoft stellt mehrere Standardfilter mit Windows Search zur Verfügung. Die Inhalte der [**IFilter-DLL**](/windows/win32/api/filter/nn-filter-ifilter)  sind in der folgenden Tabelle zusammengefasst. Wenn Sie auf den Namen eines Filterhandlers klicken, gelangen Sie zur Beschreibung für diese **IFilter-Implementierung.**

| Filterhandler                                                  | Gefilterte Dateien                              | IFilter-DLL  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [MIME-Filterhandler](#mime-filter-handler)                     | Multipurpose Internet Mail Extension (MIME) | mimefilt.dll |
| [HTML-Filterhandler](#html-filter-handler)                     | HTML 3.0 oder früher                         | nlhtml.dll   |
| [Dokumentfilterhandler](#document-filter-handler)             | Microsoft Word, Excel, PowerPoint           | offfilt.dll  |
| [Nur-Text-Filterhandler](#plain-text-filter-handler)         | Nur-Text-Dateien – Standard-IFilter          | query.dll    |
| [Binärer oder NULL-Filterhandler](#binary-or-null-filter-handler) | Binärdateien – NULL-IFilter                 | query.dll    |

### <a name="mime-filter-handler"></a>MIME-Filterhandler

Der MIME-Filterhandler (in mimefilt.dll) extrahiert Text- und Eigenschaftsinformationen aus Dateien mit den Erweiterungen EML, MHT und MHTML.

### <a name="html-filter-handler"></a>HTML-Filterhandler

Der HTML-Filterhandler (in nlhtml.dll) extrahiert Text- und Eigenschaftsinformationen aus der Klasse "htmlfiles", sodass sie durch Windows Search indiziert werden können. Eine Beschreibung der Zuordnung zwischen [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) und dem Dateityp finden Sie unter "Suchen der IFilter-DLL für eine Datei" unter [Registrieren von Filterhandlern.](-search-ifilter-registering-filters.md)

Sie können das `META` Tagfeature von HTML-Dokumenten verwenden, um spezielle Verarbeitungsanforderungen an den HTML-IFilter zu übermitteln. [](/windows/win32/api/filter/nn-filter-ifilter) `META` -Tags treten am Anfang einer HTML-Datei innerhalb der `HEAD ... /HEAD` Tags auf, wie im folgenden Beispiel veranschaulicht.

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

Einige `META` HTML-Tags werden automatisch bekannten Eigenschaftssatz- und Eigenschafts-ID-Werten (Property Identifier, PID) zugeordnet, sodass Abfragen dieser Eigenschaften den zugeordneten Inhalt durchsuchen. Einige Beispiele sind in der folgenden Tabelle aufgeführt. Eine Liste der Systemeigenschaften, die Sie für Ihre Dateiformate verwenden können, finden Sie unter [Systemdefinierte Eigenschaften für benutzerdefinierte Dateiformate.](-shell-systemdefinedpropertiesforfileformats.md)

| Eigenschaftsbeispiel                              | Zugeordnet zu                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| meta name="author" content="soll"             | Die author-Eigenschaft im Eigenschaftensatz Zusammenfassungsinformationen.            |
| meta name="subject" content="word processing" | Die subject-Eigenschaft im Eigenschaftensatz Zusammenfassungsinformationen.           |
| meta name="keywords" content="fonts, serif"   | Die Schlüsselworteigenschaft im Eigenschaftensatz Zusammenfassungsinformationen.           |
| meta name="ms.category" content="fiction"     | Die Kategorieeigenschaft im Eigenschaftensatz zusammenfassungsinformationen. |

Einige Features des [**HTML-IFilters**](/windows/win32/api/filter/nn-filter-ifilter) sind in der folgenden Tabelle aufgeführt.

[comment]: # (Diese Tabelle muss HTML sein, damit die Beispiele richtig formatiert sind.)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col  />
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Aufgabe</th>
<th>Aktion</th>
<th>Beispiel</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Erstellen spezieller Abstracts aus Dateien</td>
<td>Verwenden Sie das <code>META NAME=&quot;DESCRIPTION&quot;...</code> -Tag, um den <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> anzuweisen, die Zeichenfolge nach dem <code>CONTENT</code> Schlüsselwort als Dokumentstrah zu verwenden.
<blockquote>
[!Note]<br />
Der Filterprozess kann Abstracts für jede gefilterte Datei generieren, die standardmäßig ein Zeichensatz am Anfang der Datei ist.
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;head&gt;
  &lt;META NAME=&quot;DESCRIPTION&quot; CONTENT=&quot;This text will appear on the results page as the document&#39;s summary.&quot;&gt;
&lt;/head&gt;
 </pre></td>
</tr>
</tbody>
</table>
</td>
</tr>
<tr class="even">
<td>Verhindern der Filterung einzelner Dateien</td>
<td>Fügen Sie der Datei ein <code>meta name</code> Tag hinzu.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
  &lt;meta name=&quot;robots&quot; content=&quot;noindex&quot;&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="odd">
<td>Festlegen des Sprachcodes für eine Datei (um sicherzustellen, dass das System die richtigen Sprachbegriffs-Breaker und Füllwortdateien aus wählt)</td>
<td>Fügen Sie der Datei das folgende <code>meta name</code> Tag hinzu, wobei das Inhaltsfeld den entsprechenden Sprachcode angibt (entweder in Zeichen oder mithilfe des Gebietsschemawerts).</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col  />
</colgroup>
<tbody>
<tr class="odd">
<td><pre>
&lt;meta name=&quot;ms.locale&quot; content=&quot;EN&quot;&gt;
&lt;meta name=&quot;ms.locale&quot; content=1033&gt;
</pre></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
</tbody>
</table>
<!-- markdownlint-enable MD033 -->

### <a name="document-filter-handler"></a>Dokumentfilterhandler

Der Dokumentfilterhandler (in offilt.dll) filtert Dateien nach einigen Erweiterungen von Dokumenten in Microsoft Office. Dazu gehören beispielsweise Dateien mit den Erweiterungen .doc, MDB, .ppt und XLT.

### <a name="plain-text-filter-handler"></a>Nur-Text-Filterhandler

Bei Nur-Text-Dateien verwendet Windows Search den Textfilterhandler, der sowohl die Systemeigenschaften (z. B. Dateinamen) als auch den Inhalt einer Datei filtert. Wenn ein Dateityp keine [**IFilter-Zuordnung**](/windows/win32/api/filter/nn-filter-ifilter) in der Registrierung aufweist, Windows Search-Indizes nur die Shell-Eigenschaften für die Datei. Der Benutzer kann jedoch die **erweiterten Optionen** in der Systemsteuerung **Indizierungsoptionen** verwenden, um Eigenschaften oder **Indexeigenschaften und Dateiinhalte** zu **indizieren.**

![Screenshot des Dialogfelds "Erweiterte Optionen"](images/ifilteradvancedoptions.png)

Wenn der Benutzer diese Option für einen Dateityp ohne zugeordneten [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)ausgibt, wird der Textfilterhandler verwendet, um den Inhalt der Datei zu extrahieren. Der Textfilterhandler "versteht" kein Dokumentformat. Beim Filtern des Inhalts einer Datei wird die Datei als Zeichensequenz behandelt. Es sucht am Anfang der Datei nach der Unicode-Bytereihenfolgemarkierung.

### <a name="binary-or-null-filter-handler"></a>Binärer oder NULL-Filterhandler

Wenn eine registrierte Binärdatei gefunden wird, wird der NULL-Filterhandler verwendet. Der NULL-Filterhandler ruft nur die Systemeigenschaften ab. Der Inhalt einer Binärdatei wird nicht gefiltert. Beispiele für Systemeigenschaften sind **FileName,** **LastWriteTime,** **FileSize** und **Attributes**.

## <a name="additional-resources"></a>Weitere Ressourcen

- Das [IFilterSample-Codebeispiel,](-search-sample-ifiltersample.md) das auf [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbar ist, veranschaulicht das Erstellen einer IFilter-Basisklasse zum Implementieren der [**IFilter-Schnittstelle.**](/windows/win32/api/filter/nn-filter-ifilter)
- Eine Übersicht über den Indizierungsprozess finden Sie unter [Der Indizierungsprozess.](-search-indexing-process-overview.md)
- Eine Übersicht über Dateitypen finden Sie unter [Dateitypen.](../shell/fa-file-types.md)
- Informationen zum Abfragen von Dateizuordnungsattributen für einen Dateityp finden Sie unter [PerceivedTypes, SystemFileAssociations und Application Registration](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85)).

## <a name="related-topics"></a>Zugehörige Themen

[Entwickeln von Filterhandlern](-search-ifilter-conceptual.md)

[Informationen zu Filterhandlern in Windows Search](-search-ifilter-about.md)

[Bewährte Methoden zum Erstellen von Filterhandlern in Windows Suche](-search-3x-wds-extidx-filters.md)

[Zurückgeben von Eigenschaften von einem Filterhandler](-search-ifilter-property-filtering.md)

[Implementieren von Filterhandlern in Windows Search](-search-ifilter-constructing-filters.md)

[Registrieren von Filterhandlern](-search-ifilter-registering-filters.md)

[Testen von Filterhandlern](-search-ifilter-testing-filters.md)
