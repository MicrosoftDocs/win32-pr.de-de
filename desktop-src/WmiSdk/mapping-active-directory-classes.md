---
description: Stellt Regeln zum Mapping von WMI-Klassen Active Directory bereit.
ms.assetid: 295d3233-5729-4eb0-9fa3-1cf64fef2909
ms.tgt_platform: multiple
title: Zuordnung von Active Directory Klassen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a606cfacc2e9d56ef07973df182f5ce1a65be35
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106358584"
---
# <a name="mapping-active-directory-classes"></a><span data-ttu-id="d6e07-103">Zuordnung von Active Directory Klassen</span><span class="sxs-lookup"><span data-stu-id="d6e07-103">Mapping Active Directory Classes</span></span>

<span data-ttu-id="d6e07-104">Da Active Directory über eine Vielzahl möglicher Objekte verfügt, kann WMI keine direkte eins-zu-Eins-Zuordnung erstellen.</span><span class="sxs-lookup"><span data-stu-id="d6e07-104">Because Active Directory has a wide variety of possible objects, WMI cannot create a direct one-to-one mapping.</span></span> <span data-ttu-id="d6e07-105">Stattdessen verwendet der Verzeichnisdienst Anbieter Regeln, um Klassen zwischen den beiden Technologien zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d6e07-105">Instead, the Directory Services provider uses rules to map classes between the two technologies.</span></span>

<span data-ttu-id="d6e07-106">Die folgenden Abschnitte werden in diesem Thema behandelt:</span><span class="sxs-lookup"><span data-stu-id="d6e07-106">This following sections are discussed in this topic:</span></span>

-   [<span data-ttu-id="d6e07-107">Mapping-Klassen</span><span class="sxs-lookup"><span data-stu-id="d6e07-107">Mapping Classes</span></span>](#mapping-classes)
-   [<span data-ttu-id="d6e07-108">Mapping-Attribute</span><span class="sxs-lookup"><span data-stu-id="d6e07-108">Mapping Attributes</span></span>](#mapping-attributes)
-   [<span data-ttu-id="d6e07-109">Zuordnungs Klassen</span><span class="sxs-lookup"><span data-stu-id="d6e07-109">Association Classes</span></span>](#association-classes)

> [!Note]  
> <span data-ttu-id="d6e07-110">Weitere Informationen zur Unterstützung und Installation dieser Komponente auf einem bestimmten Betriebssystem finden Sie unter [Betriebssystem Verfügbarkeit von WMI-Komponenten](operating-system-availability-of-wmi-components.md).</span><span class="sxs-lookup"><span data-stu-id="d6e07-110">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

## <a name="mapping-classes"></a><span data-ttu-id="d6e07-111">Mapping-Klassen</span><span class="sxs-lookup"><span data-stu-id="d6e07-111">Mapping Classes</span></span>

<span data-ttu-id="d6e07-112">In der folgenden Liste werden die Richtlinien beschrieben, die der Verzeichnisdienst Anbieter zum Zuordnen von Active Directory Klassen zu WMI-Klassen verwendet:</span><span class="sxs-lookup"><span data-stu-id="d6e07-112">The following list describes the guidelines that the Directory Services provider uses to map Active Directory classes to WMI classes:</span></span>

-   <span data-ttu-id="d6e07-113">Jede abstrakte Klasse im Active Directory Schema wird einer abstrakten Klasse im WMI-Schema zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-113">Each abstract class in the Active Directory schema maps to one abstract class in the WMI schema.</span></span>

    <span data-ttu-id="d6e07-114">Im WMI-Schema wird jeder abstrakten Klasse das Präfix DS vorangestellt \_ .</span><span class="sxs-lookup"><span data-stu-id="d6e07-114">In the WMI schema, each abstract class is prefixed with DS\_.</span></span> <span data-ttu-id="d6e07-115">Beispielsweise wird die **Person** -Klasse aus dem Active Directory-Schema der **DS- \_ Person** -WMI-Klasse zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-115">For example, the **person** class from the Active Directory schema maps to the **DS\_person** WMI class.</span></span>

-   <span data-ttu-id="d6e07-116">Jede nicht abstrakte Klasse aus dem Active Directory-Schema wird den folgenden zwei Klassen im WMI-Schema zugeordnet:</span><span class="sxs-lookup"><span data-stu-id="d6e07-116">Each nonabstract class from the Active Directory schema maps to the following two classes in the WMI schema:</span></span>

    -   <span data-ttu-id="d6e07-117">Der ersten zugeordneten Klasse wird das Präfix ADS vorangestellt \_ .</span><span class="sxs-lookup"><span data-stu-id="d6e07-117">The first mapped class is prefixed with ADS\_.</span></span> <span data-ttu-id="d6e07-118">Dabei handelt es sich um abstrakte Klassen, die gemäß den folgenden Regeln zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="d6e07-118">These are abstract classes, mapped according to the rules below.</span></span>
    -   <span data-ttu-id="d6e07-119">Die zweite zugeordnete Klasse ist eine nicht abstrakte Klasse mit dem DS- \_ namens Präfix.</span><span class="sxs-lookup"><span data-stu-id="d6e07-119">The second mapped class is a nonabstract class with the DS\_ name prefix.</span></span> <span data-ttu-id="d6e07-120">Diese Klasse wird von der ADS \_ abstract-Klasse abgeleitet, wobei der [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="d6e07-120">This class is derived from the ADS\_ abstract class, with the addition of the [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

    <span data-ttu-id="d6e07-121">Beispielsweise wird die **Benutzer** Klasse aus dem Active Directory-Schema zwei Klassen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-121">For example, the **user** class from the Active Directory schema maps to two classes.</span></span> <span data-ttu-id="d6e07-122">Die erste Klasse ist die **\_ Benutzer** abstrakte Klasse ADS, die gemäß den Regeln unten zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d6e07-122">The first class is the **ADS\_user** abstract class, mapped according to rules below.</span></span> <span data-ttu-id="d6e07-123">Die zweite Klasse ist die nicht abstrakte Klasse " **DS- \_ Benutzer** ".</span><span class="sxs-lookup"><span data-stu-id="d6e07-123">The second class is the **DS\_user** nonabstract class.</span></span> <span data-ttu-id="d6e07-124">Sie wird von **ADS \_ User** abgeleitet und verfügt über den hinzugefügten [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) .</span><span class="sxs-lookup"><span data-stu-id="d6e07-124">It is derived from **ADS\_user** and has the added [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier.</span></span>

-   <span data-ttu-id="d6e07-125">Sofern nicht anders angegeben, ist der Name einer zugeordneten Klasse der gehat Wert der **LDAP-Display-Name-** Eigenschaft in der Active Directory-Klasse.</span><span class="sxs-lookup"><span data-stu-id="d6e07-125">Unless specified otherwise, the name of a mapped class is the mangled value of the **LDAP-Display-Name** property in the Active Directory class.</span></span>
-   <span data-ttu-id="d6e07-126">Wenn die **Unterklasse-of-** Eigenschaft in der Active Directory-Klasse vorhanden ist, wird die WMI-zugeordnete Klasse von der angegebenen Klasse abgeleitet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-126">If the **Sub-Class-Of** property is present on the Active Directory class, the WMI-mapped class is derived from the specified class.</span></span>

    <span data-ttu-id="d6e07-127">Wenn die **Unterklasse-of-** Eigenschaft nicht vorhanden ist, wird die WMI-zugeordnete Klasse von der **DS \_ LDAP \_ \_** -Stamm klassenklasse abgeleitet, wie in der MOF-Datei angegeben.</span><span class="sxs-lookup"><span data-stu-id="d6e07-127">If the **Sub-Class-Of** property is not present, the WMI-mapped class is derived from the **DS\_LDAP\_Root\_Class** class, as specified in the MOF file.</span></span>

    > [!Note]  
    > <span data-ttu-id="d6e07-128">Diese Klasse verfügt über die **adsipath** -Schlüsseleigenschaft mit dem Typ **VT \_ BSTR**.</span><span class="sxs-lookup"><span data-stu-id="d6e07-128">This class has the **ADSIPath** key property, with a type **VT\_BSTR**.</span></span> <span data-ttu-id="d6e07-129">Dies ist der eindeutige ADSI-Pfad, der diese Instanz identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d6e07-129">This is the unique ADSI path that identifies this instance.</span></span> <span data-ttu-id="d6e07-130">Active Directory unterstützt nur die einfache Vererbung, sodass dies funktioniert.</span><span class="sxs-lookup"><span data-stu-id="d6e07-130">Active Directory supports single-inheritance only, so this works.</span></span>

     

-   <span data-ttu-id="d6e07-131">Für jede Klasse wird ein **dynamischer** Qualifizierer vom Typ **VT \_ bool** und `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` für jede Klasse der Wert auf **true** festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d6e07-131">A **Dynamic** qualifier of type **VT\_BOOL**, and flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to **TRUE** is created for every class.</span></span> <span data-ttu-id="d6e07-132">Dies ist ein standardmäßiger WMI-Qualifizierer, der angibt, dass Instanzen dieser Klasse dynamisch bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d6e07-132">This is a standard WMI qualifier that indicates that instances of this class are provided dynamically.</span></span>
-   <span data-ttu-id="d6e07-133">Wenn die Klasse nicht abstrakt ist, erstellt der Anbieter einen [**Anbieter Qualifizierer**](/windows/desktop/api/Provider/nl-provider-provider) vom Typ **VT \_ BSTR bool** und die qualifiziererkonfiguration `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` , die für jede Klasse auf "DS-Instanzanbieter" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d6e07-133">If the class is not abstract, the provider creates a [**Provider**](/windows/desktop/api/Provider/nl-provider-provider) qualifier of type **VT\_BSTR BOOL** and qualifier flavor `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` set to "DS Instance Provider" for every class.</span></span> <span data-ttu-id="d6e07-134">Dies ist ein standardmäßiger WMI-Qualifizierer, der den Namen des Anbieters angibt, der Instanzen dieser Klasse dynamisch bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="d6e07-134">This is a standard WMI qualifier that indicates the name of the provider dynamically providing instances of this class.</span></span>

<span data-ttu-id="d6e07-135">Die restlichen ADSI-Eigenschaften werden den Klassen Qualifizierern und Eigenschaften gemäß den folgenden Tabellen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-135">The rest of the ADSI properties map to class qualifiers and properties as per the following tables.</span></span> <span data-ttu-id="d6e07-136">Alle Qualifizierer werden mit einem qualifiziererflagwert von zugeordnet `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` .</span><span class="sxs-lookup"><span data-stu-id="d6e07-136">All qualifiers map with a qualifier flag value of `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS`.</span></span>

<span data-ttu-id="d6e07-137">Im folgenden werden die Mapping-Informationen für die Active Directory-Klasse aufgelistet, die den WMI-Qualifizierer und den WMI-qualifizierungstyp für jede Active Directory</span><span class="sxs-lookup"><span data-stu-id="d6e07-137">The following lists mapping information for the Active Directory class, showing the WMI qualifier and WMI qualifier type for each Active Directory property.</span></span>

<dl> <dt>

<span data-ttu-id="d6e07-138">**Gemeinsamer Name**</span><span class="sxs-lookup"><span data-stu-id="d6e07-138">**Common-Name**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-139">**CN** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="d6e07-139">**CN** (**VT\_BSTR**)</span></span>

<span data-ttu-id="d6e07-140">Wird direkt aus dem Zeichen folgen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-140">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="d6e07-141">**Default-Object-Category**</span><span class="sxs-lookup"><span data-stu-id="d6e07-141">**Default-Object-Category**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-142">**Defaultobjectcategory** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="d6e07-142">**DefaultObjectCategory** (**VT\_BSTR**)</span></span>

<span data-ttu-id="d6e07-143">Wird direkt aus dem Zeichen folgen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-143">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="d6e07-144">**Standard-Security-Descriptor**</span><span class="sxs-lookup"><span data-stu-id="d6e07-144">**Default-Security-Descriptor**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-145">**DefaultSecurityDescriptor** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="d6e07-145">**DefaultSecurityDescriptor** (**VT\_BSTR**)</span></span>

<span data-ttu-id="d6e07-146">Wird direkt aus dem Zeichen folgen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-146">Mapped directly from the string value.</span></span>

</dd> <dt>

<span data-ttu-id="d6e07-147">**Regelt-ID**</span><span class="sxs-lookup"><span data-stu-id="d6e07-147">**Governs-Id**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-148">**GovernsId** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="d6e07-148">**GovernsId** (**VT\_BSTR**)</span></span>

<span data-ttu-id="d6e07-149">Wird von der Zeichen folgen Darstellung der OID zugeordnet. Beispiel: "{1 3 3 6}".</span><span class="sxs-lookup"><span data-stu-id="d6e07-149">Mapped from the string representation of the OID; for example, "{ 1 3 3 6 }".</span></span>

</dd> <dt>

<span data-ttu-id="d6e07-150">**Object-Klasse**</span><span class="sxs-lookup"><span data-stu-id="d6e07-150">**Object-Class**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-151">–</span><span class="sxs-lookup"><span data-stu-id="d6e07-151">N/A</span></span>

<span data-ttu-id="d6e07-152">Nicht zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-152">Not mapped.</span></span>

</dd> <dt>

<span data-ttu-id="d6e07-153">**Object-Class-Category**</span><span class="sxs-lookup"><span data-stu-id="d6e07-153">**Object-Class-Category**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-154">**ObjectClassCategory** (**VT \_ I4**)</span><span class="sxs-lookup"><span data-stu-id="d6e07-154">**ObjectClassCategory** (**VT\_I4**)</span></span>

<span data-ttu-id="d6e07-155">Wird direkt aus dem ganzzahligen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-155">Mapped directly from the integer value.</span></span> <span data-ttu-id="d6e07-156">Wenn der Wert abstrakt (2) ist, wird außerdem der standardmäßige **VT \_ bool** CIM-Qualifizierer, der als **"abstract"** -Qualifizierer bezeichnet wird, ebenfalls erstellt.</span><span class="sxs-lookup"><span data-stu-id="d6e07-156">In addition, if the value is Abstract(2), then the standard **VT\_BOOL** CIM qualifier, called the **"Abstract"** qualifier, is also created.</span></span>

</dd> <dt>

<span data-ttu-id="d6e07-157">**RDN-ATT-ID**</span><span class="sxs-lookup"><span data-stu-id="d6e07-157">**RDN-ATT-ID**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-158">**rDNAttID** (**VT \_ BSTR**)</span><span class="sxs-lookup"><span data-stu-id="d6e07-158">**RDNATTID** (**VT\_BSTR**)</span></span>

<span data-ttu-id="d6e07-159">Wird von der Zeichen folgen Darstellung des OID-Werts zugeordnet. Beispiel: "{1 3 3 6}".</span><span class="sxs-lookup"><span data-stu-id="d6e07-159">Mapped from the string representation of the OID value; for example, "{ 1 3 3 6 }".</span></span> <span data-ttu-id="d6e07-160">Außerdem wird die hier identifizierte Eigenschaft mit dem standardmäßigen **indizierten** CIM-Qualifizierer kommentiert, der auf **true** festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="d6e07-160">In addition, the property identified here is annotated with the standard **Indexed** CIM qualifier set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d6e07-161">**Nur System**</span><span class="sxs-lookup"><span data-stu-id="d6e07-161">**System-Only**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-162">**Systemonly** (**VT \_ bool**)</span><span class="sxs-lookup"><span data-stu-id="d6e07-162">**SystemOnly** (**VT\_BOOL**)</span></span>

<span data-ttu-id="d6e07-163">Wird direkt aus dem booleschen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-163">Mapped directly from the Boolean value.</span></span>

</dd> </dl>

 

<span data-ttu-id="d6e07-164">Im folgenden werden die Eigenschaften der Active Directory-Klasse aufgelistet, die WMI-Klasseneigenschaften zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d6e07-164">The following lists the Active Directory class properties mapped to WMI class properties.</span></span>

<dl> <dt>

<span data-ttu-id="d6e07-165">**Kann enthalten**</span><span class="sxs-lookup"><span data-stu-id="d6e07-165">**May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-166">Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-166">Each property in this list is mapped to a WMI property.</span></span>

</dd> <dt>

<span data-ttu-id="d6e07-167">**Muss enthalten**</span><span class="sxs-lookup"><span data-stu-id="d6e07-167">**Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-168">Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-168">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="d6e07-169">Der standardmäßige **Not \_ null** -CIM-Qualifizierer wird für jeden dieser Werte erstellt.</span><span class="sxs-lookup"><span data-stu-id="d6e07-169">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span>

</dd> <dt>

<span data-ttu-id="d6e07-170">**System-kann enthalten**</span><span class="sxs-lookup"><span data-stu-id="d6e07-170">**System-May-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-171">Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-171">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="d6e07-172">Außerdem wird jede Eigenschaft mit einem **System** Qualifizierer versehen und auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d6e07-172">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> <dt>

<span data-ttu-id="d6e07-173">**System-muss enthalten**</span><span class="sxs-lookup"><span data-stu-id="d6e07-173">**System-Must-Contain**</span></span>
</dt> <dd>

<span data-ttu-id="d6e07-174">Jede Eigenschaft in dieser Liste wird einer WMI-Eigenschaft zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-174">Each property in this list is mapped to a WMI property.</span></span> <span data-ttu-id="d6e07-175">Der standardmäßige **Not \_ null** -CIM-Qualifizierer wird für jeden dieser Werte erstellt.</span><span class="sxs-lookup"><span data-stu-id="d6e07-175">The standard **Not\_Null** CIM qualifier is created for each of these.</span></span> <span data-ttu-id="d6e07-176">Außerdem wird jede Eigenschaft mit einem **System** Qualifizierer versehen und auf " **true**" festgelegt.</span><span class="sxs-lookup"><span data-stu-id="d6e07-176">In addition, each property is annotated with a **System** qualifier, set to **TRUE**.</span></span>

</dd> </dl>

## <a name="mapping-attributes"></a><span data-ttu-id="d6e07-177">Mapping-Attribute</span><span class="sxs-lookup"><span data-stu-id="d6e07-177">Mapping Attributes</span></span>

<span data-ttu-id="d6e07-178">Der Verzeichnisdienst Anbieter ordnet jedes Attribut einer Active Directory-Klasse gemäß den Regeln in diesem Abschnitt genau einer Eigenschaft der entsprechenden WMI-Klasse zu.</span><span class="sxs-lookup"><span data-stu-id="d6e07-178">The Directory Services provider maps each attribute of an Active Directory class to exactly one property of the corresponding WMI class according to the rules in this section.</span></span> <span data-ttu-id="d6e07-179">Im allgemeinen benennt der Verzeichnis Dienstanbieter die WMI-Eigenschaft als die geschützte Version des **LDAP-Display-Name-** Werts des Active Directory Attributs.</span><span class="sxs-lookup"><span data-stu-id="d6e07-179">In general, the Directory Services Provider names the WMI property as the mangled version of the **LDAP-Display-Name** value of the Active Directory attribute.</span></span>

<span data-ttu-id="d6e07-180">Wenn die Active Directory **-** Eigenschaft den Wert " **false**" hat, wird diese WMI-Eigenschaft mit dem or-Operator mit dem CIM- **Flag- \_ \_ Array** kombiniert.</span><span class="sxs-lookup"><span data-stu-id="d6e07-180">If the Active Directory property **Is-Single-Valued** is **FALSE**, then this WMI property is combined with the OR operator with **CIM\_FLAG\_ARRAY**.</span></span> <span data-ttu-id="d6e07-181">Beachten Sie, dass jede Eigenschaft mit dem **VT \_ BSTR** -Qualifizierer " **adsyntax**" gekennzeichnet ist.</span><span class="sxs-lookup"><span data-stu-id="d6e07-181">Note that each property is tagged with the **VT\_BSTR** qualifier, **ADSyntax**.</span></span> <span data-ttu-id="d6e07-182">Sie stellt die zugrunde liegende Active Directory-Syntax dar.</span><span class="sxs-lookup"><span data-stu-id="d6e07-182">It represents the underlying Active Directory syntax.</span></span>

<span data-ttu-id="d6e07-183">In der folgenden Tabelle wird die Zuordnung der Active Directory-Syntax zum WMI-Eigenschafts Datentyp aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-183">The following table lists the mapping of the Active Directory syntax to the WMI property data type.</span></span>



| <span data-ttu-id="d6e07-184">Active Directory-Element</span><span class="sxs-lookup"><span data-stu-id="d6e07-184">Active Directory element</span></span>                                      | <span data-ttu-id="d6e07-185">WMI-Datentyp</span><span class="sxs-lookup"><span data-stu-id="d6e07-185">WMI data type</span></span>                                                           |
|---------------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="d6e07-186">**Zugriffspunkt**</span><span class="sxs-lookup"><span data-stu-id="d6e07-186">**Access-Point**</span></span>](/windows/desktop/ADSchema/s-object-access-point)            | <span data-ttu-id="d6e07-187">**CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-187">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="d6e07-188">**Booleschen**</span><span class="sxs-lookup"><span data-stu-id="d6e07-188">**Boolean**</span></span>](/windows/desktop/ADSchema/s-boolean)                             | <span data-ttu-id="d6e07-189">**CIM- \_ boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="d6e07-189">**CIM\_BOOLEAN**</span></span>                                                        |
| <span data-ttu-id="d6e07-190">**Groß-/Kleinschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6e07-190">**Case Insensitive String**</span></span>                                   | <span data-ttu-id="d6e07-191">**CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-191">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="d6e07-192">**Groß-/Kleinschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6e07-192">**Case Sensitive String**</span></span>](/windows/desktop/ADSchema/s-string-case-sensitive) | <span data-ttu-id="d6e07-193">**CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-193">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="d6e07-194">**Definierter Name**</span><span class="sxs-lookup"><span data-stu-id="d6e07-194">**Distinguished Name**</span></span>](/windows/desktop/ADSchema/s-object-ds-dn)             | <span data-ttu-id="d6e07-195">**CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-195">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="d6e07-196">**DN-Binär**</span><span class="sxs-lookup"><span data-stu-id="d6e07-196">**DN-Binary**</span></span>](/windows/desktop/ADSchema/s-object-dn-binary)                  | <span data-ttu-id="d6e07-197">Eingebettetes Objekt der Klasse **DN \_ mit \_ binärer Binärdatei** .</span><span class="sxs-lookup"><span data-stu-id="d6e07-197">Embedded object of class **DN\_With\_Binary** defined below.</span></span><br/> |
| [<span data-ttu-id="d6e07-198">**DN-Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-198">**DN-String**</span></span>](/windows/desktop/ADSchema/s-object-dn-string)                  | <span data-ttu-id="d6e07-199">Eingebettetes Objekt der Klasse **DN \_ mit \_ Zeichenfolge** , die unten definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d6e07-199">Embedded object of class **DN\_With\_String** defined below.</span></span><br/> |
| [<span data-ttu-id="d6e07-200">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d6e07-200">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="d6e07-201">**CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="d6e07-201">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="d6e07-202">**Enumeration**</span><span class="sxs-lookup"><span data-stu-id="d6e07-202">**Enumeration**</span></span>](/windows/desktop/ADSchema/s-enumeration)                     | <span data-ttu-id="d6e07-203">**CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-203">**CIM\_STRING**</span></span>                                                         |
| [<span data-ttu-id="d6e07-204">**Zah**</span><span class="sxs-lookup"><span data-stu-id="d6e07-204">**Integer**</span></span>](/windows/desktop/ADSchema/s-integer)                             | <span data-ttu-id="d6e07-205">**CIM \_ SINT32**</span><span class="sxs-lookup"><span data-stu-id="d6e07-205">**CIM\_SINT32**</span></span>                                                         |
| [<span data-ttu-id="d6e07-206">**LargeInteger**</span><span class="sxs-lookup"><span data-stu-id="d6e07-206">**LargeInteger**</span></span>](/windows/desktop/ADSchema/s-largeinteger)                   | <span data-ttu-id="d6e07-207">**CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-207">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="d6e07-208">Sicherheitsbeschreibung</span><span class="sxs-lookup"><span data-stu-id="d6e07-208">Security Descriptor</span></span>                                           | <span data-ttu-id="d6e07-209">Eingebettetes Objekt der Klasse **Uint8Array** unten definiert.</span><span class="sxs-lookup"><span data-stu-id="d6e07-209">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="d6e07-210">Numerische Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d6e07-210">Numeric String</span></span>                                                | <span data-ttu-id="d6e07-211">**CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-211">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="d6e07-212">ObjectID</span><span class="sxs-lookup"><span data-stu-id="d6e07-212">Object ID</span></span>                                                     | <span data-ttu-id="d6e07-213">**CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-213">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="d6e07-214">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d6e07-214">Octet String</span></span>                                                  | <span data-ttu-id="d6e07-215">Eingebettetes Objekt der Klasse **Uint8Array** unten definiert.</span><span class="sxs-lookup"><span data-stu-id="d6e07-215">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="d6e07-216">Oder Name</span><span class="sxs-lookup"><span data-stu-id="d6e07-216">OR Name</span></span>                                                       | <span data-ttu-id="d6e07-217">**CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-217">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="d6e07-218">Presentation-Address</span><span class="sxs-lookup"><span data-stu-id="d6e07-218">Presentation-Address</span></span>                                          | <span data-ttu-id="d6e07-219">Eingebettetes Objekt der Klasse **Uint8Array** unten definiert.</span><span class="sxs-lookup"><span data-stu-id="d6e07-219">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="d6e07-220">Print Case-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d6e07-220">Print Case String</span></span>                                             | <span data-ttu-id="d6e07-221">**CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-221">**CIM\_STRING**</span></span>                                                         |
| <span data-ttu-id="d6e07-222">Replikat Link</span><span class="sxs-lookup"><span data-stu-id="d6e07-222">Replica Link</span></span>                                                  | <span data-ttu-id="d6e07-223">Eingebettetes Objekt der Klasse **Uint8Array** unten definiert.</span><span class="sxs-lookup"><span data-stu-id="d6e07-223">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| [<span data-ttu-id="d6e07-224">**Zeichenfolge (SID)**</span><span class="sxs-lookup"><span data-stu-id="d6e07-224">**String(Sid)**</span></span>](/windows/desktop/ADSchema/s-string-sid)                      | <span data-ttu-id="d6e07-225">Eingebettetes Objekt der Klasse **Uint8Array** unten definiert.</span><span class="sxs-lookup"><span data-stu-id="d6e07-225">Embedded object of class **Uint8Array** defined below.</span></span><br/>       |
| <span data-ttu-id="d6e07-226">Time</span><span class="sxs-lookup"><span data-stu-id="d6e07-226">Time</span></span>                                                          | <span data-ttu-id="d6e07-227">**CIM- \_ DateTime**</span><span class="sxs-lookup"><span data-stu-id="d6e07-227">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="d6e07-228">UTC-codierte Zeit</span><span class="sxs-lookup"><span data-stu-id="d6e07-228">UTC Coded Time</span></span>                                                | <span data-ttu-id="d6e07-229">**CIM- \_ DateTime**</span><span class="sxs-lookup"><span data-stu-id="d6e07-229">**CIM\_DATETIME**</span></span>                                                       |
| <span data-ttu-id="d6e07-230">Unicode-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d6e07-230">Unicode String</span></span>                                                | <span data-ttu-id="d6e07-231">**CIM- \_ Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="d6e07-231">**CIM\_STRING**</span></span>                                                         |



 

<span data-ttu-id="d6e07-232">Die Oktett-Zeichen folgen Syntax, die auf ein Array von **Uint8** -Werten verweist, stellt bei der Zuordnung zu WMI ein Problem dar, da WMI Eigenschaften von Typen **Uint8** und Arrays von **Uint8** zulässt, während Active Directory Eigenschaften vom Typ Oktett String sowie Arrays von Oktett-Zeichen folgen zulässt.</span><span class="sxs-lookup"><span data-stu-id="d6e07-232">The Octet String syntax, which refers to an array of **uint8** values, presents a problem when mapped to WMI because WMI allows properties of types **uint8** and arrays of **uint8**, whereas Active Directory allows properties of type Octet String as well as arrays of Octet String.</span></span>

<span data-ttu-id="d6e07-233">Das folgende Beispiel zeigt die Verzeichnisdienst Anbieter-Klasse, die verwendet wird, um ein Array von Eigenschaften des Oktett-Zeichen folgen Typs zuzuordnen.</span><span class="sxs-lookup"><span data-stu-id="d6e07-233">The following example shows the Directory Services Provider class that is used to map an array of Octet String type properties.</span></span>

``` syntax
Class Uint8Array 
{
    uint8 values[];
    uint32 numberOfValues;
};
```

<span data-ttu-id="d6e07-234">WMI ordnet alle Oktett-Zeichen folgen Active Directory-Eigenschafts Werten eingebetteten Instanzen von **Uint8Array** zu.</span><span class="sxs-lookup"><span data-stu-id="d6e07-234">WMI maps all Octet String Active Directory property values to embedded instances of **Uint8Array**.</span></span> <span data-ttu-id="d6e07-235">Ebenso ordnet WMI Arrays von Oktett-Zeichen folgen Arrays von eingebetteten **Uint8Array** -Objekten zu.</span><span class="sxs-lookup"><span data-stu-id="d6e07-235">Similarly, WMI maps arrays of Octet String to arrays of embedded **Uint8Array** objects.</span></span>

<span data-ttu-id="d6e07-236">Das folgende Beispiel zeigt die Klassen, die von WMI zugeordnet werden, um die Eigenschaften Werte DN-Binary und DN-String DS zu.</span><span class="sxs-lookup"><span data-stu-id="d6e07-236">The following example shows the classes that are mapped by WMI to DN-Binary and DN-String DS property values.</span></span>

``` syntax
Class DN_With_String
{
    string dnString;
    string value;
};

Class DN_With_Binary
{
    string dnString;
    uint8 value[];
};
```

<span data-ttu-id="d6e07-237">In der folgenden Tabelle ist aufgelistet, wie WMI die restlichen Eigenschaften der Active Directory-Attribut Schnittstelle den WMI-Eigenschafts Qualifizierern zuordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-237">The following table lists how WMI maps the rest of the Active Directory attribute interface properties to WMI property qualifiers.</span></span>



| <span data-ttu-id="d6e07-238">Active Directory Attribut-Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="d6e07-238">Active Directory attribute-property name</span></span> | <span data-ttu-id="d6e07-239">WMI Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="d6e07-239">WMI Qualifier</span></span>       | <span data-ttu-id="d6e07-240">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d6e07-240">Data type</span></span>    | <span data-ttu-id="d6e07-241">Mapping-Informationen</span><span class="sxs-lookup"><span data-stu-id="d6e07-241">Mapping information</span></span>                               |
|------------------------------------------|---------------------|--------------|---------------------------------------------------|
| <span data-ttu-id="d6e07-242">**Attribut Syntax**</span><span class="sxs-lookup"><span data-stu-id="d6e07-242">**Attribute-Syntax**</span></span>                     | <span data-ttu-id="d6e07-243">**AttributeSyntax**</span><span class="sxs-lookup"><span data-stu-id="d6e07-243">**AttributeSyntax**</span></span> | <span data-ttu-id="d6e07-244">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="d6e07-244">**VT\_BSTR**</span></span> | <span data-ttu-id="d6e07-245">Wird von der Zeichen folgen Darstellung der OID zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-245">Mapped from the string representation of the OID.</span></span> |
| <span data-ttu-id="d6e07-246">**Gemeinsamer Name**</span><span class="sxs-lookup"><span data-stu-id="d6e07-246">**Common-Name**</span></span>                          | <span data-ttu-id="d6e07-247">**2.300**</span><span class="sxs-lookup"><span data-stu-id="d6e07-247">**CN**</span></span>              | <span data-ttu-id="d6e07-248">**VT \_ BSTR**</span><span class="sxs-lookup"><span data-stu-id="d6e07-248">**VT\_BSTR**</span></span> | <span data-ttu-id="d6e07-249">Wird vom Zeichen folgen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-249">Mapped from the string value.</span></span>                     |
| <span data-ttu-id="d6e07-250">**Nur System**</span><span class="sxs-lookup"><span data-stu-id="d6e07-250">**System-Only**</span></span>                          | <span data-ttu-id="d6e07-251">**System**</span><span class="sxs-lookup"><span data-stu-id="d6e07-251">**System**</span></span>          | <span data-ttu-id="d6e07-252">**VT \_ bool**</span><span class="sxs-lookup"><span data-stu-id="d6e07-252">**VT\_BOOL**</span></span> | <span data-ttu-id="d6e07-253">Wird vom booleschen Wert zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-253">Mapped from the Boolean value.</span></span>                    |



 

> [!Note]  
> <span data-ttu-id="d6e07-254">WMI ordnet alle Active Directory Qualifizierer den `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` qualifizierervarianten zu.</span><span class="sxs-lookup"><span data-stu-id="d6e07-254">WMI maps all Active Directory qualifiers with the `WBEM_FLAVOR_FLAG_PROPAGATE_TO_INSTANCE | WBEM_FLAVOR_FLAG_PROPAGATE_TO_DERIVED_CLASS` qualifier flavors.</span></span>

 

## <a name="association-classes"></a><span data-ttu-id="d6e07-255">Zuordnungs Klassen</span><span class="sxs-lookup"><span data-stu-id="d6e07-255">Association Classes</span></span>

<span data-ttu-id="d6e07-256">Der Verzeichnisdienst ist im Grunde ein hierarchischer Speicher von Objekten.</span><span class="sxs-lookup"><span data-stu-id="d6e07-256">The Directory Service is essentially a hierarchical store of objects.</span></span> <span data-ttu-id="d6e07-257">Die Objekte, die auf einer nicht Blatt Ebene in der Hierarchie vorkommen können, werden als "Container" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d6e07-257">Those objects that can appear at a nonleaf level in the hierarchy are called "containers".</span></span> <span data-ttu-id="d6e07-258">Die Struktur dieser Hierarchie wird weiter von den Eigenschaften "Poss-Vorgesetzten" und "System-Poss-Vorgesetzten" einer Klasse im Schema gesteuert.</span><span class="sxs-lookup"><span data-stu-id="d6e07-258">The structure of this hierarchy is further controlled by the "Poss-Superiors" and "System-Poss-Superiors" properties of a class in the schema.</span></span> <span data-ttu-id="d6e07-259">Diese geben die Klassen an, deren Instanzen in einer Instanz einer Container Klasse enthalten sein können.</span><span class="sxs-lookup"><span data-stu-id="d6e07-259">These, taken together, specify the set of classes whose instances can be contained within an instance of a container class.</span></span>

<span data-ttu-id="d6e07-260">Im folgenden Beispiel wird eine CIM-Zuordnung als Instanzen der statischen Association-Klasse [**DS \_ LDAP \_ Class \_ Containment**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment)modelliert.</span><span class="sxs-lookup"><span data-stu-id="d6e07-260">The following example models a CIM association as instances of the static association class [**DS\_LDAP\_Class\_Containment**](/previous-versions/windows/desktop/dsprov/ds-ldap-class-containment).</span></span>

``` syntax
//  DS Class Associations Provider 

// Create a class of which instances are
// provided by this provider

[
  Association : ToInstance,
  dynamic,
  HasClassRefs,
  Provider("Microsoft|DSLDAPClassAssociationProvider|V1.0")
]
class DS_LDAP_Class_Containment
{
    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass]
    object Ref ChildClass;

    [key, classref{"DS_LDAP_Root_Class"} : ToInstance ToSubClass] 
    object Ref ParentClass; // The parent DS Class
};


// Create an instance of the provider class for registration
instance of __Win32Provider as $AssociationsProvider
{
    Name = "Microsoft|DSLDAPClassAssociationProvider|V1.0";
    Clsid = "{33831ED4-42B8-11d2-93AD-00805F853771}";
    ImpersonationLevel = 1;
};    

// Specification of the instances and operation
// provided by the provider
instance of __InstanceProviderRegistration
{
    Provider = $AssociationsProvider;
    SupportsGet = TRUE;
    SupportsPut = FALSE;
    SupportsDelete = FALSE;
    SupportsEnumeration = TRUE;
};
```

<span data-ttu-id="d6e07-261">Der Association-Klassen Anbieter unterstützt die Methoden " [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) " und " [**feateclassenenumasync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) ".</span><span class="sxs-lookup"><span data-stu-id="d6e07-261">The association class provider supports the [**GetObjectAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-getobjectasync) and [**CreateClassEnumAsync**](/windows/desktop/api/WbemCli/nf-wbemcli-iwbemservices-createclassenumasync) methods.</span></span>

 

