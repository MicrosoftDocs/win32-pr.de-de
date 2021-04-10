---
description: Topologieknotenattribute
ms.assetid: 584c0670-9051-4d03-9635-c8fadc8798c3
title: Topologieknotenattribute
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 904213752c0a3444bc4c9ea2b5cf2d5c21c8bd83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959369"
---
# <a name="topology-node-attributes"></a><span data-ttu-id="36b3c-103">Topologieknotenattribute</span><span class="sxs-lookup"><span data-stu-id="36b3c-103">Topology Node Attributes</span></span>

<span data-ttu-id="36b3c-104">Die folgenden Attribute gelten für topologieknoten.</span><span class="sxs-lookup"><span data-stu-id="36b3c-104">The following attributes apply to topology nodes.</span></span>

## <a name="general-topology-node-attributes"></a><span data-ttu-id="36b3c-105">Attribute der allgemeinen topologieknoten</span><span class="sxs-lookup"><span data-stu-id="36b3c-105">General Topology Node Attributes</span></span>



| <span data-ttu-id="36b3c-106">Attribut</span><span class="sxs-lookup"><span data-stu-id="36b3c-106">Attribute</span></span>                                                                       | <span data-ttu-id="36b3c-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36b3c-107">Description</span></span>                                                                                                                                              |
|---------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36b3c-108">**MF \_ toponode \_ Connect- \_ Methode**</span><span class="sxs-lookup"><span data-stu-id="36b3c-108">**MF\_TOPONODE\_CONNECT\_METHOD**</span></span>](mf-toponode-connect-method-attribute.md)   | <span data-ttu-id="36b3c-109">Gibt an, wie der topologielader diesen topologieknoten verbindet und ob dieser Knoten optional ist.</span><span class="sxs-lookup"><span data-stu-id="36b3c-109">Specifies how the topology loader connects this topology node, and whether this node is optional.</span></span>                                                        |
| [<span data-ttu-id="36b3c-110">**MF- \_ toponode- \_ Decoder**</span><span class="sxs-lookup"><span data-stu-id="36b3c-110">**MF\_TOPONODE\_DECODER**</span></span>](mf-toponode-decoder-attribute.md)                  | <span data-ttu-id="36b3c-111">Gibt an, ob das Objekt eines topologiedjeders ein Decoder ist.</span><span class="sxs-lookup"><span data-stu-id="36b3c-111">Specifies whether a toplogy node's object is a decoder.</span></span>                                                                                                  |
| [<span data-ttu-id="36b3c-112">**MF- \_ toponode- \_ Entschlüsselung**</span><span class="sxs-lookup"><span data-stu-id="36b3c-112">**MF\_TOPONODE\_DECRYPTOR**</span></span>](mf-toponode-decryptor-attribute.md)              | <span data-ttu-id="36b3c-113">Gibt an, ob das zugrunde liegende Objekt eines topologieknotens eine Entschlüsselung ist.</span><span class="sxs-lookup"><span data-stu-id="36b3c-113">Specifies whether a toplogy node's underlying object is a decryptor.</span></span>                                                                                     |
| [<span data-ttu-id="36b3c-114">**MF- \_ toponode- \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="36b3c-114">**MF\_TOPONODE\_DISCARDABLE**</span></span>](mf-toponode-discardable-attribute.md)          | <span data-ttu-id="36b3c-115">Gibt an, ob die Pipeline Beispiele von einem topologieknoten ablegen kann.</span><span class="sxs-lookup"><span data-stu-id="36b3c-115">Specifies whether the pipeline can drop samples from a topology node.</span></span>                                                                                    |
| [<span data-ttu-id="36b3c-116">**MF- \_ toponode- \_ Fehler \_ majortype**</span><span class="sxs-lookup"><span data-stu-id="36b3c-116">**MF\_TOPONODE\_ERROR\_MAJORTYPE**</span></span>](mf-toponode-error-majortype-attribute.md) | <span data-ttu-id="36b3c-117">Enthält den Haupt Medientyp für einen topologieknoten.</span><span class="sxs-lookup"><span data-stu-id="36b3c-117">Contains the major media type for a topology node.</span></span> <span data-ttu-id="36b3c-118">Dieses Attribut wird festgelegt, wenn die Topologie nicht geladen werden kann, da der richtige Decoder nicht gefunden werden konnte.</span><span class="sxs-lookup"><span data-stu-id="36b3c-118">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span> |
| [<span data-ttu-id="36b3c-119">**MF- \_ toponode- \_ \_ Fehleruntertyp**</span><span class="sxs-lookup"><span data-stu-id="36b3c-119">**MF\_TOPONODE\_ERROR\_SUBTYPE**</span></span>](mf-toponode-error-subtype-attribute.md)     | <span data-ttu-id="36b3c-120">Enthält den Medien Untertyp für einen topologieknoten.</span><span class="sxs-lookup"><span data-stu-id="36b3c-120">Contains the media subtype for a topology node.</span></span> <span data-ttu-id="36b3c-121">Dieses Attribut wird festgelegt, wenn die Topologie nicht geladen werden kann, da der richtige Decoder nicht gefunden werden konnte.</span><span class="sxs-lookup"><span data-stu-id="36b3c-121">This attribute is set when the topology fails to load because the correct decoder could not be found.</span></span>    |
| [<span data-ttu-id="36b3c-122">**MF- \_ toponode- \_ ErrorCode**</span><span class="sxs-lookup"><span data-stu-id="36b3c-122">**MF\_TOPONODE\_ERRORCODE**</span></span>](mf-toponode-errorcode-attribute.md)              | <span data-ttu-id="36b3c-123">Enthält den Fehlercode des letzten Verbindungsfehlers für diesen topologieknoten.</span><span class="sxs-lookup"><span data-stu-id="36b3c-123">Contains the error code from the most recent connection failure for this topology node.</span></span>                                                                  |
| [<span data-ttu-id="36b3c-124">**MF- \_ toponode \_ gesperrt**</span><span class="sxs-lookup"><span data-stu-id="36b3c-124">**MF\_TOPONODE\_LOCKED**</span></span>](mf-toponode-locked-attribute.md)                    | <span data-ttu-id="36b3c-125">Gibt an, ob die Medientypen für diesen topologieknoten geändert werden können.</span><span class="sxs-lookup"><span data-stu-id="36b3c-125">Specifies whether the media types can be changed on this topology node.</span></span>                                                                                  |
| [<span data-ttu-id="36b3c-126">**Hier finden Sie ein MF- \_ toponode- \_ Markin \_**</span><span class="sxs-lookup"><span data-stu-id="36b3c-126">**MF\_TOPONODE\_MARKIN\_HERE**</span></span>](mf-toponode-markin-here-attribute.md)         | <span data-ttu-id="36b3c-127">Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet.</span><span class="sxs-lookup"><span data-stu-id="36b3c-127">Specifies whether the pipeline applies mark-in at this node.</span></span>                                                                                             |
| [<span data-ttu-id="36b3c-128">**MF \_ toponode \_ markout \_ hier**</span><span class="sxs-lookup"><span data-stu-id="36b3c-128">**MF\_TOPONODE\_MARKOUT\_HERE**</span></span>](mf-toponode-markout-here-attribute.md)       | <span data-ttu-id="36b3c-129">Gibt an, ob die Pipeline auf diesem Knoten ein Markierungszeichen anwendet.</span><span class="sxs-lookup"><span data-stu-id="36b3c-129">Specifies whether the pipeline applies mark-out at this node.</span></span>                                                                                            |



 

## <a name="source-node-attributes"></a><span data-ttu-id="36b3c-130">Quellknoten Attribute</span><span class="sxs-lookup"><span data-stu-id="36b3c-130">Source Node Attributes</span></span>



| <span data-ttu-id="36b3c-131">Attribut</span><span class="sxs-lookup"><span data-stu-id="36b3c-131">Attribute</span></span>                                                                                       | <span data-ttu-id="36b3c-132">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36b3c-132">Description</span></span>                                                                                                       |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36b3c-133">**MF \_ toponode \_ mediastart**</span><span class="sxs-lookup"><span data-stu-id="36b3c-133">**MF\_TOPONODE\_MEDIASTART**</span></span>](mf-toponode-mediastart-attribute.md)                            | <span data-ttu-id="36b3c-134">Gibt die Startzeit einer Präsentation in Relation zum Start der Medien Quelldatei in 100-Nanosecond-Einheiten an.</span><span class="sxs-lookup"><span data-stu-id="36b3c-134">Specifies the start time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span> |
| [<span data-ttu-id="36b3c-135">**MF- \_ toponode- \_ mediastop**</span><span class="sxs-lookup"><span data-stu-id="36b3c-135">**MF\_TOPONODE\_MEDIASTOP**</span></span>](mf-toponode-mediastop-attribute.md)                              | <span data-ttu-id="36b3c-136">Gibt die Endzeit einer Präsentation in 100-Nanosecond-Einheiten relativ zum Start der Medien Quelldatei an.</span><span class="sxs-lookup"><span data-stu-id="36b3c-136">Specifies the stop time of a presentation, relative to the start the media source file, in 100-nanosecond units.</span></span>  |
| [<span data-ttu-id="36b3c-137">**MF- \_ toponode- \_ Präsentations \_ Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="36b3c-137">**MF\_TOPONODE\_PRESENTATION\_DESCRIPTOR**</span></span>](mf-toponode-presentation-descriptor-attribute.md) | <span data-ttu-id="36b3c-138">Enthält einen Zeiger auf den Präsentations Deskriptor für die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="36b3c-138">Contains a pointer to the presentation descriptor for the media source.</span></span>                                           |
| [<span data-ttu-id="36b3c-139">**Element-ID der MF \_ -toponode \_ \_ -Sequenz**</span><span class="sxs-lookup"><span data-stu-id="36b3c-139">**MF\_TOPONODE\_SEQUENCE\_ELEMENTID**</span></span>](mf-toponode-sequence-elementid-attribute.md)           | <span data-ttu-id="36b3c-140">Gibt das Element an, das einen Quellknoten enthält.</span><span class="sxs-lookup"><span data-stu-id="36b3c-140">Specifies the element that contains a source node.</span></span>                                                                |
| [<span data-ttu-id="36b3c-141">**MF- \_ toponode- \_ Quelle**</span><span class="sxs-lookup"><span data-stu-id="36b3c-141">**MF\_TOPONODE\_SOURCE**</span></span>](mf-toponode-source-attribute.md)                                    | <span data-ttu-id="36b3c-142">Enthält einen Zeiger auf die Medienquelle, die einem topologieknoten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="36b3c-142">Contains a pointer to the media source associated with a topology node.</span></span>                                           |
| [<span data-ttu-id="36b3c-143">**MF- \_ toponode-Daten \_ Strom \_ Deskriptor**</span><span class="sxs-lookup"><span data-stu-id="36b3c-143">**MF\_TOPONODE\_STREAM\_DESCRIPTOR**</span></span>](mf-toponode-stream-descriptor-attribute.md)             | <span data-ttu-id="36b3c-144">Enthält einen Zeiger auf den Datenstrom Deskriptor für die Medienquelle.</span><span class="sxs-lookup"><span data-stu-id="36b3c-144">Contains a pointer to the stream descriptor for the media source.</span></span>                                                 |
| [<span data-ttu-id="36b3c-145">**MF- \_ toponode- \_ workwarteschlangen- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="36b3c-145">**MF\_TOPONODE\_WORKQUEUE\_ID**</span></span>](mf-toponode-workqueue-id-attribute.md)                       | <span data-ttu-id="36b3c-146">Gibt eine Arbeits Warteschlange für einen topologieknoten an.</span><span class="sxs-lookup"><span data-stu-id="36b3c-146">Specifies a work queue for a topology node.</span></span>                                                                       |
| [<span data-ttu-id="36b3c-147">**MF \_ toponode \_ workqueue \_ MMCSS- \_ Klasse**</span><span class="sxs-lookup"><span data-stu-id="36b3c-147">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_CLASS**</span></span>](mf-toponode-workqueue-mmcss-class-attribute.md)    | <span data-ttu-id="36b3c-148">Gibt eine MMCSS-Aufgabe (Multimedia Class Scheduler Service) für einen topologieknoten an.</span><span class="sxs-lookup"><span data-stu-id="36b3c-148">Specifies a Multimedia Class Scheduler Service (MMCSS) task for a topology node.</span></span>                                  |
| [<span data-ttu-id="36b3c-149">**MF \_ toponode \_ workqueue \_ MMCSS \_ TaskID**</span><span class="sxs-lookup"><span data-stu-id="36b3c-149">**MF\_TOPONODE\_WORKQUEUE\_MMCSS\_TASKID**</span></span>](mf-toponode-workqueue-mmcss-taskid-attribute.md)  | <span data-ttu-id="36b3c-150">Gibt einen MMCSS-Task Bezeichner für einen topologieknoten an.</span><span class="sxs-lookup"><span data-stu-id="36b3c-150">Specifies a MMCSS task identifier for a topology node.</span></span>                                                            |



 

## <a name="transform-node-attributes"></a><span data-ttu-id="36b3c-151">Knoten Attribute transformieren</span><span class="sxs-lookup"><span data-stu-id="36b3c-151">Transform Node Attributes</span></span>



| <span data-ttu-id="36b3c-152">Attribut</span><span class="sxs-lookup"><span data-stu-id="36b3c-152">Attribute</span></span>                                                                             | <span data-ttu-id="36b3c-153">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36b3c-153">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36b3c-154">**MF- \_ toponode \_ D3DAWARE**</span><span class="sxs-lookup"><span data-stu-id="36b3c-154">**MF\_TOPONODE\_D3DAWARE**</span></span>](mf-toponode-d3daware-attribute.md)                      | <span data-ttu-id="36b3c-155">Gibt an, ob die einem topologieknoten zugeordnete Transformation die DirectX-Video Beschleunigung (DXVA) unterstützt.</span><span class="sxs-lookup"><span data-stu-id="36b3c-155">Specifies whether the transform associated with a topology node supports DirectX Video Acceleration (DXVA)</span></span> |
| [<span data-ttu-id="36b3c-156">**MF- \_ toponode- \_ Ableitung**</span><span class="sxs-lookup"><span data-stu-id="36b3c-156">**MF\_TOPONODE\_DRAIN**</span></span>](mf-toponode-drain-attribute.md)                            | <span data-ttu-id="36b3c-157">Gibt an, wann eine Transformation entladen wird.</span><span class="sxs-lookup"><span data-stu-id="36b3c-157">Specifies when a transform is drained.</span></span>                                                                     |
| [<span data-ttu-id="36b3c-158">**MF- \_ toponode-Leerung \_**</span><span class="sxs-lookup"><span data-stu-id="36b3c-158">**MF\_TOPONODE\_FLUSH**</span></span>](mf-toponode-flush-attribute.md)                            | <span data-ttu-id="36b3c-159">Gibt an, wann eine Transformation geleert wird.</span><span class="sxs-lookup"><span data-stu-id="36b3c-159">Specifies when a transform is flushed.</span></span>                                                                     |
| [<span data-ttu-id="36b3c-160">**MF \_ toponode \_ Transform \_ objectID**</span><span class="sxs-lookup"><span data-stu-id="36b3c-160">**MF\_TOPONODE\_TRANSFORM\_OBJECTID**</span></span>](mf-toponode-transform-objectid-attribute.md) | <span data-ttu-id="36b3c-161">Der Klassen Bezeichner (CLSID) der diesem topologieknoten zugeordneten Transformation.</span><span class="sxs-lookup"><span data-stu-id="36b3c-161">The class identifier (CLSID) of the transform associated with this topology node.</span></span>                          |



 

## <a name="output-node-attributes"></a><span data-ttu-id="36b3c-162">Ausgabe Knoten Attribute</span><span class="sxs-lookup"><span data-stu-id="36b3c-162">Output Node Attributes</span></span>



| <span data-ttu-id="36b3c-163">Attribut</span><span class="sxs-lookup"><span data-stu-id="36b3c-163">Attribute</span></span>                                                                                  | <span data-ttu-id="36b3c-164">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36b3c-164">Description</span></span>                                                                                                      |
|--------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="36b3c-165">**MF- \_ toponode \_ Deaktivieren von \_ Preroll**</span><span class="sxs-lookup"><span data-stu-id="36b3c-165">**MF\_TOPONODE\_DISABLE\_PREROLL**</span></span>](mf-toponode-disable-preroll-attribute.md)            | <span data-ttu-id="36b3c-166">Gibt an, ob die Medien Sitzung vorab auf der Medien Senke, die durch diesen topologieknoten dargestellt wird, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="36b3c-166">Specifies whether the Media Session uses preroll on the media sink represented by this topology node.</span></span>            |
| [<span data-ttu-id="36b3c-167">**MF \_ toponode \_ noshutdown \_ beim \_ Entfernen**</span><span class="sxs-lookup"><span data-stu-id="36b3c-167">**MF\_TOPONODE\_NOSHUTDOWN\_ON\_REMOVE**</span></span>](mf-toponode-noshutdown-on-remove-attribute.md) | <span data-ttu-id="36b3c-168">Gibt an, ob die Medien Sitzung beim Entfernen des Ausgabe Knotens aus der Topologie von der Medien-Senke heruntergefahren wird.</span><span class="sxs-lookup"><span data-stu-id="36b3c-168">Specifies whether the Media Session shuts down the media sink when the output node is removed from the topology.</span></span> |
| [<span data-ttu-id="36b3c-169">**MF- \_ toponode- \_ Rate**</span><span class="sxs-lookup"><span data-stu-id="36b3c-169">**MF\_TOPONODE\_RATELESS**</span></span>](mf-toponode-rateless-attribute.md)                           | <span data-ttu-id="36b3c-170">Gibt an, ob die Medien Senke, die diesem topologieknoten zugeordnet ist, ratlos ist.</span><span class="sxs-lookup"><span data-stu-id="36b3c-170">Specifies whether the media sink associated with this topology node is rateless.</span></span>                                 |
| [<span data-ttu-id="36b3c-171">**MF- \_ toponode- \_ streamid**</span><span class="sxs-lookup"><span data-stu-id="36b3c-171">**MF\_TOPONODE\_STREAMID**</span></span>](mf-toponode-streamid-attribute.md)                           | <span data-ttu-id="36b3c-172">Der Datenstrom Bezeichner der Stream-Senke, die diesem topologieknoten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="36b3c-172">The stream identifier of the stream sink associated with this topology node.</span></span>                                     |



 

## <a name="tee-node-attributes"></a><span data-ttu-id="36b3c-173">Tee-Knoten Attribute</span><span class="sxs-lookup"><span data-stu-id="36b3c-173">Tee Node Attributes</span></span>



| <span data-ttu-id="36b3c-174">Attribut</span><span class="sxs-lookup"><span data-stu-id="36b3c-174">Attribute</span></span>                                                                  | <span data-ttu-id="36b3c-175">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="36b3c-175">Description</span></span>                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------|
| [<span data-ttu-id="36b3c-176">**MF \_ toponode \_ primaryoutput**</span><span class="sxs-lookup"><span data-stu-id="36b3c-176">**MF\_TOPONODE\_PRIMARYOUTPUT**</span></span>](mf-toponode-primaryoutput-attribute.md) | <span data-ttu-id="36b3c-177">Gibt an, welche Ausgabe die primäre Ausgabe auf einem Tee-Knoten ist.</span><span class="sxs-lookup"><span data-stu-id="36b3c-177">Indicates which output is the primary output on a tee node.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="36b3c-178">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="36b3c-178">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="36b3c-179">**Imftopologynode**</span><span class="sxs-lookup"><span data-stu-id="36b3c-179">**IMFTopologyNode**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imftopologynode)
</dt> <dt>

[<span data-ttu-id="36b3c-180">Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="36b3c-180">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="36b3c-181">Topologieattribute</span><span class="sxs-lookup"><span data-stu-id="36b3c-181">Topology Attributes</span></span>](topology-attributes.md)
</dt> </dl>

 

 



