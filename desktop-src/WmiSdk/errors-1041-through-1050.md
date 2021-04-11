---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1041 bis 1050.
ms.assetid: e7e70fb3-12c6-40b1-91a4-c550e8210c09
ms.tgt_platform: multiple
title: Fehler 1041 bis 1050
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 327ef466d1b1226b14d895fef81be24baee45354
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104042056"
---
# <a name="errors-1041-through-1050"></a><span data-ttu-id="d97a1-103">Fehler 1041 bis 1050</span><span class="sxs-lookup"><span data-stu-id="d97a1-103">Errors 1041 through 1050</span></span>

<span data-ttu-id="d97a1-104">Beschreibt die WMI-SNMP-Anbieter Fehler 1041 bis 1050.</span><span class="sxs-lookup"><span data-stu-id="d97a1-104">Describes WMI SNMP provider errors 1041 through 1050.</span></span>

[<span data-ttu-id="d97a1-105">Schwerwiegender Fehler 1041</span><span class="sxs-lookup"><span data-stu-id="d97a1-105">Fatal Error 1041</span></span>](#fatal-error-1041)

[<span data-ttu-id="d97a1-106">Schwerwiegender Fehler 1042</span><span class="sxs-lookup"><span data-stu-id="d97a1-106">Fatal Error 1042</span></span>](#fatal-error-1042)

[<span data-ttu-id="d97a1-107">Warnung 1043</span><span class="sxs-lookup"><span data-stu-id="d97a1-107">Warning 1043</span></span>](#warning-1043)

[<span data-ttu-id="d97a1-108">Schwerwiegender Fehler 1044</span><span class="sxs-lookup"><span data-stu-id="d97a1-108">Fatal Error 1044</span></span>](#fatal-error-1044)

[<span data-ttu-id="d97a1-109">Warnung 1045</span><span class="sxs-lookup"><span data-stu-id="d97a1-109">Warning 1045</span></span>](#warning-1045)

[<span data-ttu-id="d97a1-110">Warnung 1046</span><span class="sxs-lookup"><span data-stu-id="d97a1-110">Warning 1046</span></span>](#warning-1046)

[<span data-ttu-id="d97a1-111">Warnung 1047</span><span class="sxs-lookup"><span data-stu-id="d97a1-111">Warning 1047</span></span>](#warning-1047)

[<span data-ttu-id="d97a1-112">Warnung 1048</span><span class="sxs-lookup"><span data-stu-id="d97a1-112">Warning 1048</span></span>](#warning-1048)

[<span data-ttu-id="d97a1-113">Schwerwiegender Fehler 1049</span><span class="sxs-lookup"><span data-stu-id="d97a1-113">Fatal Error 1049</span></span>](#fatal-error-1049)

## <a name="fatal-error-1041"></a><span data-ttu-id="d97a1-114">Schwerwiegender Fehler 1041</span><span class="sxs-lookup"><span data-stu-id="d97a1-114">Fatal Error 1041</span></span>

<dl> <dt>

<span data-ttu-id="d97a1-115"><span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041, schwerwiegender>: " <fileName><line \#>: Bezeichner <identifier> in Bereichs Spezifikation wird nicht in einen integralen Wert aufgelöst"**</span><span class="sxs-lookup"><span data-stu-id="d97a1-115"><span id="_1041__Fatal_____fileName__line____Identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__fatal_____filename__line____identifier__identifier__in_range_specification_does_not_resolve_to_an_integral_value_"></span><span id="_1041__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_RANGE_SPECIFICATION_DOES_NOT_RESOLVE_TO_AN_INTEGRAL_VALUE_"></span>**<1041, Fatal>: "<fileName><line\#>: Identifier <identifier> in range specification does not resolve to an integral value"**</span></span>
</dt> <dd>

<span data-ttu-id="d97a1-116">Modul Semantik Fehler in Bereichs-oder Größenangabe, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d97a1-116">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d97a1-117">Das in einer Größenangabe verwendete Symbol muss in eine Oktett-Zeichenfolge oder eine nicht transparente Zeichenfolge aufgelöst werden</span><span class="sxs-lookup"><span data-stu-id="d97a1-117">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="d97a1-118">Jeder Wert, der zum Angeben eines Bereichs verwendet wird, muss eine ganze Zahl sein.</span><span class="sxs-lookup"><span data-stu-id="d97a1-118">Any value used in specifying a range must be an integer.</span></span>

</dd> </dl>

## <a name="fatal-error-1042"></a><span data-ttu-id="d97a1-119">Schwerwiegender Fehler 1042</span><span class="sxs-lookup"><span data-stu-id="d97a1-119">Fatal Error 1042</span></span>

<dl> <dt>

<span data-ttu-id="d97a1-120"><span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042, schwerwiegender>: " <fileName><line \#>: obere Grenze der Bereichs Spezifikation ist kleiner als die untere Grenze"**</span><span class="sxs-lookup"><span data-stu-id="d97a1-120"><span id="_1042__Fatal_____fileName__line____Upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__fatal_____filename__line____upper_bound_of_range_specification_is_less_than_the_lower_bound_"></span><span id="_1042__FATAL_____FILENAME__LINE____UPPER_BOUND_OF_RANGE_SPECIFICATION_IS_LESS_THAN_THE_LOWER_BOUND_"></span>**<1042, Fatal>: "<fileName><line\#>: Upper bound of range specification is less than the lower bound"**</span></span>
</dt> <dd>

<span data-ttu-id="d97a1-121">Modul Semantik Fehler in Bereichs-oder Größenangabe, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d97a1-121">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d97a1-122">Das in einer Größenangabe verwendete Symbol muss in eine Oktett-Zeichenfolge oder eine nicht transparente Zeichenfolge aufgelöst werden</span><span class="sxs-lookup"><span data-stu-id="d97a1-122">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span> <span data-ttu-id="d97a1-123">Die untere Grenze einer Bereichs-oder Größenangabe darf nicht größer als die obere Grenze sein.</span><span class="sxs-lookup"><span data-stu-id="d97a1-123">The lower bound of a range or SIZE specification must be no greater than the upper bound.</span></span>

</dd> </dl>

## <a name="warning-1043"></a><span data-ttu-id="d97a1-124">Warnung 1043</span><span class="sxs-lookup"><span data-stu-id="d97a1-124">Warning 1043</span></span>

<dl> <dt>

<span data-ttu-id="d97a1-125"><span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, Warning>: " <fileName> : <line \#>: Objekttyp mit der Syntax" Sequence ", sollte über eine Access-Klausel verfügen, auf die nicht zugegriffen werden kann.**</span><span class="sxs-lookup"><span data-stu-id="d97a1-125"><span id="_1043__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1043__warning_____filename___line____object-type_with_syntax__sequence___should_have_an_access_clause__not-accessible_"></span><span id="_1043__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span>**<1043, Warning>: "<fileName>:<line\#>: OBJECT-TYPE with SYNTAX "SEQUENCE", should have an ACCESS clause "not-accessible"**</span></span>
</dt> <dd>

<span data-ttu-id="d97a1-126">Semantik Warnung für **Objekttyp-** Makro Aufruf Modul.</span><span class="sxs-lookup"><span data-stu-id="d97a1-126">**OBJECT-TYPE** macro invocation module semantic warning.</span></span> <span data-ttu-id="d97a1-127">Eine Tabelle oder konzeptionelle Zeile (Sequenz von bzw. Sequenz Objekttypen) muss "nicht zugänglich" sein.</span><span class="sxs-lookup"><span data-stu-id="d97a1-127">A table or conceptual row (SEQUENCE OF or SEQUENCE object types, respectively) must be "not-accessible."</span></span>

<span data-ttu-id="d97a1-128">Diese Warnung kann entweder in SNMPv1 oder SNMPv2C auftreten.</span><span class="sxs-lookup"><span data-stu-id="d97a1-128">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1044"></a><span data-ttu-id="d97a1-129">Schwerwiegender Fehler 1044</span><span class="sxs-lookup"><span data-stu-id="d97a1-129">Fatal Error 1044</span></span>

<dl> <dt>

<span data-ttu-id="d97a1-130"><span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044, schwerwiegender>: " <fileName><line \#>: Neudefinition des Symbols <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="d97a1-130"><span id="_1044__Fatal_____fileName__line____Redefinition_of_symbol__identifier__"></span><span id="_1044__fatal_____filename__line____redefinition_of_symbol__identifier__"></span><span id="_1044__FATAL_____FILENAME__LINE____REDEFINITION_OF_SYMBOL__IDENTIFIER__"></span>**<1044, Fatal>: "<fileName><line\#>: Redefinition of symbol <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="d97a1-131">Modul Semantik Fehler, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d97a1-131">Module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d97a1-132">Neudefinition von Objekt Deskriptoren, Makro aufrufen und ASN. 1-Typen führt zu einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="d97a1-132">Redefinition of object descriptors, macro invocations, and ASN.1 types cause an error.</span></span>

</dd> </dl>

## <a name="warning-1045"></a><span data-ttu-id="d97a1-133">Warnung 1045</span><span class="sxs-lookup"><span data-stu-id="d97a1-133">Warning 1045</span></span>

<dl> <dt>

<span data-ttu-id="d97a1-134"><span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, Warning>: " <fileName><linereferenzierung zum Standard Symbol <symbolName> wird für die Definition als in angenommen <moduleName> . Verwenden Sie die "Module. Symbol"-Notationen, wenn Sie auf die Definition im aktuellen Modul verweisen möchten.**</span><span class="sxs-lookup"><span data-stu-id="d97a1-134"><span id="_1045__Warning_____fileName__lineReference_to_standard_symbol__symbolName__assumed_to_be_for_the_definition_as_in__moduleName_._Use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__warning_____filename__linereference_to_standard_symbol__symbolname__assumed_to_be_for_the_definition_as_in__modulename_._use_the__module.symbol__notations__if_you_want_to_refer_to_the_definition_in_the_current_module_"></span><span id="_1045__WARNING_____FILENAME__LINEREFERENCE_TO_STANDARD_SYMBOL__SYMBOLNAME__ASSUMED_TO_BE_FOR_THE_DEFINITION_AS_IN__MODULENAME_._USE_THE__MODULE.SYMBOL__NOTATIONS__IF_YOU_WANT_TO_REFER_TO_THE_DEFINITION_IN_THE_CURRENT_MODULE_"></span>**<1045, Warning>: "<fileName><lineReference to standard symbol <symbolName> assumed to be for the definition as in <moduleName>. Use the "module.symbol" notations, if you want to refer to the definition in the current module"**</span></span>
</dt> <dd>

<span data-ttu-id="d97a1-135">Modul Semantik Warnung, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d97a1-135">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d97a1-136">Ein Symbol, das dem Compiler bekannt ist, wurde neu definiert, und es wird darauf verwiesen.</span><span class="sxs-lookup"><span data-stu-id="d97a1-136">A symbol known to the compiler has been redefined, and is being referenced.</span></span> <span data-ttu-id="d97a1-137">Der Compiler nimmt die Standard Definition des Symbols an.</span><span class="sxs-lookup"><span data-stu-id="d97a1-137">The compiler assumes the standard definition of the symbol.</span></span> <span data-ttu-id="d97a1-138">Daher müssen Sie die Notation "Module. Symbol" verwenden, um eine Neudefinition des Standard Symbols zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="d97a1-138">Therefore, to use a redefinition of the standard symbol, you must use the "Module.Symbol" notation.</span></span>

</dd> </dl>

## <a name="warning-1046"></a><span data-ttu-id="d97a1-139">Warnung 1046</span><span class="sxs-lookup"><span data-stu-id="d97a1-139">Warning 1046</span></span>

<dl> <dt>

<span data-ttu-id="d97a1-140"><span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, Warnung>: " <fileName><Zeilen \#>: nicht <symbol> definiert. Annahme der Standard Definition "**</span><span class="sxs-lookup"><span data-stu-id="d97a1-140"><span id="_1046__Warning_____fileName__line_____symbol__undefined._Assuming_standard_definition_"></span><span id="_1046__warning_____filename__line_____symbol__undefined._assuming_standard_definition_"></span><span id="_1046__WARNING_____FILENAME__LINE_____SYMBOL__UNDEFINED._ASSUMING_STANDARD_DEFINITION_"></span>**<1046, Warning>: "<fileName><line\#>: <symbol> undefined. Assuming standard definition"**</span></span>
</dt> <dd>

<span data-ttu-id="d97a1-141">Modul Semantik Warnung, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d97a1-141">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d97a1-142">Ein Symbol, das dem Compiler bekannt ist, darf nicht neu definiert oder verwendet werden, ohne importiert zu werden.</span><span class="sxs-lookup"><span data-stu-id="d97a1-142">A symbol known to the compiler must not be redefined or used without being imported.</span></span>

</dd> </dl>

## <a name="warning-1047"></a><span data-ttu-id="d97a1-143">Warnung 1047</span><span class="sxs-lookup"><span data-stu-id="d97a1-143">Warning 1047</span></span>

<dl> <dt>

<span data-ttu-id="d97a1-144"><span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, Warning>: " <fileName><line \#>: Typdefinition <symbol> definiert, aber nicht referenziert"**</span><span class="sxs-lookup"><span data-stu-id="d97a1-144"><span id="_1047__Warning_____fileName__line____Type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__warning_____filename__line____type_definition__symbol__defined_but_not_referenced_"></span><span id="_1047__WARNING_____FILENAME__LINE____TYPE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1047, Warning>: "<fileName><line\#>: Type definition <symbol> defined but not referenced"**</span></span>
</dt> <dd>

<span data-ttu-id="d97a1-145">Modul Semantik Warnung, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d97a1-145">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d97a1-146">Auf alle Wert Zuweisungen und Typdefinitionen muss irgendwo verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d97a1-146">All value assignments and type definitions must be referenced somewhere.</span></span>

</dd> </dl>

## <a name="warning-1048"></a><span data-ttu-id="d97a1-147">Warnung 1048</span><span class="sxs-lookup"><span data-stu-id="d97a1-147">Warning 1048</span></span>

<dl> <dt>

<span data-ttu-id="d97a1-148"><span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, Warning>: " <fileName><line \#>: Definition von Werten <symbol> definiert, aber nicht referenziert"**</span><span class="sxs-lookup"><span data-stu-id="d97a1-148"><span id="_1048__Warning_____fileName__line____Value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__warning_____filename__line____value_definition__symbol__defined_but_not_referenced_"></span><span id="_1048__WARNING_____FILENAME__LINE____VALUE_DEFINITION__SYMBOL__DEFINED_BUT_NOT_REFERENCED_"></span>**<1048, Warning>: "<fileName><line\#>: Value definition <symbol> defined but not referenced"**</span></span>
</dt> <dd>

<span data-ttu-id="d97a1-149">Modul Semantik Warnung, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="d97a1-149">Module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="d97a1-150">Auf alle Wert Zuweisungen und Typdefinitionen muss irgendwo verwiesen werden.</span><span class="sxs-lookup"><span data-stu-id="d97a1-150">All value assignments and type definitions must be referenced somewhere.</span></span>

</dd> </dl>

## <a name="fatal-error-1049"></a><span data-ttu-id="d97a1-151">Schwerwiegender Fehler 1049</span><span class="sxs-lookup"><span data-stu-id="d97a1-151">Fatal Error 1049</span></span>

<dl> <dt>

<span data-ttu-id="d97a1-152"><span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, schwerwiegender>: " <fileName> : <line \#>: defval-Klausel für Objekttyp mit Syntax Network Address" nicht zulässig.**</span><span class="sxs-lookup"><span data-stu-id="d97a1-152"><span id="_1049__Fatal_____fileName___line____DEFVAL_clause_not_allowed_for_OBJECT-TYPE_with_SYNTAX_NetworkAddress_"></span><span id="_1049__fatal_____filename___line____defval_clause_not_allowed_for_object-type_with_syntax_networkaddress_"></span><span id="_1049__FATAL_____FILENAME___LINE____DEFVAL_CLAUSE_NOT_ALLOWED_FOR_OBJECT-TYPE_WITH_SYNTAX_NETWORKADDRESS_"></span>**<1049, Fatal>: "<fileName>:<line\#>: DEFVAL clause not allowed for OBJECT-TYPE with SYNTAX NetworkAddress"**</span></span>
</dt> <dd>

<span data-ttu-id="d97a1-153">**Objekttyp-** Makro Aufruf SNMPv1-spezifischer modulsemantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="d97a1-153">**OBJECT-TYPE** macro invocation SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="d97a1-154">Die defval-Klausel ist für einen Objekttyp, dessen Syntax Klausel in Network Address aufgelöst wird, nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="d97a1-154">The DEFVAL clause is not allowed for an OBJECT-TYPE whose SYNTAX clause resolves to NetworkAddress.</span></span>

</dd> </dl>

 

 



