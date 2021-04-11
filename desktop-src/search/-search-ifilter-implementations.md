---
description: Microsoft stellt mehrere Standardfilter mit Windows Search bereit. Clients bezeichnen diese Filter Handler (die Implementierungen der IFilter-Schnittstelle sind), um Text und Eigenschaften aus einem Dokument zu extrahieren.
ms.assetid: e19ae220-5c59-482e-8b02-00889600c4d6
title: Filtern von Handlern, die mit Windows ausgeliefert werden
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5dd5603ab913117e2c968a7508b2fa061dfb4034
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128568"
---
# <a name="filter-handlers-that-ship-with-windows"></a>Filtern von Handlern, die mit Windows ausgeliefert werden

Microsoft stellt mehrere Standardfilter mit Windows Search bereit. Clients bezeichnen diese Filter Handler (die Implementierungen der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle sind), um Text und Eigenschaften aus einem Dokument zu extrahieren.

Dieses Thema ist wie folgt organisiert:

- [Implementierungs Hinweise zur Windows-Suche](#windows-search-implementation-notes)
  - [Windows 7-und 10-Implementierung](#windows-7-and-10-implementation)
  - [Windows Vista-Implementierung](#windows-vista-implementation)
  - [Legacy Implementierung](#legacy-implementation)
- [Windows-Suchfilter](#filter-handlers-that-ship-with-windows)
  - [MIME-Filter Handler](#mime-filter-handler)
  - [HTML-Filter Handler](#html-filter-handler)
  - [Dokument Filter Handler](#document-filter-handler)
  - [Nur-Text-Filter Handler](#plain-text-filter-handler)
  - [Binärer oder NULL-Filter Handler](#binary-or-null-filter-handler)
- [Weitere Ressourcen](#additional-resources)
- [Zugehörige Themen](#related-topics)

## <a name="windows-search-implementation-notes"></a>Implementierungs Hinweise zur Windows-Suche

In Windows 7 und höher werden in verwaltetem Code geschriebene Filter explizit blockiert. Filter müssen in nativem Code geschrieben werden, da mögliche Probleme bei der CLR-Versionsverwaltung mit dem Prozess auftreten, in dem mehrere Add-Ins ausgeführt werden.

### <a name="windows-7-and-10-implementation"></a>Windows 7-und 10-Implementierung

In Windows 7 und höher gibt es ein neues Verhalten, das beim Registrieren eines Filter Handlers, eines Eigenschaften Handlers oder einer neuen Erweiterung auftritt. Wenn ein neuer Eigenschaften Handler und/oder Filter Handler installiert wird, werden Dateien mit den entsprechenden Erweiterungen automatisch neu indiziert.

In Windows 7 und höher wird empfohlen, dass Sie einen Filter Handler in Verbindung mit den entsprechenden Eigenschaften Handlern installieren und den Filter Handler vor dem Eigenschaften Handler registrieren. Die Registrierung des Eigenschaften Handler initiiert die sofortige Neuindizierung von zuvor indizierten Dateien, ohne dass zuerst ein Neustart erforderlich ist, und nutzt alle zuvor registrierten Filter Handler für die Inhalts Indizierung.

Wenn nur ein Filter Handler ohne einen entsprechenden Eigenschaften Handler installiert wird, erfolgt die automatische Neuindizierung entweder nach einem Neustart des Indizierungs dienstanzdienstanbieter oder einem Neustart des Systems.

Informationen zu eigenschaftenbeschreibungsflags, die speziell für Windows 7 gelten, finden Sie in den folgenden Referenz Themen: [getpropertystoreflags](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags), [PropDesc \_ ColumnIndex \_ Type](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type) und [PropDesc \_ SearchInfo \_ Flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags).

### <a name="windows-vista-implementation"></a>Windows Vista-Implementierung

In Windows Vista und früheren Versionen initiiert die Installation eines [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -oder Eigenschaften Handlers keine Neuindizierung vorhandener Elemente, es sei denn, ein unabhängiger Softwarehersteller (ISV) ruft explizit eine Neuerstellung oder Neuindizierung der übereinstimmenden URLs auf.

Es gibt zwei wesentliche Unterschiede zwischen Legacy Anwendungen, wie z. b. dem Indizierungs Dienst und neueren Anwendungen wie Windows Search, die Sie beim Implementieren von Filtern beachten sollten:

- Verwendung der [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) -Schnittstelle.
- Verwendung von Eigenschaften Handlern.

Zuerst erfordern Windows Vista und Windows Search 3,0 und höher die Verwendung von [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) aus den folgenden Gründen:

- Um Leistung und zukünftige Kompatibilität zu gewährleisten.
- , Um die Sicherheit zu erhöhen. Mit [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream) implementierte Filter sind sicherer, da der Kontext, in dem der Filter ausgeführt wird, nicht die Berechtigung zum Öffnen von Dateien auf dem Datenträger oder über das Netzwerk benötigt.

Obwohl bei Windows Search nur [IPersistStream](/windows/win32/api/objidl/nn-objidl-ipersiststream)verwendet wird, können Sie die [IPersistFile-Schnittstelle](/windows/win32/api/objidl/nn-objidl-ipersistfile) und/oder [IPersistStorage-Schnittstellen](/windows/win32/api/objidl/nn-objidl-ipersiststorage) Implementierungen in Ihren Filtern für die Abwärtskompatibilität einschließen.

Der zweite Hauptunterschied besteht darin, dass Windows Vista und Windows Search 3,0 und höher ein neues Eigenschaften [System](../properties/building-property-handlers.md) haben, das Eigenschafts Handler verwendet, um Eigenschaften von Elementen aufzuzählen.

Es gibt jedoch Zeiten, in denen Sie einen Filter implementieren müssen, der sowohl den Inhalt als auch die Eigenschaften behandelt, um Folgendes zu tun:

- Unterstützung von Legacy-MSSearch-Implementierungen.
- Durchsuchen von Links.
- Sprachinformationen beibehalten.
- Filtern Sie eingebettete Elemente rekursiv.

In diesen Fällen benötigen Sie eine vollständige Filter Implementierung, einschließlich der [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) -Methode, um auf Eigenschaftswerte zuzugreifen.

### <a name="legacy-implementation"></a>Legacy Implementierung

Wie bereits erwähnt, enthalten Windows Vista und Windows Search ein neues Eigenschaften System, das die Eigenschaften eines Elements kapselt, das vom Inhalt eines Elements getrennt ist. Dieses Eigenschaften System ist in früheren Versionen von Microsoft Windows Desktop Search (WDS) 2. x nicht vorhanden. Wenn der Filter andere Anwendungen unterstützen muss, wie oben beschrieben, muss er möglicherweise sowohl den Inhalt als auch die Eigenschaften verarbeiten.

Weitere Informationen zum Entwickeln eines kompatiblen Filters finden Sie in den folgenden Themen: [IFilter (für ältere Anwendungen)](/windows/win32/api/filter/nn-filter-ifilter)und [entwickeln von Filter-Add-Ins (für ältere Anwendungen)](../lwef/-search-2x-wds-ifilteraddins.md).

## <a name="windows-search-filters"></a>Windows-Suchfilter

Microsoft stellt mehrere Standardfilter mit Windows Search bereit. Der Inhalt der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)  -dll wird in der folgenden Tabelle zusammengefasst. Wenn Sie auf den Namen eines Filter Handlers klicken, gelangen Sie zur Beschreibung der **IFilter** -Implementierung.

| Filter Handler                                                  | Gefilterte Dateien                              | IFilter-DLL  |
|-----------------------------------------------------------------|---------------------------------------------|--------------|
| [MIME-Filter Handler](#mime-filter-handler)                     | Mehrzweck-Internet Mail Erweiterung (MIME) | mimefilt.dll |
| [HTML-Filter Handler](#html-filter-handler)                     | HTML 3,0 oder früher                         | nlhtml.dll   |
| [Dokument Filter Handler](#document-filter-handler)             | Microsoft Word, Excel, PowerPoint           | offfilt.dll  |
| [Nur-Text-Filter Handler](#plain-text-filter-handler)         | Nur-Text-Dateien-Standard-IFilter          | query.dll    |
| [Binärer oder NULL-Filter Handler](#binary-or-null-filter-handler) | Binäre Dateien-NULL-IFilter                 | query.dll    |

### <a name="mime-filter-handler"></a>MIME-Filter Handler

Der MIME-Filter Handler (in mimefilt.dll) extrahiert Text-und Eigenschafts Informationen aus Dateien mit den Erweiterungen ". eml", ". MHT" und ". MHTML".

### <a name="html-filter-handler"></a>HTML-Filter Handler

Der HTML-Filter Handler (in nlhtml.dll) extrahiert Text-und Eigenschafts Informationen aus der Klasse "HtmlFiles", sodass er von Windows Search indiziert werden kann. Eine Beschreibung der Zuordnung zwischen [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) und Dateityp finden Sie unter "Suchen der IFilter-DLL für eine Datei" in [Registrieren von Filter Handlern](-search-ifilter-registering-filters.md).

Sie können das `META` tagfeature von HTML-Dokumenten verwenden, um besondere Verarbeitungsanforderungen an den HTML- [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)zu übermitteln. `META` Tags treten am Anfang einer HTML-Datei innerhalb der `HEAD ... /HEAD` Tags auf, wie im folgenden Beispiel veranschaulicht.

```XML
   <head>
     <META NAME="DESCRIPTION"
           CONTENT="This text appears on the results page as the document's summary.">
   </head>
```

Einige HTML- `META` Tags werden automatisch bekannten Eigenschaften Satz-und Eigenschafts-ID-Werten (eigenschaftenbezeichnerwerte (PID)) zugeordnet, damit Abfragen für diese Eigenschaften den zugeordneten Inhalt durchsuchen. Einige Beispiele sind in der folgenden Tabelle aufgeführt. Eine Liste der Systemeigenschaften, die Sie für die Dateiformate verwenden können, finden Sie unter [System definierte Eigenschaften für benutzerdefinierte Dateiformate](-shell-systemdefinedpropertiesforfileformats.md).

| Eigenschafts Beispiel                              | Zugeordnet zu                                                               |
|-----------------------------------------------|-------------------------------------------------------------------------|
| Meta Name = "Author" Content = "Ruth"             | Die Eigenschaft "Author" in der Eigenschaften Gruppe für Zusammenfassungs Informationen.            |
| Meta Name = "Subject" Content = "Word Processing" | Die Eigenschaft "Subject" in der Eigenschaften Gruppe für Zusammenfassungs Informationen.           |
| Meta Name = "Keywords" Content = "Fonts, Serif"   | Die Schlüsselwort Eigenschaft im Eigenschaften Satz für Zusammenfassungs Informationen.           |
| Meta Name = "MS. Category" Content = "Fiction"     | Die Kategorieeigenschaft in der Eigenschaft für die Dokument Zusammenfassungs Informationen. |

Einige Features der HTML- [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) sind in der folgenden Tabelle aufgeführt.

[comment]: # (Diese Tabelle muss HTML sein, damit die Beispiele ordnungsgemäß formatiert werden.)

<!-- markdownlint-disable MD033 -->
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
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
<td>Verwenden Sie das- <code>META NAME=&quot;DESCRIPTION&quot;...</code> Tag, um den <a href="https://www.bing.com/search?q=<strong>IFilter</strong>"><strong>IFilter</strong></a> anzuweisen, die Zeichenfolge nach dem <code>CONTENT</code> Schlüsselwort als Dokument abstrakt zu verwenden.
<blockquote>
[!Note]<br />
Der Filterprozess kann für jede gefilterte Datei Abstraktionen generieren, bei denen es sich standardmäßig um einen Satz von Zeichen am Anfang der Datei handelt.
</blockquote>
<br/></td>
<td><span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td>Verhindern, dass einzelne Dateien gefiltert werden</td>
<td>Fügen Sie <code>meta name</code> der Datei ein-Tag hinzu.</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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
<td>Festlegen des Sprachcodes für eine Datei (um sicherzustellen, dass das System die richtigen Wörter Trennungen und Füll Wort Dateien der Sprache auswählt)</td>
<td>Fügen Sie der Datei das folgende- <code>meta name</code> Tag hinzu, wobei das Inhaltsfeld den entsprechenden Sprachcode angibt (entweder in Zeichen oder mithilfe des Gebiets Schema Werts).</td>
<td><div class="code">
<span data-codelanguage=""></span>
<table>
<colgroup>
<col style="width: 100%" />
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

### <a name="document-filter-handler"></a>Dokument Filter Handler

Der Dokument Filter Handler (in offilt.dll) filtert Dateien für einige Erweiterungen von Dokumenten in Microsoft Office. Dazu zählen beispielsweise Dateien mit den Erweiterungen ". doc", ". mdb", "ppt" und ". xlt".

### <a name="plain-text-filter-handler"></a>Nur-Text-Filter Handler

Für nur-Text-Dateien verwendet Windows Search den Textfilter Handler, der sowohl die Systemeigenschaften (z. b. Dateinamen) als auch den Inhalt einer Datei filtert. Wenn ein Dateityp nicht über eine [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Zuordnung in der Registrierung verfügt, indiziert Windows Search nur die Shelleigenschaften für die Datei. Der Benutzer kann jedoch die **erweiterten Optionen** in der Systemsteuerung der **Indizierungs Optionen** verwenden, um Eigenschaften oder **Index Eigenschaften und Dateiinhalte** zu **indizieren** .

![Screenshot mit dem Dialogfeld "Erweiterte Optionen"](images/ifilteradvancedoptions.png)

Wenn der Benutzer diese Option für einen Dateityp ohne zugeordneten [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)auswählt, wird der Inhalt der Datei mithilfe des Textfilter Handlers extrahiert. Der Textfilter Handler hat kein Verständnis für ein Dokumentformat. Wenn Sie den Inhalt einer Dateifiltern, wird die Datei als Sequenz von Zeichen behandelt. Er überprüft die Unicode-Byte Reihenfolge Markierung am Anfang der Datei.

### <a name="binary-or-null-filter-handler"></a>Binärer oder NULL-Filter Handler

Wenn eine registrierte Binärdatei gefunden wird, wird der NULL-Filter Handler verwendet. Der NULL-Filter Handler ruft nur die Systemeigenschaften ab. Der Inhalt einer Binärdatei wird nicht gefiltert. Beispiele für Systemeigenschaften sind **Dateiname**, **lastschreitezeit**, **FileSize** und **Attribute**.

## <a name="additional-resources"></a>Weitere Ressourcen

- Das in [GitHub](https://github.com/Microsoft/Windows-classic-samples/tree/master/Samples/Win7Samples/winui/WindowsSearch/IFilterSample)verfügbare [ifiltersample](-search-sample-ifiltersample.md) -Codebeispiel veranschaulicht, wie eine IFilter-Basisklasse für die Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle erstellt wird.
- Eine Übersicht über den Indizierungsprozess finden Sie [im Abschnitt zur Indizierung](-search-indexing-process-overview.md).
- Eine Übersicht über die Dateitypen finden Sie unter [Dateitypen](../shell/fa-file-types.md).
- Informationen zum Abfragen von Datei Zuordnungs Attributen für einen Dateityp finden Sie unter " [wahrtentypen", "systemfileassociation" und "Anwendungs Registrierung](/previous-versions/windows/desktop/legacy/cc144150(v=vs.85))".

## <a name="related-topics"></a>Zugehörige Themen

[Entwickeln von Filter Handlern](-search-ifilter-conceptual.md)

[Informationen zu Filter Handlern in Windows Search](-search-ifilter-about.md)

[Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search](-search-3x-wds-extidx-filters.md)

[Zurückgeben von Eigenschaften aus einem Filter Handler](-search-ifilter-property-filtering.md)

[Implementieren von Filter Handlern in Windows Search](-search-ifilter-constructing-filters.md)

[Registrieren von Filter Handlern](-search-ifilter-registering-filters.md)

[Testen von Filter Handlern](-search-ifilter-testing-filters.md)
