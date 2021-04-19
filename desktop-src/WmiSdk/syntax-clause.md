---
description: Enthält eine Syntax Klausel, die die Daten und den Typ für das MIB-Objekt definiert.
ms.assetid: 24c483c8-db50-492f-9c2e-72620395331a
ms.tgt_platform: multiple
title: Syntax Klausel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02d0bf25156ddda4bf71a7f40a8de1fede2a82d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359571"
---
# <a name="syntax-clause"></a><span data-ttu-id="cb9bc-103">Syntax Klausel</span><span class="sxs-lookup"><span data-stu-id="cb9bc-103">SYNTAX Clause</span></span>

<span data-ttu-id="cb9bc-104">Das [Object-Type-](object-type-macro.md) Makro enthält eine Syntax Klausel, die die Daten und den Typ für das MIB-Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-104">The [OBJECT-TYPE](object-type-macro.md) macro contains a SYNTAX clause that defines the data and type for the MIB object.</span></span> <span data-ttu-id="cb9bc-105">Während der SNMP-Anbieter allgemeine Regeln für Mapping-Syntax Klauseln beachtet, befolgt der Anbieter auch Regeln, die für verschiedene Datentypen spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-105">While the SNMP Provider observes general rules for mapping SYNTAX clauses, the provider also follows rules specific to several data types.</span></span>

> [!Note]  
> <span data-ttu-id="cb9bc-106">Weitere Informationen zum Installieren des Anbieters finden Sie unter [Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="cb9bc-106">For more information about installing the provider, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

 

<span data-ttu-id="cb9bc-107">Die folgenden Zuordnungsregeln gelten für alle Datentypen, die in der folgenden Tabelle beschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="cb9bc-107">The following mapping rules apply to all of the data types described in the table below:</span></span>

-   <span data-ttu-id="cb9bc-108">Die Textdarstellung der Syntax Klausel wird der **Text \_ Konvention** für den CIM-Eigenschaften Qualifizierer zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-108">The textual representation of the SYNTAX clause maps to the CIM property qualifier **textual\_convention**.</span></span>
-   <span data-ttu-id="cb9bc-109">Die benannte Typdefinition in der Syntax Klausel ist der CIM-Eigenschaft **qualifiziererobjektsyntax \_** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-109">The named type definition in the SYNTAX clause maps to the CIM property qualifier **object\_syntax**.</span></span> <span data-ttu-id="cb9bc-110">Diese Zuordnung unterscheidet sich je nach Datentyp.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-110">This mapping differs depending on the data type.</span></span> <span data-ttu-id="cb9bc-111">Weitere Informationen finden Sie in den Mapping-Beschreibungen.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-111">For more information, see the mapping descriptions.</span></span>
-   <span data-ttu-id="cb9bc-112">Der beim Codieren von SNMPv1-und SNMPv2C-Protokoll Rahmen verwendete SNMP-Typ wird der CIM-Eigenschaft qualifizierercodierung zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-112">The SNMP type used when encoding SNMPv1 and SNMPv2C protocol frames maps to the CIM property qualifier **encoding**.</span></span>
-   <span data-ttu-id="cb9bc-113">Der CIM-Eigenschaften **Qualifizierer CimType** enthält die Textdarstellung, die den zugrunde liegenden CIM-Protokoll Wert formatiert.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-113">The CIM property qualifier **cimtype** contains the textual representation that formats the underlying CIM protocol value.</span></span>

<span data-ttu-id="cb9bc-114">In der folgenden Tabelle sind die Datentypen aufgelistet, die bestimmte Regeln aufweisen, die das Verhalten der Anbieter Zuordnung steuern.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-114">The following table lists data types that have specific rules that govern the provider mapping behavior.</span></span>



| <span data-ttu-id="cb9bc-115">SNMP-Datentyp</span><span class="sxs-lookup"><span data-stu-id="cb9bc-115">SNMP data type</span></span>                                     | <span data-ttu-id="cb9bc-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="cb9bc-116">Description</span></span>                                                                                                                                                                                                                                      |
|----------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cb9bc-117">Primitiver Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-117">Primitive type</span></span>](#primitive-type)                  | <span data-ttu-id="cb9bc-118">Einer der grundlegenden Datentypen, die in der Struktur von Verwaltungsinformationen (SMI) definiert sind, dokumentiert RFC 1213 und RFC 1903.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-118">One of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span>                                                                                                                            |
| [<span data-ttu-id="cb9bc-119">Text Konvention</span><span class="sxs-lookup"><span data-stu-id="cb9bc-119">Textual convention</span></span>](textual-convention-macro.md) | <span data-ttu-id="cb9bc-120">Typdefinition, die durch die explizite Verwendung des SNMPv2C **-Text Konvention-** Makros generiert oder durch die Verwendung eines benannten Typs generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-120">Type definition generated through the explicit use of the SNMPv2C **TEXTUAL-CONVENTION** macro or generated through the use of a named type.</span></span> <span data-ttu-id="cb9bc-121">Eine Text Konvention weist einem vorhandenen Datentyp einen Namen und in einigen Fällen einen Wertebereich zu.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-121">A textual convention assigns a name and, in some cases, a range of values to an existing data type.</span></span> |
| [<span data-ttu-id="cb9bc-122">Benannter Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-122">Named type</span></span>](#named-type)                          | <span data-ttu-id="cb9bc-123">Benannter Verweis auf einen primitiven Typ, eine Text Konvention oder einen eingeschränkten Typ.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-123">Named reference to a primitive type, textual convention, or constrained type.</span></span>                                                                                                                                                                    |
| [<span data-ttu-id="cb9bc-124">Eingeschränkter Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-124">Constrained type</span></span>](#constrained-type)              | <span data-ttu-id="cb9bc-125">Primitiver Typ, benannter Typ oder Text Konvention, der durch einen unter Typisierungs Mechanismus eingeschränkt wurde, der in den SMI-Dokumenten RFC 1213 und RFC 1903 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-125">Primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span>                                                                                      |



 

## <a name="primitive-type"></a><span data-ttu-id="cb9bc-126">Primitiver Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-126">Primitive Type</span></span>

<span data-ttu-id="cb9bc-127">Der primitive Typ ist einer der grundlegenden Datentypen, die in der Struktur der Verwaltungsinformationen (SMI)-Dokumente RFC 1213 und RFC 1903 definiert sind.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-127">The primitive type is one of the basic data types defined in the Structure of Management Information (SMI) documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="cb9bc-128">Primitive SNMP-Typen werden CIM-definierten Typen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-128">SNMP primitive types map to CIM-defined types.</span></span> <span data-ttu-id="cb9bc-129">In der folgenden Tabelle wird die Zuordnung aufgelistet, die auftritt, wenn sich die Syntax Klausel explizit auf einen primitiven Typ für SNMPv1 bezieht.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-129">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv1.</span></span> <span data-ttu-id="cb9bc-130">Die Qualifizierer für **Text \_ Konventionen**, **Codierung** und **Objekt \_ Syntax** sind immer identisch mit dem MIB-Typ, und der Standardwert ist immer **null**.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-130">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="cb9bc-131">MIB-Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-131">MIB type</span></span>         | <span data-ttu-id="cb9bc-132">CIM-Variant-Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-132">CIM variant type</span></span> | <span data-ttu-id="cb9bc-133">CimType-Wert</span><span class="sxs-lookup"><span data-stu-id="cb9bc-133">cimtype value</span></span> |
|------------------|------------------|---------------|
| <span data-ttu-id="cb9bc-134">INTEGER</span><span class="sxs-lookup"><span data-stu-id="cb9bc-134">INTEGER</span></span>          | <span data-ttu-id="cb9bc-135">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cb9bc-135">VT\_I4</span></span>           | <span data-ttu-id="cb9bc-136">**sint32**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-136">**sint32**</span></span>    |
| <span data-ttu-id="cb9bc-137">Octetstring</span><span class="sxs-lookup"><span data-stu-id="cb9bc-137">OCTETSTRING</span></span>      | <span data-ttu-id="cb9bc-138">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-138">VT\_BSTR</span></span>         | <span data-ttu-id="cb9bc-139">**string**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-139">**string**</span></span>    |
| <span data-ttu-id="cb9bc-140">OBJECTIDENTIFIER</span><span class="sxs-lookup"><span data-stu-id="cb9bc-140">OBJECTIDENTIFIER</span></span> | <span data-ttu-id="cb9bc-141">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-141">VT\_BSTR</span></span>         | <span data-ttu-id="cb9bc-142">**string**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-142">**string**</span></span>    |
| <span data-ttu-id="cb9bc-143">NULL</span><span class="sxs-lookup"><span data-stu-id="cb9bc-143">NULL</span></span>             | <span data-ttu-id="cb9bc-144">VT \_ null</span><span class="sxs-lookup"><span data-stu-id="cb9bc-144">VT\_NULL</span></span>         | <span data-ttu-id="cb9bc-145">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cb9bc-145">Not supported</span></span> |
| <span data-ttu-id="cb9bc-146">IpAddress</span><span class="sxs-lookup"><span data-stu-id="cb9bc-146">IpAddress</span></span>        | <span data-ttu-id="cb9bc-147">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-147">VT\_BSTR</span></span>         | <span data-ttu-id="cb9bc-148">**string**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-148">**string**</span></span>    |
| <span data-ttu-id="cb9bc-149">Zähler</span><span class="sxs-lookup"><span data-stu-id="cb9bc-149">Counter</span></span>          | <span data-ttu-id="cb9bc-150">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cb9bc-150">VT\_I4</span></span>           | <span data-ttu-id="cb9bc-151">**uint32**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-151">**uint32**</span></span>    |
| <span data-ttu-id="cb9bc-152">Maßstab</span><span class="sxs-lookup"><span data-stu-id="cb9bc-152">Gauge</span></span>            | <span data-ttu-id="cb9bc-153">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cb9bc-153">VT\_I4</span></span>           | <span data-ttu-id="cb9bc-154">**uint32**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-154">**uint32**</span></span>    |
| <span data-ttu-id="cb9bc-155">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="cb9bc-155">TimeTicks</span></span>        | <span data-ttu-id="cb9bc-156">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cb9bc-156">VT\_I4</span></span>           | <span data-ttu-id="cb9bc-157">**uint32**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-157">**uint32**</span></span>    |
| <span data-ttu-id="cb9bc-158">Nicht transparent</span><span class="sxs-lookup"><span data-stu-id="cb9bc-158">Opaque</span></span>           | <span data-ttu-id="cb9bc-159">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-159">VT\_BSTR</span></span>         | <span data-ttu-id="cb9bc-160">**string**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-160">**string**</span></span>    |
| <span data-ttu-id="cb9bc-161">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="cb9bc-161">NetworkAddress</span></span>   | <span data-ttu-id="cb9bc-162">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-162">VT\_BSTR</span></span>         | <span data-ttu-id="cb9bc-163">**string**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-163">**string**</span></span>    |



 

<span data-ttu-id="cb9bc-164">Der Anbieter ignoriert das objekttypmakro, wenn die Syntax Klausel auf **null** verweist, entweder explizit oder durch eine benannte Typzuweisung.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-164">The provider ignores the OBJECT-TYPE macro when the SYNTAX clause refers to **NULL**, either explicitly or through a named type assignment.</span></span> <span data-ttu-id="cb9bc-165">In der folgenden Tabelle wird die Zuordnung aufgelistet, die auftritt, wenn sich die Syntax Klausel explizit auf einen primitiven Typ für SNMPv2 bezieht.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-165">The following table lists the mapping that occurs when the SYNTAX clause explicitly refers to a primitive type for SNMPv2.</span></span> <span data-ttu-id="cb9bc-166">Die Qualifizierer für **Text \_ Konventionen**, **Codierung** und **Objekt \_ Syntax** sind immer identisch mit dem MIB-Typ, und der Standardwert ist immer **null**.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-166">The **textual\_convention**, **encoding**, and **object\_syntax** qualifiers are always the same as the MIB type and the default value is always **NULL**.</span></span>



| <span data-ttu-id="cb9bc-167">MIB-Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-167">MIB type</span></span>          | <span data-ttu-id="cb9bc-168">CIM-Variant-Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-168">CIM variant type</span></span> | <span data-ttu-id="cb9bc-169">CimType-Wert</span><span class="sxs-lookup"><span data-stu-id="cb9bc-169">cimtype value</span></span> |
|-------------------|------------------|---------------|
| <span data-ttu-id="cb9bc-170">INTEGER</span><span class="sxs-lookup"><span data-stu-id="cb9bc-170">INTEGER</span></span>           | <span data-ttu-id="cb9bc-171">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cb9bc-171">VT\_I4</span></span>           | <span data-ttu-id="cb9bc-172">**sint32**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-172">**sint32**</span></span>    |
| <span data-ttu-id="cb9bc-173">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cb9bc-173">OCTET STRING</span></span>      | <span data-ttu-id="cb9bc-174">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-174">VT\_BSTR</span></span>         | <span data-ttu-id="cb9bc-175">**string**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-175">**string**</span></span>    |
| <span data-ttu-id="cb9bc-176">Objekt Bezeichner</span><span class="sxs-lookup"><span data-stu-id="cb9bc-176">OBJECT IDENTIFIER</span></span> | <span data-ttu-id="cb9bc-177">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-177">VT\_BSTR</span></span>         | <span data-ttu-id="cb9bc-178">**string**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-178">**string**</span></span>    |
| <span data-ttu-id="cb9bc-179">IpAddress</span><span class="sxs-lookup"><span data-stu-id="cb9bc-179">IpAddress</span></span>         | <span data-ttu-id="cb9bc-180">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-180">VT\_BSTR</span></span>         | <span data-ttu-id="cb9bc-181">**string**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-181">**string**</span></span>    |
| <span data-ttu-id="cb9bc-182">Counter32</span><span class="sxs-lookup"><span data-stu-id="cb9bc-182">Counter32</span></span>         | <span data-ttu-id="cb9bc-183">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cb9bc-183">VT\_I4</span></span>           | <span data-ttu-id="cb9bc-184">**uint32**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-184">**uint32**</span></span>    |
| <span data-ttu-id="cb9bc-185">Gauge32</span><span class="sxs-lookup"><span data-stu-id="cb9bc-185">Gauge32</span></span>           | <span data-ttu-id="cb9bc-186">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cb9bc-186">VT\_I4</span></span>           | <span data-ttu-id="cb9bc-187">**uint32**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-187">**uint32**</span></span>    |
| <span data-ttu-id="cb9bc-188">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="cb9bc-188">Unsigned32</span></span>        | <span data-ttu-id="cb9bc-189">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cb9bc-189">VT\_I4</span></span>           | <span data-ttu-id="cb9bc-190">**uint32**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-190">**uint32**</span></span>    |
| <span data-ttu-id="cb9bc-191">Integer32</span><span class="sxs-lookup"><span data-stu-id="cb9bc-191">Integer32</span></span>         | <span data-ttu-id="cb9bc-192">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cb9bc-192">VT\_I4</span></span>           | <span data-ttu-id="cb9bc-193">**sint32**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-193">**sint32**</span></span>    |
| <span data-ttu-id="cb9bc-194">Counter64</span><span class="sxs-lookup"><span data-stu-id="cb9bc-194">Counter64</span></span>         | <span data-ttu-id="cb9bc-195">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-195">VT\_BSTR</span></span>         | <span data-ttu-id="cb9bc-196">**uint64**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-196">**uint64**</span></span>    |
| <span data-ttu-id="cb9bc-197">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="cb9bc-197">TimeTicks</span></span>         | <span data-ttu-id="cb9bc-198">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="cb9bc-198">VT\_I4</span></span>           | <span data-ttu-id="cb9bc-199">**uint32**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-199">**uint32**</span></span>    |
| <span data-ttu-id="cb9bc-200">Nicht transparent</span><span class="sxs-lookup"><span data-stu-id="cb9bc-200">Opaque</span></span>            | <span data-ttu-id="cb9bc-201">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-201">VT\_BSTR</span></span>         | <span data-ttu-id="cb9bc-202">**string**</span><span class="sxs-lookup"><span data-stu-id="cb9bc-202">**string**</span></span>    |



 

## <a name="named-type"></a><span data-ttu-id="cb9bc-203">Benannter Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-203">Named Type</span></span>

<span data-ttu-id="cb9bc-204">Benannte SNMP-Typen werden CIM-definierten Typen zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-204">SNMP named types map to CIM-defined types.</span></span> <span data-ttu-id="cb9bc-205">Wenn sich die Syntax Klausel auf einen [primitiven Typ](#primitive-type), eine [Text Konvention](textual-convention-macro.md)oder einen [eingeschränkten Typ](#constrained-type) durch eine typzuweisungs Ableitung bezieht, verwenden Sie die diese Typen, um zu bestimmen, welche Zuordnungs Prozeduren angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-205">When the SYNTAX clause refers to a [primitive type](#primitive-type), [textual convention](textual-convention-macro.md), or [constrained type](#constrained-type) through a type assignment derivation, use the those types to determine which mapping procedures apply.</span></span>

-   <span data-ttu-id="cb9bc-206">Wenn bei der Ableitung der typzuweisungs Regeln eine beschränkte Typdefinition auftritt:</span><span class="sxs-lookup"><span data-stu-id="cb9bc-206">If, through derivation of the type assignment rules, you encounter a constrained type definition:</span></span>

    -   <span data-ttu-id="cb9bc-207">Wenn Sie durch weitere Ableitung eine der im [Textkonventionen-Makro](textual-convention-macro.md)aufgeführten Textkonventionen sehen, wenden Sie dann die Zuordnungsregeln für eingeschränkte Typen und Textkonventionen an.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-207">And if, through further derivation, you encounter one of the textual conventions listed in [TEXTUAL-CONVENTION Macro](textual-convention-macro.md), then apply the mapping rules for constrained types and textual conventions.</span></span>
    -   <span data-ttu-id="cb9bc-208">Wenn Sie einen der primitiven Typen sehen, die in der Tabelle primitiver Typen aufgeführt sind, wenden Sie andernfalls die Zuordnungsregeln für primitive Typen und eingeschränkte Typen an.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-208">Otherwise, if you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types and constrained types.</span></span>

-   <span data-ttu-id="cb9bc-209">Wenn eine der im [Text \_ Konvention-Makro](textual-convention-macro.md)aufgeführten Textkonventionen vorliegt, wenden Sie die Zuordnungsregeln für Textkonventionen an.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-209">If you encounter one of the textual conventions listed in [TEXTUAL\_CONVENTION Macro](textual-convention-macro.md), apply the mapping rules for textual conventions.</span></span>
-   <span data-ttu-id="cb9bc-210">Wenn Sie einen der primitiven Typen sehen, die in der Tabelle primitiver Typen aufgeführt sind, wenden Sie die Zuordnungsregeln für primitive Typen an.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-210">If you encounter one of the primitive types listed in either primitive type table, apply the mapping rules for primitive types.</span></span>

> [!Note]  
> <span data-ttu-id="cb9bc-211">Klassen, die Eigenschafts Typen enthalten, die nicht mit der oben beschriebenen Zuordnung übereinstimmen, sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-211">Classes containing property types that do not conform to the mapping described above are not valid.</span></span> <span data-ttu-id="cb9bc-212">In diesem Fall gibt der Anbieter einen Fehler zurück, wenn der Anbieter den Abruf einer Klassendefinition beim Ausführen einer Instanzabruf Funktion anfordert.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-212">In this case, the provider returns an error if and when the provider requests the retrieval of a class definition while executing an instance retrieval function.</span></span>

 

## <a name="constrained-type"></a><span data-ttu-id="cb9bc-213">Eingeschränkter Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-213">Constrained Type</span></span>

<span data-ttu-id="cb9bc-214">Ein eingeschränkter Typ ist ein primitiver Typ, benannter Typ oder eine Text Konvention, der durch einen unter Typisierungs Mechanismus eingeschränkt wurde, der in den SMI-Dokumenten RFC 1213 und RFC 1903 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-214">A constrained type is a primitive type, named type, or textual convention that has been constrained by some subtyping mechanism defined in the SMI documents RFC 1213 and RFC 1903.</span></span> <span data-ttu-id="cb9bc-215">Wenn die unter Typisierung erfolgt, sind zusätzliche CIM-Qualifizierer erforderlich, um die Untertyp Werte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-215">When subtyping occurs, additional CIM qualifiers are required to specify the subtype values.</span></span> <span data-ttu-id="cb9bc-216">Die benannte Typdefinition in der Syntax Klausel ordnet die **\_ Syntax** des CIM-Eigenschafts qualifiziererobjekts bis zu, ohne die Einschränkungen des unter Typs.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-216">The named-type definition in the SYNTAX clause maps verbatim to the CIM property qualifier **object\_syntax** up to, but not including the constraints of the subtype.</span></span>

<span data-ttu-id="cb9bc-217">Untertypen können einem der folgenden Formate folgen:</span><span class="sxs-lookup"><span data-stu-id="cb9bc-217">Subtypes may follow any of the following formats:</span></span>

-   <span data-ttu-id="cb9bc-218">Enumerierte Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="cb9bc-218">Enumerated INTEGER</span></span>

    <span data-ttu-id="cb9bc-219">Die CIM-Eigenschaft **qualifiziererenumeration** gibt die Enumerationswerte an.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-219">The CIM property qualifier **enumeration** specifies the enumerated values.</span></span> <span data-ttu-id="cb9bc-220">Dieser Qualifizierer wird als Zeichenfolge dargestellt, die eine durch Trennzeichen getrennte Liste von ganzzahligen 32-Bit-Werten enthält.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-220">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="cb9bc-221">In der folgenden Tabelle sind die-Mapping-Typen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-221">The following table lists the mapping types.</span></span> <span data-ttu-id="cb9bc-222">Der Standardwert ist immer **null**.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-222">The default value is always **NULL**.</span></span>



| <span data-ttu-id="cb9bc-223">Eingeschränkter MIB-Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-223">Constrained MIB type</span></span> | <span data-ttu-id="cb9bc-224">CIM-Variant-Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-224">CIM variant type</span></span> | <span data-ttu-id="cb9bc-225">CIM Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="cb9bc-225">CIM qualifiers</span></span>                                                                                                        |
|----------------------|------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb9bc-226">Enumerierte Ganzzahl</span><span class="sxs-lookup"><span data-stu-id="cb9bc-226">Enumerated INTEGER</span></span>   | <span data-ttu-id="cb9bc-227">VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-227">VT\_BSTR</span></span>         | <span data-ttu-id="cb9bc-228">**Text \_ Konvention**: enumeratedinteger</span><span class="sxs-lookup"><span data-stu-id="cb9bc-228">**textual\_convention**: enumeratedinteger</span></span><br/> <span data-ttu-id="cb9bc-229">**Codierung**: ganze Zahl</span><span class="sxs-lookup"><span data-stu-id="cb9bc-229">**encoding**: INTEGER</span></span><br/> <span data-ttu-id="cb9bc-230">**CimType**: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cb9bc-230">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="cb9bc-231">BITS</span><span class="sxs-lookup"><span data-stu-id="cb9bc-231">BITS</span></span>

    <span data-ttu-id="cb9bc-232">Der CIM-Eigenschaften Qualifizierer **Bits** gibt die Enumerationswerte an.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-232">The CIM property qualifier **bits** specifies the enumerated values.</span></span> <span data-ttu-id="cb9bc-233">Dieser Qualifizierer wird als Zeichenfolge dargestellt, die eine durch Trennzeichen getrennte Liste von ganzzahligen 32-Bit-Werten enthält.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-233">This qualifier is represented as a string containing a comma-separated list of signed 32-bit integer values.</span></span> <span data-ttu-id="cb9bc-234">In der folgenden Tabelle sind die-Mapping-Typen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-234">The following table lists the mapping types.</span></span> <span data-ttu-id="cb9bc-235">Der Standardwert ist immer **null**.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-235">The default value is always **NULL**.</span></span>



| <span data-ttu-id="cb9bc-236">Eingeschränkter MIB-Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-236">Constrained MIB type</span></span> | <span data-ttu-id="cb9bc-237">CIM-Variant-Typ</span><span class="sxs-lookup"><span data-stu-id="cb9bc-237">CIM variant type</span></span>      | <span data-ttu-id="cb9bc-238">CIM Qualifizierer</span><span class="sxs-lookup"><span data-stu-id="cb9bc-238">CIM qualifiers</span></span>                                                                                               |
|----------------------|-----------------------|--------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb9bc-239">BITS</span><span class="sxs-lookup"><span data-stu-id="cb9bc-239">BITS</span></span>                 | <span data-ttu-id="cb9bc-240">VT \_ array \| VT \_ BSTR</span><span class="sxs-lookup"><span data-stu-id="cb9bc-240">VT\_ARRAY \| VT\_BSTR</span></span> | <span data-ttu-id="cb9bc-241">**Text \_ Konvention**: Bits</span><span class="sxs-lookup"><span data-stu-id="cb9bc-241">**textual\_convention**: bits</span></span><br/> <span data-ttu-id="cb9bc-242">**Codierung**: octetstring</span><span class="sxs-lookup"><span data-stu-id="cb9bc-242">**encoding**: OCTETSTRING</span></span><br/> <span data-ttu-id="cb9bc-243">**CimType**: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="cb9bc-243">**cimtype**: string</span></span><br/> |



 

-   <span data-ttu-id="cb9bc-244">Variable Länge</span><span class="sxs-lookup"><span data-stu-id="cb9bc-244">Variable-length</span></span>

    <span data-ttu-id="cb9bc-245">Wenn sich die Syntax Klausel auf einen primitiven Typ, einen benannten Typ oder eine Text Konvention bezieht, die als Oktett-Zeichenfolge mit variabler Länge oder als nicht transparent typisiert ist, gibt die **\_ Länge der Länge** des CIM-Eigenschaften Qualifizierers den minimalen, maximalen und den Wert mit fester Länge an, der der Typdefinition zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-245">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a variable-length OCTET STRING or Opaque, the CIM property qualifier **variable\_length** specifies the minimum, maximum, and fixed-length values associated with the type definition.</span></span> <span data-ttu-id="cb9bc-246">Dieser Qualifizierer wird als Zeichenfolge im folgenden Format implementiert, in dem die Werte variabler Länge als Vorzeichen lose ganze Zahlen mit Vorzeichen (32 Bit) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-246">This qualifier is implemented as a string in the following format where the variable-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9) .. (0.9)) | (0.9))(, (((0.9) .. (0.9)) | (0.9)))*
    ```

-   <span data-ttu-id="cb9bc-247">Feste Länge</span><span class="sxs-lookup"><span data-stu-id="cb9bc-247">Fixed-length</span></span>

    <span data-ttu-id="cb9bc-248">Wenn sich die Syntax Klausel auf einen primitiven Typ, einen benannten Typ oder eine Text Konvention bezieht, die als Oktett-Zeichenfolge mit fester Länge oder als nicht transparent typisiert ist, gibt die **festgelegte \_ Länge** des CIM-Eigenschaften Qualifizierers den Wert mit fester Länge an.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-248">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a fixed-length OCTET STRING or Opaque, the CIM property qualifier **fixed\_length** specifies the fixed-length value.</span></span> <span data-ttu-id="cb9bc-249">Dieser Qualifizierer wird als ganzzahliger Wert ohne Vorzeichen (32 Bit) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-249">This qualifier is represented as an unsigned 32-bit integer value.</span></span>

-   <span data-ttu-id="cb9bc-250">Range</span><span class="sxs-lookup"><span data-stu-id="cb9bc-250">Range</span></span>

    <span data-ttu-id="cb9bc-251">Wenn sich die Syntax Klausel auf einen primitiven Typ, einen benannten Typ oder eine Text Konvention bezieht, die als eine ganze Zahl oder eine ganze Zahl mit fester Wert oder einem Messgerät subtypisiert ist, gibt der **\_ Wert** des CIM-Eigenschafts Qualifizierers den mit der Typdefinition verknüpften Bereich und die Werte an</span><span class="sxs-lookup"><span data-stu-id="cb9bc-251">When the SYNTAX clause refers to a primitive type, named type, or textual convention that is subtyped as a ranged or fixed-value INTEGER or Gauge, the CIM property qualifier **variable\_value** specifies the ranged and fixed values associated with the type definition.</span></span> <span data-ttu-id="cb9bc-252">Dieser Qualifizierer wird als Zeichenfolge im folgenden Format implementiert, wobei der Bereich und die Werte mit fester Länge als Vorzeichen lose ganze Zahlen mit Vorzeichen (32 Bit) dargestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-252">This qualifier is implemented as a string in the following format where the range and fixed-length values are represented as unsigned 32-bit integers.</span></span>

    ``` syntax
    (((0.9)..(0.9))|(0.9))(,(((0.9)..(0.9))|(0.9)))*
    ```

## <a name="example-code"></a><span data-ttu-id="cb9bc-253">Beispielcode</span><span class="sxs-lookup"><span data-stu-id="cb9bc-253">Example Code</span></span>

<span data-ttu-id="cb9bc-254">Im folgenden Beispiel wird ein enumerierter ganzzahliger Untertyp beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-254">The following example describes an enumerated INTEGER subtype.</span></span>

``` syntax
Status := INTEGER {
up(1),
down(2),
testing(3)
}
```

<span data-ttu-id="cb9bc-255">In diesem Beispiel wird Folgendes dargestellt:</span><span class="sxs-lookup"><span data-stu-id="cb9bc-255">This example maps to:</span></span>

``` syntax
enumeration("up(1),down(2),testing(3)")
```

<span data-ttu-id="cb9bc-256">Im folgenden Codebeispiel wird ein Bits-Untertyp beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-256">The following code example describes a BITS subtype.</span></span>

``` syntax
Status := BITS {
up(1),
down(2), 
testing(3)
}
```

<span data-ttu-id="cb9bc-257">Im folgenden Codebeispiel wird Folgendes veranschaulicht:</span><span class="sxs-lookup"><span data-stu-id="cb9bc-257">The following code example maps to:</span></span>

``` syntax
bits("up(1),down(2),testing(3)")
```

<span data-ttu-id="cb9bc-258">Im folgenden Codebeispiel wird ein Untertyp variabler Länge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-258">The following code example describes a variable-length subtype.</span></span>

``` syntax
MySnmpOSIAddress ::=  TEXTUAL-CONVENTION

    DISPLAY-HINT    "*1x:/1x:"
    STATUS        current
    DESCRIPTION
            "Represents an OSI transport-address:

            octets    contents         encoding
              1        length of NSAP   'n' as an unsigned-integer
                                        (either 0 or from 3 to 20)
              2..(n+1)  NSAP          concrete binary representation
              (n+2)..m  TSEL             string of (up to 64) octets
            "
    SYNTAX         OCTET STRING (SIZE (1|4..85))
```

<span data-ttu-id="cb9bc-259">In diesem Beispiel wird Folgendes dargestellt:</span><span class="sxs-lookup"><span data-stu-id="cb9bc-259">This example maps to:</span></span>

``` syntax
display_hint("*1x:/1x:"),
encoding("OCTETSTRING"),
textual_convention("OCTETSTRING"),
variable_length ("1,4..85")
```

<span data-ttu-id="cb9bc-260">Im folgenden Beispiel wird ein Untertyp mit fester Länge beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-260">The following example describes a fixed-length subtype.</span></span>

``` syntax
IPXADDRESS := OCTET STRING (SIZE (6))
```

<span data-ttu-id="cb9bc-261">In diesem Beispiel wird Folgendes dargestellt:</span><span class="sxs-lookup"><span data-stu-id="cb9bc-261">This example maps to:</span></span>

``` syntax
fixed_length(6)
```

<span data-ttu-id="cb9bc-262">Im folgenden Beispiel wird ein Bereichs Untertyp beschrieben.</span><span class="sxs-lookup"><span data-stu-id="cb9bc-262">The following example describes a range subtype.</span></span>

``` syntax
Status := INTEGER (10..20|8)
```

<span data-ttu-id="cb9bc-263">In diesem Beispiel wird Folgendes dargestellt:</span><span class="sxs-lookup"><span data-stu-id="cb9bc-263">This example maps to:</span></span>

``` syntax
variable_value("10..20,8")
```

 

 




