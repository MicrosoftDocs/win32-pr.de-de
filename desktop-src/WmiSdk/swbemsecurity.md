---
description: Das Swap Security-Objekt ruft Sicherheitseinstellungen ab oder legt diese fest, z. b. Berechtigungen, com-Identitätswechsel und Authentifizierungs Stufen, die einem Objekt zugewiesen sind.
ms.assetid: 794587fa-5feb-455b-be28-ecfaa25625ad
ms.tgt_platform: multiple
title: Swap Security-Objekt (wbemdisp. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SWbemSecurity
- ISWbemSecurity
api_type:
- COM
api_location:
- Wbemdisp.dll
ms.openlocfilehash: da59c3b996a80384c133336503124141f0907f79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359985"
---
# <a name="swbemsecurity-object"></a><span data-ttu-id="c059d-103">Swap Security-Objekt</span><span class="sxs-lookup"><span data-stu-id="c059d-103">SWbemSecurity object</span></span>

<span data-ttu-id="c059d-104">Das **Swap Security** -Objekt ruft Sicherheitseinstellungen ab oder legt diese fest, z. b. Berechtigungen, com-Identitätswechsel und Authentifizierungs Stufen, die einem Objekt zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="c059d-104">The **SWbemSecurity** object gets or sets security settings, such as privileges, COM impersonations, and authentication levels assigned to an object.</span></span> <span data-ttu-id="c059d-105">Die Objekte " [**errbemlocator**](swbemlocator.md)", " [**Swap Services**](swbemservices.md)", " [**errbeapbject**](swbemobject.md)", " [**errbeapbjectset**](swbemobjectset.md)", " [**errbeapbjectpath**](swbemobjectpath.md)", " [**errbemlasterror**](swbemlasterror.md)" und " [**errbemeventsource**](swbemeventsource.md) " verfügen über eine **Sicherheits \_** Eigenschaft, die das Objekt " **Swap Security** " ist</span><span class="sxs-lookup"><span data-stu-id="c059d-105">The [**SWbemLocator**](swbemlocator.md), [**SWbemServices**](swbemservices.md), [**SWbemObject**](swbemobject.md), [**SWbemObjectSet**](swbemobjectset.md), [**SWbemObjectPath**](swbemobjectpath.md), [**SWbemLastError**](swbemlasterror.md), and [**SWbemEventSource**](swbemeventsource.md) objects have a **Security\_** property, which is the **SWbemSecurity** object.</span></span> <span data-ttu-id="c059d-106">Wenn Sie eine Instanz von abrufen oder das WMI-Sicherheitsprotokoll anzeigen, müssen Sie möglicherweise die Eigenschaften des **Sicherheits \_** Objekts festlegen.</span><span class="sxs-lookup"><span data-stu-id="c059d-106">When you retrieve an instance or view the WMI security log, you might need to set the properties of the **Security\_** object.</span></span>

<span data-ttu-id="c059d-107">Der VBScript-Befehl zum Erstellen von [Objekten](/previous-versions//xzysf6hc(v=vs.85)) kann das Sicherheits Objekt nicht erstellen.</span><span class="sxs-lookup"><span data-stu-id="c059d-107">The VBScript [CreateObject](/previous-versions//xzysf6hc(v=vs.85)) call cannot create the Security object.</span></span> <span data-ttu-id="c059d-108">Die Sicherheitseinstellungen in diesem Objekt identifizieren nicht die Authentifizierungs-, Identitäts-oder Berechtigungseinstellungen für eine Verbindung mit WMI oder die Sicherheit, die für den Proxy wirksam ist, wenn ein Objekt in einem asynchronen-Befehl an eine Senke übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="c059d-108">The security settings in this object do not identify the authentication, impersonation, or privilege settings on a connection to WMI, or the security in effect for the proxy when an object is delivered to a sink in an asynchronous call.</span></span> <span data-ttu-id="c059d-109">Weitere Informationen finden Sie unter Verwalten der [WMI-Sicherheit](maintaining-wmi-security.md).</span><span class="sxs-lookup"><span data-stu-id="c059d-109">For more information, see [Maintaining WMI Security](maintaining-wmi-security.md).</span></span>

## <a name="members"></a><span data-ttu-id="c059d-110">Member</span><span class="sxs-lookup"><span data-stu-id="c059d-110">Members</span></span>

<span data-ttu-id="c059d-111">Das **taubemsecurity** -Objekt verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="c059d-111">The **SWbemSecurity** object has these types of members:</span></span>

-   [<span data-ttu-id="c059d-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c059d-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c059d-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="c059d-113">Properties</span></span>

<span data-ttu-id="c059d-114">Das **Swap Security** -Objekt verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="c059d-114">The **SWbemSecurity** object has these properties.</span></span>



| <span data-ttu-id="c059d-115">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="c059d-115">Property</span></span>                                                                    | <span data-ttu-id="c059d-116">Zugriffstyp</span><span class="sxs-lookup"><span data-stu-id="c059d-116">Access type</span></span>           | <span data-ttu-id="c059d-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c059d-117">Description</span></span>                                                                                                                                                                                                                            |
|:----------------------------------------------------------------------------|:----------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c059d-118">**AuthenticationLevel**</span><span class="sxs-lookup"><span data-stu-id="c059d-118">**AuthenticationLevel**</span></span>](swbemsecurity-authenticationlevel.md)<br/> | <span data-ttu-id="c059d-119">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c059d-119">Read/write</span></span><br/> | <span data-ttu-id="c059d-120">Numerischer Wert, der die com-Authentifizierungs Ebene definiert, die diesem-Objekt zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c059d-120">Numeric value that defines the COM Authentication level that is assigned to this object.</span></span> <span data-ttu-id="c059d-121">Mit dieser Einstellung wird bestimmt, wie die von WMI gesendeten Informationen geschützt werden.</span><span class="sxs-lookup"><span data-stu-id="c059d-121">This setting determines how you protect information sent from WMI.</span></span><br/>                                                                 |
| [<span data-ttu-id="c059d-122">**ImpersonationLevel**</span><span class="sxs-lookup"><span data-stu-id="c059d-122">**ImpersonationLevel**</span></span>](swbemsecurity-impersonationlevel.md)<br/>   | <span data-ttu-id="c059d-123">Lesen/Schreiben</span><span class="sxs-lookup"><span data-stu-id="c059d-123">Read/write</span></span><br/> | <span data-ttu-id="c059d-124">Numerischer Wert, der die Ebene des com-Identitäts Wechsels definiert, die diesem-Objekt zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="c059d-124">Numeric value that defines the COM Impersonation level that is assigned to this object.</span></span> <span data-ttu-id="c059d-125">Mit dieser Einstellung wird festgelegt, ob von WMI gehörende Prozesse ihre Sicherheits Anmelde Informationen erkennen oder verwenden können, wenn Sie Aufrufe an andere Prozesse ausführen.</span><span class="sxs-lookup"><span data-stu-id="c059d-125">This setting determines if processes owned by WMI can detect or use your security credentials when making calls to other processes.</span></span><br/> |
| [<span data-ttu-id="c059d-126">**Rechte**</span><span class="sxs-lookup"><span data-stu-id="c059d-126">**Privileges**</span></span>](swbemsecurity-privileges.md)<br/>                   | <span data-ttu-id="c059d-127">Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="c059d-127">Read-only</span></span><br/>  | <span data-ttu-id="c059d-128">Ein " [**taubemprivilegeset**](swbemprivilegeset.md) "-Objekt, das Berechtigungen für dieses Objekt definiert.</span><span class="sxs-lookup"><span data-stu-id="c059d-128">An [**SWbemPrivilegeSet**](swbemprivilegeset.md) object that defines privileges for this object.</span></span> <span data-ttu-id="c059d-129">Weitere Informationen finden Sie unter [Ausführen mit speziellen Berechtigungen](/windows/desktop/SecBP/running-with-special-privileges).</span><span class="sxs-lookup"><span data-stu-id="c059d-129">For more information, see [Running with Special Privileges](/windows/desktop/SecBP/running-with-special-privileges).</span></span><br/>                    |



 

## <a name="requirements"></a><span data-ttu-id="c059d-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c059d-130">Requirements</span></span>



| <span data-ttu-id="c059d-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c059d-131">Requirement</span></span> | <span data-ttu-id="c059d-132">Wert</span><span class="sxs-lookup"><span data-stu-id="c059d-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c059d-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c059d-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c059d-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c059d-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c059d-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c059d-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c059d-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c059d-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c059d-137">Header</span><span class="sxs-lookup"><span data-stu-id="c059d-137">Header</span></span><br/>                   | <dl> <span data-ttu-id="c059d-138"><dt>Wbemdisp. h</dt></span><span class="sxs-lookup"><span data-stu-id="c059d-138"><dt>Wbemdisp.h</dt></span></span> </dl>   |
| <span data-ttu-id="c059d-139">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="c059d-139">Type library</span></span><br/>             | <dl> <span data-ttu-id="c059d-140"><dt>Wbemdisp. tlb</dt></span><span class="sxs-lookup"><span data-stu-id="c059d-140"><dt>Wbemdisp.tlb</dt></span></span> </dl> |
| <span data-ttu-id="c059d-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c059d-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c059d-142"><dt>Wbemdisp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c059d-142"><dt>Wbemdisp.dll</dt></span></span> </dl> |
| <span data-ttu-id="c059d-143">CLSID</span><span class="sxs-lookup"><span data-stu-id="c059d-143">CLSID</span></span><br/>                    | <span data-ttu-id="c059d-144">CLSID- \_ Swap-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="c059d-144">CLSID\_SWbemSecurity</span></span><br/>                                                         |
| <span data-ttu-id="c059d-145">IID</span><span class="sxs-lookup"><span data-stu-id="c059d-145">IID</span></span><br/>                      | <span data-ttu-id="c059d-146">IID \_ iswbemsecurity</span><span class="sxs-lookup"><span data-stu-id="c059d-146">IID\_ISWbemSecurity</span></span><br/>                                                          |



## <a name="see-also"></a><span data-ttu-id="c059d-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c059d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c059d-148">API-Skript Objekte</span><span class="sxs-lookup"><span data-stu-id="c059d-148">Scripting API Objects</span></span>](scripting-api-objects.md)
</dt> <dt>

[<span data-ttu-id="c059d-149">Verwalten der WMI-Sicherheit</span><span class="sxs-lookup"><span data-stu-id="c059d-149">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="c059d-150">Festlegen der \_ Prozesssicherheit für Client Anwendungen \_</span><span class="sxs-lookup"><span data-stu-id="c059d-150">Setting Client\_Application\_Process Security</span></span>](setting-client-application-process-security.md)
</dt> <dt>

[<span data-ttu-id="c059d-151">**Wbemauthenticationlevelerum**</span><span class="sxs-lookup"><span data-stu-id="c059d-151">**WbemAuthenticationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemauthenticationlevelenum)
</dt> <dt>

[<span data-ttu-id="c059d-152">**Wbemimpersonationlevelenum**</span><span class="sxs-lookup"><span data-stu-id="c059d-152">**WbemImpersonationLevelEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemimpersonationlevelenum)
</dt> <dt>

[<span data-ttu-id="c059d-153">**Wbemprivilegeumum**</span><span class="sxs-lookup"><span data-stu-id="c059d-153">**WbemPrivilegeEnum**</span></span>](/windows/desktop/api/Wbemdisp/ne-wbemdisp-wbemprivilegeenum)
</dt> </dl>

 

