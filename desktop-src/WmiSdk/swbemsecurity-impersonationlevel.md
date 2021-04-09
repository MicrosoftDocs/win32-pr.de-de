---
description: Die Eigenschaft "Identitätswechsel Ebene" ist eine ganze Zahl, die die Ebene des com-Identitäts Wechsels definiert, die diesem Objekt zugewiesen ist.
ms.assetid: cf57620b-7827-4552-a969-d25e5eb13a89
ms.tgt_platform: multiple
title: Swap Security. Identitäts ationlevel-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity.ImpersonationLevel
- ISWbemSecurity.ImpersonationLevel
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: 3b996d5920aba91fddf880ee9ddf6bf8081fb39f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868743"
---
# <a name="swbemsecurityimpersonationlevel-property"></a><span data-ttu-id="1c963-103">Swap Security. Identitäts ationlevel-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="1c963-103">SWbemSecurity.ImpersonationLevel property</span></span>

<span data-ttu-id="1c963-104">Die Eigenschaft "Identitätswechsel **Ebene** " ist eine ganze Zahl, die die Ebene des com-Identitäts Wechsels definiert, die diesem Objekt zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="1c963-104">The **ImpersonationLevel** property is an integer that defines the COM impersonation level that is assigned to this object.</span></span> <span data-ttu-id="1c963-105">Mit dieser Einstellung wird festgelegt, ob Prozesse im Besitz von Windows-Verwaltungsinstrumentation (WMI) Ihre Sicherheits Anmelde Informationen erkennen oder verwenden können, wenn Sie Aufrufe an andere Prozesse ausführen.</span><span class="sxs-lookup"><span data-stu-id="1c963-105">This setting determines if processes owned by Windows Management Instrumentation (WMI) can detect or use your security credentials when making calls to other processes.</span></span> <span data-ttu-id="1c963-106">Weitere Informationen zu Identitätswechsel Ebenen finden Sie unter [Festlegen der \_ \_ Prozesssicherheit für Client Anwendungen](setting-client-application-process-security.md).</span><span class="sxs-lookup"><span data-stu-id="1c963-106">For more information about impersonation levels, see [Setting Client\_Application\_Process Security](setting-client-application-process-security.md).</span></span>

<span data-ttu-id="1c963-107">Wenn Sie die Identitätswechsel Ebene nicht speziell in einem Moniker oder durch Festlegen der Eigenschaft " **Swap Security. Identitäts ationlevel** " für ein Sicherungs fähiges Objekt festlegen, wird die standardmäßige Identitätswechsel Ebene von WMI auf den Wert festgelegt, der im [Standard Registrierungsschlüssel](setting-the-default-process-security-level-using-vbscript.md)der Identitätswechsel Ebene angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="1c963-107">If you do not set the impersonation level specifically in either a moniker, or by setting the **SWBemSecurity.ImpersonationLevel** property on a securable object, WMI sets the default impersonation level to the value specified in the [default impersonation level registry key](setting-the-default-process-security-level-using-vbscript.md).</span></span> <span data-ttu-id="1c963-108">Wenn diese Einstellung nicht ausreicht, wird Ihre Anforderung vom Anbieter nicht unterstützt, und der WMI-API-Aufrufe kann mit dem Fehlercode **wbemErrAccessDenied** (2147749891/0x80041003) fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="1c963-108">If this setting is not sufficient, the provider does not service your request, and the call to the WMI API can fail with an error code of **wbemErrAccessDenied** (2147749891/0x80041003).</span></span>

<span data-ttu-id="1c963-109">Eine Erläuterung dieser Syntax finden Sie unter [Dokument Konventionen für die Skript-API](document-conventions-for-the-scripting-api.md).</span><span class="sxs-lookup"><span data-stu-id="1c963-109">For an explanation of this syntax, see [Document Conventions for the Scripting API](document-conventions-for-the-scripting-api.md).</span></span>

<span data-ttu-id="1c963-110">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="1c963-110">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c963-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="1c963-111">Syntax</span></span>


```VB
SWbemSecurity.ImpersonationLevel As Integer
```



## <a name="property-value"></a><span data-ttu-id="1c963-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="1c963-112">Property value</span></span>

## <a name="remarks"></a><span data-ttu-id="1c963-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1c963-113">Remarks</span></span>

<span data-ttu-id="1c963-114">Als DCOM-Identitätswechsel Ebene kann diese Eigenschaft auf einen der folgenden Werte festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="1c963-114">As a DCOM impersonation level, this property can be set to one of the following values:</span></span>



| <span data-ttu-id="1c963-115">Wert</span><span class="sxs-lookup"><span data-stu-id="1c963-115">Value</span></span>           | <span data-ttu-id="1c963-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1c963-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |
|-----------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1c963-117">**Anonym**</span><span class="sxs-lookup"><span data-stu-id="1c963-117">**Anonymous**</span></span>   | <span data-ttu-id="1c963-118">Verbirgt die Anmeldeinformationen des Aufrufers.</span><span class="sxs-lookup"><span data-stu-id="1c963-118">Hides the credentials of the caller.</span></span> <span data-ttu-id="1c963-119">WMI unterstützt diese Identitätswechsel Ebene nicht. Wenn ein Skript "Identitätswechsel Ebene = anonym" angibt, führt WMI eine automatische Aktualisierung der Identitätswechsel Ebene durch, um zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1c963-119">WMI does not actually support this impersonation level; if a script specifies impersonationLevel=Anonymous, WMI will silently upgrade the impersonation level to Identify.</span></span> <span data-ttu-id="1c963-120">Dies ist jedoch in gewisser Weise eine bedeutungslose Übung, da Skripts, die die identifizebene verwenden, wahrscheinlich fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="1c963-120">This is in some ways a meaningless exercise, however, because scripts using the Identify level are likely to fail.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                               |
| <span data-ttu-id="1c963-121">**Identifizieren**</span><span class="sxs-lookup"><span data-stu-id="1c963-121">**Identify**</span></span>    | <span data-ttu-id="1c963-122">Ermöglicht es Objekten, die Anmelde Informationen des Aufrufers abzufragen.</span><span class="sxs-lookup"><span data-stu-id="1c963-122">Enables objects to query the credentials of the caller.</span></span> <span data-ttu-id="1c963-123">Skripts, die diese Identitätswechsel Ebene verwenden, schlagen wahrscheinlich fehl. in der Regel können Sie mit der Ebene "identifizieren" in der Regel keine Zugriffs Steuerungs Listen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1c963-123">Scripts using this impersonation level are likely to fail; the Identify level typically lets you do no more than check access control lists.</span></span> <span data-ttu-id="1c963-124">Skripts können nicht auf Remote Computern mit identifiziert werden.</span><span class="sxs-lookup"><span data-stu-id="1c963-124">You will not be able to run scripts against remote computers using Identify.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| <span data-ttu-id="1c963-125">**Impersonate**</span><span class="sxs-lookup"><span data-stu-id="1c963-125">**Impersonate**</span></span> | <span data-ttu-id="1c963-126">Ermöglicht es Objekten, die Anmelde Informationen des Aufrufers zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c963-126">Enables objects to use the credentials of the caller.</span></span> <span data-ttu-id="1c963-127">Es wird empfohlen, diese Identitätswechsel Ebene mit WMI-Skripts zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1c963-127">It is recommended that you use this impersonation level with WMI scripts.</span></span> <span data-ttu-id="1c963-128">Wenn Sie dies tun, verwendet das WMI-Skript Ihre Benutzer Anmelde Informationen. Dadurch können alle Aufgaben ausgeführt werden, die Sie ausführen können.</span><span class="sxs-lookup"><span data-stu-id="1c963-128">When you do so, the WMI script will use your user credentials; as a result, it will be able to perform any tasks that you are able to perform.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| <span data-ttu-id="1c963-129">**Delegat**</span><span class="sxs-lookup"><span data-stu-id="1c963-129">**Delegate**</span></span>    | <span data-ttu-id="1c963-130">Ermöglicht es Objekten, anderen Objekten die Verwendung der Anmelde Informationen des Aufrufers zu gestatten.</span><span class="sxs-lookup"><span data-stu-id="1c963-130">Enables objects to permit other objects to use the credentials of the caller.</span></span> <span data-ttu-id="1c963-131">Die Delegierung ermöglicht es einem Skript, Ihre Anmelde Informationen auf einem Remote Computer zu verwenden, und ermöglicht diesem Remote Computer dann die Verwendung Ihrer Anmelde Informationen auf einem anderen Remote Computer.</span><span class="sxs-lookup"><span data-stu-id="1c963-131">Delegation allows a script to use your credentials on a remote computer and then enables that remote computer to use your credentials on another remote computer.</span></span> <span data-ttu-id="1c963-132">Obwohl Sie diese Identitätswechsel Ebene innerhalb von WMI-Skripts verwenden können, sollten Sie dies nur bei Bedarf tun, da Sie ein Sicherheitsrisiko darstellen könnte.</span><span class="sxs-lookup"><span data-stu-id="1c963-132">While you can use this impersonation level within WMI scripts, you should do so only if necessary because it might pose a security risk.</span></span><br/> <span data-ttu-id="1c963-133">Die Identitätswechsel Ebene des Delegaten kann nur verwendet werden, wenn alle Benutzerkonten und Computer Konten, die an der Transaktion beteiligt sind, als vertrauenswürdig für die Delegierung in Active Directory gekennzeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="1c963-133">You cannot use the Delegate impersonation level unless all the user accounts and computer accounts involved in the transaction have all been marked as Trusted for delegation in Active Directory.</span></span> <span data-ttu-id="1c963-134">Dies trägt dazu bei, die Sicherheitsrisiken zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="1c963-134">This helps minimize the security risks.</span></span> <span data-ttu-id="1c963-135">Zwar können von einem Remote Computer Ihre Anmelde Informationen verwendet werden, dies ist jedoch nur möglich, wenn sowohl dieser als auch andere an der Transaktion beteiligte Computer für die Delegierung vertrauenswürdig sind.</span><span class="sxs-lookup"><span data-stu-id="1c963-135">Although a remote computer can use your credentials, it can do so only if both it and any other computers involved in the transaction are trusted for delegation.</span></span><br/> |



 

<span data-ttu-id="1c963-136">Wie bereits erwähnt, blendet der anonyme Identitätswechsel Ihre Anmelde Informationen aus und identifiziert das Remote Objekt, um Ihre Anmelde Informationen abzufragen, aber das Remote Objekt kann die Identität des Sicherheits Kontexts nicht annehmen.</span><span class="sxs-lookup"><span data-stu-id="1c963-136">As noted, Anonymous impersonation hides your credentials and Identify permits a remote object to query your credentials, but the remote object cannot impersonate your security context.</span></span> <span data-ttu-id="1c963-137">(Mit anderen Worten: Obwohl das Remote Objekt weiß, wer Sie sind, kann es nicht "vorgeben", Sie zu sein.) WMI-Skripts, die mit einer dieser beiden Einstellungen auf Remote Computer zugreifen, schlagen in der Regel fehl.</span><span class="sxs-lookup"><span data-stu-id="1c963-137">(In other words, although the remote object knows who you are, it cannot "pretend" to be you.) WMI scripts accessing remote computers using one of these two settings will generally fail.</span></span> <span data-ttu-id="1c963-138">Tatsächlich können die meisten Skripts, die auf dem lokalen Computer ausgeführt werden, mit einer dieser beiden Einstellungen auch fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="1c963-138">In fact, most scripts run on the local computer using one of these two settings will also fail.</span></span>

<span data-ttu-id="1c963-139">Durch den Identitätswechsel wird dem WMI-Remote Dienst ermöglicht, den angeforderten Vorgang mithilfe Ihres Sicherheits Kontexts auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1c963-139">Impersonate permits the remote WMI service to use your security context to perform the requested operation.</span></span> <span data-ttu-id="1c963-140">Eine Remote-WMI-Anforderung, die die Einstellung Identität verwenden verwendet, ist in der Regel erfolgreich, sofern Ihre Anmelde Informationen über ausreichende Berechtigungen verfügen, um den beabsichtigten Vorgang auszuführen</span><span class="sxs-lookup"><span data-stu-id="1c963-140">A remote WMI request that uses the Impersonate setting typically succeeds, provided your credentials have sufficient privileges to perform the intended operation.</span></span> <span data-ttu-id="1c963-141">Anders ausgedrückt: Sie können WMI nicht zum Ausführen einer Aktion (Remote oder anderweitig) verwenden, für die Sie keine Berechtigung außerhalb von WMI haben.</span><span class="sxs-lookup"><span data-stu-id="1c963-141">In other words, you cannot use WMI to perform an action (remotely or otherwise) that you do not have permission to perform outside WMI.</span></span>

<span data-ttu-id="1c963-142">Wenn Sie "Identitätswechsel Ebene" auf "delegieren" festlegen, kann der Remote-WMI-Dienst ihre Anmelde Informationen an andere Objekte übergeben und wird in der Regel als Sicherheitsrisiko eingestuft.</span><span class="sxs-lookup"><span data-stu-id="1c963-142">Setting impersonationLevel to Delegate permits the remote WMI service to pass your credentials on to other objects and is generally considered a security risk.</span></span>

<span data-ttu-id="1c963-143">Sie können die Identitätswechsel Ebene des Objekts " [**Swap Services**](swbemservices.md)", " [**errbewbject**](swbemobject.md)", " [**errbewbjectset**](swbemobjectset.md)", " [**errbewbjectpath**](swbemobjectpath.md)" und " [**taubemlocator**](swbemlocator.md) " festlegen, indem Sie die Eigenschaft "Identitätswechsel **Ebene** " auf den gewünschten Wert festlegen.</span><span class="sxs-lookup"><span data-stu-id="1c963-143">You can set the impersonation level of an [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), and [**SwbemLocator**](swbemlocator.md) object by setting the **ImpersonationLevel** property to the desired value.</span></span> <span data-ttu-id="1c963-144">Im folgenden Beispiel wird gezeigt, wie Sie die Identitätswechsel Ebene für ein " **errbemubject** "-Objekt festlegen:</span><span class="sxs-lookup"><span data-stu-id="1c963-144">The following example shows you how to set the impersonation level for an **SWbemObject** object:</span></span>


```VB
objinstance.Security_.ImpersonationLevel = _
    wbemImpersonationLevelImpersonate
```



<span data-ttu-id="1c963-145">Sie können auch Identitätswechsel Ebenen als Teil eines Monikers angeben.</span><span class="sxs-lookup"><span data-stu-id="1c963-145">You can also specify impersonation levels as part of a moniker.</span></span> <span data-ttu-id="1c963-146">Im folgenden Beispiel werden die Authentifizierungs Ebene und die Ebene des Identitäts Wechsels festgelegt, und eine Instanz des [**Win32- \_ Dienstanbieter**](/windows/desktop/CIMWin32Prov/win32-service)wird abgerufen.</span><span class="sxs-lookup"><span data-stu-id="1c963-146">The following example sets the authentication level and the impersonation level, and retrieves an instance of [**Win32\_Service**](/windows/desktop/CIMWin32Prov/win32-service).</span></span>


```VB
Set objinst = GetObject("WinMgmts:{impersonationLevel=impersonate,"& _
                         "authenticationLevel=pktPrivacy}"& _
                         "!root/cimv2:Win32_service='ALERTER'")
```



## <a name="requirements"></a><span data-ttu-id="1c963-147">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1c963-147">Requirements</span></span>



| <span data-ttu-id="1c963-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1c963-148">Requirement</span></span> | <span data-ttu-id="1c963-149">Wert</span><span class="sxs-lookup"><span data-stu-id="1c963-149">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1c963-150">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1c963-150">Minimum supported client</span></span><br/> | <span data-ttu-id="1c963-151">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1c963-151">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1c963-152">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1c963-152">Minimum supported server</span></span><br/> | <span data-ttu-id="1c963-153">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1c963-153">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1c963-154">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="1c963-154">Type library</span></span><br/>             | <dl> <span data-ttu-id="1c963-155"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="1c963-155"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="1c963-156">DLL</span><span class="sxs-lookup"><span data-stu-id="1c963-156">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1c963-157"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1c963-157"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="1c963-158">CLSID</span><span class="sxs-lookup"><span data-stu-id="1c963-158">CLSID</span></span><br/>                    | <span data-ttu-id="1c963-159">CLSID- \_ Swap-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="1c963-159">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="1c963-160">IID</span><span class="sxs-lookup"><span data-stu-id="1c963-160">IID</span></span><br/>                      | <span data-ttu-id="1c963-161">IID \_ iswbemsecurity</span><span class="sxs-lookup"><span data-stu-id="1c963-161">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="1c963-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c963-162">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c963-163">**Austausch Sicherheit**</span><span class="sxs-lookup"><span data-stu-id="1c963-163">**SWbemSecurity**</span></span>](swbemsecurity.md)
</dt> <dt>

[<span data-ttu-id="1c963-164">Festlegen der \_ Prozesssicherheit für Client Anwendungen \_</span><span class="sxs-lookup"><span data-stu-id="1c963-164">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="1c963-165">**Wbemimpersonationlevelenum**</span><span class="sxs-lookup"><span data-stu-id="1c963-165">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> </dl>

 

