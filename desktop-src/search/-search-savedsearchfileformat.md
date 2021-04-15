---
description: Windows-Benutzer können Suchvorgänge als Suchordner speichern, der von einer XML-Datei generiert wird, die die Abfrage in einer Form speichert, die vom Windows Search-Subsystem verwendet werden kann.
ms.assetid: 1c73e220-a999-4243-879c-ac7310151def
title: Format der gespeicherten Such Datei
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d19cf936f78b045814bf7cba31a123c40d61927a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525496"
---
# <a name="saved-search-file-format"></a>Format der gespeicherten Such Datei

In Windows Vista und höher können Benutzer Suchvorgänge als Suchordner speichern, der von einer XML-Datei generiert wird, in der die Abfrage in einer Form gespeichert wird, die vom Windows Search-Subsystem verwendet werden kann. Dieses Thema beschreibt das Dateiformat ( \* . Search-MS) und umfasst die folgenden Abschnitte:

- [Übersicht über gespeicherte Suchvorgänge](#overview-of-saved-searches)
- [\<viewInfo>-Element](/windows)
  - [\<viewInfo> Legt](/windows)
  - [\<viewInfo> Untergeordnete Elemente](/windows)
- [\<query>-Element](/windows)
  - [\<query> Untergeordnete Elemente](/windows)
- [\<properties>-Element](/windows)
- [Vollständige Spezifikation des Search-MS-Datei Formats](#full-specification-of-the-search-ms-file-format)
- [Beispiele für gespeicherte Suchvorgänge](#examples-of-saved-searches)

## <a name="overview-of-saved-searches"></a>Übersicht über gespeicherte Suchvorgänge

Benutzer können eine Suchabfrage als Suchordner speichern, ein virtueller Ordner, der im Windows-Explorer unter dem Ordner "Suchvorgänge" angezeigt wird. Beim Öffnen eines Such Ordners wird die gespeicherte Suche ausgeführt, und es werden aktuelle Ergebnisse angezeigt. In der gespeicherten Suchdatei wird die Abfrage in einem Format gespeichert, auf das Windows-Suche reagieren kann. dabei wird angegeben, was gesucht werden soll, wo gesucht werden soll und wie die Ergebnisse angezeigt werden.

Die gespeicherte Suche wird aus einer XML-Datei ( \* . Search-MS) im Ordner "% User Profile% Such" generiert \\ . Die Daten sind in drei primäre Elemente in der XML-Datei unterteilt:

- \<viewInfo> gibt Präsentationsinformationen an.
- \<query> gibt (Suchabfrage Informationen an)
- \<properties> gibt Eigenschaften der \* . Search-MS-Datei an.

Das folgende Beispiel zeigt die Struktur einer gespeicherten Suchdatei auf hoher Ebene.

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">

    <viewInfo ...>
        ...
    </viewInfo>

    <query>
        ...
    </query>

    <properties>
        ...
    </properties>

</persistedQuery>
```

## <a name="viewinfo-element"></a>\<viewInfo>-Element

Das- \<viewInfo> Element gibt an, wie die Ergebnisse für den Endbenutzer angezeigt werden. Das folgende Beispiel zeigt die Struktur des-Elements.

```XML
...
    <viewInfo viewMode=""
              iconSize=""
              stackIconSize=""
              autoListFlags=""
              folderFlags=""
              taskFlags=""
              displayName="">

        <visibleColumns>
            <column viewField=""/>
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/>
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>
        </columnChooserColumns >

        <groupBy viewField=""
                 direction=""/>

        <stackList>
            <stack viewField=""/>
        </stackList>

        <sortList>
            <sort viewField=""
                  direction=""/>
        </sortList>
    </viewInfo>
...
```

### <a name="viewinfo-attributes"></a>\<viewInfo> Legt

In der folgenden Tabelle werden die Attribute des Elements \<viewInfo> beschrieben.

| Attribut     | BESCHREIBUNG                                                                     | Werte                     |
|---------------|---------------------------------------------------------------------------------|----------------------------|
| viewMode      | Gibt die Ordneransicht an.                                                      | Kachel "Detail \| Symbole" \|  |
| iconSize      | Steuert die Standardgröße der Symbole und Miniaturansichten für Elemente, wenn Sie nicht als Stapel angezeigt werden. | Ganzzahl zwischen 16 und 256 |
| stackiconsize | Nur zur internen Verwendung. Darf nicht verwendet werden.                                              | –                        |
| displayName   | Nur zur internen Verwendung. Darf nicht verwendet werden.                                              | –                        |
| autolistflags | Nur zur internen Verwendung. Darf nicht verwendet werden.                                              | –                        |
| FolderFlags   | Nur zur internen Verwendung. Darf nicht verwendet werden.                                              | –                        |
| taskflags     | Nur zur internen Verwendung. Darf nicht verwendet werden.                                              | –                        |

### <a name="viewinfo-child-elements"></a>\<viewInfo> Untergeordnete Elemente

Die untergeordneten Elemente des- \<viewInfo> Elements geben an, welche Spalten in den Windows Explorer-Suchergebnissen angezeigt werden und wie die Ergebnisse gruppiert und sortiert werden. Jedes untergeordnete Element enthält eine geordnete Gruppe von Spalten, die durch kanonische Namen der Systemeigenschaften (z. b. System. Display Name) identifiziert wird. Wenn Sie nicht in der gespeicherten Suchdatei definiert sind, werden die Suchergebnisse mit einem Standardsatz von Spalten angezeigt, die für die angezeigten Dateitypen geeignet sind.

| Element               | BESCHREIBUNG                                                                                        | Werte                                                       |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| visiblecolumns        | Gibt eine geordnete Liste von Spalten an, die in der Ergebnis Ansicht angezeigt werden sollen. Der Benutzer kann diese Liste ändern. | Eine beliebige System Eigenschaft.                                         |
| frequentlyusedcolumns | Nur zur internen Verwendung. Darf nicht verwendet werden.                                                                 | –                                                          |
| columnchoosercolumns  | Nur zur internen Verwendung. Darf nicht verwendet werden.                                                                 | –                                                          |
| GroupBy               | Gibt eine einzelne System Eigenschaft an, nach der die Ergebnisse gruppiert werden sollen. Der Benutzer kann diesen Wert ändern.  | Eine beliebige System Eigenschaft.                                         |
| SortList              | Gibt eine geordnete Liste von Spalten an, nach denen die Ergebnisse sortiert werden sollen.                                       | Bis zu vier Systemeigenschaften. Der Benutzer kann diese Liste ändern. |
| Stacklist             | Nur zur internen Verwendung. Darf nicht verwendet werden.                                                                 | –                                                          |

## <a name="query-element"></a>\<query>-Element

Das- \<query> Element gibt die Attribute an, die definieren, wie die Ergebnisse abgefragt werden. Das folgende Beispiel zeigt die Struktur des-Elements.

```XML
...
    <query>
        <providers>
            <provider clsid=""/>    <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

### <a name="query-child-elements"></a>\<query> Untergeordnete Elemente

Die folgende Tabelle beschreibt die untergeordneten Elemente des \<scope>-Elements.

| Element    | BESCHREIBUNG                                                                                                               | Wert                                                                                                                                                                                                                                                          |
|------------|---------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| providers  | Nur zur internen Verwendung. Darf nicht verwendet werden.                                                                                        | –                                                                                                                                                                                                                                                            |
| Unterabfragen | Nur zur internen Verwendung. Darf nicht verwendet werden.                                                                                        | –                                                                                                                                                                                                                                                            |
| Bereich      | Identifiziert Standorte, die in die Suche eingeschlossen oder ausgeschlossen werden sollen.                                                                 | Entweder ein Pfad oder eine [bekannte Ordner-ID](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) des Speicher Orts, der eingeschlossen oder ausgeschlossen werden soll. Dieses Element kann auch angeben, ob die Suche untergeordnete Pfade einschließen/ausschließen soll (eine flache oder eine Tiefe Suche). |
| kindlist   | Gibt die Art der Datei (en) an, nach der gesucht werden soll.                                                                             | Ein beliebiger System. Kind-Wert.                                                                                                                                                                                                                                         |
| Bedingungen | Gibt Regeln zum Filtern von Ergebnissen an. Beispielsweise können die Ergebnisse auf e-Mails beschränkt werden, die von oder an eine bestimmte Person gesendet werden. | AndCondition, OrCondition, NotCondition, leafcondition.                                                                                                                                                                                                        |

### <a name="scope-element"></a>\<scope>-Element

Das- \<scope> Element identifiziert die Orte, die von der Suche eingeschlossen oder ausgeschlossen werden sollen. Das \<scope> -Element muss mindestens ein untergeordnetes \<include> Element enthalten und kein oder mehrere- \<exclude> Elemente. Die Speicherorte können entweder als Pfad (Umgebungsvariablen werden unterstützt) oder als [bekannter Ordner Bezeichner](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid)angegeben werden. Außerdem kann angegeben werden, dass jeder dieser Speicherorte tief oder flach durchsucht werden soll, indem die nicht rekursive Einstellung auf "true" oder "false" festgelegt wird (der Standardwert ist rekursiv). Teile der enthaltenen Speicherorte können ausgeschlossen werden, indem Ausschluss Elemente angegeben werden.

Das folgende Beispiel zeigt ein \<scope> -Element, das den Ordner "Dokumente", aber nicht seine untergeordneten Elemente durchsucht, das Volume "e:" und seine untergeordneten Elemente, aber nicht das Verzeichnis "e: \\ Windows" oder eines seiner untergeordneten Elemente:

```XML
...
    <query>
        ...
        <scope>
            <include knownFolder="{FDD39AD0-238F-46AF-ADB4-6C85480369C7}" nonRecursive="true"/>
            <include path="E:\"/>
            <exclude path="E:\Windows" nonRecursive="false"/>
        </scope>
        ...
    </query>
...
```

### <a name="kindlist-element"></a>\<kindList>-Element

Diese Elemente definieren die Vereinigung der "Art" von Elementen, die in der Bibliothek angezeigt werden sollen. Gültige Werte sind:

- Kalender
- communication
- contact
- Dokument
- email
- feed
- folder
- Modi
- sofortige Nachricht
- Nacht
- link
- Saal
- music
- Hinweis:
- picture
- Programm
- recordebug
- SearchFolder
- task
- video
- webhistory
- item
- andere

### <a name="conditions-element"></a>\<conditions>-Element

Bedingungen sind Filter, mit denen die Suchergebnisse verglichen werden. Beispielsweise können Sie Ergebnisse filtern, die bestimmte Kriterien erfüllen, wie z. b. den Namen des Autors oder der Dateigröße. Der Satz von Bedingungen wird in eine einzelne Bedingungs Struktur mit logischen and-, or-und Not branches integriert.

Das folgende Beispiel zeigt die Struktur des- \<condition> Elements.

```XML
...
    <query>
        ...
        <conditions>
            <condition type="" ...>
                <attributes>
                    <attribute attributeID="" .../>
                </attributes>
            </condition>
        </conditions>
    </query>
...
```

Der Bedingungstyp kann eine der folgenden sein:

| type          | BESCHREIBUNG                                 | Verfügbare Attribute                               |
|---------------|---------------------------------------------|----------------------------------------------------|
| andCondition  | Verbindung von mindestens zwei untergeordneten Bedingungen | –                                                |
| OrCondition   | Disjunktion von zwei untergeordneten Bedingungen | –                                                |
| NotCondition  | Negation einer untergeordneten Bedingung               | –                                                |
| leafcondition | Vergleicht eine Eigenschaft mit einem Wert.                | Property, PropertyType, Operator, Value, ValueType |

Die \<leafCondition> Attribute des Elements geben die Eigenschaften und Werte an, anhand derer die Ergebnisse gefiltert werden.

### <a name="example-conditions-element"></a>Beispiel: \<conditions> Element

Im folgenden Beispiel werden die Ergebnisse für alle von John erstellten ungelesenen Elemente gefiltert. Das heißt, die System. isread-Eigenschaft ist false, und die Zeichenfolge "John" wird in den Eigenschaften System. Author oder System. itemauthors angezeigt.

```XML
...
    <query>
        ...
        <conditions>

            <condition type="andCondition">

                <condition type="leafCondition"
                           property="System.IsRead"
                           operator="eq"
                           value="FALSE"/>

                <condition type="orCondition">

                    <condition type="leafCondition"
                               property="System.Author"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                    <condition type="leafCondition"
                               property="System.ItemAuthors"
                               propertyType="string"
                               operator="wordmatch"
                               value="John"
                               valueType="System.StructuredQueryType.String"/>

                </condition>

            </condition>

        </conditions>

    </query>
...
```

## <a name="properties-element"></a>\<properties>-Element

Das- \<properties> Element beschreibt die Eigenschaften der gespeicherten Suche selbst. Gespeicherte Suchdateien unterstützen vier Eigenschaften: \<author> , \<kind> , \<description> und \<tags> . Diese sind nur für die interne Verwendung vorgesehen.

## <a name="full-specification-of-the-search-ms-file-format"></a>Vollständige Spezifikation des Search-MS-Datei Formats

Im folgenden finden Sie ein Beispiel für den vollständigen XML-Code einer gespeicherten Suchdatei.

```XML
<?xml version="1.0"?>

<persistedQuery version="1.0">

    <!-- The viewInfo section defines how results are displayed to the end user -->
    <viewInfo viewMode=""       <!-- details | icons | tiles -->
              iconSize=""       <!-- Integer -->
              stackIconSize=""  <!-- Do not use -->
              displayName=""    <!-- Do not use -->
              folderFlags=""    <!-- Do not use -->
              taskFlags=""      <!-- Do not use -->
              autoListFlags=""> <!-- Do not use -->

        <visibleColumns>
            <column viewField=""/>  <!-- System.[propertyname] -->
        </visibleColumns>

        <frequentlyUsedColumns>
            <column viewField= ""/> <!-- Do not use -->
        </frequentlyUsedColumns>

        <columnChooserColumns >
            <column viewField=""/>  <!-- Do not use -->
        </columnChooserColumns >

        <groupBy viewField=""       <!-- System.[propertyname] -->
                 direction=""/>     <!-- ascending | descending -->

        <stackList>
            <stack viewField=""/>   <!-- Do not use -->
        </stackList>

        <sortList>
            <sort viewField=""      <!-- System.[propertyname] -->
                  direction=""/>    <!-- ascending | descending -->
        </sortList>
    </viewInfo>

    <!-- The query section defines what gets searched (locations, file kinds) -->
    <query>
        <providers>
            <provider clsid=""/>          <!-- Do not use -->
        </providers>

        <subQueries>
            <subQuery path=""/>           <!-- Do not use -->
            <subQuery knownSearch=""/>    <!-- Do not use -->
        </subQueries>

        <scope>
            <include path=""        nonRecursive=""/>   <!-- [path of location to include] -->
            <include knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
            <exclude path=""        nonRecursive=""/>   <!-- [path of location to exclude] -->
            <exclude knownFolder="" nonRecursive=""/>   <!-- Known folder ID  -->
        </scope>

        <kindList>
            <kind name=""/>     <!-- Kind value -->
        </kindList>

        <conditions>
            <condition type="" ...>     <!-- andCondition | orCondition | notCondition | leafCondition -->
                <attributes>
                    <attribute attributeID="" .../> <!-- Do not use -->
                </attributes>
            </condition>
        </conditions>
    </query>

    <!-- The properties section identifies properties of the saved search file itself. -->
    <properties>
        ...             <!-- Do not use -->
    </properties>

</persistedQuery>
```

## <a name="examples-of-saved-searches"></a>Beispiele für gespeicherte Suchvorgänge

Im folgenden finden Sie Beispiele für \* . Search-MS-Dateien.

### <a name="recent-documentssearch-ms"></a>Zuletzt verwendete Dokumente. Search-MS

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUZZXD-30NU" propertyType="wstr" />
        </conditions>
        <kindList>
            <kind name="Document"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recent-musicsearch-ms"></a>Neueste Musik. Search-MS

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <sortList>
            <sort viewField="System.DateModified" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="leafCondition" valuetype="System.StructuredQueryType.DateTime" property="System.DateModified" operator="imp" value="R00UUUUUUUUW-1WNNU" propertyType="wstr"/>
        </conditions>
        <kindList>
            <kind name="Music"/>
        </kindList>
        <subQueries>
            <subQuery knownSearch="{4f800859-0bd6-4e63-bbdc-38d3b616ca48}"/>
        </subQueries>
    </query>
</persistedQuery>
```

### <a name="recently-shared-by-mesearch-ms"></a>Vor kurzem von mir freigegeben. Suchen Sie nach MS

```XML
<?xml version="1.0"?>
<persistedQuery version="1.0">
    <viewInfo viewMode="details" iconSize="16">
        <visibleColumns>
            <column viewField="System.ItemNameDisplay"/>
            <column viewField="System.DateModified"/>
            <column viewField="System.Keywords"/>
            <column viewField="System.SharedWith"/>
            <column viewField="System.ItemFolderPathDisplayNarrow"/>
        </visibleColumns>
        <frequentlyUsedColumns>
            <column viewField="System.Author"/>
            <column viewField="System.Kind"/>
            <column viewField="System.Size"/>
            <column viewField="System.Title"/>
            <column viewField="System.Rating"/>
        </frequentlyUsedColumns>
        <sortList>
            <sort viewField="System.SharedWith" direction="descending"/>
        </sortList>
    </viewInfo>

    <query>
        <conditions>
            <condition type="andCondition">
                <condition type="leafCondition" property="System.IsShared" operator="eq" value="true"/>
                <condition type="leafCondition" property="System.FileOwner" operator="eq" value="[Me]"/>
            </condition>
        </conditions>
        <kindList>
            <kind name="item"/>
        </kindList>
        <scope>
            <include knownFolder="{5E6C858F-0E22-4760-9AFE-EA3317B67173}"/>
            <include knownFolder="{DFDF76A2-C82A-4D63-906A-5644AC457385}"/>
        </scope>
    </query>
</persistedQuery>
```
