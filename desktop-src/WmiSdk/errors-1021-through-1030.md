---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1021 bis 1033.
ms.assetid: fc638d0f-20f4-46d0-a36a-c3898415f35c
ms.tgt_platform: multiple
title: Fehler 1021 bis 1030
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f8bce9c7c4d70250fa63ad0100cf93c8d5b26984
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347095"
---
# <a name="errors-1021-through-1030"></a><span data-ttu-id="858b3-103">Fehler 1021 bis 1030</span><span class="sxs-lookup"><span data-stu-id="858b3-103">Errors 1021 through 1030</span></span>

<span data-ttu-id="858b3-104">Beschreibt die WMI-SNMP-Anbieter Fehler 1021 bis 1033.</span><span class="sxs-lookup"><span data-stu-id="858b3-104">Describes WMI SNMP provider errors 1021 through 1033.</span></span>

[<span data-ttu-id="858b3-105">Schwerwiegender Fehler 1021</span><span class="sxs-lookup"><span data-stu-id="858b3-105">Fatal Error 1021</span></span>](#fatal-error-1021)

[<span data-ttu-id="858b3-106">Schwerwiegender Fehler 1022</span><span class="sxs-lookup"><span data-stu-id="858b3-106">Fatal Error 1022</span></span>](#fatal-error-1022)

[<span data-ttu-id="858b3-107">Schwerwiegender Fehler 1023</span><span class="sxs-lookup"><span data-stu-id="858b3-107">Fatal Error 1023</span></span>](#fatal-error-1023)

[<span data-ttu-id="858b3-108">Schwerwiegender Fehler 1024</span><span class="sxs-lookup"><span data-stu-id="858b3-108">Fatal Error 1024</span></span>](#fatal-error-1024)

[<span data-ttu-id="858b3-109">Schwerwiegender Fehler 1025</span><span class="sxs-lookup"><span data-stu-id="858b3-109">Fatal Error 1025</span></span>](#fatal-error-1025)

[<span data-ttu-id="858b3-110">Schwerwiegender Fehler 1026</span><span class="sxs-lookup"><span data-stu-id="858b3-110">Fatal Error 1026</span></span>](#fatal-error-1026)

[<span data-ttu-id="858b3-111">Warnung 1027</span><span class="sxs-lookup"><span data-stu-id="858b3-111">Warning 1027</span></span>](#warning-1027)

[<span data-ttu-id="858b3-112">Schwerwiegender Fehler 1028</span><span class="sxs-lookup"><span data-stu-id="858b3-112">Fatal Error 1028</span></span>](#fatal-error-1028)

[<span data-ttu-id="858b3-113">Schwerwiegender Fehler 1029</span><span class="sxs-lookup"><span data-stu-id="858b3-113">Fatal Error 1029</span></span>](#fatal-error-1029)

[<span data-ttu-id="858b3-114">Schwerwiegender Fehler 1030</span><span class="sxs-lookup"><span data-stu-id="858b3-114">Fatal Error 1030</span></span>](#fatal-error-1030)

## <a name="fatal-error-1021"></a><span data-ttu-id="858b3-115">Schwerwiegender Fehler 1021</span><span class="sxs-lookup"><span data-stu-id="858b3-115">Fatal Error 1021</span></span>

<dl> <dt>

<span data-ttu-id="858b3-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, schwerwiegender>: " <fileName><line \#>: der <identifier> Bezeichner in der Variables-Klausel von Trap-Type wird nicht in einen skalaren Objekttyp aufgelöst."**</span><span class="sxs-lookup"><span data-stu-id="858b3-116"><span id="_1021__Fatal_____fileName__line____Identifier__identifier__in_the_VARIABLES_clause_of_TRAP-TYPE_does_not_resolve_to_a_scalar_OBJECT-TYPE_"></span><span id="_1021__fatal_____filename__line____identifier__identifier__in_the_variables_clause_of_trap-type_does_not_resolve_to_a_scalar_object-type_"></span><span id="_1021__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_THE_VARIABLES_CLAUSE_OF_TRAP-TYPE_DOES_NOT_RESOLVE_TO_A_SCALAR_OBJECT-TYPE_"></span>**<1021, Fatal>: "<fileName><line\#>: Identifier <identifier> in the VARIABLES clause of TRAP-TYPE does not resolve to a scalar OBJECT-TYPE"**</span></span>
</dt> <dd>

<span data-ttu-id="858b3-117">**Trap-Type-** Makro Aufruf, SNMPv1-spezifischer Modul Semantik Fehler.</span><span class="sxs-lookup"><span data-stu-id="858b3-117">**TRAP-TYPE** macro invocation, SNMPv1-specific module semantic error.</span></span> <span data-ttu-id="858b3-118">Jedes Element in der Liste der Variablen, das in der Variables-Klausel eines **Trap-Type-** Makro Aufrufs verwendet wird, muss in den Namen einer Instanz des skalaren Objekt Typs aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="858b3-118">Each item in the list of variables used in the VARIABLES clause of a **TRAP-TYPE** macro invocation must resolve to the name of a scalar OBJECT-TYPE instance.</span></span>

</dd> </dl>

## <a name="fatal-error-1022"></a><span data-ttu-id="858b3-119">Schwerwiegender Fehler 1022</span><span class="sxs-lookup"><span data-stu-id="858b3-119">Fatal Error 1022</span></span>

<dl> <dt>

<span data-ttu-id="858b3-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, schwerwiegender>: " <fileName><line \#>: Wert wird nicht in Typ aufgelöst <type> "**</span><span class="sxs-lookup"><span data-stu-id="858b3-120"><span id="_1022__Fatal_____fileName__line____Value_does_not_resolve_to_type__type__"></span><span id="_1022__fatal_____filename__line____value_does_not_resolve_to_type__type__"></span><span id="_1022__FATAL_____FILENAME__LINE____VALUE_DOES_NOT_RESOLVE_TO_TYPE__TYPE__"></span>**<1022, Fatal>: "<fileName><line\#>: Value does not resolve to type <type>"**</span></span>
</dt> <dd>

<span data-ttu-id="858b3-121">Semantik Fehler des Wert Zuweisungs Moduls, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="858b3-121">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="858b3-122">Der Wert für die RHS einer Ganzzahl, **null**, Oktett-Zeichenfolge oder Objekt-ID-Wert Zuweisung weist den falschen Typ auf.</span><span class="sxs-lookup"><span data-stu-id="858b3-122">The value on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment is of the wrong type.</span></span>

</dd> </dl>

## <a name="fatal-error-1023"></a><span data-ttu-id="858b3-123">Schwerwiegender Fehler 1023</span><span class="sxs-lookup"><span data-stu-id="858b3-123">Fatal Error 1023</span></span>

<dl> <dt>

<span data-ttu-id="858b3-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, schwerwiegender>: " <fileName><line \#>: Bezeichner <identifier> wird nicht in den Typ aufgelöst <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="858b3-124"><span id="_1023__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__fatal_____filename__line____identifier__identifier__does_not_resolve_to_the_type__identifier__"></span><span id="_1023__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_THE_TYPE__IDENTIFIER__"></span>**<1023, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to the type <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="858b3-125">Semantik Fehler des Wert Zuweisungs Moduls, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="858b3-125">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="858b3-126">Ein Symbol (Werte Verweis) für die RHS einer Ganzzahl, **null**, Oktett-Zeichenfolge oder Objekt-ID-Wert Zuweisung wird nicht in den richtigen Typ aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="858b3-126">A symbol (value reference) on the RHS of an INTEGER, **NULL**, OCTET STRING, or OBJECT IDENTIFIER value assignment does not resolve to the right type.</span></span>

</dd> </dl>

## <a name="fatal-error-1024"></a><span data-ttu-id="858b3-127">Schwerwiegender Fehler 1024</span><span class="sxs-lookup"><span data-stu-id="858b3-127">Fatal Error 1024</span></span>

<dl> <dt>

<span data-ttu-id="858b3-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, schwerwiegender>: " <fileName><line \#>: negative Ganzzahl in OID-Werte Definition"**</span><span class="sxs-lookup"><span data-stu-id="858b3-128"><span id="_1024__Fatal_____fileName__line____Negative_integer_in_OID_value_definition_"></span><span id="_1024__fatal_____filename__line____negative_integer_in_oid_value_definition_"></span><span id="_1024__FATAL_____FILENAME__LINE____NEGATIVE_INTEGER_IN_OID_VALUE_DEFINITION_"></span>**<1024, Fatal>: "<fileName><line\#>: Negative integer in OID value definition"**</span></span>
</dt> <dd>

<span data-ttu-id="858b3-129">Semantik Fehler des Wert Zuweisungs Moduls, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="858b3-129">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="858b3-130">Alle Werte in einer OID-Komponentenliste müssen nicht negative (vorzugsweise positive) ganze Zahlen sein.</span><span class="sxs-lookup"><span data-stu-id="858b3-130">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1025"></a><span data-ttu-id="858b3-131">Schwerwiegender Fehler 1025</span><span class="sxs-lookup"><span data-stu-id="858b3-131">Fatal Error 1025</span></span>

<dl> <dt>

<span data-ttu-id="858b3-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, schwerwiegender>: "Bezeichner <identifier> in OID-Wert wird nicht in eine positive ganze Zahl aufgelöst"**</span><span class="sxs-lookup"><span data-stu-id="858b3-132"><span id="_1025__Fatal____Identifier__identifier__in_OID_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__fatal____identifier__identifier__in_oid_value_does_not_resolve_to_a_positive_integer_"></span><span id="_1025__FATAL____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1025, Fatal>: "Identifier <identifier> in OID value does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="858b3-133">Semantik Fehler des Wert Zuweisungs Moduls, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="858b3-133">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="858b3-134">Alle Werte in einer OID-Komponentenliste müssen nicht negative (vorzugsweise positive) ganze Zahlen sein.</span><span class="sxs-lookup"><span data-stu-id="858b3-134">All values in an OID component list must be non-negative (preferably positive) integers.</span></span>

</dd> </dl>

## <a name="fatal-error-1026"></a><span data-ttu-id="858b3-135">Schwerwiegender Fehler 1026</span><span class="sxs-lookup"><span data-stu-id="858b3-135">Fatal Error 1026</span></span>

<dl> <dt>

<span data-ttu-id="858b3-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, schwerwiegender>: " <fileName><line \#>: der Bezeichner <identifier> in OID-Wert wird weder in einen OID-Wert noch in eine positive ganze Zahl aufgelöst"**</span><span class="sxs-lookup"><span data-stu-id="858b3-136"><span id="_1026__Fatal_____fileName__line____Identifier__identifier__in_OID_value_neither_resolves_to_an_OID_value_nor_a_positive_integer_"></span><span id="_1026__fatal_____filename__line____identifier__identifier__in_oid_value_neither_resolves_to_an_oid_value_nor_a_positive_integer_"></span><span id="_1026__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_OID_VALUE_NEITHER_RESOLVES_TO_AN_OID_VALUE_NOR_A_POSITIVE_INTEGER_"></span>**<1026, Fatal>: "<fileName><line\#>: Identifier <identifier> in OID value neither resolves to an OID value nor a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="858b3-137">Semantik Fehler des Wert Zuweisungs Moduls, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="858b3-137">Value assignment module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="858b3-138">Die erste Komponente, die in einem OID-Wert verwendet wird, muss in einen OID-oder eine ganze Zahl aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="858b3-138">The first component used in an OID value must resolve to an OID value or an INTEGER.</span></span>

</dd> </dl>

## <a name="warning-1027"></a><span data-ttu-id="858b3-139">Warnung 1027</span><span class="sxs-lookup"><span data-stu-id="858b3-139">Warning 1027</span></span>

<dl> <dt>

<span data-ttu-id="858b3-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, Warning>: " <fileName><line \#>: importiertes Symbol nicht <identifier> verwendet."**</span><span class="sxs-lookup"><span data-stu-id="858b3-140"><span id="_1027__Warning_____fileName__line____Imported_symbol__identifier__unused_"></span><span id="_1027__warning_____filename__line____imported_symbol__identifier__unused_"></span><span id="_1027__WARNING_____FILENAME__LINE____IMPORTED_SYMBOL__IDENTIFIER__UNUSED_"></span>**<1027, Warning>: "<fileName><line\#>: Imported symbol <identifier> unused"**</span></span>
</dt> <dd>

<span data-ttu-id="858b3-141">Gibt eine Semantik Warnung für das Abschnitts Modul aus, die spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="858b3-141">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="858b3-142">Für jedes nicht verwendete importierte Symbol wird eine Warnung ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="858b3-142">A warning is issued for every unused imported symbol.</span></span>

</dd> </dl>

## <a name="fatal-error-1028"></a><span data-ttu-id="858b3-143">Schwerwiegender Fehler 1028</span><span class="sxs-lookup"><span data-stu-id="858b3-143">Fatal Error 1028</span></span>

<dl> <dt>

<span data-ttu-id="858b3-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, schwerwiegender>: "Modul wurde <identifier> nicht in den Imports-Abschnitt importiert"**</span><span class="sxs-lookup"><span data-stu-id="858b3-144"><span id="_1028__Fatal____Module__identifier__not_imported_in_the_IMPORTS_section_"></span><span id="_1028__fatal____module__identifier__not_imported_in_the_imports_section_"></span><span id="_1028__FATAL____MODULE__IDENTIFIER__NOT_IMPORTED_IN_THE_IMPORTS_SECTION_"></span>**<1028, Fatal>: "Module <identifier> not imported in the IMPORTS section"**</span></span>
</dt> <dd>

<span data-ttu-id="858b3-145">Der Code für die Modul Semantik der Importe ist spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="858b3-145">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="858b3-146">Ein Modulname, der zum Verweisen auf ein Symbol verwendet wird, muss entweder in der Imports-Klausel vorhanden sein oder der Name des aktuellen Moduls sein.</span><span class="sxs-lookup"><span data-stu-id="858b3-146">A module name used in referencing a symbol must either be present in the IMPORTS clause, or be the name of the current module.</span></span>

</dd> </dl>

## <a name="fatal-error-1029"></a><span data-ttu-id="858b3-147">Schwerwiegender Fehler 1029</span><span class="sxs-lookup"><span data-stu-id="858b3-147">Fatal Error 1029</span></span>

<dl> <dt>

<span data-ttu-id="858b3-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, schwerwiegender>: " <fileName><line \#>: das aktuelle Modul <identifier> kann nicht importiert werden"**</span><span class="sxs-lookup"><span data-stu-id="858b3-148"><span id="_1029__Fatal_____fileName__line____Current_module__identifier__cannot_be_imported_"></span><span id="_1029__fatal_____filename__line____current_module__identifier__cannot_be_imported_"></span><span id="_1029__FATAL_____FILENAME__LINE____CURRENT_MODULE__IDENTIFIER__CANNOT_BE_IMPORTED_"></span>**<1029, Fatal>: "<fileName><line\#>: Current module <identifier> cannot be imported"**</span></span>
</dt> <dd>

<span data-ttu-id="858b3-149">Der Code für die Modul Semantik der Importe ist spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="858b3-149">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="858b3-150">Der Name des aktuellen Moduls ist auch in der Liste der Importe enthalten.</span><span class="sxs-lookup"><span data-stu-id="858b3-150">The name of the current module also figures in the IMPORTS list.</span></span>

</dd> </dl>

## <a name="fatal-error-1030"></a><span data-ttu-id="858b3-151">Schwerwiegender Fehler 1030</span><span class="sxs-lookup"><span data-stu-id="858b3-151">Fatal Error 1030</span></span>

<dl> <dt>

<span data-ttu-id="858b3-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, schwerwiegender>: " <fileName><line \#>: Symbol <identifier> nicht aus Modul importiert <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="858b3-152"><span id="_1030__Fatal____fileName__line____Symbol__identifier__not_imported_from_Module__identifier__"></span><span id="_1030__fatal____filename__line____symbol__identifier__not_imported_from_module__identifier__"></span><span id="_1030__FATAL____FILENAME__LINE____SYMBOL__IDENTIFIER__NOT_IMPORTED_FROM_MODULE__IDENTIFIER__"></span>**<1030, Fatal>:"<fileName><line\#>: Symbol <identifier> not imported from Module <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="858b3-153">Der Code für die Modul Semantik der Importe ist spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="858b3-153">IMPORTS section module semantic error, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="858b3-154">Sie haben die Notation "Module. Symbol" verwendet, aber das Symbol wurde nicht aus dem angegebenen Modul im Abschnitt Imports importiert.</span><span class="sxs-lookup"><span data-stu-id="858b3-154">You have used the "Module.Symbol" notation, but the symbol has not been imported from the specified module in the IMPORTS section.</span></span>

</dd> </dl>

 

 



