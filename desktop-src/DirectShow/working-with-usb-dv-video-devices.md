---
description: Arbeiten mit USB-DV-Video Geräten
ms.assetid: 6244f006-db9f-42b2-81cd-26eba583613e
title: Arbeiten mit USB-DV-Video Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75647aa7b53bac45c155b4e0a9283418c9af58b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214999"
---
# <a name="working-with-usb-dv-video-devices"></a><span data-ttu-id="58c58-103">Arbeiten mit USB-DV-Video Geräten</span><span class="sxs-lookup"><span data-stu-id="58c58-103">Working with USB DV Video Devices</span></span>

<span data-ttu-id="58c58-104">In diesem Thema wird beschrieben, wie Sie Anwendungen für USB-Videogeräte (Universal Serial Bus) schreiben, mit denen DV-Videos aufgezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="58c58-104">This topic describes how to write applications for Universal Serial Bus (USB) video devices that capture DV video.</span></span>

<span data-ttu-id="58c58-105">Das Standard-DV-Format hat eine Datenrate von ungefähr 25 meits pro Sekunde (Mbit/s).</span><span class="sxs-lookup"><span data-stu-id="58c58-105">Standard DV format has a data rate of about 25 megabits per second (Mbps).</span></span> <span data-ttu-id="58c58-106">Bei der ersten Einführung von USB war nicht genügend Bandbreite für die Unterstützung von DV-Videos vorhanden.</span><span class="sxs-lookup"><span data-stu-id="58c58-106">When USB was first introduced, it did not have enough bandwidth to support DV video.</span></span> <span data-ttu-id="58c58-107">USB 2,0 kann jedoch bis zu 480 Mbit/s unterstützen, was für das DV-Video mehr als ausreichend ist.</span><span class="sxs-lookup"><span data-stu-id="58c58-107">However, USB 2.0 can support up to 480 Mbps, which is more than sufficient for DV video.</span></span> <span data-ttu-id="58c58-108">Die in 2003 freigegebene Spezifikation der USB-Videogeräte Klasse (UVC) definiert das Nutz Last Format für USB-DV-Video Geräte.</span><span class="sxs-lookup"><span data-stu-id="58c58-108">The USB Video Device Class (UVC) specification, released in 2003, defines the payload format for USB DV video devices.</span></span> <span data-ttu-id="58c58-109">Ein Windows-Treibermodell (WDM)-Klassen Treiber für UVC-Geräte wurde in Windows XP Service Pack 2 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="58c58-109">A Windows Driver Model (WDM) class driver for UVC devices was introduced in Windows XP Service Pack 2.</span></span>

<span data-ttu-id="58c58-110">In den meisten Fällen unterstützt der UVC-Treiber dasselbe Programmiermodell wie der msdv-Treiber für IEEE 1394-Geräte.</span><span class="sxs-lookup"><span data-stu-id="58c58-110">In most respects, the UVC driver supports the same programming model as the MSDV driver for IEEE 1394 devices.</span></span> <span data-ttu-id="58c58-111">Für msdv geschriebene Anwendungen sollten nur geringfügige Änderungen zur Unterstützung von UVC-Geräten erforderlich sein.</span><span class="sxs-lookup"><span data-stu-id="58c58-111">Applications written for MSDV should require only minor modifications to support UVC devices.</span></span>

<span data-ttu-id="58c58-112">Der UVC-Treiber verhält sich anders als der msdv-Treiber in den folgenden Bereichen:</span><span class="sxs-lookup"><span data-stu-id="58c58-112">The UVC driver behaves differently from the MSDV driver in the following areas:</span></span>

-   [<span data-ttu-id="58c58-113">Gerätemodus</span><span class="sxs-lookup"><span data-stu-id="58c58-113">Device Mode</span></span>](device-mode.md)
-   [<span data-ttu-id="58c58-114">Streamformat</span><span class="sxs-lookup"><span data-stu-id="58c58-114">Stream Format</span></span>](stream-format.md)
-   [<span data-ttu-id="58c58-115">Signal Format</span><span class="sxs-lookup"><span data-stu-id="58c58-115">Signal Format</span></span>](signal-format.md)
-   [<span data-ttu-id="58c58-116">Band Speicherort Suche</span><span class="sxs-lookup"><span data-stu-id="58c58-116">Tape Location Search</span></span>](tape-location-search.md)
-   <span data-ttu-id="58c58-117">[Übertragen von DV von der Datei auf das Band](transmit-dv-from-file-to-tape.md).</span><span class="sxs-lookup"><span data-stu-id="58c58-117">[Transmit DV from File to Tape](transmit-dv-from-file-to-tape.md).</span></span>

<span data-ttu-id="58c58-118">Um zu ermitteln, welcher Treiber verwendet wird, nennen Sie [**IAMExtDevice:: get \_ deviceport**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport).</span><span class="sxs-lookup"><span data-stu-id="58c58-118">To determine which driver is being used, call [**IAMExtDevice::get\_DevicePort**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport).</span></span> <span data-ttu-id="58c58-119">Der msdv-Treiber gibt das \_ Flag dev Port \_ 1394 zurück, und der UVC-Treiber gibt das \_ USB-Flag für den dev-Port zurück \_ .</span><span class="sxs-lookup"><span data-stu-id="58c58-119">The MSDV driver returns the DEV\_PORT\_1394 flag, and the UVC driver returns the DEV\_PORT\_USB flag.</span></span>

<span data-ttu-id="58c58-120">**Geräteknoten**</span><span class="sxs-lookup"><span data-stu-id="58c58-120">**Device Nodes**</span></span>

<span data-ttu-id="58c58-121">In der USB-Terminologie sind Endpunkte die Punkte, an denen Daten das Gerät eingibt oder verlässt.</span><span class="sxs-lookup"><span data-stu-id="58c58-121">In USB terminology, endpoints are the points where data enters or leaves the device.</span></span> <span data-ttu-id="58c58-122">Ein Endpunkt hat eine Richtung des Datenflusses, entweder Eingabe (von Gerät zum Host) oder Ausgabe (von Host zu Gerät).</span><span class="sxs-lookup"><span data-stu-id="58c58-122">An endpoint has a direction of data flow, either input (from device to host) or output (from host to device).</span></span> <span data-ttu-id="58c58-123">Es kann hilfreich sein, sich diese Richtungen als relativ zum Host vorzustellen.</span><span class="sxs-lookup"><span data-stu-id="58c58-123">It may help to think of these directions as being relative to the host.</span></span> <span data-ttu-id="58c58-124">Die Eingabe wird an den Host weitergeleitet. die Ausgabe stammt vom Host.</span><span class="sxs-lookup"><span data-stu-id="58c58-124">Input goes to the host; output comes from the host.</span></span> <span data-ttu-id="58c58-125">Das folgende Diagramm veranschaulicht die beiden Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="58c58-125">The following diagram illustrates the two endpoints.</span></span>

![USB-Endpunkte](images/ksnodes01.png)

<span data-ttu-id="58c58-127">In einem UVC-Gerät sind die Funktionen des Geräts logisch in Komponenten unterteilt, die als Einheiten und Terminals bezeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="58c58-127">In a UVC device, the functions of the device are logically divided into components called units and terminals.</span></span> <span data-ttu-id="58c58-128">Eine Einheit empfängt mindestens einen Datenstream als Eingabe und liefert genau einen Stream als Ausgabe.</span><span class="sxs-lookup"><span data-stu-id="58c58-128">A unit receives one or more data streams as input and delivers exactly one stream as output.</span></span> <span data-ttu-id="58c58-129">Ein Terminal ist der Ausgangspunkt oder Endpunkt für einen Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="58c58-129">A terminal is the starting point or ending point for a data stream.</span></span> <span data-ttu-id="58c58-130">USB-Endpunkte entsprechen Terminals, aber die Anweisungen sind umgekehrt: ein Eingabe Endpunkt wird durch ein Ausgabe Terminal dargestellt und umgekehrt.</span><span class="sxs-lookup"><span data-stu-id="58c58-130">USB endpoints correspond to terminals, but the directions are reversed: an input endpoint is represented by an output terminal, and vice versa.</span></span> <span data-ttu-id="58c58-131">Das folgende Diagramm zeigt die Beziehung zwischen Terminals und Endpunkten.</span><span class="sxs-lookup"><span data-stu-id="58c58-131">The following diagram shows the relation between terminals and endpoints.</span></span>

![UVC-Einheiten und-Terminals](images/ksnodes02.png)

<span data-ttu-id="58c58-133">Außerdem entspricht nicht jedes Terminal einem USB-Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="58c58-133">Also, not every terminal corresponds to a USB endpoint.</span></span> <span data-ttu-id="58c58-134">Der Begriff Endpunkt bezieht sich speziell auf USB-Verbindungen, und ein Gerät kann Daten über nicht-USB-Verbindungen senden oder empfangen.</span><span class="sxs-lookup"><span data-stu-id="58c58-134">The term endpoint refers specifically to USB connections, and a device may send or receive data through non-USB connections.</span></span> <span data-ttu-id="58c58-135">Eine Videokamera ist z. b. ein Eingabe Terminal, und ein LCD-Bildschirm ist ein Ausgabe Terminal.</span><span class="sxs-lookup"><span data-stu-id="58c58-135">For example, a video camera is an input terminal and an LCD screen is an output terminal.</span></span>

<span data-ttu-id="58c58-136">Im-Server-Proxy Filter werden Einheiten und Terminals als Knoten innerhalb des Filters dargestellt.</span><span class="sxs-lookup"><span data-stu-id="58c58-136">In the KS Proxy filter, units and terminals are represented as nodes inside the filter.</span></span> <span data-ttu-id="58c58-137">Der Begriff Knoten ist allgemeiner als die Begriffe Unit und Terminal, da nicht-USB-Geräte auch über Knoten verfügen können.</span><span class="sxs-lookup"><span data-stu-id="58c58-137">The term node is more general than the terms unit and terminal because non-USB devices can also have nodes.</span></span> <span data-ttu-id="58c58-138">Um Informationen zu den Knoten in einem Filter zu erhalten, Fragen Sie den Filter nach der " [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) "-Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="58c58-138">To get information about the nodes in a filter, query the filter for the [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) interface.</span></span> <span data-ttu-id="58c58-139">Knoten Typen werden von GUIDs identifiziert.</span><span class="sxs-lookup"><span data-stu-id="58c58-139">Node types are identified by GUIDs.</span></span> <span data-ttu-id="58c58-140">Auswahl Knoten sind Knoten, die zwischen zwei oder mehr Eingaben wechseln können.</span><span class="sxs-lookup"><span data-stu-id="58c58-140">Selector nodes are nodes that can switch between two or more inputs.</span></span> <span data-ttu-id="58c58-141">Auswahl Knoten machen die [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) -Schnittstelle verfügbar.</span><span class="sxs-lookup"><span data-stu-id="58c58-141">Selector nodes expose the [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) interface.</span></span>

<span data-ttu-id="58c58-142">Der folgende Code testet, ob eine Ausgabe-PIN für einen Filter Eingaben von einem Knoten eines bestimmten Typs empfängt.</span><span class="sxs-lookup"><span data-stu-id="58c58-142">The following code tests whether an output pin on a filter receives input from a node of a given type.</span></span>


```C++
// Structure to hold topology information.
struct TopologyConnections
{
    KSTOPOLOGY_CONNECTION *connections; // Array of connections
    DWORD count;  // Number of elements in the array
};

/////////////////////////////////////////////////////////////////////
// Name: GetTopologyConnections
// Desc: Gets the topology information from a filter.
//
// pTopo:       Pointer to the filter's IKsTopologyInfo interface.
// connectInfo: Pointer to a TopologyConnections structure. The 
//              function fills in this structure.
//
// Note: If the function succeeds, call CoTaskMemFree to free the
//       pConnectInfo->connections array.
/////////////////////////////////////////////////////////////////////

HRESULT GetTopologyConnections(
    IKsTopologyInfo *pTopo, 
    TopologyConnections *pConnectInfo
    )
{
    DWORD count;
    HRESULT hr = pTopo->get_NumConnections(&count);
    if (FAILED(hr))
    {
        return hr;
    }

    pConnectInfo->count = count;
    pConnectInfo->connections = NULL;
    if (count > 0)
    {
        // Allocate an array for the connection information.
        SIZE_T cb = sizeof(KSTOPOLOGY_CONNECTION) * count;
        KSTOPOLOGY_CONNECTION *pConnections = 
            (KSTOPOLOGY_CONNECTION*) CoTaskMemAlloc(cb);
        if (pConnections == NULL)
        {
            return E_OUTOFMEMORY;
        }
        // Fill the array.
        for (DWORD ix = 0; ix < count; ix++)
        {
            hr = pTopo->get_ConnectionInfo(ix, &pConnections[ix]);
            if (FAILED(hr))
            {
                break;
            }
        }
        if (SUCCEEDED(hr))
        {
            pConnectInfo->connections = pConnections;
        }
        else
        {
           CoTaskMemFree(pConnections);
        }
    }
    return hr;
}

/////////////////////////////////////////////////////////////////////
// Name: IsNodeDownstreamFromNode
// Desc: Searches upstream from a node for a specified node type.
//
// pTopo:        Pointer to the filter's IKsTopologyInfo interface.
// connectInfo:  Contains toplogy information. To fill in this
//               structure, call GetTopologyConnections.
// nodeID:       ID of the starting node in the search.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected, or false otherwise.
//
// Note: If the source node matches the type, this function returns 
//       true without searching upstream.
/////////////////////////////////////////////////////////////////////

HRESULT IsNodeDownstreamFromNode(
    IKsTopologyInfo *pTopo,
    const TopologyConnections& connectInfo, 
    DWORD nodeID,
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    *pIsConnected = false;
    // Base case for recursion: check the source node.
    GUID type;
    HRESULT hr = pTopo->get_NodeType(nodeID, &type);
    if (FAILED(hr))
    {
        return hr;
    }
    if (type == nodeType)
    {
        *pIsConnected = true;
        return S_OK;
    }

    // If the source node is a selector, get the input node.
    CComPtr<ISelector> pSelector;
    hr = pTopo->CreateNodeInstance(nodeID, __uuidof(ISelector), 
        (void**)&pSelector);
    if (SUCCEEDED(hr))
    {
        DWORD sourceNodeID;
        hr = pSelector->get_SourceNodeId(&sourceNodeID);
        if (SUCCEEDED(hr))
        {
            // Recursive call with the selector's input node.
            return IsNodeDownstreamFromNode(pTopo, connectInfo, 
                       sourceNodeID, nodeType, pIsConnected);
        }
    }
    else if (hr == E_NOINTERFACE)
    {
        hr = S_OK;  // This node is not a selector. Not a failure.
    }
    else
    {
        return hr;
    }

    // Test all of the upstream connections on this pin. 
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == nodeID) &&
            (connectInfo.connections[ix].FromNode != KSFILTER_NODE))
        {
            // FromNode is connected to the source node.
            DWORD fromNode = connectInfo.connections[ix].FromNode;

            // Recursive call with the upstream node.
            bool bIsConnected;
            hr = IsNodeDownstreamFromNode(pTopo, connectInfo, 
                fromNode, nodeType, &bIsConnected);
            if (FAILED(hr))
            {
                break;
            }
            if (bIsConnected)
            {
                *pIsConnected = true;
                break;
            }
        }
    }
    return hr;
}


/////////////////////////////////////////////////////////////////////
// Name: GetNodeUpstreamFromPin
// Desc: Finds the node connected to an output pin.
//
// connectInfo: Contains toplogy information. To fill in this
//              structure, call GetTopologyConnections.
// nPinIndex:   Index of the output pin.
// pNodeID:     Receives the ID of the connected node.
/////////////////////////////////////////////////////////////////////

HRESULT GetNodeUpstreamFromPin(
    const TopologyConnections& connectInfo, 
    UINT nPinIndex, 
    DWORD *pNodeID
    )
{
    bool bFound = false;
    for (DWORD ix = 0; ix < connectInfo.count; ix++)
    {
        if ((connectInfo.connections[ix].ToNode == KSFILTER_NODE) &&
            (connectInfo.connections[ix].ToNodePin == nPinIndex))
        {
            *pNodeID = connectInfo.connections[ix].FromNode;
            bFound = true;
            break;
        }
    }
    if (bFound)
    {
        return S_OK;
    }
    else
    {
        return E_FAIL;
    }
}


/////////////////////////////////////////////////////////////////////
// Name: IsPinDownstreamFromNode
// Desc: Tests whether an output pin gets data from a node of
//       a specified type.
// 
// pFilter:      Pointer to the filter's IBaseFilter interface.
// UINT:         Index of the output pin to test.
// nodeType:     Type of node to find.
// pIsConnected: Receives true if connected; false otherwise.
/////////////////////////////////////////////////////////////////////

HRESULT IsPinDownstreamFromNode(
    IBaseFilter *pFilter, 
    UINT nPinIndex, 
    const GUID& nodeType,
    bool *pIsConnected
    )
{
    CComQIPtr<IKsTopologyInfo> pTopo(pFilter);
    if (pTopo == NULL)
    {
        return E_NOINTERFACE;
    }

    // Get the topology connection information.
    TopologyConnections connectionInfo;
    HRESULT hr = GetTopologyConnections(pTopo, &connectionInfo);
    if (FAILED(hr))
    {
        return hr;
    }

    // Find the node upstream from this pin.
    DWORD nodeID;
    hr = GetNodeUpstreamFromPin(connectionInfo, nPinIndex, &nodeID);
    if (SUCCEEDED(hr))
    {
        bool isConnected;
        hr = IsNodeDownstreamFromNode(pTopo, connectionInfo, 
            nodeID, nodeType, &isConnected);
        if (SUCCEEDED(hr))
        {
            *pIsConnected = isConnected;
        }
    }
    CoTaskMemFree(connectionInfo.connections);
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="58c58-143">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="58c58-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="58c58-144">Digitales Video in DirectShow</span><span class="sxs-lookup"><span data-stu-id="58c58-144">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 



