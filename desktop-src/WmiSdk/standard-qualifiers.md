---
description: Alle CIM-kompatiblen Implementierungen müssen einen Standardsatz von Qualifizierern verarbeiten.
ms.assetid: 671ea769-f68d-4788-96f5-c4f86ab3b00e
ms.tgt_platform: multiple
title: Standard Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Standard
api_type:
- NA
api_location: ''
ms.openlocfilehash: 710e93e53f9e414a44dc14ebafea426f5d7f9efd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356622"
---
# <a name="standard-qualifiers"></a><span data-ttu-id="51cb9-103">Standard Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="51cb9-103">Standard Qualifiers</span></span>

<span data-ttu-id="51cb9-104">Alle CIM-kompatiblen Implementierungen müssen einen Standardsatz von Qualifizierern verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="51cb9-104">All CIM-compliant implementations must handle a standard set of qualifiers.</span></span> <span data-ttu-id="51cb9-105">Ein bestimmtes Objekt verfügt nicht über alle aufgeführten Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="51cb9-105">Any specific object does not have all of the qualifiers listed.</span></span> <span data-ttu-id="51cb9-106">Normalerweise stellen Erweiterungs Klassen zusätzliche Qualifizierer bereit, um die Bereitstellung von Klassen Instanzen und anderen Vorgängen für die Klasse zu vereinfachen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-106">Usually, extension classes supply additional qualifiers to facilitate provision of class instances and other operations on the class.</span></span>

<span data-ttu-id="51cb9-107">Der Anbieter muss die Qualifizierer erzwingen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-107">It is the responsibility of the provider to enforce the qualifiers.</span></span> <span data-ttu-id="51cb9-108">WMI erzwingt keine Qualifizierer, sondern verwendet Sie nur, um den Benutzer darüber zu informieren, wie die-Eigenschaft verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51cb9-108">WMI does not enforce qualifiers, but uses them only to inform the user about how the property is used.</span></span>

> [!Note]  
> <span data-ttu-id="51cb9-109">WMI ist mit der CIM 2,5-Spezifikation kompatibel.</span><span class="sxs-lookup"><span data-stu-id="51cb9-109">WMI is compliant with the CIM 2.5 specification.</span></span>

 

<span data-ttu-id="51cb9-110">Qualifizierer weisen die folgenden Einschränkungen auf:</span><span class="sxs-lookup"><span data-stu-id="51cb9-110">Qualifiers have the following limitations:</span></span>

-   <span data-ttu-id="51cb9-111">Nicht alle Standard Qualifizierer können gleichzeitig verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-111">Not all standard qualifiers can be used together.</span></span>
-   <span data-ttu-id="51cb9-112">Nicht alle Qualifizierer können auf alle Konstrukte angewendet werden, wie z. b. Association oder Reference.</span><span class="sxs-lookup"><span data-stu-id="51cb9-112">Not all qualifiers can be applied to all constructs, such as association or reference.</span></span> <span data-ttu-id="51cb9-113">Diese Einschränkungen werden in der Liste gilt für identifiziert.</span><span class="sxs-lookup"><span data-stu-id="51cb9-113">These limitations are identified in the Applies to list.</span></span>
-   <span data-ttu-id="51cb9-114">Für ein bestimmtes Konstrukt, wie z. b. Zuordnung oder Verweis, kann die Verwendung der rechtlichen Qualifizierer weiter eingeschränkt werden, da sich einige Qualifizierer gegenseitig ausschließen. die Verwendung eines Qualifizierers impliziert möglicherweise einige Einschränkungen für den Wert eines anderen, usw.</span><span class="sxs-lookup"><span data-stu-id="51cb9-114">For a particular construct, such as association or reference, the use of the legal qualifiers can be further constrained because some qualifiers are mutually exclusive, the use of one qualifier may imply some restrictions on the value of another, and so on.</span></span> <span data-ttu-id="51cb9-115">Diese Verwendungs Regeln sind dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="51cb9-115">These usage rules are documented.</span></span>
-   <span data-ttu-id="51cb9-116">Juristische Qualifizierer werden nur von Entitäten wie Eigenschaften, Methoden, Instanzen oder Unterklassen geerbt, nicht von Zuordnungen oder verweisen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-116">Legal qualifiers are inherited by entities such as properties, methods, instances, or subclasses only, not by associations or references.</span></span> <span data-ttu-id="51cb9-117">Beispielsweise wird der **maxlen** -Qualifizierer, der sich auf Eigenschaften bezieht, nicht von verweisen geerbt.</span><span class="sxs-lookup"><span data-stu-id="51cb9-117">For example, the **MaxLen** qualifier that applies to properties is not inherited by references.</span></span>

<span data-ttu-id="51cb9-118">Im folgenden werden die WMI-Standard Qualifizierer aufgeführt</span><span class="sxs-lookup"><span data-stu-id="51cb9-118">The following lists WMI standard qualifiers.</span></span>

<dt>

<span data-ttu-id="51cb9-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Kter**</span><span class="sxs-lookup"><span data-stu-id="51cb9-119"><span id="Abstract"></span><span id="abstract"></span><span id="ABSTRACT"></span>**Abstract**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-120">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-120">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-121">Gilt für: Klassen, Zuordnungen, Hinweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-121">Applies to: classes, associations, indications</span></span>

<span data-ttu-id="51cb9-122">Gibt an, ob die Klasse abstrakt ist und nur als Basis für neue Klassen fungiert.</span><span class="sxs-lookup"><span data-stu-id="51cb9-122">Indicates whether the class is abstract and serves only as a base for new classes.</span></span> <span data-ttu-id="51cb9-123">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-123">The default is **FALSE**.</span></span> <span data-ttu-id="51cb9-124">Es können keine Instanzen von abstrakten Klassen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-124">You cannot create instances of abstract classes.</span></span> <span data-ttu-id="51cb9-125">Das Fehlen dieses Qualifizierers gibt an, dass die Klasse nicht abstrakt ist. Daher ist dieser Qualifizierer für alle abstrakten Klassen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="51cb9-125">The absence of this qualifier indicates that the class is not abstract; therefore, this qualifier is required for all abstract classes.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**End**</span><span class="sxs-lookup"><span data-stu-id="51cb9-126"><span id="Aggregate"></span><span id="aggregate"></span><span id="AGGREGATE"></span>**Aggregate**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-127">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-127">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-128">Gilt für: Verweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-128">Applies to: references</span></span>

<span data-ttu-id="51cb9-129">Gibt an, ob der Verweis die übergeordnete Komponente einer Aggregations Zuordnung ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-129">Indicates whether the reference is the parent component of an aggregation association.</span></span> <span data-ttu-id="51cb9-130">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-130">The default is **FALSE**.</span></span>

<span data-ttu-id="51cb9-131">Verwendung: die **Aggregations** -und **Aggregat** Qualifizierer   **werden zusammen verwendet** , um die Zuordnung zu qualifizieren, und **Aggregat** gibt den übergeordneten Verweis an.</span><span class="sxs-lookup"><span data-stu-id="51cb9-131">Usage: The **Aggregation** and **Aggregate** qualifiers are used together   **Aggregation** qualifies the association, and **Aggregate** specifies the parent reference.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Stellung**</span><span class="sxs-lookup"><span data-stu-id="51cb9-132"><span id="Aggregation"></span><span id="aggregation"></span><span id="AGGREGATION"></span>**Aggregation**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-133">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-133">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-134">Gilt für: Zuordnungen</span><span class="sxs-lookup"><span data-stu-id="51cb9-134">Applies to: associations</span></span>

<span data-ttu-id="51cb9-135">Gibt an, ob die Zuordnung eine Aggregation ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-135">Indicates whether the association is an aggregation.</span></span> <span data-ttu-id="51cb9-136">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-136">The default is **FALSE**.</span></span> <span data-ttu-id="51cb9-137">Wird zusammen mit **Aggregate** verwendet.</span><span class="sxs-lookup"><span data-stu-id="51cb9-137">Used with **Aggregate**.</span></span> <span data-ttu-id="51cb9-138">Dieser Qualifizierer ist für alle Aggregations Zuordnungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="51cb9-138">This qualifier is required for all aggregation associations.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**</span><span class="sxs-lookup"><span data-stu-id="51cb9-139"><span id="Alias"></span><span id="alias"></span><span id="ALIAS"></span>**Alias**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-140">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-140">Data type: **string**</span></span>

<span data-ttu-id="51cb9-141">Gilt für: Eigenschaften, Verweise, Methoden</span><span class="sxs-lookup"><span data-stu-id="51cb9-141">Applies to: properties, references, methods</span></span>

<span data-ttu-id="51cb9-142">Alternativer Name für eine Eigenschaft oder Methode im Schema.</span><span class="sxs-lookup"><span data-stu-id="51cb9-142">Alternate name for a property or method in the schema.</span></span> <span data-ttu-id="51cb9-143">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-143">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span><span class="sxs-lookup"><span data-stu-id="51cb9-144"><span id="ArrayType"></span><span id="arraytype"></span><span id="ARRAYTYPE"></span>**ArrayType**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-145">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-145">Data type: **string**</span></span>

<span data-ttu-id="51cb9-146">Gilt für: Eigenschaften, Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-146">Applies to: properties, parameters</span></span>

<span data-ttu-id="51cb9-147">Der Typ des qualifizierten Arrays.</span><span class="sxs-lookup"><span data-stu-id="51cb9-147">Type of the qualified array.</span></span>

<span data-ttu-id="51cb9-148">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="51cb9-148">Valid values are:</span></span>

-   <span data-ttu-id="51cb9-149">Bag (Standard)</span><span class="sxs-lookup"><span data-stu-id="51cb9-149">bag (default)</span></span>
-   <span data-ttu-id="51cb9-150">Indiziert</span><span class="sxs-lookup"><span data-stu-id="51cb9-150">indexed</span></span>
-   <span data-ttu-id="51cb9-151">geordnete</span><span class="sxs-lookup"><span data-stu-id="51cb9-151">ordered</span></span>

<span data-ttu-id="51cb9-152">Syntax: wenden Sie diese Art von Qualifizierer auf Eigenschaften und Parameter an (definiert durch Klammern-Syntax).</span><span class="sxs-lookup"><span data-stu-id="51cb9-152">Usage: Apply this type of qualifier only to properties and parameters that are arrays (defined by using bracket syntax).</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**Bitmap**</span><span class="sxs-lookup"><span data-stu-id="51cb9-153"><span id="BitMap"></span><span id="bitmap"></span><span id="BITMAP"></span>**BitMap**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-154">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="51cb9-154">Data type: **string array**</span></span>

<span data-ttu-id="51cb9-155">Gilt für: Eigenschaften, Methoden, Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-155">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="51cb9-156">Zuordnung von wichtigen Bitpositionen, bei denen jede bedeutende Position "on" oder "Off" sein kann.</span><span class="sxs-lookup"><span data-stu-id="51cb9-156">Map of significant bit positions where each significant position can be "on" or "off".</span></span> <span data-ttu-id="51cb9-157">Jedes "on"-Bit ist einem entsprechenden Wert im **BitValues** -Array zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="51cb9-157">Each "on" bit maps to a corresponding value in the **BitValues** array.</span></span> <span data-ttu-id="51cb9-158">Wenn Sie über mehrere Bits "on" verfügen, werden mehrere gleichzeitige Werte im **BitValues** -Array angegeben.</span><span class="sxs-lookup"><span data-stu-id="51cb9-158">By having multiple bits "on", multiple concurrent values in the **BitValues** array are indicated.</span></span> <span data-ttu-id="51cb9-159">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-159">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-160">Weitere Informationen finden Sie unter [Bitmap und BitValues](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="51cb9-160">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**</span><span class="sxs-lookup"><span data-stu-id="51cb9-161"><span id="BitValues"></span><span id="bitvalues"></span><span id="BITVALUES"></span>**BitValues**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-162">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="51cb9-162">Data type: **string array**</span></span>

<span data-ttu-id="51cb9-163">Gilt für: Eigenschaften, Methoden, Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-163">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="51cb9-164">Übersetzung eines bitpositions Werts in eine zugeordnete **Zeichenfolge**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-164">Translation of a bit position value into an associated **string**.</span></span> <span data-ttu-id="51cb9-165">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-165">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-166">Weitere Informationen finden Sie unter [Bitmap und BitValues](bitmap-and-bitvalues.md).</span><span class="sxs-lookup"><span data-stu-id="51cb9-166">For more information, see [BitMap and BitValues](bitmap-and-bitvalues.md).</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Konstruktor**</span><span class="sxs-lookup"><span data-stu-id="51cb9-167"><span id="Constructor"></span><span id="constructor"></span><span id="CONSTRUCTOR"></span>**Constructor**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-168">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-168">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-169">Gilt für: Methoden</span><span class="sxs-lookup"><span data-stu-id="51cb9-169">Applies to: methods</span></span>

<span data-ttu-id="51cb9-170">Gibt an, ob die Methode-Instanzen erstellt.</span><span class="sxs-lookup"><span data-stu-id="51cb9-170">Indicates whether the method creates instances.</span></span> <span data-ttu-id="51cb9-171">Diese Methoden sind nicht darauf beschränkt, für eine einzelne Instanz oder eine einzelne Klasse zu agieren.</span><span class="sxs-lookup"><span data-stu-id="51cb9-171">These methods are not constrained to acting on a single instance or a single class.</span></span> <span data-ttu-id="51cb9-172">Ein Konstruktor kann z. b. Zuordnungs Instanzen und Instanzen der Klasse erstellen, die den Konstruktor definiert.</span><span class="sxs-lookup"><span data-stu-id="51cb9-172">For example, a constructor can create association instances as well as instances of the class that defines the constructor.</span></span>

<span data-ttu-id="51cb9-173">Der **konstruktorqualifizierer** ist nur für Informationen vorgesehen, und es wird nicht erwartet, dass er vom Objekt-Manager bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="51cb9-173">The **Constructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="51cb9-174">Der Objekt-Manager muss beim Erstellen eines Objekts keine Konstruktormethoden aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-174">The object manager does not have to call constructor methods when an object is created.</span></span> <span data-ttu-id="51cb9-175">Wenn ein Konstruktor aufgerufen wird, muss der Objekt-Manager auch keine Konstruktormethoden aufrufen, die für eine übergeordnete Klasse der ursprünglichen Klasse definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-175">Also when a constructor is called, the object manager does not have to invoke any constructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="51cb9-176">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-176">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**Mit der**</span><span class="sxs-lookup"><span data-stu-id="51cb9-177"><span id="CreateBy"></span><span id="createby"></span><span id="CREATEBY"></span>**CreateBy**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-178">Data type: **string**</span></span>

<span data-ttu-id="51cb9-179">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="51cb9-179">Applies to: classes</span></span>

<span data-ttu-id="51cb9-180">Der Name der Methode, mit der Instanzen dieser Klasse erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-180">Name of the method by which instances of this class are created.</span></span> <span data-ttu-id="51cb9-181">Der Wert ist entweder "PutInstance" oder der Name einer anderen Methode, mit der die Instanzen erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-181">The value is either "PutInstance" or the name of another method that creates the instances.</span></span> <span data-ttu-id="51cb9-182">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-182">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-183">Verwendung: dieser Qualifizierer kann nur verwendet werden, wenn der **SupportsCreate-Qualifizierer** vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-183">Usage: This qualifier can only be used if the **SupportsCreate** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**Deleteby**</span><span class="sxs-lookup"><span data-stu-id="51cb9-184"><span id="DeleteBy"></span><span id="deleteby"></span><span id="DELETEBY"></span>**DeleteBy**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-185">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-185">Data type: **string**</span></span>

<span data-ttu-id="51cb9-186">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="51cb9-186">Applies to: classes</span></span>

<span data-ttu-id="51cb9-187">Der Name der Methode, mit der Instanzen dieser Klasse gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-187">Name of the method by which instances of this class are deleted.</span></span> <span data-ttu-id="51cb9-188">Der Wert ist entweder "Delta einstance" oder der Name einer anderen Methode, mit der die Instanzen gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-188">The value is either "DeleteInstance", or the name of another method that deletes the instances.</span></span> <span data-ttu-id="51cb9-189">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-189">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-190">Verwendung: dieser Qualifizierer kann nur verwendet werden, wenn der **SupportsDelete** -Qualifizierer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-190">Usage: This qualifier can only be used if the **SupportsDelete** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="51cb9-191"><span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**Description**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-192">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-192">Data type: **string**</span></span>

<span data-ttu-id="51cb9-193">Gilt für: beliebig</span><span class="sxs-lookup"><span data-stu-id="51cb9-193">Applies to: any</span></span>

<span data-ttu-id="51cb9-194">Beschreibung eines benannten Elements.</span><span class="sxs-lookup"><span data-stu-id="51cb9-194">Description of a named element.</span></span> <span data-ttu-id="51cb9-195">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-195">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destruktor**</span><span class="sxs-lookup"><span data-stu-id="51cb9-196"><span id="Destructor"></span><span id="destructor"></span><span id="DESTRUCTOR"></span>**Destructor**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-197">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-197">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-198">Gilt für: Methoden</span><span class="sxs-lookup"><span data-stu-id="51cb9-198">Applies to: methods</span></span>

<span data-ttu-id="51cb9-199">Gibt an, ob die-Methode-Instanzen löscht.</span><span class="sxs-lookup"><span data-stu-id="51cb9-199">Indicates whether the method deletes instances.</span></span> <span data-ttu-id="51cb9-200">Methoden, die den **dekonstruktorqualifizierer** verwenden, löschen die Instanz (en), auf die der Dekonstruktor angewendet wird, und sind nicht darauf beschränkt, für eine einzelne Instanz oder Klasse zu agieren.</span><span class="sxs-lookup"><span data-stu-id="51cb9-200">Methods using the **Destructor** qualifier delete the instance(s) to which the destructor is applied, and are not constrained to acting on a single instance or class.</span></span> <span data-ttu-id="51cb9-201">Beispielsweise kann ein Dekonstruktor Zuordnungs Instanzen und Instanzen der Klasse löschen, die den Dekonstruktor definiert.</span><span class="sxs-lookup"><span data-stu-id="51cb9-201">For example, a destructor might delete association instances as well as instances of the class that defines the destructor.</span></span>

<span data-ttu-id="51cb9-202">Der **debuggerqualifizierer** ist nur für Informationen vorgesehen, und es wird nicht erwartet, dass er vom Objekt-Manager bearbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="51cb9-202">The **Destructor** qualifier is intended for information only and it is not expected that it is acted on by the object manager.</span></span> <span data-ttu-id="51cb9-203">Es ist nicht zulässig, dass der Objekt-Manager eine Methode aufruft, die den **Dekonstruktor** -Qualifizierer aufweist, wenn eine Instanz gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="51cb9-203">There is no obligation for the object manager to call a method that has the **Destructor** qualifier when an instance is deleted.</span></span> <span data-ttu-id="51cb9-204">Wenn ein Dekonstruktor aufgerufen wird, muss der Objekt-Manager auch keine dekonstruktormethoden aufrufen, die für eine übergeordnete Klasse der ursprünglichen Klasse definiert wurden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-204">Also, when a destructor is called, the object manager does not have to invoke any destructor methods defined for any parent class of the original class.</span></span> <span data-ttu-id="51cb9-205">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-205">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**Display Name**</span><span class="sxs-lookup"><span data-stu-id="51cb9-206"><span id="DisplayName"></span><span id="displayname"></span><span id="DISPLAYNAME"></span>**DisplayName**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-207">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-207">Data type: **string**</span></span>

<span data-ttu-id="51cb9-208">Gilt für: beliebig</span><span class="sxs-lookup"><span data-stu-id="51cb9-208">Applies to: any</span></span>

<span data-ttu-id="51cb9-209">Der in der Benutzeroberfläche angezeigte Name und nicht der tatsächliche Name des Elements.</span><span class="sxs-lookup"><span data-stu-id="51cb9-209">Name displayed in the UI instead of the actual name of the element.</span></span> <span data-ttu-id="51cb9-210">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-210">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**Embeddecodinstance**</span><span class="sxs-lookup"><span data-stu-id="51cb9-211"><span id="EmbeddedInstance"></span><span id="embeddedinstance"></span><span id="EMBEDDEDINSTANCE"></span>**EmbeddedInstance**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-212">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-212">Data type: **string**</span></span>

<span data-ttu-id="51cb9-213">Gilt für: beliebig</span><span class="sxs-lookup"><span data-stu-id="51cb9-213">Applies to: any</span></span>

<span data-ttu-id="51cb9-214">Das qualifizierte String Type-Element enthält eine eingebettete-Instanz.</span><span class="sxs-lookup"><span data-stu-id="51cb9-214">The qualified string type element contains an embedded instance.</span></span> <span data-ttu-id="51cb9-215">Der qualifiziererwert gibt den Namen einer CIM-Klasse im gleichen Namespace wie die Klasse an, die das qualifizierte Element besitzt.</span><span class="sxs-lookup"><span data-stu-id="51cb9-215">The qualifier value specifies the name of a CIM class in the same namespace as the class owning the qualified element.</span></span> <span data-ttu-id="51cb9-216">Die eingebettete Instanz ist eine Instanz der angegebenen Klasse, einschließlich Instanzen der zugehörigen Unterklassen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-216">The embedded instance is an instance of the specified class, including instances of its subclasses.</span></span> <span data-ttu-id="51cb9-217">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-217">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Mess Gerät**</span><span class="sxs-lookup"><span data-stu-id="51cb9-218"><span id="Gauge"></span><span id="gauge"></span><span id="GAUGE"></span>**Gauge**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-219">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-219">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-220">Gilt für: beliebig</span><span class="sxs-lookup"><span data-stu-id="51cb9-220">Applies to: any</span></span>

<span data-ttu-id="51cb9-221">Gibt an, ob die-Eigenschaft eine nicht negative ganze Zahl darstellt, die vergrößert oder verringert werden kann, aber nie einen maximalen Wert überschreitet.</span><span class="sxs-lookup"><span data-stu-id="51cb9-221">Indicates whether the property represents a non-negative integer, which can increase or decrease, but never exceed a maximum value.</span></span> <span data-ttu-id="51cb9-222">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-222">The default is **FALSE**.</span></span>

<span data-ttu-id="51cb9-223">Der maximale Wert der Eigenschaft darf nicht größer als 2 ^*n* -1 sein.</span><span class="sxs-lookup"><span data-stu-id="51cb9-223">The maximum value of the property cannot be greater than 2^*n* - 1.</span></span> <span data-ttu-id="51cb9-224">*N* kann je nach Datentyp der Eigenschaft, auf die dieser Qualifizierer angewendet wird, 8, 16, 32 oder 64 sein.</span><span class="sxs-lookup"><span data-stu-id="51cb9-224">*N* can be 8, 16, 32, or 64 depending on the data type of the property to which this qualifier is applied.</span></span> <span data-ttu-id="51cb9-225">Der Wert eines Messgerätes hat seinen maximalen Wert, wenn die zu modellierenden Informationen größer oder gleich diesem maximalen Wert sind.</span><span class="sxs-lookup"><span data-stu-id="51cb9-225">The value of a gauge has its maximum value whenever the information being modeled is greater or equal to that maximum value.</span></span> <span data-ttu-id="51cb9-226">Wenn die zu modellierenden Informationen dann unter den maximalen Wert sinken, sinkt auch das Messgerät.</span><span class="sxs-lookup"><span data-stu-id="51cb9-226">If the information being modeled subsequently decreases below the maximum value, the gauge also decreases.</span></span> <span data-ttu-id="51cb9-227">Dieser Qualifizierer ist nur auf Eigenschaften mit einem Integer-Datentyp ohne Vorzeichen anwendbar.</span><span class="sxs-lookup"><span data-stu-id="51cb9-227">This qualifier is applicable only to properties with an unsigned integer data type.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**In**</span><span class="sxs-lookup"><span data-stu-id="51cb9-228"><span id="In"></span><span id="in"></span><span id="IN"></span>**In**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-229">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-229">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-230">Gilt für: Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-230">Applies to: parameters</span></span>

<span data-ttu-id="51cb9-231">Gibt an, ob der-Parameter verwendet wird, um Werte an eine Methode zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="51cb9-231">Indicates whether the parameter is used to pass values to a method.</span></span> <span data-ttu-id="51cb9-232">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="51cb9-232">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, out**</span><span class="sxs-lookup"><span data-stu-id="51cb9-233"><span id="In__Out"></span><span id="in__out"></span><span id="IN__OUT"></span>**In, Out**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-234">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-234">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-235">Gilt für: Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-235">Applies to: parameters</span></span>

<span data-ttu-id="51cb9-236">Gibt an, ob der Parameter ein Eingabe-und ein Ausgabeparameter ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-236">Indicates whether the parameter is both an input and output parameter.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Wichtigen**](key-qualifier.md)</span><span class="sxs-lookup"><span data-stu-id="51cb9-237"><span id="Key"></span><span id="key"></span><span id="KEY"></span>[**Key**](key-qualifier.md)</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-238">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-238">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-239">Gilt für: Eigenschaften, Verweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-239">Applies to: properties, references</span></span>

<span data-ttu-id="51cb9-240">Gibt an, ob die Eigenschaft Teil des Namespace Handles ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-240">Indicates whether the property is part of the namespace handle.</span></span> <span data-ttu-id="51cb9-241">Wenn mehr als eine Eigenschaft den [**Schlüssel**](key-qualifier.md) Qualifizierer aufweist, bilden alle diese Eigenschaften zusammen den Schlüssel (einen Verbund Schlüssel).</span><span class="sxs-lookup"><span data-stu-id="51cb9-241">If more than one property has the [**Key**](key-qualifier.md) qualifier, then all such properties collectively form the key (a compound key).</span></span> <span data-ttu-id="51cb9-242">Bei gemeinsamer Erstellung müssen die Schlüsseleigenschaften einen eindeutigen Verweis für jede Klasseninstanz angeben.</span><span class="sxs-lookup"><span data-stu-id="51cb9-242">When taken together, the key properties must supply a unique reference for each class instance.</span></span> <span data-ttu-id="51cb9-243">Wenn dieser Qualifizierer für eine Eigenschaft platziert wird, ist nur der Wert **true** zulässig.</span><span class="sxs-lookup"><span data-stu-id="51cb9-243">If this qualifier is placed on a property, only the value **TRUE** is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Lazy**</span><span class="sxs-lookup"><span data-stu-id="51cb9-244"><span id="Lazy"></span><span id="lazy"></span><span id="LAZY"></span>**Lazy**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-245">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51cb9-245">Applies to: properties</span></span>

<span data-ttu-id="51cb9-246">Gibt an, dass die Eigenschaft für die Rückgabe ressourcenintensiv ist und viel Prozessorzeit und Arbeitsspeicher erfordert.</span><span class="sxs-lookup"><span data-stu-id="51cb9-246">Indicates that the property is resource-intensive to return and requires a lot of processor time and memory.</span></span> <span data-ttu-id="51cb9-247">WMI verbessert die Leistung von Abfragen, indem nicht versucht wird, die mit dem **Lazy** -Qualifizierer markierten Eigenschaften zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="51cb9-247">WMI improves the performance of queries by not attempting to return the properties marked with the **Lazy** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**Mappingstrings**</span><span class="sxs-lookup"><span data-stu-id="51cb9-248"><span id="MappingStrings"></span><span id="mappingstrings"></span><span id="MAPPINGSTRINGS"></span>**MappingStrings**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-249">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="51cb9-249">Data type: **string array**</span></span>

<span data-ttu-id="51cb9-250">Gilt für: Klassen, Eigenschaften, Zuordnungen, Hinweise, Verweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-250">Applies to: classes, properties, associations, indications, references</span></span>

<span data-ttu-id="51cb9-251">Ein Satz von Werten, die einen Pfad zu einem Speicherort angeben, an dem Sie weitere Informationen über den Ursprung einer Eigenschaft, Klasse, Zuordnung, Angabe oder eines Verweises finden können.</span><span class="sxs-lookup"><span data-stu-id="51cb9-251">Set of values that indicate a path to a location where you can find more information about the origin of a property, class, association, indication, or reference.</span></span> <span data-ttu-id="51cb9-252">Bei der zuordnungszeichenfolge kann es sich um einen Verzeichnispfad, eine URL, einen Registrierungsschlüssel, eine Includedatei, einen Verweis auf eine CIM-Klasse oder ein anderes Format handeln.</span><span class="sxs-lookup"><span data-stu-id="51cb9-252">The mapping string can be a directory path, a URL, a registry key, an include file, reference to a CIM class, or some other format.</span></span> <span data-ttu-id="51cb9-253">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-253">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**</span><span class="sxs-lookup"><span data-stu-id="51cb9-254"><span id="Max"></span><span id="max"></span><span id="MAX"></span>**Max**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-255">Datentyp: **int**</span><span class="sxs-lookup"><span data-stu-id="51cb9-255">Data type: **int**</span></span>

<span data-ttu-id="51cb9-256">Gilt für: Verweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-256">Applies to: references</span></span>

<span data-ttu-id="51cb9-257">Maximale Anzahl von Werten, die ein bestimmter Verweis für jeden Satz anderer Verweis Werte in der Zuordnung aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="51cb9-257">Maximum number of values a given reference can have for each set of other reference values in the association.</span></span> <span data-ttu-id="51cb9-258">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-258">The default is **NULL**.</span></span> <span data-ttu-id="51cb9-259">Wenn eine Zuordnung z. b. eine-Instanz mit B-Instanzen verknüpft und höchstens eine-Instanz für jede B-Instanz vorhanden sein muss, sollte der Verweis auf einen-Wert maximal einen Qualifizierer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-259">For example, if an association relates A instances to B instances and there must be at most one A instance for each B instance, then the reference to A should have a maximum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span><span class="sxs-lookup"><span data-stu-id="51cb9-260"><span id="MaxLen"></span><span id="maxlen"></span><span id="MAXLEN"></span>**MaxLen**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-261">Datentyp: **int**</span><span class="sxs-lookup"><span data-stu-id="51cb9-261">Data type: **int**</span></span>

<span data-ttu-id="51cb9-262">Gilt für: Eigenschaften, Methoden, Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-262">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="51cb9-263">Maximale Länge (in Zeichen) eines **Zeichen** folgen Datenelements und gibt die Unterstützung von Arrays mit fester Länge an.</span><span class="sxs-lookup"><span data-stu-id="51cb9-263">Maximum length (in characters) of a **string** data item and indicates support of fixed-length arrays.</span></span>

<span data-ttu-id="51cb9-264">Wenn ein Array mit fester Länge gefunden wird, enthält der **maxlen** -Qualifizierer die festgelegte Länge, die beim Parsen gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="51cb9-264">If a fixed-length array is encountered, the **MaxLen** qualifier contains the fixed length found during parsing.</span></span> <span data-ttu-id="51cb9-265">Wenn ein Array variabler Länge gefunden wird, wird dieser Qualifizierer nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="51cb9-265">If a variable-length array is encountered, then this qualifier is not used.</span></span> <span data-ttu-id="51cb9-266">**Maxlen** wird verwendet, um die maximale Anzahl von Elementen vorzuschlagen, die in einem Array gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-266">**MaxLen** is used to suggest the maximum number of elements that should be stored in an array.</span></span> <span data-ttu-id="51cb9-267">Wenn Sie den Standardwert überschreiben, können alle ganzzahligen Werte ohne Vorzeichen (**UInt32**) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-267">When overriding the default value, any unsigned integer value (**uint32**) can be specified.</span></span> <span data-ttu-id="51cb9-268">Der Wert **null** (Standard) impliziert eine unbegrenzte Länge.</span><span class="sxs-lookup"><span data-stu-id="51cb9-268">A value of **NULL** (default) implies unlimited length.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span><span class="sxs-lookup"><span data-stu-id="51cb9-269"><span id="MaxValue"></span><span id="maxvalue"></span><span id="MAXVALUE"></span>**MaxValue**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-270">Datentyp: **int**</span><span class="sxs-lookup"><span data-stu-id="51cb9-270">Data type: **int**</span></span>

<span data-ttu-id="51cb9-271">Gilt für: Eigenschaften, Methoden, Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-271">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="51cb9-272">Der Höchstwert des Objekts.</span><span class="sxs-lookup"><span data-stu-id="51cb9-272">Maximum value of the object.</span></span> <span data-ttu-id="51cb9-273">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-273">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Man**</span><span class="sxs-lookup"><span data-stu-id="51cb9-274"><span id="Min"></span><span id="min"></span><span id="MIN"></span>**Min**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-275">Datentyp: **int**</span><span class="sxs-lookup"><span data-stu-id="51cb9-275">Data type: **int**</span></span>

<span data-ttu-id="51cb9-276">Gilt für: Verweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-276">Applies to: references</span></span>

<span data-ttu-id="51cb9-277">Minimale Kardinalität des Verweises (die minimale Anzahl von Werten, die ein bestimmter Verweis für jeden Satz anderer Verweis Werte in der Zuordnung aufweisen kann).</span><span class="sxs-lookup"><span data-stu-id="51cb9-277">Minimum cardinality of the reference (the minimum number of values a given reference can have for each set of other reference values in the association).</span></span> <span data-ttu-id="51cb9-278">Die Standardeinstellung ist 0.</span><span class="sxs-lookup"><span data-stu-id="51cb9-278">The default is 0.</span></span>

<span data-ttu-id="51cb9-279">Wenn eine Zuordnung z. b. eine-Instanz mit B-Instanzen verknüpft und mindestens eine-Instanz für jede b-Instanz vorhanden sein muss, sollte der Verweis auf eine mindestens einen Qualifizierer aufweisen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-279">For example, if an association relates A instances to B instances, and there must be at least one A instance for each B instance, then the reference to A should have a minimum of one qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span><span class="sxs-lookup"><span data-stu-id="51cb9-280"><span id="MinValue"></span><span id="minvalue"></span><span id="MINVALUE"></span>**MinValue**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-281">Datentyp: **int**</span><span class="sxs-lookup"><span data-stu-id="51cb9-281">Data type: **int**</span></span>

<span data-ttu-id="51cb9-282">Gilt für: Eigenschaften, Methoden, Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-282">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="51cb9-283">Gibt den minimalen Wert des-Objekts an.</span><span class="sxs-lookup"><span data-stu-id="51cb9-283">Indicates the minimum value of the object.</span></span> <span data-ttu-id="51cb9-284">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-284">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**Modelkorrespondenz**</span><span class="sxs-lookup"><span data-stu-id="51cb9-285"><span id="ModelCorrespondence"></span><span id="modelcorrespondence"></span><span id="MODELCORRESPONDENCE"></span>**ModelCorrespondence**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-286">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="51cb9-286">Data type: **string array**</span></span>

<span data-ttu-id="51cb9-287">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51cb9-287">Applies to: properties</span></span>

<span data-ttu-id="51cb9-288">Ein Satz von Werten, die die Übereinstimmung zwischen der-Eigenschaft eines Objekts und anderen Eigenschaften im CIM-Schema angeben.</span><span class="sxs-lookup"><span data-stu-id="51cb9-288">Set of values that indicate correspondence between an object's property and other properties in the CIM schema.</span></span> <span data-ttu-id="51cb9-289">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-289">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-290">Objekteigenschaften werden mit der folgenden Syntax identifiziert.</span><span class="sxs-lookup"><span data-stu-id="51cb9-290">Object properties are identified using the following syntax.</span></span>

<span data-ttu-id="51cb9-291"><schema name> "\_" <class or association name> "." <property name></span><span class="sxs-lookup"><span data-stu-id="51cb9-291"><schema name> "\_" <class or association name> "." <property name></span></span>

</dd> <dt>

<span data-ttu-id="51cb9-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Nicht lokalen**</span><span class="sxs-lookup"><span data-stu-id="51cb9-292"><span id="Nonlocal"></span><span id="nonlocal"></span><span id="NONLOCAL"></span>**Nonlocal**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-293">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-293">Data type: **string**</span></span>

<span data-ttu-id="51cb9-294">Gilt für: Verweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-294">Applies to: references</span></span>

<span data-ttu-id="51cb9-295">Speicherort einer Instanz, deren Wert <*NamespaceType*>://<*namespacehandle* ist> der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-295">Location of an instance, the value of which is <*namespacetype*>://<*namespacehandle*> The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-296">Verwendung: dieser Qualifizierer kann nicht mit dem **nonlocaltype** -Qualifizierer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-296">Usage: This qualifier cannot be used with the **NonlocalType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**Nonlocaltype**</span><span class="sxs-lookup"><span data-stu-id="51cb9-297"><span id="NonlocalType"></span><span id="nonlocaltype"></span><span id="NONLOCALTYPE"></span>**NonlocalType**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-298">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-298">Data type: **string**</span></span>

<span data-ttu-id="51cb9-299">Gilt für: Verweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-299">Applies to: references</span></span>

<span data-ttu-id="51cb9-300">Der Typ des Speicher Orts einer Instanz.</span><span class="sxs-lookup"><span data-stu-id="51cb9-300">Type of location of an instance.</span></span> <span data-ttu-id="51cb9-301">Der Wert ist <namespacetype> .</span><span class="sxs-lookup"><span data-stu-id="51cb9-301">Its value is <namespacetype>.</span></span> <span data-ttu-id="51cb9-302">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-302">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-303">Verwendung: dieser Qualifizierer kann nicht mit dem **nicht lokalen** Qualifizierer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-303">Usage: This qualifier cannot be used with the **Nonlocal** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span><span class="sxs-lookup"><span data-stu-id="51cb9-304"><span id="NullValue"></span><span id="nullvalue"></span><span id="NULLVALUE"></span>**NullValue**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-305">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-305">Data type: **string**</span></span>

<span data-ttu-id="51cb9-306">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51cb9-306">Applies to: properties</span></span>

<span data-ttu-id="51cb9-307">Ein Wert, der angibt, dass die zugeordnete Eigenschaft **null** ist (die-Eigenschaft hat keinen gültigen oder sinnvollen Wert).</span><span class="sxs-lookup"><span data-stu-id="51cb9-307">Value that indicates that the associated property is **NULL** (the property does not have a valid or meaningful value).</span></span> <span data-ttu-id="51cb9-308">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-308">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-309">Die Konventionen und Einschränkungen, die zum Definieren von **null** -Werten verwendet werden, entsprechen den Konventionen für den **ValueMap** -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="51cb9-309">The conventions and restrictions used for defining **NULL** values are the same as those applicable to the **ValueMap** qualifier.</span></span> <span data-ttu-id="51cb9-310">Hinweis Dieser Qualifizierer kann nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-310">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="51cb9-311">Es ist nicht sinnvoll, einer Unterklasse die Rückgabe eines anderen **null** -Werts als der der übergeordneten Klasse zuzulassen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-311">It is unreasonable to permit a subclass to return a different **NULL** value than that of the parent class.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Vorgenommen**</span><span class="sxs-lookup"><span data-stu-id="51cb9-312"><span id="Out"></span><span id="out"></span><span id="OUT"></span>**Out**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-313">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-313">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-314">Gilt für: Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-314">Applies to: parameters</span></span>

<span data-ttu-id="51cb9-315">Gibt an, ob der Parameterwerte aus einer Methode zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="51cb9-315">Indicates whether the parameter returns values from a method.</span></span> <span data-ttu-id="51cb9-316">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-316">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Dire**</span><span class="sxs-lookup"><span data-stu-id="51cb9-317"><span id="Override"></span><span id="override"></span><span id="OVERRIDE"></span>**Override**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-318">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-318">Data type: **string**</span></span>

<span data-ttu-id="51cb9-319">Gilt für: Eigenschaften, Methoden, Verweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-319">Applies to: properties, methods, references</span></span>

<span data-ttu-id="51cb9-320">Die übergeordnete Klasse oder das untergeordnete Konstrukt (Eigenschaft, Methode oder Verweis), die durch die Eigenschaft, die Methode oder den Verweis desselben Namens in der abgeleiteten Klasse überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="51cb9-320">Parent class or subordinate construct (property, method, or reference) which is overridden by the property, method, or reference of the same name in the derived class.</span></span> <span data-ttu-id="51cb9-321">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-321">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-322">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="51cb9-322">The format is:</span></span>

<span data-ttu-id="51cb9-323">\[<*Klassen*>. \] < unter *geordnetes Konstrukt*></span><span class="sxs-lookup"><span data-stu-id="51cb9-323">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="51cb9-324">Wenn der Klassenname weggelassen wird, gilt die außer Kraft setzung für das untergeordnete Konstrukt in der übergeordneten Klasse in der Klassenhierarchie.</span><span class="sxs-lookup"><span data-stu-id="51cb9-324">If the class name is omitted, the override applies to the subordinate construct in the parent class in the class hierarchy.</span></span>

<span data-ttu-id="51cb9-325">Verwendung: der **Überschreibungs** Qualifizierer kann auf Konstrukte verweisen, die auf dem gleichen Meta-Modell basieren.</span><span class="sxs-lookup"><span data-stu-id="51cb9-325">Usage: The **Override** qualifier can refer to constructs based on the same meta model only.</span></span> <span data-ttu-id="51cb9-326">Es ist nicht zulässig, bei einem Überschreibungs Vorgang einen Konstruktnamen oder eine Signatur zu ändern.</span><span class="sxs-lookup"><span data-stu-id="51cb9-326">It is not allowed to change a construct name or signature during an override operation.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**Override Value**</span><span class="sxs-lookup"><span data-stu-id="51cb9-327"><span id="OverrideValue"></span><span id="overridevalue"></span><span id="OVERRIDEVALUE"></span>**OverrideValue**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-328">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="51cb9-328">Applies to: classes</span></span>

<span data-ttu-id="51cb9-329">Gibt an, ob der Eigenschafts Wert einer Unterklasse den Wert in einer übergeordneten Klasse überschreibt.</span><span class="sxs-lookup"><span data-stu-id="51cb9-329">Indicates whether the property value on a subclass overrides the value in a parent class.</span></span> <span data-ttu-id="51cb9-330">Wenn Sie eine Abfrage für die übergeordnete Klasse ausführen und die **Where** -Klausel diese Eigenschaft enthält, muss das übergeordnete Element eine Instanz mit dem überschriebenen Wert zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="51cb9-330">The functional implication is that, if you perform a query against the parent class, and if your **WHERE** clause includes this property, the parent must return an instance with the overridden value.</span></span> <span data-ttu-id="51cb9-331">Folglich passt die Windows-Verwaltung die **Where** -Klausel der Abfrage an, die an die übergeordnete Klasse gesendet wird, um Verweise auf diese Eigenschaft auszuschließen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-331">As a result, Windows Management adjusts the **WHERE** clause of the query sent to the parent class to exclude references to this property.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Gepflanzt**</span><span class="sxs-lookup"><span data-stu-id="51cb9-332"><span id="Propagated"></span><span id="propagated"></span><span id="PROPAGATED"></span>**Propagated**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-333">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-333">Data type: **string**</span></span>

<span data-ttu-id="51cb9-334">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51cb9-334">Applies to: properties</span></span>

<span data-ttu-id="51cb9-335">Der Name des Schlüssels, der weitergegeben wird.</span><span class="sxs-lookup"><span data-stu-id="51cb9-335">Name of the key being propagated.</span></span> <span data-ttu-id="51cb9-336">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-336">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-337">Die Verwendung dieses Qualifizierers geht davon aus, dass es nur einen schwachen Qualifizierer für einen Verweis gibt, der die enthaltende Klasse als Ziel hat.</span><span class="sxs-lookup"><span data-stu-id="51cb9-337">Use of this qualifier assumes the existence of only one weak qualifier on a reference that has the containing class as its target.</span></span> <span data-ttu-id="51cb9-338">Die zugeordnete Eigenschaft muss denselben Wert wie die Eigenschaft aufweisen, die durch den Qualifizierer in der Klasse auf der anderen Seite der schwachen Zuordnung benannt wird.</span><span class="sxs-lookup"><span data-stu-id="51cb9-338">The associated property must have the same value as the property named by the qualifier in the class on the other side of the weak association.</span></span> <span data-ttu-id="51cb9-339">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="51cb9-339">The format is:</span></span>

<span data-ttu-id="51cb9-340">\[<*Klassen*>. \] < unter *geordnetes Konstrukt*></span><span class="sxs-lookup"><span data-stu-id="51cb9-340">\[<*class*>.\]<*subordinate construct*></span></span>

<span data-ttu-id="51cb9-341">Verwendung: Wenn der **propagierte** Qualifizierer verwendet wird, muss der [**Schlüssel**](key-qualifier.md) Qualifizierer mit dem Wert " **true**" angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-341">Usage: When the **Propagated** qualifier is used, the [**Key**](key-qualifier.md) qualifier must be specified with a value of **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Dazu**</span><span class="sxs-lookup"><span data-stu-id="51cb9-342"><span id="Read"></span><span id="read"></span><span id="READ"></span>**Read**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-343">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-343">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-344">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51cb9-344">Applies to: properties</span></span>

<span data-ttu-id="51cb9-345">Gibt an, ob die-Eigenschaft lesbar ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-345">Indicates whether the property is readable.</span></span> <span data-ttu-id="51cb9-346">Der Standardwert ist " **true**".</span><span class="sxs-lookup"><span data-stu-id="51cb9-346">The default is **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="51cb9-347"><span id="Required"></span><span id="required"></span><span id="REQUIRED"></span>**Required**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-348">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-348">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-349">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51cb9-349">Applies to: properties</span></span>

<span data-ttu-id="51cb9-350">Gibt an, ob ein nicht-NULL-Wert für die-Eigenschaft erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-350">Indicates whether a non-null value is required for the property.</span></span> <span data-ttu-id="51cb9-351">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-351">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Novel**</span><span class="sxs-lookup"><span data-stu-id="51cb9-352"><span id="Revision"></span><span id="revision"></span><span id="REVISION"></span>**Revision**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-353">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-353">Data type: **string**</span></span>

<span data-ttu-id="51cb9-354">Gilt für: Klassen, Zuordnungen, Hinweise, Schemas</span><span class="sxs-lookup"><span data-stu-id="51cb9-354">Applies to: classes, associations, indications, schemas</span></span>

<span data-ttu-id="51cb9-355">Die neben Versionsnummer des Schema Objekts.</span><span class="sxs-lookup"><span data-stu-id="51cb9-355">Minor revision number of the schema object.</span></span> <span data-ttu-id="51cb9-356">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-356">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-357">Verwendung: der **Versions** Qualifizierer muss vorhanden sein, um die Hauptversionsnummer anzugeben, wenn der **Revisions** Qualifizierer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="51cb9-357">Usage: The **Version** qualifier must be present to supply the major version number when the **Revision** qualifier is used.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Chaos**</span><span class="sxs-lookup"><span data-stu-id="51cb9-358"><span id="Schema"></span><span id="schema"></span><span id="SCHEMA"></span>**Schema**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-359">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-359">Data type: **string**</span></span>

<span data-ttu-id="51cb9-360">Gilt für: Eigenschaften, Methoden</span><span class="sxs-lookup"><span data-stu-id="51cb9-360">Applies to: properties, methods</span></span>

<span data-ttu-id="51cb9-361">Der Name des Schemas, in dem das Feature definiert ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-361">Name of the schema in which the feature is defined.</span></span> <span data-ttu-id="51cb9-362">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-362">The default is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Ausgangs**</span><span class="sxs-lookup"><span data-stu-id="51cb9-363"><span id="Source"></span><span id="source"></span><span id="SOURCE"></span>**Source**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-364">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-364">Data type: **string**</span></span>

<span data-ttu-id="51cb9-365">Gilt für: Klassen, Zuordnungen, Hinweise, Verweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-365">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="51cb9-366">Der Speicherort einer Instanz.</span><span class="sxs-lookup"><span data-stu-id="51cb9-366">Location of an instance.</span></span> <span data-ttu-id="51cb9-367">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-367">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-368">Der Qualifizierer Wert ist <*NamespaceType*>://<*namespacehandle* ->.</span><span class="sxs-lookup"><span data-stu-id="51cb9-368">The qualifier's value is <*namespacetype*>://<*namespacehandle*>.</span></span>

<span data-ttu-id="51cb9-369">Verwendung: der **Quellen** Qualifizierer kann nicht mit dem **sourceType** -Qualifizierer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-369">Usage: The **Source** qualifier cannot be used with the **SourceType** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span><span class="sxs-lookup"><span data-stu-id="51cb9-370"><span id="SourceType"></span><span id="sourcetype"></span><span id="SOURCETYPE"></span>**SourceType**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-371">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-371">Data type: **string**</span></span>

<span data-ttu-id="51cb9-372">Gilt für: Klassen, Zuordnungen, Hinweise, Verweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-372">Applies to: classes, associations, indications, references</span></span>

<span data-ttu-id="51cb9-373">Der Typ des Speicher Orts einer Instanz.</span><span class="sxs-lookup"><span data-stu-id="51cb9-373">Type of location of an instance.</span></span> <span data-ttu-id="51cb9-374">Der Wert dieses Qualifizierers ist <*NamespaceType*>.</span><span class="sxs-lookup"><span data-stu-id="51cb9-374">The value of this qualifier is <*namespacetype*>.</span></span> <span data-ttu-id="51cb9-375">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-375">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-376">Verwendung: der **sourceType** -Qualifizierer kann nicht mit dem **Quell** Qualifizierer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-376">Usage: The **SourceType** qualifier cannot be used with the **Source** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span><span class="sxs-lookup"><span data-stu-id="51cb9-377"><span id="SupportsCreate"></span><span id="supportscreate"></span><span id="SUPPORTSCREATE"></span>**SupportsCreate**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-378">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-378">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-379">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="51cb9-379">Applies to: classes</span></span>

<span data-ttu-id="51cb9-380">Gibt an, ob die-Klasse die Erstellung von-Instanzen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51cb9-380">Indicates whether the class supports the creation of instances.</span></span> <span data-ttu-id="51cb9-381">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-381">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span><span class="sxs-lookup"><span data-stu-id="51cb9-382"><span id="SupportsDelete"></span><span id="supportsdelete"></span><span id="SUPPORTSDELETE"></span>**SupportsDelete**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-383">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-383">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-384">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="51cb9-384">Applies to: classes</span></span>

<span data-ttu-id="51cb9-385">Gibt an, ob die-Klasse das Löschen von-Instanzen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51cb9-385">Indicates whether the class supports the deletion of instances.</span></span> <span data-ttu-id="51cb9-386">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-386">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**Supportsupdate**</span><span class="sxs-lookup"><span data-stu-id="51cb9-387"><span id="SupportsUpdate"></span><span id="supportsupdate"></span><span id="SUPPORTSUPDATE"></span>**SupportsUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-388">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-388">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-389">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="51cb9-389">Applies to: classes</span></span>

<span data-ttu-id="51cb9-390">Gibt an, ob die-Klasse das ändern (aktualisieren) der-Instanzen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51cb9-390">Indicates whether the class supports the modification (updating) of instances.</span></span> <span data-ttu-id="51cb9-391">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-391">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Vergütungen**</span><span class="sxs-lookup"><span data-stu-id="51cb9-392"><span id="Terminal"></span><span id="terminal"></span><span id="TERMINAL"></span>**Terminal**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-393">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-393">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-394">Gilt für: Klassen</span><span class="sxs-lookup"><span data-stu-id="51cb9-394">Applies to: classes</span></span>

<span data-ttu-id="51cb9-395">Gibt an, ob die Klasse Unterklassen aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="51cb9-395">Indicates whether the class can have subclasses.</span></span> <span data-ttu-id="51cb9-396">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-396">The default is **FALSE**.</span></span>

<span data-ttu-id="51cb9-397">Wenn eine Unterklasse deklariert wird, generiert der Compiler einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="51cb9-397">If a subclass is declared, the compiler generates an error.</span></span>

<span data-ttu-id="51cb9-398">Verwendung: dieser Qualifizierer kann nicht mit dem **abstrakten** Qualifizierer koexistieren</span><span class="sxs-lookup"><span data-stu-id="51cb9-398">Usage: This qualifier cannot coexist with the **Abstract** qualifier.</span></span> <span data-ttu-id="51cb9-399">Wenn sowohl der **Terminal** -als auch der **abstrakte** Qualifizierer angegeben werden, generiert der Compiler einen Fehler.</span><span class="sxs-lookup"><span data-stu-id="51cb9-399">If both the **Terminal** and **Abstract** qualifiers are specified, the compiler generates an error.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Einrichtungen**</span><span class="sxs-lookup"><span data-stu-id="51cb9-400"><span id="Units"></span><span id="units"></span><span id="UNITS"></span>**Units**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-401">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-401">Data type: **string**</span></span>

<span data-ttu-id="51cb9-402">Gilt für: Eigenschaften, Methoden, Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-402">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="51cb9-403">Der Typ der Einheit, in der das zugeordnete Datenelement ausgedrückt wird.</span><span class="sxs-lookup"><span data-stu-id="51cb9-403">Type of unit in which the associated data item is expressed.</span></span> <span data-ttu-id="51cb9-404">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-404">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-405">Beispielsweise kann ein Größendaten Element für **Einheiten** den Wert "Bytes" aufweisen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-405">For example, a size data item might have a value of "bytes" for **Units**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span><span class="sxs-lookup"><span data-stu-id="51cb9-406"><span id="ValueMap"></span><span id="valuemap"></span><span id="VALUEMAP"></span>**ValueMap**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-407">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="51cb9-407">Data type: **string array**</span></span>

<span data-ttu-id="51cb9-408">Gilt für: Eigenschaften, Methoden, Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-408">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="51cb9-409">Der Satz zulässiger Werte für eine Eigenschaft, einen Methoden Rückgabetyp oder einen Methoden Parameter.</span><span class="sxs-lookup"><span data-stu-id="51cb9-409">Set of permissible values for a property, method return type, or method parameter.</span></span> <span data-ttu-id="51cb9-410">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-410">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-411">Verwendung: dieser Qualifizierer kann allein oder in Kombination mit dem **Werte** Qualifizierer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-411">Usage: This qualifier can be used alone or in combination with the **Values** qualifier.</span></span> <span data-ttu-id="51cb9-412">Bei Verwendung in Kombination mit dem **Values** -Qualifizierer stellt die Position des Werts im **ValueMap** -Array den Speicherort des entsprechenden Eintrags im **Values** -Array bereit.</span><span class="sxs-lookup"><span data-stu-id="51cb9-412">When used in combination with the **Values** qualifier, the location of the value in the **ValueMap** array provides the location of the corresponding entry in the **Values** array.</span></span> <span data-ttu-id="51cb9-413">Verwenden Sie den **ValueMap** -Qualifizierer nur mit String-und Integer-Werten.</span><span class="sxs-lookup"><span data-stu-id="51cb9-413">Use the **ValueMap** qualifier only with string and integer values.</span></span> <span data-ttu-id="51cb9-414">Die Syntax für die Darstellung eines ganzzahligen Werts im Wertkarten Array ist eine \[ + \| = \] Ziffern \[ \* Ziffer \] .</span><span class="sxs-lookup"><span data-stu-id="51cb9-414">The syntax for representing an integer value in the value map array is \[+\|=\]digit\[\*digit\].</span></span> <span data-ttu-id="51cb9-415">Der Inhalt, die maximale Anzahl von Ziffern und der dargestellte Wert werden durch den Typ der zugeordneten Eigenschaft eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="51cb9-415">The content, maximum number of digits, and represented value are constrained by the type of the associated property.</span></span> <span data-ttu-id="51cb9-416">Beispielsweise kann Uint8 nicht signiert werden, muss kleiner als vier Ziffern sein und muss einen Wert kleiner als 256 darstellen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-416">For example, uint8 may not be signed, must be less than four digits, and must represent a value less than 256.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Werte**</span><span class="sxs-lookup"><span data-stu-id="51cb9-417"><span id="Values"></span><span id="values"></span><span id="VALUES"></span>**Values**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-418">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="51cb9-418">Data type: **string array**</span></span>

<span data-ttu-id="51cb9-419">Gilt für: Eigenschaften, Methoden, Parameter</span><span class="sxs-lookup"><span data-stu-id="51cb9-419">Applies to: properties, methods, parameters</span></span>

<span data-ttu-id="51cb9-420">Satz von Werten, der einen ganzzahligen Wert in eine zugeordnete Zeichenfolge übersetzt.</span><span class="sxs-lookup"><span data-stu-id="51cb9-420">Set of values translating an integer value into an associated string.</span></span> <span data-ttu-id="51cb9-421">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-421">The default is **NULL**.</span></span>

<span data-ttu-id="51cb9-422">Diese Eigenschaft gibt auch ein Array von Zeichen folgen Werten an, die einer Enumerationseigenschaft zugeordnet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="51cb9-422">This property also specifies an array of string values to be mapped to an enumeration property.</span></span> <span data-ttu-id="51cb9-423">Dieser Qualifizierer kann entweder auf eine ganzzahlige Eigenschaft oder eine Zeichen folgen Eigenschaft angewendet werden, und die Zuordnung kann implizit oder explizit sein.</span><span class="sxs-lookup"><span data-stu-id="51cb9-423">This qualifier can be applied to either an integer property or a string property, and the mapping can be implicit or explicit.</span></span> <span data-ttu-id="51cb9-424">Wenn die Zuordnung implizit ist, stellen ganzzahlige Werte oder Zeichen folgen Eigenschaftswerte Ordinalpositionen im **Werte** Array dar.</span><span class="sxs-lookup"><span data-stu-id="51cb9-424">If the mapping is implicit, integer or string property values represent ordinal positions in the **Values** array.</span></span> <span data-ttu-id="51cb9-425">Wenn die Zuordnung explizit ist, muss die-Eigenschaft eine ganze Zahl sein, und gültige Eigenschaftswerte werden in dem Array aufgelistet, das durch den **ValueMap** -Qualifizierer definiert ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-425">If the mapping is explicit, the property must be an integer, and valid property values are listed in the array defined by the **ValueMap** qualifier.</span></span> <span data-ttu-id="51cb9-426">Weitere Informationen finden Sie unter [Value Map](value-map.md).</span><span class="sxs-lookup"><span data-stu-id="51cb9-426">For more information, see [Value Map](value-map.md).</span></span>

<span data-ttu-id="51cb9-427">Wenn kein **ValueMap** -Qualifizierer vorhanden ist, wird das **Values** -Array mit dem Wert in der zugeordneten Eigenschaft, dem Methoden Rückgabetyp oder dem Methoden Parameter indiziert (null-relativ).</span><span class="sxs-lookup"><span data-stu-id="51cb9-427">If a **ValueMap** qualifier is not present, the **Values** array is indexed (zero-relative) by using the value in the associated property, method return type, or method parameter.</span></span> <span data-ttu-id="51cb9-428">Wenn ein **ValueMap** -Qualifizierer vorhanden ist, wird der Values-Index durch den Speicherort des Eigenschafts Werts in der Werte Zuordnung definiert.</span><span class="sxs-lookup"><span data-stu-id="51cb9-428">If a **ValueMap** qualifier is present, the values index is defined by the location of the property value in the value map.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span><span class="sxs-lookup"><span data-stu-id="51cb9-429"><span id="Version"></span><span id="version"></span><span id="VERSION"></span>**Version**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-430">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="51cb9-430">Data type: **string**</span></span>

<span data-ttu-id="51cb9-431">Gilt für: Klassen, Schemas, Zuordnungen, Hinweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-431">Applies to: classes, schemas, associations, indications</span></span>

<span data-ttu-id="51cb9-432">Die Hauptversionsnummer des Schema Objekts.</span><span class="sxs-lookup"><span data-stu-id="51cb9-432">Major version number of the schema object.</span></span> <span data-ttu-id="51cb9-433">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-433">The default is **NULL**.</span></span> <span data-ttu-id="51cb9-434">Die Versionsnummer wird inkrementiert, wenn Änderungen am Schema vorgenommen werden, die die Schnittstelle ändern.</span><span class="sxs-lookup"><span data-stu-id="51cb9-434">The version number is incremented when changes are made to the schema that alter the interface.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Weak**</span><span class="sxs-lookup"><span data-stu-id="51cb9-435"><span id="Weak"></span><span id="weak"></span><span id="WEAK"></span>**Weak**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-436">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-436">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-437">Gilt für: Verweise</span><span class="sxs-lookup"><span data-stu-id="51cb9-437">Applies to: references</span></span>

<span data-ttu-id="51cb9-438">Gibt an, ob die Schlüssel der Klasse, auf die verwiesen wird, die Schlüssel der anderen Teilnehmer in der Zuordnung enthalten.</span><span class="sxs-lookup"><span data-stu-id="51cb9-438">Indicates whether the keys of the referenced class include the keys of the other participants in the association.</span></span> <span data-ttu-id="51cb9-439">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-439">The default is **FALSE**.</span></span>

<span data-ttu-id="51cb9-440">Dieser Qualifizierer wird verwendet, wenn die Identität der Klasse, auf die verwiesen wird, von der Identität der anderen Teilnehmer in der Zuordnung abhängt.</span><span class="sxs-lookup"><span data-stu-id="51cb9-440">This qualifier is used when the identity of the referenced class depends on the identity of the other participants in the association.</span></span> <span data-ttu-id="51cb9-441">Es kann nicht mehr als ein Verweis auf eine bestimmte Klasse schwach sein.</span><span class="sxs-lookup"><span data-stu-id="51cb9-441">No more than one reference to any given class can be weak.</span></span> <span data-ttu-id="51cb9-442">Die anderen Klassen in der Zuordnung müssen einen Schlüssel definieren.</span><span class="sxs-lookup"><span data-stu-id="51cb9-442">The other classes in the association must define a key.</span></span> <span data-ttu-id="51cb9-443">Die Schlüssel der anderen Klassen in der Zuordnung werden in der referenzierten Klasse wiederholt und mit einem **propagierten** Qualifizierer gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="51cb9-443">The keys of the other classes in the association are repeated in the referenced class and are tagged with a **Propagated** qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Schreibung**</span><span class="sxs-lookup"><span data-stu-id="51cb9-444"><span id="Write"></span><span id="write"></span><span id="WRITE"></span>**Write**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-445">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-445">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-446">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51cb9-446">Applies to: properties</span></span>

<span data-ttu-id="51cb9-447">Gibt an, dass Anwendungen oder Skripts den Eigenschafts Wert ändern können.</span><span class="sxs-lookup"><span data-stu-id="51cb9-447">Indicates that applications or scripts can change the property value.</span></span> <span data-ttu-id="51cb9-448">Das Konto, das die Anwendung ausführt, muss Zugriff auf den Namespace haben, der Instanzen der-Klasse enthält.</span><span class="sxs-lookup"><span data-stu-id="51cb9-448">The account that runs the application must have access to the namespace that contains instances of the class.</span></span> <span data-ttu-id="51cb9-449">Die Anbieter Implementierung schränkt möglicherweise auch den Zugriff auf Anbieter Daten ein.</span><span class="sxs-lookup"><span data-stu-id="51cb9-449">The provider implementation may also limit access to provider data.</span></span> <span data-ttu-id="51cb9-450">Der Wert **true** gibt an, dass die Eigenschaft von Consumern lesbar und schreibbar ist, denen der Zugriff durch WMI und den Anbieter gestattet ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-450">A value of **TRUE** indicates that the property is readable and writeable by consumers that are allowed access by WMI and the provider.</span></span> <span data-ttu-id="51cb9-451">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-451">The default is **FALSE**.</span></span>

<span data-ttu-id="51cb9-452">Eine Eigenschaft, die nicht über den **Schreib** Qualifizierer verfügt, kann möglicherweise weiterhin geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-452">A property that lacks the **Write** qualifier may still be writeable.</span></span> <span data-ttu-id="51cb9-453">Die Anbieter Implementierung lässt möglicherweise zu, dass alle Eigenschaften in den Anbieter Klassen geändert werden, unabhängig davon, ob der **Schreib** Qualifizierer vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-453">The provider implementation may allow any properties in the provider classes to be changed, whether the **Write** qualifier is present.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**Schreibzugriff erstellen**</span><span class="sxs-lookup"><span data-stu-id="51cb9-454"><span id="WriteAtCreate"></span><span id="writeatcreate"></span><span id="WRITEATCREATE"></span>**WriteAtCreate**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-455">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-455">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-456">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51cb9-456">Applies to: properties</span></span>

<span data-ttu-id="51cb9-457">Gibt an, ob die Eigenschaft bei der Instanzerstellung beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-457">Indicates whether the property is writeable at instance creation.</span></span> <span data-ttu-id="51cb9-458">Dieser Qualifizierer kann in Verbindung mit dem **schreiberstellungs** -Qualifizierer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-458">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="51cb9-459">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-459">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="51cb9-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**Write-Update**</span><span class="sxs-lookup"><span data-stu-id="51cb9-460"><span id="WriteAtUpdate"></span><span id="writeatupdate"></span><span id="WRITEATUPDATE"></span>**WriteAtUpdate**</span></span>
</dt> <dd>

<span data-ttu-id="51cb9-461">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-461">Data type: **boolean**</span></span>

<span data-ttu-id="51cb9-462">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="51cb9-462">Applies to: properties</span></span>

<span data-ttu-id="51cb9-463">Gibt an, ob die Eigenschaft beim instanzupdate beschreibbar ist.</span><span class="sxs-lookup"><span data-stu-id="51cb9-463">Indicates whether the property is writeable at instance update.</span></span> <span data-ttu-id="51cb9-464">Dieser Qualifizierer kann in Verbindung mit dem **schreiberstellungs** -Qualifizierer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="51cb9-464">This qualifier may be used in conjunction with the **WriteAtCreate** qualifier.</span></span> <span data-ttu-id="51cb9-465">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="51cb9-465">The default is **FALSE**.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="51cb9-466">Beispiele</span><span class="sxs-lookup"><span data-stu-id="51cb9-466">Examples</span></span>

<span data-ttu-id="51cb9-467">Weitere Informationen zum Abrufen von Qualifizierern finden Sie im PowerShell-Codebeispiel [Get-wmiclassmethodsandwrite](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) in der TechNet Gallery.</span><span class="sxs-lookup"><span data-stu-id="51cb9-467">For more information on retrieving qualifiers, see the [Get-WmiClassMethodsAndWritableWmiProperties](https://Gallery.TechNet.Microsoft.Com/10670e14-4cf1-4ce5-99d0-fc4ca80dac2c) PowerShell code sample on the TechNet Gallery.</span></span>

## <a name="requirements"></a><span data-ttu-id="51cb9-468">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="51cb9-468">Requirements</span></span>



| <span data-ttu-id="51cb9-469">Anforderung</span><span class="sxs-lookup"><span data-stu-id="51cb9-469">Requirement</span></span> | <span data-ttu-id="51cb9-470">Wert</span><span class="sxs-lookup"><span data-stu-id="51cb9-470">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="51cb9-471">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="51cb9-471">Minimum supported client</span></span><br/> | <span data-ttu-id="51cb9-472">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="51cb9-472">Windows Vista</span></span><br/>       |
| <span data-ttu-id="51cb9-473">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="51cb9-473">Minimum supported server</span></span><br/> | <span data-ttu-id="51cb9-474">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="51cb9-474">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="51cb9-475">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51cb9-475">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51cb9-476">WMI Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="51cb9-476">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="51cb9-477">Fügen eines Qualifizierers</span><span class="sxs-lookup"><span data-stu-id="51cb9-477">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




