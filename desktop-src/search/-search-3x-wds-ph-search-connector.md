---
description: Windows-Explorer steuert die Erstellung eines Suchconnector für einen Protokollhandler über Registrierungsschlüssel Einträge. Durch die Registrierung können sowohl Implementierer als auch Drittanbieter neue und ältere Protokollhandler für die Teilnahme an der Windows 7-Suche aktivieren.
ms.assetid: 79abdcbc-ba60-43bd-9895-18ee8b6c5829
title: Erstellen eines Suchconnector für einen Protokoll Handler
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57b43fd7eac53ca2c89d6c8b0d2cd36fd813e63a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128597"
---
# <a name="creating-a-search-connector-for-a-protocol-handler"></a><span data-ttu-id="d3ae5-104">Erstellen eines Suchconnector für einen Protokoll Handler</span><span class="sxs-lookup"><span data-stu-id="d3ae5-104">Creating a Search Connector for a Protocol Handler</span></span>

<span data-ttu-id="d3ae5-105">Windows-Explorer steuert die Erstellung eines Suchconnector für einen Protokollhandler über Registrierungsschlüssel Einträge.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-105">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries.</span></span> <span data-ttu-id="d3ae5-106">Durch die Registrierung können sowohl Implementierer als auch Drittanbieter neue und ältere Protokollhandler für die Teilnahme an der Windows 7-Suche aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-106">Through the registry both implementers and third parties can enable new and legacy protocol handlers to participate in Windows 7 Search.</span></span>

<span data-ttu-id="d3ae5-107">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="d3ae5-107">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="d3ae5-108">Informationen zu Suchconnectors für Protokollhandler in Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3ae5-108">About Search Connectors for Protocol Handlers in Windows 7</span></span>](#about-search-connectors-for-protocol-handlers-in-windows-7)
-   [<span data-ttu-id="d3ae5-109">Aktivieren von Protokoll Handlern für die Teilnahme an der Suche</span><span class="sxs-lookup"><span data-stu-id="d3ae5-109">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
    -   [<span data-ttu-id="d3ae5-110">Der Suchconnector für die Protokoll Handler-Suche wird deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-110">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
    -   [<span data-ttu-id="d3ae5-111">Anpassen des Namens, der Beschreibung oder des foldertype für einen protokollhandlersuchconnector</span><span class="sxs-lookup"><span data-stu-id="d3ae5-111">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
    -   [<span data-ttu-id="d3ae5-112">Verwenden von Registrierungs Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="d3ae5-112">Using Registry String Redirection</span></span>](#using-registry-string-redirection)
    -   [<span data-ttu-id="d3ae5-113">Wiederherstellen eines gelöschten Suchconnector für Protokoll Handler</span><span class="sxs-lookup"><span data-stu-id="d3ae5-113">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)
-   [<span data-ttu-id="d3ae5-114">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3ae5-114">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="d3ae5-115">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3ae5-115">Related topics</span></span>](#related-topics)

## <a name="about-search-connectors-for-protocol-handlers-in-windows-7"></a><span data-ttu-id="d3ae5-116">Informationen zu Suchconnectors für Protokollhandler in Windows 7</span><span class="sxs-lookup"><span data-stu-id="d3ae5-116">About Search Connectors for Protocol Handlers in Windows 7</span></span>

<span data-ttu-id="d3ae5-117">In Windows 7 enthalten Suchvorgänge im **Startmenü** oder im Windows-Explorer nur Dateien an indizierten Speicherorten und nicht Dateisystem Elemente, wie z. b. Remote Datenspeicher oder protokollhandlerelemente, die über einen Suchconnector verfügen.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-117">In Windows 7, searches from the **Start** menu or Windows Explorer include only files in indexed locations, and non-file system items such as remote data stores or protocol handler items that have a search connector.</span></span> <span data-ttu-id="d3ae5-118">Der Suchconnector ermöglicht nicht nur die protokollhandlerelemente im Bereich von **Startmenü** und shellsuchvorgängen, sondern auch das **Startmenü** , um protokollhandlerelemente in den Ergebnissen des **Start** Menüs zu gruppieren. Dies hat den Vorteil, dass der Benutzer auf den Gruppen Header klicken und Ergebnisse nur aus dem Protokollhandler anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-118">In addition to including the protocol handler items in the scope of **Start** menu and Shell searches, the search connector enables the **Start** menu to group protocol handler items together in **Start** menu results, with the resulting benefit that the user can click the group header and view results from only the protocol handler.</span></span> <span data-ttu-id="d3ae5-119">Alternativ kann der Benutzer zum Ordner **Suchen** navigieren, die Suchconnector-Datei öffnen und eine Suche durchführen, die nur Elemente aus dem spezifischen Protokollhandler enthält, der diesem Suchconnector zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-119">Alternatively, the user can navigate to the **Searches** folder, open the search connector file, and perform a search that includes only items from the specific protocol handler associated with that search connector.</span></span>

<span data-ttu-id="d3ae5-120">Wenn ein Benutzer eine Anwendung startet, die einen Protokollhandler registriert, generiert Windows Explorer eine Suchconnector-Datei (. searchconnector-MS) für den Protokollhandler im Ordner " **Such** Vorgänge" des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-120">When a user first starts an application that registers a protocol handler, Windows Explorer generates a search connector file (.searchConnector-ms) for the protocol handler in the user's **Searches** folder.</span></span> <span data-ttu-id="d3ae5-121">Anwendungen mit Protokoll Handlern können dieses Verhalten deaktivieren oder den Namen und die Beschreibung des suchverbindungs-Connector für den Protokollhandler anpassen.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-121">Applications with protocol handlers can choose to disable this behavior or customize the name and description of the protocol handler search connector.</span></span>

> [!Note]  
> <span data-ttu-id="d3ae5-122">Der Speicherort des **Such** Ordners des Benutzers lautet "% User Profile% \\ Suchen" oder "folderid \_ savedsuchen".</span><span class="sxs-lookup"><span data-stu-id="d3ae5-122">The location of the user's **Searches** folder is %userprofile%\\Searches, or FOLDERID\_SavedSearches.</span></span> <span data-ttu-id="d3ae5-123">Die GUID für folderid \_ savedsuchen ist {7d1d3a04-Debb-4115-95cf-2f29da2920da}.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-123">The GUID for FOLDERID\_SavedSearches is {7d1d3a04-debb-4115-95cf-2f29da2920da}.</span></span>

 

<span data-ttu-id="d3ae5-124">Windows-Explorer steuert die Erstellung eines Suchconnector für einen Protokollhandler über Registrierungsschlüssel Einträge, die in den folgenden Abschnitten beschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="d3ae5-124">Windows Explorer controls the creation of a search connector for a protocol handler through registry key entries described in the following sections:</span></span>

-   [<span data-ttu-id="d3ae5-125">Aktivieren von Protokoll Handlern für die Teilnahme an der Suche</span><span class="sxs-lookup"><span data-stu-id="d3ae5-125">Enabling Protocol Handlers to Participate in Search</span></span>](#enabling-protocol-handlers-to-participate-in-search)
-   [<span data-ttu-id="d3ae5-126">Der Suchconnector für die Protokoll Handler-Suche wird deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-126">Disabling Protocol Handler Search Connector Creation</span></span>](#disabling-protocol-handler-search-connector-creation)
-   [<span data-ttu-id="d3ae5-127">Anpassen des Namens, der Beschreibung oder des foldertype für einen protokollhandlersuchconnector</span><span class="sxs-lookup"><span data-stu-id="d3ae5-127">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>](#customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector)
-   [<span data-ttu-id="d3ae5-128">Wiederherstellen eines gelöschten Suchconnector für Protokoll Handler</span><span class="sxs-lookup"><span data-stu-id="d3ae5-128">Restoring a Deleted Protocol Handler Search Connector</span></span>](#restoring-a-deleted-protocol-handler-search-connector)

> [!Note]  
> <span data-ttu-id="d3ae5-129">Es gibt keine programmatischen Möglichkeiten, einen Suchconnector für einen Protokollhandler zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-129">There are no programmatic means to create a search connector for a protocol handler.</span></span> <span data-ttu-id="d3ae5-130">Sie müssen über die Registrierung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-130">They must be configured through the registry.</span></span>

 

## <a name="enabling-protocol-handlers-to-participate-in-search"></a><span data-ttu-id="d3ae5-131">Aktivieren von Protokoll Handlern für die Teilnahme an der Suche</span><span class="sxs-lookup"><span data-stu-id="d3ae5-131">Enabling Protocol Handlers to Participate in Search</span></span>

<span data-ttu-id="d3ae5-132">Die Registrierungsschlüssel und die möglichen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-132">Registry keys and their possible values are outlined in the following table.</span></span> <span data-ttu-id="d3ae5-133">Ein Protokollhandler kann einige oder alle dieser Registrierungsschlüssel auffüllen, wobei Beispiels <protocol> Weise durch den tatsächlichen Namen des Protokolls ersetzt wird, z. b. MAPI, File oder csc.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-133">A protocol handler can populate some or all of these registry keys where <protocol> is replaced with the actual name of its protocol, such as MAPI, file, or csc, for example.</span></span>



| <span data-ttu-id="d3ae5-134">Registrierungsschlüssel</span><span class="sxs-lookup"><span data-stu-id="d3ae5-134">Registry key</span></span>                                                                                                                 | <span data-ttu-id="d3ae5-135">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="d3ae5-135">Possible value(s)</span></span>                                                                                                                     | <span data-ttu-id="d3ae5-136">Typ</span><span class="sxs-lookup"><span data-stu-id="d3ae5-136">Type</span></span>       | <span data-ttu-id="d3ae5-137">Kommentare</span><span class="sxs-lookup"><span data-stu-id="d3ae5-137">Comments</span></span>                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d3ae5-138">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Search \\ phsearchconnectors- \\ <protocol> \\ Version</span><span class="sxs-lookup"><span data-stu-id="d3ae5-138">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Version</span></span>                     | <span data-ttu-id="d3ae5-139">Ist nicht vorhanden (Standard).</span><span class="sxs-lookup"><span data-stu-id="d3ae5-139">Does not exist (default).</span></span> <span data-ttu-id="d3ae5-140">Andernfalls ist Sie 1 oder größer.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-140">Otherwise it is 1 or greater.</span></span>                                                                               | <span data-ttu-id="d3ae5-141">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="d3ae5-141">REG\_DWORD</span></span> | <span data-ttu-id="d3ae5-142">Dieser Wert wird verwendet, um Änderungen an den Speicherort Vorlagen Registrierungen für Such Stämme zu erkennen, die bereits verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-142">This value is used to detect changes to the location template registrations for search roots that have already been processed.</span></span> <span data-ttu-id="d3ae5-143">Wenn nicht vorhanden ist, verwenden Sie 0 als Standardwert.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-143">If does not exist, use 0 as a default.</span></span> <span data-ttu-id="d3ae5-144">Sie können auch die Version erhöhen, um Windows-Explorer darüber zu informieren, dass der Suchconnector neu generiert werden soll, weil eine neuere Version des Protokoll Handlers installiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-144">Alternatively, increment the version to inform Windows Explorer that the search connector should be regenerated because a newer version of the protocol handler has been installed.</span></span> |
| <span data-ttu-id="d3ae5-145">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Search \\ phsearchconnectors \\ <protocol> \\ donotkreatesearchconnectors</span><span class="sxs-lookup"><span data-stu-id="d3ae5-145">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\DoNotCreateSearchConnectors</span></span> | <span data-ttu-id="d3ae5-146">Ist nicht vorhanden (Standard).</span><span class="sxs-lookup"><span data-stu-id="d3ae5-146">Does not exist (default).</span></span> <span data-ttu-id="d3ae5-147">Andernfalls auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-147">Otherwise set to 1.</span></span>                                                                                         | <span data-ttu-id="d3ae5-148">REG \_ DWORD</span><span class="sxs-lookup"><span data-stu-id="d3ae5-148">REG\_DWORD</span></span> | <span data-ttu-id="d3ae5-149">Wenn Sie nicht vorhanden ist, erstellen Sie eine searchconnector-MS-Datei im Ordner "Suchvorgänge".</span><span class="sxs-lookup"><span data-stu-id="d3ae5-149">If it does not exist, create a .searchconnector-ms file in the Searches folder.</span></span> <span data-ttu-id="d3ae5-150">Wenn 1, markieren Sie als verarbeitet, und führen Sie nichts aus.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-150">If 1, mark as processed and do nothing.</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="d3ae5-151">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Search \\ \\ <protocol> \\ Standard \\ Beschreibung von "phsearchconnectors"</span><span class="sxs-lookup"><span data-stu-id="d3ae5-151">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Description</span></span>        | <span data-ttu-id="d3ae5-152">Eine lokalisierbare Zeichenfolge, die die Beschreibung des Suchconnector enthält.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-152">A localizable string containing the description of the search connector.</span></span>                                                              | <span data-ttu-id="d3ae5-153">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d3ae5-153">REG\_SZ</span></span>    | <span data-ttu-id="d3ae5-154">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-154">Optional.</span></span> <span data-ttu-id="d3ae5-155">Sie wird im Description-Element der. searchconnector-MS-Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-155">It is used in the Description element of the .searchconnector-ms file.</span></span>                                                                                                                                                                                                                                                                          |
| <span data-ttu-id="d3ae5-156">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Search \\ \\ <protocol> \\ Standard Name für Standard \\ Name</span><span class="sxs-lookup"><span data-stu-id="d3ae5-156">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\Name</span></span>               | <span data-ttu-id="d3ae5-157">Eine lokalisierte Zeichenfolge, um den Suchconnector zu benennen.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-157">A localized string to name the search connector.</span></span> <span data-ttu-id="d3ae5-158">Wird als Name der. searchconnector-MS-Datei verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-158">Used as the name of the .searchconnector-ms file.</span></span>                                    | <span data-ttu-id="d3ae5-159">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d3ae5-159">REG\_SZ</span></span>    | <span data-ttu-id="d3ae5-160">Jeder Speicherort muss einen eindeutigen Namen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-160">Each location must have a unique name.</span></span> <span data-ttu-id="d3ae5-161">Wenn dieser Wert nicht vorhanden ist, wird der von der [IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) des Protokoll Handlers bereitgestellte Anzeige Name verwendet.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-161">In the absence of this value, the display name provided by the protocol handler's [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) will be used.</span></span>                                                                                                                             |
| <span data-ttu-id="d3ae5-162">HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Search \\ \\ <protocol> \\ Standard \\ foldertype</span><span class="sxs-lookup"><span data-stu-id="d3ae5-162">HKEY\_LOCAL\_MACHINE\\Software\\Microsoft\\Windows Search\\PHSearchConnectors\\<protocol>\\Default\\FolderType</span></span>         | <span data-ttu-id="d3ae5-163">Eine GUID, die die [foldertypeid](../shell/foldertypeid.md) identifiziert, die auf den Suchconnector angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-163">A GUID identifying the [FOLDERTYPEID](../shell/foldertypeid.md) to apply to the search connector.</span></span> | <span data-ttu-id="d3ae5-164">REG- \_ SZ</span><span class="sxs-lookup"><span data-stu-id="d3ae5-164">REG\_SZ</span></span>    | <span data-ttu-id="d3ae5-165">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-165">Optional.</span></span> <span data-ttu-id="d3ae5-166">Wird im foldertype-Element der. searchconnector-MS-Datei verwendet, um anzugeben, welche Vorlagen zum Anzeigen von Ergebnissen verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-166">Used in the folderType element of the .searchconnector-ms file to indicate what templates should be used to display results.</span></span> <span data-ttu-id="d3ae5-167">Beispielsweise der GUID-Wert von foldertypeid- \_ Dokumenten.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-167">For example, the GUID value of FOLDERTYPEID\_Documents.</span></span>                                                                                                                                                            |



 

### <a name="disabling-protocol-handler-search-connector-creation"></a><span data-ttu-id="d3ae5-168">Der Suchconnector für die Protokoll Handler-Suche wird deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-168">Disabling Protocol Handler Search Connector Creation</span></span>

<span data-ttu-id="d3ae5-169">Wenn Ihre Anwendung Elemente über einen Protokollhandler zur Verwendung in der Anwendung selbst verfügbar macht und Sie die Elemente nicht über die Shell (im **Startmenü** und in Windows Explorer-suchen) verfügbar machen möchten, müssen Sie die Erstellung eines Suchconnector für Ihren Protokollhandler deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-169">If your application exposes items through a protocol handler for use in the application itself and you do not want to expose the items through the Shell (in **Start** menu and Windows Explorer searches), you need to disable the creation of a search connector for your protocol handler.</span></span>

<span data-ttu-id="d3ae5-170">Wenn Sie die suchconnectorerstellung deaktivieren möchten, legen Sie donotkreatesearchconnectors auf 0x00000001 (1) fest, wie im folgenden Beispiel für den Registrierungsschlüssel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-170">To disable search connector creation set DoNotCreateSearchConnectors to 0x00000001(1), as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  DoNotCreateSearchConnectors
```

<span data-ttu-id="d3ae5-171">Wenn donotkreatesearchconnectors auf 1 festgelegt ist, wird empfohlen, die [System. Shell. omitfromview](/windows/desktop/properties/props-system-shell-omitfromview) -Eigenschaft für jedes Element verfügbar zu machen, das vom Protokollhandler verfügbar gemacht wird, und den Wert dieser Eigenschaft auf **true** festzulegen.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-171">If DoNotCreateSearchConnectors is set to 1, then we recommend that you expose the [System.Shell.OmitFromView](/windows/desktop/properties/props-system-shell-omitfromview) property on each item exposed by the protocol handler, and set the value of this property to **TRUE**.</span></span> <span data-ttu-id="d3ae5-172">Dadurch wird verhindert, dass die protokollhandlerelemente unter der **Datei** Gruppe " **Startmenü** " angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-172">Doing so will prevent the protocol handler items from appearing under the **Start** menu **Files** group.</span></span>

<span data-ttu-id="d3ae5-173">Wenn donotkreatesearchconnectors vorhanden und auf 0 (null) festgelegt ist, erstellt Windows-Explorer einen Suchconnector für den Protokollhandler, und die protokollhandlerelemente werden im **Startmenü** und in Windows Explorer-suchen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-173">If DoNotCreateSearchConnectors is present and set to zero, then Windows Explorer will create a search connector for the protocol handler, and the protocol handler items will be returned in in **Start** menu and Windows Explorer searches.</span></span>

### <a name="customizing-the-name-description-or-foldertype-for-a-protocol-handler-search-connector"></a><span data-ttu-id="d3ae5-174">Anpassen des Namens, der Beschreibung oder des foldertype für einen protokollhandlersuchconnector</span><span class="sxs-lookup"><span data-stu-id="d3ae5-174">Customizing the Name, Description or FolderType for a Protocol Handler Search Connector</span></span>

<span data-ttu-id="d3ae5-175">Der suchconnectorname wird nicht nur verwendet, um den Suchconnector im **Suchordner zu** identifizieren, sondern als Gruppen Kopfzeile für die Ergebnisse im **Startmenü** .</span><span class="sxs-lookup"><span data-stu-id="d3ae5-175">The search connector name is used not only to identify the search connector in the **Searches** folder, but as the group header for the results in **Start** menu searches.</span></span> <span data-ttu-id="d3ae5-176">Daher ist es wichtig, einen beschreibenden Namen für den Suchconnector bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-176">Hence, it is important to provide a descriptive name for the search connector.</span></span> <span data-ttu-id="d3ae5-177">Wenn im Registrierungsschlüssel kein Name angegeben ist, verwendet Windows Explorer standardmäßig den von der [IShellFolder-Schnittstelle](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) bereitgestellten Namen für den Such Stamm des Protokoll Handlers und die leere Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-177">If a name is not provided in the registry key, by default Windows Explorer uses the name provided by [IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) for the protocol handler's search root and blank description.</span></span> <span data-ttu-id="d3ae5-178">Sie können den Standardnamen über einen Registrierungsschlüssel Eintrag überschreiben, ohne die IShellFolder-Schnittstelle Umbenennen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-178">You can override the default name through a registry key entry without having to rename the IShellFolder Interface.</span></span> <span data-ttu-id="d3ae5-179">Obwohl Sie nicht so sichtbar wie der Suchconnector-Name ist, können Sie die Beschreibung für den Suchconnector auch überschreiben, indem Sie eine eigene Beschreibung angeben.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-179">Although it is not as visible as the search connector name, you can also override the description for the search connector by providing your own description.</span></span>

<span data-ttu-id="d3ae5-180">Wenn Sie den Standardnamen oder die Beschreibung überschreiben möchten, legen Sie die Einträge wie im folgenden Registrierungs Beispiel dargestellt fest.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-180">To override the default name or description, set the entries as shown in the following registry example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     Name
                     Description
```

<span data-ttu-id="d3ae5-181">Außerdem kann der foldertype-Eintrag auf eine der [foldertypeid](../shell/foldertypeid.md) -GUIDs festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-181">In addition, the FolderType entry can be set to one of the [FOLDERTYPEID](../shell/foldertypeid.md) GUIDs.</span></span> <span data-ttu-id="d3ae5-182">Der Wert muss die tatsächliche GUID und nicht sein Name sein.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-182">The value should be the actual GUID, and not its name.</span></span> <span data-ttu-id="d3ae5-183">Beispiel: {94d6ddcc-4a68-4175-A374-bd584a510 B78} anstelle von foldertypeid \_ Music.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-183">For example, {94d6ddcc-4a68-4175-a374-bd584a510b78} rather than FOLDERTYPEID\_Music.</span></span> <span data-ttu-id="d3ae5-184">Die GUID für eine foldertypeid kann in der Header Datei "shlguid. h" im [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx)abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-184">The GUID for a FOLDERTYPEID can be obtained in the Shlguid.h header file in the [Windows SDK](https://msdn.microsoft.com/windowsvista/bb980924.aspx).</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Default
                     FolderType = {94d6ddcc-4a68-4175-a374-bd584a510b78}
```

### <a name="using-registry-string-redirection"></a><span data-ttu-id="d3ae5-185">Verwenden von Registrierungs Zeichenfolgen</span><span class="sxs-lookup"><span data-stu-id="d3ae5-185">Using Registry String Redirection</span></span>

<span data-ttu-id="d3ae5-186">Sie können eine [umgeleitete Zeichenfolge](../intl/using-registry-string-redirection.md) verwenden, um sicherzustellen, dass der von Ihnen für den Suchconnector bereitgestellte Name lokalisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-186">You can use a [redirected string](../intl/using-registry-string-redirection.md) to ensure that the name you provide for the search connector can be localized.</span></span> <span data-ttu-id="d3ae5-187">Sie können lokalisierbare Zeichen folgen für die Registrierungsschlüssel Name und Beschreibung einschließen, anstatt die tatsächliche Zeichenfolge in die Registrierung einzugeben.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-187">You can include localizable strings for the name and description registry keys instead of entering the actual string into the registry.</span></span>

<span data-ttu-id="d3ae5-188">Wenn Sie eine lokalisierbare Zeichenfolge für den Namen oder die Beschreibungs Werte einschließen möchten, legen Sie den Wert wie im folgenden Beispiel für den Registrierungsschlüssel gezeigt fest</span><span class="sxs-lookup"><span data-stu-id="d3ae5-188">To include a localizable string for the Name or Description values, set the value as shown in the following registry key example.</span></span>

```
HKEY_LOCAL_MACHINE
   Software
      Microsoft
         Windows Search
            PHSearchConnectors
               <protocol>
                  Name = @dllname.dll,-resourceID
```

<span data-ttu-id="d3ae5-189">Die lokalisierbare Zeichenfolge hat das folgende Format:</span><span class="sxs-lookup"><span data-stu-id="d3ae5-189">The localizable string takes the following format:</span></span>

-   <span data-ttu-id="d3ae5-190">@dllname.dll,-ResourceID, wobei:</span><span class="sxs-lookup"><span data-stu-id="d3ae5-190">@dllname.dll,-resourceID, where:</span></span>
    -   <span data-ttu-id="d3ae5-191">@dllname.dll der Pfad zu der dll, die die Zeichen folgen Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-191">@dllname.dll is the path to the DLL that contains the string resource</span></span>
    -   <span data-ttu-id="d3ae5-192">ResourceId ist die ganzzahlige Ressourcen-ID der Zeichen folgen Ressource.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-192">resourceID is the integer resource ID of the string resource</span></span>

<span data-ttu-id="d3ae5-193">Das Format für eine indirekte Zeichenfolge und eine indirekte Zeichenfolge, die mit einem versionsmodifizierer angehängt wird, werden in der [shloadderetstring-Funktion](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-193">The format for an indirect string, and an indirect string appended with a version modifier, is described in [SHLoadIndirectString Function](/windows/win32/api/shlwapi/nf-shlwapi-shloadindirectstring).</span></span>

### <a name="restoring-a-deleted-protocol-handler-search-connector"></a><span data-ttu-id="d3ae5-194">Wiederherstellen eines gelöschten Suchconnector für Protokoll Handler</span><span class="sxs-lookup"><span data-stu-id="d3ae5-194">Restoring a Deleted Protocol Handler Search Connector</span></span>

<span data-ttu-id="d3ae5-195">Da Suchconnectors Dateien auf dem Computer des Benutzers sind, können Sie versehentlich gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-195">Because search connectors are files on the user's computer, they can be mistakenly deleted.</span></span> <span data-ttu-id="d3ae5-196">Um alle gelöschten Suchconnectors für Protokollhandler wiederherzustellen, stellen Sie die Standardbibliotheken wieder her.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-196">To restore all deleted protocol handler search connectors, restore the default libraries.</span></span> <span data-ttu-id="d3ae5-197">Öffnen Sie hierzu Windows-Explorer, klicken Sie mit der rechten Maustaste auf den Ordner **Bibliotheken** , und wählen Sie dann **Standardbibliotheken wiederherstellen** aus.</span><span class="sxs-lookup"><span data-stu-id="d3ae5-197">To so do, open Windows Explorer, right-click the **Libraries** folder, and then select **Restore Default Libraries**.</span></span>

![Screenshot mit der Menüoption "Standardbibliotheken wiederherstellen"](images/libraries.png)

## <a name="additional-resources"></a><span data-ttu-id="d3ae5-199">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="d3ae5-199">Additional Resources</span></span>

-   [<span data-ttu-id="d3ae5-200">IShellItem:: GetDisplayName</span><span class="sxs-lookup"><span data-stu-id="d3ae5-200">IShellItem::GetDisplayName</span></span>](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellitem-getdisplayname)
-   [<span data-ttu-id="d3ae5-201">Signatur- \_ Normal Anzeige</span><span class="sxs-lookup"><span data-stu-id="d3ae5-201">SIGDN\_NORMALDISPLAY</span></span>](/windows/win32/api/shobjidl_core/ne-shobjidl_core-sigdn)

## <a name="related-topics"></a><span data-ttu-id="d3ae5-202">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="d3ae5-202">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="d3ae5-203">**Licher**</span><span class="sxs-lookup"><span data-stu-id="d3ae5-203">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="d3ae5-204">Grundlegendes zu Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="d3ae5-204">Understanding Protocol Handlers</span></span>](-search-3x-wds-extidx-prot-implementing.md)
</dt> <dt>

[<span data-ttu-id="d3ae5-205">Entwickeln von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="d3ae5-205">Developing Protocol Handlers</span></span>](-search-3x-wds-phaddins.md)
</dt> <dt>

[<span data-ttu-id="d3ae5-206">Benachrichtigen des Index von Änderungen</span><span class="sxs-lookup"><span data-stu-id="d3ae5-206">Notifying the Index of Changes</span></span>](-search-3x-wds-notifyingofchanges.md)
</dt> <dt>

[<span data-ttu-id="d3ae5-207">Hinzufügen von Symbolen und Kontextmenüs</span><span class="sxs-lookup"><span data-stu-id="d3ae5-207">Adding Icons and Context Menus</span></span>](-search-3x-wds-ph-ui-extensions.md)
</dt> <dt>

[<span data-ttu-id="d3ae5-208">Code Beispiel: Shellerweiterungen für Protokollhandler</span><span class="sxs-lookup"><span data-stu-id="d3ae5-208">Code Sample: Shell Extensions for Protocol Handlers</span></span>](-search-3x-wds-ph-ui-samplecode.md)
</dt> <dt>

[<span data-ttu-id="d3ae5-209">Installieren und Registrieren von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="d3ae5-209">Installing and Registering Protocol Handlers</span></span>](-search-3x-wds-ph-install-registration.md)
</dt> <dt>

[<span data-ttu-id="d3ae5-210">Debuggen von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="d3ae5-210">Debugging Protocol Handlers</span></span>](-search-ws-protocolhandlertesting.md)
</dt> </dl>

 

 
