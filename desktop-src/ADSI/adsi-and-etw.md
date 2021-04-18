---
title: Ereignis Ablauf Verfolgung in ADSI
description: Windows Server 2008 und Windows Vista stellen die Ereignis Ablauf Verfolgung in Active Directory Service Interfaces (ADSI) vor.
ms.assetid: 743aeeba-5b48-47c7-aaf5-0e9b48e206db
ms.tgt_platform: multiple
keywords:
- Ereignis Ablauf Verfolgung ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f43c0d840cd1f3f70d293a0a4f5c299fd129efe
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "106340734"
---
# <a name="event-tracing-in-adsi"></a><span data-ttu-id="5f3ac-104">Ereignis Ablauf Verfolgung in ADSI</span><span class="sxs-lookup"><span data-stu-id="5f3ac-104">Event Tracing in ADSI</span></span>

<span data-ttu-id="5f3ac-105">Windows Server 2008 und Windows Vista stellen die [Ereignis Ablauf Verfolgung](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI) vor.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-105">Windows Server 2008 and Windows Vista introduce [Event Tracing](/windows/desktop/ETW/event-tracing-portal) in [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md) (ADSI).</span></span> <span data-ttu-id="5f3ac-106">Bestimmte Bereiche des ADSI LDAP-Anbieters haben eine zugrunde liegende Implementierung, die komplex ist oder eine Abfolge von Schritten umfasst, die das Diagnostizieren von Problemen erschwert.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-106">Certain areas of the ADSI LDAP Provider have an underlying implementation that is complex or that involves a sequence of steps that makes it difficult to diagnose problems.</span></span> <span data-ttu-id="5f3ac-107">Zur Unterstützung der Problembehandlung für Anwendungsentwickler wurde die Ereignis Ablauf Verfolgung den folgenden Bereichen hinzugefügt:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-107">To help application developers troubleshoot, Event Tracing has been added to the following areas:</span></span>

## <a name="schema-parsing-and-downloading"></a><span data-ttu-id="5f3ac-108">Schema-und Download</span><span class="sxs-lookup"><span data-stu-id="5f3ac-108">Schema Parsing and Downloading</span></span>

<span data-ttu-id="5f3ac-109">Die IADs-Schnittstelle in ADSI erfordert, dass das LDAP-Schema auf dem Client zwischengespeichert wird, damit Attribute ordnungsgemäß gemarshallt werden können (wie im [ADSI-Schema Modell](adsi-schema-model.md)beschrieben).</span><span class="sxs-lookup"><span data-stu-id="5f3ac-109">The IADs interface in ADSI requires that the LDAP schema be cached on the client so that attributes can be marshaled correctly (as described in the [ADSI Schema Model](adsi-schema-model.md)).</span></span> <span data-ttu-id="5f3ac-110">Um dies zu erreichen, lädt ADSI das Schema für jeden Prozess (und für jeden LDAP-Server/jede LDAP-Domäne) entweder aus einer Schema Datei (. sch), die auf dem lokalen Datenträger gespeichert ist, oder durch Herunterladen vom LDAP-Server in den Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-110">To achieve this, ADSI loads the schema for each process (and for each LDAP server/domain) into memory either from a schema (.sch) file that is saved on the local disk or by downloading it from the LDAP server.</span></span> <span data-ttu-id="5f3ac-111">Bei verschiedenen Prozessen auf dem gleichen Client Computer wird das zwischengespeicherte Schema auf dem Datenträger verwendet, wenn es verfügbar und anwendbar ist.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-111">Different processes on the same client machine use the cached schema on disk if it is available and applicable.</span></span>

<span data-ttu-id="5f3ac-112">Wenn das Schema nicht vom Datenträger oder vom Server abgerufen werden kann, verwendet ADSI ein hart codiertes Standardschema.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-112">If the schema cannot be obtained from the disk or the server, ADSI uses a hardcoded default schema.</span></span> <span data-ttu-id="5f3ac-113">In diesem Fall können Attribute, die nicht Teil dieses Standard Schemas sind, nicht gemarshallt werden, und ADSI gibt beim Abrufen dieser Attribute einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-113">When this occurs, attributes that are not part of this default schema cannot be marshaled and ADSI returns an error while retrieving these attributes.</span></span> <span data-ttu-id="5f3ac-114">Dies kann zu einer Reihe von Faktoren führen, einschließlich Problemen bei der Paket Ausführung und unzureichender Berechtigungen zum Herunterladen des Schemas.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-114">A number of factors could cause this to happen, including problems in parsing the schema, and insufficient privileges to download the schema.</span></span> <span data-ttu-id="5f3ac-115">Es ist oft schwierig zu bestimmen, warum ein bestimmtes Standardschema verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-115">It is often difficult to determine why a certain default schema is being used.</span></span> <span data-ttu-id="5f3ac-116">Die Verwendung der Ereignis Ablauf Verfolgung in diesem Bereich hilft, das Problem schneller zu diagnostizieren und zu beheben.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-116">Using Event Tracing in this area will help to more quickly diagnose the problem and fix it.</span></span>

## <a name="changing-and-setting-the-password"></a><span data-ttu-id="5f3ac-117">Ändern und Festlegen des Kennworts</span><span class="sxs-lookup"><span data-stu-id="5f3ac-117">Changing and Setting the Password</span></span>

<span data-ttu-id="5f3ac-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) und [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) verwenden mehr als einen Mechanismus, um den angeforderten Vorgang basierend auf der verfügbaren Konfiguration auszuführen (wie unter [festlegen und Ändern von Benutzer Kennwörtern mit dem LDAP-Anbieter](setting-user-passwords-for-ldap-providers.md)beschrieben).</span><span class="sxs-lookup"><span data-stu-id="5f3ac-118">[**ChangePassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-changepassword) and [**SetPassword**](/windows/desktop/api/Iads/nf-iads-iadsuser-setpassword) employ more than one mechanism to perform the requested operation based on the available configuration (as described in [Setting and Changing User Passwords with the LDAP Provider](setting-user-passwords-for-ldap-providers.md)).</span></span> <span data-ttu-id="5f3ac-119">Wenn **ChangePassword** und **SetPassword** ausfallen, kann es schwierig sein, genau zu bestimmen, warum und die Ereignis Ablauf Verfolgung bei der Behebung von Problemen mit diesen Methoden hilfreich ist.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-119">When **ChangePassword** and **SetPassword** fail, it can be difficult to determine exactly why, and Event Tracing will help to troubleshoot problems with these methods.</span></span>

## <a name="adsi-bind-cache"></a><span data-ttu-id="5f3ac-120">ADSI-Bindungs Cache</span><span class="sxs-lookup"><span data-stu-id="5f3ac-120">ADSI Bind Cache</span></span>

<span data-ttu-id="5f3ac-121">ADSI versucht nach Möglichkeit intern, LDAP-Verbindungen wiederzuverwenden (siehe [Verbindungs Caching](connection-caching.md)).</span><span class="sxs-lookup"><span data-stu-id="5f3ac-121">ADSI internally tries to reuse LDAP connections whenever possible (see [Connection Caching](connection-caching.md)).</span></span> <span data-ttu-id="5f3ac-122">Bei der Problembehandlung ist es sinnvoll, zu verfolgen, ob eine neue Verbindung für die Kommunikation mit dem Server geöffnet wurde oder ob eine vorhandene Verbindung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-122">When troubleshooting, it is useful to trace whether a new connection was opened for communication with the server or whether an existing connection was used.</span></span> <span data-ttu-id="5f3ac-123">Dies kann auch hilfreich sein, um den Lebenszyklus des Verbindungs Caches (auch als Bindungs Cache bezeichnet) und die Erstellung oder Schließung zu verfolgen, und ob ein Verbindungs Verweis stattfindet.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-123">It can also be useful to trace the lifecycle of the connection cache (sometimes referred to as the bind cache) and its creation or closure, and whether a connection referral took place.</span></span> <span data-ttu-id="5f3ac-124">Bei einer Server [losen Bindung](/windows/desktop/AD/serverless-binding-and-rootdse)ruft ADSI den DC-Serverlocatorpunkt auf, um einen Server für die Domäne des Benutzer Kontexts auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-124">In the case of a [serverless bind](/windows/desktop/AD/serverless-binding-and-rootdse), ADSI calls the DC locator to select a server for the domain of the user's context.</span></span> <span data-ttu-id="5f3ac-125">ADSI verwaltet dann einen Cache der Domänen Server Zuordnung für nachfolgende Verbindungen.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-125">ADSI then maintains a cache of the domain-server mapping for subsequent connections.</span></span> <span data-ttu-id="5f3ac-126">Die Ereignis Ablauf Verfolgung hilft bei der Nachverfolgung der Auswahl des Domänen Controllers und ist daher bei der Behandlung von Verbindungs bezogenen Problemen hilfreich.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-126">Event Tracing helps to trace the selection of the DC, and is therefore helpful in troubleshooting connection-related issues.</span></span>

## <a name="enabling-tracing-and-starting-a-tracing-session"></a><span data-ttu-id="5f3ac-127">Aktivieren der Ablauf Verfolgung und Starten einer Ablauf Verfolgungs Sitzung</span><span class="sxs-lookup"><span data-stu-id="5f3ac-127">Enabling Tracing and Starting a Tracing Session</span></span>

<span data-ttu-id="5f3ac-128">Um die ADSI-Ablauf Verfolgung zu aktivieren, erstellen Sie den folgenden Registrierungsschlüssel:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-128">To turn on ADSI tracing, create the following registry key:</span></span>

<span data-ttu-id="5f3ac-129">**HKEY \_ Lokales \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ ***ProcessName***</span><span class="sxs-lookup"><span data-stu-id="5f3ac-129">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\***ProcessName***</span></span>

<span data-ttu-id="5f3ac-130">*ProcessName* ist der vollständige Name des Prozesses, den Sie verfolgen möchten, einschließlich seiner Erweiterung (z. b. "Svchost.exe").</span><span class="sxs-lookup"><span data-stu-id="5f3ac-130">*ProcessName* is the full name of the process that you want to trace, including its extension (for example, "Svchost.exe").</span></span> <span data-ttu-id="5f3ac-131">Außerdem können Sie in diesem Schlüssel einen optionalen Wert des Typs **DWORD** mit dem Namen PID platzieren.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-131">In addition, you can place an optional value of type **DWORD** named PID in this key.</span></span> <span data-ttu-id="5f3ac-132">Es wird dringend empfohlen, diesen Wert festzulegen und damit nur einen bestimmten Prozess nachzuverfolgen.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-132">It is highly recommended that you set this value and thereby trace only a particular process.</span></span> <span data-ttu-id="5f3ac-133">Andernfalls werden alle Instanzen der Anwendung, die von *ProcessName* angegeben werden, nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-133">Otherwise, all instances of the application specified by *ProcessName* will be traced.</span></span>

<span data-ttu-id="5f3ac-134">Führen Sie dann den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-134">Then execute the following command:</span></span>

<span data-ttu-id="5f3ac-135">**tracelog.exe-Start** *Sessionname*  \* *-GUID \# \* \* \* Anbieter \_ GUID* **-f** *Dateiname* **-Flag** *TraceFlags* **-Level** *TraceLevel*</span><span class="sxs-lookup"><span data-stu-id="5f3ac-135">**tracelog.exe -start** *sessionname* \**-guid \#\*\*\*provider\_guid* **-f** *filename* **-flag** *traceFlags* **-level** *traceLevel*</span></span>

<span data-ttu-id="5f3ac-136">*Sessionname* ist einfach ein beliebiger Bezeichner, der zum bezeichnen der Ablauf Verfolgungs Sitzung verwendet wird (Sie müssen später auf diesen Sitzungs Namen verweisen, wenn Sie die Ablauf Verfolgungs Sitzung beenden).</span><span class="sxs-lookup"><span data-stu-id="5f3ac-136">*sessionname* is simply an arbitrary identifier that is used to label the tracing session (you will need to refer to this session name later when you stop the tracing session).</span></span> <span data-ttu-id="5f3ac-137">Die GUID für den ADSI-Überwachungs Anbieter lautet "7288c9f8-d63c-4932-A345-89d6b060174d".</span><span class="sxs-lookup"><span data-stu-id="5f3ac-137">The GUID for the ADSI tracking provider is "7288c9f8-d63c-4932-a345-89d6b060174d".</span></span> <span data-ttu-id="5f3ac-138">*filename* gibt die Protokolldatei an, in die Ereignisse geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-138">*filename* specifies the logfile to which events will be written.</span></span> <span data-ttu-id="5f3ac-139">*TraceFlags* muss einer der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-139">*traceFlags* should be one of the following values:</span></span>



|                                 |                       |
|---------------------------------|-----------------------|
| <span data-ttu-id="5f3ac-140">**Debug- \_ Schema**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-140">**DEBUG\_SCHEMA**</span></span><br/>    | <span data-ttu-id="5f3ac-141">0x00000001</span><span class="sxs-lookup"><span data-stu-id="5f3ac-141">0x00000001</span></span><br/> |
| <span data-ttu-id="5f3ac-142">**\_CHANGEPWD Debuggen**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-142">**DEBUG\_CHANGEPWD**</span></span><br/> | <span data-ttu-id="5f3ac-143">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5f3ac-143">0x00000002</span></span><br/> |
| <span data-ttu-id="5f3ac-144">**Debuggen von \_ SetPwd**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-144">**DEBUG\_SETPWD**</span></span><br/>    | <span data-ttu-id="5f3ac-145">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5f3ac-145">0x00000004</span></span><br/> |
| <span data-ttu-id="5f3ac-146">**bindcache Debuggen \_**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-146">**DEBUG\_BINDCACHE**</span></span><br/> | <span data-ttu-id="5f3ac-147">0x00000008</span><span class="sxs-lookup"><span data-stu-id="5f3ac-147">0x00000008</span></span><br/> |



 

<span data-ttu-id="5f3ac-148">Diese Flags bestimmen, welche [ADSI](active-directory-service-interfaces-adsi.md) -Methoden gemäß der folgenden Tabelle verfolgt werden:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-148">These flags determine which [ADSI](active-directory-service-interfaces-adsi.md) methods will be traced, according to the following table:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5f3ac-149"><strong>DEBUG_SCHEMA</strong></span><span class="sxs-lookup"><span data-stu-id="5f3ac-149"><strong>DEBUG_SCHEMA</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="5f3ac-150">Ldapgetschema</span><span class="sxs-lookup"><span data-stu-id="5f3ac-150">LdapGetSchema</span></span></li>
<li><span data-ttu-id="5f3ac-151">Getschemainfotime</span><span class="sxs-lookup"><span data-stu-id="5f3ac-151">GetSchemaInfoTime</span></span></li>
<li><span data-ttu-id="5f3ac-152">Ldapreadschemainfofromserver</span><span class="sxs-lookup"><span data-stu-id="5f3ac-152">LdapReadSchemaInfoFromServer</span></span></li>
<li><span data-ttu-id="5f3ac-153">Processschemainfo</span><span class="sxs-lookup"><span data-stu-id="5f3ac-153">ProcessSchemaInfo</span></span></li>
<li><span data-ttu-id="5f3ac-154">Helperlesldapschemainfo</span><span class="sxs-lookup"><span data-stu-id="5f3ac-154">HelperReadLdapSchemaInfo</span></span></li>
<li><span data-ttu-id="5f3ac-155">Processclassinfoarray</span><span class="sxs-lookup"><span data-stu-id="5f3ac-155">ProcessClassInfoArray</span></span></li>
<li><span data-ttu-id="5f3ac-156">"Read schemainfofromregistry"</span><span class="sxs-lookup"><span data-stu-id="5f3ac-156">ReadSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="5f3ac-157">Storeschemainfofromregistry</span><span class="sxs-lookup"><span data-stu-id="5f3ac-157">StoreSchemaInfoFromRegistry</span></span></li>
<li><span data-ttu-id="5f3ac-158">Attributetypedescription</span><span class="sxs-lookup"><span data-stu-id="5f3ac-158">AttributeTypeDescription</span></span></li>
<li><span data-ttu-id="5f3ac-159">Objectclassdescription</span><span class="sxs-lookup"><span data-stu-id="5f3ac-159">ObjectClassDescription</span></span></li>
<li><span data-ttu-id="5f3ac-160">Ditcontentruledescription</span><span class="sxs-lookup"><span data-stu-id="5f3ac-160">DITContentRuleDescription</span></span></li>
<li><span data-ttu-id="5f3ac-161">Directoriystring</span><span class="sxs-lookup"><span data-stu-id="5f3ac-161">DirectoryString</span></span></li>
<li><span data-ttu-id="5f3ac-162">Directoriystrings</span><span class="sxs-lookup"><span data-stu-id="5f3ac-162">DirectoryStrings</span></span></li>
<li><span data-ttu-id="5f3ac-163">Ditcontentruledescription</span><span class="sxs-lookup"><span data-stu-id="5f3ac-163">DITContentRuleDescription</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f3ac-164"><strong>DEBUG_CHANGEPWD</strong></span><span class="sxs-lookup"><span data-stu-id="5f3ac-164"><strong>DEBUG_CHANGEPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="5f3ac-165">Cadsuser:: ChangePassword</span><span class="sxs-lookup"><span data-stu-id="5f3ac-165">CADsUser::ChangePassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5f3ac-166"><strong>DEBUG_SETPWD</strong></span><span class="sxs-lookup"><span data-stu-id="5f3ac-166"><strong>DEBUG_SETPWD</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="5f3ac-167">Cadsuser:: SetPassword</span><span class="sxs-lookup"><span data-stu-id="5f3ac-167">CADsUser::SetPassword</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5f3ac-168"><strong>DEBUG_BINDCACHE</strong></span><span class="sxs-lookup"><span data-stu-id="5f3ac-168"><strong>DEBUG_BINDCACHE</strong></span></span><br/></td>
<td><ul>
<li><span data-ttu-id="5f3ac-169">Getserverbasedobject</span><span class="sxs-lookup"><span data-stu-id="5f3ac-169">GetServerBasedObject</span></span></li>
<li><span data-ttu-id="5f3ac-170">Getserverlessbasedobject</span><span class="sxs-lookup"><span data-stu-id="5f3ac-170">GetServerLessBasedObject</span></span></li>
<li><span data-ttu-id="5f3ac-171">Getgcdomainname</span><span class="sxs-lookup"><span data-stu-id="5f3ac-171">GetGCDomainName</span></span></li>
<li><span data-ttu-id="5f3ac-172">GetDefaultDomain Name</span><span class="sxs-lookup"><span data-stu-id="5f3ac-172">GetDefaultDomainName</span></span></li>
<li><span data-ttu-id="5f3ac-173">Getuserdomainflatname</span><span class="sxs-lookup"><span data-stu-id="5f3ac-173">GetUserDomainFlatName</span></span></li>
<li><span data-ttu-id="5f3ac-174">Bindcachelookup</span><span class="sxs-lookup"><span data-stu-id="5f3ac-174">BindCacheLookup</span></span></li>
<li><span data-ttu-id="5f3ac-175">Equivalentportnumbers</span><span class="sxs-lookup"><span data-stu-id="5f3ac-175">EquivalentPortNumbers</span></span></li>
<li><span data-ttu-id="5f3ac-176">Cankredentialsbereused</span><span class="sxs-lookup"><span data-stu-id="5f3ac-176">CanCredentialsBeReused</span></span></li>
<li><span data-ttu-id="5f3ac-177">Bindcacheadd</span><span class="sxs-lookup"><span data-stu-id="5f3ac-177">BindCacheAdd</span></span></li>
<li><span data-ttu-id="5f3ac-178">Bindcacheadressf</span><span class="sxs-lookup"><span data-stu-id="5f3ac-178">BindCacheAddRef</span></span></li>
<li><span data-ttu-id="5f3ac-179">Adressferrallink</span><span class="sxs-lookup"><span data-stu-id="5f3ac-179">AddReferralLink</span></span></li>
<li><span data-ttu-id="5f3ac-180">Commonremoveentry</span><span class="sxs-lookup"><span data-stu-id="5f3ac-180">CommonRemoveEntry</span></span></li>
<li><span data-ttu-id="5f3ac-181">Bindcachederefhelper</span><span class="sxs-lookup"><span data-stu-id="5f3ac-181">BindCacheDerefHelper</span></span></li>
<li><span data-ttu-id="5f3ac-182">NotifyNewConnection</span><span class="sxs-lookup"><span data-stu-id="5f3ac-182">NotifyNewConnection</span></span></li>
<li><span data-ttu-id="5f3ac-183">QueryForConnection</span><span class="sxs-lookup"><span data-stu-id="5f3ac-183">QueryForConnection</span></span></li>
<li><span data-ttu-id="5f3ac-184">Ldapoprebindwithanmelde Informationen</span><span class="sxs-lookup"><span data-stu-id="5f3ac-184">LdapOpenBindWithCredentials</span></span></li>
<li><span data-ttu-id="5f3ac-185">Ldapoprebindwithdefaultanmeldeinformationen</span><span class="sxs-lookup"><span data-stu-id="5f3ac-185">LdapOpenBindWithDefaultCredentials</span></span></li>
</ul>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="5f3ac-186">Sie können Flags kombinieren, indem Sie die entsprechenden Bits im *TraceFlags* -Argument kombinieren.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-186">You can combine flags by combining the appropriate bits in the *traceFlags* argument.</span></span> <span data-ttu-id="5f3ac-187">Um z. b. das **Debug- \_ Schema** und das **Debug- \_ bindcache** -Flags anzugeben, wäre der geeignete *TraceFlags* -Wert 0x00000009.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-187">For example, to specify the **DEBUG\_SCHEMA** and **DEBUG\_BINDCACHE** flags, the appropriate *traceFlags* value would be 0x00000009.</span></span>

<span data-ttu-id="5f3ac-188">Schließlich sollte das *TraceLevel* -Flag einen der folgenden Werte aufweisen:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-188">Finally, the *traceLevel* flag should be one of the following values:</span></span>



|                                          |                       |
|------------------------------------------|-----------------------|
| <span data-ttu-id="5f3ac-189">**Fehler auf Ablauf Verfolgungs \_ Ebene \_**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-189">**TRACE\_LEVEL\_ERROR**</span></span><br/>       | <span data-ttu-id="5f3ac-190">0x00000002</span><span class="sxs-lookup"><span data-stu-id="5f3ac-190">0x00000002</span></span><br/> |
| <span data-ttu-id="5f3ac-191">**Informationen der Ablauf Verfolgungs \_ Ebene \_**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-191">**TRACE\_LEVEL\_INFORMATION**</span></span><br/> | <span data-ttu-id="5f3ac-192">0x00000004</span><span class="sxs-lookup"><span data-stu-id="5f3ac-192">0x00000004</span></span><br/> |



 

<span data-ttu-id="5f3ac-193">Ablauf **Verfolgung \_ Die Ebene der \_ Informationen** bewirkt, dass der Ablauf Verfolgungs Prozess alle Ereignisse zeichnet, wohingegen der Ablauf Verfolgungs Prozess bewirkt, dass der Ablauf Verfolgungs Prozess nur Fehlerereignisse erfasst. **\_ \_**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-193">**TRACE\_LEVEL\_INFORMATION** causes the tracing process to record all events, whereas **TRACE\_LEVEL\_ERROR** causes the tracing process to record only error events.</span></span>

<span data-ttu-id="5f3ac-194">Führen Sie den folgenden Befehl aus, um die Ablauf Verfolgung zu beenden:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-194">To terminate tracing, run the following command:</span></span>

<span data-ttu-id="5f3ac-195">**tracelog.exe-** " *Sessionname* " wird beendet.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-195">**tracelog.exe -stop** *sessionname*</span></span>

<span data-ttu-id="5f3ac-196">Im vorherigen Beispiel ist *Sessionname* derselbe Name wie der, der mit dem Befehl bereitgestellt wurde, der den Abschnitt Ablauf Verfolgung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-196">In the previous example, *sessionname* is the same name as the one that was provided with the command that started the tracing section.</span></span>

## <a name="remarks"></a><span data-ttu-id="5f3ac-197">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5f3ac-197">Remarks</span></span>

<span data-ttu-id="5f3ac-198">Es ist effektiver, nur bestimmte Prozesse zu verfolgen, indem eine bestimmte PID angegeben wird, als alle Prozesse auf einem Computer zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-198">It is more effective to trace only specific processes by specifying a particular PID than to trace all processes on a computer.</span></span> <span data-ttu-id="5f3ac-199">Wenn Sie mehrere Anwendungen auf demselben Computer verfolgen müssen, wirkt sich dies möglicherweise auf die Leistung aus. Es gibt eine beträchtliche Debugausgabe in leistungsorientierten Abschnitten des Codes.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-199">If you do need to trace multiple applications on the same machine, there might be a performance impact; there is substantial debugging output in performance-oriented sections of the code.</span></span> <span data-ttu-id="5f3ac-200">Außerdem müssen Administratoren darauf achten, die Berechtigungen der Protokolldateien ordnungsgemäß festzulegen, wenn Sie mehrere Prozesse verfolgen. Andernfalls können alle Benutzer die Ablauf Verfolgungs Protokolle lesen, und andere Benutzer können Prozesse nachverfolgen, die sichere Informationen enthalten.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-200">Also, administrators must be careful to properly set the permissions of the log files when tracing multiple processes; otherwise, any user might be able to read the tracing logs, and other users will be able to trace processes that contain secure information.</span></span>

<span data-ttu-id="5f3ac-201">Nehmen Sie beispielsweise an, dass der Administrator die Ablauf Verfolgung für eine Anwendung "Test.exe" einrichtet und keine PID in der Registrierung angibt, um mehrere Instanzen des Prozesses zu verfolgen.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-201">For example, presume the administrator sets up tracing for an application "Test.exe", and does not specify a PID in the registry to trace multiple instances of the process.</span></span> <span data-ttu-id="5f3ac-202">Jetzt möchte ein anderer Benutzer die Anwendung "Secure.exe" verfolgen.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-202">Now another user wants to trace the application "Secure.exe".</span></span> <span data-ttu-id="5f3ac-203">Wenn die Ablauf Verfolgungs Protokolldateien nicht ordnungsgemäß eingeschränkt sind, muss der Benutzer nur "Secure.exe" in "Test.exe" umbenennen, und er wird nachverfolgt.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-203">If the tracing log files are not properly restricted, all that user needs to do is rename "Secure.exe" to "Test.exe", and it will be traced.</span></span> <span data-ttu-id="5f3ac-204">Im Allgemeinen ist es am besten, bei der Problembehandlung nur bestimmte Prozesse zu verfolgen und den Registrierungsschlüssel für die Ablauf Verfolgung zu entfernen, sobald die Problembehandlung erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-204">In general, it is best to trace only specific processes while troubleshooting, and to remove the tracing registry key as soon as troubleshooting is done.</span></span>

<span data-ttu-id="5f3ac-205">Da durch Aktivieren der Ereignis Ablauf Verfolgung zusätzliche Protokolldateien erzeugt werden, sollten Administratoren die Protokolldatei Größen sorgfältig überwachen. fehlender Speicherplatz auf dem lokalen Computer kann zu einem Denial-of-Service-Angriff führen.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-205">Since enabling Event Tracing will produce extra log files, administrators should carefully monitor log file sizes; lack of disk space on the local computer can cause a denial-of-service.</span></span>

## <a name="example-scenarios"></a><span data-ttu-id="5f3ac-206">Beispielszenarien</span><span class="sxs-lookup"><span data-stu-id="5f3ac-206">Example Scenarios</span></span>

<span data-ttu-id="5f3ac-207">Szenario 1: dem Administrator wird ein unerwarteter Fehler in einer Anwendung angezeigt, mit der Kenn Wörter für Benutzerkonten festgelegt werden, sodass die folgenden Schritte ausgeführt werden, um das Problem mithilfe der Ereignis Ablauf Verfolgung zu beheben.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-207">Scenario 1: The administrator sees an unexpected error in an application that sets passwords for user accounts, so they would take the following steps to fix the problem using Event Tracing.</span></span>

1.  <span data-ttu-id="5f3ac-208">Schreiben Sie ein Skript, das das Problem erneut erzeugt, und erstellen Sie den Registrierungsschlüssel.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-208">Write a script that reproduces the problem, and create the registry key</span></span>

    <span data-ttu-id="5f3ac-209">**HKEY \_ System für lokale \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-209">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

2.  <span data-ttu-id="5f3ac-210">Starten Sie eine Ablauf Verfolgungs Sitzung, und legen Sie *TraceFlags* auf 0x2 (**Debug \_ changepasswd**) und *TraceLevel* auf 0x4 (**\_ \_ Informationen** der Ablauf Verfolgungs Ebene) fest, indem Sie den folgenden Befehl verwenden:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-210">Start a tracing session, setting *traceFlags* to 0x2 (**DEBUG\_CHANGEPASSWD**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**), using the following command:</span></span>

    <span data-ttu-id="5f3ac-211">**tracelog.exe-Start scripttrace-GUID \# 7288c9o8-d63c-4932-A345-89d6b060174d-f. \\ ADSI. ETL-Flag 0x2-Ebene 0x4**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-211">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

3.  <span data-ttu-id="5f3ac-212">Führen Sie cscript.exe mit dem zugehörigen Testskript aus, um das Problem zu reproduzieren, und beenden Sie dann die Ablauf Verfolgungs Sitzung:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-212">Run cscript.exe with their test script to reproduce the problem, and then terminate the tracing session:</span></span>

    <span data-ttu-id="5f3ac-213">**Abbrechen von scripttracetracelog.exe**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-213">**tracelog.exe -stop scripttrace**</span></span>

4.  <span data-ttu-id="5f3ac-214">Registrierungsschlüssel löschen</span><span class="sxs-lookup"><span data-stu-id="5f3ac-214">Delete the registry key</span></span>

    <span data-ttu-id="5f3ac-215">**HKEY \_ System für lokale \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **cscript.exe**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-215">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**cscript.exe**</span></span>

5.  <span data-ttu-id="5f3ac-216">Führen Sie das ETW-Tool Tracerpt.exe aus, um die Ablauf Verfolgungs Informationen aus dem Protokoll zu analysieren:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-216">Run the ETW tool Tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="5f3ac-217">**tracelog.exe-Start scripttrace-GUID \# 7288c9o8-d63c-4932-A345-89d6b060174d-f. \\ ADSI. ETL-Flag 0x2-Ebene 0x4**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-217">**tracelog.exe -start scripttrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\adsi.etl -flag 0x2 -level 0x4**</span></span>

<span data-ttu-id="5f3ac-218">Szenario 2: der Administrator möchte die Schema Analyse-und Download Vorgänge in einer [ASP](https://msdn.microsoft.com/asp.net/default.aspx) -Anwendung mit dem Namen w3wp.exe verfolgen, die bereits ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-218">Scenario 2: The administrator wants to trace the schema parsing and download operations in an [ASP](https://msdn.microsoft.com/asp.net/default.aspx) application named w3wp.exe that is already running.</span></span> <span data-ttu-id="5f3ac-219">Hierzu führt der Administrator die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-219">To do this, the administrator would take the following steps:</span></span>

1.  <span data-ttu-id="5f3ac-220">Registrierungsschlüssel erstellen</span><span class="sxs-lookup"><span data-stu-id="5f3ac-220">Create the registry key</span></span>

    <span data-ttu-id="5f3ac-221">**HKEY \_ System für lokale \_ Computer** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **w3wp.exe**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-221">**HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**</span></span>

    <span data-ttu-id="5f3ac-222">Erstellen Sie in diesem Schlüssel einen Wert vom Typ DWORD, der den Namen PID hat, und legen Sie ihn auf die Prozess-ID der Instanz von w3wp.exe fest, die derzeit auf dem lokalen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-222">and inside that key, create a value of type DWORD that is named PID and set it to the process ID of the instance of w3wp.exe that is currently running on the local computer.</span></span>

2.  <span data-ttu-id="5f3ac-223">Anschließend erstellen Sie eine Ablauf Verfolgungs Sitzung, indem Sie *TraceFlags* auf 0x1 (**\_ debugschema**) und *TraceLevel* auf 0x4 (**\_ \_ Informationen** der Ablauf Verfolgungs Ebene) festlegen:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-223">Then they create a tracing session, setting *traceFlags* to 0x1 (**DEBUG\_SCHEMA**) and *traceLevel* to 0x4 (**TRACE\_LEVEL\_INFORMATION**):</span></span>

    <span data-ttu-id="5f3ac-224">**tracelog.exe-Start w3wptrace-GUID \# 7288c9o8-d63c-4932-A345-89d6b060174d-f. \\ w3wp. ETL-Flag 0x1-Ebene 0x4**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-224">**tracelog.exe -start w3wptrace -guid \#7288c9f8-d63c-4932-a345-89d6b060174d -f .\\w3wp.etl -flag 0x1 -level 0x4**</span></span>

3.  <span data-ttu-id="5f3ac-225">Reproduzieren Sie den Vorgang, der die Problembehandlung erfordert.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-225">Reproduce the operation that needs troubleshooting.</span></span>
4.  <span data-ttu-id="5f3ac-226">Beenden Sie die Ablauf Verfolgungs Sitzung:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-226">Terminate the tracing session:</span></span>

    <span data-ttu-id="5f3ac-227">**tracelog.exe w3wptrace**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-227">**tracelog.exe -stop w3wptrace**</span></span>

5.  <span data-ttu-id="5f3ac-228">Löschen Sie den Registrierungsschlüssel **HKEY \_ local \_ Machine** \\ **System** \\ **CurrentControlSet** \\ **Services** \\ **ADSI** \\ **Tracing** \\ **w3wp.exe**.</span><span class="sxs-lookup"><span data-stu-id="5f3ac-228">Delete the registry key **HKEY\_LOCAL\_MACHINE**\\**System**\\**CurrentControlSet**\\**Services**\\**adsi**\\**Tracing**\\**w3wp.exe**.</span></span>
6.  <span data-ttu-id="5f3ac-229">Führen Sie das ETW-Tool tracerpt.exe aus, um die Ablauf Verfolgungs Informationen aus dem Protokoll zu analysieren:</span><span class="sxs-lookup"><span data-stu-id="5f3ac-229">Run the ETW tool tracerpt.exe to parse the tracing information from the log:</span></span>

    <span data-ttu-id="5f3ac-230">**tracerpt.exe. \\ w3wp. ETL-o-Report**</span><span class="sxs-lookup"><span data-stu-id="5f3ac-230">**tracerpt.exe .\\w3wp.etl -o -report**</span></span>

 

