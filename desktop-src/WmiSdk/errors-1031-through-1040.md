---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 1031 bis 1040.
ms.assetid: 5fc519ac-ae05-4daf-a681-7935190f1d46
ms.tgt_platform: multiple
title: Fehler 1031 bis 1040
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d34079c2cbdb8e50aef04e8c364ba99abee760fe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106350003"
---
# <a name="errors-1031-through-1040"></a><span data-ttu-id="fc8ce-103">Fehler 1031 bis 1040</span><span class="sxs-lookup"><span data-stu-id="fc8ce-103">Errors 1031 through 1040</span></span>

<span data-ttu-id="fc8ce-104">Beschreibt die WMI-SNMP-Anbieter Fehler 1031 bis 1040.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-104">Describes WMI SNMP provider errors 1031 through 1040.</span></span>

[<span data-ttu-id="fc8ce-105">Warnung 1031</span><span class="sxs-lookup"><span data-stu-id="fc8ce-105">Warning 1031</span></span>](#warning-1031)

[<span data-ttu-id="fc8ce-106">Schwerwiegender Fehler 1032</span><span class="sxs-lookup"><span data-stu-id="fc8ce-106">Fatal Error 1032</span></span>](#fatal-error-1032)

[<span data-ttu-id="fc8ce-107">Schwerwiegender Fehler 1033</span><span class="sxs-lookup"><span data-stu-id="fc8ce-107">Fatal Error 1033</span></span>](#fatal-error-1033)

[<span data-ttu-id="fc8ce-108">Warnung 1034</span><span class="sxs-lookup"><span data-stu-id="fc8ce-108">Warning 1034</span></span>](#warning-1034)

[<span data-ttu-id="fc8ce-109">Warnung 1036</span><span class="sxs-lookup"><span data-stu-id="fc8ce-109">Warning 1036</span></span>](#warning-1036)

[<span data-ttu-id="fc8ce-110">Schwerwiegender Fehler 1037</span><span class="sxs-lookup"><span data-stu-id="fc8ce-110">Fatal Error 1037</span></span>](#fatal-error-1037)

[<span data-ttu-id="fc8ce-111">Schwerwiegender Fehler 1038</span><span class="sxs-lookup"><span data-stu-id="fc8ce-111">Fatal Error 1038</span></span>](#fatal-error-1038)

[<span data-ttu-id="fc8ce-112">Schwerwiegender Fehler 1039</span><span class="sxs-lookup"><span data-stu-id="fc8ce-112">Fatal Error 1039</span></span>](#fatal-error-1039)

[<span data-ttu-id="fc8ce-113">Schwerwiegender Fehler 1040</span><span class="sxs-lookup"><span data-stu-id="fc8ce-113">Fatal Error 1040</span></span>](#fatal-error-1040)

## <a name="warning-1031"></a><span data-ttu-id="fc8ce-114">Warnung 1031</span><span class="sxs-lookup"><span data-stu-id="fc8ce-114">Warning 1031</span></span>

<dl> <dt>

<span data-ttu-id="fc8ce-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Warning>: " <fileName> : <line \#>: das Standard Symbol <identifier> sollte aus dem Modul importiert werden <identifier> . Angenommen, die Standard Definition. "**</span><span class="sxs-lookup"><span data-stu-id="fc8ce-115"><span id="_1031__Warning_____fileName___line____Standard_symbol__identifier__should_be_imported_from_module__identifier_._Assuming_the_standard_definition._"></span><span id="_1031__warning_____filename___line____standard_symbol__identifier__should_be_imported_from_module__identifier_._assuming_the_standard_definition._"></span><span id="_1031__WARNING_____FILENAME___LINE____STANDARD_SYMBOL__IDENTIFIER__SHOULD_BE_IMPORTED_FROM_MODULE__IDENTIFIER_._ASSUMING_THE_STANDARD_DEFINITION._"></span>**<1031, Warning>: "<fileName>:<line\#>: Standard symbol <identifier> should be imported from module <identifier>. Assuming the standard definition."**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ce-116">Gibt eine Semantik Warnung für das Abschnitts Modul aus, die spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-116">IMPORTS section module semantic warning, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="fc8ce-117">Wenn sich ein SNMP-Bezeichner, der dem Compiler bekannt ist, im Imports-Abschnitt befindet, muss das Modul, aus dem es importiert wird, eines der Standardmodule sein.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-117">If an SNMP identifier known to the compiler is in the IMPORTS section, then the module from which it is imported must be one of the standard modules.</span></span>

<span data-ttu-id="fc8ce-118">Bestimmte häufig verwendete Importe werden im Rahmen des Compilers "angenommen".</span><span class="sxs-lookup"><span data-stu-id="fc8ce-118">Certain commonly used IMPORTS are "assumed knowledge" on the part of the compiler.</span></span> <span data-ttu-id="fc8ce-119">Es ist nicht erforderlich, dass der Compiler Zugriff auf andere Informationsmodule benötigt, um diese zu beheben.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-119">It is unnecessary for the compiler to require access to other information modules to resolve these.</span></span>

<span data-ttu-id="fc8ce-120">Die integrierten SNMPv1-und SNMPv2C-Importe werden in den folgenden Tabellen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-120">The built-in SNMPv1 and SNMPv2C IMPORTS are described in the following tables.</span></span>

</dd> </dl>

<span data-ttu-id="fc8ce-121">**Integrierte SNMPv1-Importe**</span><span class="sxs-lookup"><span data-stu-id="fc8ce-121">**Built-in SNMPv1 IMPORTS**</span></span>



| <span data-ttu-id="fc8ce-122">Import Klasse</span><span class="sxs-lookup"><span data-stu-id="fc8ce-122">Import Class</span></span> | <span data-ttu-id="fc8ce-123">Modul</span><span class="sxs-lookup"><span data-stu-id="fc8ce-123">Module</span></span>      | <span data-ttu-id="fc8ce-124">Instanzen</span><span class="sxs-lookup"><span data-stu-id="fc8ce-124">Instances</span></span>                                                           |
|--------------|-------------|---------------------------------------------------------------------|
| <span data-ttu-id="fc8ce-125">ASN. 1-Wert</span><span class="sxs-lookup"><span data-stu-id="fc8ce-125">ASN.1 Value</span></span>  | <span data-ttu-id="fc8ce-126">RFC1155-SMI</span><span class="sxs-lookup"><span data-stu-id="fc8ce-126">RFC1155-SMI</span></span> | <span data-ttu-id="fc8ce-127">Internet, Verzeichnis, Verwaltung, experimentell, privat, Unternehmen</span><span class="sxs-lookup"><span data-stu-id="fc8ce-127">Internet, directory, management, experimental, private, enterprises</span></span> |
|              | <span data-ttu-id="fc8ce-128">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="fc8ce-128">RFC1213-MIB</span></span> | <span data-ttu-id="fc8ce-129">MIB-II und IP, Schnittstellen, Übertragung</span><span class="sxs-lookup"><span data-stu-id="fc8ce-129">MIB-II and IP, interfaces, transmission</span></span>                             |
| <span data-ttu-id="fc8ce-130">ASN. 1-Typ</span><span class="sxs-lookup"><span data-stu-id="fc8ce-130">ASN.1 Type</span></span>   | <span data-ttu-id="fc8ce-131">RFC1155-SMI</span><span class="sxs-lookup"><span data-stu-id="fc8ce-131">RFC1155-SMI</span></span> | <span data-ttu-id="fc8ce-132">Network Address, IPAddress, Counter, Messgerät, TimeTicks, undurchsichtig</span><span class="sxs-lookup"><span data-stu-id="fc8ce-132">NetworkAddress, IpAddress, Counter, Gauge, TimeTicks, Opaque</span></span>        |
|              | <span data-ttu-id="fc8ce-133">RFC1213-MIB</span><span class="sxs-lookup"><span data-stu-id="fc8ce-133">RFC1213-MIB</span></span> | <span data-ttu-id="fc8ce-134">Display String, physaddress</span><span class="sxs-lookup"><span data-stu-id="fc8ce-134">DisplayString, PhysAddress</span></span>                                          |
| <span data-ttu-id="fc8ce-135">ASN. 1-Makro</span><span class="sxs-lookup"><span data-stu-id="fc8ce-135">ASN.1 Macro</span></span>  | <span data-ttu-id="fc8ce-136">RFC-1212</span><span class="sxs-lookup"><span data-stu-id="fc8ce-136">RFC-1212</span></span>    | <span data-ttu-id="fc8ce-137">Objekttyp</span><span class="sxs-lookup"><span data-stu-id="fc8ce-137">OBJECT-TYPE</span></span>                                                         |
|              | <span data-ttu-id="fc8ce-138">RFC-1215</span><span class="sxs-lookup"><span data-stu-id="fc8ce-138">RFC-1215</span></span>    | <span data-ttu-id="fc8ce-139">Trap-Typ</span><span class="sxs-lookup"><span data-stu-id="fc8ce-139">TRAP-TYPE</span></span>                                                           |



 

<span data-ttu-id="fc8ce-140">**Integrierte SNMPv2C-Importe**</span><span class="sxs-lookup"><span data-stu-id="fc8ce-140">**Built-in SNMPv2C IMPORTS**</span></span>



| <span data-ttu-id="fc8ce-141">Import Klasse</span><span class="sxs-lookup"><span data-stu-id="fc8ce-141">Import Class</span></span>       | <span data-ttu-id="fc8ce-142">Modul</span><span class="sxs-lookup"><span data-stu-id="fc8ce-142">Module</span></span>      | <span data-ttu-id="fc8ce-143">Instanzen</span><span class="sxs-lookup"><span data-stu-id="fc8ce-143">Instances</span></span>                                                                                                                                                                                                      |
|--------------------|-------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fc8ce-144">ASN. 1-Wert</span><span class="sxs-lookup"><span data-stu-id="fc8ce-144">ASN.1 Value</span></span>        | <span data-ttu-id="fc8ce-145">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="fc8ce-145">SNMPv2-SMI</span></span>  | <span data-ttu-id="fc8ce-146">org, DoD, Internet, Verzeichnis, Mgmt, MIB-2, Übertragung, experimentell, privat, Unternehmen, Sicherheit, SNMPv2, snmpdomains, snmpproxys, snmpModules</span><span class="sxs-lookup"><span data-stu-id="fc8ce-146">org, dod, Internet, directory, mgmt, mib-2, transmission, experimental, private, enterprises, security, snmpv2, snmpDomains, snmpProxys, snmpModules</span></span>                                                           |
|                    | <span data-ttu-id="fc8ce-147">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="fc8ce-147">SNMPv2-TM</span></span>   | <span data-ttu-id="fc8ce-148">rfc1157Proxy</span><span class="sxs-lookup"><span data-stu-id="fc8ce-148">rfc1157Proxy</span></span>                                                                                                                                                                                                   |
| <span data-ttu-id="fc8ce-149">Objektidentität</span><span class="sxs-lookup"><span data-stu-id="fc8ce-149">Object Identity</span></span>    | <span data-ttu-id="fc8ce-150">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="fc8ce-150">SNMPv2-SMI</span></span>  | <span data-ttu-id="fc8ce-151">zerodotzero</span><span class="sxs-lookup"><span data-stu-id="fc8ce-151">zeroDotZero</span></span>                                                                                                                                                                                                    |
|                    | <span data-ttu-id="fc8ce-152">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="fc8ce-152">SNMPv2-TM</span></span>   | <span data-ttu-id="fc8ce-153">snmpudpdomain, snmpclnsdomain, smnpmsdomain, snmpddpdomain, snmpipxdomain, rfc1157Domain</span><span class="sxs-lookup"><span data-stu-id="fc8ce-153">snmpUDPDomain, snmpCLNSDomain, smnpCONSDomain, snmpDDPDomain, snmpIPXDomain, rfc1157Domain</span></span>                                                                                                                     |
| <span data-ttu-id="fc8ce-154">ASN. 1-Typ</span><span class="sxs-lookup"><span data-stu-id="fc8ce-154">ASN.1 Type</span></span>         | <span data-ttu-id="fc8ce-155">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="fc8ce-155">SNMPv2-SMI</span></span>  | <span data-ttu-id="fc8ce-156">Integer32, IPAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32</span><span class="sxs-lookup"><span data-stu-id="fc8ce-156">Integer32, IpAddress, Counter32, TimeTicks, Opaque, Counter64, Unsigned32, Gauge32</span></span>                                                                                                                             |
| <span data-ttu-id="fc8ce-157">ASN. 1-Makro</span><span class="sxs-lookup"><span data-stu-id="fc8ce-157">ASN.1 Macro</span></span>        | <span data-ttu-id="fc8ce-158">SNMPv2-SMI</span><span class="sxs-lookup"><span data-stu-id="fc8ce-158">SNMPv2-SMI</span></span>  | <span data-ttu-id="fc8ce-159">Modul Identität, Objekt Identität, Objekttyp, Benachrichtigungstyp</span><span class="sxs-lookup"><span data-stu-id="fc8ce-159">MODULE-IDENTITY, OBJECT-IDENTITY, OBJECT-TYPE, NOTIFICATION-TYPE</span></span>                                                                                                                                               |
|                    | <span data-ttu-id="fc8ce-160">SNMPv2-conf</span><span class="sxs-lookup"><span data-stu-id="fc8ce-160">SNMPv2-CONF</span></span> | <span data-ttu-id="fc8ce-161">Objektgruppe, Benachrichtigungs Gruppe, Modul Konformität, Agentfunktionen</span><span class="sxs-lookup"><span data-stu-id="fc8ce-161">OBJECT-GROUP, NOTIFICATION-GROUP, MODULE-COMPLIANCE, AGENT-CAPABILITIES</span></span>                                                                                                                                        |
|                    | <span data-ttu-id="fc8ce-162">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="fc8ce-162">SNMPv2-TC</span></span>   | <span data-ttu-id="fc8ce-163">Text Konvention</span><span class="sxs-lookup"><span data-stu-id="fc8ce-163">TEXTUAL-CONVENTION</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="fc8ce-164">Text Konvention</span><span class="sxs-lookup"><span data-stu-id="fc8ce-164">Textual Convention</span></span> | <span data-ttu-id="fc8ce-165">SNMPv2-TC</span><span class="sxs-lookup"><span data-stu-id="fc8ce-165">SNMPv2-TC</span></span>   | <span data-ttu-id="fc8ce-166">Display String, physaddress, MACAddress, Wahrheitswert, testandincr, autonomoustype, instancepointer, variablepointer, rowpointer, rowstatus, timestamp, TimeInterval, DateAndTime, StorageType, tdomain, taddress</span><span class="sxs-lookup"><span data-stu-id="fc8ce-166">DisplayString, PhysAddress, MacAddress, TruthValue, TestAndIncr, AutonomousType, InstancePointer, VariablePointer, RowPointer, RowStatus, TimeStamp, TimeInterval, DateAndTime, StorageType, Tdomain, Taddress</span></span> |
|                    | <span data-ttu-id="fc8ce-167">SNMPv2-TM</span><span class="sxs-lookup"><span data-stu-id="fc8ce-167">SNMPv2-TM</span></span>   | <span data-ttu-id="fc8ce-168">Snmpudpaddress, snmposiaddress, snmpnbpaddress, snmpipxaddress</span><span class="sxs-lookup"><span data-stu-id="fc8ce-168">SnmpUDPAddress, SnmpOSIAddress, SnmpNBPAddress, SnmpIPXAddress</span></span>                                                                                                                                                 |



 

## <a name="fatal-error-1032"></a><span data-ttu-id="fc8ce-169">Schwerwiegender Fehler 1032</span><span class="sxs-lookup"><span data-stu-id="fc8ce-169">Fatal Error 1032</span></span>

<dl> <dt>

<span data-ttu-id="fc8ce-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, schwerwiegender>: " <fileName><line \#>: doppelter Wert <value> in der Enumeration"**</span><span class="sxs-lookup"><span data-stu-id="fc8ce-170"><span id="_1032__Fatal_____fileName__line____Duplicate_value__value__in_enumeration_"></span><span id="_1032__fatal_____filename__line____duplicate_value__value__in_enumeration_"></span><span id="_1032__FATAL_____FILENAME__LINE____DUPLICATE_VALUE__VALUE__IN_ENUMERATION_"></span>**<1032, Fatal>: "<fileName><line\#>: Duplicate value <value> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ce-171">Modul Semantik Fehler in einer Enumeration, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-171">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="fc8ce-172">Es dürfen keine doppelten Werte vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-172">There must not be any duplicate values.</span></span> <span data-ttu-id="fc8ce-173">Der <Zeile \#> Parameter ist die Position der Wiederholung des Namens/Werts.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-173">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="fatal-error-1033"></a><span data-ttu-id="fc8ce-174">Schwerwiegender Fehler 1033</span><span class="sxs-lookup"><span data-stu-id="fc8ce-174">Fatal Error 1033</span></span>

<dl> <dt>

<span data-ttu-id="fc8ce-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, schwerwiegender>: " <fileName><line \#>: Doppelter Name <identifier> in Enumeration"**</span><span class="sxs-lookup"><span data-stu-id="fc8ce-175"><span id="_1033__Fatal_____fileName__line____Duplicate_name__identifier__in_enumeration_"></span><span id="_1033__fatal_____filename__line____duplicate_name__identifier__in_enumeration_"></span><span id="_1033__FATAL_____FILENAME__LINE____DUPLICATE_NAME__IDENTIFIER__IN_ENUMERATION_"></span>**<1033, Fatal>: "<fileName><line\#>: Duplicate name <identifier> in enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ce-176">Modul Semantik Fehler in einer Enumeration, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-176">Module semantic error in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="fc8ce-177">Es dürfen keine doppelten Namen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-177">There must not be any duplicate names.</span></span> <span data-ttu-id="fc8ce-178">Der <Zeile \#> Parameter ist die Position der Wiederholung des Namens/Werts.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-178">The <line\#> parameter is the position of the recurrence of the name/value.</span></span>

</dd> </dl>

## <a name="warning-1034"></a><span data-ttu-id="fc8ce-179">Warnung 1034</span><span class="sxs-lookup"><span data-stu-id="fc8ce-179">Warning 1034</span></span>

<dl> <dt>

<span data-ttu-id="fc8ce-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Warning>: " <fileName><line \#>: der Wert 0 ist in einer Enumeration unzulässig."**</span><span class="sxs-lookup"><span data-stu-id="fc8ce-180"><span id="_1034__Warning_____fileName__line____A_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__warning_____filename__line____a_value_of_0_disallowed_in_an_enumeration_"></span><span id="_1034__WARNING_____FILENAME__LINE____A_VALUE_OF_0_DISALLOWED_IN_AN_ENUMERATION_"></span>**<1034, Warning>: "<fileName><line\#>: A value of 0 disallowed in an enumeration"**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ce-181">Modul Semantik Warnung in einer Enumeration, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-181">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="fc8ce-182">Es wird empfohlen, dass ein benannter Wert von NULL nicht in einer Enumeration verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-182">It is recommended that a named value of zero not be used in an enumeration.</span></span>

</dd> </dl>

## <a name="warning-1036"></a><span data-ttu-id="fc8ce-183">Warnung 1036</span><span class="sxs-lookup"><span data-stu-id="fc8ce-183">Warning 1036</span></span>

<dl> <dt>

<span data-ttu-id="fc8ce-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036 wird die Warnung> " <fileName><Zeilen \#>: Wert in der Enumeration nicht in eine positive ganze Zahl aufgelöst"**</span><span class="sxs-lookup"><span data-stu-id="fc8ce-184"><span id="_1036__Warning____fileName__line____Value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__warning____filename__line____value_in_enumeration_does_not_resolve_to_a_positive_integer_"></span><span id="_1036__WARNING____FILENAME__LINE____VALUE_IN_ENUMERATION_DOES_NOT_RESOLVE_TO_A_POSITIVE_INTEGER_"></span>**<1036, Warning> "<fileName><line\#>: Value in enumeration does not resolve to a positive integer"**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ce-185">Modul Semantik Warnung in einer Enumeration, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-185">Module semantic warning in an enumeration, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="fc8ce-186">Ein negativer Wert ist in einer Enumeration nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-186">A negative value is not allowed in an enumeration.</span></span>

</dd> </dl>

## <a name="fatal-error-1037"></a><span data-ttu-id="fc8ce-187">Schwerwiegender Fehler 1037</span><span class="sxs-lookup"><span data-stu-id="fc8ce-187">Fatal Error 1037</span></span>

<dl> <dt>

<span data-ttu-id="fc8ce-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, schwerwiegender>: " <fileName><line \#>: Bezeichner <identifier> wird nicht in Oktett-Zeichen folgen oder nicht transparente Typen aufgelöst"**</span><span class="sxs-lookup"><span data-stu-id="fc8ce-188"><span id="_1037__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_to_OCTET_STRING_or_Opaque_types_"></span><span id="_1037__fatal_____filename__line____identifier__identifier__does_not_resolve_to_octet_string_or_opaque_types_"></span><span id="_1037__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_TO_OCTET_STRING_OR_OPAQUE_TYPES_"></span>**<1037, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve to OCTET STRING or Opaque types"**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ce-189">Modul Semantik Fehler in der Größenangabe, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-189">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="fc8ce-190">Das in einer Größenangabe verwendete Symbol muss in eine Oktett-Zeichenfolge oder eine nicht transparente Zeichenfolge aufgelöst werden</span><span class="sxs-lookup"><span data-stu-id="fc8ce-190">The symbol used in a SIZE specification must resolve to OCTET STRING or Opaque.</span></span>

</dd> </dl>

## <a name="fatal-error-1038"></a><span data-ttu-id="fc8ce-191">Schwerwiegender Fehler 1038</span><span class="sxs-lookup"><span data-stu-id="fc8ce-191">Fatal Error 1038</span></span>

<dl> <dt>

<span data-ttu-id="fc8ce-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, schwerwiegender>: " <fileName><line \#>: Bezeichner <identifier> löst keine Ganzzahl oder keinen Mess Zeichentyp aus."**</span><span class="sxs-lookup"><span data-stu-id="fc8ce-192"><span id="_1038__Fatal_____fileName__line____Identifier__identifier__does_not_resolve_an_INTEGER_or_Gauge_type_"></span><span id="_1038__fatal_____filename__line____identifier__identifier__does_not_resolve_an_integer_or_gauge_type_"></span><span id="_1038__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__DOES_NOT_RESOLVE_AN_INTEGER_OR_GAUGE_TYPE_"></span>**<1038, Fatal>: "<fileName><line\#>: Identifier <identifier> does not resolve an INTEGER or Gauge type"**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ce-193">Modul Semantik Fehler in Bereichs Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-193">Module semantic error in range specification.</span></span> <span data-ttu-id="fc8ce-194">Dieser Fehler kann entweder in SNMPv1 oder SNMPv2C auftreten.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-194">This error can occur in either SNMPv1 or SNMPv2C.</span></span>

<span data-ttu-id="fc8ce-195">In SNMPv1 muss das Symbol, das in einer Bereichs Spezifikation verwendet wird, in eine ganze Zahl oder ein Messgerät aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-195">In SNMPv1, the symbol used in a Range specification must resolve to INTEGER or Gauge.</span></span>

<span data-ttu-id="fc8ce-196">In SNMPv2C muss das in einer Bereichs Spezifikation verwendete Symbol in "Integer", "Gauge32", "Integer32" oder "Unsigned32" aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-196">In SNMPv2C, the symbol used in a Range specification must resolve to INTEGER, Gauge32, Integer32, or Unsigned32.</span></span>

</dd> </dl>

## <a name="fatal-error-1039"></a><span data-ttu-id="fc8ce-197">Schwerwiegender Fehler 1039</span><span class="sxs-lookup"><span data-stu-id="fc8ce-197">Fatal Error 1039</span></span>

<dl> <dt>

<span data-ttu-id="fc8ce-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, schwerwiegender>: <fileName><Zeilen \#>: negativer Wert, der in der Größenangabe verwendet wird. "**</span><span class="sxs-lookup"><span data-stu-id="fc8ce-198"><span id="_1039__Fatal___fileName__line____Negative_value_used_in_SIZE_specification_"></span><span id="_1039__fatal___filename__line____negative_value_used_in_size_specification_"></span><span id="_1039__FATAL___FILENAME__LINE____NEGATIVE_VALUE_USED_IN_SIZE_SPECIFICATION_"></span>**<1039, Fatal>:<fileName><line\#>: Negative value used in SIZE specification"**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ce-199">Modul Semantik Fehler in der Größenangabe, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-199">Module semantic error in SIZE specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="fc8ce-200">Jeder Wert, der zum Angeben der Größe verwendet wird, muss nicht negativ sein.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-200">Any value used in specifying the SIZE must be non-negative.</span></span>

</dd> </dl>

## <a name="fatal-error-1040"></a><span data-ttu-id="fc8ce-201">Schwerwiegender Fehler 1040</span><span class="sxs-lookup"><span data-stu-id="fc8ce-201">Fatal Error 1040</span></span>

<dl> <dt>

<span data-ttu-id="fc8ce-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, schwerwiegender>: " <fileName><line \#>: Bezeichner <identifier> in der Größenangabe wird nicht in einen nicht negativen integralen Wert aufgelöst"**</span><span class="sxs-lookup"><span data-stu-id="fc8ce-202"><span id="_1040__Fatal_____fileName__line____Identifier__identifier__in_SIZE_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__fatal_____filename__line____identifier__identifier__in_size_specification_does_not_resolve_to_a_non-negative_integral_value_"></span><span id="_1040__FATAL_____FILENAME__LINE____IDENTIFIER__IDENTIFIER__IN_SIZE_SPECIFICATION_DOES_NOT_RESOLVE_TO_A_NON-NEGATIVE_INTEGRAL_VALUE_"></span>**<1040, Fatal>: "<fileName><line\#>: Identifier <identifier> in SIZE specification does not resolve to a non-negative integral value"**</span></span>
</dt> <dd>

<span data-ttu-id="fc8ce-203">Modul Semantik Fehler in Bereichs-oder Größenangabe, spezifisch für weder SNMPv1 noch SNMPv2C.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-203">Module semantic error in range or size specification, specific to neither SNMPv1 nor SNMPv2C.</span></span> <span data-ttu-id="fc8ce-204">Jedes Symbol, das verwendet wird, um einen Wert in einer Größenangabe anzugeben, wird in einen nicht negativen Wert aufgelöst.</span><span class="sxs-lookup"><span data-stu-id="fc8ce-204">Any symbol used in specifying a value in a SIZE specification resolves to a non-negative value.</span></span>

</dd> </dl>

 

 



