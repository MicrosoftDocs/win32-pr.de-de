---
title: Implementieren eines Protokollhandlers für WDS
description: Das Erstellen eines Protokollhandlers umfasst die Implementierung von ISearchProtocol zum Verwalten von UrlAccessor-Objekten, IUrlAccessor zum Generieren von Metadaten zu und zum Identifizieren geeigneter Filter für Elemente im Datenspeicher, IProtocolHandlerSite zum Instanziieren eines SearchProtocol-Objekts und Identifizieren geeigneter Filter und IFilter, um proprietäre Dateien zu filtern oder hierarchisch gespeicherte Dateien aufzuzählen und zu filtern.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 32e33a7ebf6d5f14d0ec4d78031e25b17d59bac5fb99ee7ea6d20046fbe95c78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119963490"
---
# <a name="implementing-a-protocol-handler-for-wds"></a>Implementieren eines Protokollhandlers für WDS

> [!NOTE]
> Windows Desktop Search 2.x ist eine veraltete Technologie, die ursprünglich als Add-In für Windows XP und Windows Server 2003 verfügbar war. Verwenden Sie in späteren [Versionen Windows Search.](../search/-search-3x-wds-overview.md)

Das Erstellen eines Protokollhandlers umfasst die Implementierung von [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) zum Verwalten von UrlAccessor-Objekten, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) zum Generieren von Metadaten zu und zum Identifizieren geeigneter Filter für Elemente im Datenspeicher, IProtocolHandlerSite zum Instanziieren eines SearchProtocol-Objekts und Identifizieren geeigneter Filter und [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)zum Filtern proprietärer Dateien oder zum Aufzählen und Filtern hierarchisch gespeicherter Dateien. Der Protokollhandler muss multithreaded sein.

Diese Abschnitte enthalten die folgenden Themen:

-   [Hinweis zu URLs](#note-on-urls)
-   [Protokollhandlerschnittstellen](#protocol-handler-interfaces)
-   [IFilters für Container](#ifilters-for-containers)
-   [Hinzufügen der Funktionalität für Protokollhandleroptionen](#adding-protocol-handler-options-functionality)
    -   [ISearchProtocolOptions](#isearchprotocoloptions)
-   [Zugehörige Themen](#related-topics)

## <a name="note-on-urls"></a>Hinweis zu URLs

Microsoft Windows Desktop Search (WDS) verwendet URLs, um Elemente in einem Dateisystem, in einem datenbankbasierten Speicher oder im Web eindeutig zu identifizieren. Eine URL, die einen Einstiegsknoten definiert, wird als Startseite bezeichnet. WDS beginnt bei dieser Startseite und durchforstung den Datenspeicher rekursiv. Die typische URL-Struktur ist:

`protocol://host/path/name.extension`

> [!Note]
>
> Wenn Sie einen neuen Datenspeicher hinzufügen möchten, müssen Sie einen Namen auswählen, um ihn zu identifizieren, der nicht mit dem aktuellen Datenspeicher in Konflikt steht. Es wird empfohlen, diese Benennungskonvention zu verwenden: companyName.scheme.

 

## <a name="protocol-handler-interfaces"></a>Protokollhandlerschnittstellen

**ISearchProtocol**

Die [**ISearchProtocol-Schnittstelle**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) ruft UrlAccessor-Objekte auf, initialisiert und verwaltet sie. Weitere Informationen zum Implementieren der ISearchProtocol-Schnittstelle finden Sie in der **Referenz zur ISearchProtocol-Schnittstelle.**

**IUrlAccessor**

Für eine angegebene URL generiert die [**IUrlAccessor-Schnittstelle**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) Metadaten über die Speicherortstruktur sowie enthaltene Elemente und bindet diese Elemente an einen Filter. Das **IUrlAccessor-Objekt** wird von einem SearchProtocol-Objekt instanziiert und initialisiert. Sie können jedoch auch eine interne Initialisierungsmethode implementieren, damit Ihr **IUrlAccessor-Objekt** initialisierungsaufgaben ausführen kann, die für Ihren Protokollhandler spezifisch sind, z. B. das Überprüfen der URL für ein Element, auf das zugegriffen wird, oder das Überprüfen des Zeitpunkts der letzten Änderung, um zu bestimmen, ob eine Datei in der aktuellen Durchforstung verarbeitet werden muss.

> [!Note]
>
> Geänderte Zeiten für Verzeichnisse werden ignoriert. Das [**IUrlAccessor-Objekt**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) muss die untergeordneten Objekte aufzählen, um zu bestimmen, ob Änderungen oder Löschungen vorgenommen wurden.

 

Ein Größerer Teil des Entwurfs des **UrlAccessor-Objekts** hängt davon ab, ob die Struktur hierarchisch oder link-basiert ist. Bei hierarchischen Datenspeichern muss das **UrlAccessor-Objekt** einen Filter finden, der seinen Inhalt aufzählen kann. Ein weiterer Unterschied zwischen hierarchischen und linkbasierten Protokollhandlern ist die Verwendung der IsDirectory-Methode. In linkbasierten Protokollhandlern sollte diese Methode S \_ FALSE zurückgeben. Hierarchische Protokollhandler müssen S \_ OK für Container zurückgeben.

Weitere Anweisungen zum Implementieren einer [**IUrlAccessor-Schnittstelle**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) finden Sie in der [**Referenz zur IUrlAccessor-Schnittstelle.**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor)

**IProtocolHandlerSite**

Diese Schnittstelle wird verwendet, um ein **SearchProtocol-Objekt** zu instanziieren, und stellt dem **UrlAccessor-Objekt** einen entsprechenden Filter für eine angegebene Klassen-ID (CLSID) bereit.

## <a name="ifilters-for-containers"></a>IFilters für Container

Wenn Sie einen hierarchischen Protokollhandler implementieren, müssen Sie eine [**IFilter-Containerkomponente**](/windows/desktop/api/filter/nn-filter-ifilter)implementieren, die URLs aufzählt, die Container oder Ordner darstellen. Der Enumerationsprozess ist eine Schleife durch die **GetChunk-** und **GetValue-Methoden** der IFilter-Schnittstelle, die eine Liste von URLs zurückgeben, die jedes Element im Container darstellen.

**GetChunk gibt zunächst** eine FULLPROSPEC mit dem Eigenschaftensatz GATHER \_ PROPSET und einer der folgenden Zurück:

-   PID \_ GTHR \_ DIRLINK, die URL zum Element ohne zeitpunkt der letzten Änderung, oder
-   PID \_ GTHR \_ DIRLINK \_ WITH \_ TIME, die URL zusammen mit dem Zeitpunkt der letzten Änderung

Die GUID für den Eigenschaftensatz für GATHER \_ PROPSET ist 0B63E343-9CCC-11D0-BCDB-00805FCCCE04. Die PROPSPEC-Eigenschaft ist entweder PID \_ GTHR \_ DIRLINK=2 oder PID \_ GTHR \_ DIRLINK \_ WITH TIME = \_ 12 decimal.

Die Rückgabe von PID GTHR DIRLINK WITH TIME ist effizienter, da der Indexer sofort bestimmen kann, ob das Element indiziert werden muss, ohne die \_ \_ Methoden \_ \_ ISearchProtocol->CreateUrlAccessor() und IUrlAccessor->GetLastModified() auf aufruft.

Anschließend gibt **GetValue** eine PROPVARIANT-Eigenschaft für die URL (und den Zeitpunkt der letzten Änderung bei Verwendung) zurück:

-   VT \_ LPWSTR, die URL des untergeordneten Elements oder
-   Vektor der URL gefolgt von filetime

Der folgende Beispielcode veranschaulicht, wie sie den richtigen PID \_ GTHR \_ DIRLINK \_ WITH TIME \_ erstellen.

> [!Note]
>
> **DIESER CODE UND DIE INFORMATIONEN WERDEN "WIE BEFÄHRT" BEREITGESTELLT, OHNE JEGLICHE GEWÄHRLEISTUNG, ENTWEDER AUSGEDRÜCKT ODER KONKLUDENT, EINSCHLIEßLICH, ABER NICHT BESCHRÄNKT AUF DIE KONKLUDENTEN GEWÄHRLEISTUNGEN DER HANDELSIERBARKEIT UND/ODER EIGNUNG FÜR EINEN BESTIMMTEN ZWECK.**
>
> Copyright (C) Microsoft. All rights reserved.

 


```
// params are assumed to be valid

HRESULT GetPropVariantForUrlAndTime(PCWSTR pszUrl, const FILETIME &ftLastModified, PROPVARIANT **ppPropValue)
{
    *ppPropValue = NULL;

    // allocate the propvariant pointer
    *ppPropValue = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*ppPropValue));
    HRESULT hr = *ppPropValue ? S_OK : E_OUTOFMEMORY;

    if (SUCCEEDED(hr))
    {
        PropVariantInit(*ppPropValue);  // zero init the value

        // now allocate enough memory for 2 nested PropVariants.
        // PID_GTHR_DIRLINK_WITH_TIME is an array of 2 PROPVARIANTs
        PROPVARIANT *pVector = (PROPVARIANT *)CoTaskMemAlloc(sizeof(*pVector) * 2);
        hr = pVector ? S_OK : E_OUTOFMEMORY;

        if (SUCCEEDED(hr))
        {
            // set the container PROPVARIANT that it is a vector of 2 PROPVARIANTS
            (*ppPropValue)->vt = VT_VARIANT | VT_VECTOR;
            (*ppPropValue)->capropvar.cElems = 2;
            (*ppPropValue)->capropvar.pElems = pVector;
            PWSTR pszUrlAlloc;
            hr = SHStrDup(pszUrl, &pszUrlAlloc);

            if (SUCCEEDED(hr))
            {
                // now fill the array of PROPVARIANTS
                // put the pointer to the URL into the vector
                (*ppPropValue)->capropvar.pElems[0].vt = VT_LPWSTR; 
                (*ppPropValue)->capropvar.pElems[0].pwszVal = pszUrlAlloc;

                 // put the FILETIME into vector
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
>
> Eine [**IFilter-Containerkomponente**](/windows/desktop/api/filter/nn-filter-ifilter)sollte immer alle untergeordneten URLs auflisten, auch wenn sich die untergeordneten URLs nicht geändert haben, da der Indexer Löschungen über den Enumerationsprozess erkennt. Wenn die Datumsausgabe in einer DIR LINKS WITH TIME angibt, dass die Daten nicht geändert wurden, aktualisiert der Indexer die Daten für \_ \_ diese URL \_ nicht.

 

Die physische URL ist die URL, die vom **UrlAccessor-Objekt** verarbeitet wird. Wenn der Filter keine benutzerfreundliche DisplayUrl aus gibt, zeigt WDS die physische URL für den Benutzer als Teil der Suchergebnisse an. Das WDS-Schema enthält zwei Eigenschaften, um zu steuern, was dem Endbenutzer angezeigt wird, wie in der folgenden Tabelle gezeigt.



| GUID                                 | PROPSPEC      | Beschreibung                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | DisplayFolder | Ordnerpfad, der dem Benutzer in den Suchergebnissen angezeigt wird |
| D5CDD505-2E9C-101B-9397-08002B2CF9AE | FolderName    | Anzeigename des übergeordneten Ordners                   |



 

Wenn Ihr Code keinen DisplayFolder oder FolderName aus gibt, werden diese Werte aus der DisplayUrl berechnet. Schrägstriche in der URL bezeichnen Container innerhalb des Speichers oder Dateisystems.

## <a name="adding-protocol-handler-options-functionality"></a>Hinzufügen der Funktionalität für Protokollhandleroptionen

Damit Ihr Protokollhandler über eine Standardstartseite (und url des Einstiegsknotens) verfügen kann, müssen Sie die **ISearchProtocolOptions-Schnittstelle** implementieren. In zukünftigen Versionen von WDS stellt diese Schnittstelle Hooks für das Dialogfeld Optionen bereit, um die Benutzerfreundlichkeit zu verbessern. Diese Schnittstelle bietet die folgenden Funktionen:

-   Bestimmt, ob die Anforderungen für ihren Protokollhandler erfüllt sind. Beispielsweise kann der Speicher des Protokollhandlers Zugriff auf eine bestimmte Anwendung erfordern, um die Daten der Anwendung ordnungsgemäß zu indizieren, aber diese Anwendung ist nicht verfügbar.
-   Gibt die Mindestanforderungen an, die Ihr Protokollhandler zum Verarbeiten eines Elements benötigt. Anforderungen können in einer benutzerfreundlichen, lokalisierten Beschreibung ausgedrückt werden, z. B. "Microsoft Outlook 2000 oder höher".
-   Definiert die URLs, die ihr Protokollhandler standardmäßig verarbeiten soll.

### <a name="isearchprotocoloptions"></a>ISearchProtocolOptions

In der folgenden Tabelle werden die Methoden beschrieben, die Sie für die **ISearchProtocolOptions-Schnittstelle implementieren** müssen.



| Methode               | Beschreibung                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| CheckRequirements    | Bestimmt, ob die Mindestanforderungen eines benutzerdefinierten Protokollhandlers erfüllt sind.                             |
| GetDefaultCrawlScope | Gibt eine Liste der Standard-URLs innerhalb eines angegebenen Speichers für einen benutzerdefinierten Protokollhandler zurück.                   |
| GetRequirements      | Identifiziert eine benutzerfreundliche, lokalisierte Beschreibung der Mindestanforderungen für einen benutzerdefinierten Protokollhandler. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

**Referenz**
</dt> <dt>

[Benachrichtigen des Indexes über Änderungen](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[Hinzufügen von Symbolen, Vorschauen und Kontextmenüs mit Shellerweiterungen](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[Installieren und Registrieren von Protokollhandlern](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 