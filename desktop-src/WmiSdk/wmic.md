---
description: Das WMI-Befehlszeilen Hilfsprogramm (WMIC) stellt eine Befehlszeilenschnittstelle für WMI bereit.
ms.assetid: a0f5c1e2-9a4d-4c2b-b324-58ec01e67b6e
ms.tgt_platform: multiple
title: wmic
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 070b21cb21381fb989b81795a6c7e0b787b5c89a
ms.sourcegitcommit: 556bf3a984f2fc4d18e370329c3043bf3329c93f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/09/2021
ms.locfileid: "107222928"
---
# <a name="wmic"></a><span data-ttu-id="17628-103">wmic</span><span class="sxs-lookup"><span data-stu-id="17628-103">wmic</span></span>

<span data-ttu-id="17628-104">Das WMI-Befehlszeilen Hilfsprogramm (WMIC) stellt eine Befehlszeilenschnittstelle für Windows-Verwaltungsinstrumentation (WMI) bereit.</span><span class="sxs-lookup"><span data-stu-id="17628-104">The WMI command-line (WMIC) utility provides a command-line interface for Windows Management Instrumentation (WMI).</span></span> <span data-ttu-id="17628-105">WMIC ist kompatibel mit vorhandenen Shells und Utility-Befehlen.</span><span class="sxs-lookup"><span data-stu-id="17628-105">WMIC is compatible with existing shells and utility commands.</span></span> <span data-ttu-id="17628-106">Im folgenden finden Sie ein Allgemeines Referenz Thema für WMIC.</span><span class="sxs-lookup"><span data-stu-id="17628-106">The following is a general reference topic for WMIC.</span></span> <span data-ttu-id="17628-107">Weitere Informationen und Richtlinien zur Verwendung von WMIC, einschließlich zusätzlicher Informationen zu Aliasen, Verben, Switches und Befehlen, finden [Sie unter Using Windows-Verwaltungsinstrumentation Command-Line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) und [WMIC-Take Command-Line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span><span class="sxs-lookup"><span data-stu-id="17628-107">For more information and guidelines on how to use WMIC, including additional information on aliases, verbs, switches, and commands, see [Using Windows Management Instrumentation Command-line](/previous-versions/windows/it-pro/windows-server-2003/cc779482(v=ws.10)) and [WMIC - Take Command-line Control over WMI](/previous-versions/windows/it-pro/windows-2000-server/bb742610(v=technet.10)).</span></span>

## <a name="alias"></a><span data-ttu-id="17628-108">Alias</span><span class="sxs-lookup"><span data-stu-id="17628-108">Alias</span></span>

<span data-ttu-id="17628-109">Ein Alias ist ein benutzerfreundliches Umbenennen einer Klasse, einer Eigenschaft oder einer Methode, die das verwenden und Lesen von WMI erleichtert.</span><span class="sxs-lookup"><span data-stu-id="17628-109">An alias is a friendly renaming of a class, property, or method that makes WMI easier to use and read.</span></span> <span data-ttu-id="17628-110">Sie können bestimmen, welche Aliase für WMIC verfügbar sind, indem Sie **/?**</span><span class="sxs-lookup"><span data-stu-id="17628-110">You can determine what aliases are available for WMIC through the **/?**</span></span> <span data-ttu-id="17628-111">ausführen.</span><span class="sxs-lookup"><span data-stu-id="17628-111">command.</span></span> <span data-ttu-id="17628-112">Sie können die Aliase für eine bestimmte Klasse auch mit dem **<className> /?**</span><span class="sxs-lookup"><span data-stu-id="17628-112">You can also determine the aliases for a specific class using the **<className> /?**</span></span> <span data-ttu-id="17628-113">ausführen.</span><span class="sxs-lookup"><span data-stu-id="17628-113">command.</span></span> <span data-ttu-id="17628-114">Weitere Informationen finden Sie unter [WMIC Aliases](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="17628-114">For more information, see [WMIC Aliases](/previous-versions/windows/it-pro/windows-server-2003/cc736307(v=ws.10)).</span></span>

## <a name="switch"></a><span data-ttu-id="17628-115">Schalter</span><span class="sxs-lookup"><span data-stu-id="17628-115">Switch</span></span>

<span data-ttu-id="17628-116">Ein Switch ist eine WMIC-Option, die Sie Global oder optional festlegen können.</span><span class="sxs-lookup"><span data-stu-id="17628-116">A switch is a WMIC option you can set globally or optionally.</span></span> <span data-ttu-id="17628-117">Eine Liste der verfügbaren Switches finden Sie unter [WMIC Switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="17628-117">For a list of available switches, see [WMIC Switches](/previous-versions/windows/it-pro/windows-server-2003/cc787035(v=ws.10)).</span></span>

## <a name="verbs"></a><span data-ttu-id="17628-118">Verben</span><span class="sxs-lookup"><span data-stu-id="17628-118">Verbs</span></span>

<span data-ttu-id="17628-119">Geben Sie den Aliasnamen gefolgt vom Verb ein, um Verben in WMIC zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="17628-119">To use verbs in WMIC, enter the alias name followed by the verb.</span></span> <span data-ttu-id="17628-120">Wenn ein-Alias kein Verb unterstützt, erhalten Sie die Meldung, dass der Anbieter nicht in der Lage ist, den Vorgang auszuführen.</span><span class="sxs-lookup"><span data-stu-id="17628-120">If an alias does not support a verb, you receive the message "provider is not capable of the attempted operation."</span></span> <span data-ttu-id="17628-121">Weitere Informationen finden Sie unter [WMIC Verbs](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="17628-121">For more information, see [WMIC Verbs](/previous-versions/windows/it-pro/windows-server-2003/cc784966(v=ws.10)).</span></span>

<span data-ttu-id="17628-122">Die meisten Aliase unterstützen die folgenden Verben.</span><span class="sxs-lookup"><span data-stu-id="17628-122">Most aliases support the following verbs.</span></span>

<dl> <dt>

<span data-ttu-id="17628-123"><span id="ASSOC"></span><span id="assoc"></span>Assoc</span><span class="sxs-lookup"><span data-stu-id="17628-123"><span id="ASSOC"></span><span id="assoc"></span>ASSOC</span></span>
</dt> <dd>

<span data-ttu-id="17628-124">Gibt das Ergebnis der Abfrage zurück, `Associators of (<wmi_object>)` bei der *<WMI- \_ Objekt>* der Pfad von Objekten ist, die von den **path** -oder **Class** -Befehlen zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="17628-124">Returns the result of the `Associators of (<wmi_object>)` query where *<wmi\_object>* is the path of objects returned by the **PATH** or **CLASS** commands.</span></span> <span data-ttu-id="17628-125">Die Ergebnisse sind Instanzen, die dem-Objekt zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="17628-125">The results are instances associated with the object.</span></span> <span data-ttu-id="17628-126">Wenn Assoc mit einem Alias verwendet wird, werden die Klassen mit der Klasse zurückgegeben, die dem Alias zugrunde liegt.</span><span class="sxs-lookup"><span data-stu-id="17628-126">When ASSOC is used with an alias, the classes with the class underlying the alias are returned.</span></span> <span data-ttu-id="17628-127">Standardmäßig wird die Ausgabe im HTML-Format zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="17628-127">By default the output is returned in HTML format.</span></span>

<span data-ttu-id="17628-128">Das Assoc-Verb verfügt über die folgenden Schalter.</span><span class="sxs-lookup"><span data-stu-id="17628-128">The ASSOC verb has the following switches.</span></span>



| <span data-ttu-id="17628-129">Schalter</span><span class="sxs-lookup"><span data-stu-id="17628-129">Switch</span></span>                         | <span data-ttu-id="17628-130">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17628-130">Description</span></span>                                                                                                       |
|--------------------------------|-------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17628-131">/RESULTCLASS:<classname></span><span class="sxs-lookup"><span data-stu-id="17628-131">/RESULTCLASS:<classname></span></span> | <span data-ttu-id="17628-132">Zurückgegebene Endpunkte, die dem Quell Objekt zugeordnet sind, müssen zu der angegebenen Klasse gehören oder davon abgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="17628-132">Returned endpoints associated with the source object must belong to, or be derived from the specified class.</span></span>      |
| <span data-ttu-id="17628-133">/RESULTROLE:<rolename></span><span class="sxs-lookup"><span data-stu-id="17628-133">/RESULTROLE:<rolename></span></span>   | <span data-ttu-id="17628-134">Zurückgegebene Endpunkte müssen eine bestimmte Rolle in Zuordnungen mit dem Quell Objekt wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="17628-134">Returned endpoints must play a specific role in associations with the source object.</span></span>                              |
| <span data-ttu-id="17628-135">/ASSOCCLASS:<assocclass></span><span class="sxs-lookup"><span data-stu-id="17628-135">/ASSOCCLASS:<assocclass></span></span> | <span data-ttu-id="17628-136">Zurückgegebene Endpunkte müssen mithilfe der angegebenen Klasse oder einer davon abgeleiteten Klasse mit der Quelle verknüpft werden.</span><span class="sxs-lookup"><span data-stu-id="17628-136">Returned endpoints must be associated with the source through the specified class, or one of its derived classes.</span></span> |



 

<span data-ttu-id="17628-137">Beispiel: **OS Assoc**</span><span class="sxs-lookup"><span data-stu-id="17628-137">Example: **OS ASSOC**</span></span>

</dd> <dt>

<span data-ttu-id="17628-138"><span id="CALL"></span><span id="call"></span>Erfordern</span><span class="sxs-lookup"><span data-stu-id="17628-138"><span id="CALL"></span><span id="call"></span>CALL</span></span>
</dt> <dd>

<span data-ttu-id="17628-139">Führt eine Methode aus.</span><span class="sxs-lookup"><span data-stu-id="17628-139">Executes a method.</span></span>

<span data-ttu-id="17628-140">Beispiel: **Dienst, bei dem Caption = ' Telnet ' den StartService aufruft**</span><span class="sxs-lookup"><span data-stu-id="17628-140">Example: **SERVICE WHERE CAPTION='TELNET' CALL STARTSERVICE**</span></span>

> [!Note]  
> <span data-ttu-id="17628-141">Verwenden Sie **/?**, um die verfügbaren Methoden für eine bestimmte Klasse zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="17628-141">To determine the methods available for a given class, use **/?**.</span></span> <span data-ttu-id="17628-142">Beispiel: **Dienst, bei dem Caption = ' Telnet ' aufgerufen/?**</span><span class="sxs-lookup"><span data-stu-id="17628-142">For example, **SERVICE WHERE CAPTION='TELNET' CALL /?**</span></span> <span data-ttu-id="17628-143">Listet die verfügbaren Funktionen für die Dienstklasse auf.</span><span class="sxs-lookup"><span data-stu-id="17628-143">lists the available functions for the service class.</span></span>

 

</dd> <dt>

<span data-ttu-id="17628-144"><span id="CREATE"></span><span id="create"></span>Stelle</span><span class="sxs-lookup"><span data-stu-id="17628-144"><span id="CREATE"></span><span id="create"></span>CREATE</span></span>
</dt> <dd>

<span data-ttu-id="17628-145">Erstellt eine neue-Instanz und legt die Eigenschaftswerte fest.</span><span class="sxs-lookup"><span data-stu-id="17628-145">Creates a new instance and sets the property values.</span></span> <span data-ttu-id="17628-146">Create kann nicht zum Erstellen einer neuen Klasse verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17628-146">CREATE cannot be used to create a new class.</span></span>

<span data-ttu-id="17628-147">Beispiel: **Environment Create Name = "Temp"; VariableValue = "New"**</span><span class="sxs-lookup"><span data-stu-id="17628-147">Example: **ENVIRONMENT CREATE NAME="TEMP"; VARIABLEVALUE="NEW"**</span></span>

</dd> <dt>

<span data-ttu-id="17628-148"><span id="DELETE"></span><span id="delete"></span>Lösch</span><span class="sxs-lookup"><span data-stu-id="17628-148"><span id="DELETE"></span><span id="delete"></span>DELETE</span></span>
</dt> <dd>

<span data-ttu-id="17628-149">Löscht die aktuelle Instanz oder den Satz von Instanzen.</span><span class="sxs-lookup"><span data-stu-id="17628-149">Deletes the current instance or set of instances.</span></span> <span data-ttu-id="17628-150">DELETE kann verwendet werden, um eine Klasse zu löschen.</span><span class="sxs-lookup"><span data-stu-id="17628-150">DELETE can be used to delete a class.</span></span>

<span data-ttu-id="17628-151">Beispiel: **Process WHERE Name = "CALC.EXE" Delete**</span><span class="sxs-lookup"><span data-stu-id="17628-151">Example: **PROCESS WHERE NAME="CALC.EXE" DELETE**</span></span>

</dd> <dt>

<span data-ttu-id="17628-152"><span id="GET"></span><span id="get"></span>Erhalten</span><span class="sxs-lookup"><span data-stu-id="17628-152"><span id="GET"></span><span id="get"></span>GET</span></span>
</dt> <dd>

<span data-ttu-id="17628-153">Ruft bestimmte Eigenschaftswerte ab.</span><span class="sxs-lookup"><span data-stu-id="17628-153">Retrieve specific property values.</span></span>

<span data-ttu-id="17628-154">Get verfügt über die folgenden Schalter.</span><span class="sxs-lookup"><span data-stu-id="17628-154">GET has the following switches.</span></span>



| <span data-ttu-id="17628-155">Schalter</span><span class="sxs-lookup"><span data-stu-id="17628-155">Switch</span></span>                               | <span data-ttu-id="17628-156">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17628-156">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17628-157">/Value</span><span class="sxs-lookup"><span data-stu-id="17628-157">/VALUE</span></span>                               | <span data-ttu-id="17628-158">Die Ausgabe wird mit jedem Wert formatiert, der in einer separaten Zeile und mit dem Namen der Eigenschaft aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="17628-158">Output is formatted with each value listed on a separate line and with the name of the property.</span></span>                                           |
| <span data-ttu-id="17628-159">/ALL</span><span class="sxs-lookup"><span data-stu-id="17628-159">/ALL</span></span>                                 | <span data-ttu-id="17628-160">Die Ausgabe wird als Tabelle formatiert.</span><span class="sxs-lookup"><span data-stu-id="17628-160">Output is formatted as a table.</span></span>                                                                                                            |
| <span data-ttu-id="17628-161">Tragen<translation table></span><span class="sxs-lookup"><span data-stu-id="17628-161">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="17628-162">Übersetzen Sie die Ausgabe mithilfe der Übersetzungstabelle, die durch den Befehl benannt wird.</span><span class="sxs-lookup"><span data-stu-id="17628-162">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="17628-163">Die Übersetzungstabellen BasicXML und NoComma sind in WMIC enthalten.</span><span class="sxs-lookup"><span data-stu-id="17628-163">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="17628-164">Jeden<interval></span><span class="sxs-lookup"><span data-stu-id="17628-164">/EVERY:<interval></span></span>              | <span data-ttu-id="17628-165">Wiederholen Sie den Befehl alle <interval> Sekunden.</span><span class="sxs-lookup"><span data-stu-id="17628-165">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="17628-166">Ges<format specifier></span><span class="sxs-lookup"><span data-stu-id="17628-166">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="17628-167">Gibt ein Schlüsselwort oder einen XSL-Dateinamen an, um die Daten zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="17628-167">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="17628-168">Beispiel: **Process Get Name**</span><span class="sxs-lookup"><span data-stu-id="17628-168">Example: **PROCESS GET NAME**</span></span>

</dd> <dt>

<span data-ttu-id="17628-169"><span id="LIST"></span><span id="list"></span>List</span><span class="sxs-lookup"><span data-stu-id="17628-169"><span id="LIST"></span><span id="list"></span>LIST</span></span>
</dt> <dd>

<span data-ttu-id="17628-170">Zeigt Daten an.</span><span class="sxs-lookup"><span data-stu-id="17628-170">Shows data.</span></span> <span data-ttu-id="17628-171">List ist das Standardverb.</span><span class="sxs-lookup"><span data-stu-id="17628-171">LIST is the default verb.</span></span>

<span data-ttu-id="17628-172">Die Liste enthält die folgenden adversb.</span><span class="sxs-lookup"><span data-stu-id="17628-172">LIST has the following adverbs.</span></span>



| <span data-ttu-id="17628-173">Adverbfilter</span><span class="sxs-lookup"><span data-stu-id="17628-173">Adverb</span></span>   | <span data-ttu-id="17628-174">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="17628-174">Description</span></span>                                                  |
|----------|--------------------------------------------------------------|
| <span data-ttu-id="17628-175">KURZ</span><span class="sxs-lookup"><span data-stu-id="17628-175">BRIEF</span></span>    | <span data-ttu-id="17628-176">Der Kernsatz der Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17628-176">Core set of the properties.</span></span>                                  |
| <span data-ttu-id="17628-177">FULL</span><span class="sxs-lookup"><span data-stu-id="17628-177">FULL</span></span>     | <span data-ttu-id="17628-178">Vollständiger Satz von Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17628-178">Full set of properties.</span></span> <span data-ttu-id="17628-179">Dies ist das standardmäßige adverbfilter für List.</span><span class="sxs-lookup"><span data-stu-id="17628-179">This is the default adverb for LIST.</span></span> |
| <span data-ttu-id="17628-180">INSTANCE</span><span class="sxs-lookup"><span data-stu-id="17628-180">INSTANCE</span></span> | <span data-ttu-id="17628-181">Nur Instanzpfade.</span><span class="sxs-lookup"><span data-stu-id="17628-181">Instance paths only.</span></span>                                         |
| <span data-ttu-id="17628-182">STATUS</span><span class="sxs-lookup"><span data-stu-id="17628-182">STATUS</span></span>   | <span data-ttu-id="17628-183">Der Status der Objekte.</span><span class="sxs-lookup"><span data-stu-id="17628-183">Status of the objects.</span></span>                                       |
| <span data-ttu-id="17628-184">SYSTEM</span><span class="sxs-lookup"><span data-stu-id="17628-184">SYSTEM</span></span>   | <span data-ttu-id="17628-185">Systemeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="17628-185">System properties.</span></span>                                           |



 

<span data-ttu-id="17628-186">Die Liste enthält die folgenden Schalter.</span><span class="sxs-lookup"><span data-stu-id="17628-186">LIST has the following switches.</span></span>



| <span data-ttu-id="17628-187">Schalter</span><span class="sxs-lookup"><span data-stu-id="17628-187">Switch</span></span>                               | <span data-ttu-id="17628-188">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="17628-188">Description</span></span>                                                                                                                                |
|--------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17628-189">Tragen<translation table></span><span class="sxs-lookup"><span data-stu-id="17628-189">/TRANSLATE:<translation table></span></span> | <span data-ttu-id="17628-190">Übersetzen Sie die Ausgabe mithilfe der Übersetzungstabelle, die durch den Befehl benannt wird.</span><span class="sxs-lookup"><span data-stu-id="17628-190">Translate the output using the translation table named by the command.</span></span> <span data-ttu-id="17628-191">Die Übersetzungstabellen BasicXML und NoComma sind in WMIC enthalten.</span><span class="sxs-lookup"><span data-stu-id="17628-191">The translation tables BasicXml and NoComma are included with WMIC.</span></span> |
| <span data-ttu-id="17628-192">Jeden<interval></span><span class="sxs-lookup"><span data-stu-id="17628-192">/EVERY:<interval></span></span>              | <span data-ttu-id="17628-193">Wiederholen Sie den Befehl alle <interval> Sekunden.</span><span class="sxs-lookup"><span data-stu-id="17628-193">Repeat the command every <interval> seconds.</span></span>                                                                                         |
| <span data-ttu-id="17628-194">Ges<format specifier></span><span class="sxs-lookup"><span data-stu-id="17628-194">/FORMAT:<format specifier></span></span>     | <span data-ttu-id="17628-195">Gibt ein Schlüsselwort oder einen XSL-Dateinamen an, um die Daten zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="17628-195">Specifies a key word or XSL file name to format the data.</span></span>                                                                                  |



 

<span data-ttu-id="17628-196">Beispiel: **Prozesslisten Brief**</span><span class="sxs-lookup"><span data-stu-id="17628-196">Example: **PROCESS LIST BRIEF**</span></span>

</dd> <dt>

<span data-ttu-id="17628-197"><span id="SET"></span><span id="set"></span>Set</span><span class="sxs-lookup"><span data-stu-id="17628-197"><span id="SET"></span><span id="set"></span>SET</span></span>
</dt> <dd>

<span data-ttu-id="17628-198">Weist Eigenschaften Werte zu.</span><span class="sxs-lookup"><span data-stu-id="17628-198">Assigns values to properties.</span></span> <span data-ttu-id="17628-199">Beispiel: **Umgebungs Satz Name = "Temp"**, **VariableValue = "New"**</span><span class="sxs-lookup"><span data-stu-id="17628-199">Example: **ENVIRONMENT SET NAME="TEMP"**, **VARIABLEVALUE="NEW"**</span></span>

</dd> </dl>

## <a name="switches"></a><span data-ttu-id="17628-200">Switches</span><span class="sxs-lookup"><span data-stu-id="17628-200">Switches</span></span>

<span data-ttu-id="17628-201">Globale Switches werden verwendet, um Standardwerte für die WMIC-Umgebung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="17628-201">Global switches are used to set defaults for the WMIC environment.</span></span> <span data-ttu-id="17628-202">Sie können den aktuellen Wert der von diesen Schaltern festgelegten Bedingungen anzeigen, indem Sie den **Kontext** Befehl eingeben.</span><span class="sxs-lookup"><span data-stu-id="17628-202">You can view the current value of the conditions set by these switches by entering the **CONTEXT** command.</span></span>

<dl> <dt>

<span data-ttu-id="17628-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/Namespace</span><span class="sxs-lookup"><span data-stu-id="17628-203"><span id="_NAMESPACE"></span><span id="_namespace"></span>/NAMESPACE</span></span>
</dt> <dd>

<span data-ttu-id="17628-204">Der Namespace, der vom Alias verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17628-204">Namespace the alias uses typically.</span></span> <span data-ttu-id="17628-205">Der Standardwert ist root \\ CIMV2.</span><span class="sxs-lookup"><span data-stu-id="17628-205">The default is root\\cimv2.</span></span>

<span data-ttu-id="17628-206">Beispiel: **/Namespace: \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="17628-206">Example: **/NAMESPACE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="17628-207"><span id="_ROLE"></span><span id="_role"></span>/Role</span><span class="sxs-lookup"><span data-stu-id="17628-207"><span id="_ROLE"></span><span id="_role"></span>/ROLE</span></span>
</dt> <dd>

<span data-ttu-id="17628-208">Namespace-WMIC sucht in der Regel nach Aliasen und anderen WMIC-Informationen.</span><span class="sxs-lookup"><span data-stu-id="17628-208">Namespace WMIC typically looks in for aliases and other WMIC information.</span></span>

<span data-ttu-id="17628-209">Beispiel: **/role: \\ \\ root**</span><span class="sxs-lookup"><span data-stu-id="17628-209">Example: **/ROLE:\\\\root**</span></span>

</dd> <dt>

<span data-ttu-id="17628-210"><span id="_NODE"></span><span id="_node"></span>/Node</span><span class="sxs-lookup"><span data-stu-id="17628-210"><span id="_NODE"></span><span id="_node"></span>/NODE</span></span>
</dt> <dd>

<span data-ttu-id="17628-211">Computer Namen, durch Kommas getrennt.</span><span class="sxs-lookup"><span data-stu-id="17628-211">Computer names, comma delimited.</span></span> <span data-ttu-id="17628-212">Alle Befehle werden synchron auf allen Computern ausgeführt, die in diesem Wert aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="17628-212">All commands are synchronously executed against all computers listed in this value.</span></span> <span data-ttu-id="17628-213">Dateinamen müssen & vorangestellt sein.</span><span class="sxs-lookup"><span data-stu-id="17628-213">File names must be prefixed with &.</span></span> <span data-ttu-id="17628-214">Computer Namen innerhalb einer Datei müssen durch Kommas getrennt oder in separaten Zeilen enthalten sein.</span><span class="sxs-lookup"><span data-stu-id="17628-214">Computer names within a file must be comma delimited or on separate lines.</span></span>

</dd> <dt>

<span data-ttu-id="17628-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span><span class="sxs-lookup"><span data-stu-id="17628-215"><span id="_IMPLEVEL"></span><span id="_implevel"></span>/IMPLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="17628-216">Identitätswechselebene.</span><span class="sxs-lookup"><span data-stu-id="17628-216">Impersonation level.</span></span>

<span data-ttu-id="17628-217">Beispiel: **/IMPLEVEL: Anonymous**</span><span class="sxs-lookup"><span data-stu-id="17628-217">Example: **/IMPLEVEL:Anonymous**</span></span>

</dd> <dt>

<span data-ttu-id="17628-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span><span class="sxs-lookup"><span data-stu-id="17628-218"><span id="_AUTHLEVEL"></span><span id="_authlevel"></span>/AUTHLEVEL</span></span>
</dt> <dd>

<span data-ttu-id="17628-219">Authentifizierungs Ebene.</span><span class="sxs-lookup"><span data-stu-id="17628-219">Authentication level.</span></span>

<span data-ttu-id="17628-220">Beispiel: **/AUTHLEVEL: Pkt**</span><span class="sxs-lookup"><span data-stu-id="17628-220">Example: **/AUTHLEVEL:Pkt**</span></span>

</dd> <dt>

<span data-ttu-id="17628-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span><span class="sxs-lookup"><span data-stu-id="17628-221"><span id="_LOCALE"></span><span id="_locale"></span>/LOCALE</span></span>
</dt> <dd>

<span data-ttu-id="17628-222">Konfigurations.</span><span class="sxs-lookup"><span data-stu-id="17628-222">Locale.</span></span>

<span data-ttu-id="17628-223">Beispiel: **/locale: ms \_ 411**</span><span class="sxs-lookup"><span data-stu-id="17628-223">Example: **/LOCALE:MS\_411**</span></span>

</dd> <dt>

<span data-ttu-id="17628-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span><span class="sxs-lookup"><span data-stu-id="17628-224"><span id="_PRIVILEGES"></span><span id="_privileges"></span>/PRIVILEGES</span></span>
</dt> <dd>

<span data-ttu-id="17628-225">Aktivieren oder deaktivieren Sie alle Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="17628-225">Enable or disable all privileges.</span></span>

<span data-ttu-id="17628-226">Beispiel: **/privileges: enable** oder **/privileges: deaktivieren**</span><span class="sxs-lookup"><span data-stu-id="17628-226">Example: **/PRIVILEGES:ENABLE** or **/PRIVILEGES:DISABLE**</span></span>

</dd> <dt>

<span data-ttu-id="17628-227"><span id="_TRACE"></span><span id="_trace"></span>/Trace</span><span class="sxs-lookup"><span data-stu-id="17628-227"><span id="_TRACE"></span><span id="_trace"></span>/TRACE</span></span>
</dt> <dd>

<span data-ttu-id="17628-228">Zeigt den Erfolg oder Misserfolg aller Funktionen an, die zum Ausführen von WMIC-Befehlen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17628-228">Display the success or failure of all functions used to execute WMIC commands.</span></span>

<span data-ttu-id="17628-229">Beispiel: **/Trace: on** oder **/Trace: Off**</span><span class="sxs-lookup"><span data-stu-id="17628-229">Example: **/TRACE:ON** or **/TRACE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="17628-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span><span class="sxs-lookup"><span data-stu-id="17628-230"><span id="_RECORD"></span><span id="_record"></span>/RECORD</span></span>
</dt> <dd>

<span data-ttu-id="17628-231">Zeichnet die gesamte Ausgabe in eine XML-Datei auf.</span><span class="sxs-lookup"><span data-stu-id="17628-231">Records all output to an XML file.</span></span> <span data-ttu-id="17628-232">Die Ausgabe wird auch an der Eingabeaufforderung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="17628-232">Output is also displayed at the command prompt.</span></span>

<span data-ttu-id="17628-233">Beispiel: **/Record:** _MyOutput.xml_</span><span class="sxs-lookup"><span data-stu-id="17628-233">Example: **/RECORD:**_MyOutput.xml_</span></span>

</dd> <dt>

<span data-ttu-id="17628-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span><span class="sxs-lookup"><span data-stu-id="17628-234"><span id="_INTERACTIVE"></span><span id="_interactive"></span>/INTERACTIVE</span></span>
</dt> <dd>

<span data-ttu-id="17628-235">In der Regel werden Lösch Befehle bestätigt.</span><span class="sxs-lookup"><span data-stu-id="17628-235">Typically, delete commands are confirmed.</span></span>

<span data-ttu-id="17628-236">Beispiel: **/Interactive: on** oder **/Interactive: Off**</span><span class="sxs-lookup"><span data-stu-id="17628-236">Example: **/INTERACTIVE:ON** or **/INTERACTIVE:OFF**</span></span>

</dd> <dt>

<span data-ttu-id="17628-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FailFast **on** \|  \| *timeoutinmilliseconds*</span><span class="sxs-lookup"><span data-stu-id="17628-237"><span id="_FAILFAST_on_off_TimeoutInMilliseconds"></span><span id="_failfast_on_off_timeoutinmilliseconds"></span><span id="_FAILFAST_ON_OFF_TIMEOUTINMILLISECONDS"></span>/FAILFAST **on**\|**off**\|*TimeoutInMilliseconds*</span></span>
</dt> <dd>

<span data-ttu-id="17628-238">Wenn auf den/Node-Computern ein Ping-Befehl gesendet wird, bevor WMIC-Befehle an Sie gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="17628-238">If ON the /NODE computers are pinged before sending WMIC commands to them.</span></span> <span data-ttu-id="17628-239">Wenn ein Computer nicht antwortet, werden die WMIC-Befehle nicht an ihn gesendet.</span><span class="sxs-lookup"><span data-stu-id="17628-239">If a computer does not respond the WMIC commands are not sent to it.</span></span>

<span data-ttu-id="17628-240">Beispiel: "/FailFast: on" oder "/FailFast: Off"</span><span class="sxs-lookup"><span data-stu-id="17628-240">Example: "/FAILFAST:ON" or "/FAILFAST:OFF"</span></span>

<span data-ttu-id="17628-241">**WMIC-/FailFast: 1000**</span><span class="sxs-lookup"><span data-stu-id="17628-241">**WMIC /FAILFAST:1000**</span></span>

</dd> <dt>

<span data-ttu-id="17628-242"><span id="_USER"></span><span id="_user"></span>/User</span><span class="sxs-lookup"><span data-stu-id="17628-242"><span id="_USER"></span><span id="_user"></span>/USER</span></span>
</dt> <dd>

<span data-ttu-id="17628-243">Benutzername, der von WMIC beim Zugriff auf die in den Aliasen angegebenen/Node-Computer oder-Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17628-243">User name used by WMIC when accessing the /NODE computers or computers specified in the aliases.</span></span> <span data-ttu-id="17628-244">Sie werden aufgefordert, das Kennwort einzugeben.</span><span class="sxs-lookup"><span data-stu-id="17628-244">You are prompted for the password.</span></span> <span data-ttu-id="17628-245">Ein Benutzername darf nicht mit dem lokalen Computer verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="17628-245">A user name cannot be used with the local computer.</span></span>

<span data-ttu-id="17628-246">Beispiel: **/User:**_jsmith_</span><span class="sxs-lookup"><span data-stu-id="17628-246">Example: **/USER:**_JSMITH_</span></span>

</dd> <dt>

<span data-ttu-id="17628-247"><span id="_PASSWORD"></span><span id="_password"></span>/Password</span><span class="sxs-lookup"><span data-stu-id="17628-247"><span id="_PASSWORD"></span><span id="_password"></span>/PASSWORD</span></span>
</dt> <dd>

<span data-ttu-id="17628-248">Kennwort, das von WMIC beim Zugriff auf/Node-Computer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="17628-248">Password used by WMIC when accessing the /NODE computers.</span></span> <span data-ttu-id="17628-249">Das Kennwort ist in der Befehlszeile sichtbar.</span><span class="sxs-lookup"><span data-stu-id="17628-249">The password is visible at the command line.</span></span>

<span data-ttu-id="17628-250">Beispiel: **/Password:**_Password_</span><span class="sxs-lookup"><span data-stu-id="17628-250">Example: **/PASSWORD:**_password_</span></span>

</dd> <dt>

<span data-ttu-id="17628-251"><span id="_OUTPUT"></span><span id="_output"></span>/Output</span><span class="sxs-lookup"><span data-stu-id="17628-251"><span id="_OUTPUT"></span><span id="_output"></span>/OUTPUT</span></span>
</dt> <dd>

<span data-ttu-id="17628-252">Gibt einen Modus für alle Ausgabe Umleitungen an.</span><span class="sxs-lookup"><span data-stu-id="17628-252">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="17628-253">Die Ausgabe wird nicht in der Befehlszeile angezeigt, und das Ziel wird vor Beginn der Ausgabe gelöscht.</span><span class="sxs-lookup"><span data-stu-id="17628-253">Output does not appear at the command line and the destination is cleared before output begins.</span></span> <span data-ttu-id="17628-254">Gültige Werte sind stdout, Zwischenablage oder ein Dateiname.</span><span class="sxs-lookup"><span data-stu-id="17628-254">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="17628-255">Beispiel: **/Output: Zwischenablage**</span><span class="sxs-lookup"><span data-stu-id="17628-255">Example: **/OUTPUT:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="17628-256"><span id="_APPEND"></span><span id="_append"></span>/Append</span><span class="sxs-lookup"><span data-stu-id="17628-256"><span id="_APPEND"></span><span id="_append"></span>/APPEND</span></span>
</dt> <dd>

<span data-ttu-id="17628-257">Gibt einen Modus für alle Ausgabe Umleitungen an.</span><span class="sxs-lookup"><span data-stu-id="17628-257">Specifies a mode for all output redirection.</span></span> <span data-ttu-id="17628-258">Die Ausgabe wird nicht in der Befehlszeile angezeigt, und das Ziel wird vor Beginn der Ausgabe nicht gelöscht, und die Ausgabe wird an das Ende des aktuellen Inhalts des Ziels angehängt.</span><span class="sxs-lookup"><span data-stu-id="17628-258">Output does not appear at the command line and the destination is not cleared before output begins and output is appended to the end of the current contents of the destination.</span></span> <span data-ttu-id="17628-259">Gültige Werte sind stdout, Zwischenablage oder ein Dateiname.</span><span class="sxs-lookup"><span data-stu-id="17628-259">Valid values are STDOUT, CLIPBOARD or a file name.</span></span>

<span data-ttu-id="17628-260">Beispiel: **/Append: Zwischenablage**</span><span class="sxs-lookup"><span data-stu-id="17628-260">Example: **/APPEND:CLIPBOARD**</span></span>

</dd> <dt>

<span data-ttu-id="17628-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span><span class="sxs-lookup"><span data-stu-id="17628-261"><span id="_AGGREGATE"></span><span id="_aggregate"></span>/AGGREGATE</span></span>
</dt> <dd>

<span data-ttu-id="17628-262">Wird mit dem Schalter **List** und **Get/every** verwendet.</span><span class="sxs-lookup"><span data-stu-id="17628-262">Used with the **LIST** and **GET /EVERY** switch.</span></span> <span data-ttu-id="17628-263">Wenn Aggregate auf ON fest steht, werden die Ergebnisse in List und Get angezeigt, wenn für alle Computer in der/Node entweder geantwortet oder ein Timeout aufgetreten ist. Wenn Aggregate auf OFF eingestellt ist, werden die Ergebnisse in List und Get angezeigt, sobald Sie empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="17628-263">If AGGREGATE is ON, LIST and GET display their results when all computers in the /NODE have either responded or timed out. If AGGREGATE is OFF, LIST and GET display their results as soon as they are received.</span></span>

<span data-ttu-id="17628-264">Beispiel: **/Aggregate: Off** oder **/Aggregate: on**</span><span class="sxs-lookup"><span data-stu-id="17628-264">Example: **/AGGREGATE:OFF** or **/AGGREGATE:ON**</span></span>

</dd> </dl>

## <a name="commands"></a><span data-ttu-id="17628-265">Befehle</span><span class="sxs-lookup"><span data-stu-id="17628-265">Commands</span></span>

<span data-ttu-id="17628-266">Die folgenden WMIC-Befehle sind jederzeit verfügbar.</span><span class="sxs-lookup"><span data-stu-id="17628-266">The following WMIC commands are available at all times.</span></span> <span data-ttu-id="17628-267">Weitere Informationen finden Sie unter [WMIC-Befehle](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="17628-267">For more information, see [WMIC Commands](/previous-versions/windows/it-pro/windows-server-2003/cc779647(v=ws.10)).</span></span>

<dl> <dt>

<span data-ttu-id="17628-268"><span id="CLASS"></span><span id="class"></span>Klassi</span><span class="sxs-lookup"><span data-stu-id="17628-268"><span id="CLASS"></span><span id="class"></span>CLASS</span></span>
</dt> <dd>

<span data-ttu-id="17628-269">Escapezeichen aus dem Standardalias Modus von WMIC, um direkt auf Klassen im WMI-Schema zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="17628-269">Escape from the default alias mode of WMIC to access classes in the WMI schema directly.</span></span> <span data-ttu-id="17628-270">Weitere Informationen zu verfügbaren WMI-Klassen finden Sie unter [WMI-Klassen](wmi-classes.md).</span><span class="sxs-lookup"><span data-stu-id="17628-270">For more information on available WMI classes, see [WMI Classes](wmi-classes.md).</span></span>

<span data-ttu-id="17628-271">Beispiel: **WMIC/Output: c: \\ClassOutput.htm Klasse Win32 \_ Sound Device**</span><span class="sxs-lookup"><span data-stu-id="17628-271">Example: **WMIC /OUTPUT:c:\\ClassOutput.htm CLASS Win32\_SoundDevice**</span></span>

</dd> <dt>

<span data-ttu-id="17628-272"><span id="PATH"></span><span id="path"></span>ADS</span><span class="sxs-lookup"><span data-stu-id="17628-272"><span id="PATH"></span><span id="path"></span>PATH</span></span>
</dt> <dd>

<span data-ttu-id="17628-273">Escapezeichen aus dem Standardalias Modus von WMIC, um direkt auf Instanzen im WMI-Schema zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="17628-273">Escape from the default alias mode of WMIC to access instances in the WMI schema directly.</span></span>

<span data-ttu-id="17628-274">Beispiel: **WMIC/Output: c: \\PathOutput.txt Pfad Win32 \_ Sound Device Get/Value**</span><span class="sxs-lookup"><span data-stu-id="17628-274">Example: **WMIC /OUTPUT:c:\\PathOutput.txt PATH Win32\_SoundDevice GET /VALUE**</span></span>

</dd> <dt>

<span data-ttu-id="17628-275"><span id="CONTEXT"></span><span id="context"></span>Kontext</span><span class="sxs-lookup"><span data-stu-id="17628-275"><span id="CONTEXT"></span><span id="context"></span>CONTEXT</span></span>
</dt> <dd>

<span data-ttu-id="17628-276">Zeigt die aktuellen Werte aller globalen Switches an.</span><span class="sxs-lookup"><span data-stu-id="17628-276">Display the current values of all global switches.</span></span>

<span data-ttu-id="17628-277">Beispiel: **WMIC-Kontext**</span><span class="sxs-lookup"><span data-stu-id="17628-277">Example: **WMIC CONTEXT**</span></span>

</dd> <dt>

<span data-ttu-id="17628-278"><span id="QUIT"></span><span id="quit"></span>Beendeten</span><span class="sxs-lookup"><span data-stu-id="17628-278"><span id="QUIT"></span><span id="quit"></span>QUIT</span></span>
</dt> <dd>

<span data-ttu-id="17628-279">Beenden Sie den WMIC-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="17628-279">Exit from WMIC.</span></span>

<span data-ttu-id="17628-280">Beispiel: **WMIC Quit**</span><span class="sxs-lookup"><span data-stu-id="17628-280">Example: **WMIC QUIT**</span></span>

</dd> <dt>

<span data-ttu-id="17628-281"><span id="EXIT"></span><span id="exit"></span>Abstiegs</span><span class="sxs-lookup"><span data-stu-id="17628-281"><span id="EXIT"></span><span id="exit"></span>EXIT</span></span>
</dt> <dd>

<span data-ttu-id="17628-282">Beenden Sie den WMIC-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="17628-282">Exit from WMIC.</span></span>

<span data-ttu-id="17628-283">Beispiel: **WMIC Exit**</span><span class="sxs-lookup"><span data-stu-id="17628-283">Example: **WMIC EXIT**</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="17628-284">Beispiele</span><span class="sxs-lookup"><span data-stu-id="17628-284">Examples</span></span>

<span data-ttu-id="17628-285">Das [Skript zum Festlegen von IP/Subnetz/Gateway/DNS mithilfe von WMIC](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) Sample in der TechNet Gallery beschreibt, wie IP-, Subnetz-, Gateway-und DNS-Einstellungen geändert und aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="17628-285">The [Script for setting IP/Subnet/Gateway/DNS using wmic](https://Gallery.TechNet.Microsoft.Com/Batch-per-settare-487c1b3f) sample on TechNet Gallery describes how to modify and update IP, Subnet, Gateway, and DNS settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="17628-286">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="17628-286">Requirements</span></span>



| <span data-ttu-id="17628-287">Anforderung</span><span class="sxs-lookup"><span data-stu-id="17628-287">Requirement</span></span> | <span data-ttu-id="17628-288">Wert</span><span class="sxs-lookup"><span data-stu-id="17628-288">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="17628-289">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="17628-289">Minimum supported client</span></span><br/> | <span data-ttu-id="17628-290">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="17628-290">Windows Vista</span></span><br/>       |
| <span data-ttu-id="17628-291">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="17628-291">Minimum supported server</span></span><br/> | <span data-ttu-id="17628-292">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="17628-292">Windows Server 2008</span></span><br/> |



 

