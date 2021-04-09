---
description: Eine ganzzahlige Vorgehensweise beim Testen und Debuggen Ihrer protokollhandlerimplementierungen ist das Verständnis der Art und Weise
ms.assetid: 33c99620-7381-4719-9fc6-4c8284481411
title: Debuggen von Protokoll Handlern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 321d59c0c7915f9bbf84a80091408ba88a9a75ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128516"
---
# <a name="debugging-protocol-handlers"></a><span data-ttu-id="f2fd5-103">Debuggen von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="f2fd5-103">Debugging Protocol Handlers</span></span>

<span data-ttu-id="f2fd5-104">Eine ganzzahlige Vorgehensweise beim Testen und Debuggen Ihrer protokollhandlerimplementierungen ist das Verständnis der Art und Weise</span><span class="sxs-lookup"><span data-stu-id="f2fd5-104">Integral to testing and debugging your protocol handler implementations is understanding how protocol handlers are launched.</span></span>

<span data-ttu-id="f2fd5-105">Dieses Thema ist wie folgt organisiert:</span><span class="sxs-lookup"><span data-stu-id="f2fd5-105">This topic is organized as follows:</span></span>

-   [<span data-ttu-id="f2fd5-106">Informationen zum Debugging von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="f2fd5-106">About Debugging Protocol Handlers</span></span>](#about-debugging-protocol-handlers)
-   [<span data-ttu-id="f2fd5-107">Einrichten des Debuggens</span><span class="sxs-lookup"><span data-stu-id="f2fd5-107">Setting Up Debugging</span></span>](#setting-up-debugging)
-   [<span data-ttu-id="f2fd5-108">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f2fd5-108">Additional Resources</span></span>](#additional-resources)
-   [<span data-ttu-id="f2fd5-109">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2fd5-109">Related topics</span></span>](#related-topics)

## <a name="about-debugging-protocol-handlers"></a><span data-ttu-id="f2fd5-110">Informationen zum Debugging von Protokoll Handlern</span><span class="sxs-lookup"><span data-stu-id="f2fd5-110">About Debugging Protocol Handlers</span></span>

<span data-ttu-id="f2fd5-111">Der SearchIndexer-Prozess (searchindexer.exe) beginnt eine Kopie des SearchProtocolHost-Prozesses (SearchProtocolHost.exe) im Systemkontext und eine weitere Kopie im Benutzer Kontext.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-111">The SearchIndexer process (searchindexer.exe) launches one copy of the SearchProtocolHost process (SearchProtocolHost.exe) in the system context and another copy in the user context.</span></span> <span data-ttu-id="f2fd5-112">Anschließend werden die Protokollhandler nach Bedarf in den SearchProtocolHost-Prozess geladen.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-112">Then, the protocol handlers are loaded in the SearchProtocolHost process as needed.</span></span> <span data-ttu-id="f2fd5-113">Sie werden erst entladen, wenn der Suchdienst beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-113">They are not unloaded until the search service is stopped.</span></span> <span data-ttu-id="f2fd5-114">Dieselbe Instanz eines Protokoll Handlers wird beliebig oft wieder verwendet, während der Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-114">The same instance of a protocol handler is reused any number of times while the service is running.</span></span>

<span data-ttu-id="f2fd5-115">Die SearchIndexer-und SearchProtocolHost-Prozesse kommunizieren häufig während der Indizierung.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-115">The SearchIndexer and SearchProtocolHost processes communicate frequently during indexing.</span></span> <span data-ttu-id="f2fd5-116">Wenn Sie den Prozess zum Debuggen von SearchProtocolHost anhalten oder anhalten, startet der SearchIndexer einen neuen SearchProtocolHost-Prozess, wodurch Ihre Debuggingsitzung ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-116">If you pause or stop the SearchProtocolHost process to debug, the SearchIndexer will launch a new SearchProtocolHost process, invalidating your debugging session.</span></span> <span data-ttu-id="f2fd5-117">Wenn Sie den Debugger direkt an den SearchProtocolHost-Prozess anfügen, können Sie die Handle-Vererbung von searchindexer.exe zu searchprotocolhost.exe unterbrechen, und die beiden Prozesse können nicht miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-117">Also, if you attach your debugger directly to the SearchProtocolHost process, you can break handle-inheritance from searchindexer.exe to searchprotocolhost.exe, and the two processes will be unable to communicate.</span></span>

<span data-ttu-id="f2fd5-118">Um diese Probleme zu vermeiden, müssen Sie den Suchdienst Benachrichtigen, den Sie Debuggen, und Sie müssen den Debugger an den SearchIndexer-Prozess anfügen, um die untergeordneten Prozesse wie im folgenden beschrieben zu debuggen.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-118">To avoid these problems, you need to notify the search service that you are debugging, and you need to attach the debugger to the SearchIndexer process with instructions to debug child processes, as described next.</span></span>

## <a name="setting-up-debugging"></a><span data-ttu-id="f2fd5-119">Einrichten des Debuggens</span><span class="sxs-lookup"><span data-stu-id="f2fd5-119">Setting Up Debugging</span></span>

<span data-ttu-id="f2fd5-120">Führen Sie die folgenden Schritte aus, um das Debuggen für Ihren Protokollhandler einzurichten.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-120">Follow these steps to set up debugging for your protocol handler.</span></span>

1.  <span data-ttu-id="f2fd5-121">Benachrichtigen Sie den Search-Dienst, den Sie Debuggen, indem Sie den debugfilters-Wert in der Registrierung auf 1 festlegen:</span><span class="sxs-lookup"><span data-stu-id="f2fd5-121">Notify the search service that you are debugging by setting the DebugFilters value to 1 in the registry:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft
       Windows Search
          Gathering Manager
             DebugFilters = 1
    ```

2.  <span data-ttu-id="f2fd5-122">Fügen Sie einen Debugger mit dem Registrierungsschlüssel für die Bild Datei Ausführungs Optionen an:</span><span class="sxs-lookup"><span data-stu-id="f2fd5-122">Attach a debugger using the Image File Execution Options registry key:</span></span>

    ```
    HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Windows NT\CurrentVersion
       Image File Execution Options
          SearchIndexer.exe
             Debugger = <path to debugger> <debugger options> 
    ```

    <span data-ttu-id="f2fd5-123">Die Optionen für einen Beispiel Debugger werden in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-123">The options for a sample debugger are described in the following table.</span></span>

    

    <span data-ttu-id="f2fd5-124">**Beispiel für die Verwendung des NGS-Debugger-**   *Debugger = C: Debugger \\ \\ntsd.exe-odgx-C: "sxe ld mydll.dll; g"*</span><span class="sxs-lookup"><span data-stu-id="f2fd5-124">**Example using the ntsd debugger**   *Debugger = C:\\debuggers\\ntsd.exe -odGx -c: "sxe ld mydll.dll;g"*</span></span><br/>

3.  <span data-ttu-id="f2fd5-125">Starten Sie searchindexer.exe unter dem Debugger mithilfe von "compmgmt. msc", "Services. msc" oder einem Befehlsfenster mit Befehlen ähnlich den folgenden:</span><span class="sxs-lookup"><span data-stu-id="f2fd5-125">Restart searchindexer.exe under the debugger using compmgmt.msc, services.msc, or a command window with commands similar to the following:</span></span>
    ```
    net stop wsearch
    <copy new DLLs for debugging>
    net start wsearch
            
    ```

    

<span data-ttu-id="f2fd5-126">Um zwischen einem im Systemkontext laufenden SearchProtocolHost-Prozess und einem im Benutzer Kontext laufenden Prozess zu unterscheiden, können Sie die Umgebungs Zeichenfolgen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-126">To distinguish between a SearchProtocolHost process running in the system context and one running in the user context, you can review the environment strings.</span></span> <span data-ttu-id="f2fd5-127">Mit ntsd.exe können Sie z. b. den Erweiterungs Befehl " **!** " verwenden, um eine formatierte Ansicht der Informationen im Process Environment Block (-Peer) anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f2fd5-127">With ntsd.exe, for example, you can use extension command **!peb** to display a formatted view of the information in the process environment block (PEB).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f2fd5-128">Weitere Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f2fd5-128">Additional Resources</span></span>

-   <span data-ttu-id="f2fd5-129">Weitere Informationen zum Erstellen von Handlern finden Sie unter [Registrieren von Shellerweiterungen](../shell/reg-shell-exts.md).</span><span class="sxs-lookup"><span data-stu-id="f2fd5-129">For information on creating handlers, see [Registering Shell Extensions](../shell/reg-shell-exts.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="f2fd5-130">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="f2fd5-130">Related topics</span></span>

<dl> <span data-ttu-id="f2fd5-131"><dt>**Konzeptionelle**</dt> <dt><a href="-search-3x-wds-phaddins.md">Entwicklung von Protokoll Handlern</a></dt> mit Informationen zu <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Protokoll Handlern</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">, die den Index von Änderungen beim</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Hinzufügen von Symbolen und Kontextmenüs</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">angeben Code Beispiel: Shellerweiterungen für Protokoll</a></dt> Handler <dt><a href="-search-3x-wds-ph-search-connector.md">Erstellen eines Suchconnector für einen Protokollhandler erstellen</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">und Registrieren von Protokoll Handlern</a></dt> </span><span class="sxs-lookup"><span data-stu-id="f2fd5-131"><dt>**Conceptual**</dt> <dt><a href="-search-3x-wds-phaddins.md">Developing Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-extidx-prot-implementing.md">Understanding Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-notifyingofchanges.md">Notifying the Index of Changes</a></dt> <dt><a href="-search-3x-wds-ph-ui-extensions.md">Adding Icons and Context Menus</a></dt> <dt><a href="-search-3x-wds-ph-ui-samplecode.md">Code Sample: Shell Extensions for Protocol Handlers</a></dt> <dt><a href="-search-3x-wds-ph-search-connector.md">Creating a Search Connector for a Protocol Handler</a></dt> <dt><a href="-search-3x-wds-ph-install-registration.md">Installing and Registering Protocol Handlers</a></dt> </span></span></dl>

 

 
