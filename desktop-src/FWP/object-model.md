---
title: Objektmodell
description: In der folgenden Tabelle sind die Objekttypen aufgelistet, die durch die verschiedenen von der Windows-Filter Plattform (WFP) bereitgestellten API-Sätze bearbeitet werden können.
ms.assetid: 6931583f-785c-4e27-b5e4-d185d23a54ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa90b4757a39617616c6f83b6b79fe322b2e64c8
ms.sourcegitcommit: 60ad94096619da5476f9bbcd4cc231b40b6f5358
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104038600"
---
# <a name="object-model"></a><span data-ttu-id="310f0-103">Objektmodell</span><span class="sxs-lookup"><span data-stu-id="310f0-103">Object Model</span></span>

<span data-ttu-id="310f0-104">In der folgenden Tabelle sind die Objekttypen aufgelistet, die durch die verschiedenen von der Windows-Filter Plattform (WFP) bereitgestellten API-Sätze bearbeitet werden können.</span><span class="sxs-lookup"><span data-stu-id="310f0-104">The following table lists the object types that can be manipulated through the various API sets supplied by the Windows Filtering Platform (WFP).</span></span>



<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="310f0-105">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="310f0-105">Object Type</span></span></th>
<th><span data-ttu-id="310f0-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="310f0-106">Description</span></span></th>
<th><span data-ttu-id="310f0-107">Beispiel Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="310f0-107">Sample Properties</span></span></th>
<th><span data-ttu-id="310f0-108">Beispiel</span><span class="sxs-lookup"><span data-stu-id="310f0-108">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="310f0-109">Filter</span><span class="sxs-lookup"><span data-stu-id="310f0-109">Filter</span></span></td>
<td><span data-ttu-id="310f0-110">Eine Regel, die die Klassifizierung regelt.</span><span class="sxs-lookup"><span data-stu-id="310f0-110">A rule that governs classification.</span></span> <span data-ttu-id="310f0-111">Wenn die Bedingungen erfüllt sind, wird die Aktion aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="310f0-111">If the conditions are met, the action is invoked.</span></span> <br/> <span data-ttu-id="310f0-112">Dies ist das komplexeste Objekt, das von WFP verfügbar gemacht wird, da alle anderen Objekttypen miteinander verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="310f0-112">This is the most complex object exposed by WFP since it ties together all the other object types.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="310f0-113">Array von Bedingungen</span><span class="sxs-lookup"><span data-stu-id="310f0-113">Array of conditions</span></span></li>
<li><span data-ttu-id="310f0-114">Aktion (zulassen, blockieren, Legenden)</span><span class="sxs-lookup"><span data-stu-id="310f0-114">Action (Permit, Block, Callout)</span></span></li>
<li><span data-ttu-id="310f0-115"><a href="filter-weight-assignment.md">Weight</a></span><span class="sxs-lookup"><span data-stu-id="310f0-115"><a href="filter-weight-assignment.md">Weight</a></span></span></li>
<li><span data-ttu-id="310f0-116">Kontext</span><span class="sxs-lookup"><span data-stu-id="310f0-116">Context</span></span></li>
</ul></td>
<td><span data-ttu-id="310f0-117">&quot;Blockieren Sie den Datenverkehr mit einem TCP-Port größer als 1024.&quot;</span><span class="sxs-lookup"><span data-stu-id="310f0-117">&quot;Block traffic with a TCP port greater than 1024.&quot;</span></span> <br/> <span data-ttu-id="310f0-118">&quot;Gibt für den gesamten Datenverkehr, der nicht gesichert ist, IDs an.&quot;</span><span class="sxs-lookup"><span data-stu-id="310f0-118">&quot;Callout to IDS for all traffic that is not secured.&quot;</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="310f0-119">Legende</span><span class="sxs-lookup"><span data-stu-id="310f0-119">Callout</span></span></td>
<td><span data-ttu-id="310f0-120">Eine Reihe von Funktionen, die am Klassifizierungsprozess teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="310f0-120">A set of functions that participate in the classification process.</span></span><br/> <span data-ttu-id="310f0-121">Dadurch kann die benutzerdefinierte Paketverarbeitung ausgeführt werden, wenn bestimmte Bedingungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="310f0-121">It allows for custom packet processing to be done when certain conditions are met.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="310f0-122">id</span><span class="sxs-lookup"><span data-stu-id="310f0-122">ID</span></span></li>
<li><span data-ttu-id="310f0-123">Anwendbare Ebene</span><span class="sxs-lookup"><span data-stu-id="310f0-123">Applicable layer</span></span></li>
</ul></td>
<td><span data-ttu-id="310f0-124">Der NAT-Treiber</span><span class="sxs-lookup"><span data-stu-id="310f0-124">The NAT driver</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="310f0-125">Ebene</span><span class="sxs-lookup"><span data-stu-id="310f0-125">Layer</span></span></td>
<td><span data-ttu-id="310f0-126">Ein Filter Container in der Filter-Engine.</span><span class="sxs-lookup"><span data-stu-id="310f0-126">A filter container in the filter engine.</span></span> <br/> <span data-ttu-id="310f0-127">Stellt einen bestimmten Punkt in der Verarbeitung des Netzwerk Datenverkehrs dar, bei dem die Filter-Engine aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="310f0-127">Represents a specific point in network traffic processing where the filter engine is invoked.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="310f0-128">Schema für Filter, die der Ebene hinzugefügt werden können</span><span class="sxs-lookup"><span data-stu-id="310f0-128">Schema for filters that can be added to the layer</span></span></li>
</ul></td>
<td><span data-ttu-id="310f0-129">Die eingehende Transport Schicht</span><span class="sxs-lookup"><span data-stu-id="310f0-129">The Inbound Transport Layer</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="310f0-130">Unterebene</span><span class="sxs-lookup"><span data-stu-id="310f0-130">Sub-layer</span></span></td>
<td><span data-ttu-id="310f0-131">Eine untergeordnete Komponente einer Ebene, die bei der <a href="filter-arbitration.md">Filterung von Filtern</a>verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="310f0-131">A sub-component of a layer, used in <a href="filter-arbitration.md">filter arbitration</a>.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="310f0-132">Weight</span><span class="sxs-lookup"><span data-stu-id="310f0-132">Weight</span></span></li>
</ul></td>
<td><span data-ttu-id="310f0-133">Die IPSec-Tunnel Unterschicht</span><span class="sxs-lookup"><span data-stu-id="310f0-133">The IPsec Tunnel sub-layer</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="310f0-134">Anbieter</span><span class="sxs-lookup"><span data-stu-id="310f0-134">Provider</span></span></td>
<td><span data-ttu-id="310f0-135">Ein Richtlinien Anbieter, der eine Lösung auf WFP erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="310f0-135">A policy provider that has built a solution on WFP.</span></span><br/> <span data-ttu-id="310f0-136">Sie wird ausschließlich zur Verwaltung verwendet. Sie wirkt sich nicht auf die Lauf Zeit Paketverarbeitung aus.</span><span class="sxs-lookup"><span data-stu-id="310f0-136">It is used solely for management; it does not affect run-time packet processing.</span></span><br/></td>
<td><ul>
<li><span data-ttu-id="310f0-137">id</span><span class="sxs-lookup"><span data-stu-id="310f0-137">ID</span></span></li>
<li><span data-ttu-id="310f0-138">Dienstname</span><span class="sxs-lookup"><span data-stu-id="310f0-138">Service name</span></span></li>
</ul></td>
<td><span data-ttu-id="310f0-139">Windows-Firewall mit erweiterter Sicherheit</span><span class="sxs-lookup"><span data-stu-id="310f0-139">Windows Firewall with Advanced Security</span></span><br/> <span data-ttu-id="310f0-140">Eine Drittanbieter-URL-Filterungs Anwendung</span><span class="sxs-lookup"><span data-stu-id="310f0-140">A 3rd-party URL filtering application</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="310f0-141">Anbieter Kontext</span><span class="sxs-lookup"><span data-stu-id="310f0-141">Provider Context</span></span></td>
<td><span data-ttu-id="310f0-142">Ein Daten-BLOB, das von einem Richtlinien Anbieter zum Speichern beliebiger Kontextinformationen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="310f0-142">A data blob used by a policy provider to store arbitrary context information.</span></span> <br/> <span data-ttu-id="310f0-143">Es wird verwendet, um benutzerdefinierte Konfigurationsinformationen an eine Legende zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="310f0-143">It is used to pass custom configuration information to a callout.</span></span><br/> <span data-ttu-id="310f0-144">Die gängigste Methode, die Kontextinformationen zu verwenden, besteht darin, dass Filter auf einen Anbieter Kontext verweisen.</span><span class="sxs-lookup"><span data-stu-id="310f0-144">The most common way to use the context information is to have filters reference a provider context.</span></span> <br/></td>
<td><ul>
<li><span data-ttu-id="310f0-145">id</span><span class="sxs-lookup"><span data-stu-id="310f0-145">ID</span></span></li>
<li><span data-ttu-id="310f0-146">Datenblob</span><span class="sxs-lookup"><span data-stu-id="310f0-146">Data blob</span></span></li>
</ul></td>
<td><span data-ttu-id="310f0-147">IPSec speichert Authentifizierungs Einstellungen in der Basis Filter-Engine (BFE).</span><span class="sxs-lookup"><span data-stu-id="310f0-147">IPsec stores authentication settings in the Base Filtering Engine ( BFE).</span></span> <span data-ttu-id="310f0-148">Die &quot; Kontext &quot; Eigenschaft eines Filters gibt die Authentifizierungs Einstellungen an, die für den Datenverkehr verwendet werden sollen, der vom Filter beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="310f0-148">The &quot;Context&quot; property of a filter indicates the authentication settings to use for the traffic that the filter describes.</span></span><br/> <span data-ttu-id="310f0-149">Der SSL-zertifizierungsauswahl-Shim speichert Zertifizierungs Informationen in einem Anbieter Kontext.</span><span class="sxs-lookup"><span data-stu-id="310f0-149">The SSL certification selection shim will store certification information in a provider context.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="310f0-150">Die von der WFP-API verfügbar gemachten Objekttypen haben eine konsistente Semantik.</span><span class="sxs-lookup"><span data-stu-id="310f0-150">The object types exposed by WFP API have consistent semantics.</span></span> <span data-ttu-id="310f0-151">Die Aktionen von Add, Enumerate, subscribe usw. sind für alle Objekttypen ähnlich.</span><span class="sxs-lookup"><span data-stu-id="310f0-151">The actions of add, enumerate, subscribe, and so on are similar for all object types.</span></span>

<span data-ttu-id="310f0-152">Jeder Objekttyp wird durch eine Datenstruktur dargestellt (z. b. " [**f \_ FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)").</span><span class="sxs-lookup"><span data-stu-id="310f0-152">Each object type is represented by a data structure (for example, [**FWPM\_FILTER0**](/windows/desktop/api/Fwpmtypes/ns-fwpmtypes-fwpm_filter0)).</span></span> <span data-ttu-id="310f0-153">Um die Anzahl der unterschiedlichen Datenstrukturen zu minimieren, die von der WFP-API verfügbar gemacht werden, wird die gleiche Datenstruktur sowohl für das Hinzufügen neuer Objekte als auch für das Abrufen vorhandener Objekte verwendet.</span><span class="sxs-lookup"><span data-stu-id="310f0-153">In order to minimize the number of different data structures exposed by the WFP API, the same data structure is used for both adding new objects and retrieving existing ones.</span></span> <span data-ttu-id="310f0-154">Daher können in jeder Datenstruktur Felder vorhanden sein, die beim Hinzufügen eines neuen Objekts ignoriert werden, da diese Felder von der Basis Filter-Engine (BFE) und nicht vom Aufrufer ausgefüllt werden.</span><span class="sxs-lookup"><span data-stu-id="310f0-154">Thus, there may be fields in each data structure that are ignored when adding a new object since these fields are filled in by the Base Filtering Engine (BFE), and not by the caller.</span></span> <span data-ttu-id="310f0-155">Beispielsweise verfügt eine **\_ FILTER0** -Datenstruktur vom Typ " **filterid** " über ein Feld "filterid", das die **LUID** der entsprechenden "f"- **\_ FILTER0** enthält.</span><span class="sxs-lookup"><span data-stu-id="310f0-155">For example, an **FWPM\_FILTER0** data structure has a **filterId** field that contains the **LUID** of the corresponding **FWPS\_FILTER0**.</span></span> <span data-ttu-id="310f0-156">Diese **LUID** wird von BFE zugewiesen, und dieses Feld wird daher im [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0)-Aufrufe ignoriert.</span><span class="sxs-lookup"><span data-stu-id="310f0-156">This **LUID** is assigned by BFE, and thus, this field is ignored in the call to [**FwpmFilterAdd0**](/windows/desktop/api/Fwpmu/nf-fwpmu-fwpmfilteradd0).</span></span>

## <a name="related-topics"></a><span data-ttu-id="310f0-157">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="310f0-157">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="310f0-158">Objekt Verwaltung</span><span class="sxs-lookup"><span data-stu-id="310f0-158">Object Management</span></span>](object-management.md)
</dt> </dl>

 

 





