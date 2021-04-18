---
description: Optionale Qualifizierer behandeln wiederkehrende Situationen, die nicht für alle CIM-kompatiblen Implementierungen gelten, die für die Interpretation dieser Qualifizierer nicht erforderlich sind.
ms.assetid: f31162d1-25e6-494a-bc7d-f66955b514a6
ms.tgt_platform: multiple
title: Optionale Qualifizierer
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Optional
api_type:
- NA
api_location: ''
ms.openlocfilehash: 36fe1b9ceee1211a3b09ce70e03044b7af57eac2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351081"
---
# <a name="optional-qualifiers"></a><span data-ttu-id="b3bb4-103">Optionale Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="b3bb4-103">Optional Qualifiers</span></span>

<span data-ttu-id="b3bb4-104">Optionale Qualifizierer behandeln wiederkehrende Situationen, die nicht für alle CIM-kompatiblen Implementierungen gelten, die für die Interpretation dieser Qualifizierer nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-104">Optional qualifiers address recurring situations not common to all CIM-compliant implementations, which are not required to interpret these qualifiers.</span></span> <span data-ttu-id="b3bb4-105">Optionale Qualifizierer werden in der Spezifikation bereitgestellt, um zufällige benutzerdefinierte Qualifizierer zu vermeiden, die in diesen wiederkehrenden Situationen auftreten können.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-105">Optional qualifiers are provided in the specification to avoid random user-defined qualifiers that might occur in these recurring situations.</span></span>

<dt>

<span data-ttu-id="b3bb4-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Lösch**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-106"><span id="Delete"></span><span id="delete"></span><span id="DELETE"></span>**Delete**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-107">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b3bb4-107">Data type: **boolean**</span></span>

<span data-ttu-id="b3bb4-108">Gilt für: Zuordnungen, Verweise</span><span class="sxs-lookup"><span data-stu-id="b3bb4-108">Applies to: associations, references</span></span>

<span data-ttu-id="b3bb4-109">Gibt für Zuordnungen an, ob die qualifizierte Zuordnung gelöscht werden muss, wenn eines der Objekte, auf die in der Zuordnung verwiesen wird, gelöscht wird und das entsprechende Objekt, auf das in der Zuordnung verwiesen wird, mit **ifdeleted** qualifiziert ist.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-109">For associations, indicates whether the qualified association must be deleted if any of the objects referenced in the association are deleted and if the respective object referenced in the association is qualified with **IfDeleted**.</span></span> <span data-ttu-id="b3bb4-110">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-110">The default is **FALSE**.</span></span>

<span data-ttu-id="b3bb4-111">Bei verweisen gibt dieser Qualifizierer an, ob das Objekt, auf das verwiesen wird, gelöscht werden muss, wenn die Zuordnung, die den Verweis enthält, gelöscht **und mit** **ifdeleted** qualifiziert wird, oder wenn eines der Objekte, auf die in der Zuordnung verwiesen wird, gelöscht wird und das entsprechende Objekt, auf das in der Zuordnung verwiesen wird</span><span class="sxs-lookup"><span data-stu-id="b3bb4-111">For references, this qualifier indicates whether the referenced object must be deleted if the association containing the reference is deleted and qualified with **IfDeleted**, or if any of the objects referenced in the association are deleted and the respective object referenced in the association is qualified with **IfDeleted**.</span></span>

<span data-ttu-id="b3bb4-112">Verwendung: Anwendungen müssen mit dem **Delete** -Qualifizierer markierte Zuordnungen und Verweise nachverfolgen und die Zuordnung oder den Verweis entsprechend löschen.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-112">Usage: Applications must track associations and references marked with the **Delete** qualifier and delete the association or reference appropriately.</span></span> <span data-ttu-id="b3bb4-113">Wenn ein Objekt in der Zuordnung gelöscht, aber nicht mit **ifdeleted** gekennzeichnet wurde, sollte die Zuordnung nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-113">If an object in the association has been deleted but is not marked with **IfDeleted**, then the association should not be deleted.</span></span>

<span data-ttu-id="b3bb4-114">Diese Verwendungs Regel muss überprüft werden, wenn das CIM-Sicherheitsmodell definiert ist.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-114">This usage rule must be verified when the CIM security model is defined.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Eres**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-115"><span id="Expensive"></span><span id="expensive"></span><span id="EXPENSIVE"></span>**Expensive**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-116">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b3bb4-116">Data type: **boolean**</span></span>

<span data-ttu-id="b3bb4-117">Gilt für: Eigenschaften, Verweise, Klassen, Zuordnungen, Methoden</span><span class="sxs-lookup"><span data-stu-id="b3bb4-117">Applies to: properties, references, classes, associations, methods</span></span>

<span data-ttu-id="b3bb4-118">Gibt an, ob die implizite Aktion eine umfangreiche Berechnung erfordert.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-118">Indicates whether the implied action requires extensive computation.</span></span> <span data-ttu-id="b3bb4-119">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-119">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**Ifdeleted**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-120"><span id="IfDeleted"></span><span id="ifdeleted"></span><span id="IFDELETED"></span>**IfDeleted**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-121">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b3bb4-121">Data type: **boolean**</span></span>

<span data-ttu-id="b3bb4-122">Gilt für: Zuordnungen und Verweise</span><span class="sxs-lookup"><span data-stu-id="b3bb4-122">Applies to: associations and references</span></span>

<span data-ttu-id="b3bb4-123">Gibt an, ob alle Objekte innerhalb einer durch **Delete** gekennzeichneten Zuordnung gelöscht werden müssen, wenn das Objekt, auf das verwiesen wird, oder die Zuordnung gelöscht wird.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-123">Indicates whether all objects within an association that is qualified by **Delete** must be deleted if the referenced object or the association is deleted.</span></span> <span data-ttu-id="b3bb4-124">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-124">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Zierenden**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-125"><span id="Indexed"></span><span id="indexed"></span><span id="INDEXED"></span>**Indexed**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-126">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b3bb4-126">Data type: **boolean**</span></span>

<span data-ttu-id="b3bb4-127">Gilt für: Eigenschaften, Methoden</span><span class="sxs-lookup"><span data-stu-id="b3bb4-127">Applies to: properties, methods</span></span>

<span data-ttu-id="b3bb4-128">Gibt an, ob eine Klassen Eigenschaft indiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-128">Indicates whether a class property should be indexed.</span></span> <span data-ttu-id="b3bb4-129">Dies hat bei der Anwendung auf Eigenschaften in Klassen, die vom Repository gehostet werden, nur die Bedeutung, dass (zum Zeitpunkt der Klassen Erstellung) eine schnelle sekundäre Abfrage Suche für diese Eigenschaft erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-129">When applied to properties in classes hosted by the repository, this only has the meaning of creating (at the time of class creation) a fast secondary query lookup for that property.</span></span>

<span data-ttu-id="b3bb4-130">Nur der Wert **true** (Standard) ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-130">Only the value **TRUE** (default) is allowed.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Unsichtbar**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-131"><span id="Invisible"></span><span id="invisible"></span><span id="INVISIBLE"></span>**Invisible**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-132">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b3bb4-132">Data type: **boolean**</span></span>

<span data-ttu-id="b3bb4-133">Gilt für: Zuordnungen, Eigenschaften, Methoden, Verweise, Klassen</span><span class="sxs-lookup"><span data-stu-id="b3bb4-133">Applies to: associations, properties, methods, references, classes</span></span>

<span data-ttu-id="b3bb4-134">Gibt an, ob die Zuordnung nur für interne Zwecke definiert ist (z. b. für die Definition der Abhängigkeits Semantik) und nicht angezeigt werden soll (z. b. in Maps).</span><span class="sxs-lookup"><span data-stu-id="b3bb4-134">Indicates whether the association is defined only for internal purposes (for example, for definition of dependency semantics) and should not be displayed (for example, in maps).</span></span> <span data-ttu-id="b3bb4-135">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-135">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Viele**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-136"><span id="Large"></span><span id="large"></span><span id="LARGE"></span>**Large**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-137">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b3bb4-137">Data type: **boolean**</span></span>

<span data-ttu-id="b3bb4-138">Gilt für: Eigenschaften, Klassen</span><span class="sxs-lookup"><span data-stu-id="b3bb4-138">Applies to: properties, classes</span></span>

<span data-ttu-id="b3bb4-139">Gibt an, ob für die Eigenschaft oder Klasse eine große Menge an Speicherplatz erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-139">Indicates whether the property or class requires a large amount of storage space.</span></span> <span data-ttu-id="b3bb4-140">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-140">The default is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Nicht \_ null**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-141"><span id="Not_Null"></span><span id="not_null"></span><span id="NOT_NULL"></span>**Not\_Null**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-142">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b3bb4-142">Data type: **boolean**</span></span>

<span data-ttu-id="b3bb4-143">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3bb4-143">Applies to: properties</span></span>

<span data-ttu-id="b3bb4-144">Gibt an, ob eine Klassen Eigenschaft einen **null** -Wert (**VT \_ null**) nicht annehmen kann.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-144">Indicates whether a class property cannot take on a value of **NULL** (**VT\_NULL**).</span></span> <span data-ttu-id="b3bb4-145">Nur der Wert **true** (Standard) ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-145">Only the value **TRUE** (default) is allowed.</span></span>

<span data-ttu-id="b3bb4-146">Wenn dieser Qualifizierer angegeben wird, lässt WMI keine Erstellung von-Instanzen zu, deren-Eigenschaft auf **null** festgelegt ist, und **null** -Eigenschaften geben den Fehlercode " **WBEM \_ E unzulässig \_ \_ null** " zurück.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-146">If this qualifier is specified, WMI does not allow creation of instances with the property set to **NULL**, and **NULL** properties return the **WBEM\_E\_ILLEGAL\_NULL** error code.</span></span>

<span data-ttu-id="b3bb4-147">Beachten Sie, dass der [**Schlüssel**](standard-qualifiers.md) und die **indizierten** Qualifizierer dieses Verhalten bereits implizieren.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-147">Note that the [**Key**](standard-qualifiers.md) and **Indexed** qualifiers already imply this behavior.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Ab**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-148"><span id="Provider"></span><span id="provider"></span><span id="PROVIDER"></span>**Provider**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-149">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-149">Data type: **string**</span></span>

<span data-ttu-id="b3bb4-150">Gilt für: beliebig</span><span class="sxs-lookup"><span data-stu-id="b3bb4-150">Applies to: Any</span></span>

<span data-ttu-id="b3bb4-151">Gibt an, dass das Schema Element dynamisch ist und daher von einem Anbieter aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-151">Indication that the schema element is dynamic and thus populated by a provider.</span></span> <span data-ttu-id="b3bb4-152">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-152">The default is **NULL**.</span></span> <span data-ttu-id="b3bb4-153">Dieser Qualifizierer ist ein Implementierungs spezifisches Handle der Instrumentierung.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-153">This qualifier is an implementation-specific handle to the instrumentation.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Eller**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-154"><span id="Experimental"></span><span id="experimental"></span><span id="EXPERIMENTAL"></span>**Experimental**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-155">Datentyp: **boolescher** Wert</span><span class="sxs-lookup"><span data-stu-id="b3bb4-155">Data type: **boolean**</span></span>

<span data-ttu-id="b3bb4-156">Gilt für: beliebig</span><span class="sxs-lookup"><span data-stu-id="b3bb4-156">Applies to: any</span></span>

<span data-ttu-id="b3bb4-157">Gibt an, dass das angegebene Element als Teil einer zukünftigen Freigabe der CIM-Schemas vorgeschlagen wurde, aber noch nicht Teil des Standard Schemas ist.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-157">Indicates that the specified element has been proposed to be a part of a future release of the CIM Schemas, but is not yet part of the standard Schema.</span></span> <span data-ttu-id="b3bb4-158">Stattdessen ist das-Element zum Experimentieren, implementieren und Bereitstellen von Feedback für Benutzer verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-158">Instead, the element is available for users to experiment, implement, and provide feedback on.</span></span> <span data-ttu-id="b3bb4-159">Basierend auf dem Feedback kann das Element dem Standard hinzugefügt werden, wie er dargestellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-159">Based on feedback, the element may added to the standard as presented, modified, or removed.</span></span> <span data-ttu-id="b3bb4-160">Der Standardwert ist **false**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-160">The default is **FALSE**.</span></span> <span data-ttu-id="b3bb4-161">Eine-Implementierung muss kein Element mit diesem Qualifizierer unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-161">An implementation does not have to support an element with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-162"><span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**Syntax**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-163">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-163">Data type: **string**</span></span>

<span data-ttu-id="b3bb4-164">Gilt für: Eigenschaften, Verweise, Methoden, Parameter</span><span class="sxs-lookup"><span data-stu-id="b3bb4-164">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="b3bb4-165">Ein bestimmter Typ, der einem Datenelement zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-165">Specific type assigned to a data item.</span></span> <span data-ttu-id="b3bb4-166">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-166">The default is **NULL**.</span></span>

<span data-ttu-id="b3bb4-167">Verwendung: der **syntaxtype** -Qualifizierer muss mit diesem Qualifizierer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-167">Usage: You must use the **SyntaxType** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**Syntaxtype**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-168"><span id="SyntaxType"></span><span id="syntaxtype"></span><span id="SYNTAXTYPE"></span>**SyntaxType**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-169">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-169">Data type: **string**</span></span>

<span data-ttu-id="b3bb4-170">Gilt für: Eigenschaften, Verweise, Methoden, Parameter</span><span class="sxs-lookup"><span data-stu-id="b3bb4-170">Applies to: properties, references, methods, parameters</span></span>

<span data-ttu-id="b3bb4-171">Das Format des **Syntax** Qualifizierers.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-171">Format of the **Syntax** qualifier.</span></span> <span data-ttu-id="b3bb4-172">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-172">The default is **NULL**.</span></span>

<span data-ttu-id="b3bb4-173">Verwendung: Sie müssen den **Syntax** Qualifizierer mit diesem Qualifizierer verwenden.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-173">Usage: You must use the **Syntax** qualifier with this qualifier.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-174"><span id="TriggerType"></span><span id="triggertype"></span><span id="TRIGGERTYPE"></span>**TriggerType**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-175">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-175">Data type: **string**</span></span>

<span data-ttu-id="b3bb4-176">Gilt für: Klassen, Eigenschaften, Methoden, Zuordnungen, Hinweise, Verweise</span><span class="sxs-lookup"><span data-stu-id="b3bb4-176">Applies to: classes, properties, methods, associations, indications, references</span></span>

<span data-ttu-id="b3bb4-177">Umstände, unter denen ein-Fehler ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-177">Circumstances under which a trigger is fired.</span></span> <span data-ttu-id="b3bb4-178">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-178">The default is **NULL**.</span></span> <span data-ttu-id="b3bb4-179">Die Auslösertypen variieren je nach metamodellkonstrukt.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-179">The trigger types vary by meta-model construct.</span></span>

<span data-ttu-id="b3bb4-180">Für Klassen und Zuordnungen lauten die folgenden zulässigen Werte:</span><span class="sxs-lookup"><span data-stu-id="b3bb4-180">For classes and associations, the legal values are:</span></span>

<span data-ttu-id="b3bb4-181">Erstellen</span><span class="sxs-lookup"><span data-stu-id="b3bb4-181">Create</span></span>

<span data-ttu-id="b3bb4-182">Löschen</span><span class="sxs-lookup"><span data-stu-id="b3bb4-182">Delete</span></span>

<span data-ttu-id="b3bb4-183">Aktualisieren</span><span class="sxs-lookup"><span data-stu-id="b3bb4-183">Update</span></span>

<span data-ttu-id="b3bb4-184">Access</span><span class="sxs-lookup"><span data-stu-id="b3bb4-184">Access</span></span>

<span data-ttu-id="b3bb4-185">Für Eigenschaften und Verweise lauten die zulässigen Werte: Update und Access.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-185">For properties and references, the legal values are: Update and Access.</span></span>

<span data-ttu-id="b3bb4-186">Bei-Methoden sind die zulässigen Werte vor und nach.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-186">For methods, the legal values are Before and After.</span></span>

<span data-ttu-id="b3bb4-187">Für Hinweise wird der zulässige Wert ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-187">For indications, the legal value is Thrown.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**Unknownvalues**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-188"><span id="UnknownValues"></span><span id="unknownvalues"></span><span id="UNKNOWNVALUES"></span>**UnknownValues**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-189">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-189">Data type: **string array**</span></span>

<span data-ttu-id="b3bb4-190">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3bb4-190">Applies to: properties</span></span>

<span data-ttu-id="b3bb4-191">Ein Satz von Werten, der angibt, dass der Wert der zugeordneten Eigenschaft unbekannt ist (die Eigenschaft kann nicht als gültiger oder sinnvoller Wert angesehen werden).</span><span class="sxs-lookup"><span data-stu-id="b3bb4-191">Set of values indicating that the value of the associated property is unknown (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="b3bb4-192">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-192">The default is **NULL**.</span></span>

<span data-ttu-id="b3bb4-193">Die Konventionen und Einschränkungen, die zum Definieren unbekannter Werte verwendet werden, entsprechen den Konventionen für den [**ValueMap**](standard-qualifiers.md) -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-193">The conventions and restrictions used for defining unknown values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="b3bb4-194">Beachten Sie, dass dieser Qualifizierer nicht überschrieben werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-194">Note that this qualifier cannot be overridden.</span></span> <span data-ttu-id="b3bb4-195">Es ist nicht sinnvoll, einer Unterklasse das Behandeln eines Werts als bekannten Wert zu gestatten, wenn er von einer übergeordneten Klasse als unbekannt behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-195">It is unreasonable to permit a subclass to treat a value as a known value when it is treated as unknown by some parent class.</span></span>

</dd> <dt>

<span data-ttu-id="b3bb4-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**Unsupportedvalues**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-196"><span id="UnsupportedValues"></span><span id="unsupportedvalues"></span><span id="UNSUPPORTEDVALUES"></span>**UnsupportedValues**</span></span>
</dt> <dd>

<span data-ttu-id="b3bb4-197">Datentyp: **Zeichen folgen Array**</span><span class="sxs-lookup"><span data-stu-id="b3bb4-197">Data type: **string array**</span></span>

<span data-ttu-id="b3bb4-198">Gilt für: Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="b3bb4-198">Applies to: properties</span></span>

<span data-ttu-id="b3bb4-199">Ein Satz von Werten, der angibt, dass der Wert der zugeordneten Eigenschaft nicht unterstützt wird (die Eigenschaft kann nicht als gültiger oder sinnvoller Wert angesehen werden).</span><span class="sxs-lookup"><span data-stu-id="b3bb4-199">Set of values indicating that the value of the associated property is unsupported (the property cannot be considered as having a valid or meaningful value).</span></span> <span data-ttu-id="b3bb4-200">Der Standardwert ist **null**.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-200">The default is **NULL**.</span></span>

<span data-ttu-id="b3bb4-201">Die Konventionen und Einschränkungen, die für die Definition nicht unterstützter Werte verwendet werden, entsprechen den Konventionen für den [**ValueMap**](standard-qualifiers.md) -Qualifizierer.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-201">The conventions and restrictions used for defining unsupported values are the same as those applicable to the [**ValueMap**](standard-qualifiers.md) qualifier.</span></span>

<span data-ttu-id="b3bb4-202">Hinweis Dieser Qualifizierer kann nicht überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-202">Note this qualifier cannot be overridden.</span></span> <span data-ttu-id="b3bb4-203">Es ist nicht sinnvoll, einer Unterklasse das Behandeln eines Werts als unterstützten Wert zu gestatten, der von einer übergeordneten Klasse als unbekannt behandelt wird.</span><span class="sxs-lookup"><span data-stu-id="b3bb4-203">It is unreasonable to permit a subclass to treat a value as a supported value that is treated as unknown by some parent class.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b3bb4-204">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b3bb4-204">Requirements</span></span>



| <span data-ttu-id="b3bb4-205">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b3bb4-205">Requirement</span></span> | <span data-ttu-id="b3bb4-206">Wert</span><span class="sxs-lookup"><span data-stu-id="b3bb4-206">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="b3bb4-207">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b3bb4-207">Minimum supported client</span></span><br/> | <span data-ttu-id="b3bb4-208">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b3bb4-208">Windows Vista</span></span><br/>       |
| <span data-ttu-id="b3bb4-209">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b3bb4-209">Minimum supported server</span></span><br/> | <span data-ttu-id="b3bb4-210">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b3bb4-210">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="b3bb4-211">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3bb4-211">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3bb4-212">WMI Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="b3bb4-212">WMI Qualifiers</span></span>](wmi-qualifiers.md)
</dt> <dt>

[<span data-ttu-id="b3bb4-213">Fügen eines Qualifizierers</span><span class="sxs-lookup"><span data-stu-id="b3bb4-213">Adding a Qualifier</span></span>](adding-a-qualifier.md)
</dt> </dl>

 

 




