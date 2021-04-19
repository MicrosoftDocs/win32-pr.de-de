---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1081 bis 1090.
ms.assetid: aa953c53-a61f-48e4-9234-acc450b9bdf1
ms.tgt_platform: multiple
title: Fehler 1081 bis 1090
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a80399ef61bce644813447559a76bf9710873be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348547"
---
# <a name="errors-1081-through-1090"></a><span data-ttu-id="0670e-103">Fehler 1081 bis 1090</span><span class="sxs-lookup"><span data-stu-id="0670e-103">Errors 1081 through 1090</span></span>

<span data-ttu-id="0670e-104">Beschreibt die WMI-SNMP-Anbieter Fehler 1081 bis 1090.</span><span class="sxs-lookup"><span data-stu-id="0670e-104">Describes WMI SNMP provider errors 1081 through 1090.</span></span>

[<span data-ttu-id="0670e-105">Schwerwiegender Fehler 1081</span><span class="sxs-lookup"><span data-stu-id="0670e-105">Fatal Error 1081</span></span>](#fatal-error-1081)

[<span data-ttu-id="0670e-106">Schwerwiegender Fehler 1082</span><span class="sxs-lookup"><span data-stu-id="0670e-106">Fatal Error 1082</span></span>](#fatal-error-1082)

[<span data-ttu-id="0670e-107">Schwerwiegender Fehler 1084</span><span class="sxs-lookup"><span data-stu-id="0670e-107">Fatal Error 1084</span></span>](#fatal-error-1084)

[<span data-ttu-id="0670e-108">Warnung 1085</span><span class="sxs-lookup"><span data-stu-id="0670e-108">Warning 1085</span></span>](#warning-1085)

[<span data-ttu-id="0670e-109">Warnung 1086</span><span class="sxs-lookup"><span data-stu-id="0670e-109">Warning 1086</span></span>](#warning-1086)

[<span data-ttu-id="0670e-110">Schwerwiegender Fehler 1087</span><span class="sxs-lookup"><span data-stu-id="0670e-110">Fatal Error 1087</span></span>](#fatal-error-1087)

[<span data-ttu-id="0670e-111">Schwerwiegender Fehler 1089</span><span class="sxs-lookup"><span data-stu-id="0670e-111">Fatal Error 1089</span></span>](#fatal-error-1089)

[<span data-ttu-id="0670e-112">Schwerwiegender Fehler 1090</span><span class="sxs-lookup"><span data-stu-id="0670e-112">Fatal Error 1090</span></span>](#fatal-error-1090)

## <a name="fatal-error-1081"></a><span data-ttu-id="0670e-113">Schwerwiegender Fehler 1081</span><span class="sxs-lookup"><span data-stu-id="0670e-113">Fatal Error 1081</span></span>

<dl> <dt>

<span data-ttu-id="0670e-114"><span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081, schwerwiegender>: " <fileName> line \#>: Symbol <identifier> nicht im importierten Modul vorhanden <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="0670e-114"><span id="_1081__Fatal_____fileName_line____Symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__fatal_____filename_line____symbol__identifier__not_present_in_imported_module__identifier__"></span><span id="_1081__FATAL_____FILENAME_LINE____SYMBOL__IDENTIFIER__NOT_PRESENT_IN_IMPORTED_MODULE__IDENTIFIER__"></span>**<1081, Fatal>: "<fileName>line\#>: Symbol <identifier> not present in imported module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="0670e-115">Modul Semantik Fehler in Querverweisen, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="0670e-115">Module semantic error in cross-referencing, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="0670e-116">Ein Symbol, das aus einem Modul importiert wird, wird in nichts in diesem Modul aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="0670e-116">A symbol imported from a module does not resolve to anything in that module.</span></span> <span data-ttu-id="0670e-117">Wenn im MIB tatsächlich auf dieses Symbol verwiesen wird, tritt dieser Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="0670e-117">If that symbol is actually referenced in the MIB, this error occurs.</span></span>

</dd> </dl>

## <a name="fatal-error-1082"></a><span data-ttu-id="0670e-118">Schwerwiegender Fehler 1082</span><span class="sxs-lookup"><span data-stu-id="0670e-118">Fatal Error 1082</span></span>

<dl> <dt>

<span data-ttu-id="0670e-119"><span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082, schwerwiegender>: " <fileName> : <line \#>: Ungültige Status Klausel <clause> "**</span><span class="sxs-lookup"><span data-stu-id="0670e-119"><span id="_1082__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1082__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1082__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span>**<1082, Fatal>: "<fileName>:<line\#>: Invalid STATUS clause <clause>"**</span></span>
</dt> <dd>

<span data-ttu-id="0670e-120">**Objekt-Identitäts** -Makro Aufruf, SNMPv2C-spezifischer Modul Semantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="0670e-120">**OBJECT-IDENTITY** macro invocation, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="0670e-121">Die Status-Klausel eines **Objekt Identitäts aufbilden** muss "Current", "deprecated" oder "deprecated" lauten.</span><span class="sxs-lookup"><span data-stu-id="0670e-121">The STATUS clause of an **OBJECT-IDENTITY** invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="fatal-error-1084"></a><span data-ttu-id="0670e-122">Schwerwiegender Fehler 1084</span><span class="sxs-lookup"><span data-stu-id="0670e-122">Fatal Error 1084</span></span>

<dl> <dt>

<span data-ttu-id="0670e-123"><span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084, schwerwiegender>: "Dateiname><Zeile \#>: erforderliche Module-Identity nach dem Import Abschnitt für alle SNMPv2-Module"**</span><span class="sxs-lookup"><span data-stu-id="0670e-123"><span id="_1084__Fatal____fileName__line____MODULE-IDENTITY_required_after_the_IMPORTS_section_for_all_SNMPv2_modules_"></span><span id="_1084__fatal____filename__line____module-identity_required_after_the_imports_section_for_all_snmpv2_modules_"></span><span id="_1084__FATAL____FILENAME__LINE____MODULE-IDENTITY_REQUIRED_AFTER_THE_IMPORTS_SECTION_FOR_ALL_SNMPV2_MODULES_"></span>**<1084, Fatal>: "fileName><line\#>: MODULE-IDENTITY required after the IMPORTS section for all SNMPv2 modules"**</span></span>
</dt> <dd>

<span data-ttu-id="0670e-124">**Modul-Identity-** Makro Aufruf, SNMPv2C-spezifischer Modul Semantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="0670e-124">**MODULE-IDENTITY** macro invocation, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="0670e-125">Es darf nur ein **Modul Identitäts** Aufruf in einem SNMPv2C MIB vorhanden sein, unmittelbar nach dem Import Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="0670e-125">There must be one and only one **MODULE-IDENTITY** invocation in an SNMPv2C MIB, immediately after the IMPORTS section.</span></span>

</dd> </dl>

## <a name="warning-1085"></a><span data-ttu-id="0670e-126">Warnung 1085</span><span class="sxs-lookup"><span data-stu-id="0670e-126">Warning 1085</span></span>

<dl> <dt>

<span data-ttu-id="0670e-127"><span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, Warning>: " <fileName><line \#>: im Modul wurden keine Gruppen gefunden <name> . Die Modul Identität konnte nicht fabriziert werden. Der Versuch, das Modul in SMIR zu laden, schlägt fehl.**</span><span class="sxs-lookup"><span data-stu-id="0670e-127"><span id="_1085__Warning_____fileName__line____No_groups_found_in_module__name_._Could_not_fabricate_MODULE-IDENTITY._Attempt_to_load_the_module_into_the_SMIR_will_fail_"></span><span id="_1085__warning_____filename__line____no_groups_found_in_module__name_._could_not_fabricate_module-identity._attempt_to_load_the_module_into_the_smir_will_fail_"></span><span id="_1085__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME_._COULD_NOT_FABRICATE_MODULE-IDENTITY._ATTEMPT_TO_LOAD_THE_MODULE_INTO_THE_SMIR_WILL_FAIL_"></span>**<1085, Warning>: "<fileName><line\#>: No groups found in module <name>. Could not fabricate MODULE-IDENTITY. Attempt to load the module into the SMIR will fail"**</span></span>
</dt> <dd>

<span data-ttu-id="0670e-128">Modul Semantik SNMPv1 spezifische Warnung.</span><span class="sxs-lookup"><span data-stu-id="0670e-128">Module semantic SNMPv1-specific warning.</span></span> <span data-ttu-id="0670e-129">Dieser Fehler wird generiert, wenn in einem Modul keine Objektgruppen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="0670e-129">This error is generated if no object groups are found in a module.</span></span>

</dd> </dl>

## <a name="warning-1086"></a><span data-ttu-id="0670e-130">Warnung 1086</span><span class="sxs-lookup"><span data-stu-id="0670e-130">Warning 1086</span></span>

<dl> <dt>

<span data-ttu-id="0670e-131"><span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, Warning>: " <fileName><line \#>: im Modul wurden keine Gruppen gefunden <name> "**</span><span class="sxs-lookup"><span data-stu-id="0670e-131"><span id="_1086__Warning_____fileName__line____No_groups_found_in_module__name__"></span><span id="_1086__warning_____filename__line____no_groups_found_in_module__name__"></span><span id="_1086__WARNING_____FILENAME__LINE____NO_GROUPS_FOUND_IN_MODULE__NAME__"></span>**<1086, Warning>: "<fileName><line\#>: No groups found in module <name>"**</span></span>
</dt> <dd>

<span data-ttu-id="0670e-132">Modul Semantik SNMPv1 spezifische Warnung.</span><span class="sxs-lookup"><span data-stu-id="0670e-132">Module semantic SNMPv1-specific warning.</span></span> <span data-ttu-id="0670e-133">Dieser Fehler wird generiert, wenn in einem Modul keine Objektgruppen gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="0670e-133">This error is generated if no object groups are found in a module.</span></span>

</dd> </dl>

## <a name="fatal-error-1087"></a><span data-ttu-id="0670e-134">Schwerwiegender Fehler 1087</span><span class="sxs-lookup"><span data-stu-id="0670e-134">Fatal Error 1087</span></span>

<dl> <dt>

<span data-ttu-id="0670e-135"><span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087. Schwerwiegender>: " <fileName><line \#>: Ungültige Status Klausel <clause> für ein Textkonventionen-Makro"**</span><span class="sxs-lookup"><span data-stu-id="0670e-135"><span id="_1087._Fatal_____fileName__line____Invalid_STATUS_clause__clause__for_a_TEXTUAL-CONVENTION_macro_"></span><span id="_1087._fatal_____filename__line____invalid_status_clause__clause__for_a_textual-convention_macro_"></span><span id="_1087._FATAL_____FILENAME__LINE____INVALID_STATUS_CLAUSE__CLAUSE__FOR_A_TEXTUAL-CONVENTION_MACRO_"></span>**<1087. Fatal>: "<fileName><line\#>: Invalid STATUS clause <clause> for a TEXTUAL-CONVENTION macro"**</span></span>
</dt> <dd>

<span data-ttu-id="0670e-136">Typzuweisung, SNMPv2C-spezifischer modulsemantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="0670e-136">Type assignment, SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="0670e-137">Die Status-Klausel eines **Textkonventionen-Makro Aufrufes** muss "Current", "deprecated" oder "deprecated" lauten.</span><span class="sxs-lookup"><span data-stu-id="0670e-137">The status clause of a **TEXTUAL-CONVENTION** macro invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="fatal-error-1089"></a><span data-ttu-id="0670e-138">Schwerwiegender Fehler 1089</span><span class="sxs-lookup"><span data-stu-id="0670e-138">Fatal Error 1089</span></span>

<dl> <dt>

<span data-ttu-id="0670e-139"><span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, schwerwiegender>: " <fileName> : <line \#>: <identifier> das Symbol in der Augments-Klausel wird nicht in einen Row-Objekttyp aufgelöst."**</span><span class="sxs-lookup"><span data-stu-id="0670e-139"><span id="_1089__Fatal_____fileName___line____Symbol__identifier__in_AUGMENTS_clause_does_not_resolve_to_a_row_OBJECT-TYPE_"></span><span id="_1089__fatal_____filename___line____symbol__identifier__in_augments_clause_does_not_resolve_to_a_row_object-type_"></span><span id="_1089__FATAL_____FILENAME___LINE____SYMBOL__IDENTIFIER__IN_AUGMENTS_CLAUSE_DOES_NOT_RESOLVE_TO_A_ROW_OBJECT-TYPE_"></span><**1089, Fatal>: "<fileName>:<line\#>: Symbol <identifier> in AUGMENTS clause does not resolve to a row OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="0670e-140">**Objekttyp-** Makro Aufruf SNMPv2C-spezifischer modulsemantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="0670e-140">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="0670e-141">Wenn eine Erweiterungs Klausel vorhanden ist, muss der Bezeichner in der Augments-Klausel in einen Table-Objekttyp aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="0670e-141">If an AUGMENTS clause is present, then the identifier in the AUGMENTS clause must resolve to a table OBJECT-TYPE.</span></span>

</dd> </dl>

## <a name="fatal-error-1090"></a><span data-ttu-id="0670e-142">Schwerwiegender Fehler 1090</span><span class="sxs-lookup"><span data-stu-id="0670e-142">Fatal Error 1090</span></span>

<dl> <dt>

<span data-ttu-id="0670e-143"><span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090, schwerwiegender>: " <fileName> : <line \#> implizierte Klausel ist nur für das letzte Index Objekt nützlich."**</span><span class="sxs-lookup"><span data-stu-id="0670e-143"><span id="_1090__Fatal_____fileName___line___IMPLIED_clause_is_useful_only_for_the_last_INDEX_object_"></span><span id="_1090__fatal_____filename___line___implied_clause_is_useful_only_for_the_last_index_object_"></span><span id="_1090__FATAL_____FILENAME___LINE___IMPLIED_CLAUSE_IS_USEFUL_ONLY_FOR_THE_LAST_INDEX_OBJECT_"></span>**<1090, Fatal>: "<fileName>:<line\#> IMPLIED clause is useful only for the last INDEX object"**</span></span>
</dt> <dd>

<span data-ttu-id="0670e-144">**Objekttyp-** Makro Aufruf SNMPv2C-spezifischer modulsemantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="0670e-144">**OBJECT-TYPE** macro invocation SNMPv2C-specific module semantic error.</span></span> <span data-ttu-id="0670e-145">Die implizierte Klausel kann nur mit dem letzten Objekt in der Index Klausel verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="0670e-145">The IMPLIED clause can be associated only with the last object in the INDEX clause.</span></span>

</dd> </dl>

 

 



