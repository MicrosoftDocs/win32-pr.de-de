---
title: Ereignisablaufverfolgung in ADSI
description: Unter Windows Server 2008 und Windows Vista wird die Ereignisablaufverfolgung in Active Directory Service Interfaces (ADSI) eingeführt.
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- Ereignisablaufverfolgung ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b26aee00404f5cf97d228698f64fec804c28e62
ms.sourcegitcommit: 0f7a8198bacd5493ab1e78a9583c7a3578794765
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/25/2021
ms.locfileid: "110423711"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="d9152-104">Ereignisablaufverfolgung in ADSI</span><span class="sxs-lookup"><span data-stu-id="d9152-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="d9152-105">Unter Windows Server 2008 und Windows Vista wird die [Ereignisablaufverfolgung](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d9152-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="d9152-106">Bestimmte Bereiche des ADSI LDAP-Anbieters verfügen über eine zugrunde liegende Implementierung, die komplex ist oder eine Abfolge von Schritten umfasst, die die Diagnose von Problemen erschwert.</span><span class="sxs-lookup"><span data-stu-id="d9152-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="d9152-107">Um Anwendungsentwickler bei der Problembehandlung zu unterstützen, wurde die Ereignisablaufverfolgung zu den folgenden Bereichen hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="d9152-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="d9152-108">Schema analysieren und herunterladen</span><span class="sxs-lookup"><span data-stu-id="d9152-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="d9152-109">Die IADs-Schnittstelle in ADSI erfordert, dass das LDAP-Schema auf dem Client zwischengespeichert wird, damit Attribute ordnungsgemäß gemarshallt werden können (wie im [ADSI-Schemamodell](adsi-schema-model.md)beschrieben).</span><span class="sxs-lookup"><span data-stu-id="d9152-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="d9152-110">Um dies zu erreichen, lädt ADSI das Schema für jeden Prozess (und für jeden LDAP-Server/jede LDAP-Domäne) entweder aus einer Schemadatei (SCH), die auf dem lokalen Datenträger gespeichert ist, oder durch Herunterladen vom LDAP-Server in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="d9152-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="d9152-111">Verschiedene Prozesse auf demselben Clientcomputer verwenden das zwischengespeicherte Schema auf dem Datenträger, wenn es verfügbar und anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="d9152-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="d9152-112">Wenn das Schema nicht vom Datenträger oder Server abgerufen werden kann, verwendet ADSI ein hartcodiertes Standardschema.</span><span class="sxs-lookup"><span data-stu-id="d9152-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="d9152-113">In diesem Fall können Attribute, die nicht Teil dieses Standardschemas sind, nicht gemarshallt werden, und ADSI gibt beim Abrufen dieser Attribute einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="d9152-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="d9152-114">Dies kann durch eine Reihe von Faktoren verursacht werden, z. B. Probleme beim Analysieren des Schemas und unzureichende Berechtigungen zum Herunterladen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="d9152-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="d9152-115">Es ist oft schwierig zu bestimmen, warum ein bestimmtes Standardschema verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d9152-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="d9152-116">Die Verwendung der Ereignisablaufverfolgung in diesem Bereich hilft, das Problem schneller zu diagnostizieren und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="d9152-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="d9152-117">Ändern und Festlegen des Kennworts</span><span class="sxs-lookup"><span data-stu-id="d9152-117">Changing and Setting the Password</span></span>

<span data-ttu-id="d9152-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) und [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) verwenden mehrere Mechanismen, um den angeforderten Vorgang basierend auf der verfügbaren Konfiguration auszuführen (wie unter [Festlegen und Ändern von Benutzerpasswörtern mit dem LDAP-Anbieter](setting-user-passwords-for-ldap-providers.md)beschrieben).</span><span class="sxs-lookup"><span data-stu-id="d9152-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="d9152-119">Wenn **ChangePassword und** **SetPassword** fehlschlagen, kann es schwierig sein, genau den Grund zu ermitteln, und die Ereignisablaufverfolgung hilft bei der Behandlung von Problemen mit diesen Methoden.</span><span class="sxs-lookup"><span data-stu-id="d9152-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="d9152-120">ADSI-Bindungscache</span><span class="sxs-lookup"><span data-stu-id="d9152-120">ADSI Bind Cache</span></span>

<span data-ttu-id="d9152-121">ADSI versucht intern, LDAP-Verbindungen nach Möglichkeit wiederzuverwenden (siehe [Verbindungszwischenspeicherung](connection-caching.md)).</span><span class="sxs-lookup"><span data-stu-id="d9152-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="d9152-122">Bei der Problembehandlung ist es hilfreich zu verfolgen, ob eine neue Verbindung für die Kommunikation mit dem Server geöffnet wurde oder ob eine vorhandene Verbindung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d9152-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="d9152-123">Es kann auch nützlich sein, den Lebenszyklus des Verbindungscaches (manchmal auch als Bindungscache bezeichnet) und dessen Erstellung oder Abschluss zu verfolgen und zu überprüfen, ob eine Verbindungsempfehlung stattgefunden hat.</span><span class="sxs-lookup"><span data-stu-id="d9152-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="d9152-124">Bei einer serverlosen Bindung ruft ADSI den DC-Locator [auf,](/windows/desktop/AD/serverless-binding-and-rootdse)um einen Server für die Domäne des Kontexts des Benutzers auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="d9152-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="d9152-125">ADSI verwaltet dann einen Cache der Domänenserverzuordnung für nachfolgende Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="d9152-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="d9152-126">Die Ereignisablaufverfolgung hilft bei der Nachverfolgung der Auswahl des Domänencontrollers und ist daher hilfreich bei der Behandlung von verbindungsbezogenen Problemen.</span><span class="sxs-lookup"><span data-stu-id="d9152-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="d9152-127">Aktivieren der Ablaufverfolgung und Starten einer Ablaufverfolgungssitzung</span><span class="sxs-lookup"><span data-stu-id="d9152-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="d9152-128">Um die ADSI-Ablaufverfolgung zu aktivieren, erstellen Sie den folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="d9152-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="d9152-129">**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **_ProcessName_**</span><span class="sxs-lookup"><span data-stu-id="d9152-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**_ProcessName_**</span></span>

<span data-ttu-id="d9152-130">*ProcessName* ist der vollständige Name des Prozesses, den Sie verfolgen möchten, einschließlich der Erweiterung (z. B. "Svchost.exe").</span><span class="sxs-lookup"><span data-stu-id="d9152-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="d9152-131">Darüber hinaus können Sie einen optionalen Wert vom Typ **DWORD** mit dem Namen PID in diesen Schlüssel platzieren.</span><span class="sxs-lookup"><span data-stu-id="d9152-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="d9152-132">Es wird dringend empfohlen, diesen Wert zu setzen und dadurch nur einen bestimmten Prozess zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="d9152-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="d9152-133">Andernfalls werden alle Durch *ProcessName* angegebenen Instanzen der Anwendung nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="d9152-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="d9152-134">Führen Sie dann den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="d9152-134">Then execute the following command:</span></span>

<span data-ttu-id="d9152-135">**tracelog.exe -start** *sessionname* **-guid \#** provider _\_ guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span><span class="sxs-lookup"><span data-stu-id="d9152-135">**tracelog.exe -start** *sessionname* **-guid \#**_provider\_guid_ **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="d9152-136">*sessionname* ist einfach ein beliebiger Bezeichner, der zum Bezeichnen der Ablaufverfolgungssitzung verwendet wird (Sie müssen später auf diesen Sitzungsnamen verweisen, wenn Sie die Ablaufverfolgungssitzung beenden).</span><span class="sxs-lookup"><span data-stu-id="d9152-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="d9152-137">Die GUID für den ADSI-Nachverfolgungsanbieter lautet "7288c9f8-d63c-4932-a345-89d6b060174d".</span><span class="sxs-lookup"><span data-stu-id="d9152-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="d9152-138">*filename* gibt die Protokolldatei an, in die Ereignisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d9152-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="d9152-139">*traceFlags* sollte einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="d9152-139">*traceFlags* should be one of the following values:</span></span>



|         <span data-ttu-id="d9152-140">Flag</span><span class="sxs-lookup"><span data-stu-id="d9152-140">Flag</span></span>                        |         <span data-ttu-id="d9152-141">Wert</span><span class="sxs-lookup"><span data-stu-id="d9152-141">Value</span></span>              |
|---------------------------------|-----------------------|
| <span data-ttu-id="d9152-142">**\_DEBUGSCHEMA**</span><span class="sxs-lookup"><span data-stu-id="d9152-142">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="d9152-143">0x00000001</span><span class="sxs-lookup"><span data-stu-id="d9152-143">0x00000001</span></span><br/> |
| <span data-ttu-id="d9152-144">**DEBUGGEN \_ VON CHANGEPWD**</span><span class="sxs-lookup"><span data-stu-id="d9152-144">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="d9152-145">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d9152-145">0x00000002</span></span><br/> |
| <span data-ttu-id="d9152-146">**DEBUGGEN \_ VON SETPWD**</span><span class="sxs-lookup"><span data-stu-id="d9152-146">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="d9152-147">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d9152-147">0x00000004</span></span><br/> |
| <span data-ttu-id="d9152-148">**DEBUGGEN \_ VON BINDCACHE**</span><span class="sxs-lookup"><span data-stu-id="d9152-148">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="d9152-149">0x00000008</span><span class="sxs-lookup"><span data-stu-id="d9152-149">0x00000008</span></span><br/> |



 

<span data-ttu-id="d9152-150">Diese Flags bestimmen gemäß der folgenden Tabelle, welche [ADSI-Methoden](active-directory-service-interfaces-adsi.md) nachverfolgt werden:</span><span class="sxs-lookup"><span data-stu-id="d9152-150">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9152-151"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="d9152-151"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="d9152-152">LdapGetSchema</span><span class="sxs-lookup"><span data-stu-id="d9152-152">LdapGetSchema</span></span></li>
<li><span data-ttu-id="d9152-153">GetSchemaInfoTime</span><span class="sxs-lookup"><span data-stu-id="d9152-153">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="d9152-154">LdapReadSchemaInfoFromServer</span><span class="sxs-lookup"><span data-stu-id="d9152-154">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="d9152-155">ProcessSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="d9152-155">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="d9152-156">HelperReadLdapSchemaInfo</span><span class="sxs-lookup"><span data-stu-id="d9152-156">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="d9152-157">ProcessClassInfoArray</span><span class="sxs-lookup"><span data-stu-id="d9152-157">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="d9152-158">ReadSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="d9152-158">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="d9152-159">StoreSchemaInfoFromRegistry</span><span class="sxs-lookup"><span data-stu-id="d9152-159">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="d9152-160">AttributeTypeDescription</span><span class="sxs-lookup"><span data-stu-id="d9152-160">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="d9152-161">ObjectClassDescription</span><span class="sxs-lookup"><span data-stu-id="d9152-161">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="d9152-162">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="d9152-162">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="d9152-163">DirectoryString</span><span class="sxs-lookup"><span data-stu-id="d9152-163">DirectoryString</span></span></li>
<li><span data-ttu-id="d9152-164">DirectoryStrings</span><span class="sxs-lookup"><span data-stu-id="d9152-164">DirectoryStrings</span></span></li>
<li><span data-ttu-id="d9152-165">DITContentRuleDescription</span><span class="sxs-lookup"><span data-stu-id="d9152-165">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9152-166"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="d9152-166"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="d9152-167">CADsUser::ChangePassword</span><span class="sxs-lookup"><span data-stu-id="d9152-167">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d9152-168"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="d9152-168"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="d9152-169">CADsUser::SetPassword</span><span class="sxs-lookup"><span data-stu-id="d9152-169">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9152-170"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="d9152-170"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="d9152-171">GetServerBasedObject</span><span class="sxs-lookup"><span data-stu-id="d9152-171">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="d9152-172">GetServerLessBasedObject</span><span class="sxs-lookup"><span data-stu-id="d9152-172">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="d9152-173">GetGCDomainName</span><span class="sxs-lookup"><span data-stu-id="d9152-173">GetGCDomainName</span></span></li>
<li><span data-ttu-id="d9152-174">GetDefaultDomainName</span><span class="sxs-lookup"><span data-stu-id="d9152-174">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="d9152-175">GetUserDomainFlatName</span><span class="sxs-lookup"><span data-stu-id="d9152-175">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="d9152-176">BindCacheLookup</span><span class="sxs-lookup"><span data-stu-id="d9152-176">BindCacheLookup</span></span></li>
<li><span data-ttu-id="d9152-177">EquivalentPortNumbers</span><span class="sxs-lookup"><span data-stu-id="d9152-177">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="d9152-178">CanCredentialsBeReused</span><span class="sxs-lookup"><span data-stu-id="d9152-178">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="d9152-179">BindCacheAdd</span><span class="sxs-lookup"><span data-stu-id="d9152-179">BindCacheAdd</span></span></li>
<li><span data-ttu-id="d9152-180">BindCacheAddRef</span><span class="sxs-lookup"><span data-stu-id="d9152-180">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="d9152-181">AddReferralLink</span><span class="sxs-lookup"><span data-stu-id="d9152-181">AddReferralLink</span></span></li>
<li><span data-ttu-id="d9152-182">CommonRemoveEntry</span><span class="sxs-lookup"><span data-stu-id="d9152-182">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="d9152-183">BindCacheDerefHelper</span><span class="sxs-lookup"><span data-stu-id="d9152-183">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="d9152-184">NotifyNewConnection</span><span class="sxs-lookup"><span data-stu-id="d9152-184">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="d9152-185">QueryForConnection</span><span class="sxs-lookup"><span data-stu-id="d9152-185">QueryForConnection</span></span></li>
<li><span data-ttu-id="d9152-186">LdapOpenBindWithCredentials</span><span class="sxs-lookup"><span data-stu-id="d9152-186">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="d9152-187">LdapOpenBindWithDefaultCredentials</span><span class="sxs-lookup"><span data-stu-id="d9152-187">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d9152-188">Sie können Flags kombinieren, indem Sie die entsprechenden Bits im *traceFlags-Argument* kombinieren.</span><span class="sxs-lookup"><span data-stu-id="d9152-188">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="d9152-189">Um beispielsweise die **FLAGS DEBUG \_ SCHEMA** und **DEBUG \_ BINDCACHE** anzugeben, wird der entsprechende *traceFlags-Wert* 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="d9152-189">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="d9152-190">Schließlich sollte das *flag traceLevel* einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="d9152-190">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|      <span data-ttu-id="d9152-191">Flag</span><span class="sxs-lookup"><span data-stu-id="d9152-191">Flag</span></span>                                    |       <span data-ttu-id="d9152-192">Wert</span><span class="sxs-lookup"><span data-stu-id="d9152-192">Value</span></span>                |
|------------------------------------------|-----------------------|
| <span data-ttu-id="d9152-193">**\_FEHLER AUF ABLAUFVERFOLGUNGSEBENE \_**</span><span class="sxs-lookup"><span data-stu-id="d9152-193">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="d9152-194">0x00000002</span><span class="sxs-lookup"><span data-stu-id="d9152-194">0x00000002</span></span><br/> |
| <span data-ttu-id="d9152-195">**\_INFORMATIONEN AUF ABLAUFVERFOLGUNGSEBENE \_**</span><span class="sxs-lookup"><span data-stu-id="d9152-195">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="d9152-196">0x00000004</span><span class="sxs-lookup"><span data-stu-id="d9152-196">0x00000004</span></span><br/> |



 

<span data-ttu-id="d9152-197">**TRACE \_ LEVEL \_ INFORMATION** bewirkt, dass der Ablaufverfolgungsprozess alle Ereignisse aufzeichnet, während **TRACE LEVEL \_ \_ ERROR** bewirkt, dass der Ablaufverfolgungsprozess nur Fehlerereignisse aufzeichnet.</span><span class="sxs-lookup"><span data-stu-id="d9152-197">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="d9152-198">Führen Sie den folgenden Befehl aus, um die Ablaufverfolgung zu beenden:</span><span class="sxs-lookup"><span data-stu-id="d9152-198">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="d9152-199">**tracelog.exe -stop** *sessionname*</span><span class="sxs-lookup"><span data-stu-id="d9152-199">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="d9152-200">Im vorherigen Beispiel ist *sessionname* derselbe Name wie der, der mit dem Befehl bereitgestellt wurde, der den Ablaufverfolgungsabschnitt gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d9152-200">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="d9152-201">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d9152-201">Remarks</span></span>

<span data-ttu-id="d9152-202">Es ist effektiver, nur bestimmte Prozesse durch Angabe einer bestimmten PID nachzuverfolgen, als alle Prozesse auf einem Computer nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="d9152-202">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="d9152-203">Wenn Sie mehrere Anwendungen auf demselben Computer nachverfolgen müssen, kann dies auswirkungen auf die Leistung haben. in leistungsorientierten Abschnitten des Codes gibt es umfangreiche Debugausgaben.</span><span class="sxs-lookup"><span data-stu-id="d9152-203">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="d9152-204">Außerdem müssen Administratoren darauf achten, die Berechtigungen der Protokolldateien bei der Ablaufverfolgung mehrerer Prozesse ordnungsgemäß festzulegen. Andernfalls kann jeder Benutzer die Ablaufverfolgungsprotokolle lesen, und andere Benutzer können Prozesse nachverfolgen, die sichere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="d9152-204">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="d9152-205">Angenommen, der Administrator richtet die Ablaufverfolgung für eine Anwendung "Test.exe" ein und gibt keine PID in der Registrierung an, um mehrere Instanzen des Prozesses zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="d9152-205">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="d9152-206">Nun möchte ein anderer Benutzer die Anwendung "Secure.exe" verfolgen.</span><span class="sxs-lookup"><span data-stu-id="d9152-206">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="d9152-207">Wenn die Ablaufverfolgungsprotokolldateien nicht ordnungsgemäß eingeschränkt sind, muss der Benutzer nur "Secure.exe" in "Test.exe" umbenennen, und er wird nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="d9152-207">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="d9152-208">Im Allgemeinen ist es am besten, bei der Problembehandlung nur bestimmte Prozesse zu verfolgen und den Registrierungsschlüssel für die Ablaufverfolgung zu entfernen, sobald die Problembehandlung durchgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="d9152-208">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="d9152-209">Da die Aktivierung der Ereignisablaufverfolgung zusätzliche Protokolldateien erzeugt, sollten Administratoren die Protokolldateigrößen sorgfältig überwachen. Fehlender Speicherplatz auf dem lokalen Computer kann zu einem Denial-of-Service-Angriff führen.</span><span class="sxs-lookup"><span data-stu-id="d9152-209">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="d9152-210">Beispielszenarien</span><span class="sxs-lookup"><span data-stu-id="d9152-210">Example Scenarios</span></span>

<span data-ttu-id="d9152-211">Szenario 1: Der Administrator sieht einen unerwarteten Fehler in einer Anwendung, die Kennwörter für Benutzerkonten festgelegt, sodass er die folgenden Schritte ausführen würde, um das Problem mithilfe der Ereignisablaufverfolgung zu beheben.</span><span class="sxs-lookup"><span data-stu-id="d9152-211">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="d9152-212">Schreiben Sie ein Skript, das das Problem reproduziert, und erstellen Sie den Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="d9152-212">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="d9152-213">**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="d9152-213">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="d9152-214">Starten Sie mithilfe des folgenden Befehls eine Ablaufverfolgungssitzung, indem Sie *traceFlags* auf 0x2 (**DEBUG \_ CHANGEPASSWD**) und *traceLevel* auf 0x4 (**TRACE LEVEL \_ \_ INFORMATION)** festlegen:</span><span class="sxs-lookup"><span data-stu-id="d9152-214">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="d9152-215">**tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**</span><span class="sxs-lookup"><span data-stu-id="d9152-215">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="d9152-216">Führen cscript.exe Testskript aus, um das Problem zu reproduzieren, und beenden Sie dann die Ablaufverfolgungssitzung:</span><span class="sxs-lookup"><span data-stu-id="d9152-216">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="d9152-217">**tracelog.exe -stop scripttrace**</span><span class="sxs-lookup"><span data-stu-id="d9152-217">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="d9152-218">Löschen des Registrierungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="d9152-218">Delete the registry key</span></span>

    <span data-ttu-id="d9152-219">**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="d9152-219">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="d9152-220">Führen Sie das ETW-Tool Tracerpt.exe, um die Ablaufverfolgungsinformationen aus dem Protokoll zu analysieren:</span><span class="sxs-lookup"><span data-stu-id="d9152-220">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="d9152-221">**tracelog.exe -start scripttrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ adsi.etl -flag 0x2 -level 0x4**</span><span class="sxs-lookup"><span data-stu-id="d9152-221">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="d9152-222">Szenario 2: Der Administrator möchte die Schemaparsing- und Downloadvorgänge in einer [ASP-Anwendung](https://msdn.microsoft.com/asp.net/default.aspx) mit dem Namen w3wp.exe, die bereits ausgeführt wird, nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="d9152-222">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="d9152-223">Dazu würde der Administrator die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="d9152-223">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="d9152-224">Erstellen des Registrierungsschlüssels</span><span class="sxs-lookup"><span data-stu-id="d9152-224">Create the registry key</span></span>

    <span data-ttu-id="d9152-225">**HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**</span><span class="sxs-lookup"><span data-stu-id="d9152-225">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="d9152-226">erstellen Sie in diesem Schlüssel einen Wert vom Typ DWORD mit dem Namen PID, und legen Sie ihn auf die Prozess-ID der Instanz von w3wp.exe fest, die derzeit auf dem lokalen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d9152-226">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="d9152-227">Anschließend erstellen sie eine Ablaufverfolgungssitzung und legen *traceFlags* auf 0x1 (**DEBUG \_ SCHEMA**) und *traceLevel* auf 0x4 (**TRACE LEVEL \_ \_ INFORMATION**) fest:</span><span class="sxs-lookup"><span data-stu-id="d9152-227">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="d9152-228">**tracelog.exe -start w3wptrace -guid \# 7288c9f8-d63c-4932-a345-89d6b060174d -f . \\ w3wp.etl -flag 0x1 -level 0x4**</span><span class="sxs-lookup"><span data-stu-id="d9152-228">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="d9152-229">Reproduzieren Sie den Vorgang, für den eine Problembehandlung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d9152-229">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="d9152-230">Beenden Sie die Ablaufverfolgungssitzung:</span><span class="sxs-lookup"><span data-stu-id="d9152-230">Terminate the tracing session:</span></span>

    <span data-ttu-id="d9152-231">**tracelog.exe -stop w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="d9152-231">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="d9152-232">Löschen Sie den Registrierungsschlüssel **HKEY \_ LOCAL \_ MACHINE** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **adsi** \\ **Tracing** \\ **w3wp.exe**.</span><span class="sxs-lookup"><span data-stu-id="d9152-232">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="d9152-233">Führen Sie das ETW-Tool tracerpt.exe aus, um die Ablaufverfolgungsinformationen aus dem Protokoll zu analysieren:</span><span class="sxs-lookup"><span data-stu-id="d9152-233">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="d9152-234">**tracerpt.exe . \\ w3wp.etl -o -report**</span><span class="sxs-lookup"><span data-stu-id="d9152-234">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 

