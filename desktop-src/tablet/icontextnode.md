---
description: Stellt einen Knoten in einer Struktur von Objekten dar, die als Teil der frei Hand Analyse erstellt werden.
ms.assetid: 44ef4401-cb14-4348-9ed8-b11a40d04940
title: Icontextnode-Schnittstelle (iacom. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 2dbc9d7a0c1cc6ededf5d59585c806b54d6cfa32
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104041763"
---
# <a name="icontextnode-interface"></a><span data-ttu-id="afcac-103">Icontextnode-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="afcac-103">IContextNode interface</span></span>

<span data-ttu-id="afcac-104">Stellt einen Knoten in einer Struktur von Objekten dar, die als Teil der frei Hand Analyse erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="afcac-104">Represents a node in a tree of objects that are created as part of ink analysis.</span></span>

## <a name="members"></a><span data-ttu-id="afcac-105">Member</span><span class="sxs-lookup"><span data-stu-id="afcac-105">Members</span></span>

<span data-ttu-id="afcac-106">Die **icontextnode** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="afcac-106">The **IContextNode** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="afcac-107">**Icontextnode** verfügt auch über die folgenden Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="afcac-107">**IContextNode** also has these types of members:</span></span>

-   [<span data-ttu-id="afcac-108">Methoden</span><span class="sxs-lookup"><span data-stu-id="afcac-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="afcac-109">Methoden</span><span class="sxs-lookup"><span data-stu-id="afcac-109">Methods</span></span>

<span data-ttu-id="afcac-110">Die **icontextnode** -Schnittstelle verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="afcac-110">The **IContextNode** interface has these methods.</span></span>



| <span data-ttu-id="afcac-111">Methode</span><span class="sxs-lookup"><span data-stu-id="afcac-111">Method</span></span>                                                                                  | <span data-ttu-id="afcac-112">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="afcac-112">Description</span></span>                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="afcac-113">**Addcontextlink**</span><span class="sxs-lookup"><span data-stu-id="afcac-113">**AddContextLink**</span></span>](icontextnode-addcontextlink.md)                                   | <span data-ttu-id="afcac-114">Fügt der Kontext Link Auflistung des **icontextnode** -Objekts einen neuen [**icontextlink**](icontextlink.md) hinzu.</span><span class="sxs-lookup"><span data-stu-id="afcac-114">Adds a new [**IContextLink**](icontextlink.md) to the **IContextNode** object's context link collection.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="afcac-115">**AddPropertyData**</span><span class="sxs-lookup"><span data-stu-id="afcac-115">**AddPropertyData**</span></span>](icontextnode-addpropertydata.md)                                 | <span data-ttu-id="afcac-116">Fügt eine bestimmte anwendungsspezifische Daten hinzu.</span><span class="sxs-lookup"><span data-stu-id="afcac-116">Adds a piece of application-specific data.</span></span><br/>                                                                                                                                                                         |
| [<span data-ttu-id="afcac-117">**Confirm**</span><span class="sxs-lookup"><span data-stu-id="afcac-117">**Confirm**</span></span>](icontextnode-confirm.md)                                                 | <span data-ttu-id="afcac-118">Ändert den bestäalisierungstyp, der steuert, was das [**iinkanalyzer**](iinkanalyzer.md) -Objekt über den **icontextnode** ändern kann.</span><span class="sxs-lookup"><span data-stu-id="afcac-118">Modifies the confirmation type, which controls what the [**IInkAnalyzer**](iinkanalyzer.md) object can change about the **IContextNode**.</span></span><br/>                                                                         |
| [<span data-ttu-id="afcac-119">**ContainsPropertyData**</span><span class="sxs-lookup"><span data-stu-id="afcac-119">**ContainsPropertyData**</span></span>](icontextnode-containspropertydata.md)                       | <span data-ttu-id="afcac-120">Bestimmt, ob das **icontextnode** -Objektdaten enthält, die unter dem angegebenen Bezeichner gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="afcac-120">Determines whether the **IContextNode** object contains data stored under the specified identifier.</span></span><br/>                                                                                                                |
| [<span data-ttu-id="afcac-121">**"Kreatepartiallypopulatedsubnode"**</span><span class="sxs-lookup"><span data-stu-id="afcac-121">**CreatePartiallyPopulatedSubNode**</span></span>](icontextnode-createpartiallypopulatedsubnode.md) | <span data-ttu-id="afcac-122">Erstellt ein untergeordnetes **icontextnode** -Objekt, das nur Informationen zu Typ, Bezeichner und Speicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="afcac-122">Creates a child **IContextNode** object that contains only information on type, identifier, and location.</span></span><br/>                                                                                                          |
| [<span data-ttu-id="afcac-123">**"Kreatesubnode"**</span><span class="sxs-lookup"><span data-stu-id="afcac-123">**CreateSubNode**</span></span>](icontextnode-createsubnode.md)                                     | <span data-ttu-id="afcac-124">Erstellt ein neues untergeordnetes **icontextnode** -Objekt.</span><span class="sxs-lookup"><span data-stu-id="afcac-124">Creates a new child **IContextNode** object.</span></span><br/>                                                                                                                                                                       |
| [<span data-ttu-id="afcac-125">**Deletecontextlink**</span><span class="sxs-lookup"><span data-stu-id="afcac-125">**DeleteContextLink**</span></span>](icontextnode-deletecontextlink.md)                             | <span data-ttu-id="afcac-126">Löscht ein [**icontextlink**](icontextlink.md) -Objekt aus der Link Auflistung des **icontextnode** -Objekts.</span><span class="sxs-lookup"><span data-stu-id="afcac-126">Deletes an [**IContextLink**](icontextlink.md) object from the **IContextNode** object's link collection.</span></span><br/>                                                                                                         |
| [<span data-ttu-id="afcac-127">**Delta esubnode**</span><span class="sxs-lookup"><span data-stu-id="afcac-127">**DeleteSubNode**</span></span>](icontextnode-deletesubnode.md)                                     | <span data-ttu-id="afcac-128">Entfernt einen untergeordneten **icontextnode**.</span><span class="sxs-lookup"><span data-stu-id="afcac-128">Removes a child **IContextNode**.</span></span><br/>                                                                                                                                                                                  |
| [<span data-ttu-id="afcac-129">**Getcontextlinks**</span><span class="sxs-lookup"><span data-stu-id="afcac-129">**GetContextLinks**</span></span>](icontextnode-getcontextlinks.md)                                 | <span data-ttu-id="afcac-130">Ruft eine Auflistung von [**icontextlink**](icontextlink.md) -Objekten ab, die Beziehungen mit anderen **icontextnode** -Objekten darstellt.</span><span class="sxs-lookup"><span data-stu-id="afcac-130">Retrieves a collection of [**IContextLink**](icontextlink.md) objects that represents relationships with other **IContextNode** objects.</span></span><br/>                                                                          |
| [<span data-ttu-id="afcac-131">**GetId**</span><span class="sxs-lookup"><span data-stu-id="afcac-131">**GetId**</span></span>](icontextnode-getid.md)                                                     | <span data-ttu-id="afcac-132">Ruft den Bezeichner für das **icontextnode** -Objekt ab.</span><span class="sxs-lookup"><span data-stu-id="afcac-132">Retrieves the identifier for the **IContextNode** object.</span></span><br/>                                                                                                                                                          |
| [<span data-ttu-id="afcac-133">**GetLocation**</span><span class="sxs-lookup"><span data-stu-id="afcac-133">**GetLocation**</span></span>](icontextnode-getlocation.md)                                         | <span data-ttu-id="afcac-134">Ruft die Position und die Größe des **icontextnode** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="afcac-134">Retrieves the position and size of the **IContextNode** object.</span></span><br/>                                                                                                                                                    |
| [<span data-ttu-id="afcac-135">**Getparameentnode**</span><span class="sxs-lookup"><span data-stu-id="afcac-135">**GetParentNode**</span></span>](icontextnode-getparentnode.md)                                     | <span data-ttu-id="afcac-136">Ruft den übergeordneten Knoten dieses **icontextnode** in der Kontext Knoten Struktur ab.</span><span class="sxs-lookup"><span data-stu-id="afcac-136">Retrieves the parent node of this **IContextNode** in the context node tree.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="afcac-137">**Getpartiallyausgefüllt**</span><span class="sxs-lookup"><span data-stu-id="afcac-137">**GetPartiallyPopulated**</span></span>](icontextnode-getpartiallypopulated.md)                     | <span data-ttu-id="afcac-138">Ruft den Wert ab, der angibt, ob ein **icontextnode** -Objekt teilweise aufgefüllt oder vollständig ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="afcac-138">Retrieves the value that indicates whether an **IContextNode** object is partially populated or fully populated.</span></span><br/>                                                                                                   |
| [<span data-ttu-id="afcac-139">**GetPropertyData**</span><span class="sxs-lookup"><span data-stu-id="afcac-139">**GetPropertyData**</span></span>](icontextnode-getpropertydata.md)                                 | <span data-ttu-id="afcac-140">Ruft anwendungsspezifische Daten oder andere Eigenschafts Daten mit dem angegebenen Bezeichner ab.</span><span class="sxs-lookup"><span data-stu-id="afcac-140">Retrieves application-specific data or other property data given the specified identifier.</span></span><br/>                                                                                                                         |
| [<span data-ttu-id="afcac-141">**GetPropertyDataIds**</span><span class="sxs-lookup"><span data-stu-id="afcac-141">**GetPropertyDataIds**</span></span>](icontextnode-getpropertydataids.md)                           | <span data-ttu-id="afcac-142">Ruft die Bezeichner ab, für die Eigenschafts Daten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="afcac-142">Retrieves the identifiers for which there is property data.</span></span><br/>                                                                                                                                                        |
| [<span data-ttu-id="afcac-143">**Getstrokecount**</span><span class="sxs-lookup"><span data-stu-id="afcac-143">**GetStrokeCount**</span></span>](icontextnode-getstrokecount.md)                                   | <span data-ttu-id="afcac-144">Ruft die Anzahl der Striche ab, die dem **icontextnode** -Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="afcac-144">Retrieves the number of strokes associated with the **IContextNode** object.</span></span><br/>                                                                                                                                       |
| [<span data-ttu-id="afcac-145">**Getstrokeid**</span><span class="sxs-lookup"><span data-stu-id="afcac-145">**GetStrokeId**</span></span>](icontextnode-getstrokeid.md)                                         | <span data-ttu-id="afcac-146">Ruft den Strich Bezeichner für den Strich ab, auf den durch einen Indexwert im **icontextnode** -Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="afcac-146">Retrieves the stroke identifier for the stroke referenced by an index value within the **IContextNode** object.</span></span><br/>                                                                                                    |
| [<span data-ttu-id="afcac-147">**GetStrokeIds**</span><span class="sxs-lookup"><span data-stu-id="afcac-147">**GetStrokeIds**</span></span>](icontextnode-getstrokeids.md)                                       | <span data-ttu-id="afcac-148">Ruft ein Array von bezeichern für die Striche innerhalb des **icontextnode** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="afcac-148">Retrieves an array of identifiers for the strokes within the **IContextNode** object.</span></span><br/>                                                                                                                              |
| [<span data-ttu-id="afcac-149">**Getstrokepacketdatabyid**</span><span class="sxs-lookup"><span data-stu-id="afcac-149">**GetStrokePacketDataById**</span></span>](icontextnode-getstrokepacketdatabyid.md)                 | <span data-ttu-id="afcac-150">Ruft ein Array ab, das die Paket Eigenschafts Daten für den angegebenen Strich enthält.</span><span class="sxs-lookup"><span data-stu-id="afcac-150">Retrieves an array containing the packet property data for the specified stroke.</span></span><br/>                                                                                                                                   |
| [<span data-ttu-id="afcac-151">**Getstrokepacketdescriptionbyid**</span><span class="sxs-lookup"><span data-stu-id="afcac-151">**GetStrokePacketDescriptionById**</span></span>](icontextnode-getstrokepacketdescriptionbyid.md)   | <span data-ttu-id="afcac-152">Ruft ein Array ab, das die Paket Eigenschaften Bezeichner für den angegebenen Strich enthält.</span><span class="sxs-lookup"><span data-stu-id="afcac-152">Retrieves an array containing the packet property identifiers for the specified stroke.</span></span><br/>                                                                                                                            |
| [<span data-ttu-id="afcac-153">**Getsubnodes**</span><span class="sxs-lookup"><span data-stu-id="afcac-153">**GetSubNodes**</span></span>](icontextnode-getsubnodes.md)                                         | <span data-ttu-id="afcac-154">Ruft die direkt untergeordneten Knoten des **icontextnode** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="afcac-154">Retrieves the direct child nodes of the **IContextNode** object.</span></span><br/>                                                                                                                                                   |
| [<span data-ttu-id="afcac-155">**GetType**</span><span class="sxs-lookup"><span data-stu-id="afcac-155">**GetType**</span></span>](icontextnode-gettype.md)                                                 | <span data-ttu-id="afcac-156">Ruft den Typ des **icontextnode** -Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="afcac-156">Retrieves the type of the **IContextNode** object.</span></span><br/>                                                                                                                                                                 |
| [<span data-ttu-id="afcac-157">**Gettyname**</span><span class="sxs-lookup"><span data-stu-id="afcac-157">**GetTypeName**</span></span>](icontextnode-gettypename.md)                                         | <span data-ttu-id="afcac-158">Ruft einen lesbaren Typnamen dieses **icontextnode** ab.</span><span class="sxs-lookup"><span data-stu-id="afcac-158">Retrieves a human-readable type name of this **IContextNode**.</span></span><br/>                                                                                                                                                     |
| [<span data-ttu-id="afcac-159">**Isbestätigt**</span><span class="sxs-lookup"><span data-stu-id="afcac-159">**IsConfirmed**</span></span>](icontextnode-isconfirmed.md)                                         | <span data-ttu-id="afcac-160">Ruft einen Wert ab, der angibt, ob das **icontextnode** -Objekt bestätigt ist.</span><span class="sxs-lookup"><span data-stu-id="afcac-160">Retrieves a value that indicates whether the **IContextNode** object is confirmed.</span></span> <span data-ttu-id="afcac-161">Der Knotentyp und die zugehörigen Striche für bestätigte **icontextnode** -Objekte können von [**iinkanalyzer**](iinkanalyzer.md) nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="afcac-161">[**IInkAnalyzer**](iinkanalyzer.md) cannot change the node type and associated strokes for confirmed **IContextNode** objects.</span></span><br/> |
| [<span data-ttu-id="afcac-162">**Loadpropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="afcac-162">**LoadPropertiesData**</span></span>](icontextnode-loadpropertiesdata.md)                           | <span data-ttu-id="afcac-163">Erstellt die anwendungsspezifischen und internen Eigenschaften Daten für ein Bytearray, das zuvor mit [**icontextnode:: savepropertiesdata**](icontextnode-savepropertiesdata.md)erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="afcac-163">Recreates the application-specific and internal property data for an array of bytes that was previously created with [**IContextNode::SavePropertiesData**](icontextnode-savepropertiesdata.md).</span></span><br/>                  |
| [<span data-ttu-id="afcac-164">**"Muvesbnodebug"**</span><span class="sxs-lookup"><span data-stu-id="afcac-164">**MoveSubNodeToPosition**</span></span>](icontextnode-movesubnodetoposition.md)                     | <span data-ttu-id="afcac-165">Ordnet ein angegebenes untergeordnetes **icontextnode** -Objekt an den angegebenen Index zurück.</span><span class="sxs-lookup"><span data-stu-id="afcac-165">Reorders a specified child **IContextNode** object to the specified index.</span></span><br/>                                                                                                                                         |
| [<span data-ttu-id="afcac-166">**RemovePropertyData**</span><span class="sxs-lookup"><span data-stu-id="afcac-166">**RemovePropertyData**</span></span>](icontextnode-removepropertydata.md)                           | <span data-ttu-id="afcac-167">Entfernt anwendungsspezifische Daten.</span><span class="sxs-lookup"><span data-stu-id="afcac-167">Removes a piece of application-specific data.</span></span><br/>                                                                                                                                                                      |
| [<span data-ttu-id="afcac-168">**Neu zuordnen**</span><span class="sxs-lookup"><span data-stu-id="afcac-168">**Reparent**</span></span>](icontextnode-reparent.md)                                               | <span data-ttu-id="afcac-169">Verschiebt dieses **icontextnode** -Objekt aus der Auflistung der untergeordneten Knoten des übergeordneten Kontext Knotens in die Auflistung der untergeordneten Knoten des angegebenen Kontext Knotens.</span><span class="sxs-lookup"><span data-stu-id="afcac-169">Moves this **IContextNode** object from its parent context node's subnodes collection to the specified context node's subnodes collection.</span></span><br/>                                                                         |
| [<span data-ttu-id="afcac-170">**Analyse von "Analyse"**</span><span class="sxs-lookup"><span data-stu-id="afcac-170">**ReparentStrokeByIdToNode**</span></span>](icontextnode-reparentstrokebyidtonode.md)               | <span data-ttu-id="afcac-171">Verschiebt die Strich Daten aus diesem **icontextnode** in den angegebenen **icontextnode**.</span><span class="sxs-lookup"><span data-stu-id="afcac-171">Moves stroke data from this **IContextNode** to the specified **IContextNode**.</span></span><br/>                                                                                                                                    |
| [<span data-ttu-id="afcac-172">**Savepropertiesdata**</span><span class="sxs-lookup"><span data-stu-id="afcac-172">**SavePropertiesData**</span></span>](icontextnode-savepropertiesdata.md)                           | <span data-ttu-id="afcac-173">Ruft ein Bytearray ab, das die anwendungsspezifischen und internen Eigenschaften Daten für diesen **icontextnode** enthält.</span><span class="sxs-lookup"><span data-stu-id="afcac-173">Retrieves an array of bytes that contains the application-specific and internal property data for this **IContextNode**.</span></span><br/>                                                                                           |
| [<span data-ttu-id="afcac-174">**SetLocation**</span><span class="sxs-lookup"><span data-stu-id="afcac-174">**SetLocation**</span></span>](icontextnode-setlocation.md)                                         | <span data-ttu-id="afcac-175">Aktualisiert die Position und Größe dieses **icontextnode**.</span><span class="sxs-lookup"><span data-stu-id="afcac-175">Updates the position and size of this **IContextNode**.</span></span><br/>                                                                                                                                                            |
| [<span data-ttu-id="afcac-176">**Setpartiallyausgefüllt**</span><span class="sxs-lookup"><span data-stu-id="afcac-176">**SetPartiallyPopulated**</span></span>](icontextnode-setpartiallypopulated.md)                     | <span data-ttu-id="afcac-177">Ändert den Wert, der angibt, ob dieser **icontextnode** teilweise oder vollständig ausgefüllt ist.</span><span class="sxs-lookup"><span data-stu-id="afcac-177">Modifies the value that indicates whether this **IContextNode** is partially or fully populated.</span></span><br/>                                                                                                                   |
| [<span data-ttu-id="afcac-178">**Setstrokes**</span><span class="sxs-lookup"><span data-stu-id="afcac-178">**SetStrokes**</span></span>](icontextnode-setstrokes.md)                                           | <span data-ttu-id="afcac-179">Ordnet diesem **icontextnode** die angegebenen Striche zu.</span><span class="sxs-lookup"><span data-stu-id="afcac-179">Associates the specified strokes with this **IContextNode**.</span></span><br/>                                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="afcac-180">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="afcac-180">Remarks</span></span>

<span data-ttu-id="afcac-181">Die Knoten Typen werden in den [Kontext Knoten Typen](context-node-types.md) -Konstanten beschrieben.</span><span class="sxs-lookup"><span data-stu-id="afcac-181">The types of nodes are described in the [Context Node Types](context-node-types.md) constants.</span></span>

## <a name="examples"></a><span data-ttu-id="afcac-182">Beispiele</span><span class="sxs-lookup"><span data-stu-id="afcac-182">Examples</span></span>

<span data-ttu-id="afcac-183">Das folgende Beispiel zeigt eine Methode, die einen **icontextnode** untersucht. die-Methode führt Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="afcac-183">The following example shows a method that examines an **IContextNode**; the method does the following:</span></span>

-   <span data-ttu-id="afcac-184">Ruft den Typ des Kontext Knotens ab.</span><span class="sxs-lookup"><span data-stu-id="afcac-184">Gets the context node's type.</span></span> <span data-ttu-id="afcac-185">Handelt es sich bei dem Kontext Knoten um einen nicht klassifizierten Ink-, Analyse-oder benutzerdefinierten Erkennungs Knoten, wird eine Hilfsmethode aufgerufen, um bestimmte Eigenschaften des Knoten Typs zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="afcac-185">If the context node is an unclassified ink, analysis hint, or custom recognizer node, it calls a helper method to examine specific properties of the node type.</span></span>
-   <span data-ttu-id="afcac-186">Wenn der Knoten über untergeordnete Knoten verfügt, werden die einzelnen unter Knoten durch Aufrufen von sich selbst untersucht.</span><span class="sxs-lookup"><span data-stu-id="afcac-186">If the node has subnodes, it examines each subnode by calling itself.</span></span>
-   <span data-ttu-id="afcac-187">Wenn der Knoten ein frei Hand Blattknoten ist, werden die Strich Daten für den Knoten durch Aufrufen einer Hilfsmethode untersucht.</span><span class="sxs-lookup"><span data-stu-id="afcac-187">If the node is an ink leaf node, it examines the stroke data for the node by calling a helper method.</span></span>

<span data-ttu-id="afcac-188">Die IHE InkAnalysis-API ermöglicht es Ihnen, einen Zeilen Knoten zu erstellen, der frei Hand Wörter und Text Wörter enthält.</span><span class="sxs-lookup"><span data-stu-id="afcac-188">Ihe InkAnalysis API allows you to create a line node that contains ink words and text words.</span></span> <span data-ttu-id="afcac-189">Der Parser ignoriert diese gemischten Knoten jedoch und behandelt Sie wie fremde Knoten.</span><span class="sxs-lookup"><span data-stu-id="afcac-189">However, the parser will ignore these mixed nodes and will treat them like foreign nodes.</span></span> <span data-ttu-id="afcac-190">Dies hat Auswirkungen auf die Verarbeitungsgenauigkeit bei der Erkennung von frei Hand Anmerkungen, wenn der Endbenutzer diesen gemischten Knoten ein-oder eingibt.</span><span class="sxs-lookup"><span data-stu-id="afcac-190">This will have impact the parsing accuracy of detecting ink annotations when the end user writes on or around this mixed node.</span></span>


```C++
HRESULT CMyClass::ExploreContextNode(
    IContextNode *pContextNode)
{
    // Check for certain types of context nodes.
    GUID ContextNodeType;
    HRESULT hr = pContextNode->GetType(&ContextNodeType);

    if (SUCCEEDED(hr))
    {
        if (IsEqualGUID(GUID_CNT_UNCLASSIFIEDINK, ContextNodeType))
        {
            // Call a helper method that explores unclassified ink nodes.
            hr = this->ExploreUnclassifiedInkNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_ANALYSISHINT, ContextNodeType))
        {
            // Call a helper method that explores analysis hint nodes.
            hr = this->ExploreAnalysisHintNode(pContextNode);
        }
        else if (IsEqualGUID(GUID_CNT_CUSTOMRECOGNIZER, ContextNodeType))
        {
            // Call a helper method that explores custom recognizer nodes.
            hr = this->ExploreCustomRecognizerNode(pContextNode);
        }

        if (SUCCEEDED(hr))
        {
            // Check if this node is a branch or a leaf node.
            IContextNodes *pSubNodes = NULL;
            hr = pContextNode->GetSubNodes(&pSubNodes);

            if (SUCCEEDED(hr))
            {
                ULONG ulSubNodeCount;
                hr = pSubNodes->GetCount(&ulSubNodeCount);

                if (SUCCEEDED(hr))
                {
                    if (ulSubNodeCount > 0)
                    {
                        // This node has child nodes; explore each child node.
                        IContextNode *pSubNode = NULL;
                        for (ULONG index=0; index<ulSubNodeCount; index++)
                        {
                            hr = pSubNodes->GetContextNode(index, &pSubNode);

                            if (SUCCEEDED(hr))
                            {
                                // Recursive call to explore the child node of this
                                // context node.
                                hr = this->ExploreContextNode(pSubNode);
                            }

                            // Release this reference to the child context node.
                            if (pSubNode != NULL)
                            {
                                pSubNode->Release();
                                pSubNode = NULL;
                            }

                            if (FAILED(hr))
                            {
                                break;
                            }
                        }
                    }
                    else
                    {
                        // This is a leaf node. Check if it contains stroke data.
                        ULONG ulStrokeCount;
                        hr = pContextNode->GetStrokeCount(&ulStrokeCount);

                        if (SUCCEEDED(hr))
                        {
                            if (ulStrokeCount > 0)
                            {
                                // This node is an ink leaf node; call helper
                                // method that explores available stroke data.
                                hr = this->ExploreNodeStrokeData(pContextNode);
                            }
                        }
                    }
                }
            }

            // Release this reference to the subnodes collection.
            if (pSubNodes != NULL)
            {
                pSubNodes->Release();
                pSubNodes = NULL;
            }
        }
    }

    return hr;
}
```



## <a name="requirements"></a><span data-ttu-id="afcac-191">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="afcac-191">Requirements</span></span>



| <span data-ttu-id="afcac-192">Anforderung</span><span class="sxs-lookup"><span data-stu-id="afcac-192">Requirement</span></span> | <span data-ttu-id="afcac-193">Wert</span><span class="sxs-lookup"><span data-stu-id="afcac-193">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="afcac-194">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="afcac-194">Minimum supported client</span></span><br/> | <span data-ttu-id="afcac-195">Nur Windows XP Tablet PC Edition \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="afcac-195">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="afcac-196">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="afcac-196">Minimum supported server</span></span><br/> | <span data-ttu-id="afcac-197">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="afcac-197">None supported</span></span><br/>                                                                                     |
| <span data-ttu-id="afcac-198">Header</span><span class="sxs-lookup"><span data-stu-id="afcac-198">Header</span></span><br/>                   | <dl> <span data-ttu-id="afcac-199"><dt>Iacom. h (erfordert auch iacom \_ i. c)</dt></span><span class="sxs-lookup"><span data-stu-id="afcac-199"><dt>IACom.h (also requires IACom\_i.c)</dt></span></span> </dl> |
| <span data-ttu-id="afcac-200">DLL</span><span class="sxs-lookup"><span data-stu-id="afcac-200">DLL</span></span><br/>                      | <dl> <span data-ttu-id="afcac-201"><dt>IACom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="afcac-201"><dt>IACom.dll</dt></span></span> </dl>                          |



## <a name="see-also"></a><span data-ttu-id="afcac-202">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="afcac-202">See also</span></span>

<dl> <dt>

[<span data-ttu-id="afcac-203">**Icontextnodes**</span><span class="sxs-lookup"><span data-stu-id="afcac-203">**IContextNodes**</span></span>](icontextnodes.md)
</dt> <dt>

[<span data-ttu-id="afcac-204">Kontext Knoten Typen</span><span class="sxs-lookup"><span data-stu-id="afcac-204">Context Node Types</span></span>](context-node-types.md)
</dt> <dt>

[<span data-ttu-id="afcac-205">**Iinkanalyzer**</span><span class="sxs-lookup"><span data-stu-id="afcac-205">**IInkAnalyzer**</span></span>](iinkanalyzer.md)
</dt> <dt>

[<span data-ttu-id="afcac-206">Ink-Analyse Referenz</span><span class="sxs-lookup"><span data-stu-id="afcac-206">Ink Analysis Reference</span></span>](ink-analysis-reference.md)
</dt> </dl>

 

