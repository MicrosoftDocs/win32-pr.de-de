---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1001 bis 1010.
ms.assetid: dbc0e062-6b2f-41b1-8d6a-ab2c37d2dd1f
ms.tgt_platform: multiple
title: Fehler 1001 bis 1010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa10b83c660d617bdbf37b6f119e824bbba60616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348063"
---
# <a name="errors-1001-through-1010"></a><span data-ttu-id="2b780-103">Fehler 1001 bis 1010</span><span class="sxs-lookup"><span data-stu-id="2b780-103">Errors 1001 through 1010</span></span>

<span data-ttu-id="2b780-104">Beschreibt die WMI-SNMP-Anbieter Fehler 1001 bis 1010.</span><span class="sxs-lookup"><span data-stu-id="2b780-104">Describes WMI SNMP provider errors 1001 through 1010.</span></span>

[<span data-ttu-id="2b780-105">Schwerwiegender Fehler 1001</span><span class="sxs-lookup"><span data-stu-id="2b780-105">Fatal Error 1001</span></span>](#fatal-error-1001)

[<span data-ttu-id="2b780-106">Schwerwiegender Fehler 1002</span><span class="sxs-lookup"><span data-stu-id="2b780-106">Fatal Error 1002</span></span>](#fatal-error-1002)

[<span data-ttu-id="2b780-107">Schwerwiegender Fehler 1003</span><span class="sxs-lookup"><span data-stu-id="2b780-107">Fatal Error 1003</span></span>](#fatal-error-1003)

[<span data-ttu-id="2b780-108">Warnung 1004</span><span class="sxs-lookup"><span data-stu-id="2b780-108">Warning 1004</span></span>](#warning-1004)

[<span data-ttu-id="2b780-109">Warnung 1005</span><span class="sxs-lookup"><span data-stu-id="2b780-109">Warning 1005</span></span>](#warning-1005)

[<span data-ttu-id="2b780-110">Schwerwiegender Fehler 1006</span><span class="sxs-lookup"><span data-stu-id="2b780-110">Fatal Error 1006</span></span>](#fatal-error-1006)

[<span data-ttu-id="2b780-111">Schwerwiegender Fehler 1008</span><span class="sxs-lookup"><span data-stu-id="2b780-111">Fatal Error 1008</span></span>](#fatal-error-1008)

## <a name="fatal-error-1001"></a><span data-ttu-id="2b780-112">Schwerwiegender Fehler 1001</span><span class="sxs-lookup"><span data-stu-id="2b780-112">Fatal Error 1001</span></span>

<dl> <dt>

<span data-ttu-id="2b780-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, schwerwiegender>: " <fileName> : <line \#>: Syntax Klausel des Objekttyps wird nicht in zulässige Typen aufgelöst"</span><span class="sxs-lookup"><span data-stu-id="2b780-113"><span id="_1001__Fatal_____fileName___line____SYNTAX_clause_of_OBJECT-TYPE_does_not_resolve_to_allowed_types_"></span><span id="_1001__fatal_____filename___line____syntax_clause_of_object-type_does_not_resolve_to_allowed_types_"></span><span id="_1001__FATAL_____FILENAME___LINE____SYNTAX_CLAUSE_OF_OBJECT-TYPE_DOES_NOT_RESOLVE_TO_ALLOWED_TYPES_"></span><1001, Fatal>: "<fileName>:<line\#>: SYNTAX clause of OBJECT-TYPE does not resolve to allowed types"</span></span>
</dt> <dd>

<span data-ttu-id="2b780-114">Semantik Fehler des Objekttyp-Makro Aufruf Moduls.</span><span class="sxs-lookup"><span data-stu-id="2b780-114">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="2b780-115">Die Syntax Klausel des Objekttyp Makros muss in einen Typ oder einen Untertyp aufgelöst werden, der mit der Größen-oder Bereichs Spezifikation, die das SNMPv1-oder SNMPv2C SMI zulässt, gebildet wird.</span><span class="sxs-lookup"><span data-stu-id="2b780-115">The SYNTAX clause of the OBJECT-TYPE macro must resolve to a type or subtype, formed by using the SIZE or range specification that the SNMPv1 or SNMPv2C SMI allows.</span></span> <span data-ttu-id="2b780-116">Wenn dies nicht der Fall ist, wird ein schwerwiegender Fehler 1001 gemeldet.</span><span class="sxs-lookup"><span data-stu-id="2b780-116">If this is not the case, fatal error 1001 is reported.</span></span>

<span data-ttu-id="2b780-117">Dieser Fehler kann auftreten, wenn ein SNMPv1-oder SNMPv2C-MIB kompiliert wird.</span><span class="sxs-lookup"><span data-stu-id="2b780-117">This error can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

<span data-ttu-id="2b780-118">Die SNMPv1 SMI erlaubt folgende Typen:</span><span class="sxs-lookup"><span data-stu-id="2b780-118">Types allowed by the SNMPv1 SMI are:</span></span>

-   <span data-ttu-id="2b780-119">INTEGER</span><span class="sxs-lookup"><span data-stu-id="2b780-119">INTEGER</span></span>
-   <span data-ttu-id="2b780-120">NULL</span><span class="sxs-lookup"><span data-stu-id="2b780-120">NULL</span></span>
-   <span data-ttu-id="2b780-121">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b780-121">OCTET STRING</span></span>
-   <span data-ttu-id="2b780-122">Objekt Bezeichner</span><span class="sxs-lookup"><span data-stu-id="2b780-122">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="2b780-123">NetworkAddress</span><span class="sxs-lookup"><span data-stu-id="2b780-123">NetworkAddress</span></span>
-   <span data-ttu-id="2b780-124">IpAddress</span><span class="sxs-lookup"><span data-stu-id="2b780-124">IpAddress</span></span>
-   <span data-ttu-id="2b780-125">Zähler</span><span class="sxs-lookup"><span data-stu-id="2b780-125">Counter</span></span>
-   <span data-ttu-id="2b780-126">Maßstab</span><span class="sxs-lookup"><span data-stu-id="2b780-126">Gauge</span></span>
-   <span data-ttu-id="2b780-127">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="2b780-127">TimeTicks</span></span>
-   <span data-ttu-id="2b780-128">Nicht transparent</span><span class="sxs-lookup"><span data-stu-id="2b780-128">Opaque</span></span>
-   <span data-ttu-id="2b780-129">DisplayString</span><span class="sxs-lookup"><span data-stu-id="2b780-129">DisplayString</span></span>
-   <span data-ttu-id="2b780-130">Physaddress</span><span class="sxs-lookup"><span data-stu-id="2b780-130">PhysAddress</span></span>

<span data-ttu-id="2b780-131">Die SNMPv2C SMI erlaubt folgende Typen:</span><span class="sxs-lookup"><span data-stu-id="2b780-131">Types allowed by the SNMPv2C SMI are:</span></span>

-   <span data-ttu-id="2b780-132">INTEGER</span><span class="sxs-lookup"><span data-stu-id="2b780-132">INTEGER</span></span>
-   <span data-ttu-id="2b780-133">Oktett-Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="2b780-133">OCTET STRING</span></span>
-   <span data-ttu-id="2b780-134">Objekt Bezeichner</span><span class="sxs-lookup"><span data-stu-id="2b780-134">OBJECT IDENTIFIER</span></span>
-   <span data-ttu-id="2b780-135">BITS</span><span class="sxs-lookup"><span data-stu-id="2b780-135">BITS</span></span>
-   <span data-ttu-id="2b780-136">Integer32</span><span class="sxs-lookup"><span data-stu-id="2b780-136">Integer32</span></span>
-   <span data-ttu-id="2b780-137">IpAddress</span><span class="sxs-lookup"><span data-stu-id="2b780-137">IpAddress</span></span>
-   <span data-ttu-id="2b780-138">Counter32</span><span class="sxs-lookup"><span data-stu-id="2b780-138">Counter32</span></span>
-   <span data-ttu-id="2b780-139">TimeTicks</span><span class="sxs-lookup"><span data-stu-id="2b780-139">TimeTicks</span></span>
-   <span data-ttu-id="2b780-140">Nicht transparent</span><span class="sxs-lookup"><span data-stu-id="2b780-140">Opaque</span></span>
-   <span data-ttu-id="2b780-141">Counter64</span><span class="sxs-lookup"><span data-stu-id="2b780-141">Counter64</span></span>
-   <span data-ttu-id="2b780-142">Unsigned32</span><span class="sxs-lookup"><span data-stu-id="2b780-142">Unsigned32</span></span>
-   <span data-ttu-id="2b780-143">DisplayString</span><span class="sxs-lookup"><span data-stu-id="2b780-143">DisplayString</span></span>
-   <span data-ttu-id="2b780-144">Physaddress</span><span class="sxs-lookup"><span data-stu-id="2b780-144">PhysAddress</span></span>
-   <span data-ttu-id="2b780-145">MacAddress</span><span class="sxs-lookup"><span data-stu-id="2b780-145">MacAddress</span></span>
-   <span data-ttu-id="2b780-146">Wahrheitswert</span><span class="sxs-lookup"><span data-stu-id="2b780-146">TruthValue</span></span>
-   <span data-ttu-id="2b780-147">Testandincr</span><span class="sxs-lookup"><span data-stu-id="2b780-147">TestAndIncr</span></span>
-   <span data-ttu-id="2b780-148">Autonomoustype</span><span class="sxs-lookup"><span data-stu-id="2b780-148">AutonomousType</span></span>
-   <span data-ttu-id="2b780-149">Instancepointer</span><span class="sxs-lookup"><span data-stu-id="2b780-149">InstancePointer</span></span>
-   <span data-ttu-id="2b780-150">Variablepointer</span><span class="sxs-lookup"><span data-stu-id="2b780-150">VariablePointer</span></span>
-   <span data-ttu-id="2b780-151">Zeilen Zeiger</span><span class="sxs-lookup"><span data-stu-id="2b780-151">RowPointer</span></span>
-   <span data-ttu-id="2b780-152">Rowstatus</span><span class="sxs-lookup"><span data-stu-id="2b780-152">RowStatus</span></span>
-   <span data-ttu-id="2b780-153">TimeStamp</span><span class="sxs-lookup"><span data-stu-id="2b780-153">TimeStamp</span></span>
-   <span data-ttu-id="2b780-154">TimeInterval</span><span class="sxs-lookup"><span data-stu-id="2b780-154">TimeInterval</span></span>
-   <span data-ttu-id="2b780-155">DateAndTime</span><span class="sxs-lookup"><span data-stu-id="2b780-155">DateAndTime</span></span>
-   <span data-ttu-id="2b780-156">StorageType</span><span class="sxs-lookup"><span data-stu-id="2b780-156">StorageType</span></span>
-   <span data-ttu-id="2b780-157">Tdomäne</span><span class="sxs-lookup"><span data-stu-id="2b780-157">Tdomain</span></span>
-   <span data-ttu-id="2b780-158">Taddress</span><span class="sxs-lookup"><span data-stu-id="2b780-158">Taddress</span></span>

</dd> </dl>

## <a name="fatal-error-1002"></a><span data-ttu-id="2b780-159">Schwerwiegender Fehler 1002</span><span class="sxs-lookup"><span data-stu-id="2b780-159">Fatal Error 1002</span></span>

<dl> <dt>

<span data-ttu-id="2b780-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, schwerwiegender>: " <fileName> : <line \#>: Ungültige Zugriffs Klausel <clause> "</span><span class="sxs-lookup"><span data-stu-id="2b780-160"><span id="_1002__Fatal_____fileName___line____Invalid_ACCESS_clause__clause__"></span><span id="_1002__fatal_____filename___line____invalid_access_clause__clause__"></span><span id="_1002__FATAL_____FILENAME___LINE____INVALID_ACCESS_CLAUSE__CLAUSE__"></span><1002, Fatal>: "<fileName>:<line\#>: Invalid ACCESS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="2b780-161">Semantik Fehler des Objekttyp-Makro Aufruf Moduls.</span><span class="sxs-lookup"><span data-stu-id="2b780-161">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="2b780-162">Für SNMPv1 muss die Access-Klausel des Objekttyp Makros "schreibgeschützt", "schreibgeschützt", "Lesen/Schreiben" oder "nicht verfügbar" lauten.</span><span class="sxs-lookup"><span data-stu-id="2b780-162">For SNMPv1, the ACCESS clause of the OBJECT-TYPE macro must be "read-only," "write-only," "read/write," or "not-accessible."</span></span>

<span data-ttu-id="2b780-163">Bei SNMPv2C muss die Max-Access-Klausel "schreibgeschützt", "Lesen/erstellen", "Lesen/Schreiben" oder "nicht verfügbar" lauten.</span><span class="sxs-lookup"><span data-stu-id="2b780-163">For SNMPv2C, the MAX-ACCESS clause must be "read-only," "read-create," "read/write," or "not-accessible."</span></span>

</dd> </dl>

## <a name="fatal-error-1003"></a><span data-ttu-id="2b780-164">Schwerwiegender Fehler 1003</span><span class="sxs-lookup"><span data-stu-id="2b780-164">Fatal Error 1003</span></span>

<dl> <dt>

<span data-ttu-id="2b780-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, schwerwiegender>: " <fileName> : <line \#>: Ungültige Status Klausel <clause> "</span><span class="sxs-lookup"><span data-stu-id="2b780-165"><span id="_1003__Fatal_____fileName___line____Invalid_STATUS_clause__clause__"></span><span id="_1003__fatal_____filename___line____invalid_status_clause__clause__"></span><span id="_1003__FATAL_____FILENAME___LINE____INVALID_STATUS_CLAUSE__CLAUSE__"></span><1003, Fatal>: "<fileName>:<line\#>: Invalid STATUS clause <clause>"</span></span>
</dt> <dd>

<span data-ttu-id="2b780-166">Semantik Fehler des Objekttyp-Makro Aufruf Moduls.</span><span class="sxs-lookup"><span data-stu-id="2b780-166">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="2b780-167">Für SNMPv1 muss die Status-Klausel eines Objekttyp-Makro aufgabenaufes "obligatorisch", "optional", "veraltet" oder "veraltet" lauten.</span><span class="sxs-lookup"><span data-stu-id="2b780-167">For SNMPv1, the STATUS clause of an OBJECT-TYPE macro invocation must be "mandatory," "optional," "obsolete," or "deprecated."</span></span>

<span data-ttu-id="2b780-168">Bei SNMPv2C muss die Status-Klausel eines Objekttyp-Makro auf-aufgabens "Current", "deprecated" oder "deprecated" lauten.</span><span class="sxs-lookup"><span data-stu-id="2b780-168">For SNMPv2C, the STATUS clause of an OBJECT-TYPE macro invocation must be "current," "deprecated," or "obsolete."</span></span>

</dd> </dl>

## <a name="warning-1004"></a><span data-ttu-id="2b780-169">Warnung 1004</span><span class="sxs-lookup"><span data-stu-id="2b780-169">Warning 1004</span></span>

<dl> <dt>

<span data-ttu-id="2b780-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: " <fileName> : <line \#>: <identifier> Objekttyp, dessen Syntax zu einem der Counter-Typen aufgelöst wird, endet nicht mit dem Buchstaben" "</span><span class="sxs-lookup"><span data-stu-id="2b780-170"><span id="_1004__Warning_____fileName___line____OBJECT-TYPE__identifier___whose_syntax_resolves_to_one_of_the_Counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__warning_____filename___line____object-type__identifier___whose_syntax_resolves_to_one_of_the_counter_types_does_not_end_with_the_letter__s___"></span><span id="_1004__WARNING_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHOSE_SYNTAX_RESOLVES_TO_ONE_OF_THE_COUNTER_TYPES_DOES_NOT_END_WITH_THE_LETTER__S___"></span><1004, Warning>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, whose syntax resolves to one of the Counter types does not end with the letter 's' "</span></span>
</dt> <dd>

<span data-ttu-id="2b780-171">Semantik Warnung für Objekttyp-Makro Aufruf Modul.</span><span class="sxs-lookup"><span data-stu-id="2b780-171">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="2b780-172">Der Bezeichner für ein Objekt des Syntax Zählers (SNMPv1) oder Counter32 und Counter64 (SNMPv2C) muss den Plural aufweisen.</span><span class="sxs-lookup"><span data-stu-id="2b780-172">The identifier for an object of SYNTAX Counter (SNMPv1) or Counter32 and Counter64 (SNMPv2C) must be plural.</span></span>

<span data-ttu-id="2b780-173">Diese Warnung kann auftreten, wenn Sie ein SNMPv1-oder SNMPv2C-MIB kompilieren.</span><span class="sxs-lookup"><span data-stu-id="2b780-173">This warning can occur when compiling either an SNMPv1 or SNMPv2C MIB.</span></span>

</dd> </dl>

## <a name="warning-1005"></a><span data-ttu-id="2b780-174">Warnung 1005</span><span class="sxs-lookup"><span data-stu-id="2b780-174">Warning 1005</span></span>

<dl> <dt>

<span data-ttu-id="2b780-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Warning>: " <fileName> : <line \#>: Objekttyp mit der Syntax" Sequence of ", sollte über eine Access-Klausel verfügen, auf die nicht zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="2b780-175"><span id="_1005__Warning_____fileName___line____OBJECT-TYPE_with_SYNTAX__SEQUENCE_OF___should_have_an_ACCESS_clause__not-accessible_"></span><span id="_1005__warning_____filename___line____object-type_with_syntax__sequence_of___should_have_an_access_clause__not-accessible_"></span><span id="_1005__WARNING_____FILENAME___LINE____OBJECT-TYPE_WITH_SYNTAX__SEQUENCE_OF___SHOULD_HAVE_AN_ACCESS_CLAUSE__NOT-ACCESSIBLE_"></span><1005, Warning>: "<fileName>:<line\#>: OBJECT-TYPE with SYNTAX "SEQUENCE OF", should have an ACCESS clause "not-accessible"</span></span>
</dt> <dd>

<span data-ttu-id="2b780-176">Semantik Warnung für Objekttyp-Makro Aufruf Modul.</span><span class="sxs-lookup"><span data-stu-id="2b780-176">OBJECT-TYPE macro invocation module semantic warning.</span></span> <span data-ttu-id="2b780-177">Eine Tabelle oder konzeptionelle Zeile (Sequenz von bzw. Sequenz Objekttypen) muss "nicht zugänglich" sein.</span><span class="sxs-lookup"><span data-stu-id="2b780-177">A table or conceptual row (SEQUENCE OF or SEQUENCE object types, respectively) must be "not-accessible."</span></span>

<span data-ttu-id="2b780-178">Diese Warnung kann entweder in SNMPv1 oder SNMPv2C auftreten.</span><span class="sxs-lookup"><span data-stu-id="2b780-178">This warning can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

## <a name="fatal-error-1006"></a><span data-ttu-id="2b780-179">Schwerwiegender Fehler 1006</span><span class="sxs-lookup"><span data-stu-id="2b780-179">Fatal Error 1006</span></span>

<dl> <dt>

<span data-ttu-id="2b780-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, schwerwiegender>: " <fileName> : <Zeile \#> Objekttyp <identifier> , der eine Syntax Sequenz hat, verfügt nicht über eine Index-oder Erweiterungs Klausel"</span><span class="sxs-lookup"><span data-stu-id="2b780-180"><span id="_1006__Fatal_____fileName___line___OBJECT-TYPE__identifier___which_is_of_SYNTAX_SEQUENCE__does_not_have_an_INDEX_or_AUGMENTS_clause_"></span><span id="_1006__fatal_____filename___line___object-type__identifier___which_is_of_syntax_sequence__does_not_have_an_index_or_augments_clause_"></span><span id="_1006__FATAL_____FILENAME___LINE___OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX_SEQUENCE__DOES_NOT_HAVE_AN_INDEX_OR_AUGMENTS_CLAUSE_"></span><1006, Fatal>: "<fileName>:<line\#> OBJECT-TYPE <identifier>, which is of SYNTAX SEQUENCE, does not have an INDEX or AUGMENTS clause"</span></span>
</dt> <dd>

<span data-ttu-id="2b780-181">Semantik Fehler des Objekttyp-Makro Aufruf Moduls.</span><span class="sxs-lookup"><span data-stu-id="2b780-181">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="2b780-182">Für SNMPv1 muss die Index-Klausel für eine Objekttyp Definition vorhanden sein, deren Syntax zu einem Sequenztyp aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="2b780-182">For SNMPv1, the INDEX clause must be present for an OBJECT-TYPE definition whose SYNTAX resolves to a SEQUENCE type.</span></span>

<span data-ttu-id="2b780-183">Für SNMPv2C muss entweder die Index-oder die Augments-Klausel für eine konzeptionelle Zeilen Deklaration vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="2b780-183">For SNMPv2C, either the INDEX or the AUGMENTS clause must be present for a conceptual row declaration.</span></span>

</dd> </dl>

## <a name="fatal-error-1008"></a><span data-ttu-id="2b780-184">Schwerwiegender Fehler 1008</span><span class="sxs-lookup"><span data-stu-id="2b780-184">Fatal Error 1008</span></span>

<dl> <dt>

<span data-ttu-id="2b780-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, schwerwiegender>: " <fileName> : <line \#>: der Objekttyp <identifier> , für den die Syntax" Sequenz "nicht referenziert wurde.</span><span class="sxs-lookup"><span data-stu-id="2b780-185"><span id="_1008__Fatal_____fileName___line____OBJECT-TYPE__identifier___which_is_of_SYNTAX__SEQUENCE__has_not_been_referenced_"></span><span id="_1008__fatal_____filename___line____object-type__identifier___which_is_of_syntax__sequence__has_not_been_referenced_"></span><span id="_1008__FATAL_____FILENAME___LINE____OBJECT-TYPE__IDENTIFIER___WHICH_IS_OF_SYNTAX__SEQUENCE__HAS_NOT_BEEN_REFERENCED_"></span><1008, Fatal>: "<fileName>:<line\#>: OBJECT-TYPE <identifier>, which is of SYNTAX "SEQUENCE" has not been referenced"</span></span>
</dt> <dd>

<span data-ttu-id="2b780-186">Semantik Fehler des Objekttyp-Makro Aufruf Moduls.</span><span class="sxs-lookup"><span data-stu-id="2b780-186">OBJECT-TYPE macro invocation module semantic error.</span></span> <span data-ttu-id="2b780-187">Ein Objekttyp mit der Syntax Klausel als Sequenztyp muss in der Syntax Klausel von genau einem Objekttyp Aufruf enthalten sein, der für eine Tabellen Deklaration steht, d. h. ein Objekt mit der Syntax Klausel als Sequenz vom Typ.</span><span class="sxs-lookup"><span data-stu-id="2b780-187">An OBJECT-TYPE with the SYNTAX clause as a SEQUENCE type must figure in the SYNTAX clause of exactly one OBJECT-TYPE invocation that stands for a table declaration, that is, an object with the SYNTAX clause as a SEQUENCE OF type.</span></span> <span data-ttu-id="2b780-188">Der <Zeilen \#> Parameter verweist auf den zweiten Verweis Punkt.</span><span class="sxs-lookup"><span data-stu-id="2b780-188">The <line\#> parameter refers to the second point of reference.</span></span>

<span data-ttu-id="2b780-189">Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.</span><span class="sxs-lookup"><span data-stu-id="2b780-189">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

</dd> </dl>

 

 



