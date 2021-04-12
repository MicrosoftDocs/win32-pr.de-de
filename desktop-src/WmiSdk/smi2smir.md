---
description: Der SNMP-Compiler wird als einzelne ausführbare Datei im Befehlszeilen Modus ausgeführt.
ms.assetid: 0e85fe84-dacb-4720-8242-ffa0046780f3
ms.tgt_platform: multiple
title: smi2smir
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a34e1d757293b5ee128f2ce1bc2bd5ec8479d9b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104218307"
---
# <a name="smi2smir"></a><span data-ttu-id="3b1ee-103">smi2smir</span><span class="sxs-lookup"><span data-stu-id="3b1ee-103">smi2smir</span></span>

<span data-ttu-id="3b1ee-104">Der SNMP-Compiler wird als einzelne ausführbare Datei im Befehlszeilen Modus ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-104">The SNMP compiler runs as a single executable file in the command-line mode.</span></span> <span data-ttu-id="3b1ee-105">Der Compiler akzeptiert ein SNMP-Informationsmodul als Eingabe und akzeptiert alle zusätzlichen Module, die zum Auflösen externer Verweise erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-105">The compiler accepts one SNMP information module as input, and accepts any additional modules necessary to resolve external references.</span></span> <span data-ttu-id="3b1ee-106">Verwenden Sie eines der folgenden Beispiele für die Befehlszeilen Syntax.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-106">Use one of the following command-line syntax examples.</span></span>

<span data-ttu-id="3b1ee-107">Weitere Informationen zur Verwendung dieses Compilers finden [Sie unter Einrichten der WMI-SNMP-Umgebung](setting-up-the-wmi-snmp-environment.md).</span><span class="sxs-lookup"><span data-stu-id="3b1ee-107">For more information about when this compiler is used, see [Setting up the WMI SNMP Environment](setting-up-the-wmi-snmp-environment.md).</span></span>

``` syntax
smi2smir [<DiagnosticArgs>] [<VersionArgs>]
     <CommandArgs> <MIB file> [<Import Files>]

smi2smir [<DiagnosticArgs>] <RegistryArgs> [<Directory>]

smi2smir <ModuleInfoArgs> <MIB file>

smi2smir <HelpArgs>
```

## <a name="switches"></a><span data-ttu-id="3b1ee-108">Switches</span><span class="sxs-lookup"><span data-stu-id="3b1ee-108">Switches</span></span>

<dl> <span data-ttu-id="3b1ee-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*Diagnosticargs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3b1ee-109"><dt>

<span id="_DiagnosticArgs_"></span><span id="_diagnosticargs_"></span><span id="_DIAGNOSTICARGS_"></span><*DiagnosticArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3b1ee-110">Der Compiler akzeptiert die folgenden Diagnose Argumente.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-110">The compiler accepts the following diagnostic arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3b1ee-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<** _Diagnose Ebene_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3b1ee-111"><span id="_m__diagnostic-level_"></span><span id="_M__DIAGNOSTIC-LEVEL_"></span>**/m** **<**_diagnostic-level_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-112">Typ der anzuzeigenden Diagnose.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-112">Type of diagnostics to display.</span></span> <span data-ttu-id="3b1ee-113">Der Standardwert ist 2.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-113">The default is 2.</span></span>

<span data-ttu-id="3b1ee-114">Im folgenden finden Sie eine Liste der Werte für die Diagnose Ebene, die festgelegt werden können:</span><span class="sxs-lookup"><span data-stu-id="3b1ee-114">The following is a list of the diagnostic level values that can be set:</span></span>

-   <span data-ttu-id="3b1ee-115">0 = unbeaufsichtigt</span><span class="sxs-lookup"><span data-stu-id="3b1ee-115">0 = Silent</span></span>
-   <span data-ttu-id="3b1ee-116">1 = schwerwiegend</span><span class="sxs-lookup"><span data-stu-id="3b1ee-116">1 = Fatal</span></span>
-   <span data-ttu-id="3b1ee-117">2 = schwerwiegend und Warnung</span><span class="sxs-lookup"><span data-stu-id="3b1ee-117">2 = Fatal and warning</span></span>
-   <span data-ttu-id="3b1ee-118">3 = schwerwiegende, Warn-und Informationsmeldungen</span><span class="sxs-lookup"><span data-stu-id="3b1ee-118">3 = Fatal, warning, and information messages</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<** _Anzahl_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3b1ee-119"><span id="_c__count_"></span><span id="_C__COUNT_"></span>**/c** **<**_count_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-120">Maximale Anzahl von schwerwiegenden und Warnmeldungen, die angezeigt werden sollen. "count" muss eine positive ganze *Zahl* sein.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-120">Maximum number of fatal and warning messages to display; *count* must be a positive decimal integer.</span></span> <span data-ttu-id="3b1ee-121">Wenn **/c** nicht angegeben ist, gibt es keine Beschränkung für die Anzahl von Fehlern, die gemeldet werden können.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-121">If **/c** is not specified, there is no limit to the number of errors that can be reported.</span></span>

<span data-ttu-id="3b1ee-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*Versionargs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3b1ee-122"></dd> </dl> </dd> <dt>

<span id="_VersionArgs_"></span><span id="_versionargs_"></span><span id="_VERSIONARGS_"></span><*VersionArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3b1ee-123">Der Compiler akzeptiert die folgenden Versions Argumente.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-123">The compiler accepts the following version arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3b1ee-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-124"><span id="_v1"></span><span id="_V1"></span>**/v1**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-125">Gibt eine strikte Übereinstimmung mit dem SNMPv1 SMI an.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-125">Specifies strict conformance to the SNMPv1 SMI.</span></span> <span data-ttu-id="3b1ee-126">Der Compiler meldet einen Fehler, wenn er nicht-SNMPv1-Anweisungen erkennt.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-126">The compiler reports an error if it detects non-SNMPv1 statements.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-127"><span id="_v2c"></span><span id="_V2C"></span>**/v2c**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-128">Gibt eine strikte Übereinstimmung mit dem SNMPv2 SMI an.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-128">Specifies strict conformance to the SNMPv2 SMI.</span></span> <span data-ttu-id="3b1ee-129">Der Compiler meldet einen Fehler, wenn er nicht-SNMPv2-Anweisungen erkennt.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-129">The compiler reports an error if it detects non-SNMPv2 statements.</span></span>

<span data-ttu-id="3b1ee-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*"Commandargs"*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3b1ee-130"></dd> </dl> </dd> <dt>

<span id="_CommandArgs_"></span><span id="_commandargs_"></span><span id="_COMMANDARGS_"></span><*CommandArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3b1ee-131">Der Compiler akzeptiert die folgenden Befehlsargumente.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-131">The compiler accepts the following command arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3b1ee-132"><span id="_d"></span><span id="_D"></span>**/d**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-132"><span id="_d"></span><span id="_D"></span>**/d**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-133">Löscht das angegebene Modul aus dem SMIR.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-133">Deletes the specified module from the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-134"><span id="_p"></span><span id="_P"></span>**/p**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-134"><span id="_p"></span><span id="_P"></span>**/p**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-135">Löscht alle Module in SMIR.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-135">Deletes all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-136"><span id="_l"></span><span id="_L"></span>**/l**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-136"><span id="_l"></span><span id="_L"></span>**/l**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-137">Listet alle Module in SMIR auf.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-137">Lists all modules in the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-138"><span id="_lc"></span><span id="_LC"></span>**/lc**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-139">Führt eine lokale Syntax Überprüfung für das Modul aus.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-139">Performs a local syntax check on the module.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/EC** **\[<** _Commandmodifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="3b1ee-140"><span id="_ec___CommandModifier__"></span><span id="_ec___commandmodifier__"></span><span id="_EC___COMMANDMODIFIER__"></span>**/ec** **\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-141">Führt lokale und externe Überprüfungen für das Modul aus.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-141">Performs local and external checks on the module.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**\[ /a <** _Commandmodifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="3b1ee-142"><span id="_a__CommandModifier__"></span><span id="_a__commandmodifier__"></span><span id="_A__COMMANDMODIFIER__"></span>**/a\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-143">Führt lokale und externe Prüfungen durch und lädt das Modul in SMIR.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-143">Performs local and external checks and loads the module into the SMIR.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**\[ /sa ein. <** _Commandmodifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="3b1ee-144"><span id="_sa__CommandModifier__"></span><span id="_sa__commandmodifier__"></span><span id="_SA__COMMANDMODIFIER__"></span>**/sa\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-145">Identisch mit **/a**, funktioniert jedoch im Hintergrund.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-145">Same as **/a**, but works silently.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**\[ /g <** _Commandmodifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="3b1ee-146"><span id="_g__CommandModifier__"></span><span id="_g__commandmodifier__"></span><span id="_G__COMMANDMODIFIER__"></span>**/g\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-147">Generiert eine SMIR. MOF-Datei, die Sie später mit dem MOF-Compiler in WMI laden können.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-147">Generates a SMIR .mof file that you can later load into WMI using the MOF compiler.</span></span> <span data-ttu-id="3b1ee-148">Wird vom SNMP-Klassen Anbieter verwendet, um Klassen dynamisch für einen oder mehrere Namespaces bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-148">Used by the SNMP class provider to provide classes dynamically to one or more namespaces.</span></span> <span data-ttu-id="3b1ee-149">Verwenden Sie diese Option, wenn Sie nicht wissen, welche MISB von den verwalteten SNMP-Geräten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-149">Use this option when you do not know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="3b1ee-150">Der SNMP-Klassen Anbieter überprüft das Gerät zur Laufzeit auf das vorhanden sein dieses MIB und stellt die Klassen dynamisch für den Namespace bereit.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-150">The SNMP class provider checks the device at runtime for the presence of this MIB and supplies the classes dynamically to the namespace.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**\[ /GC <** _Commandmodifier_*_>\]_*</span><span class="sxs-lookup"><span data-stu-id="3b1ee-151"><span id="_gc__CommandModifier__"></span><span id="_gc__commandmodifier__"></span><span id="_GC__COMMANDMODIFIER__"></span>**/gc\[<**_CommandModifier_*_>\]_*</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-152">Generiert eine statische MOF-Datei, die später in WMI als statische Klassen für einen bestimmten Namespace geladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-152">Generates a static .mof file that can be loaded later into WMI as static classes for a particular namespace.</span></span> <span data-ttu-id="3b1ee-153">Verwenden Sie diese Option, wenn Sie wissen, welche MISB von den verwalteten SNMP-Geräten unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-153">Use this option when you know which MIBs are supported by the SNMP devices being managed.</span></span> <span data-ttu-id="3b1ee-154">Sie können die MOF-Datei definieren, die generiert werden soll, indem Sie die Ausgabe des Befehls an eine angegebene Datei weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-154">You can define the .mof file to be generated by directing the output of your command to a specified file.</span></span> <span data-ttu-id="3b1ee-155">Verwenden Sie with **/ext/o** nicht.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-155">Do not use with **/ext/o**.</span></span>

<span data-ttu-id="3b1ee-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*Commandmodifier*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3b1ee-156"></dd> </dl> </dd> <dt>

<span id="_CommandModifiers_"></span><span id="_commandmodifiers_"></span><span id="_COMMANDMODIFIERS_"></span><*CommandModifiers*>
</dt> </span></span><dd>

<span data-ttu-id="3b1ee-157">Der Compiler akzeptiert die folgenden befehlsmodifiziererer.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-157">The compiler accepts the following command modifiers.</span></span>

<dl> <dt>

<span data-ttu-id="3b1ee-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<** _Verzeichnis_*_>_*</span><span class="sxs-lookup"><span data-stu-id="3b1ee-158"><span id="_i_directory_"></span><span id="_I_DIRECTORY_"></span>**/i<**_directory_*_>_*</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-159">Gibt ein Verzeichnis an, das nach abhängigen MIB-Modulen durchsucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-159">Specifies a directory to be searched for dependent MIB modules.</span></span> <span data-ttu-id="3b1ee-160">Verwendung mit **/a**, **/EC**, **/g**, **/GC** und **/sa ein.**.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-160">Use with **/a**, **/ec**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="3b1ee-161">Die **/i** -Option kann mehrmals im Befehl angezeigt werden. Verzeichnisse werden in der im Befehl angegebenen Reihenfolge durchsucht.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-161">The **/i** option can appear multiple times in the command; directories are searched in the order specified in the command.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-162"><span id="_ch"></span><span id="_CH"></span>**/ch**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-162"><span id="_ch"></span><span id="_CH"></span>**/ch**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-163">Generiert Kontextinformationen, z. b. Datum, Uhrzeit, Host oder Benutzer, im MOF-Dateiheader.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-163">Generates context information, such as the date, time, host, or user, in the MOF file header.</span></span> <span data-ttu-id="3b1ee-164">Verwendung mit **/g** und **/GC**.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-164">Use with **/g** and **/gc**.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-165"><span id="_t"></span><span id="_T"></span>**/t**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-165"><span id="_t"></span><span id="_T"></span>**/t**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-166">Generiert [SnmpNotification](snmpnotification.md) -Klassen.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-166">Generates [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="3b1ee-167">Verwenden Sie mit **/a**, **/g** und **/sa ein.**.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-167">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-168"><span id="_ext"></span><span id="_EXT"></span>**/ext**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-169">Generiert [snmpextendednotification](snmpextendednotification.md) -Klassen.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-169">Generates [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="3b1ee-170">Verwenden Sie mit **/a**, **/g** und **/sa ein.**.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-170">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-171"><span id="_t_o"></span><span id="_T_O"></span>**/t/o**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-172">Generiert nur [SnmpNotification](snmpnotification.md) -Klassen.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-172">Generates only [SnmpNotification](snmpnotification.md) classes.</span></span> <span data-ttu-id="3b1ee-173">Verwenden Sie mit **/a**, **/g** und **/sa ein.**.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-173">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-174"><span id="_ext_o"></span><span id="_EXT_O"></span>**/ext/o**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-175">Generiert nur [snmpextendednotification](snmpextendednotification.md) -Klassen.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-175">Generates only [SnmpExtendedNotification](snmpextendednotification.md) classes.</span></span> <span data-ttu-id="3b1ee-176">Verwenden Sie mit **/a**, **/g** und **/sa ein.**.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-176">Use with **/a**, **/g**, and **/sa**.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-177"><span id="_s"></span><span id="_S"></span>**/s**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-177"><span id="_s"></span><span id="_S"></span>**/s**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-178">Ordnet den Text der Description-Klausel nicht zu.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-178">Does not map the text of the DESCRIPTION clause.</span></span> <span data-ttu-id="3b1ee-179">Verwendung mit **/a**, **/g**, **/GC** und **/sa ein.**.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-179">Use with **/a**, **/g**, **/gc**, and **/sa**.</span></span> <span data-ttu-id="3b1ee-180">Verwenden Sie diese Option, wenn Sie die Speicheranforderungen minimieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-180">Use this option when you want to minimize storage requirements.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-181"><span id="_auto"></span><span id="_AUTO"></span>**/Auto**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-181"><span id="_auto"></span><span id="_AUTO"></span>**/auto**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-182">Erstellt die MIB-Nachschlage Tabelle neu, bevor die <*commandarg*> Switch abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-182">Rebuilds the MIB lookup table before completing the <*CommandArg*> switch.</span></span> <span data-ttu-id="3b1ee-183">Verwendung mit **/a**, **/EC**, **/g** und **/GC**.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-183">Use with **/a**, **/ec**, **/g**, and **/gc**.</span></span>

<span data-ttu-id="3b1ee-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*Registryargs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3b1ee-184"></dd> </dl> </dd> <dt>

<span id="_RegistryArgs_"></span><span id="_registryargs_"></span><span id="_REGISTRYARGS_"></span><*RegistryArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3b1ee-185">Der Compiler akzeptiert die folgenden Registrierungs Argumente.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-185">The compiler accepts the following registry arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3b1ee-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-186"><span id="_pa"></span><span id="_PA"></span>**/pa**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-187">Fügt der Registrierung das angegebene Verzeichnis hinzu.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-187">Adds the specified directory to the registry.</span></span> <span data-ttu-id="3b1ee-188">Der Standardwert ist das aktuelle Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-188">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-189"><span id="_pd"></span><span id="_PD"></span>**/PD**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-189"><span id="_pd"></span><span id="_PD"></span>**/pd**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-190">Löscht das angegebene Verzeichnis aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-190">Deletes the specified directory from the registry.</span></span> <span data-ttu-id="3b1ee-191">Der Standardwert ist das aktuelle Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-191">The default is the current directory.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-192"><span id="_pl"></span><span id="_PL"></span>**"/pl"**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-192"><span id="_pl"></span><span id="_PL"></span>**/pl**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-193">Listet die MIB-Such Verzeichnisse in der Registrierung auf.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-193">Lists the MIB lookup directories in the registry.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-194"><span id="_r"></span><span id="_R"></span>**/r**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-194"><span id="_r"></span><span id="_R"></span>**/r**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-195">Erstellt die gesamte MIB-Nachschlage Tabelle neu.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-195">Rebuilds the entire MIB lookup table.</span></span>

<span data-ttu-id="3b1ee-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*Moduleinfoargs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3b1ee-196"></dd> </dl> </dd> <dt>

<span id="_ModuleInfoArgs_"></span><span id="_moduleinfoargs_"></span><span id="_MODULEINFOARGS_"></span><*ModuleInfoArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3b1ee-197">Der Compiler akzeptiert die folgenden Modul Informations Argumente.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-197">The compiler accepts the following module information arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3b1ee-198"><span id="_n"></span><span id="_N"></span>**/n**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-198"><span id="_n"></span><span id="_N"></span>**/n**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-199">Gibt den ASN. 1-Namen des angegebenen Moduls zurück.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-199">Returns the ASN.1 name of the specified module.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-200"><span id="_ni"></span><span id="_NI"></span>**/ni**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-201">Gibt die ASN. 1-Namen aller Import Module zurück, auf die vom Eingabe Modul verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-201">Returns the ASN.1 names of all import modules referred to by the input module.</span></span>

<span data-ttu-id="3b1ee-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*Helparamegs*>
</dt> </span><span class="sxs-lookup"><span data-stu-id="3b1ee-202"></dd> </dl> </dd> <dt>

<span id="_HelpArgs_"></span><span id="_helpargs_"></span><span id="_HELPARGS_"></span><*HelpArgs*>
</dt> </span></span><dd>

<span data-ttu-id="3b1ee-203">Der Compiler akzeptiert die folgenden Hilfe Argumente.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-203">The compiler accepts the following help arguments.</span></span>

<dl> <dt>

<span data-ttu-id="3b1ee-204"><span id="_h"></span><span id="_H"></span>**/h**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-204"><span id="_h"></span><span id="_H"></span>**/h**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-205">Zeigt die Hilfe zur SNMP-compilersyntax an.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-205">Displays help on the SNMP compiler syntax.</span></span>

</dd> <dt>

<span data-ttu-id="3b1ee-206"><span id="__"></span>**/?**</span><span class="sxs-lookup"><span data-stu-id="3b1ee-206"><span id="__"></span>**/?**</span></span>
</dt> <dd>

<span data-ttu-id="3b1ee-207">Zeigt die Hilfe zur SNMP-compilersyntax an.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-207">Displays help on the SNMP compiler syntax.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3b1ee-208">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b1ee-208">Remarks</span></span>

<span data-ttu-id="3b1ee-209">SNMP-Informationsmodule werden in einer Teilmenge der abstrakten Syntax Notation One (ASN. 1) geschrieben, der der Compiler die folgenden Funktionen ausführt:</span><span class="sxs-lookup"><span data-stu-id="3b1ee-209">SNMP information modules are written in a subset of the Abstract Syntax Notation One (ASN.1) The compiler performs the following functions:</span></span>

-   <span data-ttu-id="3b1ee-210">Lädt die Daten aus dem SNMP-Informationsmodul.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-210">Loads the data from the SNMP information module.</span></span>
-   <span data-ttu-id="3b1ee-211">Überprüfungsvorgänge für das Informationsmodul.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-211">Performs checking operations on the information module.</span></span> <span data-ttu-id="3b1ee-212">Er überprüft beispielsweise die lokale Syntax und überprüft externe Verweise auf Informationen in den Tochter Modulen.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-212">For example, it checks the local syntax and it checks external references against information in the subsidiary modules.</span></span>
-   <span data-ttu-id="3b1ee-213">Entfernen aller zuvor geladenen Daten aus dem SMIR oder Entfernen geladener Daten aus einem Informationsmodul.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-213">Removes all previously loaded data from the SMIR, or removes data loaded from one information module.</span></span>
-   <span data-ttu-id="3b1ee-214">Gibt den ASN. 1-Modulnamen einer angegebenen Datei zurück oder gibt die ASN. 1-Modulnamen aller importierten Module in einer angegebenen Datei zurück.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-214">Returns the ASN.1 module name of a specified file or returns the ASN.1 module names of all imported modules in a specified file.</span></span>
-   <span data-ttu-id="3b1ee-215">Zurückgeben der ASN.1-Modulnamen aller derzeit im SMIR geladenen SNMP-Informationsmodule.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-215">Returns the ASN.1 module names of all SNMP information modules currently loaded in the SMIR.</span></span>
-   <span data-ttu-id="3b1ee-216">Führt die automatische Auflösung importierter Module durch und erfordert nicht, dass Benutzer die erforderlichen Module manuell angeben müssen.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-216">Performs automatic resolution of imported modules rather than requiring users to specify the required modules manually.</span></span>
-   <span data-ttu-id="3b1ee-217">Führt einen Vorgang zum automatischen Laden aus, der keine Ausgabe generiert, aber zum Laden von Daten in SMIR während eines Installationsvorgangs verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-217">Performs a silent-loading mode of operation that does not generate any output, but can be used to load data into the SMIR during an installation operation.</span></span>
-   <span data-ttu-id="3b1ee-218">Gibt die Daten aus dem SNMP-Informationsmodul in SMIR aus.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-218">Outputs the data from the SNMP information module into the SMIR.</span></span>
-   <span data-ttu-id="3b1ee-219">Erstellt optional eine statische oder SMIR-MOF-Datei, die die Ausgabe des Informations Moduls enthält.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-219">Optionally creates a static or SMIR MOF file containing the output from the information module.</span></span>

    <span data-ttu-id="3b1ee-220">Falls erforderlich, können Sie die Datei "static. mof" in einen WMI-Namespace laden.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-220">If necessary, you can load the static .mof file into a WMI namespace.</span></span> <span data-ttu-id="3b1ee-221">Eine SMIR. MOF-Datei enthält den Namen des SNMP-Namespace, in dem sich die Klassen befinden sollten.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-221">A SMIR .mof file contains the name of the SNMP namespace in which the classes should reside.</span></span>

## <a name="examples"></a><span data-ttu-id="3b1ee-222">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3b1ee-222">Examples</span></span>

<span data-ttu-id="3b1ee-223">Im folgenden Beispiel wird die Datei "Pra. mof" als Ausgabe aus der Datei "Pra. MIB" definiert.</span><span class="sxs-lookup"><span data-stu-id="3b1ee-223">The following example defines the pra.mof file to be the output from the pra.mib file.</span></span>

``` syntax
smi2smir /m 3 /v1 /gc /pra.mib > pra.mof
```

## <a name="requirements"></a><span data-ttu-id="3b1ee-224">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b1ee-224">Requirements</span></span>



| <span data-ttu-id="3b1ee-225">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3b1ee-225">Requirement</span></span> | <span data-ttu-id="3b1ee-226">Wert</span><span class="sxs-lookup"><span data-stu-id="3b1ee-226">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="3b1ee-227">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3b1ee-227">Minimum supported client</span></span><br/> | <span data-ttu-id="3b1ee-228">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3b1ee-228">Windows Vista</span></span><br/>       |
| <span data-ttu-id="3b1ee-229">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3b1ee-229">Minimum supported server</span></span><br/> | <span data-ttu-id="3b1ee-230">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3b1ee-230">Windows Server 2008</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="3b1ee-231">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b1ee-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b1ee-232">SNMP-Compilerfehlermeldungen</span><span class="sxs-lookup"><span data-stu-id="3b1ee-232">SNMP Compiler Error Messages</span></span>](snmp-compiler-error-messages.md)
</dt> <dt>

[<span data-ttu-id="3b1ee-233">Einrichten der WMI-SNMP-Umgebung</span><span class="sxs-lookup"><span data-stu-id="3b1ee-233">Setting up the WMI SNMP Environment</span></span>](setting-up-the-wmi-snmp-environment.md)
</dt> <dt>

[<span data-ttu-id="3b1ee-234">Zugreifen auf SNMP-Geräte</span><span class="sxs-lookup"><span data-stu-id="3b1ee-234">Accessing SNMP Devices</span></span>](accessing-snmp-devices.md)
</dt> </dl>

 

 




