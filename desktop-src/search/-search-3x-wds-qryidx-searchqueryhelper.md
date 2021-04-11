---
description: 'Sie können die isearchqueryhelper-Schnittstelle verwenden, um den Index abzufragen. Diese Schnittstelle wird als Hilfsklasse in isearchcatalogmanager (und ISearchCatalogManager2) implementiert und durch Aufrufen von isearchcatalogmanager:: getqueryhelper abgerufen.'
ms.assetid: 6e567c09-8763-4866-bf02-ad6651b454db
title: Abfragen des Indexes mit isearchqueryhelper
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 56b9d970a1e3f416081d3b7fd3e9d6c2af0a2bca
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214463"
---
# <a name="querying-the-index-with-isearchqueryhelper"></a>Abfragen des Indexes mit isearchqueryhelper

Sie können die [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle verwenden, um den Index abzufragen. Diese Schnittstelle wird als Hilfsklasse in [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) (und [**ISearchCatalogManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager2)) implementiert und durch Aufrufen von [**isearchcatalogmanager:: getqueryhelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)abgerufen. Diese Schnittstelle ermöglicht Folgendes:

-   Rufen Sie eine OLE DB Verbindungs Zeichenfolge für die Verbindung mit der Windows Search-Datenbank ab.
-   Konvertieren von Benutzer Abfragen der erweiterten Abfrage Syntax (AQS) in Windows Search Structured Query Language (SQL).
-   Geben Sie Abfrage Einschränkungen an, die in SQL ausgedrückt werden können, aber nicht in AQS.

Dieses Thema ist wie folgt organisiert:

-   [Ersten Einstieg in isearchqueryhelper](#getting-started-with-isearchqueryhelper)
-   [Verwenden der generatesqlfromuserquery-Methode](#using-the-generatesqlfromuserquery-method)
-   [Arbeiten mit Gebiets Schema Bezeichnerzeichen](#working-with-locale-identifiers)
-   [Arbeiten mit Eigenschaften und Spalten](#working-with-properties-and-columns)
-   [Arbeiten mit der Abfrage Begriffs Erweiterung](#working-with-query-term-expansion)
-   [Arbeiten mit anderen isearchqueryhelper-Methoden](#working-with-other-isearchqueryhelper-methods)
-   [Zugehörige Themen](#related-topics)

## <a name="getting-started-with-isearchqueryhelper"></a>Ersten Einstieg in isearchqueryhelper

Es gibt einige wichtige Schnittstellen und Methoden, die Sie kennen sollten, bevor Sie mit der [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle Programm gesteuert mit der Windows-Suche beginnen können. Auf hoher Ebene müssen Sie die folgenden Schritte ausführen:

1.  Instanziieren Sie eine [**isearchmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchmanager) -Instanz.
    ```
    // Create ISearchManager instance
    ISearchManager* pSearchManager;

    // Use library SearchSDK.lib for CLSID_CSearchManager.
    hr = CoCreateInstance(CLSID_CSearchManager, NULL, CLSCTX_LOCAL_SERVER, IID_PPV_ARGS(&pSearchManager));      
    ```

    

2.  Rufen Sie mithilfe von [**isearchmanager:: getCatalog**](/windows/desktop/api/Searchapi/nf-searchapi-isearchmanager-getcatalog)eine Instanz von [**isearchcatalogmanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcatalogmanager) ab. Der Name des System Katalogs für Windows Search lautet `SYSTEMINDEX` .
    ```
    // Create ISearchCatalogManager instance 
    ISearchCatalogManager* pSearchCatalogManager;

    // Call ISearchManager::GetCatalog for "SystemIndex" to access the catalog to the ISearchCatalogManager
    hr = pSearchManager->GetCatalog(L"SystemIndex", &pSearchCatalogManager);
            
    ```

    

3.  Rufen Sie eine Instanz von [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) mithilfe von [**isearchcatalogmanager:: getqueryhelper**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcatalogmanager-getqueryhelper)ab.
    ```
    // Call ISearchCatalogManager::GetQueryHelper to get the ISearchQueryHelper interface
    ISearchQueryHelper* pQueryHelper;

    hr = pSearchCatalogManager->GetQueryHelper(&pQueryHelper);
            
    ```

    

4.  Nachdem Sie über eine Instanz von [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper)verfügen, können Sie die Verbindungs Zeichenfolge abrufen, die zum Herstellen einer Verbindung mit dem Windows Search-Index OLE DB-Connector verwendet wird.
    ```
    // Call get_ConnectionString to get the OLE DB connection string
    LPWSTR pszConnectionString=NULL;

    hr = pQueryHelper->get_ConnectionString(&pszConnectionString);
    // NOTE: YOU MUST call CoTaskMemFree() on the string
        
    ```

    

## <a name="using-the-generatesqlfromuserquery-method"></a>Verwenden der generatesqlfromuserquery-Methode

Die [**isearchqueryhelper:: generatesqlfromuserquery**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-generatesqlfromuserquery) -Methode wandelt Benutzereingaben in eine SQL-Abfrage Zeichenfolge um, die dann an den OLE DB-Anbieter für Windows Search übermittelt werden kann. Diese Methode übersetzt die vom Benutzer eingegebene [Erweiterte Abfrage Syntax](-search-3x-advancedquerysyntax.md) (AQS) oder die NQS-Abfrage (Natural Query Syntax) in SQL und ermöglicht das Hinzufügen anderer SQL-Fragmente nach Bedarf.

Die SQL-Abfrage Zeichenfolge wird im folgenden Format zurückgegeben:


```
SELECT <QuerySelectColumns> 
FROM <CatalogName that created query helper>
WHERE <Result of interpreting the user query passed into this function according to QuerySyntax>
      [ AND|OR <QueryWhereRestrictions> ]
    
```



Es folgt ein Beispiel für die SQL-Zeichenfolge, die vom-Befehl zurückgegeben wird `GenerateSQLFromUserQuery("comput")` :


```
SELECT "System.ItemUrl" 
FROM "SystemIndex" 
WHERE ((CONTAINS(*,'"comput*"',1033) RANK BY COERCION(Absolute, 1)) OR 
       (FREETEXT(("System.ItemNameDisplay":0.9, *:0.1), 'comput', 1033) AND CONTAINS(*,'"comput"',1033)))
ORDER BY "System.ItemUrl"
```



> [!Note]  
> Die-Methode generiert sowohl den fretext-als auch das-Prädikat "enthält", da "enthält allein" keine sinnvolle Rangfolge generiert

 

## <a name="working-with-locale-identifiers"></a>Arbeiten mit Gebiets Schema Bezeichnerzeichen



| Methode                                                                                                                                                                                                                                   | BESCHREIBUNG                                                                                                                                                                                                        |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Isearchqueryhelper:: get \_ querycontentlocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentlocale)/<br/> [**Isearchqueryhelper::p UT \_ querycontentlocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentlocale)<br/> | Ruft den Sprachcode Bezeichner (LCID) der Abfrage ab oder legt ihn fest. Dadurch werden die richtigen Wörter Trennungen und Wort Stamm Erkennung zum Vergleichen von Abfrage Begriffen mit dem Katalog-/invertierten Index unterstützt. Der Standardwert ist das aktuelle Eingabe Gebiets Schema. |
| [**Isearchqueryhelper:: get \_ querykeywordlocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querykeywordlocale)/<br/> [**Isearchqueryhelper::p UT \_ querykeywordlocale**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querykeywordlocale)<br/> | Ruft die LCID für die Sprache ab, die beim Abfragen von AQS-Schlüsselwörtern (Advanced Query Syntax) verwendet werden soll, oder legt Sie fest. Der Standardwert ist das Standard Gebiets Schema des Benutzers.                                                                              |



 

Das **Inhalts** Gebiets Schema und das **Schlüsselwort** Gebiets Schema sind Gebiets Schema Bezeichner (Locale Identifier, LCID), die dem Suchmodul helfen, die richtigen Wörter Trennungen zu verwenden, indem die Sprache der Abfrage Begriffe und die Sprache der AQS-Schlüsselwörter Dabei handelt es sich nicht immer um die gleichen LCIDs, da Windows Search in einer Reihe von internationalen Versionen angeboten wird und auch mehrsprachige Benutzeroberflächen Pakete (MUI) für weitere Sprachen enthalten. Das Content-Gebiets Schema identifiziert die LCID für die Sprache, die Benutzer in die Suchabfrage eingeben, während das Schlüsselwort locale die LCID identifiziert, die die Suchmaschine beim Durchsuchen von Schlüsselwörtern für die Erweiterte Abfrage Syntax (AQS) verwendet.

Wenn Sie z. b. die englischsprachige Version ohne MUI-Pakete haben, sind sowohl das Gebiets Schema des Inhalts Gebiets Schemas als auch das Schlüsselwort locale 1033. Wenn Sie über die deutsche Version ohne MUI-Pakete verfügen, sind sowohl das Gebiets Schema des Inhalts Gebiets Schemas als auch das Schlüsselwort locale 1031 (Gr-GR). Wenn Sie jedoch über die englische Version mit dem rumänischen MUI Pack verfügen, ist das Inhalts Gebiets Schema 2072 (RO), und das Schlüsselwort locale ist 1033 (en-US).

## <a name="working-with-properties-and-columns"></a>Arbeiten mit Eigenschaften und Spalten



| Methoden                                                                                                                                                                                                                                                  | BESCHREIBUNG                                                                                                                                     |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Isearchqueryhelper:: get \_ querycontentproperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querycontentproperties)/<br/> [**Isearchqueryhelper::p UT \_ querycontentproperties**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querycontentproperties)<br/> | Dient zum Abrufen oder Festlegen der Inhalts Eigenschaften für die Suche (in der enthält-Klausel oder der frei Text Klausel aufgeführte Eigenschafts Spalte).                                   |
| [**Isearchqueryhelper:: get \_ queryselectcolumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_queryselectcolumns)/<br/> [**Isearchqueryhelper::p UT \_ queryselectcolumns**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_queryselectcolumns)<br/>                 | Ruft die in der SELECT-Anweisung angeforderten Spalten (oder Eigenschaften) ab oder legt Sie fest. Der Standardwert ist System. itemurl und Eigenschaften, die in der WHERE-Klausel verwendet werden. |



 

Elemente werden im Eigenschaften Speicher als Zeile dargestellt. Jede Zeile enthält eine Reihe von Spalten, die Eigenschaften für dieses Element darstellen. Nicht alle Elemente haben einen Wert für eine bestimmte Eigenschaft. Beispielsweise enthält eine Audiodatei in der Regel keinen Wert für die System. Property. FromName-Eigenschaft, kann jedoch Informationen zu System. Music. Artist enthalten.

Mit diesen Methoden greifen Sie auf die-Eigenschaft mit einer durch Trennzeichen getrennten, auf NULL endenden Unicode-Zeichenfolge zu, die einen oder mehrere Spaltennamen des Eigenschaften Stores angibt: "System.Document. Autor, System.Doc. Title ".

## <a name="working-with-query-term-expansion"></a>Arbeiten mit der Abfrage Begriffs Erweiterung



| Methoden                                                                                                                                                                                                                                 | BESCHREIBUNG                               |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------|
| [**Isearchqueryhelper:: get \_ querytermexpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querytermexpansion)<br/> [**Isearchqueryhelper::p UT \_ querytermexpansion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querytermexpansion)<br/> | Ruft das Erweiterungs Flag für den Suchbegriff ab oder legt es fest. |



 

Diese Methode ermöglicht die Erweiterung einiger Abfrage Ausdrücke mit Platzhalter Zeichen, ähnlich der Erweiterung regulärer Ausdrücke. Präfix Erweiterung sucht nach Wörtern mit dem gleichen Präfix (Spaß/Trichter). Wenn nicht festgelegt, lautet der Standardwert Such \_ Begriff " \_ alle" \_ . Die folgenden Werte sind für die Enumeration der [**\_ \_ Erweiterungs**](/windows/desktop/api/Searchapi/ne-searchapi-search_term_expansion) Enumeration unterstützt:

-   Such \_ Begriff \_ Präfix \_ alle-alle Suchbegriffe werden erweitert
-   Such \_ Begriff \_ keine \_ Erweiterung-keine Suchbegriffe erweitert

## <a name="working-with-other-isearchqueryhelper-methods"></a>Arbeiten mit anderen isearchqueryhelper-Methoden

Viele der Methoden in der [**isearchqueryhelper**](/windows/desktop/api/Searchapi/nn-searchapi-isearchqueryhelper) -Schnittstelle werden verwendet, um Abfrage Argumente festzulegen oder die zurückgegebenen Eigenschaften zu definieren.



| Methoden                                                                                                                                                                                                                                                 | BESCHREIBUNG                                                                                                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Isearchqueryhelper:: get \_ ConnectionString**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_connectionstring)<br/>                                                                                                                                         | Gibt die OLE DB Verbindungs Zeichenfolge zurück. Dies ist die bevorzugte Methode, um eine ordnungsgemäß formatierte und korrekte Verbindungs Zeichenfolge zu erhalten.                                  |
| [**Isearchqueryhelper:: get \_ querymaxresults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querymaxresults)<br/> [**Isearchqueryhelper::p UT \_ querymaxresults**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querymaxresults)<br/>                             | Ruft die maximale Anzahl von Ergebnissen ab, die von einer Abfrage zurückgegeben werden sollen (d. h. Select Top n), oder legt Sie fest. Der Standardwert ist-1. Dies bedeutet, dass keine maximale Ergebnis Klausel generiert wird. |
| [**Isearchqueryhelper:: get \_ querysortierung**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysorting)<br/> [**Isearchqueryhelper::p UT- \_ querysortierung**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysorting)<br/>                                         | Gibt die Sortierreihenfolge für das Abfrageresultset zurück (Order by). Wenn keine ORDER BY-Klausel vorhanden ist, werden die Ergebnisse in nicht deterministischer Reihenfolge zurückgegeben.                   |
| [**Isearchqueryhelper:: get \_ querysyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querysyntax)<br/> [**Isearchqueryhelper::p UT- \_ querysyntax**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querysyntax)<br/>                                             | Ruft die Syntax der Abfrage ab oder legt Sie fest: Erweiterte Abfrage Syntax oder Syntax für natürliche Abfragen.                                                                                  |
| [**Isearchqueryhelper:: get \_ querywhererestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-get_querywhererestrictions)<br/> [**Isearchqueryhelper::p UT \_ querywhererestrictions**](/windows/desktop/api/Searchapi/nf-searchapi-isearchqueryhelper-put_querywhererestrictions)<br/> | Gibt die Einschränkungen an, die über WHERE-Klauseln angefügt werden                                                                                                             |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Programm gesteuertes Abfragen des Indexes](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Verwenden von SQL-und AQS-Ansätzen zum Abfragen des Indexes](-search-3x-wds-qryidx-overview.md)
</dt> <dt>

[Abfragen des Indexes mit dem Search-MS-Protokoll](-search-3x-wds-qryidx-searchms.md)
</dt> <dt>

[Abfragen des Indexes mit der SQL-Syntax von Windows Search](-search-sql-windowssearch-entry.md)
</dt> <dt>

[Programm gesteuertes verwenden der erweiterten Abfrage Syntax](-search-3x-advancedquerysyntax.md)
</dt> </dl>

 

 




