---
title: Implementieren eines Protokoll Handlers für WDS
description: Zum Erstellen eines Protokoll Handlers gehört das Implementieren von isearchprotocol zum Verwalten von urlaccessor-Objekten, iurlaccessor zum Generieren von Metadaten über und das identifizieren geeigneter Filter für Elemente im Datenspeicher, iprotocolhandlersite zum Instanziieren eines searchprotocol-Objekts und identifizieren geeigneter Filter, und ifilterto filtert proprietäre Dateien oder hierarchisch gespeicherte Dateien.
ms.assetid: d4bcf370-4152-4cfd-a92e-eb9196d23ab4
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2c5a88ca5137b012431fff75bf5975a8b4820121
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "104101538"
---
# <a name="implementing-a-protocol-handler-for-wds"></a><span data-ttu-id="b72b3-103">Implementieren eines Protokoll Handlers für WDS</span><span class="sxs-lookup"><span data-stu-id="b72b3-103">Implementing a Protocol Handler for WDS</span></span>

> [!NOTE]
> <span data-ttu-id="b72b3-104">Windows-Desktop Suche 2. x ist eine veraltete Technologie, die ursprünglich als Add-in für Windows XP und Windows Server 2003 verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="b72b3-104">Windows Desktop Search 2.x is an obsolete technology that was originally available as an add-in for Windows XP and Windows Server 2003.</span></span> <span data-ttu-id="b72b3-105">Verwenden Sie in späteren Versionen stattdessen [Windows Search](../search/-search-3x-wds-overview.md) .</span><span class="sxs-lookup"><span data-stu-id="b72b3-105">On later releases, use [Windows Search](../search/-search-3x-wds-overview.md) instead.</span></span>

<span data-ttu-id="b72b3-106">Das Erstellen eines Protokoll Handlers umfasst das Implementieren von [**isearchprotocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) zum Verwalten von urlaccessor-Objekten, [**iurlaccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) zum Generieren von Metadaten über und das Ermitteln geeigneter Filter für Elemente im Datenspeicher, iprotocolhandlersite zum Instanziieren eines searchprotocol-Objekts und identifizieren geeigneter Filter und [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)zum Filtern von proprietären Dateien oder zum Auflisten und Filtern hierarchischer Dateien.</span><span class="sxs-lookup"><span data-stu-id="b72b3-106">Creating a protocol handler involves implementing [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) to manage UrlAccessor objects, [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) to generate metadata about and to identify appropriate filters for items in the data store, IProtocolHandlerSite to instantiate a SearchProtocol object and identify appropriate filters, and [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)to filter proprietary files or to enumerate and filter hierarchically stored files.</span></span> <span data-ttu-id="b72b3-107">Der Protokollhandler muss einen Multithread aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b72b3-107">The protocol handler must be multithreaded.</span></span>

<span data-ttu-id="b72b3-108">Diese Abschnitte enthalten die folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="b72b3-108">This sections contains the following topics:</span></span>

-   [<span data-ttu-id="b72b3-109">Hinweis zu URLs</span><span class="sxs-lookup"><span data-stu-id="b72b3-109">Note on URLs</span></span>](#note-on-urls)
-   [<span data-ttu-id="b72b3-110">Protokollhandlerschnittstellen</span><span class="sxs-lookup"><span data-stu-id="b72b3-110">Protocol Handler Interfaces</span></span>](#protocol-handler-interfaces)
-   [<span data-ttu-id="b72b3-111">IFilters für Container</span><span class="sxs-lookup"><span data-stu-id="b72b3-111">IFilters for Containers</span></span>](#ifilters-for-containers)
-   [<span data-ttu-id="b72b3-112">Hinzufügen von protokollhandleroptionen</span><span class="sxs-lookup"><span data-stu-id="b72b3-112">Adding Protocol Handler Options Functionality</span></span>](#adding-protocol-handler-options-functionality)
    -   [<span data-ttu-id="b72b3-113">Isearchprotocoloptions</span><span class="sxs-lookup"><span data-stu-id="b72b3-113">ISearchProtocolOptions</span></span>](#isearchprotocoloptions)
-   [<span data-ttu-id="b72b3-114">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b72b3-114">Related topics</span></span>](#related-topics)

## <a name="note-on-urls"></a><span data-ttu-id="b72b3-115">Hinweis zu URLs</span><span class="sxs-lookup"><span data-stu-id="b72b3-115">Note on URLs</span></span>

<span data-ttu-id="b72b3-116">Die Microsoft Windows-Desktop Suche (WDS) verwendet URLs, um Elemente in einem Dateisystem, in einem Daten bankähnlichen Speicher oder im Web eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b72b3-116">Microsoft Windows Desktop Search (WDS) uses URLs to uniquely identify items in a file system, inside a database-like store, or on the Web.</span></span> <span data-ttu-id="b72b3-117">Eine URL, die einen Einstiegs Knoten definiert, wird als Startseite bezeichnet. WDS beginnt an dieser Startseite und rekursiv den Datenspeicher durch Crawlen.</span><span class="sxs-lookup"><span data-stu-id="b72b3-117">A URL that defines an entry node is called a start page; WDS begins at that start page and recursively crawls the data store.</span></span> <span data-ttu-id="b72b3-118">Die typische URL-Struktur lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b72b3-118">The typical URL structure is:</span></span>

`protocol://host/path/name.extension`

> [!Note]
>
> <span data-ttu-id="b72b3-119">Wenn Sie einen neuen Datenspeicher hinzufügen möchten, müssen Sie einen Namen auswählen, um ihn zu identifizieren, der nicht mit aktuellen Konflikten in Konflikt steht.</span><span class="sxs-lookup"><span data-stu-id="b72b3-119">When you want to add a new data store, you'll need to select a name to identify it that does not conflict with current ones.</span></span> <span data-ttu-id="b72b3-120">Diese Benennungs Konvention wird empfohlen: CompanyName. Scheme.</span><span class="sxs-lookup"><span data-stu-id="b72b3-120">We recommend this naming convention: companyName.scheme.</span></span>

 

## <a name="protocol-handler-interfaces"></a><span data-ttu-id="b72b3-121">Protokollhandlerschnittstellen</span><span class="sxs-lookup"><span data-stu-id="b72b3-121">Protocol Handler Interfaces</span></span>

<span data-ttu-id="b72b3-122">**Isearchprotocol**</span><span class="sxs-lookup"><span data-stu-id="b72b3-122">**ISearchProtocol**</span></span>

<span data-ttu-id="b72b3-123">Die [**isearchprotocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) -Schnittstelle ruft urlaccessor-Objekte auf, initialisiert und verwaltet Sie.</span><span class="sxs-lookup"><span data-stu-id="b72b3-123">The [**ISearchProtocol**](/windows/desktop/api/searchapi/nn-searchapi-isearchprotocol) interface invokes, initializes, and manages UrlAccessor objects.</span></span> <span data-ttu-id="b72b3-124">Weitere Informationen zum Implementieren der isearchprotocol-Schnittstelle finden Sie unter **isearchprotocol Interface Reference**.</span><span class="sxs-lookup"><span data-stu-id="b72b3-124">For more information on implementing the ISearchProtocol interface, see **ISearchProtocol Interface reference**.</span></span>

<span data-ttu-id="b72b3-125">**Iurlaccessor**</span><span class="sxs-lookup"><span data-stu-id="b72b3-125">**IUrlAccessor**</span></span>

<span data-ttu-id="b72b3-126">Für eine angegebene URL generiert die [**iurlaccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) -Schnittstelle Metadaten über die Standortstruktur sowie enthaltene Elemente und bindet diese Elemente an einen Filter.</span><span class="sxs-lookup"><span data-stu-id="b72b3-126">For a specified URL, the [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface generates metadata about the location structure as well as contained items, and it binds those items to an filter.</span></span> <span data-ttu-id="b72b3-127">Das **iurlaccessor** -Objekt wird von einem searchprotocol-Objekt instanziiert und initialisiert. Sie können jedoch auch eine interne Initialisierungs Methode implementieren, damit Ihr **iurlaccessor** -Objekt Initialisierungs Aufgaben ausführen kann, die für den Protokollhandler spezifisch sind, z. b. das Überprüfen der URL für ein Element, auf das zugegriffen wird, oder das Überprüfen der Uhrzeit der letzten Änderung, um zu bestimmen, ob eine Datei in der aktuellen durch Forstung</span><span class="sxs-lookup"><span data-stu-id="b72b3-127">The **IUrlAccessor** object is instantiated and initialized by an SearchProtocol object; however, you can also implement an internal initialization method so your **IUrlAccessor** object can perform initialization tasks specific to your protocol handler, such as validating the URL for an item being accessed or checking the last modified time to determine if a file must be processed in the current crawl.</span></span>

> [!Note]
>
> <span data-ttu-id="b72b3-128">Geänderte Zeiten für Verzeichnisse werden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="b72b3-128">Modified times for directories are ignored.</span></span> <span data-ttu-id="b72b3-129">Das [**iurlaccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) -Objekt muss die untergeordneten Objekte auflisten, um zu bestimmen, ob Änderungen oder Löschungen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b72b3-129">The [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) object must enumerate the child objects to determine whether there have been any modifications or deletions.</span></span>

 

<span data-ttu-id="b72b3-130">Ein Großteil des Entwurfs des **urlaccessor** -Objekts ist davon abhängig, ob die Struktur hierarchisch oder Links basiert ist.</span><span class="sxs-lookup"><span data-stu-id="b72b3-130">Much of the design of the **UrlAccessor** object is dependent on whether the structure is hierarchical or link-based.</span></span> <span data-ttu-id="b72b3-131">Bei hierarchischen Daten speichern muss das **urlaccessor** -Objekt einen Filter finden, der ihren Inhalt auflisten kann.</span><span class="sxs-lookup"><span data-stu-id="b72b3-131">For hierarchical data stores, the **UrlAccessor** object must find an filter that can enumerate their contents.</span></span> <span data-ttu-id="b72b3-132">Ein weiterer Unterschied zwischen hierarchischen und Link basierten Protokoll Handlern ist die Verwendung der IsDirectory-Methode.</span><span class="sxs-lookup"><span data-stu-id="b72b3-132">Another distinction between hierarchical and link-based protocol handlers is the use of the IsDirectory method.</span></span> <span data-ttu-id="b72b3-133">In Link basierten Protokoll Handlern sollte diese Methode den Wert S false zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="b72b3-133">In link-based protocol handlers, this method should return S\_FALSE.</span></span> <span data-ttu-id="b72b3-134">Hierarchische Protokollhandler müssen für Container den Wert S OK zurückgeben \_ .</span><span class="sxs-lookup"><span data-stu-id="b72b3-134">Hierarchical protocol handlers must return S\_OK for containers.</span></span>

<span data-ttu-id="b72b3-135">Weitere Anweisungen zum Implementieren einer [**iurlaccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) -Schnittstelle finden Sie unter [**iurlaccessor Interface**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) Reference.</span><span class="sxs-lookup"><span data-stu-id="b72b3-135">For further instructions on implementing an [**IUrlAccessor**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) interface, see the [**IUrlAccessor Interface**](/windows/desktop/api/searchapi/nn-searchapi-iurlaccessor) reference.</span></span>

<span data-ttu-id="b72b3-136">**Iprotocolhandlersite**</span><span class="sxs-lookup"><span data-stu-id="b72b3-136">**IProtocolHandlerSite**</span></span>

<span data-ttu-id="b72b3-137">Diese Schnittstelle wird verwendet, um ein **searchprotocol** -Objekt zu instanziieren und das **urlaccessor** -Objekt mit einem geeigneten Filter für eine angegebene Klassen-ID (CLSID) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b72b3-137">This interface is used to instantiate a **SearchProtocol** object and also provides the **UrlAccessor** object with an appropriate filter for a specified class ID (CLSID).</span></span>

## <a name="ifilters-for-containers"></a><span data-ttu-id="b72b3-138">IFilters für Container</span><span class="sxs-lookup"><span data-stu-id="b72b3-138">IFilters for Containers</span></span>

<span data-ttu-id="b72b3-139">Wenn Sie einen hierarchischen Protokollhandler implementieren, müssen Sie eine [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Container Komponente implementieren, die URLs auflistet, die Container oder Ordner darstellen.</span><span class="sxs-lookup"><span data-stu-id="b72b3-139">If you are implementing a hierarchical protocol handler, you must implement a container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component that enumerates URLs representing containers or folders.</span></span> <span data-ttu-id="b72b3-140">Der enumerationsprozess ist eine Schleife durch die **GetChunk** -Methode und die **GetValue** -Methode der IFilter-Schnittstelle, die eine Liste von URLs zurückgeben, die jedes Element im Container darstellen.</span><span class="sxs-lookup"><span data-stu-id="b72b3-140">The enumeration process is a loop through the **GetChunk** and **GetValue** methods of the IFilter interface that return a list of URLs that represent each item in the container.</span></span>

<span data-ttu-id="b72b3-141">Zuerst gibt **GetChunk** eine Vollversion mit dem Eigenschaften Satz Gather \_ -propset zurück und eine der folgenden:</span><span class="sxs-lookup"><span data-stu-id="b72b3-141">First, **GetChunk** returns a FULLPROSPEC with the property set GATHER\_PROPSET and either:</span></span>

-   <span data-ttu-id="b72b3-142">PID \_ gthr \_ dirlink, die URL zu dem Element ohne den Zeitpunkt der letzten Änderung, oder</span><span class="sxs-lookup"><span data-stu-id="b72b3-142">PID\_GTHR\_DIRLINK, the URL to the item without the last modified time, or</span></span>
-   <span data-ttu-id="b72b3-143">PID \_ gthr \_ dirlink \_ with \_ Time, die URL zusammen mit dem Zeitpunkt der letzten Änderung</span><span class="sxs-lookup"><span data-stu-id="b72b3-143">PID\_GTHR\_DIRLINK\_WITH\_TIME, the URL along with the last modified time</span></span>

<span data-ttu-id="b72b3-144">Der Eigenschafts Satz-GUID für das Gather- \_ propset lautet 0b63e343-9ccc-11D0-bcdb-00805f ccce04.</span><span class="sxs-lookup"><span data-stu-id="b72b3-144">The property set GUID for GATHER\_PROPSET is 0B63E343-9CCC-11D0-BCDB-00805FCCCE04.</span></span> <span data-ttu-id="b72b3-145">Die PROPSPEC-Eigenschaft ist entweder PID \_ gthr \_ dirlink = 2 oder PID \_ gthr \_ dirlink \_ mit \_ Time = 12 Decimal.</span><span class="sxs-lookup"><span data-stu-id="b72b3-145">The PROPSPEC Property is either PID\_GTHR\_DIRLINK=2 or PID\_GTHR\_DIRLINK\_WITH\_TIME = 12 decimal.</span></span>

<span data-ttu-id="b72b3-146">Die Rückgabe \_ von PID gthr \_ dirlink \_ mit \_ Zeit ist effizienter, da der Indexer sofort ermitteln kann, ob das Element indiziert werden muss, ohne die Methoden isearchprotocol->createurlaccessor () und iurlaccessor->getLastModified () aufzurufende.</span><span class="sxs-lookup"><span data-stu-id="b72b3-146">Returning PID\_GTHR\_DIRLINK\_WITH\_TIME is more efficient because the indexer can immediately determine whether the item needs to be indexed without calling the ISearchProtocol->CreateUrlAccessor() and IUrlAccessor->GetLastModified() methods.</span></span>

<span data-ttu-id="b72b3-147">Anschließend gibt **GetValue** eine PROPVARIANT für die URL (und die Uhrzeit der letzten Änderung) wie folgt zurück:</span><span class="sxs-lookup"><span data-stu-id="b72b3-147">Then **GetValue** returns a PROPVARIANT for the URL (and last modified time if used), as either:</span></span>

-   <span data-ttu-id="b72b3-148">VT \_ LPWSTR, die URL des untergeordneten Elements oder</span><span class="sxs-lookup"><span data-stu-id="b72b3-148">VT\_LPWSTR, the URL of the child item, or</span></span>
-   <span data-ttu-id="b72b3-149">Vektor der URL, auf die eine FILETIME folgt.</span><span class="sxs-lookup"><span data-stu-id="b72b3-149">Vector of the URL followed by a FILETIME</span></span>

<span data-ttu-id="b72b3-150">Der folgende Beispielcode veranschaulicht, wie die richtige PID \_ gthr \_ dirlink \_ mit \_ Zeit erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b72b3-150">The following sample code demonstrates how to build the proper PID\_GTHR\_DIRLINK\_WITH\_TIME.</span></span>

> [!Note]
>
> <span data-ttu-id="b72b3-151">**Dieser Code und diese Informationen werden "wie immer" bereitgestellt, ohne jegliche Gewährleistungen jeglicher Art, entweder ausgedrückt oder impliziert, einschließlich, aber nicht beschränkt auf die impliziten Gewährleistungen der Handels Üblichkeit und/oder Eignung für einen bestimmten Zweck.**</span><span class="sxs-lookup"><span data-stu-id="b72b3-151">**THIS CODE AND INFORMATION IS PROVIDED "AS IS" WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE.**</span></span>
>
> <span data-ttu-id="b72b3-152">Copyright (C) Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b72b3-152">Copyright (C) Microsoft.</span></span> <span data-ttu-id="b72b3-153">Alle Rechte vorbehalten.</span><span class="sxs-lookup"><span data-stu-id="b72b3-153">All rights reserved.</span></span>

 


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
> <span data-ttu-id="b72b3-154">Eine [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)-Container Komponente sollte immer alle untergeordneten URLs auflisten, auch wenn sich die untergeordneten URLs nicht geändert haben, da der Indexer Löschungen durch den enumerationsprozess erkennt.</span><span class="sxs-lookup"><span data-stu-id="b72b3-154">A container [**IFilter**](/windows/desktop/api/filter/nn-filter-ifilter)component should always enumerate all child URLs even if the child URLs have not changed, because the Indexer detects deletions through the enumeration process.</span></span> <span data-ttu-id="b72b3-155">Wenn die Datums Ausgabe in einem dir- \_ Link \_ mit \_ der Zeit anzeigt, dass die Daten nicht geändert wurden, aktualisiert der Indexer nicht die Daten für diese URL.</span><span class="sxs-lookup"><span data-stu-id="b72b3-155">If the date output in a DIR\_LINKS\_WITH\_TIME indicates that the data has not changed, the indexer does not update the data for that URL.</span></span>

 

<span data-ttu-id="b72b3-156">Die physische URL ist die URL, die vom **urlaccessor** -Objekt verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="b72b3-156">The physical URL is the URL that the **UrlAccessor** object processes.</span></span> <span data-ttu-id="b72b3-157">Wenn der Filter keine benutzerfreundliche Display URL ausgibt, zeigt WDS die physische URL für den Benutzer als Teil der Suchergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="b72b3-157">If the filter does not emit a user-friendly DisplayUrl, WDS displays the physical URL to the user as part of the search results.</span></span> <span data-ttu-id="b72b3-158">Das WDS-Schema enthält zwei Eigenschaften, mit denen gesteuert werden kann, was für den Endbenutzer angezeigt wird, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="b72b3-158">The WDS schema contains two properties to control what is displayed to the end user, as shown in the table below.</span></span>



| <span data-ttu-id="b72b3-159">GUID</span><span class="sxs-lookup"><span data-stu-id="b72b3-159">GUID</span></span>                                 | <span data-ttu-id="b72b3-160">PROPSPEC</span><span class="sxs-lookup"><span data-stu-id="b72b3-160">PROPSPEC</span></span>      | <span data-ttu-id="b72b3-161">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b72b3-161">Description</span></span>                                         |
|--------------------------------------|---------------|-----------------------------------------------------|
| <span data-ttu-id="b72b3-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="b72b3-162">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="b72b3-163">DisplayFolder</span><span class="sxs-lookup"><span data-stu-id="b72b3-163">DisplayFolder</span></span> | <span data-ttu-id="b72b3-164">Ordner Pfad, der dem Benutzer in den Suchergebnissen angezeigt wird</span><span class="sxs-lookup"><span data-stu-id="b72b3-164">Folder Path displayed to the user in search results</span></span> |
| <span data-ttu-id="b72b3-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span><span class="sxs-lookup"><span data-stu-id="b72b3-165">D5CDD505-2E9C-101B-9397-08002B2CF9AE</span></span> | <span data-ttu-id="b72b3-166">FolderName</span><span class="sxs-lookup"><span data-stu-id="b72b3-166">FolderName</span></span>    | <span data-ttu-id="b72b3-167">Anzeige Name des übergeordneten Ordners</span><span class="sxs-lookup"><span data-stu-id="b72b3-167">Display name of the parent folder</span></span>                   |



 

<span data-ttu-id="b72b3-168">Wenn Ihr Code keinen DisplayFolder oder FolderName ausgibt, werden diese Werte aus der displayurl berechnet.</span><span class="sxs-lookup"><span data-stu-id="b72b3-168">If your code does not emit a DisplayFolder or FolderName, these values are computed from the DisplayUrl.</span></span> <span data-ttu-id="b72b3-169">Schrägstriche in der URL bezeichnen Container innerhalb des Stores oder Dateisystems.</span><span class="sxs-lookup"><span data-stu-id="b72b3-169">Forward slashes in the URL denote containers within the store or file system.</span></span>

## <a name="adding-protocol-handler-options-functionality"></a><span data-ttu-id="b72b3-170">Hinzufügen von protokollhandleroptionen</span><span class="sxs-lookup"><span data-stu-id="b72b3-170">Adding Protocol Handler Options Functionality</span></span>

<span data-ttu-id="b72b3-171">Damit der Protokollhandler über eine Standard Startseite (und eine Eingabe Knoten-URL) verfügt, müssen Sie die **isearchprotocoloptions** -Schnittstelle implementieren.</span><span class="sxs-lookup"><span data-stu-id="b72b3-171">For your protocol handler to have a default start page (and entry node URL), you must implement the **ISearchProtocolOptions** interface.</span></span> <span data-ttu-id="b72b3-172">In zukünftigen Versionen von WDS stellt diese Schnittstelle dem Dialogfeld "Optionen" Hooks für eine verbesserte Benutzeroberfläche bereit.</span><span class="sxs-lookup"><span data-stu-id="b72b3-172">In future versions of WDS, this interface will provide hooks to the Options dialog for an enhanced user experience.</span></span> <span data-ttu-id="b72b3-173">Diese Schnittstelle bietet die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="b72b3-173">This interface provides the following functionality:</span></span>

-   <span data-ttu-id="b72b3-174">Bestimmt, ob die Anforderungen für den Protokollhandler erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="b72b3-174">Determines whether the requirements for your protocol handler are met.</span></span> <span data-ttu-id="b72b3-175">Der Speicher des Protokoll Handlers benötigt z. b. möglicherweise Zugriff auf eine bestimmte Anwendung, um die Daten der Anwendung ordnungsgemäß zu indizieren, aber diese Anwendung ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b72b3-175">For example, your protocol handler's store may require access to a given application to properly index the application's data but that application is unavailable.</span></span>
-   <span data-ttu-id="b72b3-176">Gibt die Mindestanforderungen an, die der Protokollhandler für die Verarbeitung eines Elements benötigt.</span><span class="sxs-lookup"><span data-stu-id="b72b3-176">Identifies the minimum requirements your protocol handler needs to process an item.</span></span> <span data-ttu-id="b72b3-177">Anforderungen können in einer benutzerfreundlichen, lokalisierten Beschreibung ausgedrückt werden, z. b. "Microsoft Outlook 2000 oder höher".</span><span class="sxs-lookup"><span data-stu-id="b72b3-177">Requirements can be expressed in a user-friendly, localized description, such as "Microsoft Outlook 2000 or greater."</span></span>
-   <span data-ttu-id="b72b3-178">Definiert die URLs, die der Protokollhandler standardmäßig verarbeiten soll.</span><span class="sxs-lookup"><span data-stu-id="b72b3-178">Defines the URLs your protocol handler should process by default.</span></span>

### <a name="isearchprotocoloptions"></a><span data-ttu-id="b72b3-179">Isearchprotocoloptions</span><span class="sxs-lookup"><span data-stu-id="b72b3-179">ISearchProtocolOptions</span></span>

<span data-ttu-id="b72b3-180">In der folgenden Tabelle werden die Methoden beschrieben, die Sie für die **isearchprotocoloptions** -Schnittstelle implementieren müssen.</span><span class="sxs-lookup"><span data-stu-id="b72b3-180">The following table describes the methods you need to implement for the **ISearchProtocolOptions** interface.</span></span>



| <span data-ttu-id="b72b3-181">Methode</span><span class="sxs-lookup"><span data-stu-id="b72b3-181">Method</span></span>               | <span data-ttu-id="b72b3-182">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="b72b3-182">Description</span></span>                                                                                             |
|----------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b72b3-183">Prüfanforderungen</span><span class="sxs-lookup"><span data-stu-id="b72b3-183">CheckRequirements</span></span>    | <span data-ttu-id="b72b3-184">Bestimmt, ob die Mindestanforderungen eines benutzerdefinierten Protokoll Handlers erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="b72b3-184">Determines whether a custom protocol handler's minimum requirements are met</span></span>                             |
| <span data-ttu-id="b72b3-185">Getdefaultcrawlscope</span><span class="sxs-lookup"><span data-stu-id="b72b3-185">GetDefaultCrawlScope</span></span> | <span data-ttu-id="b72b3-186">Gibt eine Liste von Standard-URLs in einem angegebenen Speicher für einen benutzerdefinierten Protokollhandler zurück.</span><span class="sxs-lookup"><span data-stu-id="b72b3-186">Returns a list of default URLs within a specified store for a custom protocol handler</span></span>                   |
| <span data-ttu-id="b72b3-187">Getrequierungen</span><span class="sxs-lookup"><span data-stu-id="b72b3-187">GetRequirements</span></span>      | <span data-ttu-id="b72b3-188">Identifiziert eine benutzerfreundliche, lokalisierte Beschreibung der Mindestanforderungen für einen benutzerdefinierten Protokollhandler.</span><span class="sxs-lookup"><span data-stu-id="b72b3-188">Identifies a user-friendly, localized description of minimum requirements for a custom protocol handler</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="b72b3-189">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="b72b3-189">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="b72b3-190">**Referenz**</span><span class="sxs-lookup"><span data-stu-id="b72b3-190">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="b72b3-191">Benachrichtigen des Index von Änderungen</span><span class="sxs-lookup"><span data-stu-id="b72b3-191">Notifying the Index of Changes</span></span>](-search-2x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="b72b3-192">Hinzufügen von Symbolen, Vorschauen und Kontextmenüs mit Shellerweiterungen</span><span class="sxs-lookup"><span data-stu-id="b72b3-192">Adding Icons, Previews, and Context Menus with Shell Extensions</span></span>](-search-2x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="b72b3-193">Installieren und Registrieren von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="b72b3-193">Installing and Registering Protocol Handlers</span></span>](-search-2x-wds-ph-install-registration.md)
</dt> </dl>

 

 