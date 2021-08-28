---
description: Microsoft Windows Search verwendet Eigenschaftenhandler, um die Werte von Eigenschaften aus Elementen zu extrahieren, und verwendet das Eigenschaftensystemschema, um zu bestimmen, wie eine bestimmte Eigenschaft indiziert werden soll.
ms.assetid: b475329a-1ed7-43a4-8e11-3700889a4ce9
title: Entwickeln von Eigenschaftenhandlern für die Windows Suche
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3933353d8bf00c3a68a2259daf94a1ce4f13d295
ms.sourcegitcommit: c276a8912787b2cda74dcf54eb96df961bb1188b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2021
ms.locfileid: "122627325"
---
# <a name="developing-property-handlers-for-windows-search"></a>Entwickeln von Eigenschaftenhandlern für die Windows Suche

Microsoft Windows Search verwendet Eigenschaftenhandler, um die Werte von Eigenschaften aus Elementen zu extrahieren, und verwendet das Eigenschaftensystemschema, um zu bestimmen, wie eine bestimmte Eigenschaft indiziert werden soll. Zum Lesen und Indizieren von Eigenschaftswerten werden Eigenschaftshandler von Windows Search außerhalb des Prozesses aufgerufen, um die Sicherheit und Stabilität zu verbessern. Im Gegensatz dazu werden Eigenschaftshandler von Windows Explorer prozessin-process aufgerufen, um Eigenschaftswerte zu lesen und zu schreiben.

Dieses Thema ergänzt das Thema [Eigenschaftensystem](../properties/building-property-handlers.md) um spezifische Informationen für Windows Search und enthält die folgenden Abschnitte:

-   [Entwurfsentscheidungen für Eigenschaftenhandler](#design-decisions-for-property-handlers)
    -   [Eigenschaftenentscheidungen](#property-decisions)
    -   [Volltextunterstützung](#full-text-support)
    -   [Überlegungen zur Implementierung des Betriebssystems](#operating-system-implementatation-considerations)
-   [Schreiben von Eigenschaftenbeschreibungsdateien](#writing-property-description-files)
-   [Implementieren von Eigenschaftenhandlern](#implementing-property-handlers)
    -   [Iinitializewithstream](#iinitializewithstream)
    -   [Ipropertystore](#ipropertystore)
    -   [IPropertyStoreCapabilities](#ipropertystorecapabilities)
-   [Sicherstellen, dass Ihre Elemente indiziert werden](#ensuring-your-items-get-indexed)
-   [Installieren und Registrieren von Eigenschaftenhandlern](#installing-and-registering-property-handlers)
-   [Testen und Problembehandlung von Eigenschaftenhandlern](#testing-and-troubleshooting-property-handlers)
    -   [Installations- und Setuptests](#installation-and-setup-tests)
    -   [Problembehandlung bei Eigenschaftenhandlern](#troubleshooting-property-handlers)
-   [Verwenden von System-Supplied-Eigenschaftenhandlern](#using-system-supplied-property-handlers)
-   [Zugehörige Themen](#related-topics)

 

## <a name="design-decisions-for-property-handlers"></a>Entwurfsentscheidungen für Eigenschaftenhandler

Das Implementieren von Eigenschaftenhandlern umfasst die folgenden Schritte:

1.  Treffen von Entwurfsentscheidungen in Bezug auf die Eigenschaften, die Sie unterstützen möchten.
2.  Erstellen einer Eigenschaftenbeschreibungsdatei (.propdesc) für Eigenschaften, die nicht bereits im Eigenschaftensystem vorhanden sind.
3.  Implementieren und Testen des Eigenschaftenhandlers.
4.  Installieren und Registrieren der Eigenschaftenhandler- und Eigenschaftenbeschreibungsdateien.
5.  Testen der Installation und Registrierung von Eigenschaftenhandlern.

Bevor Sie beginnen, müssen Sie die folgenden Designfragen berücksichtigen:

-   Welche Eigenschaften unterstützt bzw. sollte das Dateiformat unterstützen?
-   Sind diese Eigenschaften bereits im Systemschema enthalten?
-   Kann ich einen vorhandenen vom System bereitgestellten Eigenschaftenhandler verwenden?
-   Welche Eigenschaften können Endbenutzern angezeigt werden?
-   Welche Eigenschaften können Benutzer bearbeiten?
-   Sollte die Volltextsuche von einem Eigenschaftenhandler oder Filter unterstützt werden?
-   Muss ich Legacyanwendungen unterstützen? Wenn ja, was implementiere ich?

> [!Note]  
> Bevor Sie fortfahren, lesen [Sie Using System-Supplied Property Handlers (Verwenden von System-Supplied-Eigenschaftenhandlern),](#using-system-supplied-property-handlers) um festzustellen, ob Sie einen vom System bereitgestellten Eigenschaftenhandler verwenden können, um Sowohl Zeit als auch Entwicklungsressourcen zu sparen.

 

Nachdem Sie diese Entscheidungen getroffen haben, können Sie formale Beschreibungen Ihrer benutzerdefinierten Eigenschaften schreiben, damit die Windows-Suchmaschine mit der Indizierung Ihrer Dateien und Eigenschaften beginnen kann. Bei diesen formalen Beschreibungen handelt es sich um XML-Dateien, die unter [Eigenschaftenbeschreibungsschema](/previous-versions//cc144127(v=vs.85))beschrieben werden.

### <a name="property-decisions"></a>Eigenschaftenentscheidungen

Wenn Sie überlegen, welche Eigenschaften unterstützt werden sollen, sollten Sie die Indizierungs- und Suchanforderungen Ihrer Benutzer identifizieren. Beispielsweise können Sie möglicherweise hundert potenziell nützliche Eigenschaften für Ihren Dateityp identifizieren, aber Benutzer sind möglicherweise nur an einer Handvoll Suchvorgänge interessiert. Darüber hinaus können Sie benutzern in Windows Explorer eine andere, größere oder kleinere Gruppe dieser Eigenschaften anzeigen und Benutzern erlauben, nur eine Teilmenge dieser angezeigten Eigenschaften zu bearbeiten.

Ihr Dateityp kann alle benutzerdefinierten Eigenschaften unterstützen, die Sie definieren, sowie eine Reihe von systemdefinierte Eigenschaften. Lesen Sie vor dem Erstellen einer benutzerdefinierten Eigenschaft die Informationen unter [Systemeigenschaften,](https://msdn.microsoft.com/library/bb763010(VS.85).aspx) um festzustellen, ob die eigenschaft, die Sie unterstützen möchten, bereits durch eine Systemeigenschaft definiert ist. Stellen Sie immer sicher, dass Sie die wichtigsten systemdefinierte Eigenschaften unterstützen.

Es wird empfohlen, eine Matrix zu verwenden, um Ihre Eigenschaften zu entwerfen:



| Eigenschaftenname | Ist indexierbar? | Kann angezeigt werden? | Kann bearbeitet werden? |
|---------------|---------------|-----------------|--------------|
| property1     | J             | J               | N            |
| Eigenschaft...   | J             | J               | N            |
| propertyn     | N             | N               | N            |



 

Für jede dieser Eigenschaften müssen Sie bestimmen, welche Attribute sie aufweisen soll, und sie dann formell in XML-Dateien zur Eigenschaftenbeschreibung (PROPDESC) beschreiben. Zu den Attributen gehören der Datentyp der Eigenschaft, die Bezeichnung, die Hilfezeichenfolge und vieles mehr. Bei indizierbaren Eigenschaften sollten Sie besonders auf die folgenden Eigenschaftsattribute achten, die sich im [searchInfo](../properties/propdesc-schema-searchinfo.md)   XML-Element der Eigenschaftenbeschreibungsdatei befinden.



<table>
<colgroup>
<col  />
<col  />
</colgroup>
<thead>
<tr class="header">
<th>Attribut</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>inInvertedIndex</td>
<td>Optional. Gibt an, ob ein Zeichenfolgeneigenschaftswert in Wörter unterteilt und jedes Wort im umgekehrten Index gespeichert werden soll. Der invertierte Index ermöglicht eine effiziente Suche nach Wörtern und Ausdrücken über den Eigenschaftswert mit CONTAINS oder FREETEXT (z. B. SELECT ... WHERE CONTAINS &quot; sometext &quot; ). Wenn <strong>false</strong>festgelegt ist, werden Suchvorgänge für die gesamte Zeichenfolge durchgeführt. Für die meisten Zeichenfolgeneigenschaften sollte diese auf <strong>TRUE</strong>festgelegt sein. Eigenschaften, die keine Zeichenfolgen sind, sollten auf FALSE festgelegt <strong>sein.</strong> Der Standardwert ist <strong>FALSE.</strong></td>
</tr>
<tr class="even">
<td>isColumn</td>
<td>Optional. Gibt an, ob die Eigenschaft in der Windows Search-Datenbank als Spalte gespeichert werden soll. Das Speichern der Eigenschaft als Spalte ermöglicht das Abrufen, Sortieren, Gruppieren und Filtern (d. h. das Verwenden eines beliebigen Prädikats mit Ausnahme von CONTAINS oder FREETEXT) für den gesamten Spaltenwert. Eigenschaften, die dem Benutzer angezeigt werden, sollten auf <strong>TRUE</strong> festgelegt sein, es sei denn, es handelt sich um eine sehr große Texteigenschaft (z. B. den Text eines Dokuments), die im umgekehrten Index durchsucht werden würde. Der Standardwert ist <strong>FALSE.</strong></td>
</tr>
<tr class="odd">
<td>isColumnSparse</td>
<td>Optional. Gibt an, ob eine Eigenschaft keinen Speicherplatz einnimmt, wenn der Wert <strong>NULL</strong>ist. Eine Nicht-Sparseeigenschaft nimmt Speicherplatz für jedes Element in Anspruch, auch wenn der Wert <strong>NULL</strong>ist. Wenn die -Eigenschaft mehrwertiger ist, ist dieses Attribut immer <strong>TRUE.</strong> Dieses Attribut sollte nur <strong>FALSE</strong> sein, wenn für jedes Element ein Wert vorhanden ist. Der Standardwert ist <strong>TRUE.</strong></td>
</tr>
<tr class="even">
<td>columnIndexType</td>
<td>Optional. Zur Optimierung der Abfrage kann die Windows-Suchmaschine sekundäre Indizes für Eigenschaften erstellen, die isColumn=<strong>TRUE</strong>aufweisen. Dies erfordert mehr Verarbeitung und Speicherplatz während der Indizierung, verbessert aber die Leistung während der Abfrage. Wenn die Eigenschaft häufig nach Benutzern sortiert, gruppiert oder gefiltert wird (d. h. mit =, !=, <, >, LIKE, MATCHES), sollte dieses Attribut auf OnDisk festgelegt &quot; &quot; werden. Der Standardwert ist &quot; NotIndexed. &quot; Folgende Werte sind gültig:
<ul>
<li>NotIndexed: Es wird kein sekundärer Index erstellt.</li>
<li>OnDisk: Erstellen und speichern Sie einen sekundären Index auf dem Datenträger.</li>
</ul></td>
</tr>
<tr class="odd">
<td>Maxsize</td>
<td>Optional. Gibt die maximal zulässige Größe für den Eigenschaftswert an, der in der datenbankgespeicherten Windows gespeichert ist. Dieser Grenzwert gilt für die einzelnen Elemente eines Vektors, nicht für den Vektor als Ganzes. Werte, die über diese Größe hinausgehen, werden abgeschnitten. Der Standardwert ist &quot; 128 &quot; (Bytes).<br/> Derzeit verwendet Windows Search bei der Berechnung der Datenmenge, die sie aus einer Datei akzeptiert, nicht maxSize. Stattdessen ist das Limit, das Windows Search verwendet, das Produkt der Dateigröße und des MaxGrowFactor (Dateigröße N * MaxGrowFactor), das unter HKEY_LOCAL_MACHINE->Software->Microsoft->Windows Search->Gathering Manager->MaxGrowFactor aus der Registrierung gelesen wird. Der Standardwert von MaxGrowFactor ist vier (4). Wenn Ihr Dateityp tendenziell klein ist, aber größere Eigenschaften aufweist, akzeptiert Windows Search möglicherweise nicht alle Eigenschaftsdaten, die Sie aus geben möchten. Sie können den MaxGrowFactor jedoch entsprechend Ihren Anforderungen erhöhen. <br/></td>
</tr>
</tbody>
</table>



 

> [!Note]  
> Für das columnIndexType-Attribut muss der Vorteil schnellerer Abfragen gegen die höheren Indizierungszeit- und Speicherplatzkosten abgewogen werden, die die sekundären Indizes verursachen können. Diese Kosten werden jedoch nur für Elemente bezahlt, deren Wert nicht NULL ist, sodass dieses Attribut für die meisten Eigenschaften auf "OnDisk" festgelegt werden kann.

 

### <a name="full-text-support"></a>Volltextunterstützung

Im Allgemeinen wird die Volltextsuche von Komponenten unterstützt, die als Filter [bezeichnet werden.](-search-3x-wds-extidx-filters.md) Bei textbasierten Dateitypen mit formatbasierten Dateiformaten können Eigenschaftenhandler diese Funktionalität jedoch mit geringerem Entwicklungsaufwand bereitstellen. Im Abschnitt Volltextinhalt [finden](../properties/building-property-handlers-property-handlers.md) Sie einen Vergleich der Filter- und Eigenschaftenhandlerfunktionen, damit Sie entscheiden können, was für Ihren Dateityp am besten ist. Von besonderer Bedeutung ist die Tatsache, dass Filter mehrere Sprachcodebezeichner (Language Code Identifiers, LCIDs) pro Datei verarbeiten können, während Eigenschaftenhandler dies nicht können.

> [!Note]  
> Da Eigenschaftenhandler Inhalte nicht auf die Weise, wie Filter es können, auf blockieren können, müssen große Dateien (selbst wenn es sich um unformatierte Dateiformate handelt) vollständig in den Arbeitsspeicher geladen werden.

 

### <a name="operating-system-implementatation-considerations"></a>Überlegungen zur Implementierung des Betriebssystems

### <a name="implementation-information-for-windows-7"></a>Implementierungsinformationen für Windows 7

In Windows 7 und höher gibt es ein neues Verhalten beim Registrieren eines Eigenschaftenhandlers, [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter)oder einer neuen Erweiterung. Wenn ein neuer Eigenschaftenhandler und/oder **IFilter** installiert wird, werden Dateien mit den entsprechenden Erweiterungen automatisch neu indiziert.

In Windows 7 wird empfohlen, einen [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) in Verbindung mit den entsprechenden Eigenschaftenhandlern zu installieren und den **IFilter** vor dem Eigenschaftenhandler zu registrieren. Die Registrierung des Eigenschaftenhandlers initiiert eine sofortige neuindizierte Indizierung zuvor indizierter Dateien, ohne dass zuerst ein Neustart erforderlich ist, und nutzt alle zuvor registrierten IFilter für die Inhaltsindizierung.

Wenn nur [**ein IFilter**](/windows/win32/api/filter/nn-filter-ifilter) ohne einen entsprechenden Eigenschaftenhandler installiert ist, erfolgt die automatische Neuindizierung entweder nach einem Neustart des Indizierungsdiensts oder nach einem Neustart des Systems.

Spezifische Eigenschaftenbeschreibungsflags für Windows 7 finden Sie in den folgenden Referenzthemen:

-   [GETPROPERTYSTOREFLAGS](/windows/win32/api/propsys/ne-propsys-getpropertystoreflags)
-   [PROPDESC \_ \_ COLUMNINDEX-TYP](/windows/win32/api/propsys/ne-propsys-propdesc_columnindex_type)
-   [PROPDESC \_ \_ SEARCHINFO-FLAGS](/windows/win32/api/propsys/ne-propsys-propdesc_searchinfo_flags)

### <a name="implementation-information-for-windows-vista-and-earlier"></a>Implementierungsinformationen für Windows Vista und früher

Vor der Windows Vista stellten Filter Unterstützung für das Analyse- und Aufzählen von Dateiinhalten und -eigenschaften zur Verfügung. Mit der Einführung des Eigenschaftensystems verarbeiten Eigenschaftenhandler Dateieigenschaften, während Filter Dateiinhalte verarbeiten. Für Windows Vista müssen Sie nur eine partielle Implementierung der [**IFilter-Schnittstelle**](/windows/win32/api/filter/nn-filter-ifilter)in Koordination mit einem Eigenschaftenhandler entwickeln, wie unter [Best Practices for Creating Filter Handlers in Windows Search](-search-3x-wds-extidx-filters.md)beschrieben.

Das Eigenschaftensystem ist zwar auch in der Windows Search-Installation für Windows XP enthalten, aber für Drittanbieter- und Legacyanwendungen kann es erforderlich sein, dass Filter sowohl Inhalte als auch Eigenschaften verarbeiten. Wenn Sie also auf der Windows XP-Plattform entwickeln, sollten Sie eine vollständige Filterimplementierung sowie einen Eigenschaftenhandler für Den Dateityp oder die benutzerdefinierte Eigenschaft bereitstellen.

 

## <a name="writing-property-description-files"></a>Schreiben von Eigenschaftenbeschreibungsdateien

Die Struktur von XML-Dateien mit Eigenschaftenbeschreibung (.propdesc) wird im [Thema propertyDescription](../properties/propdesc-schema-propertydescription.md) beschrieben. Von besonderem Interesse für die Suche sind die Attribute des [searchInfo-Elements.](../properties/propdesc-schema-searchinfo.md) Nachdem Sie entschieden haben, welche Eigenschaften unterstützt werden, müssen Sie Eigenschaftenbeschreibungsdateien für jede Eigenschaft erstellen und registrieren. Wenn Sie Ihre PROPDESC-Dateien registrieren, sind sie in der Eigenschaftenbeschreibungsliste des Schemas enthalten und werden zu Spaltennamen im Eigenschaftenspeicher der Suchmaschine.

Sie können Ihre benutzerdefinierten Eigenschaftenbeschreibungen mithilfe der [PSRegisterPropertySchema-Funktion](/windows/win32/api/propsys/nf-propsys-psregisterpropertyschema) registrieren, einer Wrapper-API, die das IPropertySystem::RegisterPropertySchema des Schemasubsystems aufruft. Diese Funktion informiert das Schemasubsystem über das Hinzufügen von Eigenschaftenbeschreibungsschemadateien (PROPDESC-Dateien) mithilfe von Dateipfaden zu den PROPDESC-Dateien auf dem lokalen Computer, in der Regel über das Installationsverzeichnis der Anwendung unter "Programme". In der Regel wird diese Methode von einem Setup oder einer Anwendung (z. B. ihrem Installationsprogramm für den Eigenschaftenhandler) nach der Installation der PROPDESC-Datei(en) aufgerufen.

 

## <a name="implementing-property-handlers"></a>Implementieren von Eigenschaftenhandlern

Das Entwickeln eines Eigenschaftenhandlers umfasst die Implementierung der folgenden Schnittstellen:

-   IInitialzeWithStream: Ermöglicht die streambasierte Initialisierung Ihres Eigenschaftenhandlers.
-   IPropertyStore: Aufzählt, ruft Eigenschaftswerte ab und legt sie fest.
-   IPropertyStoreCapabilities: Optional. Gibt an, ob Benutzer eine Eigenschaft über eine Benutzeroberfläche bearbeiten können.

### <a name="iinitializewithstream"></a>Iinitializewithstream

Wie im Thema [Eigenschaftensystem beschrieben,](../properties/building-property-handlers.md) wird dringend empfohlen, Eigenschaftenhandler mit **IInitializeWithStream** zu implementieren, um die streambasierte Initialisierung zu verwenden. Wenn Sie sich gegen die Implementierung von IInitializeWithStream entschieden haben, muss der Eigenschaftenhandler die Ausführung im Isolationsprozess deaktivieren, indem er das DisableProcessIsolation-Flag für den Registrierungsschlüssel des Eigenschaftenhandlers festlegen. Das Deaktivieren der Prozessisolation ist in der Regel nur für Legacyeigenschaftshandler vorgesehen und sollte durch neuen Code auf jeden Fall vermieden werden.

### <a name="ipropertystore"></a>Ipropertystore

Um einen Eigenschaftenhandler zu erstellen, müssen Sie die [**IPropertyStore-Schnittstelle**](/windows/win32/api/propsys/nn-propsys-ipropertystore) mit den folgenden Methoden implementieren.



| Methode   | Beschreibung                                                         |
|----------|---------------------------------------------------------------------|
| Commit   | Speichert eine Eigenschaftsänderung in der Datei.                                |
| GetAt    | Ruft einen Eigenschaftsschlüssel aus dem Array von Eigenschaften eines Elements ab.        |
| GetCount | Ruft die Anzahl der eigenschaften ab, die an die Datei angefügt sind.                 |
| GetValue | Ruft Daten für eine bestimmte Eigenschaft ab.                             |
| SetValue | Legt einen neuen Eigenschaftswert fest oder ersetzt oder entfernt einen vorhandenen Wert. |



 

 

 

Wichtige Überlegungen zur Implementierung dieser Schnittstelle sind in der [**IPropertyStore-Dokumentation**](/windows/win32/api/propsys/nn-propsys-ipropertystore) enthalten.

> [!Note]  
> Wenn ihr Eigenschaftenhandler mehrere Werte für dieselbe Eigenschaft für ein bestimmtes Element aus gibt, wird nur der zuletzt ausgegebene Wert im Katalog gespeichert.

 

 

### <a name="ipropertystorecapabilities"></a>IPropertyStoreCapabilities

Eigenschaftshandler können diese Schnittstelle optional implementieren, um die Fähigkeit eines Benutzers zu deaktivieren, bestimmte Eigenschaften zu bearbeiten. Diese Eigenschaften können normalerweise auf der Seite Details und im Bereich bearbeitet werden, aber das Bearbeiten ist unter dem implementierenden Eigenschaftenhandler nicht zulässig. Die korrekte Implementierung dieser Schnittstelle bietet eine bessere Benutzererfahrung als die Alternative– einen einfachen Laufzeitfehler von der Shell.

 

## <a name="ensuring-your-items-get-indexed"></a>Sicherstellen, dass Ihre Elemente indiziert werden

Nachdem Sie ihren Eigenschaftenhandler implementiert haben, möchten Sie sicherstellen, dass die Elemente, für die Ihr Handler registriert ist, indiziert werden. Sie können den [Katalog-Manager](-search-3x-wds-mngidx-catalog-manager.md) verwenden, um die erneute [Indizierung](-search-3x-wds-extidx-csm.md) zu initiieren, und Sie können auch den Durchforstungsbereich-Manager zum Einrichten von Standardregeln verwenden, die die URLs angeben, die der Indexer durchforsten soll. Eine weitere Option ist das Befolgen des Codebeispiels ReIndex im Windows [Search SDK Samples](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

Weitere Informationen finden Sie unter [Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md) und [Verwenden des Durchforstungsbereich-Manager](-search-3x-wds-extidx-csm.md).

 

## <a name="installing-and-registering-property-handlers"></a>Installieren und Registrieren von Eigenschaftenhandlern

Wenn der Eigenschaftenhandler implementiert ist, muss er registriert werden, und seine Dateierweiterung muss dem Handler zugeordnet sein. Das folgende Beispiel zeigt die Registrierungsschlüssel und -werte, die dafür erforderlich sind.

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

 

## <a name="testing-and-troubleshooting-property-handlers"></a>Testen und Behandeln von Problemen mit Eigenschaftenhandlern

Die folgende Liste enthält Hinweise zu den Arten von Tests, die Sie ausführen sollten:

-   Testen Sie das Abrufen der Ausgabe jeder einzelnen Eigenschaft, die vom Dateityp unterstützt wird.
-   Verwenden Sie große Eigenschaftswerte, z. B. ein großes Metatag in HTML-Dokumenten.
-   Stellen Sie sicher, dass der Eigenschaftenhandler keine Dateihandles aufweist, indem Sie sie nach dem Abrufen der Ausgabe des Eigenschaftenhandlers bearbeiten oder ein Tool wie oh.exe vor und nach dem Aufzählen von Dateieigenschaften verwenden.
-   Testen Sie alle Dateitypen, die dem Eigenschaftenhandler zugeordnet sind. Überprüfen Sie beispielsweise, ob der HTML-Filter mit .htm und .html funktioniert.
-   Testen Sie mit beschädigten Dateien. Der Eigenschaftenhandler sollte ordnungsgemäß fehlschlagen.
-   Wenn eine Anwendung die Verschlüsselung unterstützt, testen Sie, ob der Eigenschaftenhandler keinen verschlüsselten Text aus gibt.
-   Wenn der Eigenschaftenhandler die Volltextsuche unterstützt:
    -   Verwenden Sie mehrere Unicode-Sonderzeichen im Dateiinhalt, und testen Sie deren Ausgabe.
    -   Testen Sie die Verarbeitung sehr großer Dokumente, um sicherzustellen, dass der Eigenschaftenhandler wie erwartet funktioniert.

### <a name="installation-and-setup-tests"></a>Installations- und Setuptests

Schließlich müssen Sie Ihre Installations- und Deinstallationsroutinen testen.

-   Die Installation muss nach fehlerhaften Installationen wiederhergestellt werden (z. B. nach dem Abbrechen und anschließenden Neustarten des Setups).
-   Bei der Deinstallation müssen alle Dateien gelöscht werden, die dem Eigenschaftenhandler zugeordnet sind.
-   Die Deinstallation darf keine dateien löschen, die nicht der Installation des Eigenschaftenhandlers zugeordnet sind.
-   Registrierungsschlüssel, die dem Eigenschaftenhandler zugeordnet sind, müssen entfernt werden, wenn sie deinstalliert werden.
-   Die Deinstallation muss auch funktionieren, wenn Dateien aus dem Installationsverzeichnis gelöscht werden.

### <a name="troubleshooting-property-handlers"></a>Problembehandlung bei Eigenschaftenhandlern

Im Folgenden sind einige häufige Fehler aufgeführt, die beim Entwickeln von Eigenschaftenhandlern auftreten:

-   Installieren von PROPDESC-Dateien oder DLLs in einem Benutzerverzeichnis.
-   Registrieren von Komponenten mit relativen Pfaden.
-   Registrieren von Komponenten unter HKEY \_ CURRENT USER anstelle von \_ HKEY LOCAL \_ \_ MACHINE.
-   Vergessen Sie, DisableProcessIsolation für Nicht-Streamhandler festzulegen.
-   Platzieren der Testdatei an einem nicht indizierten Speicherort.

Wenn Sie Probleme haben, ihren Eigenschaftenhandler mit dem Indexer zu verwenden, finden Sie hier einige Tipps zur Problembehandlung:

-   Vergewissern Sie sich, dass Ihre Eigenschaftenbeschreibungen (PROPDESC-Dateien) entsprechend mit isColumn="**true**", isViewable="**true**", and isQueryable="**true**" gekennzeichnet sind.
-   Überprüfen Sie, ob sich Ihre PROPDESC-Dateien an einem globalen Speicherort befinden.
-   Vergewissern Sie sich, dass Sie Ihre PROPDESC-Dateien mit absoluten Pfaden registriert haben.
-   Vergewissern Sie sich, dass im Ereignisprotokoll keine Fehler beim Registrieren Ihrer PROPDESC-Datei aufgezeichnet wurden.
-   Vergewissern Sie sich, dass sich Ihre DLLs an einem globalen Speicherort (und nicht unter Ihrem Benutzerprofil) befinden.
-   Überprüfen Sie, ob Ihre DLLs unter HKEY LOCAL MACHINE Software Classes registriert \_ \_ \\ \\ sind.
-   Stellen Sie sicher, dass Ihre DLLs mit vollständigen Pfaden registriert sind (oder REG \_ EXPAND \_ SZ-Zeichenfolgen, die mithilfe von Umgebungsvariablen, die vom Systemkonto bekannt sind, auf absolute Pfade erweitert werden).
-   Vergewissern Sie sich, dass Ihr Eigenschaftenhandler unter Windows Explorer funktioniert.
-   Es wird empfohlen, IInitializeWithStream zu verwenden. Wenn Sie IInitializeWithFile oder IInitializeWithItem verwenden müssen, überprüfen Sie, ob Sie DisableProcessIsolation angeben.
-   Vergewissern Sie sich, dass der Dateityp im Systemsteuerung Indizierungsoptionen als indizierter Dateityp aufgeführt ist.
-   Überprüfen Sie, ob sich die Testdatei an einem indizierten Speicherort befindet.
-   Vergewissern Sie sich, dass die Testdatei seit der Installation des Eigenschaftenhandlers geändert wurde.

Wenn sich die Testdatei an einem indizierten Speicherort befindet und der Indexer diesen Speicherort bereits durchforstet hat, müssen Sie die Datei auf irgendeine Weise ändern, um eine Neuindizierung der Datei auszulösen.

 

## <a name="using-system-supplied-property-handlers"></a>Verwenden von System-Supplied-Eigenschaftenhandlern

Windows enthält eine Reihe von vom System bereitgestellten Eigenschaftenhandlern, die Sie verwenden können, wenn das Format Ihres Dateityps kompatibel ist. Wenn Sie eine neue Dateierweiterung definieren, die eines dieser Formate verwendet, können Sie die vom System bereitgestellten Handler verwenden, indem Sie den Handlerklassenbezeichner (CLSID) für Ihre Dateierweiterung registrieren.

Sie können die in der folgenden Tabelle aufgeführte CLSID verwenden, um die vom System bereitgestellten Eigenschaftenhandler für Ihren Dateiformattyp zu registrieren.



| Format          | CLSID                                  |
|-----------------|----------------------------------------|
| OLE DocFile     | {8d80504a-0826-40c5-97e1-ebc68f953792} |
| Speichern von Spiel-XML   | {ECDD6472-2B9B-4b4b-AE36-F316DF3C8D60} |
| XPS/OPC-Handler | {45670FA8-ED97-4F44-BC93-305082590BFB} |
| XML             | {c73f6f30-97a0-4ad1-a08f-540d4e9bc7b9} |



 

Bevor Sie eine benutzerdefinierte Eigenschaft erstellen, sollten Sie sicherstellen, dass es keine systemdefinierte Eigenschaft gibt, die Sie stattdessen verwenden können. Sie können die systemdefinierte Eigenschaften aufzählen, indem Sie [**PSEnumeratePropertyDescriptions**](/windows/win32/api/propsys/nf-propsys-psenumeratepropertydescriptions) aufrufen oder das befehlszeilentool prop.exe verwenden.

Das Systemschema definiert, wie diese Eigenschaften mit dem Indexer interagieren, und Sie können dies nicht ändern. Darüber hinaus muss die Anwendung, die Sie zum Erstellen, Bearbeiten und Speichern Ihres Dateityps verwenden, auch bestimmtem Verhalten entsprechen. Wenn die Anwendung beispielsweise sicheres Speichern implementiert (wobei während der Bearbeitung eine temporäre Datei erstellt und dann ReplaceFile() verwendet wird, um die neue Version gegen die alte zu tauschen, muss sie alle Eigenschaften aus der ursprünglichen Datei in die neue Datei übertragen. Wenn dies nicht der Fall ist, verliert die Datei die Eigenschaften, die von Benutzern oder anderen Anwendungen hinzugefügt wurden.

 

**Beispiel**

Das folgende Beispiel zeigt die Registrierung des vom System bereitgestellten OLE DocFile-Handlers für einen Dateityp mit einem . OLEDocFile-Erweiterung.

```
HKEY_CLASSES_ROOT
   SystemFileAssociations
      .OLEDocFile
         shellex
            {BB2E617C-0920-11d1-9A0B-00C04FC2D6C1}
               (Default) = {9DBD2C50-62AD-11d0-B806-00C04FD706EC}
```

Das folgende Beispiel zeigt die Registrierung der Eigenschaftenlisteninformationen, sodass eigenschaften von sind. OLEDocFile-Dateien werden auf der Registerkarte Details und im Bereich angezeigt.

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

[Eigenschaftenzuordnungen](-search-3x-wds-propertymappings.md)
</dt> <dt>

**Konzeptionellen**
</dt> <dt>

[Bewährte Methoden zum Erstellen von Filterhandlern in Windows Suche](-search-3x-wds-extidx-filters.md)
</dt> <dt>

[Der Indizierungsprozess](-search-indexing-process-overview.md)
</dt> <dt>

[Entwickeln von Protokollhandlern](-search-3x-wds-phaddins.md)
</dt> <dt>

[Systemdefinierte Eigenschaften für benutzerdefinierte Dateiformate](-shell-systemdefinedpropertiesforfileformats.md)
</dt> <dt>

**Andere Ressourcen**
</dt> <dt>

[Eigenschaftensystem](../properties/building-property-handlers.md)
</dt> <dt>

[Systemeigenschaften](https://msdn.microsoft.com/library/bb763010(VS.85).aspx)
</dt> <dt>

[Windows Suchen von SDK-Beispielen](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8)
</dt> </dl>

 

 
