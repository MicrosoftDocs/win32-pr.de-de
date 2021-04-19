---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1091 bis 1100.
ms.assetid: 9b7db4fc-8ae8-46f7-a40f-e4401a335c5d
ms.tgt_platform: multiple
title: Fehler 1091 bis 1100
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf582a3df41fbc7c329f5a993555a2d76145ded0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366490"
---
# <a name="errors-1091-through-1100"></a><span data-ttu-id="ef890-103">Fehler 1091 bis 1100</span><span class="sxs-lookup"><span data-stu-id="ef890-103">Errors 1091 through 1100</span></span>

<span data-ttu-id="ef890-104">Beschreibt die WMI-SNMP-Anbieter Fehler 1091 bis 1100.</span><span class="sxs-lookup"><span data-stu-id="ef890-104">Describes WMI SNMP provider errors 1091 through 1100.</span></span>

[<span data-ttu-id="ef890-105">Warnung 1091</span><span class="sxs-lookup"><span data-stu-id="ef890-105">Warning 1091</span></span>](#warning-1091)

[<span data-ttu-id="ef890-106">Schwerwiegender Fehler 1092</span><span class="sxs-lookup"><span data-stu-id="ef890-106">Fatal Error 1092</span></span>](#fatal-error-1092)

[<span data-ttu-id="ef890-107">Schwerwiegender Fehler 1093</span><span class="sxs-lookup"><span data-stu-id="ef890-107">Fatal Error 1093</span></span>](#fatal-error-1093)

[<span data-ttu-id="ef890-108">Schwerwiegender Fehler 1094</span><span class="sxs-lookup"><span data-stu-id="ef890-108">Fatal Error 1094</span></span>](#fatal-error-1094)

[<span data-ttu-id="ef890-109">Schwerwiegender Fehler 1095</span><span class="sxs-lookup"><span data-stu-id="ef890-109">Fatal Error 1095</span></span>](#fatal-error-1095)

[<span data-ttu-id="ef890-110">Schwerwiegender Fehler 1097</span><span class="sxs-lookup"><span data-stu-id="ef890-110">Fatal Error 1097</span></span>](#fatal-error-1097)

[<span data-ttu-id="ef890-111">Schwerwiegender Fehler 1098</span><span class="sxs-lookup"><span data-stu-id="ef890-111">Fatal Error 1098</span></span>](#fatal-error-1098)

[<span data-ttu-id="ef890-112">Schwerwiegender Fehler 1099</span><span class="sxs-lookup"><span data-stu-id="ef890-112">Fatal Error 1099</span></span>](#fatal-error-1099)

## <a name="warning-1091"></a><span data-ttu-id="ef890-113">Warnung 1091</span><span class="sxs-lookup"><span data-stu-id="ef890-113">Warning 1091</span></span>

<dl> <dt>

<span data-ttu-id="ef890-114"><span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, Warning>: " <fileName> : <line \#> implizierte Klausel ist für Objekte mit fester Größe nicht zulässig"**</span><span class="sxs-lookup"><span data-stu-id="ef890-114"><span id="_1091__Warning_____fileName___line___IMPLIED_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__warning_____filename___line___implied_clause_is_not_allowed_for_fixed_size_objects_"></span><span id="_1091__WARNING_____FILENAME___LINE___IMPLIED_CLAUSE_IS_NOT_ALLOWED_FOR_FIXED_SIZE_OBJECTS_"></span>**<1091, Warning>: "<fileName>:<line\#> IMPLIED clause is not allowed for fixed size objects"**</span></span>
</dt> <dd>

<span data-ttu-id="ef890-115">**Objekttyp-** Makro Aufruf SNMPv2C-spezifische Modul Semantik Warnung.</span><span class="sxs-lookup"><span data-stu-id="ef890-115">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic warning.</span></span> <span data-ttu-id="ef890-116">Das implizierte Schlüsselwort kann nur für ein Objekt vorhanden sein, das eine Syntax mit variabler Länge aufweist, wie z. b. ein Objekt Bezeichner oder eine Oktett-Zeichenfolge mit variabler Länge in der Index-Klausel.</span><span class="sxs-lookup"><span data-stu-id="ef890-116">The IMPLIED keyword can only be present for an object having a variable-length syntax, such as an OBJECT IDENTIFIER or variable-length OCTET STRING, in the INDEX clause.</span></span>

</dd> </dl>

## <a name="fatal-error-1092"></a><span data-ttu-id="ef890-117">Schwerwiegender Fehler 1092</span><span class="sxs-lookup"><span data-stu-id="ef890-117">Fatal Error 1092</span></span>

<dl> <dt>

<span data-ttu-id="ef890-118"><span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, schwerwiegender>: " <fileName> : <Zeile \#> implizierte Klausel ist für Objekte mit einer Länge von NULL nicht zulässig."**</span><span class="sxs-lookup"><span data-stu-id="ef890-118"><span id="_1092__Fatal_____fileName___line___IMPLIED_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__fatal_____filename___line___implied_clause_not_allowed_for_potentially_zero-length_objects_"></span><span id="_1092__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_NOT_ALLOWED_FOR_POTENTIALLY_ZERO-LENGTH_OBJECTS_"></span>**<1092, Fatal>: "<fileName>:<line\#> IMPLIED clause not allowed for potentially zero-length objects"**</span></span>
</dt> <dd>

<span data-ttu-id="ef890-119">**Objekttyp-** Makro Aufruf SNMPv2C-spezifischer modulsemantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="ef890-119">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="ef890-120">Die implizite-Klausel kann nicht für ein Objekt variabler Länge verwendet werden, wenn dieses Objekt eine Länge von 0 (null) aufweisen kann.</span><span class="sxs-lookup"><span data-stu-id="ef890-120">The IMPLIED clause cannot be used on a variable-length object if that object can have a zero length.</span></span>

</dd> </dl>

## <a name="fatal-error-1093"></a><span data-ttu-id="ef890-121">Schwerwiegender Fehler 1093</span><span class="sxs-lookup"><span data-stu-id="ef890-121">Fatal Error 1093</span></span>

<dl> <dt>

<span data-ttu-id="ef890-122"><span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093. Schwerwiegender>: " <fileName><Zeile \#>: nur der Typ" Integer "kann gemäß v1 SMI aufgelistet werden.**</span><span class="sxs-lookup"><span data-stu-id="ef890-122"><span id="_1093._Fatal_____fileName__line____Only_the_type__INTEGER__can_be_enumerated_according_to_the_V1_SMI_"></span><span id="_1093._fatal_____filename__line____only_the_type__integer__can_be_enumerated_according_to_the_v1_smi_"></span><span id="_1093._FATAL_____FILENAME__LINE____ONLY_THE_TYPE__INTEGER__CAN_BE_ENUMERATED_ACCORDING_TO_THE_V1_SMI_"></span>**<1093. Fatal>: "<fileName><line\#>: Only the type "INTEGER" can be enumerated according to the V1 SMI"**</span></span>
</dt> <dd>

<span data-ttu-id="ef890-123">Typzuweisung, SNMPv1-spezifischer modulsemantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="ef890-123">Type assignment, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="ef890-124">Eine SNMPv1 MIB-Enumeration kann nur den Integer-Typ verwenden.</span><span class="sxs-lookup"><span data-stu-id="ef890-124">An SNMPv1 MIB enumeration can use only the type INTEGER.</span></span>

</dd> </dl>

## <a name="fatal-error-1094"></a><span data-ttu-id="ef890-125">Schwerwiegender Fehler 1094</span><span class="sxs-lookup"><span data-stu-id="ef890-125">Fatal Error 1094</span></span>

<dl> <dt>

<span data-ttu-id="ef890-126"><span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094. Schwerwiegender>: " <fileName><Zeilen \#>: der in der Enumeration verwendete Typ wird nicht in einen der zulässigen Typen aufgelöst."**</span><span class="sxs-lookup"><span data-stu-id="ef890-126"><span id="_1094._Fatal_____fileName__line____The_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._fatal_____filename__line____the_type_used_in_the_enumeration_does_not_resolve_to_one_of_the_allowed_types_"></span><span id="_1094._FATAL_____FILENAME__LINE____THE_TYPE_USED_IN_THE_ENUMERATION_DOES_NOT_RESOLVE_TO_ONE_OF_THE_ALLOWED_TYPES_"></span>**<1094. Fatal>: "<fileName><line\#>: The type used in the enumeration does not resolve to one of the allowed types"**</span></span>
</dt> <dd>

<span data-ttu-id="ef890-127">Typzuweisung, SNMPv2C-spezifischer modulsemantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="ef890-127">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="ef890-128">Der in einer Enumeration verwendete Typ muss ein ganzzahliger Typ oder ein entsprechender Typ oder eine andere Enumeration sein.</span><span class="sxs-lookup"><span data-stu-id="ef890-128">The type used in an enumeration must be INTEGER or an equivalent type, or another enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1095"></a><span data-ttu-id="ef890-129">Schwerwiegender Fehler 1095</span><span class="sxs-lookup"><span data-stu-id="ef890-129">Fatal Error 1095</span></span>

<dl> <dt>

<span data-ttu-id="ef890-130"><span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095. Schwerwiegender>: " <fileName><line \#>: der Enumerationsmember ist kein Member der übergeordneten Enumeration"**</span><span class="sxs-lookup"><span data-stu-id="ef890-130"><span id="_1095._Fatal_____fileName__line____Enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._fatal_____filename__line____enumeration_member_is_not_a_member_of_the_parent_enumeration_"></span><span id="_1095._FATAL_____FILENAME__LINE____ENUMERATION_MEMBER_IS_NOT_A_MEMBER_OF_THE_PARENT_ENUMERATION_"></span>**<1095. Fatal>: "<fileName><line\#>: Enumeration member is not a member of the parent enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="ef890-131">Typzuweisung, SNMPv2C-spezifischer modulsemantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="ef890-131">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="ef890-132">Wenn eine andere Enumeration verwendet wird, muss der Satz von Elementen eine Teilmenge der Elemente der übergeordneten Enumeration sein.</span><span class="sxs-lookup"><span data-stu-id="ef890-132">If another enumeration is used, its set of items must be a subset of the parent enumeration's set of items.</span></span>

</dd> </dl>

## <a name="fatal-error-1097"></a><span data-ttu-id="ef890-133">Schwerwiegender Fehler 1097</span><span class="sxs-lookup"><span data-stu-id="ef890-133">Fatal Error 1097</span></span>

<dl> <dt>

<span data-ttu-id="ef890-134"><span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097, schwerwiegender>: " <fileName><line \#>: Bezeichner <name> wird nicht in einen ganzzahligen Wert aufgelöst"**</span><span class="sxs-lookup"><span data-stu-id="ef890-134"><span id="_1097__Fatal_____fileName__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__fatal_____filename__line____identifier__name__does_not_resolve_to_an_integer_value_"></span><span id="_1097__FATAL_____FILENAME__LINE____IDENTIFIER__NAME__DOES_NOT_RESOLVE_TO_AN_INTEGER_VALUE_"></span>**<1097, Fatal>: "<fileName><line\#>: identifier <name> does not resolve to an integer value"**</span></span>
</dt> <dd>

<span data-ttu-id="ef890-135">Typzuweisung, SNMPv2C-spezifischer modulsemantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="ef890-135">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="ef890-136">Die Werte im Bits-Typ müssen ganzzahlige Werte sein.</span><span class="sxs-lookup"><span data-stu-id="ef890-136">The values in the BITS type must be integer values.</span></span>

</dd> </dl>

## <a name="fatal-error-1098"></a><span data-ttu-id="ef890-137">Schwerwiegender Fehler 1098</span><span class="sxs-lookup"><span data-stu-id="ef890-137">Fatal Error 1098</span></span>

<dl> <dt>

<span data-ttu-id="ef890-138"><span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098, schwerwiegender>: " <fileName><Zeilen \#>: doppelter Wert <value> in Bits-Konstrukt"**</span><span class="sxs-lookup"><span data-stu-id="ef890-138"><span id="_1098__Fatal_____fileName__line____Duplicate_value__value__in_BITS_construct_"></span><span id="_1098__fatal_____filename__line____duplicate_value__value__in_bits_construct_"></span><span id="_1098__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_BITS_CONSTRUCT_"></span>**<1098, Fatal>: "<fileName><line\#>: Duplicate value <value> in BITS construct"**</span></span>
</dt> <dd>

<span data-ttu-id="ef890-139">Typzuweisung, SNMPv2C-spezifischer modulsemantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="ef890-139">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="ef890-140">In einem Bits-Konstrukt dürfen keine doppelten Namen und Werte vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ef890-140">There must be no duplicate names and values in a BITS construct.</span></span> <span data-ttu-id="ef890-141">Der <Zeile \#> Parameter ist die Position der Wiederholung des Namens/Werts.</span><span class="sxs-lookup"><span data-stu-id="ef890-141">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1099"></a><span data-ttu-id="ef890-142">Schwerwiegender Fehler 1099</span><span class="sxs-lookup"><span data-stu-id="ef890-142">Fatal Error 1099</span></span>

<dl> <dt>

<span data-ttu-id="ef890-143"><span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099, schwerwiegender>: " <fileName><line \#>: Doppelter Name <identifier> in Bits-Konstrukt"**</span><span class="sxs-lookup"><span data-stu-id="ef890-143"><span id="_1099__Fatal_____fileName__line____Duplicate_name__identifier__in_BITS_construct_"></span><span id="_1099__fatal_____filename__line____duplicate_name__identifier__in_bits_construct_"></span><span id="_1099__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_BITS_CONSTRUCT_"></span>**<1099, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in BITS construct"**</span></span>
</dt> <dd>

<span data-ttu-id="ef890-144">Typzuweisung, SNMPv2C-spezifischer modulsemantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="ef890-144">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="ef890-145">In einem Bits-Konstrukt dürfen keine doppelten Namen und Werte vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ef890-145">There must be no duplicate names and values in a BITS construct.</span></span> <span data-ttu-id="ef890-146">Der <Zeile \#> Parameter ist die Position der Wiederholung des Namens/Werts.</span><span class="sxs-lookup"><span data-stu-id="ef890-146">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

 

 



