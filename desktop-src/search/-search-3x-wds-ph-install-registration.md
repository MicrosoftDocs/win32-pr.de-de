---
description: Die Installation eines Protokoll Handlers umfasst das Kopieren der dll (s) an einen geeigneten Speicherort im Verzeichnis "Programme" und das anschließende Registrieren des Protokoll Handlers über die Registrierung.
ms.assetid: 07c40c0c-2729-462c-ba40-e05ffea2b889
title: Installieren und Registrieren von Protokoll Handlern (Windows Search)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7cb30032ef200832446a8a2f37b2ec427ab40b58
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106353028"
---
# <a name="installing-and-registering-protocol-handlers-windows-search"></a>Installieren und Registrieren von Protokoll Handlern (Windows Search)

Die Installation eines Protokoll Handlers umfasst das Kopieren der dll (s) an einen geeigneten Speicherort im Verzeichnis "Programme" und das anschließende Registrieren des Protokoll Handlers über die Registrierung. Die Installationsanwendung kann auch eine Such Stamm-und Bereichs Regel hinzufügen, um einen Standard-Crawlen Bereich für die shelldatenquelle zu definieren.

Dieses Thema ist wie folgt organisiert:

-   [Informationen zu URLs](#about-urls)
-   [Implementieren von protokollhandlerschnittstellen](#implementing-protocol-handler-interfaces)
    -   [Isearchprotocol und ISearchProtocol2](#isearchprotocol-and-isearchprotocol2)
    -   [Iurlaccessor, IUrlAccessor2, IUrlAccessor3 und IUrlAccessor4](#iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4)
    -   [Iprotocolhandlersite](#iprotocolhandlersite)
-   [Implementieren von Filter Handlern für Container](#implementing-filter-handlers-for-containers)
-   [Installieren und Registrieren eines Protokoll Handlers](#installing-and-registering-a-protocol-handler)
    -   [Richtlinien zum Registrieren eines Protokoll Handlers](#guidelines-for-registering-a-protocol-handler)
    -   [Registrieren eines Protokoll Handlers](#installing-and-registering-a-protocol-handler)
    -   [Registrieren des Dateityp Handlers des Protokoll Handlers](#registering-the-protocol-handlers-file-type-handler)
-   [Sicherstellen, dass ihre Elemente indiziert werden](#ensuring-that-your-items-are-indexed)
-   [Zugehörige Themen](#related-topics)

## <a name="about-urls"></a>Informationen zu URLs

Windows Search verwendet URLs, um Elemente in der Hierarchie der shelldatenquelle eindeutig zu identifizieren. Die URL, die der erste Knoten in der Hierarchie ist, wird als [Suchstamm](-search-3x-wds-extidx-csm-searchroots.md)bezeichnet. Windows Search beginnt mit der Indizierung am Suchstamm und fordert an, dass der Protokollhandler für jede URL untergeordnete Links aufzählt.

Die typische URL-Struktur lautet wie folgt:


```
<protocol>:// [{user SID}/] <localhost>/<path>/[<ItemID>]
```



Die URL-Syntax wird in der folgenden Tabelle beschrieben.



| Syntax           | BESCHREIBUNG                                                                                                                                                                                                        |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <protocol> | Gibt an, welcher Protokollhandler für die URL aufgerufen werden soll.                                                                                                                                                           |
| {Benutzer-sid}       | Gibt den Benutzer Sicherheitskontext an, unter dem der Protokollhandler aufgerufen wird. Wenn keine Benutzersicherheits-ID (SID) identifiziert wird, wird der Protokollhandler im Sicherheitskontext des-System Diensts aufgerufen. |
| <path>     | Definiert die Hierarchie des Stores, wobei jeder Schrägstrich ("/") ein Trennzeichen zwischen den Ordnernamen ist.                                                                                                            |
| <ItemID>   | Stellt eine eindeutige Zeichenfolge dar, die das untergeordnete Element identifiziert (z. b. den Dateinamen).                                                                                                                            |



 

Der Windows Search-Indexer schneidet den abschließenden Schrägstrich aus den URLs ab. Daher können Sie sich nicht darauf verlassen, dass ein abschließender Schrägstrich vorhanden ist, um ein Verzeichnis im Vergleich zu einem Element zu identifizieren. Der Protokollhandler muss diese URL-Syntax verarbeiten können. Stellen Sie sicher, dass der Protokoll Name, den Sie zur Identifizierung der shelldatenquelle ausgewählt haben, nicht mit den aktuellen Konflikten in Konflikt steht. Diese Benennungs Konvention wird empfohlen: `companyName.scheme` .

Weitere Informationen zum Erstellen einer shelldatenquelle finden Sie unter [Implementieren der grundlegenden Ordner Objekt Schnittstellen](/previous-versions/windows/desktop/legacy/cc144093(v=vs.85)).

## <a name="implementing-protocol-handler-interfaces"></a>Implementieren von protokollhandlerschnittstellen

Das Erstellen eines Protokoll Handlers erfordert die Implementierung der folgenden drei Schnittstellen:

-   [**Isearchprotocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol) zum Verwalten von urlaccessor-Objekten.
-   [**Iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) , um Eigenschaften verfügbar zu machen und geeignete Filter für Elemente in der shelldatenquelle zu identifizieren.
-   [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) zum Filtern von proprietären Dateien oder zum Auflisten und Filtern hierarchisch gespeicherter Dateien.

Die anderen Schnittstellen sind optional, außer den drei obligatorischen aufgelisteten Schnittstellen, sind optional, und Sie haben die Wahl, welche optionalen Schnittstellen für die jeweilige Aufgabe am besten geeignet sind.

### <a name="isearchprotocol-and-isearchprotocol2"></a>Isearchprotocol und ISearchProtocol2

Die searchprotocol-Schnittstellen initialisieren und verwalten die urlaccessor-Objekte des Protokoll Handlers. Die [**ISearchProtocol2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol2) -Schnittstelle ist eine optionale Erweiterung von [**isearchprotocol**](/windows/desktop/api/Searchapi/nn-searchapi-isearchprotocol)und umfasst eine zusätzliche Methode, um weitere Informationen über den Benutzer und das Element anzugeben.

### <a name="iurlaccessor-iurlaccessor2-iurlaccessor3-and-iurlaccessor4"></a>Iurlaccessor, IUrlAccessor2, IUrlAccessor3 und IUrlAccessor4

Die [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) -Schnittstellen werden in der folgenden Tabelle beschrieben.



| Schnittstelle                                                 | BESCHREIBUNG                                                                                                                                                                                                                                                                                             |
|-----------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor)              | Für eine angegebene URL bietet die [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) -Schnittstelle Zugriff auf die Eigenschaften des Elements, das in der URL verfügbar gemacht wird. Diese Eigenschaften können auch an einen protokollhandlerspezifischen Filter gebunden werden (d. h., es handelt sich um einen anderen Filter als den, der dem Dateinamen zugeordnet ist). |
| [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) (optional) | Die [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) -Schnittstelle erweitert [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) mit Methoden, die eine Codepage für die Eigenschaften des Elements und seine Anzeige-URL erhalten und den Typ des Elements in der URL (Dokument oder Verzeichnis) erhalten.                                    |
| [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) (optional) | Die [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) -Schnittstelle erweitert [**IUrlAccessor2**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor2) mit einer Methode, die ein Array von Benutzer-SIDs abruft, sodass der Such Protokoll Host die Identität dieser Benutzer annimmt, um das Element zu indizieren.                                                      |
| [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) (optional) | Die [**IUrlAccessor4**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor4) -Schnittstelle erweitert die Funktionalität der [**IUrlAccessor3**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor3) -Schnittstelle mit einer Methode, die angibt, ob der Inhalt des Elements indiziert werden soll.                                                                 |



 

Das urlaccessor-Objekt wird von einem searchprotocol-Objekt instanziiert und initialisiert. Die [**iurlaccessor**](/windows/desktop/api/Searchapi/nn-searchapi-iurlaccessor) -Schnittstellen ermöglichen den Zugriff auf wichtige Informationen mithilfe der in der folgenden Tabelle beschriebenen Methoden.



| Methode                                                                                        | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                        |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iurlaccessor:: getLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified)                 | Gibt die Uhrzeit zurück, zu der die URL zuletzt geändert wurde. Wenn diese Zeit aktueller ist als der letzte Zeitpunkt, zu dem der Indexer diese URL verarbeitet hat, werden Filter Handler (Implementierungen der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle) aufgerufen, um die (möglicherweise) geänderten Daten für dieses Element zu extrahieren. Geänderte Zeiten für Verzeichnisse werden ignoriert. |
| [**Iurlaccessor:: IsDirectory**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-isdirectory)                         | Gibt an, ob die URL einen Ordner mit untergeordneten URLs darstellt.                                                                                                                                                                                                                                                            |
| [**Iurlaccessor:: BindTo Stream**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtostream)                       | Bindet an eine [IStream-Schnittstelle](/windows/win32/api/objidl/nn-objidl-istream) , die die Daten einer Datei in einem benutzerdefinierten Datenspeicher darstellt.                                                                                                                                                                           |
| [**Iurlaccessor:: BindTo Filter**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-bindtofilter)                       | Bindet an einen protokollhandlerspezifischen [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter), der Eigenschaften für das Element verfügbar machen kann.                                                                                                                                                                                                                 |
| [**IUrlAccessor4:: Schultern**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor4-shouldindexitemcontent) | Gibt an, ob der Inhalt des Elements indiziert werden soll.                                                                                                                                                                                                                                                                      |



 

### <a name="iprotocolhandlersite"></a>Iprotocolhandlersite

Die [**iprotocolhandlersite**](/windows/desktop/api/Searchapi/nn-searchapi-iprotocolhandlersite) -Schnittstelle wird verwendet, um einen Filter Handler zu instanziieren, der in einem isolierten Prozess gehostet wird. Der geeignete Filter Handler wird für eine angegebene CLSID (persistente Klassen-ID), Dokument Speicher Klasse oder Dateinamenerweiterung abgerufen. Der Vorteil, dass der Host Prozess an [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) gebunden werden muss, besteht darin, dass der Host Prozess den Prozess des Auffinden eines geeigneten Filter Handlers verwalten und die beim Aufrufen des Handlers beteiligte Sicherheit steuern kann.

## <a name="implementing-filter-handlers-for-containers"></a>Implementieren von Filter Handlern für Container

Wenn Sie einen hierarchischen Protokollhandler implementieren, müssen Sie einen Filter Handler für einen Container implementieren, der untergeordnete URLs auflistet. Ein Filter Handler ist eine Implementierung der [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Schnittstelle. Der enumerationsprozess ist eine Schleife durch die [**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) -Methode und die [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) -Methode der **IFilter** -Schnittstelle. Jede untergeordnete URL wird als Wert der-Eigenschaft verfügbar gemacht.

[**IFilter:: GetChunk**](/windows/win32/api/filter/nf-filter-ifilter-getchunk) gibt die Eigenschaften des Containers zurück. Um untergeordnete URLs aufzulisten, gibt **IFilter:: GetChunk** einen der folgenden zurück:

-   [Pkey \_ \_Urlyindex durchsuchen](/previous-versions/windows/desktop/legacy/bb760177(v=vs.85)):

    Die URL des Elements ohne den Zeitpunkt der letzten Änderung. [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) gibt eine PROPVARIANT zurück, die die untergeordnete URL enthält.

-   [Pkey \_ Suchen Sie \_ urldeindexwithmodificationtime](../properties/props-system-search-urltoindexwithmodificationtime.md):

    Die URL und die Uhrzeit der letzten Änderung. [**IFilter:: GetValue**](/windows/win32/api/filter/nf-filter-ifilter-getvalue) gibt eine PROPVARIANT zurück, die einen Vektor der untergeordneten URL und der Uhrzeit der letzten Änderung enthält.

Das Zurückgeben der [pkey- \_ Suche \_ urltoindexwithmodificationtime](../properties/props-system-search-urltoindexwithmodificationtime.md) ist effizienter, da der Indexer sofort ermitteln kann, ob das Element indiziert werden muss, ohne die Methoden [**isearchprotocol:: CreateAccessor**](/windows/desktop/api/Searchapi/nf-searchapi-isearchprotocol-createaccessor) und [**iurlaccessor:: getLastModified**](/windows/desktop/api/Searchapi/nf-searchapi-iurlaccessor-getlastmodified) aufrufen zu müssen.

Im folgenden Beispielcode wird veranschaulicht, wie die Eigenschaft " [ \_ \_ urltoindexwithmodificationtime" der pkey-Suche](../properties/props-system-search-urltoindexwithmodificationtime.md) zurückgegeben wird.

> [!IMPORTANT]
>
> Copyright (c) Microsoft Corporation. Alle Rechte vorbehalten.

 


```
// Parameters are assumed to be valid

HRESULT GetPropVariantForUrlAndTime
    (PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // Allocate the propvariant pointer.
    size_t const cbAlloc = sizeof(**ppPropValue);
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(cbAlloc));

    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // Zero init the value

        // Now allocate enough memory for 2 nested PropVariants.
        // PKEY_Search_UrlToIndexWithModificationTime is an array of two PROPVARIANTs.
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // Set the container PROPVARIANT to be a vector of two PROPVARIANTS.
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // Now fill the array of PROPVARIANTS.
                // Put the pointer to the URL into the vector.
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // Put the FILETIME into vector.
                (*ppPropValue)->capropvar.pElems[1].vt = VT_FILETIME; 
                (*ppPropValue)->capropvar.pElems[1].filetime = ftLastModified;
            }

            else
            {
                CoTaskMemFree(pVector);
            }
        }
 
        if (FAILED(hr))
        {
            CoTaskMemFree(*ppPropValue);
            *ppPropValue = NULL;
        }
    }
    return S_OK;
}

```



> [!Note]  
> Eine [**IFilter**](/windows/win32/api/filter/nn-filter-ifilter) -Container Komponente sollte immer alle untergeordneten URLs auflisten, auch wenn sich die untergeordneten URLs nicht geändert haben, da der Indexer Löschungen durch den enumerationsprozess erkennt. Wenn die Datums Ausgabe in einer [pkey- \_ Suche \_ urltoindexwithmodificationtime](../properties/props-system-search-urltoindexwithmodificationtime.md) angibt, dass die Daten nicht geändert wurden, aktualisiert der Indexer nicht die Daten für diese URL.

 

## <a name="installing-and-registering-a-protocol-handler"></a>Installieren und Registrieren eines Protokoll Handlers

Das Installieren von Protokoll Handlern umfasst das Kopieren der dll (s) an einen geeigneten Speicherort im Verzeichnis "Programme" und das anschließende Registrieren der dll (s). Protokollhandler sollten die Selbstregistrierung für die Installation implementieren. Die Installationsanwendung kann auch einen Such Stamm und Bereichs Regeln hinzufügen, um einen Standard-Crawlen Bereich für die Shell-Datenquelle zu definieren. Dies wird unter [sicherstellen, dass ihre Elemente](#ensuring-that-your-items-are-indexed) am Ende dieses Themas indiziert werden.

### <a name="guidelines-for-registering-a-protocol-handler"></a>Richtlinien zum Registrieren eines Protokoll Handlers

Beachten Sie beim Registrieren eines Protokoll Handlers die folgenden Richtlinien:

-   Das Installationsprogramm muss entweder exe oder das MSI-Installationsprogramm verwenden.
-   Anmerkungen zu dieser Version müssen bereitgestellt werden.
-   Ein Eintrag zum Hinzufügen/Entfernen von Programmen muss für jedes installierte Add-in erstellt werden.
-   Das Installationsprogramm muss alle Registrierungs Einstellungen für einen bestimmten Dateityp oder-Speicher übernehmen, den das aktuelle Add-in versteht.
-   Wenn ein vorheriges Add-in überschrieben wird, sollte das Installationsprogramm den Benutzer benachrichtigen.
-   Wenn das vorherige Add-in von einem neueren Add-in überschrieben wurde, sollte es möglich sein, die vorherige Add-in-Funktionalität wiederherzustellen und das Standard-Add-in für diesen Dateityp erneut zu erstellen.
-   Das Installationsprogramm sollte einen Standard Durchforstungs Bereich für den Indexer definieren, indem er mithilfe von Crawl Scope Manager (CSM) einen Such Stamm und Bereichs Regeln hinzufügt.

### <a name="registering-a-protocol-handler"></a>Registrieren eines Protokoll Handlers

Sie müssen 14 Einträge in der Registrierung vornehmen, um die Protokollhandlerkomponente zu registrieren, wobei Folgendes gilt:

-   *Ver \_ IND \_ ProgID* ist die Versions unabhängige ProgID der protokollhandlerimplementierung.
-   *Ver \_ DEP \_ ProgID* ist die Versions abhängige ProgID der protokollhandlerimplementierung.
-   *CLSID \_ 1* ist die CLSID der protokollhandlerimplementierung.

**So registrieren Sie einen Protokollhandler:**

1.  Registrieren Sie die Versions unabhängige ProgID mit den folgenden Schlüsseln und Werten:

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Ind_ProgID>
          CurVer
             (Default) = <Ver_Dep_ProgID>
    ```

2.  Registrieren Sie die Versions abhängige ProgID mit den folgenden Schlüsseln und Werten:

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       <Ver_Dep_ProgID>
          CLSID
             (Default) = {CLSID_1}
    ```

3.  Registrieren Sie die CLSID des Protokoll Handlers mit den folgenden Schlüsseln und Werten:

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          (Default) = <Protocol Handler Class Description>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          {InprocServer32}
             (Default) = <DLL Install Path>
             Threading Model = Both
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ProgID>
             (Default) = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          <ShellFolder>
             Attributes = dword:a0180000
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          TypeLib
             (Default) = {LIBID of PH Component}
    ```

    ```
    HKEY_CLASSES_ROOT
       {CLSID_1}
          VersionIndependentProgID
             (Default) = <Ver_Ind_ProgID>
    ```

4.  Registrieren Sie den Protokollhandler bei Windows Search. Im folgenden Beispiel <Protocol Name> ist der Name des Protokolls, wie z. b. File, MAPI usw.:

    ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Search
                ProtocolHandlers
                   <Protocol Name> = <Ver_Dep_ProgID>
    ```

    Vor Windows Vista:

    ```
    HKEY_CURRENT_USER
       SOFTWARE
          Microsoft
             Windows Desktop Search
                DS
                   Index
                      ProtocolHandlers
                         <Protocol Name>
                            HasRequirements = dword:00000000
                            HasStartPage = dword:00000000
    ```

### <a name="registering-the-protocol-handlers-file-type-handler"></a>Registrieren des Dateityp Handlers des Protokoll Handlers

Sie müssen zwei Einträge in der Registrierung vornehmen, um den Dateityp Handler des Protokoll Handlers zu registrieren (dieser wird auch als Shellerweiterung bezeichnet).

1.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Desktop
                         NameSpace
                            {CLSID of PH Implementation}
                               (Default) = <Shell Implementation Description>
    ```

2.  ```
    HKEY_LOCAL_MACHINE
       SOFTWARE
          Microsoft
             Windows
                CurrentVersion
                   Explorer
                      Shell Extensions
                         Approved
                            {CLSID of PH Implementation} = <Shell Implementation Description>
    ```

## <a name="ensuring-that-your-items-are-indexed"></a>Sicherstellen, dass ihre Elemente indiziert werden

Nachdem Sie den Protokollhandler implementiert haben, müssen Sie angeben, welche shellelemente der Protokollhandler indizieren soll. Sie können den Katalog-Manager verwenden, um die erneute Indizierung zu initiieren (Weitere Informationen finden Sie unter [Verwenden des Katalog-Managers](-search-3x-wds-mngidx-catalog-manager.md)). Sie können auch den Crawl Scope Manager (CSM) zum Einrichten von Standardregeln verwenden, um die URLs anzugeben, die der Indexer durchforsten soll (Weitere Informationen finden Sie unter [Verwenden von Crawl Scope Manager](-search-3x-wds-extidx-csm.md) und [Verwalten von Bereichs Regeln](-search-3x-wds-extidx-csm-scoperules.md)). Sie können auch einen Suchstamm hinzufügen (Weitere Informationen finden Sie unter [Verwalten von Such](-search-3x-wds-extidx-csm-searchroots.md)Stämmen). Eine weitere Option, die Ihnen zur Verfügung steht, ist die Vorgehensweise im Beispiel zum erneuten indizieren in den [Windows Search SDK-Beispielen](https://www.microsoft.com/downloads/details.aspx?FamilyID=645300AE-5E7A-4CE7-95F0-49793F8F76E8).

Die [**isearchcrawlscopemanager**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager) -Schnittstelle stellt Methoden bereit, die das Suchmodul von Containern zum durchforsten und/oder überwachen sowie Elemente unter diesen Containern Benachrichtigen, die beim Crawlen oder beim Zuschauen eingeschlossen oder ausgeschlossen werden sollen. In Windows 7 und höher erweitert [**ISearchCrawlScopeManager2**](/windows/desktop/api/Searchapi/nn-searchapi-isearchcrawlscopemanager2) **isearchcrawlscopemanager** mit der [**ISearchCrawlScopeManager2:: GetVersion**](/windows/desktop/api/Searchapi/nf-searchapi-isearchcrawlscopemanager2-getversion) -Methode, die die Version abruft, die Clients informiert, ob sich der Zustand des CSM geändert hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Licher**
</dt> <dt>

[Grundlegendes zu Protokoll Handlern](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[Entwickeln von Protokoll Handlern](-search-3x-wds-phaddins.md)
</dt> <dt>

[Benachrichtigen des Index von Änderungen](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[Hinzufügen von Symbolen und Kontextmenüs](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[Code Beispiel: Shellerweiterungen für Protokollhandler](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[Erstellen eines Suchconnector für einen Protokoll Handler](-search-3x-wds-ph-search-connector.md)
</dt> <dt>

[Debuggen von Protokoll Handlern](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
