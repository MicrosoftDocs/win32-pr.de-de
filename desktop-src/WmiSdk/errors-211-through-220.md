---
description: Beschreibt die WMI-SNMP-Anbieter Fehler 211 bis 220.
ms.assetid: beaa644d-51b3-4a57-8853-0b37f69f615a
ms.tgt_platform: multiple
title: Fehler 211 bis 220
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f25dbf8cb8f27d4c58a1505176eca218b8d947d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759433"
---
# <a name="errors-211-through-220"></a><span data-ttu-id="eee83-103">Fehler 211 bis 220</span><span class="sxs-lookup"><span data-stu-id="eee83-103">Errors 211 through 220</span></span>

<span data-ttu-id="eee83-104">Beschreibt die WMI-SNMP-Anbieter Fehler 211 bis 220.</span><span class="sxs-lookup"><span data-stu-id="eee83-104">Describes WMI SNMP provider errors 211 through 220.</span></span>

[<span data-ttu-id="eee83-105">Informations Meldung 211</span><span class="sxs-lookup"><span data-stu-id="eee83-105">Information Message 211</span></span>](#information-message-211)

[<span data-ttu-id="eee83-106">Schwerwiegender Fehler 212</span><span class="sxs-lookup"><span data-stu-id="eee83-106">Fatal Error 212</span></span>](#fatal-error-212)

[<span data-ttu-id="eee83-107">Schwerwiegender Fehler 213</span><span class="sxs-lookup"><span data-stu-id="eee83-107">Fatal Error 213</span></span>](#fatal-error-213)

[<span data-ttu-id="eee83-108">Schwerwiegender Fehler 214</span><span class="sxs-lookup"><span data-stu-id="eee83-108">Fatal Error 214</span></span>](#fatal-error-214)

[<span data-ttu-id="eee83-109">Schwerwiegender Fehler 215</span><span class="sxs-lookup"><span data-stu-id="eee83-109">Fatal Error 215</span></span>](#fatal-error-215)

[<span data-ttu-id="eee83-110">Schwerwiegender Fehler 216</span><span class="sxs-lookup"><span data-stu-id="eee83-110">Fatal Error 216</span></span>](#fatal-error-216)

[<span data-ttu-id="eee83-111">Schwerwiegender Fehler 217</span><span class="sxs-lookup"><span data-stu-id="eee83-111">Fatal Error 217</span></span>](#fatal-error-217)

[<span data-ttu-id="eee83-112">Schwerwiegender Fehler 218</span><span class="sxs-lookup"><span data-stu-id="eee83-112">Fatal Error 218</span></span>](#fatal-error-218)

[<span data-ttu-id="eee83-113">Schwerwiegender Fehler 219</span><span class="sxs-lookup"><span data-stu-id="eee83-113">Fatal Error 219</span></span>](#fatal-error-219)

[<span data-ttu-id="eee83-114">Schwerwiegender Fehler 220</span><span class="sxs-lookup"><span data-stu-id="eee83-114">Fatal Error 220</span></span>](#fatal-error-220)

## <a name="information-message-211"></a><span data-ttu-id="eee83-115">Informations Meldung 211</span><span class="sxs-lookup"><span data-stu-id="eee83-115">Information Message 211</span></span>

<dl> <dt>

<span data-ttu-id="eee83-116"><span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, Informationen>: "Trap-Typ wird übersprungen <identifier> "**</span><span class="sxs-lookup"><span data-stu-id="eee83-116"><span id="_211__Information____Skipping_TRAP-TYPE__identifier__"></span><span id="_211__information____skipping_trap-type__identifier__"></span><span id="_211__INFORMATION____SKIPPING_TRAP-TYPE__IDENTIFIER__"></span>**<211, Information>: "Skipping TRAP-TYPE <identifier>"**</span></span>
</dt> <dd>

<span data-ttu-id="eee83-117">Alle Fehler in der Trap-Type-Definition generieren diese Meldung.</span><span class="sxs-lookup"><span data-stu-id="eee83-117">Any errors in the TRAP-TYPE definition generate this message.</span></span>

</dd> </dl>

## <a name="fatal-error-212"></a><span data-ttu-id="eee83-118">Schwerwiegender Fehler 212</span><span class="sxs-lookup"><span data-stu-id="eee83-118">Fatal Error 212</span></span>

<dl> <dt>

<span data-ttu-id="eee83-119"><span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212, schwerwiegender>: " <fileName> : <Zeile \#>: Syntax Fehler in Sequenz Definition. Letzter gelesener Token ist <token> "**</span><span class="sxs-lookup"><span data-stu-id="eee83-119"><span id="_212__Fatal_____fileName___line____Syntax_Error_in_SEQUENCE_definition._Last_token_read_is__token__"></span><span id="_212__fatal_____filename___line____syntax_error_in_sequence_definition._last_token_read_is__token__"></span><span id="_212__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SEQUENCE_DEFINITION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<212, Fatal>: "<fileName>:<line\#>: Syntax Error in SEQUENCE definition. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eee83-120">Modul Syntax Fehler in Typzuweisung.</span><span class="sxs-lookup"><span data-stu-id="eee83-120">Module syntax error in type assignment.</span></span> <span data-ttu-id="eee83-121">Zwischen der linken und der rechten Klammer eines Sequenz Konstrukts besteht ein Fehler, der auf einen Syntax Fehler in einer MIB-Typzuweisung zuweist.</span><span class="sxs-lookup"><span data-stu-id="eee83-121">There is an error between the left and right braces of a SEQUENCE construct, which amounts to a syntax error in a MIB type assignment.</span></span>

</dd> </dl>

## <a name="fatal-error-213"></a><span data-ttu-id="eee83-122">Schwerwiegender Fehler 213</span><span class="sxs-lookup"><span data-stu-id="eee83-122">Fatal Error 213</span></span>

<dl> <dt>

<span data-ttu-id="eee83-123"><span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213, schwerwiegender>: " <fileName> : <Zeile \#>: Syntax Fehler in Objektbezeichnerwert. Letzter gelesener Token ist <token> "**</span><span class="sxs-lookup"><span data-stu-id="eee83-123"><span id="_213__Fatal_____fileName___line____Syntax_Error_in_Object_Identifier_value._Last_token_read_is__token__"></span><span id="_213__fatal_____filename___line____syntax_error_in_object_identifier_value._last_token_read_is__token__"></span><span id="_213__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_OBJECT_IDENTIFIER_VALUE._LAST_TOKEN_READ_IS__TOKEN__"></span>**<213, Fatal>: "<fileName>:<line\#>: Syntax Error in Object Identifier value. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eee83-124">Modul Syntax Fehler in Wert Zuweisung.</span><span class="sxs-lookup"><span data-stu-id="eee83-124">Module syntax error in value assignment.</span></span> <span data-ttu-id="eee83-125">Zwischen der linken und der rechten Klammer eines objektbezeichnerwerts ist ein Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="eee83-125">There is an error between the left and right braces of an object identifier value.</span></span>

</dd> </dl>

## <a name="fatal-error-214"></a><span data-ttu-id="eee83-126">Schwerwiegender Fehler 214</span><span class="sxs-lookup"><span data-stu-id="eee83-126">Fatal Error 214</span></span>

<dl> <dt>

<span data-ttu-id="eee83-127"><span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214, schwerwiegender>: " <fileName> : <line \#>: Syntax Fehler in der Liste der Symbole in Imports. Letzter gelesener Token ist <token> "**</span><span class="sxs-lookup"><span data-stu-id="eee83-127"><span id="_214__Fatal_____fileName___line____Syntax_Error_in_the_list_of_symbols_in_IMPORTS._Last_token_read_is__token__"></span><span id="_214__fatal_____filename___line____syntax_error_in_the_list_of_symbols_in_imports._last_token_read_is__token__"></span><span id="_214__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_LIST_OF_SYMBOLS_IN_IMPORTS._LAST_TOKEN_READ_IS__TOKEN__"></span>**<214, Fatal>: "<fileName>:<line\#>: Syntax Error in the list of symbols in IMPORTS. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eee83-128">Modul Syntax Fehler im Imports-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="eee83-128">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-215"></a><span data-ttu-id="eee83-129">Schwerwiegender Fehler 215</span><span class="sxs-lookup"><span data-stu-id="eee83-129">Fatal Error 215</span></span>

<dl> <dt>

<span data-ttu-id="eee83-130"><span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215, schwerwiegender>: " <fileName> : <Zeile \#>: Syntax Fehler in Importe (fehlender Modulname?). Letzter gelesener Token ist <token> "**</span><span class="sxs-lookup"><span data-stu-id="eee83-130"><span id="_215__Fatal_____fileName___line____Syntax_Error_in_IMPORTS__missing_module_name__._Last_token_read_is__token__"></span><span id="_215__fatal_____filename___line____syntax_error_in_imports__missing_module_name__._last_token_read_is__token__"></span><span id="_215__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_IMPORTS__MISSING_MODULE_NAME__._LAST_TOKEN_READ_IS__TOKEN__"></span>**<215, Fatal>: "<fileName>:<line\#>: Syntax Error in IMPORTS (missing module name?). Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eee83-131">Modul Syntax Fehler im Imports-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="eee83-131">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-216"></a><span data-ttu-id="eee83-132">Schwerwiegender Fehler 216</span><span class="sxs-lookup"><span data-stu-id="eee83-132">Fatal Error 216</span></span>

<dl> <dt>

<span data-ttu-id="eee83-133"><span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216, schwerwiegender>: " <fileName> : <line \#>: Syntax Fehler im Imports-Abschnitt. Letzter gelesener Token ist <token> "**</span><span class="sxs-lookup"><span data-stu-id="eee83-133"><span id="_216__Fatal_____fileName___line____Syntax_Error_in_the_IMPORTS_section._Last_token_read_is__token__"></span><span id="_216__fatal_____filename___line____syntax_error_in_the_imports_section._last_token_read_is__token__"></span><span id="_216__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_THE_IMPORTS_SECTION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<216, Fatal>: "<fileName>:<line\#>: Syntax Error in the IMPORTS section. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eee83-134">Modul Syntax Fehler im Imports-Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="eee83-134">Module syntax error in the IMPORTS section.</span></span>

</dd> </dl>

## <a name="fatal-error-217"></a><span data-ttu-id="eee83-135">Schwerwiegender Fehler 217</span><span class="sxs-lookup"><span data-stu-id="eee83-135">Fatal Error 217</span></span>

<dl> <dt>

<span data-ttu-id="eee83-136"><span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217, schwerwiegender>: " <fileName> : <line \#>: Syntax Fehler in Integer-Enumeration. Letzter gelesener Token ist <token> "**</span><span class="sxs-lookup"><span data-stu-id="eee83-136"><span id="_217__Fatal_____fileName___line____Syntax_error_in_INTEGER_Enumeration._Last_token_read_is__token__"></span><span id="_217__fatal_____filename___line____syntax_error_in_integer_enumeration._last_token_read_is__token__"></span><span id="_217__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_INTEGER_ENUMERATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<217, Fatal>: "<fileName>:<line\#>: Syntax error in INTEGER Enumeration. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eee83-137">Jeder Modul Syntax Fehler zwischen der linken und der rechten Klammer einer MIB-Enumerationsdefinition generiert diese Meldung.</span><span class="sxs-lookup"><span data-stu-id="eee83-137">Any module syntax error between the left and right braces of a MIB enumeration definition generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-218"></a><span data-ttu-id="eee83-138">Schwerwiegender Fehler 218</span><span class="sxs-lookup"><span data-stu-id="eee83-138">Fatal Error 218</span></span>

<dl> <dt>

<span data-ttu-id="eee83-139"><span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218, schwerwiegender>: " <fileName> : <line \#>: Syntax Fehler in der Sub-Type-Spezifikation. Letzter gelesener Token ist <token> "**</span><span class="sxs-lookup"><span data-stu-id="eee83-139"><span id="_218__Fatal_____fileName___line____Syntax_Error_in_sub-type_specification._Last_token_read_is__token__"></span><span id="_218__fatal_____filename___line____syntax_error_in_sub-type_specification._last_token_read_is__token__"></span><span id="_218__FATAL_____FILENAME___LINE____SYNTAX_ERROR_IN_SUB-TYPE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<218, Fatal>: "<fileName>:<line\#>: Syntax Error in sub-type specification. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eee83-140">Jeder Modul Syntax Fehler zwischen den Klammern in einer Untertyp Spezifikation generiert diese Meldung.</span><span class="sxs-lookup"><span data-stu-id="eee83-140">Any module syntax error between the parentheses in a sub-type specification generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-219"></a><span data-ttu-id="eee83-141">Schwerwiegender Fehler 219</span><span class="sxs-lookup"><span data-stu-id="eee83-141">Fatal Error 219</span></span>

<dl> <dt>

<span data-ttu-id="eee83-142"><span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219, schwerwiegender>: " <fileName> : <line \#>: Syntax Fehler in der Größenangabe. Letzter gelesener Token ist <token> "**</span><span class="sxs-lookup"><span data-stu-id="eee83-142"><span id="_219__Fatal____fileName___line____Syntax_Error_in_the_SIZE_specification._Last_token_read_is__token__"></span><span id="_219__fatal____filename___line____syntax_error_in_the_size_specification._last_token_read_is__token__"></span><span id="_219__FATAL____FILENAME___LINE____SYNTAX_ERROR_IN_THE_SIZE_SPECIFICATION._LAST_TOKEN_READ_IS__TOKEN__"></span>**<219, Fatal>:"<fileName>:<line\#>: Syntax Error in the SIZE specification. Last token read is <token>"**</span></span>
</dt> <dd>

<span data-ttu-id="eee83-143">Jeder Modul Syntax Fehler in der size-Klausel zwischen der linken und der rechten Klammer generiert diese Meldung.</span><span class="sxs-lookup"><span data-stu-id="eee83-143">Any module syntax error in the SIZE clause between the left and right parentheses generates this message.</span></span>

</dd> </dl>

## <a name="fatal-error-220"></a><span data-ttu-id="eee83-144">Schwerwiegender Fehler 220</span><span class="sxs-lookup"><span data-stu-id="eee83-144">Fatal Error 220</span></span>

<dl> <dt>

<span data-ttu-id="eee83-145"><span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220, schwerwiegender>: " <fileName> : <line \#>: Objekttyp Aufruf von SNMPv2SMI nicht zulässig"**</span><span class="sxs-lookup"><span data-stu-id="eee83-145"><span id="_220__Fatal____fileName___line____OBJECT-TYPE_invocation_of_SNMPv2SMI_not_allowed_"></span><span id="_220__fatal____filename___line____object-type_invocation_of_snmpv2smi_not_allowed_"></span><span id="_220__FATAL____FILENAME___LINE____OBJECT-TYPE_INVOCATION_OF_SNMPV2SMI_NOT_ALLOWED_"></span>**<220, Fatal>:"<fileName>:<line\#>: OBJECT-TYPE invocation of SNMPv2SMI not allowed"**</span></span>
</dt> <dd>

<span data-ttu-id="eee83-146">Modul Syntax Fehler.</span><span class="sxs-lookup"><span data-stu-id="eee83-146">Module syntax error.</span></span> <span data-ttu-id="eee83-147">Sie haben den SNMPv2C-spezifischen **Objekttyp** Aufruf in der MIB verwendet, haben jedoch den **/v1** -Schalter angegeben, der eine strikte Übereinstimmung mit SNMPv1-Syntax erfordert.</span><span class="sxs-lookup"><span data-stu-id="eee83-147">You have used the SNMPv2C-specific **OBJECT-TYPE** invocation in the MIB, but have specified the **/v1** switch, which requires strict conformance to SNMPv1 syntax.</span></span>

</dd> </dl>

 

 



