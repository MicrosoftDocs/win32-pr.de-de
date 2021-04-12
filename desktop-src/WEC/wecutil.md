---
title: Wecutil.exe
description: Wecutil.exe ist ein Windows-Ereignis Sammler-Hilfsprogramm, mit dem Administratoren Abonnements für Ereignisse erstellen und verwalten können, die von Remote Ereignis Quellen weitergeleitet werden, die das WS-Management-Protokoll unterstützen.
ms.assetid: 93ce25df-f829-43b9-96f2-7f2f291d100e
ms.tgt_platform: multiple
keywords:
- Wecutil.exe
topic_type:
- apiref
api_name:
- Wecutil.exe
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aaf6f74007b56cff85c28c4106fd4345c5627d4e
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/10/2021
ms.locfileid: "104353979"
---
# <a name="wecutilexe"></a><span data-ttu-id="0073a-104">Wecutil.exe</span><span class="sxs-lookup"><span data-stu-id="0073a-104">Wecutil.exe</span></span>

<span data-ttu-id="0073a-105">Wecutil.exe ist ein Windows-Ereignis Sammler-Hilfsprogramm, mit dem Administratoren Abonnements für Ereignisse erstellen und verwalten können, die von Remote Ereignis Quellen weitergeleitet werden, die das WS-Management-Protokoll unterstützen.</span><span class="sxs-lookup"><span data-stu-id="0073a-105">Wecutil.exe is a Windows Event Collector utility that enables an administrator to create and manage subscriptions to events forwarded from remote event sources that support the WS-Management protocol.</span></span> <span data-ttu-id="0073a-106">Bei Befehlen, Optionen und Options Werten wird die Groß-/Kleinschreibung für dieses Hilfsprogramm nicht beachtet.</span><span class="sxs-lookup"><span data-stu-id="0073a-106">Commands, options, and option values are case-insensitive for this utility.</span></span>

<span data-ttu-id="0073a-107">Wenn Sie eine Meldung erhalten, die besagt, dass der RPC-Server nicht verfügbar ist oder die Schnittstelle unbekannt ist, müssen Sie den Windows-Ereignis Sammlungs Dienst (Wecsvc) starten, wenn Sie versuchen, wecutil auszuführen.</span><span class="sxs-lookup"><span data-stu-id="0073a-107">If you receive a message that says "The RPC server is unavailable" or "The interface is unknown" when you try to run wecutil, then you need to start the Windows Event Collector service (wecsvc).</span></span> <span data-ttu-id="0073a-108">Um Wecsvc zu starten, geben Sie an einer Eingabeaufforderung mit erhöhten Rechten **net Start Wecsvc** ein.</span><span class="sxs-lookup"><span data-stu-id="0073a-108">To start wecsvc, at an elevated command prompt type **net start wecsvc**.</span></span>

## <a name="list-existing-subscriptions"></a><span data-ttu-id="0073a-109">Auflisten vorhandener Abonnements</span><span class="sxs-lookup"><span data-stu-id="0073a-109">List existing subscriptions</span></span>

<span data-ttu-id="0073a-110">Die folgende Syntax wird verwendet, um vorhandene Remote Ereignis Abonnements aufzulisten.</span><span class="sxs-lookup"><span data-stu-id="0073a-110">The following syntax is used to list existing remote event subscriptions.</span></span>

``` syntax
wecutil { es | enum-subscription }
```

<span data-ttu-id="0073a-111">Wenn Sie ein Skript verwenden, um die Namen der Abonnements aus der Ausgabe zu erhalten, müssen Sie die UTF-8-BOM-Zeichen in der ersten Zeile der Ausgabe umgehen.</span><span class="sxs-lookup"><span data-stu-id="0073a-111">If you use a script to get the names of the subscriptions from the output, you will need to bypass the UTF-8 BOM characters in the first line of the output.</span></span> <span data-ttu-id="0073a-112">Das folgende Skript zeigt ein Beispiel dafür, wie Sie die BOM-Zeichen überspringen können.</span><span class="sxs-lookup"><span data-stu-id="0073a-112">The following script shows an example of how you might skip the BOM characters.</span></span>

``` syntax
setlocal enabledelayedexpansion

set bomskipped=
for /f %%i in ('wecutil es') do (
    set sub=%%i
    if not defined bomskipped (
        set sub=!sub:~3!
        set bomskipped=yes
    )
    echo !sub!
)
goto :eof

endlocal
```

## <a name="get-subscription-configuration"></a><span data-ttu-id="0073a-113">Abonnement Konfiguration erhalten</span><span class="sxs-lookup"><span data-stu-id="0073a-113">Get subscription configuration</span></span>

<span data-ttu-id="0073a-114">Die folgende Syntax wird verwendet, um Konfigurationsdaten für Remote Ereignis Abonnements anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0073a-114">The following syntax is used to display remote event subscription configuration data.</span></span>

``` syntax
wecutil { gs | get-subscription } SUBSCRIPTION_ID [/f:VALUE 
[/u:VALUE] ...]
```

## <a name="get-configuration-parameters"></a><span data-ttu-id="0073a-115">Konfigurationsparameter erhalten</span><span class="sxs-lookup"><span data-stu-id="0073a-115">Get Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0073a-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**Abonnement- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="0073a-116"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="0073a-117">Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0073a-117">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="0073a-118">Dieser Bezeichner wird in der XML-Konfigurationsdatei, die zum Erstellen des Abonnements verwendet wird, im **Abonnement-ID** -Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="0073a-118">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f: \* Wert**\*</span><span class="sxs-lookup"><span data-stu-id="0073a-119"><span id="_f_VALUE"></span><span id="_f_value"></span><span id="_F_VALUE"></span>**/f:\*VALUE**\*</span></span>
</dt> <dd>

<span data-ttu-id="0073a-120">Ein-Wert, der die Ausgabe der Abonnement Konfigurationsdaten angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-120">A value that specifies the output of the subscription configuration data.</span></span> <span data-ttu-id="0073a-121">Der Wert kann "XML" oder "Terse" lauten, der Standard *Wert* ist "Terse".</span><span class="sxs-lookup"><span data-stu-id="0073a-121">*VALUE* can be "XML" or "Terse", and the default is "Terse".</span></span> <span data-ttu-id="0073a-122">Wenn *value* "XML" ist, wird die Ausgabe im XML-Format gedruckt.</span><span class="sxs-lookup"><span data-stu-id="0073a-122">If *VALUE* is "XML", then the output is printed in "XML" format.</span></span> <span data-ttu-id="0073a-123">Wenn *value* "Terse" ist, wird die Ausgabe in Name-Wert-Paaren ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="0073a-123">If *VALUE* is "Terse", then the output is printed in name-value pairs.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *Wert***</span><span class="sxs-lookup"><span data-stu-id="0073a-124"><span id="_u_VALUE"></span><span id="_u_value"></span><span id="_U_VALUE"></span>**/u: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-125">Ein-Wert, der angibt, ob die Ausgabe im Unicode-Format vorliegt.</span><span class="sxs-lookup"><span data-stu-id="0073a-125">A value that specifies whether the output is in Unicode format.</span></span> <span data-ttu-id="0073a-126">Der *Wert* kann "true" oder "false" lauten.</span><span class="sxs-lookup"><span data-stu-id="0073a-126">*VALUE* can be "true" or "false".</span></span> <span data-ttu-id="0073a-127">Wenn *value den Wert* "true" hat, erfolgt die Ausgabe im Unicode-Format, und wenn *value den Wert* "false" hat, erfolgt die Ausgabe nicht im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="0073a-127">If *VALUE* is "true", then the output is in Unicode format, and if *VALUE* is "false", then the output is not in Unicode format.</span></span>

</dd> </dl>

## <a name="get-subscription-runtime-status"></a><span data-ttu-id="0073a-128">Abonnement Lauf Zeit Status erhalten</span><span class="sxs-lookup"><span data-stu-id="0073a-128">Get subscription runtime status</span></span>

<span data-ttu-id="0073a-129">Die folgende Syntax wird verwendet, um den Abonnement Lauf Zeit Status anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="0073a-129">The following syntax is used to display the subscription runtime status.</span></span>

``` syntax
wecutil { gr | get-subscriptionruntimestatus } SUBSCRIPTION_ID
 [EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="get-status-parameters"></a><span data-ttu-id="0073a-130">Status Parameter erhalten</span><span class="sxs-lookup"><span data-stu-id="0073a-130">Get Status Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0073a-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**Abonnement- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="0073a-131"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="0073a-132">Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0073a-132">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="0073a-133">Dieser Bezeichner wird in der XML-Konfigurationsdatei, die zum Erstellen des Abonnements verwendet wird, im **Abonnement-ID** -Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="0073a-133">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**Ereignis \_ Quelle**</span><span class="sxs-lookup"><span data-stu-id="0073a-134"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="0073a-135">Ein-Wert, der einen Computer identifiziert, bei dem es sich um eine Ereignis Quelle für ein Ereignis Abonnement handelt.</span><span class="sxs-lookup"><span data-stu-id="0073a-135">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="0073a-136">Bei diesem Wert kann es sich um den voll qualifizierten Domänen Namen für den Computer, den NetBIOS-Namen oder die IP-Adresse handeln.</span><span class="sxs-lookup"><span data-stu-id="0073a-136">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="set-subscription-configuration-information"></a><span data-ttu-id="0073a-137">Festlegen von Informationen zur Abonnement Konfiguration</span><span class="sxs-lookup"><span data-stu-id="0073a-137">Set Subscription Configuration Information</span></span>

<span data-ttu-id="0073a-138">Die folgende Syntax wird verwendet, um die Abonnement Konfigurationsdaten festzulegen, indem Sie die Abonnement Parameter von der Befehlszeile aus ändern oder eine XML-Konfigurationsdatei verwenden.</span><span class="sxs-lookup"><span data-stu-id="0073a-138">The following syntax is used to set subscription configuration data by changing subscription parameters from the command line or using an XML configuration file.</span></span>

``` syntax
wecutil { ss | set_subscription } SUBSCRIPTION_ID [/e:VALUE] 
[/esa:EVENT_SOURCE [/ese:VALUE] [/aes] [/res] [/un:USERNAME] [/up:PASSWORD]] 
[/d:DESCRIPTION] [/uri:URI] [/cm:CONFIGURATION_MODE] [/ex:DATE_TIME] 
[/q:QUERY] [/dia:DIALECT] [/tn:TRANSPORTNAME] [/tp:TRANSPORTPORT] [/dm:MODE] 
[/dmi:NUMBER] [/dmlt:MS] [/hi:MS] [/cf:FORMAT] [/l:LOCALE] [/ree:[VALUE]] 
[/lf:FILENAME] [/pn:PUBLISHER] [/hn:NAME] [/ct:TYPE] 
[/cun:USERNAME] [/cup:PASSWORD] 
[/ica:THUMBPRINTS] [/as:ALLOWED] [/ds:DENIED] [/adc:SDDL]

wecutil {ss | set_subscription } /c:CONGIG_FILE [/cun:USERNAME] 
[/cup:PASSWORD]
```

### <a name="remarks"></a><span data-ttu-id="0073a-139">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0073a-139">Remarks</span></span>

<span data-ttu-id="0073a-140">Wenn im Befehl " **wecutil SS** " ein falscher Benutzername oder ein falscher Kennwort angegeben ist, wird kein Fehler gemeldet, bis Sie den Lauf Zeit Status des Abonnements mit dem Befehl " **wecutil GR** " anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0073a-140">When an incorrect username or password is specified in the **wecutil ss** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="set-configuration-parameters"></a><span data-ttu-id="0073a-141">Festlegen von Konfigurationsparametern</span><span class="sxs-lookup"><span data-stu-id="0073a-141">Set Configuration Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0073a-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**Abonnement- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="0073a-142"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="0073a-143">Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0073a-143">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="0073a-144">Dieser Bezeichner wird in der XML-Konfigurationsdatei, die zum Erstellen des Abonnements verwendet wird, im **Abonnement-ID** -Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="0073a-144">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *Konfigurations \_ Datei***</span><span class="sxs-lookup"><span data-stu-id="0073a-145"><span id="_c_CONGIG_FILE"></span><span id="_c_congig_file"></span><span id="_C_CONGIG_FILE"></span>**/c: *CONGIG\_FILE***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-146">Ein-Wert, der den Pfad zur XML-Datei angibt, die Informationen zur Abonnement Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="0073a-146">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="0073a-147">Der Pfad kann absolut oder relativ zum aktuellen Verzeichnis sein.</span><span class="sxs-lookup"><span data-stu-id="0073a-147">The path can be absolute or relative to the current directory.</span></span> <span data-ttu-id="0073a-148">Dieser Parameter kann nur mit den optionalen Parametern/CUS und/Cup verwendet werden und schließt sich gegenseitig mit allen anderen Parametern aus.</span><span class="sxs-lookup"><span data-stu-id="0073a-148">This parameter can only be used with the optional /cus and /cup parameters, and is mutually exclusive with all the other parameters.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *Wert***</span><span class="sxs-lookup"><span data-stu-id="0073a-149"><span id="_e_VALUE"></span><span id="_e_value"></span><span id="_E_VALUE"></span>**/e: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-150">Ein-Wert, der bestimmt, ob das Abonnement aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0073a-150">A value that determines whether to enable or disable the subscription.</span></span> <span data-ttu-id="0073a-151">Der Wert kann "true" oder "false" sein.</span><span class="sxs-lookup"><span data-stu-id="0073a-151">VALUE can be true or false.</span></span> <span data-ttu-id="0073a-152">Der Standardwert ist "true", wodurch das Abonnement aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-152">The default value is true, which enables the subscription.</span></span>

> [!Note]  
> <span data-ttu-id="0073a-153">Wenn Sie ein vom Collector initiiertes Abonnement deaktivieren, wird die Ereignis Quelle nicht deaktiviert, sondern inaktiv.</span><span class="sxs-lookup"><span data-stu-id="0073a-153">When you disable a collector initiated subscription, the event source becomes inactive instead of disabled.</span></span> <span data-ttu-id="0073a-154">In einem vom Collector initiierten Abonnement können Sie eine Ereignis Quelle deaktivieren, die unabhängig vom Abonnement ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-154">In a collector initiated subscription, you can disable an event source independent of the subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="0073a-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *Beschreibung***</span><span class="sxs-lookup"><span data-stu-id="0073a-155"><span id="_d_DESCRIPTION"></span><span id="_d_description"></span><span id="_D_DESCRIPTION"></span>**/d: *DESCRIPTION***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-156">Ein-Wert, der eine Beschreibung für das Ereignis Abonnement angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-156">A value that specifies a description for the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/Ex: *Datum/ \_ Uhrzeit***</span><span class="sxs-lookup"><span data-stu-id="0073a-157"><span id="_ex_DATE_TIME"></span><span id="_ex_date_time"></span><span id="_EX_DATE_TIME"></span>**/ex: *DATE\_TIME***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-158">Ein-Wert, der die Ablaufzeit des Abonnements angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-158">A value that specifies the subscription expiration time.</span></span> <span data-ttu-id="0073a-159">*Datum \_ Time* ist ein Wert, der in Standard-XML-oder ISO8601-Datums-/Uhrzeitformat angegeben ist: "yyyy-mm-ddThh: mm: SS \[ . sss \] \[ Z \] ", wobei "T" das Zeit Trennzeichen und "Z" die UTC-Zeit angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-159">*DATE\_TIME* is a value specified in standard XML or ISO8601 date-time format: "yyyy-MM-ddThh:mm:ss\[.sss\]\[Z\]" where "T" is the time separator and "Z" indicates UTC time.</span></span> <span data-ttu-id="0073a-160">Wenn z. b. *Datum/ \_ Uhrzeit* "2007-01-12t01:20:00" ist, ist die Ablaufzeit des Abonnements der 12. Januar 2007, 01:20.</span><span class="sxs-lookup"><span data-stu-id="0073a-160">For example, if *DATE\_TIME* is "2007-01-12T01:20:00", then the subscription expiration time is January 12th, 2007, 01:20.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/URI: *URI***</span><span class="sxs-lookup"><span data-stu-id="0073a-161"><span id="_uri_URI"></span><span id="_uri_uri"></span><span id="_URI_URI"></span>**/uri: *URI***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-162">Ein-Wert, der den Typ der Ereignisse angibt, die vom Abonnement genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="0073a-162">A value that specifies the type of events consumed by the subscription.</span></span> <span data-ttu-id="0073a-163">Die Adresse des Ereignis Quell Computers zusammen mit dem URI (Uniform Resource Identifier) identifiziert die Quelle der Ereignisse eindeutig.</span><span class="sxs-lookup"><span data-stu-id="0073a-163">The address of the event source computer along with the uniform resource identifier (URI) uniquely identifies the source of the events.</span></span> <span data-ttu-id="0073a-164">Die URI-Zeichenfolge wird für alle Ereignis Quelladressen im Abonnement verwendet.</span><span class="sxs-lookup"><span data-stu-id="0073a-164">The URI string is used for all event source addresses in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *Konfigurations \_ Modus***</span><span class="sxs-lookup"><span data-stu-id="0073a-165"><span id="_cm_CONFIGURATION_MODE"></span><span id="_cm_configuration_mode"></span><span id="_CM_CONFIGURATION_MODE"></span>**/cm: *CONFIGURATION\_MODE***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-166">Ein-Wert, der den Konfigurations Modus des Ereignis Abonnements angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-166">A value that specifies the configuration mode of the event subscription.</span></span> <span data-ttu-id="0073a-167">*Konfiguration \_ Der Modus* kann eine der folgenden Zeichen folgen sein: "Normal", "Custom", "minlatency" oder "minbandwidth".</span><span class="sxs-lookup"><span data-stu-id="0073a-167">*CONFIGURATION\_MODE* can be one of the following strings: "Normal", "Custom", "MinLatency", or "MinBandwidth".</span></span> <span data-ttu-id="0073a-168">Die [**\_ \_ Konfigurations \_ Modus**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) -Enumeration des EC-Abonnements definiert die Konfigurations Modi.</span><span class="sxs-lookup"><span data-stu-id="0073a-168">The [**EC\_SUBSCRIPTION\_CONFIGURATION\_MODE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_configuration_mode) enumeration defines the configuration modes.</span></span> <span data-ttu-id="0073a-169">Die Parameter/DM,/DMI,/Hi und/dmlt können nur angegeben werden, wenn der Konfigurations Modus auf Custom festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-169">The /dm, /dmi, /hi, and /dmlt parameters can only be specified if the configuration mode is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *Abfrage***</span><span class="sxs-lookup"><span data-stu-id="0073a-170"><span id="_q_QUERY"></span><span id="_q_query"></span><span id="_Q_QUERY"></span>**/q: *QUERY***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-171">Ein-Wert, der die Abfrage Zeichenfolge für das Abonnement angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-171">A value that specifies the query string for the subscription.</span></span> <span data-ttu-id="0073a-172">Das Format dieser Zeichenfolge kann für unterschiedliche URI-Werte unterschiedlich sein und gilt für alle Ereignis Quellen im Abonnement.</span><span class="sxs-lookup"><span data-stu-id="0073a-172">The format of this string can be different for different URI values and applies to all event sources in the subscription.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/Dia: *Dialekt***</span><span class="sxs-lookup"><span data-stu-id="0073a-173"><span id="_dia_DIALECT"></span><span id="_dia_dialect"></span><span id="_DIA_DIALECT"></span>**/dia: *DIALECT***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-174">Ein-Wert, der den von der Abfrage Zeichenfolge verwendeten Dialekt angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-174">A value that specifies the dialect the query string uses.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/CF: *Format***</span><span class="sxs-lookup"><span data-stu-id="0073a-175"><span id="_cf_FORMAT"></span><span id="_cf_format"></span><span id="_CF_FORMAT"></span>**/cf: *FORMAT***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-176">Ein-Wert, der das Format der zurückgegebenen Ereignisse angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-176">A value that specifies the format of the returned events.</span></span> <span data-ttu-id="0073a-177">Das *Format* kann "Events" oder "renderedtext" lauten.</span><span class="sxs-lookup"><span data-stu-id="0073a-177">*FORMAT* can be "Events" or "RenderedText".</span></span> <span data-ttu-id="0073a-178">Wenn der Wert "renderedtext" ist, werden die Ereignisse mit den lokalisierten Zeichen folgen (z. b. Ereignis Beschreibungs Zeichenfolgen) zurückgegeben, die den Ereignissen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="0073a-178">When the value is "RenderedText", the events are returned with the localized strings (such as event description strings) attached to the events.</span></span> <span data-ttu-id="0073a-179">Der Standardwert von *Format* ist "renderedtext".</span><span class="sxs-lookup"><span data-stu-id="0073a-179">The default value of *FORMAT* is "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="0073a-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *Gebiets* Schema**</span><span class="sxs-lookup"><span data-stu-id="0073a-180"><span id="_l_LOCALE"></span><span id="_l_locale"></span><span id="_L_LOCALE"></span>**/l: *LOCALE***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-181">Ein-Wert, der das Gebiets Schema für die Übermittlung der lokalisierten Zeichen folgen im gerenderten Textformat angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-181">A value that specifies the locale for delivery of the localized strings in rendered text format.</span></span> <span data-ttu-id="0073a-182">*Locale* ist ein sprach-/Länder Kultur Bezeichner, z. b. "en-US".</span><span class="sxs-lookup"><span data-stu-id="0073a-182">*LOCALE* is a language/country culture identifier, for example, "EN-us".</span></span> <span data-ttu-id="0073a-183">Dieser Parameter ist nur gültig, wenn der/CF-Parameter auf "renderedtext" festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-183">This parameter is only valid when the /cf parameter is set to "RenderedText".</span></span>

</dd> <dt>

<span data-ttu-id="0073a-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/Ree: \[ *Wert*\]**</span><span class="sxs-lookup"><span data-stu-id="0073a-184"><span id="_ree__VALUE_"></span><span id="_ree__value_"></span><span id="_REE__VALUE_"></span>**/ree:\[*VALUE*\]**</span></span>
</dt> <dd>

<span data-ttu-id="0073a-185">Ein-Wert, der angibt, welche Ereignisse für das Abonnement übermittelt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="0073a-185">A value that specifies which events are to be delivered for the subscription.</span></span> <span data-ttu-id="0073a-186">Der *Wert* kann "true" oder "false" sein.</span><span class="sxs-lookup"><span data-stu-id="0073a-186">*VALUE* can be true or false.</span></span> <span data-ttu-id="0073a-187">Wenn *value den Wert* true hat, werden alle vorhandenen Ereignisse aus den Abonnement Ereignis Quellen gelesen.</span><span class="sxs-lookup"><span data-stu-id="0073a-187">When *VALUE* is true, all existing events are read from the subscription event sources.</span></span> <span data-ttu-id="0073a-188">Wenn der *Wert* false ist, werden nur zukünftige (eingehende) Ereignisse übermittelt.</span><span class="sxs-lookup"><span data-stu-id="0073a-188">When *VALUE* is false, only future (arriving) events are delivered.</span></span> <span data-ttu-id="0073a-189">Der Standardwert ist true, wenn/Ree ohne einen-Wert angegeben wird, und der Standardwert ist false, wenn/Ree nicht angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-189">The default is true when /ree is specified without a value, and the default is false if /ree is not specified.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/LF: *Dateiname***</span><span class="sxs-lookup"><span data-stu-id="0073a-190"><span id="_lf_FILENAME"></span><span id="_lf_filename"></span><span id="_LF_FILENAME"></span>**/lf: *FILENAME***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-191">Ein-Wert, der das lokale Ereignisprotokoll angibt, das zum Speichern der vom Ereignis Abonnement empfangenen Ereignisse verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-191">A value that specifies the local event log that is used to store events received from the event subscription.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/PN: *Publisher***</span><span class="sxs-lookup"><span data-stu-id="0073a-192"><span id="_pn_PUBLISHER"></span><span id="_pn_publisher"></span><span id="_PN_PUBLISHER"></span>**/pn: *PUBLISHER***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-193">Ein-Wert, der den Namen des Ereignis Verlegers (Anbieter) angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-193">A value that specifies the event publisher (provider) name.</span></span> <span data-ttu-id="0073a-194">Dabei muss es sich um einen Verleger handeln, der das durch den/LF-Parameter angegebene Protokoll besitzt oder importiert.</span><span class="sxs-lookup"><span data-stu-id="0073a-194">It must be a publisher which owns or imports the log specified by the /lf parameter.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/DM: *Modus***</span><span class="sxs-lookup"><span data-stu-id="0073a-195"><span id="_dm_MODE"></span><span id="_dm_mode"></span><span id="_DM_MODE"></span>**/dm: *MODE***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-196">Ein-Wert, der den abonnementzustellungs Modus angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-196">A value that specifies the subscription delivery mode.</span></span> <span data-ttu-id="0073a-197">Der *Modus* kann Push oder Pull lauten.</span><span class="sxs-lookup"><span data-stu-id="0073a-197">*MODE* can be either push or pull.</span></span> <span data-ttu-id="0073a-198">Diese Option ist nur gültig, wenn der/cm-Parameter auf Custom festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-198">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/DMI: *Zahl***</span><span class="sxs-lookup"><span data-stu-id="0073a-199"><span id="_dmi_NUMBER"></span><span id="_dmi_number"></span><span id="_DMI_NUMBER"></span>**/dmi: *NUMBER***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-200">Ein-Wert, der die maximale Anzahl von Elementen für die Batch Übermittlung im Ereignis Abonnement angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-200">A value that specifies the maximum number of items for batched delivery in the event subscription.</span></span> <span data-ttu-id="0073a-201">Diese Option ist nur gültig, wenn der/cm-Parameter auf Custom festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-201">This option is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***</span><span class="sxs-lookup"><span data-stu-id="0073a-202"><span id="_dmlt_MS"></span><span id="_dmlt_ms"></span><span id="_DMLT_MS"></span>**/dmlt: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-203">Ein-Wert, der die maximale Latenz angibt, die für die Bereitstellung eines Batch von Ereignissen zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-203">A value that specifies the maximum latency allowed in delivering a batch of events.</span></span> <span data-ttu-id="0073a-204">MS ist die zulässige Anzahl von Millisekunden.</span><span class="sxs-lookup"><span data-stu-id="0073a-204">MS is the number of milliseconds allowed.</span></span> <span data-ttu-id="0073a-205">Dieser Parameter ist nur gültig, wenn der/cm-Parameter auf Custom festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-205">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/Hi: *MS***</span><span class="sxs-lookup"><span data-stu-id="0073a-206"><span id="_hi_MS"></span><span id="_hi_ms"></span><span id="_HI_MS"></span>**/hi: *MS***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-207">Ein-Wert, der das Takt Intervall für das Abonnement angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-207">A value that specifies the heartbeat interval for the subscription.</span></span> <span data-ttu-id="0073a-208">*MS* ist die Anzahl der Millisekunden, die im Intervall verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0073a-208">*MS* is the number of milliseconds used in the interval.</span></span> <span data-ttu-id="0073a-209">Dieser Parameter ist nur gültig, wenn der/cm-Parameter auf Custom festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-209">This parameter is only valid if the /cm parameter is set to Custom.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/TN: *TransportName***</span><span class="sxs-lookup"><span data-stu-id="0073a-210"><span id="_tn_TRANSPORTNAME"></span><span id="_tn_transportname"></span><span id="_TN_TRANSPORTNAME"></span>**/tn: *TRANSPORTNAME***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-211">Ein-Wert, der den Namen des Transports angibt, der zum Herstellen der Verbindung mit dem Remote-Ereignis Quellcomputer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-211">A value that specifies the name of the transport used to connect to the remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/ESA: *Ereignis \_ Quelle***</span><span class="sxs-lookup"><span data-stu-id="0073a-212"><span id="_esa_EVENT_SOURCE"></span><span id="_esa_event_source"></span><span id="_ESA_EVENT_SOURCE"></span>**/esa: *EVENT\_SOURCE***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-213">Ein-Wert, der die Adresse eines Ereignis Quell Computers angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-213">A value that specifies the address of an event source computer.</span></span> <span data-ttu-id="0073a-214">*Ereignis \_ Quelle* ist eine Zeichenfolge, die einen Ereignis Quellcomputer mit dem voll qualifizierten Domänen Namen für den Computer, den NetBIOS-Namen oder die IP-Adresse identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0073a-214">*EVENT\_SOURCE* is a string that identifies an event source computer using the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span> <span data-ttu-id="0073a-215">Dieser Parameter kann mit den Parametern/ESE,/AES,/res oder/UN und/up verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0073a-215">This parameter can be used with the /ese, /aes, /res, or /un and /up parameters.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ESE: *Wert***</span><span class="sxs-lookup"><span data-stu-id="0073a-216"><span id="_ese_VALUE"></span><span id="_ese_value"></span><span id="_ESE_VALUE"></span>**/ese: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-217">Ein Wert, der bestimmt, ob eine Ereignis Quelle aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0073a-217">A value that determines whether to enable or disable an event source.</span></span> <span data-ttu-id="0073a-218">Der *Wert* kann "true" oder "false" sein.</span><span class="sxs-lookup"><span data-stu-id="0073a-218">*VALUE* can be true or false.</span></span> <span data-ttu-id="0073a-219">Der Standardwert ist "true", wodurch die Ereignis Quelle aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-219">The default value is true, which enables the event source.</span></span> <span data-ttu-id="0073a-220">Dieser Parameter wird nur verwendet, wenn der/ESA-Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-220">This parameter is only used if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span><span class="sxs-lookup"><span data-stu-id="0073a-221"><span id="_aes"></span><span id="_AES"></span>**/aes**</span></span>
</dt> <dd>

<span data-ttu-id="0073a-222">Ein-Wert, der die vom/ESA-Parameter angegebene Ereignis Quelle hinzufügt, wenn die Ereignis Quelle nicht bereits Teil des Ereignis Abonnements ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-222">A value that adds the event source specified by the /esa parameter if the event source is not already part of the event subscription.</span></span> <span data-ttu-id="0073a-223">Wenn der durch den/ESA-Parameter angegebene Computer bereits Teil des Abonnements ist, wird ein Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0073a-223">If the computer specified by the /esa parameter is already a part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="0073a-224">Dieser Parameter ist nur zulässig, wenn der/ESA-Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-224">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-225"><span id="_res"></span><span id="_RES"></span>**/res**</span><span class="sxs-lookup"><span data-stu-id="0073a-225"><span id="_res"></span><span id="_RES"></span>**/res**</span></span>
</dt> <dd>

<span data-ttu-id="0073a-226">Ein-Wert, der die vom/ESA-Parameter angegebene Ereignis Quelle entfernt, wenn die Ereignis Quelle bereits Teil des Ereignis Abonnements ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-226">A value that removes the event source specified by the /esa parameter if the event source is already part of the event subscription.</span></span> <span data-ttu-id="0073a-227">Wenn der durch den/ESA-Parameter angegebene Computer nicht Teil des Abonnements ist, wird ein Fehler angezeigt.</span><span class="sxs-lookup"><span data-stu-id="0073a-227">If the computer specified by the /esa parameter is not part of the subscription, then an error is displayed.</span></span> <span data-ttu-id="0073a-228">Dieser Parameter ist nur zulässig, wenn der/ESA-Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-228">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/UN: *Benutzername***</span><span class="sxs-lookup"><span data-stu-id="0073a-229"><span id="_un_USERNAME"></span><span id="_un_username"></span><span id="_UN_USERNAME"></span>**/un: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-230">Ein-Wert, der den Benutzernamen angibt, der in den Anmelde Informationen zum Herstellen einer Verbindung mit der im/ESA-Parameter angegebenen Ereignis Quelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-230">A value that specifies the user name used in the credentials to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="0073a-231">Dieser Parameter ist nur zulässig, wenn der/ESA-Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-231">This parameter is allowed only if the /esa parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *Kennwort***</span><span class="sxs-lookup"><span data-stu-id="0073a-232"><span id="_up_PASSWORD"></span><span id="_up_password"></span><span id="_UP_PASSWORD"></span>**/up: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-233">Ein-Wert, der das Kennwort für den Benutzernamen angibt, der im/UN-Parameter angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-233">A value that specifies the password for the user name specified in the /un parameter.</span></span> <span data-ttu-id="0073a-234">Die Anmelde Informationen für Benutzername und Kennwort werden verwendet, um eine Verbindung mit der im/ESA-Parameter angegebenen Ereignis Quelle herzustellen.</span><span class="sxs-lookup"><span data-stu-id="0073a-234">The user name and password credentials are used to connect to the event source specified in the /esa parameter.</span></span> <span data-ttu-id="0073a-235">Dieser Parameter ist nur zulässig, wenn der/UN-Parameter verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-235">This parameter is allowed only if the /un parameter is used.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/TP: *transportport***</span><span class="sxs-lookup"><span data-stu-id="0073a-236"><span id="_tp_TRANSPORTPORT"></span><span id="_tp_transportport"></span><span id="_TP_TRANSPORTPORT"></span>**/tp: *TRANSPORTPORT***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-237">Ein-Wert, der die Portnummer angibt, die vom Transport beim Herstellen einer Verbindung mit einem Remote-Ereignis Quellcomputer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-237">A value that specifies the port number used by the transport when connecting to a remote event source computer.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/HN: *Name***</span><span class="sxs-lookup"><span data-stu-id="0073a-238"><span id="_hn_NAME"></span><span id="_hn_name"></span><span id="_HN_NAME"></span>**/hn: *NAME***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-239">Ein-Wert, der den DNS-Namen des lokalen Computers angibt.</span><span class="sxs-lookup"><span data-stu-id="0073a-239">A value that specifies the DNS name of the local computer.</span></span> <span data-ttu-id="0073a-240">Dieser Name wird von Remote Ereignis Quellen verwendet, um Ereignisse per Push zurückzusetzen, und er muss nur für Pushabonnements verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0073a-240">This name is used by remote event sources to push back events and must be used for push subscriptions only.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/CT: *Typ***</span><span class="sxs-lookup"><span data-stu-id="0073a-241"><span id="_ct_TYPE"></span><span id="_ct_type"></span><span id="_CT_TYPE"></span>**/ct: *TYPE***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-242">Ein-Wert, der den Anmelde Informationstyp angibt, der für den Zugriff auf Remote Ereignis Quellen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-242">A value that specifies the credential type used for accessing remote event sources.</span></span> <span data-ttu-id="0073a-243">*Type* kann "Default", "Aushandlungs", "Digest", "Basic" oder "LocalMachine" lauten.</span><span class="sxs-lookup"><span data-stu-id="0073a-243">*TYPE* can be "default", "negotiate", "digest", "basic", or "localmachine".</span></span> <span data-ttu-id="0073a-244">Der Standardwert ist "Default".</span><span class="sxs-lookup"><span data-stu-id="0073a-244">The default is "default".</span></span> <span data-ttu-id="0073a-245">Diese Werte werden in der [**\_ \_ \_ Type**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) -Enumeration der Anmelde Informationen des EC-Abonnements definiert.</span><span class="sxs-lookup"><span data-stu-id="0073a-245">These values are defined in the [**EC\_SUBSCRIPTION\_CREDENTIALS\_TYPE**](/windows/desktop/api/Evcoll/ne-evcoll-ec_subscription_credentials_type) enumeration.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/Cun: *Benutzername***</span><span class="sxs-lookup"><span data-stu-id="0073a-246"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-247">Ein-Wert, der die Anmelde Informationen für den freigegebenen Benutzer festlegt, die für Ereignis Quellen verwendet werden, die keine eigenen Anmelde Informationen besitzen.</span><span class="sxs-lookup"><span data-stu-id="0073a-247">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span>

> [!Note]  
> <span data-ttu-id="0073a-248">Wenn dieser Parameter mit der/c-Option verwendet wird, werden die Benutzernamen-und Kenn Wort Einstellungen für einzelne Ereignis Quellen aus der Konfigurationsdatei ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0073a-248">If this parameter is used with the /c option, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="0073a-249">Wenn Sie andere Anmelde Informationen für eine bestimmte Ereignis Quelle verwenden möchten, können Sie diesen Wert überschreiben, indem Sie den/UN-Parameter und den/up-Parameter für eine bestimmte Ereignis Quelle in der Befehlszeile eines anderen Set-Abonnement-Befehls angeben.</span><span class="sxs-lookup"><span data-stu-id="0073a-249">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="0073a-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *Kennwort***</span><span class="sxs-lookup"><span data-stu-id="0073a-250"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-251">Ein-Wert, der das Benutzer Kennwort für die freigegebenen Benutzer Anmelde Informationen festlegt.</span><span class="sxs-lookup"><span data-stu-id="0073a-251">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="0073a-252">Wenn *Password* auf \* (Sternchen) festgelegt ist, wird das Kennwort aus der Konsole gelesen.</span><span class="sxs-lookup"><span data-stu-id="0073a-252">When *PASSWORD* is set to \* (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="0073a-253">Diese Option ist nur gültig, wenn der/Cun-Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-253">This option is only valid when the /cun parameter is specified.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ICA: Finger *Abdrücke***</span><span class="sxs-lookup"><span data-stu-id="0073a-254"><span id="_ica_THUMBPRINTS"></span><span id="_ica_thumbprints"></span><span id="_ICA_THUMBPRINTS"></span>**/ica: *THUMBPRINTS***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-255">Ein-Wert, der die Liste der Fingerabdrücke für Aussteller Zertifikate in einer durch Trennzeichen getrennten Liste festlegt.</span><span class="sxs-lookup"><span data-stu-id="0073a-255">A value that sets the list of issuer certificate thumb prints, in a comma-separated list.</span></span>

> [!Note]  
> <span data-ttu-id="0073a-256">Diese Option ist nur für Quellen initiierte Abonnements spezifisch.</span><span class="sxs-lookup"><span data-stu-id="0073a-256">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="0073a-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *zulässig***</span><span class="sxs-lookup"><span data-stu-id="0073a-257"><span id="_as_ALLOWED"></span><span id="_as_allowed"></span><span id="_AS_ALLOWED"></span>**/as: *ALLOWED***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-258">Ein Wert, der eine durch Trennzeichen getrennte Liste von Zeichen folgen festlegt, die die DNS-Namen von nicht-Domänen Computern angeben, die Abonnements initiieren dürfen.</span><span class="sxs-lookup"><span data-stu-id="0073a-258">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are allowed to initiate subscriptions.</span></span> <span data-ttu-id="0073a-259">Die Namen können mithilfe von Platzhaltern angegeben werden, z \* . b. ". mydomain.com".</span><span class="sxs-lookup"><span data-stu-id="0073a-259">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="0073a-260">Standardmäßig ist diese Liste leer.</span><span class="sxs-lookup"><span data-stu-id="0073a-260">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="0073a-261">Diese Option ist nur für Quellen initiierte Abonnements spezifisch.</span><span class="sxs-lookup"><span data-stu-id="0073a-261">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="0073a-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/DS: *verweigert***</span><span class="sxs-lookup"><span data-stu-id="0073a-262"><span id="_ds_DENIED"></span><span id="_ds_denied"></span><span id="_DS_DENIED"></span>**/ds: *DENIED***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-263">Ein Wert, der eine durch Trennzeichen getrennte Liste von Zeichen folgen festlegt, die die DNS-Namen von nicht-Domänen Computern angeben, die keine Abonnements initiieren dürfen.</span><span class="sxs-lookup"><span data-stu-id="0073a-263">A value that sets a comma-separated list of string that specify the DNS names of non-domain computers that are not allowed to initiate subscriptions.</span></span> <span data-ttu-id="0073a-264">Die Namen können mithilfe von Platzhaltern angegeben werden, z \* . b. ". mydomain.com".</span><span class="sxs-lookup"><span data-stu-id="0073a-264">The names can be specified using wildcards, such as "\*.mydomain.com".</span></span> <span data-ttu-id="0073a-265">Standardmäßig ist diese Liste leer.</span><span class="sxs-lookup"><span data-stu-id="0073a-265">By default, this list is empty.</span></span>

> [!Note]  
> <span data-ttu-id="0073a-266">Diese Option ist nur für Quellen initiierte Abonnements spezifisch.</span><span class="sxs-lookup"><span data-stu-id="0073a-266">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> <dt>

<span data-ttu-id="0073a-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/ADC: *SDDL***</span><span class="sxs-lookup"><span data-stu-id="0073a-267"><span id="_adc_SDDL"></span><span id="_adc_sddl"></span><span id="_ADC_SDDL"></span>**/adc: *SDDL***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-268">Ein Wert, der eine Zeichenfolge im SDDL-Format festlegt, die angibt, welche Domänen Computer zum Initiieren von Abonnements zulässig sind oder nicht.</span><span class="sxs-lookup"><span data-stu-id="0073a-268">A value that sets a string, in SDDL format, that specifies which domain computers are allowed or not allowed to initiate subscriptions.</span></span> <span data-ttu-id="0073a-269">Standardmäßig wird allen Domänen Computern das Initiieren von Abonnements gestattet.</span><span class="sxs-lookup"><span data-stu-id="0073a-269">The default is to allow all domain computers to initiate subscriptions.</span></span>

> [!Note]  
> <span data-ttu-id="0073a-270">Diese Option ist nur für Quellen initiierte Abonnements spezifisch.</span><span class="sxs-lookup"><span data-stu-id="0073a-270">This option is specific to source initiated subscriptions only.</span></span>

 

</dd> </dl>

## <a name="create-a-new-subscription"></a><span data-ttu-id="0073a-271">Erstellen eines neuen Abonnements</span><span class="sxs-lookup"><span data-stu-id="0073a-271">Create a New Subscription</span></span>

<span data-ttu-id="0073a-272">Die folgende Syntax wird verwendet, um ein Ereignis Abonnement für Ereignisse auf einem Remote Computer zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="0073a-272">The following syntax is used to create an event subscription for events on a remote computer.</span></span>

``` syntax
wecutil {cs | create-subscription } CONFIGURATION_FILE [/cun:USERNAME]
[/cup:PASSWORD] 
```

### <a name="remarks"></a><span data-ttu-id="0073a-273">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0073a-273">Remarks</span></span>

<span data-ttu-id="0073a-274">Wenn im Befehl " **wecutil CS** " ein falscher Benutzername oder ein falscher Kennwort angegeben wird, wird kein Fehler gemeldet, bis Sie den Lauf Zeit Status des Abonnements mit dem Befehl " **wecutil GR** " anzeigen.</span><span class="sxs-lookup"><span data-stu-id="0073a-274">When an incorrect username or password is specified in the **wecutil cs** command, no error is reported until you view the runtime status of the subscription using the **wecutil gr** command.</span></span>

## <a name="creation-parameters"></a><span data-ttu-id="0073a-275">Erstellungs Parameter</span><span class="sxs-lookup"><span data-stu-id="0073a-275">Creation Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0073a-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**Konfigurations \_ Datei**</span><span class="sxs-lookup"><span data-stu-id="0073a-276"><span id="CONFIGURATION_FILE"></span><span id="configuration_file"></span>**CONFIGURATION\_FILE**</span></span>
</dt> <dd>

<span data-ttu-id="0073a-277">Ein-Wert, der den Pfad zur XML-Datei angibt, die Informationen zur Abonnement Konfiguration enthält.</span><span class="sxs-lookup"><span data-stu-id="0073a-277">A value that specifies the path to the XML file that contains subscription configuration information.</span></span> <span data-ttu-id="0073a-278">Der Pfad kann absolut oder relativ zum aktuellen Verzeichnis sein.</span><span class="sxs-lookup"><span data-stu-id="0073a-278">The path can be absolute or relative to the current directory.</span></span>

<span data-ttu-id="0073a-279">Der folgende XML-Code ist ein Beispiel für eine Abonnement Konfigurationsdatei, die ein vom Collector initiiertes Abonnement erstellt, um Ereignisse aus dem Anwendungs Ereignisprotokoll eines Remote Computers an das ForwardedEvents-Protokoll weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="0073a-279">The following XML is an example of a subscription configuration file that creates a collector initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleCISubscription</SubscriptionId>
    <SubscriptionType>CollectorInitiated</SubscriptionType>
    <Description>Collector Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>20</MaxItems>
            <MaxLatencyTime>60000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <HostName>thisMachine.myDomain.com</HostName>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2010-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>*</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>false</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <CredentialsType>Default</CredentialsType>

    <EventSources>
        <EventSource Enabled="true">
            <Address>mySource.myDomain.com</Address>
            <UserName>myUserName</UserName>
        </EventSource>
    </EventSources>
</Subscription>
```



<span data-ttu-id="0073a-280">Der folgende XML-Code ist ein Beispiel für eine Abonnement Konfigurationsdatei, die ein von der Quelle initiiertes Abonnement erstellt, mit dem Ereignisse aus dem Anwendungs Ereignisprotokoll eines Remote Computers an das ForwardedEvents-Protokoll weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="0073a-280">The following XML is an example of a subscription configuration file that creates a source initiated subscription to forward events from the Application event log of a remote computer to the ForwardedEvents log.</span></span>


```XML
<Subscription xmlns="http://schemas.microsoft.com/2006/03/windows/events/subscription">
    <SubscriptionId>SampleSISubscription</SubscriptionId>
    <SubscriptionType>SourceInitiated</SubscriptionType>
    <Description>Source Initiated Subscription Sample</Description>
    <Enabled>true</Enabled>
    <Uri>http://schemas.microsoft.com/wbem/wsman/1/windows/EventLog</Uri>

    <!-- Use Normal (default), Custom, MinLatency, MinBandwidth -->
    <ConfigurationMode>Custom</ConfigurationMode>

    <Delivery Mode="Push">
        <Batching>
            <MaxItems>1</MaxItems>
            <MaxLatencyTime>1000</MaxLatencyTime>
        </Batching>
        <PushSettings>
            <Heartbeat Interval="60000"/>
        </PushSettings>
    </Delivery>

    <Expires>2018-01-01T00:00:00.000Z</Expires>

    <Query>
        <![CDATA[
            <QueryList>
                <Query Path="Application">
                    <Select>Event[System/EventID='999']</Select>
                </Query>
            </QueryList>
        ]]>
    </Query>

    <ReadExistingEvents>true</ReadExistingEvents>
    <TransportName>http</TransportName>
    <ContentFormat>RenderedText</ContentFormat>
    <Locale Language="en-US"/>
    <LogFile>ForwardedEvents</LogFile>
    <AllowedSourceNonDomainComputers></AllowedSourceNonDomainComputers>
    <AllowedSourceDomainComputers>O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)</AllowedSourceDomainComputers>
</Subscription>
```



> [!Note]  
> <span data-ttu-id="0073a-281">Beim Erstellen eines von der Quelle initiierten Abonnements werden, wenn " **zugswedsourcedomaincomputers**", "zugswedsourcenondomaincomputers  / **issuercalist**", " **zugswedsubjetlist**" und " **deniedsubjetlist** " leer sind, standardmäßig ein Standardwert für "' o:NSG: nsd: (a;;  GA;;;D C) (A;; GA;;; NS) ".</span><span class="sxs-lookup"><span data-stu-id="0073a-281">When creating a source initiated subscription, if **AllowedSourceDomainComputers**, **AllowedSourceNonDomainComputers**/**IssuerCAList**, **AllowedSubjectList**, and **DeniedSubjectList** are all empty, then a default will be provided for **AllowedSourceDomainComputers** - "O:NSG:NSD:(A;;GA;;;DC)(A;;GA;;;NS)".</span></span> <span data-ttu-id="0073a-282">Diese SDDL-Standardeinstellung gewährt Mitgliedern der Domänen Gruppe "Domänen Computer" sowie der Gruppe "lokaler Netzwerkdienst" (für die lokale Weiterleitung) die Möglichkeit, Ereignisse für dieses Abonnement zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="0073a-282">This SDDL default grants members of the Domain Computers domain group, as well as the local Network Service group (for the local forwarder), the ability to raise events for this subscription.</span></span>

 

</dd> <dt>

<span data-ttu-id="0073a-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/Cun: *Benutzername***</span><span class="sxs-lookup"><span data-stu-id="0073a-283"><span id="_cun_USERNAME"></span><span id="_cun_username"></span><span id="_CUN_USERNAME"></span>**/cun: *USERNAME***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-284">Ein-Wert, der die Anmelde Informationen für den freigegebenen Benutzer festlegt, die für Ereignis Quellen verwendet werden, die keine eigenen Anmelde Informationen besitzen.</span><span class="sxs-lookup"><span data-stu-id="0073a-284">A value that sets the shared user credentials used for event sources that do not have their own user credentials.</span></span> <span data-ttu-id="0073a-285">Dieser Wert gilt nur für vom Collector initiierte Abonnements.</span><span class="sxs-lookup"><span data-stu-id="0073a-285">This value applies to collector initiated subscriptions only.</span></span>

> [!Note]  
> <span data-ttu-id="0073a-286">Wenn dieser Parameter angegeben ist, werden die Einstellungen für Benutzername und Kennwort für einzelne Ereignis Quellen aus der Konfigurationsdatei ignoriert.</span><span class="sxs-lookup"><span data-stu-id="0073a-286">If this parameter is specified, then user name and password settings for individual event sources from the configuration file are ignored.</span></span> <span data-ttu-id="0073a-287">Wenn Sie andere Anmelde Informationen für eine bestimmte Ereignis Quelle verwenden möchten, können Sie diesen Wert überschreiben, indem Sie den/UN-Parameter und den/up-Parameter für eine bestimmte Ereignis Quelle in der Befehlszeile eines anderen Set-Abonnement-Befehls angeben.</span><span class="sxs-lookup"><span data-stu-id="0073a-287">If you want to use different credentials for a specific event source, you can override this value by specifying the /un and /up parameters for a specific event source on the command line of another set-subscription command.</span></span>

 

</dd> <dt>

<span data-ttu-id="0073a-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/Cup: *Kennwort***</span><span class="sxs-lookup"><span data-stu-id="0073a-288"><span id="_cup_PASSWORD"></span><span id="_cup_password"></span><span id="_CUP_PASSWORD"></span>**/cup: *PASSWORD***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-289">Ein-Wert, der das Benutzer Kennwort für die freigegebenen Benutzer Anmelde Informationen festlegt.</span><span class="sxs-lookup"><span data-stu-id="0073a-289">A value that sets the user password for the shared user credentials.</span></span> <span data-ttu-id="0073a-290">Wenn *Password* auf " \* " (Sternchen) festgelegt ist, wird das Kennwort aus der Konsole gelesen.</span><span class="sxs-lookup"><span data-stu-id="0073a-290">When *PASSWORD* is set to "\*" (asterisk), then the password is read from the console.</span></span> <span data-ttu-id="0073a-291">Diese Option ist nur gültig, wenn der/Cun-Parameter angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-291">This option is only valid when the /cun parameter is specified.</span></span>

</dd> </dl>

## <a name="delete-a-subscription"></a><span data-ttu-id="0073a-292">Löschen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="0073a-292">Delete a Subscription</span></span>

<span data-ttu-id="0073a-293">Die folgende Syntax wird verwendet, um ein Ereignis Abonnement zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0073a-293">The following syntax is used to delete an event subscription.</span></span>

``` syntax
wecutil { ds | delete-subscription } SUBSCRIPTION_ID
```

## <a name="deletion-parameters"></a><span data-ttu-id="0073a-294">Lösch Parameter</span><span class="sxs-lookup"><span data-stu-id="0073a-294">Deletion Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0073a-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**Abonnement- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="0073a-295"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="0073a-296">Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0073a-296">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="0073a-297">Dieser Bezeichner wird in der XML-Konfigurationsdatei, die zum Erstellen des Abonnements verwendet wird, im **Abonnement-ID** -Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="0073a-297">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="0073a-298">Das in diesem Parameter identifizierte Abonnement wird gelöscht.</span><span class="sxs-lookup"><span data-stu-id="0073a-298">The subscription identified in this parameter will be deleted.</span></span>

</dd> </dl>

## <a name="retry-a-subscription"></a><span data-ttu-id="0073a-299">Wiederholen eines Abonnements</span><span class="sxs-lookup"><span data-stu-id="0073a-299">Retry a subscription</span></span>

<span data-ttu-id="0073a-300">Die folgende Syntax wird verwendet, um ein inaktives Abonnement zu wiederholen, indem versucht wird, alle oder angegebene Ereignis Quellen zu reaktivieren, indem eine Verbindung mit jeder Ereignis Quelle hergestellt und eine Remote Abonnement Anforderung an die Ereignis Quelle gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-300">The following syntax is used to retry an inactive subscription by attempting to reactivate all or specified event sources by establishing a connection to each event source and sending a remote subscription request to the event source.</span></span> <span data-ttu-id="0073a-301">Deaktivierte Ereignis Quellen werden nicht wiederholt.</span><span class="sxs-lookup"><span data-stu-id="0073a-301">Disabled event sources are not retried.</span></span>

``` syntax
wecutil { rs | retry-subscription } SUBSCRIPTION_ID 
[EVENT_SOURCE [EVENT_SOURCE] ...]
```

## <a name="retry-parameters"></a><span data-ttu-id="0073a-302">Wiederholungs Parameter</span><span class="sxs-lookup"><span data-stu-id="0073a-302">Retry Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0073a-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**Abonnement- \_ ID**</span><span class="sxs-lookup"><span data-stu-id="0073a-303"><span id="SUBSCRIPTION_ID"></span><span id="subscription_id"></span>**SUBSCRIPTION\_ID**</span></span>
</dt> <dd>

<span data-ttu-id="0073a-304">Eine Zeichenfolge, die ein Abonnement eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0073a-304">A string that uniquely identifies a subscription.</span></span> <span data-ttu-id="0073a-305">Dieser Bezeichner wird in der XML-Konfigurationsdatei, die zum Erstellen des Abonnements verwendet wird, im **Abonnement-ID** -Element angegeben.</span><span class="sxs-lookup"><span data-stu-id="0073a-305">This identifier is specified in the **SubscriptionId** element in the XML configuration file used to create the subscription.</span></span> <span data-ttu-id="0073a-306">Das in diesem Parameter identifizierte Abonnement wird wiederholt.</span><span class="sxs-lookup"><span data-stu-id="0073a-306">The subscription identified in this parameter will be retried.</span></span>

</dd> <dt>

<span data-ttu-id="0073a-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**Ereignis \_ Quelle**</span><span class="sxs-lookup"><span data-stu-id="0073a-307"><span id="EVENT_SOURCE"></span><span id="event_source"></span>**EVENT\_SOURCE**</span></span>
</dt> <dd>

<span data-ttu-id="0073a-308">Ein-Wert, der einen Computer identifiziert, bei dem es sich um eine Ereignis Quelle für ein Ereignis Abonnement handelt.</span><span class="sxs-lookup"><span data-stu-id="0073a-308">A value that identifies a computer that is an event source for an event subscription.</span></span> <span data-ttu-id="0073a-309">Bei diesem Wert kann es sich um den voll qualifizierten Domänen Namen für den Computer, den NetBIOS-Namen oder die IP-Adresse handeln.</span><span class="sxs-lookup"><span data-stu-id="0073a-309">This value can be the fully qualified domain name for the computer, NetBIOS name, or IP address.</span></span>

</dd> </dl>

## <a name="configure-the-windows-event-collector-service"></a><span data-ttu-id="0073a-310">Konfigurieren des Windows-Ereignis Sammler Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0073a-310">Configure the Windows Event Collector Service</span></span>

<span data-ttu-id="0073a-311">Die folgende Syntax wird verwendet, um den Windows-Ereignis Sammlungs Dienst zu konfigurieren, um sicherzustellen, dass Ereignis Abonnements durch Neustarts von Computern erstellt und aufrechterhalten werden können.</span><span class="sxs-lookup"><span data-stu-id="0073a-311">The following syntax is used to configure the Windows Event Collector service to ensure event subscriptions can be created and sustained through computer restarts.</span></span> <span data-ttu-id="0073a-312">Dies umfasst das folgende Verfahren:</span><span class="sxs-lookup"><span data-stu-id="0073a-312">This includes the following procedure:</span></span>

<span data-ttu-id="0073a-313">**So konfigurieren Sie den Windows-Ereignis Sammlungs Dienst**</span><span class="sxs-lookup"><span data-stu-id="0073a-313">**To configure the Windows Event Collector service**</span></span>

1.  <span data-ttu-id="0073a-314">Aktivieren Sie den Kanal ForwardedEvents, wenn er deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0073a-314">Enable the ForwardedEvents channel if it is disabled.</span></span>
2.  <span data-ttu-id="0073a-315">Verzögern Sie den Start des Windows-Ereignis Sammlungs Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="0073a-315">Delay the start of the Windows Event Collector service.</span></span>
3.  <span data-ttu-id="0073a-316">Starten Sie den Windows-Ereignis Sammler Dienst, wenn er nicht ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-316">Start the Windows Event Collector service if it is not running.</span></span>

``` syntax
wecutil { qc | quick-config } /q:VALUE
```

## <a name="configure-event-collector-parameters"></a><span data-ttu-id="0073a-317">Ereignis Sammler Parameter konfigurieren</span><span class="sxs-lookup"><span data-stu-id="0073a-317">Configure Event Collector Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0073a-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *Wert***</span><span class="sxs-lookup"><span data-stu-id="0073a-318"><span id="_q_VALUE"></span><span id="_q_value"></span><span id="_Q_VALUE"></span>**/q: *VALUE***</span></span>
</dt> <dd>

<span data-ttu-id="0073a-319">Ein-Wert, der bestimmt, ob der Quick-config-Befehl zur Bestätigung aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="0073a-319">A value that determines whether the quick-config command will prompt for confirmation.</span></span> <span data-ttu-id="0073a-320">Der Wert kann "true" oder "false" sein.</span><span class="sxs-lookup"><span data-stu-id="0073a-320">VALUE can be true or false.</span></span> <span data-ttu-id="0073a-321">Wenn value den Wert true hat, wird der Befehl zur Bestätigung aufgefordert.</span><span class="sxs-lookup"><span data-stu-id="0073a-321">If VALUE is true, then the command will prompt for confirmation.</span></span> <span data-ttu-id="0073a-322">Der Standardwert ist „FALSE“.</span><span class="sxs-lookup"><span data-stu-id="0073a-322">The default value is false.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0073a-323">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0073a-323">Requirements</span></span>



| <span data-ttu-id="0073a-324">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0073a-324">Requirement</span></span> | <span data-ttu-id="0073a-325">Wert</span><span class="sxs-lookup"><span data-stu-id="0073a-325">Value</span></span> |
|-------------------------------------|--------------------------------|
| <span data-ttu-id="0073a-326">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0073a-326">Minimum supported client</span></span><br/> | <span data-ttu-id="0073a-327">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="0073a-327">Windows Vista</span></span><br/>       |
| <span data-ttu-id="0073a-328">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0073a-328">Minimum supported server</span></span><br/> | <span data-ttu-id="0073a-329">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0073a-329">Windows Server 2008</span></span><br/> |



 

 





