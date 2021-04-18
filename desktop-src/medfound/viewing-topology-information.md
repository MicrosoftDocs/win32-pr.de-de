---
description: Anzeigen von Topologieinformationen
ms.assetid: d687ecd3-9ad6-46d5-b927-d9b99af2002f
title: Anzeigen von Topologieinformationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c4e6808fb2414de14817c63f9f4736acc9223f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347087"
---
# <a name="viewing-topology-information"></a><span data-ttu-id="a21e3-103">Anzeigen von Topologieinformationen</span><span class="sxs-lookup"><span data-stu-id="a21e3-103">Viewing Topology Information</span></span>

<span data-ttu-id="a21e3-104">In topoedit verfügt jedes topologieelement, z. b. Knoten, Knoten Eingaben und Knoten Ausgaben, über einen zugeordneten Attribut Speicher, der das Verhalten des Knotens verwaltet.</span><span class="sxs-lookup"><span data-stu-id="a21e3-104">In TopoEdit, each topology item, such as nodes, node inputs, and node outputs, has an associated attribute store that manages the behavior of the node.</span></span> <span data-ttu-id="a21e3-105">Um die Attribute anzuzeigen, wählen Sie das Element aus, und im Bereich **Attribute** werden die Informationen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a21e3-105">To see the attributes, select the item, and the **Attributes Pane** displays the information.</span></span> <span data-ttu-id="a21e3-106">Für Topologien, die aus einer XML-Datei geladen werden, zeigen einige der Knoten möglicherweise nicht den gesamten Attribut Speicher an.</span><span class="sxs-lookup"><span data-stu-id="a21e3-106">For topologies that are loaded from an XML file, some of the nodes may not display the entire attribute store.</span></span> <span data-ttu-id="a21e3-107">Um den gesamten Attribut Speicher anzuzeigen, müssen Sie die Topologie auflösen.</span><span class="sxs-lookup"><span data-stu-id="a21e3-107">To see the entire attribute store, resolve the topology.</span></span> <span data-ttu-id="a21e3-108">Weitere Informationen finden Sie unter [Auflösen einer Topologie mit topoedit](resolving-a-topology-with-topoedit.md).</span><span class="sxs-lookup"><span data-stu-id="a21e3-108">For more information, see [Resolving a Topology with TopoEdit](resolving-a-topology-with-topoedit.md).</span></span>

<span data-ttu-id="a21e3-109">In der folgenden Tabelle werden die Topologieelemente und die Attribute angezeigt, die im Bereich angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a21e3-109">The following table shows the topology item and the attributes that the pane displays.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a21e3-110">Topologieelement</span><span class="sxs-lookup"><span data-stu-id="a21e3-110">Topology item</span></span></th>
<th><span data-ttu-id="a21e3-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="a21e3-111">Attributes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a21e3-112">Topologieknoten</span><span class="sxs-lookup"><span data-stu-id="a21e3-112">Topology nodes</span></span></td>
<td><ul>
<li><span data-ttu-id="a21e3-113"><a href="topology-node-attributes.md">Topologieknotenattribute</a> für alle Knoten.</span><span class="sxs-lookup"><span data-stu-id="a21e3-113"><a href="topology-node-attributes.md">Topology Node Attributes</a> for all nodes.</span></span><br/></li>
<li><span data-ttu-id="a21e3-114"><a href="presentation-descriptor-attributes.md">Präsentations deskriptorattribute</a> nur für Quellknoten.</span><span class="sxs-lookup"><span data-stu-id="a21e3-114"><a href="presentation-descriptor-attributes.md">Presentation Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="a21e3-115">Eingabe-und Ausgabe Vertrauensstellungs Informationen für Transformations-und Ausgabe Knoten.</span><span class="sxs-lookup"><span data-stu-id="a21e3-115">Input and output trust authority information for transform and output nodes.</span></span><br/></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a21e3-116">Knoten Eingabe</span><span class="sxs-lookup"><span data-stu-id="a21e3-116">Node input</span></span></td>
<td><ul>
<li><span data-ttu-id="a21e3-117"><a href="media-type-attributes.md">Medientyp Attribute</a> für alle Knoten.</span><span class="sxs-lookup"><span data-stu-id="a21e3-117"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a21e3-118">Knoten Ausgabe</span><span class="sxs-lookup"><span data-stu-id="a21e3-118">Node output</span></span></td>
<td><ul>
<li><span data-ttu-id="a21e3-119"><a href="stream-descriptor-attributes.md">Streamdeskriptorattribute</a> nur für Quellknoten.</span><span class="sxs-lookup"><span data-stu-id="a21e3-119"><a href="stream-descriptor-attributes.md">Stream Descriptor Attributes</a> for source nodes only.</span></span><br/></li>
<li><span data-ttu-id="a21e3-120"><a href="media-type-attributes.md">Medientyp Attribute</a> für alle Knoten.</span><span class="sxs-lookup"><span data-stu-id="a21e3-120"><a href="media-type-attributes.md">Media Type Attributes</a> for all nodes.</span></span><br/></li>
</ul></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a21e3-121">Die Attributwerte, außer Zeiger Verweise und Array Werte, können geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a21e3-121">The attribute values, except for pointer references and array values, can be changed.</span></span> <span data-ttu-id="a21e3-122">Um einen Attribut Wert zu ändern, geben Sie den neuen Wert neben dem Attribut ein, und klicken Sie im Bereich **Attribute** auf **Speichern** .</span><span class="sxs-lookup"><span data-stu-id="a21e3-122">To change an attribute value, type in the new value next to the attribute and click **Save** on the **Attributes Pane**.</span></span> <span data-ttu-id="a21e3-123">Der neue Wert wird im Attribut Speicher aktualisiert und erst dann auf die Topologie angewendet, nachdem er aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="a21e3-123">The new value is updated in the attribute store and applied to the topology only after it is resolved.</span></span>

## <a name="to-add-a-new-attribute-for-a-node"></a><span data-ttu-id="a21e3-124">So fügen Sie ein neues Attribut für einen Knoten hinzu</span><span class="sxs-lookup"><span data-stu-id="a21e3-124">To add a new attribute for a node</span></span>

1.  <span data-ttu-id="a21e3-125">Wählen Sie den Knoten aus, indem Sie im Bereich **Topologie** darauf klicken.</span><span class="sxs-lookup"><span data-stu-id="a21e3-125">Select the node by clicking it on the **Topology Pane**.</span></span>

    <span data-ttu-id="a21e3-126">Die Attribute, die für den Knoten festgelegt werden, werden im Bereich **Attribute** angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a21e3-126">The attributes that are set on the node are shown on the **Attributes Pane**.</span></span>

2.  <span data-ttu-id="a21e3-127">Klicken Sie im Bereich **Attribute** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="a21e3-127">On the **Attributes Pane**, click **Add**.</span></span>

    <span data-ttu-id="a21e3-128">Dadurch wird das Dialogfeld **Attribut hinzufügen** geöffnet.</span><span class="sxs-lookup"><span data-stu-id="a21e3-128">This opens the **Add Attribute** dialog box.</span></span>

3.  <span data-ttu-id="a21e3-129">Wählen Sie in der ersten Dropdown Liste die Attribut Kategorie aus.</span><span class="sxs-lookup"><span data-stu-id="a21e3-129">From the first drop-down list, choose the Attribute category.</span></span>

    <span data-ttu-id="a21e3-130">Die Kategorien sind vom topologieknoten abhängig.</span><span class="sxs-lookup"><span data-stu-id="a21e3-130">The categories depend on the topology node.</span></span> <span data-ttu-id="a21e3-131">Beispielsweise zeigt die Dropdown Liste für den Quellknoten die **Präsentations deskriptorattribute** und **Knoten Attribute** als verfügbare Kategorien an.</span><span class="sxs-lookup"><span data-stu-id="a21e3-131">For example, for the source node, the drop-down list shows **Presentation Descriptor Attributes** and **Node Attributes** as the available categories.</span></span>

4.  <span data-ttu-id="a21e3-132">Wählen Sie in der zweiten Dropdown Liste das Attribut aus, das Sie für den Knoten festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="a21e3-132">From the second drop-down list, choose the attribute that you want to set on the node.</span></span>

5.  <span data-ttu-id="a21e3-133">Fügen Sie im Bearbeitungsfeld den Wert für das-Attribut hinzu.</span><span class="sxs-lookup"><span data-stu-id="a21e3-133">In the edit box, add the value for the attribute.</span></span>

6.  <span data-ttu-id="a21e3-134">Klicken Sie auf **Hinzufügen** , um das Attribut hinzuzufügen und zum Hauptfenster zurückzukehren, oder auf **Abbrechen** , um den Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="a21e3-134">Click **Add** to add the attribute and return to the main window, or click **Cancel** to cancel the operation.</span></span>

7.  <span data-ttu-id="a21e3-135">Klicken Sie im Menü **Topologie** auf **Topologie auflösen** , um das neue Attribut auf die Topologie festzulegen.</span><span class="sxs-lookup"><span data-stu-id="a21e3-135">From the **Topology** menu, click **Resolve Topology** to set the new attribute to the topology.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a21e3-136">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="a21e3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a21e3-137">Topoedit</span><span class="sxs-lookup"><span data-stu-id="a21e3-137">TopoEdit</span></span>](topoedit.md)
</dt> </dl>

 

 




