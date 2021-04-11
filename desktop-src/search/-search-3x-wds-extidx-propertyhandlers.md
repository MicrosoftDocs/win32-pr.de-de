---
description: Microsoft Windows Search verwendet Eigenschafts Handler, um die Werte von Eigenschaften aus Elementen zu extrahieren, und verwendet das Eigenschafts System Schema, um zu bestimmen, wie eine bestimmte Eigenschaft indiziert werden soll.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Entwickeln von Eigenschaften Handlern für Windows Search
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ac96e47738040321025b7f600e2c91109b08d51
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214465"
---
# <a name="developing-property-handlers-for-windows-search"></a>Entwickeln von Eigenschaften Handlern für Windows Search

Microsoft Windows Search verwendet Eigenschafts Handler, um die Werte von Eigenschaften aus Elementen zu extrahieren, und verwendet das Eigenschafts System Schema, um zu bestimmen, wie eine bestimmte Eigenschaft indiziert werden soll. Um Eigenschaftswerte zu lesen und zu indizieren, werden die Eigenschaften Handler von Windows Search außerhalb des Prozesses aufgerufen, um die Sicherheit und Stabilität zu verbessern. Im Gegensatz dazu werden Eigenschaften Handler in-Process von Windows-Explorer aufgerufen, um Eigenschaftswerte zu lesen und zu schreiben.

In diesem Thema wird das Thema " [Eigenschaften System](../properties/building-property-handlers.md) " mit speziellen Informationen zu Windows Search ergänzt. es enthält die folgenden Abschnitte:

-   [Entwurfsentscheidungen für Eigenschaften Handler](#design-decisions-for-property-handlers)
    -   [Eigenschafts Entscheidungen](#property-decisions)
    -   [Volltextunterstützung](#full-text-support)
    -   [Überlegungen zur Betriebs System Implementierung](#operating-system-implementatation-considerations)
-   [Schreiben von Eigenschafts Beschreibungsdateien](#writing-property-description-files)
-   [Implementieren von Eigenschaften Handlern](#implementing-property-handlers)
    -   [IInitializeWithStream](#iinitializewithstream)
    -   [IPropertyStore](#ipropertystore)
    -   [Ipropertystorecapabilitäten](#ipropertystorecapabilities)
-   [Sicherstellen, dass ihre Elemente indiziert werden](#ensuring-your-items-get-indexed)
-   [Installieren und Registrieren von Eigenschaften Handlern](#installing-and-registering-property-handlers)
-   [Testen und Problembehandlung von Eigenschaften Handlern](#testing-and-troubleshooting-property-handlers)
    -   [Installations-und Setup Tests](#installation-and-setup-tests)
    -   [Problembehandlung bei Eigenschaften Handlern](#troubleshooting-property-handlers)
-   [Verwenden von System-Supplied-Eigenschaften Handlern](#using-system-supplied-property-handlers)
-   [Zugehörige Themen](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a>Entwurfsentscheidungen für Eigenschaften Handler

Das Implementieren von Eigenschaften Handlern umfasst die folgenden Schritte:

1.  Treffen Sie Entwurfsentscheidungen bezüglich der Eigenschaften, die Sie unterstützen möchten.
2.  Erstellen einer Eigenschafts Beschreibungsdatei (. PropDesc) für Eigenschaften, die sich nicht bereits im Eigenschaften System befinden.
3.  Implementieren und Testen des Eigenschaften Handlers.
4.  Installieren und Registrieren des eigenschaftenhandlers und der Eigenschaften Beschreibungsdateien.
5.  Testen der Installation und Registrierung des eigenschaftenhandlers.

Bevor Sie beginnen, müssen Sie die folgenden Entwurfs Fragen berücksichtigen:

-   Welche Eigenschaften unterstützt das Dateiformat?
-   Sind diese Eigenschaften bereits im System Schema vorhanden?
-   Kann ein vorhandener vom System bereitgestellter Eigenschaften Handler verwendet werden?
-   Welche Eigenschaften können Endbenutzern angezeigt werden?
-   Welche Eigenschaften können Benutzer bearbeiten?
-   Sollte die Unterstützung für die Volltextsuche von einem Eigenschafts Handler oder einem Filter stammen?
-   Muss ich Legacy Anwendungen unterstützen? Wenn dies der Fall ist, was implementiere ich?

> [!Note]  
> Bevor Sie fortfahren, finden Sie weitere Informationen unter [Verwenden von System-Supplied-Eigenschaften Handlern](#using-system-supplied-property-handlers) , um zu ermitteln, ob Sie einen vom System bereitgestellten Eigenschaften Handler verwenden können

 

Nachdem Sie diese Entscheidungen getroffen haben, können Sie formale Beschreibungen Ihrer benutzerdefinierten Eigenschaften schreiben, damit die Windows-Suchmaschine mit der Indizierung Ihrer Dateien und Eigenschaften beginnen kann. Diese formalen Beschreibungen sind XML-Dateien, die im [Eigenschafts Beschreibungs Schema](/previous-versions//cc144127(v=vs.85))beschrieben werden.

### <a name="property-decisions"></a>Eigenschafts Entscheidungen

Wenn Sie überlegen, welche Eigenschaften unterstützt werden sollen, sollten Sie die Indizierungs-und Suchanforderungen Ihrer Benutzer identifizieren. Beispielsweise können Sie möglicherweise 100 möglicherweise nützliche Eigenschaften für Ihren Dateityp identifizieren, aber Benutzer sind möglicherweise an der Suche nach nur einer Handvoll interessiert. Außerdem empfiehlt es sich, Benutzern in Windows-Explorer eine andere, größere oder kleinere Gruppe dieser Eigenschaften anzuzeigen und Benutzern zu gestatten, nur eine Teilmenge der angezeigten Eigenschaften zu bearbeiten.

Ihr Dateityp unterstützt alle benutzerdefinierten Eigenschaften, die Sie definieren, sowie eine Reihe von System definierten Eigenschaften. Bevor Sie eine benutzerdefinierte Eigenschaft erstellen, überprüfen Sie die [Systemeigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) , um festzustellen, ob die Eigenschaft, die Sie unterstützen möchten, bereits durch eine System Eigenschaft definiert ist. Stellen Sie immer sicher, dass Sie die wichtigsten System definierten Eigenschaften unterstützen.

Es wird empfohlen, eine Matrix zu verwenden, die Sie beim Entwerfen Ihrer Eigenschaften unterstützt:



| Eigenschaftenname | Ist Indexable? | Kann angezeigt werden? | Kann bearbeitet werden? |
|---------------|---------------|-----------------|--------------|
| property1     | J             | J               | N            |
| Eigenschaft...   | J             | J               | N            |
| propertyN     | N             | N               | N            |



 

Sie müssen für jede dieser Eigenschaften bestimmen, welche Attribute vorhanden sein sollten, und Sie dann formal in den Eigenschafts Beschreibungs-XML-Dateien (. PropDesc) beschreiben. Zu den Attributen zählen der Datentyp der Eigenschaft, die Bezeichnung, die Hilfe Zeichenfolge und mehr. Bei indizierbaren Eigenschaften sollten Sie besonders auf die folgenden Eigenschafts Attribute achten, die im XML-Element [SearchInfo](../properties/propdesc-schema-searchinfo.md)   der Eigenschafts Beschreibungsdatei gefunden wurden.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>BESCHREIBUNG</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>ininvertedindex</td>
<td>Dies ist optional. Gibt an, ob ein Zeichen folgen Eigenschafts Wert in Wörter und jedes im umgekehrten Index gespeicherte Wort unterteilt werden soll. Der invertierte Index ermöglicht das effiziente suchen nach Wörtern und Ausdrücken über den Eigenschafts Wert mit "enthält" oder "frei Text" (z. b. Select... Where enthält einen &quot; Text &quot; ). Wenn diese Einstellung auf " <strong>false</strong>" festgelegt ist, erfolgt die Suche anhand der gesamten Zeichenfolge Für die meisten Zeichen folgen Eigenschaften sollte diese Eigenschaft auf <strong>true</strong>festgelegt sein. für nicht-Zeichen folgen Eigenschaften sollte This auf <strong>false</strong>festgelegt sein. Der Standardwert ist <strong>false</strong>.</td>
</tr>
<tr class="even">
<td>iscolumn</td>
<td>Dies ist optional. Gibt an, ob die-Eigenschaft in der Windows Search-Datenbank als Spalte gespeichert werden soll. Das Speichern der Eigenschaft als Spalte ermöglicht das Abrufen, sortieren, gruppieren und Filtern (d. h. die Verwendung eines beliebigen Prädikats außer enthält oder frei Text) für den gesamten Spaltenwert. Für Eigenschaften, die dem Benutzer angezeigt werden, sollte diese Eigenschaft auf " <strong>true</strong> " festgelegt sein, es sei denn, es handelt sich um eine sehr große Text Eigenschaft (z. b Der Standardwert ist <strong>false</strong>.</td>
</tr>
<tr class="odd">
<td>iscolumnsparse</td>
<td>Dies ist optional. Gibt an, ob eine Eigenschaft keinen Speicherplatz annimmt, wenn der Wert <strong>null</strong>ist. Eine nicht-Sparse-Eigenschaft benötigt für jedes Element Platz, auch wenn der Wert <strong>null</strong>ist. Wenn die Eigenschaft mehr wertig ist, ist dieses Attribut immer " <strong>true</strong>". Dieses Attribut sollte nur dann <strong>false</strong> lauten, wenn für jedes Element ein Wert vorhanden ist. Der Standardwert ist " <strong>true</strong>".</td>
</tr>
<tr class="even">
<td>columnindextype</td>
<td>Dies ist optional. Um die Abfrage zu optimieren, kann das Windows Search-Modul sekundäre Indizes für Eigenschaften erstellen, deren iscolumn =<strong>true</strong>ist. Dies erfordert mehr Verarbeitung und Speicherplatz während der Indizierung, verbessert jedoch die Leistung während der Abfrage. Wenn die Eigenschaft tendenziell sortiert, gruppiert oder gefiltert wird (d. h., Sie verwendet =,! =, < >, wie z. b. Übereinstimmungen), sollte dieses Attribut auf ondisk festgelegt werden &quot; &quot; . Der Standardwert ist " &quot; notindiziert" &quot; . Folgende Werte sind gültig:
<ul>
<li>Notindiziert: Es wird kein sekundärer Index erstellt.</li>
<li>Ondisk: Erstellen und speichern Sie einen sekundären Index auf dem Datenträger.</li>
</ul></td>
</tr>
<tr class="odd">
<td>MaxSize</td>
<td>Dies ist optional. Gibt die maximal zulässige Größe für den Eigenschafts Wert an, der in der Windows Search-Datenbank gespeichert ist. Dieser Grenzwert gilt für die einzeidualen Elemente eines Vektors, nicht für den Vektor als Ganzes. Werte, die diese Größe überschreiten, werden abgeschnitten. Der Standardwert ist &quot; 128 &quot; (Bytes).<br/> Derzeit verwendet Windows Search nicht den MAXSIZE-Wert, wenn die Menge der Daten berechnet wird, die Sie aus einer Datei akzeptiert. Stattdessen ist der Grenzwert, den Windows Search verwendet, das Produkt der Dateigröße und der MaxGrowFactor (Dateigröße N * MaxGrowFactor), die aus der Registrierung bei HKEY_LOCAL_MACHINE->Software >Microsoft->Windows Search->Erteilungs-Manager->MaxGrowFactor gelesen wird. Der Standardwert für MaxGrowFactor ist vier (4). Wenn Ihr Dateityp tendenziell klein ist, aber größere Eigenschaften hat, akzeptiert Windows Search möglicherweise nicht alle Eigenschaften Daten, die Sie ausgeben möchten. Sie können jedoch den MaxGrowFactor-Faktor entsprechend Ihren Anforderungen erhöhen. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Für das columnindextype-Attribut muss der Vorteil von schnelleren Abfragen mit der größeren Indizierungs Zeit und den Speicherplatz Kosten abgewogen werden, die die sekundären Indizes verursachen können. Diese Kosten werden jedoch nur für Elemente mit einem Wert ungleich **null** gezahlt, sodass dieses Attribut für die meisten Eigenschaften auf "ondisk" festgelegt werden kann.

 

### <a name="full-text-support"></a>Volltextunterstützung

Im Allgemeinen wird die Volltextsuche von Komponenten unterstützt, die als [Filter](-search-3x-wds-extidx-filters.md)bezeichnet werden. bei textbasierten Dateitypen mit unkomplizierten Dateiformaten können Eigenschafts Handler diese Funktionalität jedoch mit weniger Entwicklungsaufwand bereitstellen. Lesen Sie den Abschnitt [voll Text Inhalte](../properties/building-property-handlers-property-handlers.md) , um einen Vergleich der Filter-und eigenschaftenhandlerfunktionen zu finden, mit denen Sie entscheiden können, was für den Dateityp am besten ist. Besonders wichtig ist die Tatsache, dass Filter mehrere Sprachcode Bezeichner (LCIDs) pro Datei verarbeiten können, während dies bei Eigenschaften Handlern nicht der Fall ist.

> [!Note]  
> Da Eigenschafts Handler Inhalte nicht wie Filter segmentieren können, müssen große Dateien vollständig in den Arbeitsspeicher geladen werden.

 

### <a name="operating-system-implementatation-considerations"></a>Überlegungen zur Betriebs System Implementierung

### <a name="implementation-information-for-windows-7"></a>Implementierungs Informationen für Windows 7

In Windows 7 und höher gibt es neues Verhalten beim Registrieren eines Eigenschaften Handlers, [**IFilters**](/windows/win32/api/filter/nn-filter-ifilter)oder einer neuen Erweiterung. Wenn ein neuer Eigenschaften Handler und/oder **IFilter** installiert wird, werden Dateien mit den entsprechenden Erweiterungen automatisch neu indiziert.

In Windows 7 wird empfohlen, dass ein [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) in Verbindung mit den entsprechenden Eigenschaften Handlern installiert wird und dass der **IFilter** vor dem Eigenschaften Handler registriert wird. Durch die Registrierung des Eigenschaften Handlers wird die sofortige Neuindizierung von zuvor indizierten Dateien initiiert, ohne dass zunächst ein Neustart erforderlich ist. dabei werden alle zuvor registrierten IFilter für die Inhalts Indizierung genutzt.

Wenn nur ein [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ohne entsprechenden Eigenschaften Handler installiert wird, erfolgt die automatische Neuindizierung entweder nach einem Neustart des Indizierungs dienstanzdienstanzdienstanbieter oder einem Neustart des Systems.

Informationen zu eigenschaftenbeschreibungsflags für Windows 7 finden Sie in den folgenden Referenz Themen:

-   [Getpropertystoreflags](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [PropDesc- \_ ColumnIndex- \_ Typ](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [propde- \_ SearchInfo- \_ Flags](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a>Implementierungs Informationen für Windows Vista und frühere Versionen

Vor Windows Vista wurden von Filtern Unterstützung für das Auswerten und Auflisten von Dateiinhalten und-Eigenschaften bereitgestellt. Mit der Einführung des Eigenschaften Systems behandeln Eigenschaften Handler Dateieigenschaften, während Filterdatei Inhalte verarbeiten. Für Windows Vista müssen Sie nur eine partielle Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)-Schnittstelle in Abstimmung mit einem Eigenschafts Handler entwickeln, wie in [bewährte Methoden zum Erstellen von Filter Handlern in Windows Search](-search-3x-wds-extidx-filters.md)beschrieben.

Obwohl das-Eigenschaften System auch in der Windows Search-Installation für Windows XP enthalten ist, ist es für Drittanbieter-und Legacy Anwendungen möglicherweise erforderlich, dass Filter sowohl Inhalte als auch Eigenschaften verarbeiten. Wenn Sie auf der Windows XP-Plattform entwickeln, sollten Sie daher eine vollständige Filter Implementierung und einen Eigenschafts Handler für den Dateityp oder die benutzerdefinierte Eigenschaft bereitstellen.

 

## <a name="writing-property-description-files"></a>Schreiben von Eigenschafts Beschreibungsdateien

Die Struktur der Eigenschafts Beschreibungs-XML-Dateien (. PropDesc) wird im Thema [propertydescription](../properties/propdesc-schema-propertydescription.md) beschrieben. Besonderes Interesse für die Suche sind die Attribute des [SearchInfo](../properties/propdesc-schema-searchinfo.md) -Elements. Nachdem Sie entschieden haben, welche Eigenschaften unterstützt werden sollen, müssen Sie Eigenschafts Beschreibungsdateien für die einzelnen Eigenschaften erstellen und registrieren. Wenn Sie Ihre. PropDesc-Dateien registrieren, sind Sie in der Eigenschafts Beschreibungs Liste des Schemas enthalten und werden zu Spaltennamen innerhalb des Eigenschaften Stores der Suchmaschine.

Sie können Ihre benutzerdefinierten Eigenschaften Beschreibungen mithilfe der [psregisterpropertyschema](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) -Funktion registrieren, einer Wrapper-API, die das ipropertysystem:: registerpropertyschema des Schema Subsystems aufruft. Diese Funktion informiert das Schema Subsystem über das Hinzufügen von Eigenschafts Beschreibungs-Schema Dateien (. PropDesc) mithilfe von Dateipfaden zu den. PropDesc-Dateien auf dem lokalen Computer, in der Regel das Installationsverzeichnis der Anwendung unter "Programme". In der Regel Ruft ein Setup oder eine Anwendung (z. b. das Installationsprogramm des Eigenschaften Handlers) diese Methode nach der Installation der. PropDesc-Datei (en) auf.

 

## <a name="implementing-property-handlers"></a>Implementieren von Eigenschaften Handlern

Die Entwicklung eines Eigenschaften Handlers umfasst die Implementierung der folgenden Schnittstellen:

-   Iinitialzewithstream: stellt die streambasierte Initialisierung des Eigenschafts Handlers bereit.
-   IPropertyStore: Listet Eigenschaftswerte auf, ruft Sie ab und legt Sie fest.
-   Ipropertystorecapabili: optional. Gibt an, ob Benutzer eine Eigenschaft von einer Benutzeroberfläche aus bearbeiten können.

### <a name="iinitializewithstream"></a>IInitializeWithStream

Wie im Thema " [Eigenschaften System](../properties/building-property-handlers.md) " beschrieben, wird dringend empfohlen, Eigenschafts Handler mit **IInitializeWithStream** zu implementieren, um die streambasierte Initialisierung durchzuführen. Wenn Sie IInitializeWithStream nicht implementieren möchten, muss der Eigenschafts Handler die Ausführung im Isolations Prozess deaktivieren, indem das Flag disableprocessisolation für den Registrierungsschlüssel des Eigenschaften Handlers festgelegt wird. Die Deaktivierung der Prozess Isolation ist in der Regel nur für Legacy-Eigenschaften Handler vorgesehen und sollte durch neuen Code energisch vermieden werden.

### <a name="ipropertystore"></a>IPropertyStore

Zum Erstellen eines Eigenschaften Handlers müssen Sie die [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Schnittstelle mit den folgenden Methoden implementieren.



| Methode   | BESCHREIBUNG                                                         |
|----------|---------------------------------------------------------------------|
| Commit   | Speichert eine Eigenschafts Änderung in der Datei.                                |
| GetAt    | Ruft einen Eigenschafts Schlüssel aus dem Array von Eigenschaften eines Elements ab.        |
| GetCount | Ruft die Anzahl der Eigenschaften ab, die an die Datei angefügt sind.                 |
| GetValue | Ruft Daten für eine bestimmte Eigenschaft ab.                             |
| SetValue | Legt einen neuen Eigenschafts Wert fest oder ersetzt oder entfernt einen vorhandenen Wert. |



 

 

 

Wichtige Überlegungen zur Implementierung dieser Schnittstelle sind in der [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore) -Dokumentation enthalten.

> [!Note]  
> Wenn der Eigenschafts Handler mehrere Werte für dieselbe Eigenschaft für ein bestimmtes Element ausgibt, wird nur der letzte ausgegebene Wert im Katalog gespeichert.

 

 

### <a name="ipropertystorecapabilities"></a>Ipropertystorecapabilitäten

Eigenschaften Handler können diese Schnittstelle optional implementieren, um die Fähigkeit eines Benutzers zu deaktivieren, bestimmte Eigenschaften zu bearbeiten. Diese Eigenschaften sind in der Regel auf der Detailseite und im Bereich bearbeitbar, Sie können jedoch nicht unter dem implementierenden Eigenschaften Handler bearbeitet werden. Die Implementierung dieser Schnittstelle bietet eine bessere Benutzeroberfläche als die Alternative – ein einfacher Laufzeitfehler in der Shell.

 

## <a name="ensuring-your-items-get-indexed"></a>Sicherstellen, dass ihre Elemente indiziert werden

Nachdem Sie den Eigenschafts Handler implementiert haben, möchten Sie sicherstellen, dass die Elemente, für die der Handler registriert ist, indiziert werden. Sie können den [Katalog-Manager](-search-3x-wds-mngidx-catalog-manager.md) verwenden, um die erneute Indizierung zu initiieren. Außerdem können Sie mit dem [Crawl Scope-Manager](-search-3x-wds-extidx-csm.md) Standardregeln einrichten, die die URLs angeben, die der Indexer durchforsten soll. Eine weitere Möglichkeit besteht darin, das Codebeispiel "REINDEX" in den [Windows Search SDK-Beispielen](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)zu befolgen.

Weitere Informationen finden Sie unter [Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md) und [Verwenden des Crawl Scope-Managers](-search-3x-wds-extidx-csm.md).

 

## <a name="installing-and-registering-property-handlers"></a>Installieren und Registrieren von Eigenschaften Handlern

Nachdem der Eigenschaften Handler implementiert wurde, muss er registriert und seine Dateinamenerweiterung dem Handler zugeordnet sein. Das folgende Beispiel zeigt die Registrierungsschlüssel und-Werte, die hierfür erforderlich sind.

```
HKEY_CLASSES_ROOT
   CLSID
      {<CLSID for property handler>}
         (Default) = <Property Handler Name>
         InProcServer32
            (Default) = <full path to property handler dll>
            ThreadingModel = <your threading model>
```

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         Windows
            CurrentVersion
               PropertySystem
                  PropertyHandlers
                     <.fileextention>
                        (Default) = {<CLSID for property handler>}
```

 

## <a name="testing-and-troubleshooting-property-handlers"></a>Testen und Problembehandlung von Eigenschaften Handlern

In der folgenden Liste finden Sie Ratschläge zu den Arten von Tests, die Sie durchführen sollten:

-   Testen Sie die Ausgabe von jeder einzelnen Eigenschaft, die vom Dateityp unterstützt wird.
-   Verwenden Sie große Eigenschaftswerte, z. b. ein großes-Metatag in HTML-Dokumenten.
-   Überprüfen Sie, ob der Eigenschafts Handler Datei Handles nicht löscht, indem Sie Sie bearbeiten, nachdem Sie die Ausgabe des Eigenschaften Handlers erhalten haben, oder indem Sie ein Tool wie oh.exe vor und nach dem Auflisten von Dateieigenschaften verwenden.
-   Testen Sie alle Dateitypen, die dem Eigenschaften Handler zugeordnet sind. Überprüfen Sie z. b., ob der HTML-Filter mit den Dateitypen htm und HTML funktioniert.
-   Testen Sie mit beschädigten Dateien. Der Eigenschafts Handler sollte ordnungsgemäß fehlschlagen.
-   Wenn eine Anwendung die Verschlüsselung unterstützt, testen Sie, ob der Eigenschaften Handler verschlüsselten Text ausgibt.
-   Wenn der Eigenschafts Handler die Volltextsuche unterstützt:
    -   Verwenden Sie mehrere spezielle Unicode-Zeichen im Dateiinhalt, und testen Sie Ihre Ausgabe.
    -   Testen Sie die Verarbeitung sehr großer Dokumente, um sicherzustellen, dass der Eigenschafts Handler erwartungsgemäß funktioniert.

### <a name="installation-and-setup-tests"></a>Installations-und Setup Tests

Schließlich müssen Sie die Installations-und Deinstallations Routinen testen.

-   Die Installation muss bei fehlgeschlagenen Installationen (z. b. beim Abbrechen und anschließenden erneuten Starten des Setups) wieder hergestellt werden.
-   Die Deinstallation muss alle Dateien löschen, die dem Eigenschaften Handler zugeordnet sind.
-   Bei der Deinstallation dürfen Dateien nicht gelöscht werden, die mit der Installation des Eigenschaften Handlers verknüpft sind.
-   Die dem Eigenschafts Handler zugeordneten Registrierungsschlüssel müssen entfernt werden, wenn Sie deinstalliert werden.
-   Die Deinstallation muss funktionieren, auch wenn Dateien aus dem Installationsverzeichnis gelöscht werden.

### <a name="troubleshooting-property-handlers"></a>Problembehandlung bei Eigenschaften Handlern

Im folgenden werden einige häufige Fehler beim Entwickeln von Eigenschaften Handlern aufgeführt:

-   Installieren von. PropDesc-Dateien oder-DLLs unter einem Benutzerverzeichnis.
-   Registrieren von Komponenten mithilfe relativer Pfade.
-   Die Komponenten unter HKEY \_ Current \_ User anstelle des lokalen HKEY-Computers werden registriert \_ \_ .
-   Das Festlegen von disableprocessisolations für nicht-Stream-Handler wird vergessen.
-   Die Testdatei wird an einem nicht indizierten Speicherort platziert.

Wenn Sie Probleme haben, den Eigenschaftenhandler mit dem Indexer zu arbeiten, finden Sie hier einige Tipps, die Ihnen bei der Problembehandlung helfen:

-   Überprüfen Sie, ob ihre Eigenschaften Beschreibungen (. PropDesc-Dateien) nach Bedarf als iscolumn = "**true**", "isviewable ="**true**"und" isquervable = "**true**" gekennzeichnet sind.
-   Überprüfen Sie, ob sich Ihre. PropDesc-Dateien an einem globalen Speicherort befinden.
-   Vergewissern Sie sich, dass Sie Ihre. PropDesc-Dateien mit absoluten Pfaden registriert haben.
-   Vergewissern Sie sich, dass das Ereignisprotokoll keine Fehler beim Registrieren Ihrer. PropDesc-Datei aufgezeichnet hat.
-   Stellen Sie sicher, dass sich Ihre DLLs an einem globalen Speicherort befinden (und nicht unter Ihrem Benutzerprofil).
-   Überprüfen Sie, ob Ihre DLLs unter HKEY- \_ Software Klassen für lokale Computer registriert sind \_ \\ \\ .
-   Stellen Sie sicher, dass Ihre DLLs mit vollständigen Pfaden registriert sind (oder reg-Zeichen folgen \_ \_ , die auf absolute Pfade erweitert werden, mithilfe von Umgebungsvariablen, die vom System Konto bekannt sind).
-   Überprüfen Sie, ob der Eigenschafts Handler im Windows-Explorer funktioniert.
-   Es wird empfohlen, IInitializeWithStream zu verwenden, wenn Sie IInitializeWithFile oder IInitializeWithItem verwenden müssen, vergewissern Sie sich, dass Sie disableprocessisolations angeben.
-   Vergewissern Sie sich, dass der Dateityp in der Systemsteuerung für die Indizierungs Optionen als indizierter Dateityp
-   Überprüfen Sie, ob sich die Testdatei an einem indizierten Speicherort befindet
-   Vergewissern Sie sich, dass die Testdatei seit der Installation des Eigenschaften Handlers geändert wurde.

Wenn sich die Testdatei an einem indizierten Speicherort befindet und der Indexer diese Position bereits durchlaufen hat, müssen Sie die Datei auf irgendeine Weise ändern, um eine Neuindizierung der Datei zu initiieren.

 

## <a name="using-system-supplied-property-handlers"></a>Verwenden von System-Supplied-Eigenschaften Handlern

Windows enthält eine Reihe von vom System bereitgestellten Eigenschaften Handlern, die Sie verwenden können, wenn das Format des Dateityps kompatibel ist. Wenn Sie eine neue Dateierweiterung definieren, die eines dieser Formate verwendet, können Sie die vom System bereitgestellten Handler verwenden, indem Sie die Handlerklassen-ID (CLSID) für die Dateierweiterung registrieren.

Sie können die in der folgenden Tabelle aufgeführte CLSID verwenden, um die vom System bereitgestellten Eigenschaften Handler für den Datei Formattyp zu registrieren.



| Format          | CLSID                                  |
|-----------------|----------------------------------------|
| OLE-DOCFILE     | {8d80504a-0826-40c5-97e1-ebc68f 953792} |
| Speichern von Spiel-XML   | {ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60} |
| XPS-/OPC-Handler | {45670fa8-ed97-4f 44-bc93-305082590bfb} |
| XML             | {c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9} |



 

Vor dem Erstellen einer benutzerdefinierten Eigenschaft sollten Sie sicherstellen, dass es keine System definierte Eigenschaft gibt, die Sie stattdessen verwenden können. Sie können die System definierten Eigenschaften auflisten, indem Sie [**psenumeratepropertybeschreibungen**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) aufrufen oder das Befehlszeilen Tool prop.exe verwenden.

Das System Schema definiert, wie diese Eigenschaften mit dem Indexer interagieren, und Sie können diese Eigenschaften nicht ändern. Außerdem muss die Anwendung, mit der Sie den Dateityp erstellen, bearbeiten und speichern, auch mit einem bestimmten Verhalten übereinstimmen. Wenn die Anwendung z. b. Sicheres Speichern implementiert (wobei eine temporäre Datei während der Bearbeitung erstellt wird und dann ReplaceFile () verwendet wird, um die neue Version für die alte zu tauschen), muss Sie alle Eigenschaften der ursprünglichen Datei in die neue Datei übertragen. Dies bedeutet, dass die Datei von Benutzern oder anderen Anwendungen hinzugefügte Eigenschaften verliert.

 

**Beispiel**

Im folgenden Beispiel wird die Registrierung des vom System bereitgestellten OLE DOCFILE-Handlers für einen Dateityp mit einem gezeigt. Oledocfile-Erweiterung.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

Das folgende Beispiel zeigt die Registrierung der Eigenschaften Listen Informationen, sodass Eigenschaften von. Oledocfile-Dateien werden auf der Registerkarte Details und im Bereich angezeigt.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         ExtendedTileInfo = prop:System.ItemType;System.Size;System.DateModified;System.Author;System.OfflineAvailability
         FullDetails = prop:System.PropGroup.Description;System.Title;System.Subject;
System.Keywords;System.Category;System.Comment;System.PropGroup.Origin;
System.Author;System.Document.LastAuthor;System.Document.RevisionNumber;
System.Document.Version;System.ApplicationName;System.Company;System.Document.Manager;
System.Document.DateCreated;System.Document.DateSaved;System.Document.DatePrinted;
System.Document.TotalEditingTime;System.PropGroup.Content;System.ContentStatus;
System.ContentType;System.Document.PageCount;System.Document.WordCount;
System.Document.CharacterCount;System.Document.LineCount;
System.Document.ParagraphCount;System.Document.Template;System.Document.Scale;
System.Document.LinksDirty;System.Language;System.PropGroup.FileSystem;
System.ItemNameDisplay;System.ItemType;System.ItemFolderPathDisplay;
System.DateCreated;System.DateModified;System.Size;System.FileAttributes;
System.OfflineAvailability;System.OfflineStatus;System.SharedWith;
System.FileOwner;System.ComputerName
         InfoTip = prop:System.ItemType;System.Size;System.DateModified;System.Document.PageCoun
         PerceivedType = document
         PreviewDetails = prop:*System.DateModified;System.Author;System.Keywords;
*System.Size;System.Title;System.Comment;System.Category;
*System.Document.PageCount;System.ContentStatus;System.ContentType;
*System.OfflineAvailability;*System.OfflineStatus;System.Subject;
*System.DateCreated;*System.SharedWith
```

 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Eigenschafts Zuordnungen](-search-3x-wds-propertymappings.md)
</dt> <dt>

**Licher**
</dt> <dt>

[Bewährte Methoden zum Erstellen von Filter Handlern in Windows Search](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[Der Indizierungsprozess](-search-indexing-process-overview.md)
</dt> <dt>

[Entwickeln von Protokoll Handlern](-search-3x-wds-phaddins.md)
</dt> <dt>

[System definierte Eigenschaften für benutzerdefinierte Dateiformate](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Eigenschaften System](../properties/building-property-handlers.md)
</dt> <dt>

[System Eigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> <dt>

[Beispiele für Windows Search SDK](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
