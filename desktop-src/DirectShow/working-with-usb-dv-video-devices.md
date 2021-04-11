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
# <a name="working-with-usb-dv-video-devices"></a>Arbeiten mit USB-DV-Video Geräten

In diesem Thema wird beschrieben, wie Sie Anwendungen für USB-Videogeräte (Universal Serial Bus) schreiben, mit denen DV-Videos aufgezeichnet werden.

Das Standard-DV-Format hat eine Datenrate von ungefähr 25 meits pro Sekunde (Mbit/s). Bei der ersten Einführung von USB war nicht genügend Bandbreite für die Unterstützung von DV-Videos vorhanden. USB 2,0 kann jedoch bis zu 480 Mbit/s unterstützen, was für das DV-Video mehr als ausreichend ist. Die in 2003 freigegebene Spezifikation der USB-Videogeräte Klasse (UVC) definiert das Nutz Last Format für USB-DV-Video Geräte. Ein Windows-Treibermodell (WDM)-Klassen Treiber für UVC-Geräte wurde in Windows XP Service Pack 2 eingeführt.

In den meisten Fällen unterstützt der UVC-Treiber dasselbe Programmiermodell wie der msdv-Treiber für IEEE 1394-Geräte. Für msdv geschriebene Anwendungen sollten nur geringfügige Änderungen zur Unterstützung von UVC-Geräten erforderlich sein.

Der UVC-Treiber verhält sich anders als der msdv-Treiber in den folgenden Bereichen:

-   [Gerätemodus](device-mode.md)
-   [Streamformat](stream-format.md)
-   [Signal Format](signal-format.md)
-   [Band Speicherort Suche](tape-location-search.md)
-   [Übertragen von DV von der Datei auf das Band](transmit-dv-from-file-to-tape.md).

Um zu ermitteln, welcher Treiber verwendet wird, nennen Sie [**IAMExtDevice:: get \_ deviceport**](/windows/desktop/api/Strmif/nf-strmif-iamextdevice-get_deviceport). Der msdv-Treiber gibt das \_ Flag dev Port \_ 1394 zurück, und der UVC-Treiber gibt das \_ USB-Flag für den dev-Port zurück \_ .

**Geräteknoten**

In der USB-Terminologie sind Endpunkte die Punkte, an denen Daten das Gerät eingibt oder verlässt. Ein Endpunkt hat eine Richtung des Datenflusses, entweder Eingabe (von Gerät zum Host) oder Ausgabe (von Host zu Gerät). Es kann hilfreich sein, sich diese Richtungen als relativ zum Host vorzustellen. Die Eingabe wird an den Host weitergeleitet. die Ausgabe stammt vom Host. Das folgende Diagramm veranschaulicht die beiden Endpunkte.

![USB-Endpunkte](images/ksnodes01.png)

In einem UVC-Gerät sind die Funktionen des Geräts logisch in Komponenten unterteilt, die als Einheiten und Terminals bezeichnet werden. Eine Einheit empfängt mindestens einen Datenstream als Eingabe und liefert genau einen Stream als Ausgabe. Ein Terminal ist der Ausgangspunkt oder Endpunkt für einen Datenstrom. USB-Endpunkte entsprechen Terminals, aber die Anweisungen sind umgekehrt: ein Eingabe Endpunkt wird durch ein Ausgabe Terminal dargestellt und umgekehrt. Das folgende Diagramm zeigt die Beziehung zwischen Terminals und Endpunkten.

![UVC-Einheiten und-Terminals](images/ksnodes02.png)

Außerdem entspricht nicht jedes Terminal einem USB-Endpunkt. Der Begriff Endpunkt bezieht sich speziell auf USB-Verbindungen, und ein Gerät kann Daten über nicht-USB-Verbindungen senden oder empfangen. Eine Videokamera ist z. b. ein Eingabe Terminal, und ein LCD-Bildschirm ist ein Ausgabe Terminal.

Im-Server-Proxy Filter werden Einheiten und Terminals als Knoten innerhalb des Filters dargestellt. Der Begriff Knoten ist allgemeiner als die Begriffe Unit und Terminal, da nicht-USB-Geräte auch über Knoten verfügen können. Um Informationen zu den Knoten in einem Filter zu erhalten, Fragen Sie den Filter nach der " [**IKsTopologyInfo**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-ikstopologyinfo) "-Schnittstelle ab. Knoten Typen werden von GUIDs identifiziert. Auswahl Knoten sind Knoten, die zwischen zwei oder mehr Eingaben wechseln können. Auswahl Knoten machen die [**ISelector**](/previous-versions/windows/desktop/api/Vidcap/nn-vidcap-iselector) -Schnittstelle verfügbar.

Der folgende Code testet, ob eine Ausgabe-PIN für einen Filter Eingaben von einem Knoten eines bestimmten Typs empfängt.


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



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Digitales Video in DirectShow](digital-video-in-directshow.md)
</dt> </dl>

 

 



