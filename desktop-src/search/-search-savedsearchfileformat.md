---
description: Windows Können Suchvorgänge als Suchordner speichern, der von einer XML-Datei generiert wird, in der die Abfrage in einem Formular gespeichert wird, das vom Windows verwendet werden kann.
ms.assetid: 1c73e220-a999-4243-879c-ac7310151def
title: Gespeichertes Suchdateiformat
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 614eb357a82d2c70e068a9fa5258974423d755c48e779d5f5fe8be184a864d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117863723"
---
# <a name="saved-search-file-format"></a>Gespeichertes Suchdateiformat

In Windows Vista und höher können Benutzer Suchvorgänge als Suchordner speichern, der von einer XML-Datei generiert wird, die die Abfrage in einem Formular speichert, das vom Windows verwendet werden kann. Dieses Thema beschreibt das Dateiformat ( \* .search-ms) und enthält die folgenden Abschnitte:

- [Übersicht über gespeicherte Suchvorgänge](#overview-of-saved-searches)
- [\<viewInfo>-Element](/windows)
  - [\<viewInfo> Attribute](/windows)
  - [\<viewInfo> Untergeordnete Elemente](/windows)
- [\<query>-Element](/windows)
  - [\<query> Untergeordnete Elemente](/windows)
- [\<properties>-Element](/windows)
- [Vollständige Spezifikation des Dateiformats search-ms](#full-specification-of-the-search-ms-file-format)
- [Beispiele für gespeicherte Suchvorgänge](#examples-of-saved-searches)

## <a name="overview-of-saved-searches"></a>Übersicht über gespeicherte Suchvorgänge

Benutzer können eine Suchabfrage als Suchordner speichern, einen virtuellen Ordner, der im Windows Explorer unter dem Ordner Suchen angezeigt wird. Beim Öffnen eines Suchordners wird die gespeicherte Suche ausgeführt und aktuelle Ergebnisse angezeigt. In der gespeicherten Suchdatei wird die Abfrage in einem Format gespeichert, Windows die Suche ausgeführt werden kann. Dabei wird angegeben, nach was gesucht werden soll, wo gesucht werden soll und wie die Ergebnisse präsentiert werden.

Die gespeicherte Suche wird aus einer \* XML-Datei ( .search-ms) im Ordner %userprofile% \\ Searches generiert. Die Daten sind in drei primäre Elemente in der XML-Datei unterteilt:

- \<viewInfo> gibt Präsentationsinformationen an
- \<query> gibt an (Suchabfrageinformationen)
- \<properties> gibt die Eigenschaften der \* .search-ms-Datei selbst an.

Das folgende Beispiel zeigt die obere Struktur einer gespeicherten Suchdatei.

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

Das \<viewInfo> -Element gibt an, wie die Ergebnisse dem Endbenutzer angezeigt werden. Das folgende Beispiel zeigt die Struktur des -Elements.

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

### <a name="viewinfo-attributes"></a>\<viewInfo> Attribute

In der folgenden Tabelle werden die Attribute des Elements \<viewInfo> beschrieben.

| attribute     | BESCHREIBUNG                                                                     | Werte                     |
|---------------|---------------------------------------------------------------------------------|----------------------------|
| Viewmode      | Gibt die Ordneransicht an.                                                      | \| \| Detailsymbolkacheln  |
| iconSize      | Steuert die Standardgröße der Symbole und Miniaturansichten für Elemente, wenn sie nicht gestapelt sind. | Ganze Zahl zwischen 16 und 256 |
| stackIconSize | Nur zur internen Verwendung. Darf nicht verwendet werden.                                              | –                        |
| displayName   | Nur zur internen Verwendung. Darf nicht verwendet werden.                                              | –                        |
| autoListFlags | Nur zur internen Verwendung. Darf nicht verwendet werden.                                              | –                        |
| folderFlags   | Nur zur internen Verwendung. Darf nicht verwendet werden.                                              | –                        |
| taskFlags     | Nur zur internen Verwendung. Darf nicht verwendet werden.                                              | –                        |

### <a name="viewinfo-child-elements"></a>\<viewInfo> Untergeordnete Elemente

Die untergeordneten Elemente des -Elements geben an, welche Spalten in den Suchergebnissen des Windows Explorers angezeigt werden und wie die Ergebnisse \<viewInfo> gruppiert und sortiert werden. Jedes untergeordnete Element enthält eine geordnete Gruppe von Spalten, die durch kanonische Namen von Systemeigenschaften (z. B. System.DisplayName) identifiziert werden. Wenn dies nicht in der gespeicherten Suchdatei definiert ist, wird den Suchergebnissen ein Standardsatz von Spalten angezeigt, die für die angezeigten Dateitypen geeignet sind.

| Element               | BESCHREIBUNG                                                                                        | Werte                                                       |
|-----------------------|----------------------------------------------------------------------------------------------------|--------------------------------------------------------------|
| visibleColumns        | Gibt eine geordnete Liste von Spalten an, die in der Ergebnisansicht angezeigt werden sollen. Der Benutzer kann diese Liste ändern. | Eine beliebige Systemeigenschaft.                                         |
| frequentlyUsedColumns | Nur zur internen Verwendung. Darf nicht verwendet werden.                                                                 | –                                                          |
| columnChooserColumns  | Nur zur internen Verwendung. Darf nicht verwendet werden.                                                                 | –                                                          |
| Groupby               | Gibt eine einzelne Systemeigenschaft an, nach der die Ergebnisse gruppiert werden. Der Benutzer kann diesen Wert ändern.  | Eine beliebige Systemeigenschaft.                                         |
| Sortlist              | Gibt eine sortierte Liste von Spalten an, nach der die Ergebnisse sortiert werden sollen.                                       | Bis zu vier Systemeigenschaften. Der Benutzer kann diese Liste ändern. |
| stackList             | Nur zur internen Verwendung. Darf nicht verwendet werden.                                                                 | –                                                          |

## <a name="query-element"></a>\<query>-Element

Das \<query> -Element gibt die Attribute an, die definieren, wie die Ergebnisse abgefragt werden. Das folgende Beispiel zeigt die Struktur des -Elements.

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
| Bereich      | Identifiziert Orte, die in die Suche ein- oder ausgeschlossen werden.                                                                 | Entweder ein Pfad oder eine [bekannte Ordner-ID](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) des ein- oder auszuschließenden Speicherorts. Dieses Element kann auch angeben, ob die Suche untergeordnete Pfade (flache oder tiefe Suche) ein- bzw. ausschließen soll. |
| kindList   | Gibt die Art der zu suchden Dateien an.                                                                             | Ein beliebiger System.Kind-Wert.                                                                                                                                                                                                                                         |
| Bedingungen | Gibt Regeln zum Filtern von Ergebnissen an. Die Ergebnisse können beispielsweise auf E-Mails beschränkt werden, die von oder an eine bestimmte Person gesendet werden. | andCondition, orCondition, notCondition, leafCondition.                                                                                                                                                                                                        |

### <a name="scope-element"></a>\<scope>-Element

Das \<scope> -Element identifiziert die Orte, die in die Suche ein- oder ausgeschlossen werden. Das \<scope> Element muss mindestens ein untergeordnetes Element und null oder mehr Elemente \<include> \<exclude> enthalten. Die Speicherorte können entweder als Pfad (Umgebungsvariablen werden unterstützt) oder als bekannter [Ordnerbezeichner angegeben werden.](/windows/win32/api/shobjidl_core/nf-shobjidl_core-iknownfolder-getid) Darüber hinaus kann jeder dieser Orte so angegeben werden, dass er tief oder flach durchsucht wird, indem "nonRecursive" auf "true" oder "false" festgelegt wird (der Standardwert ist rekursiv). Teile der eingeschlossenen Liste von Speicherorten können ausgeschlossen werden, indem Exclude-Elemente angegeben werden.

Das folgende Element zeigt ein -Element, das den speziellen Ordner der Dokumente durchsucht, jedoch nicht seine unteren Elemente, das Volume "E:" und seine unteren Elemente, aber nicht das Verzeichnis "E: windows" oder eines seiner unteren \<scope> \\ Elemente:

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
- Spiel
- instantmessage
- Journal
- link
- Film
- music
- Hinweis:
- picture
- Programm
- recordedtv
- searchfolder
- task
- video
- webhistory
- item
- Sonstige

### <a name="conditions-element"></a>\<conditions>-Element

Bedingungen sind Filter, mit denen Suchergebnisse verglichen werden. Beispielsweise können Sie Ergebnisse filtern, die bestimmte Kriterien erfüllen, z. B. Den Namen des Autors oder die Dateigröße. Der Satz von Bedingungen ist in eine einzelne Bedingungsstruktur mit logischen VERZWEIGUNGEN UND, OR und NOT integriert.

Das folgende Beispiel zeigt die Struktur des \<condition> -Elements.

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

Der Bedingungstyp kann einer der folgenden sein:

| type          | BESCHREIBUNG                                 | Verfügbare Attribute                               |
|---------------|---------------------------------------------|----------------------------------------------------|
| Andcondition  | Konjunktion von zwei oder mehr untergeordneten Bedingungen | –                                                |
| Orcondition   | Disjunktion von zwei von mehr untergeordneten Bedingungen | –                                                |
| Notcondition  | Negation einer untergeordneten Bedingung               | –                                                |
| leafCondition | Vergleicht eine Eigenschaft mit dem Wert                | property, propertyType, operator, value, valuetype |

Die \<leafCondition> Attribute des Elements identifizieren die Eigenschaften und Werte, nach deren Filterung die Ergebnisse gefiltert werden.

### <a name="example-conditions-element"></a>Beispiel: \<conditions> Element

Im folgenden Beispiel werden die Ergebnisse für alle ungelesenen Elemente, die von John verfasst wurden, filtert. Das heißt, die System.IsRead-Eigenschaft ist false, und die Zeichenfolge "john" wird in den Eigenschaften System.Author oder System.ItemAuthors angezeigt.

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

Das \<properties> -Element beschreibt die Eigenschaften der gespeicherten Suche selbst. Gespeicherte Suchdateien unterstützen vier Eigenschaften: \<author> \<kind> , , und \<description> \<tags> . Diese sind nur für die interne Verwendung.

## <a name="full-specification-of-the-search-ms-file-format"></a>Vollständige Spezifikation des Dateiformats search-ms

Im Folgenden finden Sie ein Beispiel für den vollständigen XML-Code für eine gespeicherte Suchdatei.

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

Im Folgenden finden Sie Beispiele für \* SEARCH-MS-Dateien.

### <a name="recent-documentssearch-ms"></a>Recent Documents.search-ms

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

### <a name="recent-musicsearch-ms"></a>Zuletzt Musik.search-ms

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

### <a name="recently-shared-by-mesearch-ms"></a>Kürzlich von Me.search-ms freigegeben

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
