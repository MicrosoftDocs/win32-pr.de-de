---
description: Anpassen der Debugausgabe mit ID3D10InfoQueue (Direct3D 10)
ms.assetid: 082c7783-c53a-4b73-b8f2-3f60e2c2689a
title: Anpassen der Debugausgabe mit ID3D10InfoQueue (Direct3D 10)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 843ac7dd34b19cfe1fc7835a2026ae2dd28b9dcd
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041466"
---
# <a name="customize-debug-output-with-id3d10infoqueue-direct3d-10"></a><span data-ttu-id="43c36-103">Anpassen der Debugausgabe mit ID3D10InfoQueue (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="43c36-103">Customize Debug Output with ID3D10InfoQueue (Direct3D 10)</span></span>

<span data-ttu-id="43c36-104">Die Informations Warteschlange wird von einer Schnittstelle (siehe [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) verwaltet, die Debugmeldungen speichert, abruft und filtert.</span><span class="sxs-lookup"><span data-stu-id="43c36-104">The information queue is managed by an interface (see [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue)) that stores, retrieves, and filters debug messages.</span></span> <span data-ttu-id="43c36-105">Die Warteschlange besteht aus: einer Nachrichten Warteschlange, einem optionalen Speicher Filter Stapel und einem optionalen Abruf Filter Stapel.</span><span class="sxs-lookup"><span data-stu-id="43c36-105">The queue consists of: a message queue, an optional storage filter stack, and a optional retrieval filter stack.</span></span> <span data-ttu-id="43c36-106">Der Speicher Filter Stapel kann verwendet werden, um die Nachrichten zu filtern, die gespeichert werden sollen. der Abruf Filter Stapel kann verwendet werden, um die Nachrichten zu filtern, die gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="43c36-106">The storage-filter stack can be used to filter the messages you want stored; the retrieval-filter stack can be used to filter the messages you want stored.</span></span> <span data-ttu-id="43c36-107">Nachdem Sie eine Meldung gefiltert haben, wird die Nachricht im Debugfenster ausgegeben und im entsprechenden Stapel gespeichert.</span><span class="sxs-lookup"><span data-stu-id="43c36-107">Once you have filtered a message, the message will be printed out to the debug window and stored in the appropriate stack.</span></span>

<span data-ttu-id="43c36-108">Im Allgemeinen:</span><span class="sxs-lookup"><span data-stu-id="43c36-108">In general:</span></span>

-   <span data-ttu-id="43c36-109">Rufen Sie [**ID3D10InfoQueue:: addapplicationmessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) auf, um benutzerdefinierte Meldungen zu generieren.</span><span class="sxs-lookup"><span data-stu-id="43c36-109">Call [**ID3D10InfoQueue::AddApplicationMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addapplicationmessage) to generate user-defined messages</span></span>
-   <span data-ttu-id="43c36-110">Aufrufen von [**ID3D10InfoQueue:: getMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) dient zum Abrufen von Nachrichten (die einen optionalen Abruf Filter übergeben).</span><span class="sxs-lookup"><span data-stu-id="43c36-110">Call [**ID3D10InfoQueue::GetMessage**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-getmessage) is used to get messages (that pass an optional retrieval filter).</span></span>

## <a name="registry-controls"></a><span data-ttu-id="43c36-111">Registrierungs Steuerelemente</span><span class="sxs-lookup"><span data-stu-id="43c36-111">Registry Controls</span></span>

<span data-ttu-id="43c36-112">Verwenden Sie die Registrierungsschlüssel zum Anpassen von Filtereinstellungen, zum Anpassen von Breakpoints und zum stumm schalten der Debugausgabe.</span><span class="sxs-lookup"><span data-stu-id="43c36-112">Use registry keys to adjust filter settings, adjust break points, and to mute the debug output.</span></span> <span data-ttu-id="43c36-113">Die debugschicht prüft diese Pfade auf Registrierungsschlüssel. der erste gefundene Pfad wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="43c36-113">The debug layer will check these paths for registry keys; the first path found will be used.</span></span>

1.  <span data-ttu-id="43c36-114">HKCU \\ Software \\ Microsoft \\ Direct3D \\<benutzerdefinierter Unterschlüssel></span><span class="sxs-lookup"><span data-stu-id="43c36-114">HKCU\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
2.  <span data-ttu-id="43c36-115">HKLM \\ Software \\ Microsoft \\ Direct3D \\<benutzerdefinierter Unterschlüssel></span><span class="sxs-lookup"><span data-stu-id="43c36-115">HKLM\\Software\\Microsoft\\Direct3D\\<user-defined subkey></span></span>
3.  <span data-ttu-id="43c36-116">HKCU- \\ Software \\ Microsoft \\ Direct3D</span><span class="sxs-lookup"><span data-stu-id="43c36-116">HKCU\\Software\\Microsoft\\Direct3D</span></span>

<span data-ttu-id="43c36-117">Hierbei gilt:</span><span class="sxs-lookup"><span data-stu-id="43c36-117">Where:</span></span>

-   <span data-ttu-id="43c36-118">HKCU steht für HKEY \_ Current \_ User und HKLM für HKEY \_ local \_ Machine.</span><span class="sxs-lookup"><span data-stu-id="43c36-118">HKCU stand for HKEY\_CURRENT\_USER, and HKLM stand for HKEY\_LOCAL\_MACHINE.</span></span>
-   <span data-ttu-id="43c36-119"><benutzerdefinierter Unterschlüssel> ein beliebiger Name zum Speichern der Debugeinstellungen für eine Anwendung ist.</span><span class="sxs-lookup"><span data-stu-id="43c36-119"><user-defined subkey> is an arbitrary name to store debug settings for an application</span></span>

### <a name="filtering-debug-messages-using-registry-keys"></a><span data-ttu-id="43c36-120">Filtern von Debugmeldungen mithilfe von Registrierungs Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="43c36-120">Filtering Debug Messages using Registry Keys</span></span>

<span data-ttu-id="43c36-121">Wenn die Registrierung einen infoqueuestoragefilteroverride-Schlüssel enthält (und nicht NULL ist), können Nachrichten (und Debugausgaben) gefiltert werden, indem Sie die folgenden Registrierungs Steuerelemente hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="43c36-121">If the registry contains an InfoQueueStorageFilterOverride key (and is non-zero), then messages (and debug output) can be filtered by adding the following registry controls.</span></span>

-   <span data-ttu-id="43c36-122">DWORD stumm \_ Kategorie \_ \* -Debugausgabe, wenn dieser Schlüssel ungleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="43c36-122">DWORD Mute\_CATEGORY\_\* - Debug output if this key is non-zero.</span></span>
-   <span data-ttu-id="43c36-123">DWORD-Wert zum stumm schalten \_ \_ \* : die Debug-Ausgabe ist deaktiviert, wenn dieser Schlüssel nicht NULL ist.</span><span class="sxs-lookup"><span data-stu-id="43c36-123">DWORD Mute\_SEVERITY\_\* - Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="43c36-124">DWORD \_ -stumm \_ \* -ID: der Name oder die Nummer der Nachricht kann für verwendet werden \* (genau wie bei der zuvor beschriebenen breakon- \_ ID \_ \* ).</span><span class="sxs-lookup"><span data-stu-id="43c36-124">DWORD Mute\_ID\_\* - Message name or number can be used for \* (just like for BreakOn\_ID\_\* described earlier).</span></span> <span data-ttu-id="43c36-125">Die Debugausgabe ist deaktiviert, wenn dieser Schlüssel ungleich 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="43c36-125">Debug output is disabled if this key is non-zero.</span></span>
-   <span data-ttu-id="43c36-126">DWORD: unstumm \_ Schweregrad \_ Info-die Debug-Ausgabe ist aktiviert, wenn dieser Schlüssel nicht 0 (null) ist.</span><span class="sxs-lookup"><span data-stu-id="43c36-126">DWORD Unmute\_SEVERITY\_INFO - Debug output is ENABLED if this key is non-zero.</span></span> <span data-ttu-id="43c36-127">Wenn infoqueuestoragefilteroverride aktiviert ist, werden standardmäßig Debugmeldungen mit dem Schweregrad Info stumm geschaltet. Daher können für diesen Schlüssel die Informationen wieder aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="43c36-127">By default when InfoQueueStorageFilterOverride is enabled, debug messages with severity INFO are muted - therefore for this key allows INFO to be turned back on.</span></span>

<span data-ttu-id="43c36-128">Diese Steuerelemente ändern, ob eine Nachricht aufgezeichnet oder angezeigt wird. Sie haben keine Auswirkung darauf, ob eine API erfolgreich verläuft oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="43c36-128">These controls change whether a message is recorded or displayed; they do not affect whether an API passes or fails.</span></span>

### <a name="setting-break-conditions-using-registry-keys"></a><span data-ttu-id="43c36-129">Festlegen von Abbruch Bedingungen mithilfe von Registrierungs Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="43c36-129">Setting Break Conditions using Registry Keys</span></span>

<span data-ttu-id="43c36-130">Anwendungen können mit den folgenden Registrierungs Schlüsseln gezwungen werden, eine Nachricht zu unterbrechen.</span><span class="sxs-lookup"><span data-stu-id="43c36-130">Applications can be forced to break on a message using the following registry keys.</span></span>

<span data-ttu-id="43c36-131">**Enableatemkonmessage** : dieser Schlüssel ermöglicht das Unterbrechen von Nachrichten (und bewirkt, dass die Einstellungen für "setbreakoncategory ()/SetBreakOnSeverity ()/SetBreakOnID ()" ignoriert werden).</span><span class="sxs-lookup"><span data-stu-id="43c36-131">**EnableBreakOnMessage** - This key enables breaking on messages (and causes i's SetBreakOnCategory()/SetBreakOnSeverity()/SetBreakOnID() settings to be ignored).</span></span> <span data-ttu-id="43c36-132">Die eigentlichen Nachrichten, für die die Unterbrechung durchlaufen werden soll, werden mit einem oder mehreren Break on- \_ \* Werten definiert</span><span class="sxs-lookup"><span data-stu-id="43c36-132">The actual messages to break on are defined using one or more BreakOn\_\* values defined below.</span></span>

-   <span data-ttu-id="43c36-133">\**Break on \_ \_Kategorie \** _: unterbrechen Sie jede Nachricht, die die Speicher Filter durchläuft.</span><span class="sxs-lookup"><span data-stu-id="43c36-133">\**BreakOn\_CATEGORY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="43c36-134">\_ ist eine der \_ \_ kategorienachrichten der d3d10-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="43c36-134">\_ is one of the D3D10\_MESSAGE\_CATEGORY messages.</span></span>
-   <span data-ttu-id="43c36-135">\**Break on \_ Schwere \_ \* Grad* _: unterbrechen Sie jede Nachricht, die die Speicher Filter durchläuft.</span><span class="sxs-lookup"><span data-stu-id="43c36-135">\**BreakOn\_SEVERITY\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="43c36-136">\_ ist eine der \_ Nachrichten Schweregrade der d3d10-Nachricht \_ \_ .</span><span class="sxs-lookup"><span data-stu-id="43c36-136">\_ is one of the D3D10\_MESSAGE\_SEVERITY\_ messages.</span></span>
-   <span data-ttu-id="43c36-137">\**Break on \_ \_ID \** _: unterbrechen Sie jede Nachricht, die die Speicher Filter durchläuft.</span><span class="sxs-lookup"><span data-stu-id="43c36-137">\**BreakOn\_ID\_\** _ - Break on any message passing through the storage filters.</span></span> <span data-ttu-id="43c36-138">\_ ist eine der d3d10- \_ \_ Nachrichten-ID- \_ Nachrichten oder kann der numerische Wert der Error-Enumeration sein.</span><span class="sxs-lookup"><span data-stu-id="43c36-138">\_ is one of the D3D10\_MESSAGE\_ID\_ messages or can be the numerical value of the error enumeration.</span></span> <span data-ttu-id="43c36-139">Nehmen wir beispielsweise an, dass die Nachricht mit der ID "d3d10 \_ Message \_ ID \_ hypothetisch" den Wert 123 in der d3d10-nach \_ richten-ID- \_ Enumeration enthielt.</span><span class="sxs-lookup"><span data-stu-id="43c36-139">For example, Suppose the message with ID "D3D10\_MESSAGE\_ID\_HYPOTHETICAL" had the value 123 in the D3D10\_MESSAGE\_ID enumeration.</span></span> <span data-ttu-id="43c36-140">In diesem Fall würde das Erstellen der Wert breakon- \_ ID \_ hypothetisch = 1 oder breakon \_ ID \_ 123 = 1 denselben Vorgang unterbrechen, wenn eine Nachricht mit der ID d3d10 \_ Message \_ ID \_ hypothetisch vorkommt.</span><span class="sxs-lookup"><span data-stu-id="43c36-140">In this case, creating the value BreakOn\_ID\_HYPOTHETICAL=1 or BreakOn\_ID\_123=1 would both accomplish the same thing - break when a message having ID D3D10\_MESSAGE\_ID\_HYPOTHETICAL is encountered.</span></span>

### <a name="muting-debug-output-using-registry-keys"></a><span data-ttu-id="43c36-141">Muting Debugausgabe mithilfe von Registrierungs Schlüsseln</span><span class="sxs-lookup"><span data-stu-id="43c36-141">Muting Debug Output using Registry Keys</span></span>

<span data-ttu-id="43c36-142">Die Debugausgabe kann mit einem mutedebugoutput-Schlüssel stumm geschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="43c36-142">Debug output can be muted using a MuteDebugOutput key.</span></span> <span data-ttu-id="43c36-143">Das vorhanden sein dieses Werts in der Registrierung erzwingt das Überschreiben der [**ID3D10InfoQueue:: setmutedebugoutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) -Methode der infoqueue.</span><span class="sxs-lookup"><span data-stu-id="43c36-143">The presence of this value in the registry forces override of the InfoQueue's [**ID3D10InfoQueue::SetMuteDebugOutput**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-setmutedebugoutput) method.</span></span> <span data-ttu-id="43c36-144">"Mutedebugoutput" beendet Nachrichten, die den Speicher Filter übergeben, an die Debugausgabe.</span><span class="sxs-lookup"><span data-stu-id="43c36-144">MuteDebugOutput stops messages that pass the storage filter from being sent to debug output.</span></span>

## <a name="disabling-debug-layer-messages"></a><span data-ttu-id="43c36-145">Debugebenennachrichten werden deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="43c36-145">Disabling Debug Layer Messages</span></span>

<span data-ttu-id="43c36-146">Debugebenennachrichten können einzeln oder als Gruppe zur Laufzeit deaktiviert werden, indem Filter mithilfe von [**ID3D10InfoQueue:: addstoragefilterentries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries)angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="43c36-146">Debug layer messages can be disabled individualy or as a group at runtime by specifying filters using [**ID3D10InfoQueue::AddStorageFilterEntries**](/windows/desktop/api/D3D10SDKLayers/nf-d3d10sdklayers-id3d10infoqueue-addstoragefilterentries).</span></span> <span data-ttu-id="43c36-147">Das *pFilter* -Argument für **ID3D10InfoQueue:: addstoragefilterentries** übernimmt eine [**d3d10 \_ Info Queue- \_ \_ Filter**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) Struktur, die eine Zulassungsliste und eine Verweigerungs Liste enthält.</span><span class="sxs-lookup"><span data-stu-id="43c36-147">The *pFilter* argument to **ID3D10InfoQueue::AddStorageFilterEntries** takes a [**D3D10\_INFO\_QUEUE\_FILTER**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter) structure that contains an allow list and a deny list.</span></span> <span data-ttu-id="43c36-148">Die Zulassungs-und Verweigerungs Listen werden von den [**d3d10 \_ Info \_ Queue \_ Filter \_ DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) -Strukturen beschrieben, die die Angabe von Filtern durch catergory, Schweregrad und einzelne Nachrichten-ID ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="43c36-148">The allow and deny lists are described by [**D3D10\_INFO\_QUEUE\_FILTER\_DESC**](/windows/desktop/api/d3d10sdklayers/ns-d3d10sdklayers-d3d10_info_queue_filter_desc) structures that allow filtering to be specified by catergory, severity and individual message ID.</span></span>

<span data-ttu-id="43c36-149">Der folgende Code ist ein Beispiel für das Einrichten der [**ID3D10InfoQueue-Schnittstelle**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) zum Verweigern der d3d10-nach \_ richten- \_ ID \_ Geräte \_ \_ Index \_ Puffer \_ zu \_ klein.</span><span class="sxs-lookup"><span data-stu-id="43c36-149">The following code is an example of setting up the [**ID3D10InfoQueue Interface**](/windows/desktop/api/D3D10SDKLayers/nn-d3d10sdklayers-id3d10infoqueue) to deny the D3D10\_MESSAGE\_ID\_DEVICE\_DRAW\_INDEX\_BUFFER\_TOO\_SMALL message.</span></span>


```
  //retrieve the ID3D10InfoQueue from a Direct3D device created with the D3D10_CREATE_DEVICE_DEBUG flag
  ID3D10InfoQueue * pInfoQueue;
    g_pd3dDevice->QueryInterface( __uuidof(ID3D10InfoQueue),  (void **)&pInfoQueue );
    
  //set up the list of messages to filter
    D3D10_MESSAGE_ID messageIDs [] = { D3D10_MESSAGE_ID_DEVICE_DRAW_INDEX_BUFFER_TOO_SMALL };
    
  //set the DenyList to use the list of messages
    D3D10_INFO_QUEUE_FILTER filter = { 0 };
    filter.DenyList.NumIDs = 1;
    filter.DenyList.pIDList = messageIDs;
    
  //apply the filter to the info queue
    pInfoQueue->AddStorageFilterEntries( &filter );  
```



## <a name="related-topics"></a><span data-ttu-id="43c36-150">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43c36-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43c36-151">API-Ebenen</span><span class="sxs-lookup"><span data-stu-id="43c36-151">API Layers</span></span>](d3d10-graphics-programming-guide-api-features-layers.md)
</dt> <dt>

[<span data-ttu-id="43c36-152">API-Features (Direct3D 10)</span><span class="sxs-lookup"><span data-stu-id="43c36-152">API Features (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-api-features.md)
</dt> </dl>

 

 



