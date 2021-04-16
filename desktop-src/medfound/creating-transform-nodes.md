---
description: Erstellen von Transformations Knoten
ms.assetid: d70a3c2b-2f0e-4e29-9a8f-84a50d9f1682
title: Erstellen von Transformations Knoten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f39eed9f49e10501fadc00f47b57cf95705a7cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104524611"
---
# <a name="creating-transform-nodes"></a>Erstellen von Transformations Knoten

Ein Transformations Knoten stellt eine Media Foundation Transformation (MFT) dar, z. b. einen Decoder oder einen Encoder. Es gibt verschiedene Möglichkeiten, einen Transformations Knoten zu initialisieren:

-   Von einem Zeiger auf die MFT.
-   Von einer CLSID für die MFT.
-   Von einem Zeiger auf ein Aktivierungs Objekt für die MFT.

Wenn Sie die Topologie innerhalb des geschützten Medien Pfads (PMP) laden möchten, müssen Sie entweder die CLSID oder ein Aktivierungs Objekt verwenden, damit die MFT im geschützten Prozess erstellt werden kann. Der erste Ansatz (mithilfe eines Zeigers auf die MFT) funktioniert nicht mit dem PMP.

## <a name="creating-a-transform-node-from-an-mft"></a>Erstellen eines Transformations Knotens aus einem MFT

Gehen Sie folgendermaßen vor, um einen Transformations Knoten von einem MFT zu erstellen:

1.  Erstellen Sie eine Instanz des MFT, und rufen Sie einen Zeiger auf die [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Schnittstelle der MFT ab.
2.  Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Knoten Flag für die **MF- \_ Topologie \_ \_** auf, um den Transformations Knoten zu erstellen.
3.  Nennen Sie [**imftopologynode:: abtobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) , und übergeben Sie den [**imftransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) -Zeiger.
4.  Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.

Im folgenden Beispiel wird ein Transformations Knoten von einem MFT erstellt und initialisiert.


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFTransform *pMFT,         // MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pMFT);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-a-clsid"></a>Erstellen eines Transformations Knotens aus einer CLSID

Gehen Sie folgendermaßen vor, um einen Transformations Knoten aus einer CLSID zu erstellen:

1.  Suchen Sie die CLSID des MFT. Sie können die [**mftenum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) -Funktion verwenden, um die CLSIDs von MFTs nach Kategorie zu suchen, z. b. Decoder oder Encoder. Sie können auch die CLSID einer bestimmten MFT kennen, die Sie verwenden möchten (z. b. Wenn Sie Ihre eigene benutzerdefinierte MFT implementiert haben).
2.  Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Knoten Flag für die **MF- \_ Topologie \_ \_** auf, um den Transformations Knoten zu erstellen.
3.  Legen Sie das Attribut " **MF \_ toponode \_ Transform \_ objectID** " für den Knoten fest. Der Attribut Wert ist die CLSID.
4.  Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.

Im folgenden Beispiel wird ein Transformations Knoten aus einer CLSID erstellt und initialisiert.


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    const CLSID& clsid,         // CLSID of the MFT.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the CLSID attribute.

    if (SUCCEEDED(hr))
    {
        hr = pNode->SetGUID(MF_TOPONODE_TRANSFORM_OBJECTID, clsid);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="creating-a-transform-node-from-an-activation-object"></a>Erstellen eines Transformations Knotens aus einem Aktivierungs Objekt

Einige MFTs stellen Aktivierungs Objekte bereit. Beispielsweise gibt die [**MF**](/windows/desktop/api/wmcontainer/nf-wmcontainer-mfcreatewmaencoderactivate) -Funktion (MF-Datei) ein Aktivierungs Objekt für den Windows Media Audio (WMA)-Encoder zurück. Die genaue Funktion hängt vom MFT ab. Nicht jede MFT stellt ein Aktivierungs Objekt bereit. Weitere Informationen finden Sie unter [Activation Objects](activation-objects.md).

Sie können auch ein MFT-Aktivierungs Objekt abrufen, indem Sie die [**mftenumex**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) -Funktion aufrufen.

Gehen Sie folgendermaßen vor, um einen Transformations Knoten aus einem Aktivierungs Objekt zu erstellen:

1.  Erstellen Sie das Aktivierungs Objekt, und rufen Sie einen Zeiger auf die [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Schnittstelle des Aktivierungs Objekts ab.
2.  Rufen Sie [**mfkreatetopologynode**](/windows/desktop/api/mfidl/nf-mfidl-mfcreatetopologynode) mit dem Knoten Flag für die **MF- \_ Topologie \_ \_** auf, um den Transformations Knoten zu erstellen.
3.  Nennen Sie [**imftopologynode:: abtobject**](/windows/desktop/api/mfidl/nf-mfidl-imftopologynode-setobject) , und übergeben Sie den [**imfaktivate**](/windows/desktop/api/mfobjects/nn-mfobjects-imfactivate) -Zeiger.
4.  Nennen Sie [**imftopology:: AddNode**](/windows/desktop/api/mfidl/nf-mfidl-imftopology-addnode) , um den Knoten der Topologie hinzuzufügen.

Im folgenden Beispiel wird ein Transformations Knoten von einem Aktivierungs Objekt erstellt und initialisiert.


```C++
HRESULT AddTransformNode(
    IMFTopology *pTopology,     // Topology.
    IMFActivate *pActivate,     // MFT activation object.
    IMFTopologyNode **ppNode    // Receives the node pointer.
    )
{
    *ppNode = NULL;

    IMFTopologyNode *pNode = NULL;
    
    // Create the node.
    HRESULT hr = MFCreateTopologyNode(MF_TOPOLOGY_TRANSFORM_NODE, &pNode);

    // Set the object pointer.
    if (SUCCEEDED(hr))
    {
        hr = pNode->SetObject(pActivate);
    }

    // Add the node to the topology.
    if (SUCCEEDED(hr))
    {
        hr = pTopology->AddNode(pNode);
    }

    // Return the pointer to the caller.
    if (SUCCEEDED(hr))
    {
        *ppNode = pNode;
        (*ppNode)->AddRef();
    }

    SafeRelease(&pNode);
    return hr;
}
```



## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Erstellen von Topologien](creating-topologies.md)
</dt> <dt>

[Topologien](topologies.md)
</dt> <dt>

[**Imftopologynode**](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> </dl>

 

 



