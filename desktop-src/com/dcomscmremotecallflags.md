---
title: Dcomscmremotecallflags
description: Steuert das Verhalten von Aufrufen vom lokalen DCOM-Dienststeuerungs-Manager (dcomscm) zu einem Remote-dcomscm.
ms.assetid: fb306da7-4b9a-4386-8525-7f78bd6bf728
keywords:
- Dcomscmremotecallflags-Registrierungs Wert com
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6fda58975e40ac6ac1633db8aa78f2c7636f9103
ms.sourcegitcommit: 5f33645661bf8c825a7a2e73950b1f4ea0f1cd82
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/21/2020
ms.locfileid: "104039662"
---
# <a name="dcomscmremotecallflags"></a><span data-ttu-id="4a23c-104">Dcomscmremotecallflags</span><span class="sxs-lookup"><span data-stu-id="4a23c-104">DCOMSCMRemoteCallFlags</span></span>

<span data-ttu-id="4a23c-105">Steuert das Verhalten von Aufrufen vom lokalen DCOM-Dienststeuerungs-Manager (dcomscm) zu einem Remote-dcomscm.</span><span class="sxs-lookup"><span data-stu-id="4a23c-105">Controls the behavior of calls from the local DCOM Service Control Manager (DCOMSCM) to a remote DCOMSCM.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="4a23c-106">Registrierungseintrag</span><span class="sxs-lookup"><span data-stu-id="4a23c-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\Ole
   DCOMSCMRemoteCallFlags = value
```

## <a name="remarks"></a><span data-ttu-id="4a23c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4a23c-107">Remarks</span></span>

<span data-ttu-id="4a23c-108">Dies ist ein **reg \_ DWORD** -Wert.</span><span class="sxs-lookup"><span data-stu-id="4a23c-108">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="4a23c-109">Wert</span><span class="sxs-lookup"><span data-stu-id="4a23c-109">Value</span></span> | <span data-ttu-id="4a23c-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4a23c-110">Description</span></span>                                       |
|-------|---------------------------------------------------|
| <span data-ttu-id="4a23c-111">0x1</span><span class="sxs-lookup"><span data-stu-id="4a23c-111">0x1</span></span>   | <span data-ttu-id="4a23c-112">**dcomscm \_ - \_ Aktivierung \_ alle \_ authnservices verwenden**</span><span class="sxs-lookup"><span data-stu-id="4a23c-112">**DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES**</span></span>  |
| <span data-ttu-id="4a23c-113">0x2</span><span class="sxs-lookup"><span data-stu-id="4a23c-113">0x2</span></span>   | <span data-ttu-id="4a23c-114">**nicht sicheren Rückruf durch dcomscm- \_ Aktivierung \_ \_ nicht zulassen \_**</span><span class="sxs-lookup"><span data-stu-id="4a23c-114">**DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL**</span></span> |
| <span data-ttu-id="4a23c-115">0x4</span><span class="sxs-lookup"><span data-stu-id="4a23c-115">0x4</span></span>   | <span data-ttu-id="4a23c-116">**dcomscm \_ Auflösen der \_ Verwendung \_ aller \_ authnservices**</span><span class="sxs-lookup"><span data-stu-id="4a23c-116">**DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES**</span></span>     |
| <span data-ttu-id="4a23c-117">0x8</span><span class="sxs-lookup"><span data-stu-id="4a23c-117">0x8</span></span>   | <span data-ttu-id="4a23c-118">**dcomscm \_ Auflösen \_ \_ unsichere Aufrufe nicht zulassen \_**</span><span class="sxs-lookup"><span data-stu-id="4a23c-118">**DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL**</span></span>    |
| <span data-ttu-id="4a23c-119">0x10</span><span class="sxs-lookup"><span data-stu-id="4a23c-119">0x10</span></span>  | <span data-ttu-id="4a23c-120">**dcomscm- \_ ping \_ verwendet \_ Mid \_ authnservice.**</span><span class="sxs-lookup"><span data-stu-id="4a23c-120">**DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE**</span></span>         |



 

## <a name="dcomscm_activation_use_all_authnservices-description"></a><span data-ttu-id="4a23c-121">Dcomscm \_ - \_ Aktivierung \_ alle \_ authnservices-Beschreibungen verwenden</span><span class="sxs-lookup"><span data-stu-id="4a23c-121">DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="4a23c-122">Wenn der Client eine Aktivierungs Anforderung ausgibt, bei der die Standard Sicherheitseinstellungen verwendet werden, verwendet der lokale dcomscm den Aushandlungs Authentifizierungsdienst, wenn der Remote-dcomscm aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="4a23c-122">When the client issues an activation request that uses the default security settings, the local DCOMSCM uses the Negotiate authentication service when making the activation RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="4a23c-123">Wenn der Aufruf fehlschlägt, führt der lokale dcomscm den RPC-Aktivierungs Aufruf ohne Sicherheit aus.</span><span class="sxs-lookup"><span data-stu-id="4a23c-123">If the call fails, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="4a23c-124">**Windows Server 2003 und Windows XP/2000:** Wenn der RPC-Aktivierungs Aufruf, der den Aushandlungs Authentifizierungsdienst verwendet, fehlschlägt, führt der lokale dcomscm den RPC-Aktivierungs Aufruf mithilfe von Kerberos, NTLM oder anderen konfigurierten Sicherheitsanbietern aus.</span><span class="sxs-lookup"><span data-stu-id="4a23c-124">**Windows Server 2003 and Windows XP/2000:** If the activation RPC call that uses the Negotiate authentication service fails, the local DCOMSCM makes the activation RPC call using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="4a23c-125">Wenn keine Sicherheitsanbieter funktionieren, stellt der lokale dcomscm den RPC-Aktivierungs Aufruf ohne Sicherheit dar.</span><span class="sxs-lookup"><span data-stu-id="4a23c-125">If no security providers work, the local DCOMSCM makes the activation RPC call using no security.</span></span>

<span data-ttu-id="4a23c-126">Wenn Sie dieses Flag festlegen, kann der lokale dcomscm unter Windows Vista oder höher so gestaltet werden, dass es sich wie vor Vista-Systemen verhält.</span><span class="sxs-lookup"><span data-stu-id="4a23c-126">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="4a23c-127">Es wird nicht empfohlen, dieses Flag festzulegen, sofern dies aus Kompatibilitätsgründen nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4a23c-127">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_activation_disallow_unsecure_call-description"></a><span data-ttu-id="4a23c-128">Dcomscm- \_ Aktivierung \_ \_ unsichere \_ aufrufsbeschreibung nicht zulassen</span><span class="sxs-lookup"><span data-stu-id="4a23c-128">DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="4a23c-129">Wenn die **dcomscm- \_ Aktivierung \_ \_ unsicheres \_ Aufruf** Flag nicht zulassen festgelegt ist, führt der lokale dcomscm keinen nicht sicheren Aktivierungs-RPC-Aufruf aus.</span><span class="sxs-lookup"><span data-stu-id="4a23c-129">If the **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure activation RPC call.</span></span> <span data-ttu-id="4a23c-130">Wenn Sie zulassen möchten, dass Clients Aktivierungs Anforderungen mit nicht standardmäßigen Sicherheitseinstellungen herstellen, geben Sie die [**coauthinfo**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) -Struktur beim Ausführen der Aktivierungs Anforderung an.</span><span class="sxs-lookup"><span data-stu-id="4a23c-130">To enable clients to make activation requests with non-default security settings, specify the [**COAUTHINFO**](/windows/desktop/api/wtypesbase/ns-wtypesbase-coauthinfo) structure when making the activation request.</span></span> <span data-ttu-id="4a23c-131">In diesem Fall werden bei der **dcomscm- \_ Aktivierung \_ \_ alle \_ authnservices verwendet** , und die **dcomscm-Aktivierung verhindert, \_ \_ dass \_ unsichere \_ callflags** ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="4a23c-131">In this case, the **DCOMSCM\_ACTIVATION\_USE\_ALL\_AUTHNSERVICES** and **DCOMSCM\_ACTIVATION\_DISALLOW\_UNSECURE\_CALL** flags are ignored.</span></span>

<span data-ttu-id="4a23c-132">Es wird nicht empfohlen, dieses Flag festzulegen, es sei denn, alle Clients und Server im Netzwerk sind vollständig authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="4a23c-132">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_resolve_use_all_authnservices-description"></a><span data-ttu-id="4a23c-133">Dcomscm \_ - \_ Beschreibung "use \_ All \_ authnservices" auflösen</span><span class="sxs-lookup"><span data-stu-id="4a23c-133">DCOMSCM\_RESOLVE\_USE\_ALL\_AUTHNSERVICES Description</span></span>

<span data-ttu-id="4a23c-134">Wenn der Client einen Objekt Verweis aufnimmt, verwendet der lokale dcomscm den Aushandlungs Authentifizierungsdienst, wenn der RPC-Auflösungs-RPC-Aufruf an den Remote-dcomscm erfolgt.</span><span class="sxs-lookup"><span data-stu-id="4a23c-134">When the client unmarshals an object reference, the local DCOMSCM uses the Negotiate authentication service when making the OXID Resolution RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="4a23c-135">Wenn der Aufruf fehlschlägt, führt der lokale dcomscm den RPC-Aufruf der oxid Auflösung ohne Sicherheit aus.</span><span class="sxs-lookup"><span data-stu-id="4a23c-135">If the call fails, the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="4a23c-136">**Windows Server 2003 und Windows XP/2000:** Wenn bei der RPC-Auflösung ein RPC-Aufruf mit dem Aushandlungs Authentifizierungsdienst fehlschlägt, führt der lokale dcomscm den RPC-Aufruf der oxid Auflösung mithilfe von Kerberos, NTLM oder anderen konfigurierten Sicherheitsanbietern aus.</span><span class="sxs-lookup"><span data-stu-id="4a23c-136">**Windows Server 2003 and Windows XP/2000:** If the OXID Resolution RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the OXID Resolution RPC call by using Kerberos, NTLM, or other configured security providers.</span></span> <span data-ttu-id="4a23c-137">Wenn keine Sicherheitsanbieter funktionieren, führt der lokale dcomscm den RPC-Aufruf der oxid Auflösung ohne Sicherheit aus.</span><span class="sxs-lookup"><span data-stu-id="4a23c-137">If no security providers work, then the local DCOMSCM makes the OXID Resolution RPC call using no security.</span></span>

<span data-ttu-id="4a23c-138">Wenn Sie dieses Flag festlegen, kann der lokale dcomscm unter Windows Vista oder höher so gestaltet werden, dass es sich wie vor Vista-Systemen verhält.</span><span class="sxs-lookup"><span data-stu-id="4a23c-138">By setting this flag, the local DCOMSCM on Windows Vista or higher can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="4a23c-139">Es wird nicht empfohlen, dieses Flag festzulegen, sofern dies aus Kompatibilitätsgründen nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4a23c-139">It is not recommended to set this flag unless required for compatibility reasons.</span></span>

## <a name="dcomscm_resolve_disallow_unsecure_call-description"></a><span data-ttu-id="4a23c-140">Dcomscm \_ Auflösen \_ \_ unsichere \_ aufrufsbeschreibung nicht zulassen</span><span class="sxs-lookup"><span data-stu-id="4a23c-140">DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL Description</span></span>

<span data-ttu-id="4a23c-141">Wenn das Flag zum **\_ Auflösen von \_ \_ unsicherem \_ Aufruf durch dcomscm auflösen nicht zulassen** festgelegt ist, führt der lokale dcomscm keinen nicht sicheren RPC-Auflösungs Aufruf aus.</span><span class="sxs-lookup"><span data-stu-id="4a23c-141">If the **DCOMSCM\_RESOLVE\_DISALLOW\_UNSECURE\_CALL** flag is set, the local DCOMSCM does not make an unsecure OXID Resolution RPC call.</span></span> <span data-ttu-id="4a23c-142">Außerdem führt der lokale dcomscm keinen unsicheren Garbage Collection Ping-RPC-Aufruf aus.</span><span class="sxs-lookup"><span data-stu-id="4a23c-142">In addition, the local DCOMSCM does not make an unsecure garbage collection Ping RPC call.</span></span> <span data-ttu-id="4a23c-143">Es wird nicht empfohlen, dieses Flag festzulegen, es sei denn, alle Clients und Server im Netzwerk sind vollständig authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="4a23c-143">It is not recommended to set this flag unless all the clients and servers in the network are fully authenticated.</span></span>

## <a name="dcomscm_ping_use_mid_authnservice-description"></a><span data-ttu-id="4a23c-144">Dcomscm \_ ping \_ use \_ Mid \_ authnservice Description</span><span class="sxs-lookup"><span data-stu-id="4a23c-144">DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE Description</span></span>

<span data-ttu-id="4a23c-145">Der lokale dcomscm verwendet den Aushandlungs Authentifizierungsdienst, wenn der RPC-Aufruf der Garbage Collection an den Remote-dcomscm gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="4a23c-145">The local DCOMSCM uses the Negotiate authentication service when making the garbage-collection Ping RPC call to the remote DCOMSCM.</span></span> <span data-ttu-id="4a23c-146">Wenn der Aufruf fehlschlägt, führt der lokale dcomscm den RPC-Aufruf der Garbage Collection per Ping ohne Sicherheit aus.</span><span class="sxs-lookup"><span data-stu-id="4a23c-146">If the call fails, the local DCOMSCM makes the garbage-collection Ping RPC call using no security.</span></span>

<span data-ttu-id="4a23c-147">**Windows Server 2003 und Windows XP/2000:** Wenn das Ping-RPC-Aufruf der Garbage Collection mithilfe des Aushandlungs Authentifizierungs Diensts fehlschlägt, führt der lokale dcomscm den Garbage Collection Ping-RPC-Aufruf mithilfe von Kerberos, NTLM und anderen konfigurierten Sicherheitsanbietern aus.</span><span class="sxs-lookup"><span data-stu-id="4a23c-147">**Windows Server 2003 and Windows XP/2000:** If the garbage-collection Ping RPC call using the Negotiate authentication service fails, the local DCOMSCM makes the garbage collection Ping RPC call by using Kerberos, NTLM, and other configured security providers.</span></span> <span data-ttu-id="4a23c-148">Wenn keine Sicherheitsanbieter funktionieren, führt der lokale dcomscm den Garbage Collection Ping-RPC-Aufruf mithilfe von No Security aus.</span><span class="sxs-lookup"><span data-stu-id="4a23c-148">If no security providers work, then the local DCOMSCM makes the garbage collection Ping RPC call using no security.</span></span>

<span data-ttu-id="4a23c-149">Wenn Sie dieses Flag festlegen, kann der lokale dcomscm unter Windows Vista oder höher so gestaltet werden, dass es sich wie vor Vista-Systemen verhält.</span><span class="sxs-lookup"><span data-stu-id="4a23c-149">By setting this flag, the local DCOMSCM on Windows Vista or above can be made to behave like pre-Vista systems.</span></span> <span data-ttu-id="4a23c-150">Es wird nicht empfohlen, das Flag " **dcomscm \_ ping \_ use \_ Mid \_ authnservice** " festzulegen, sofern dies aus Kompatibilitätsgründen nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4a23c-150">It is not recommended to set the **DCOMSCM\_PING\_USE\_MID\_AUTHNSERVICE** flag unless required for compatibility reasons.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4a23c-151">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="4a23c-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4a23c-152">Authentifizierung für Remote Verbindungen</span><span class="sxs-lookup"><span data-stu-id="4a23c-152">Authentication for Remote Connections</span></span>](/windows/desktop/WinRM/authentication-for-remote-connections)
</dt> <dt>

[<span data-ttu-id="4a23c-153">EnableDCOM</span><span class="sxs-lookup"><span data-stu-id="4a23c-153">EnableDCOM</span></span>](enabledcom.md)
</dt> <dt>

[<span data-ttu-id="4a23c-154">Registrieren von com-Servern</span><span class="sxs-lookup"><span data-stu-id="4a23c-154">Registering COM Servers</span></span>](registering-com-servers.md)
</dt> <dt>

[<span data-ttu-id="4a23c-155">Sicherheit in com</span><span class="sxs-lookup"><span data-stu-id="4a23c-155">Security in COM</span></span>](security-in-com.md)
</dt> </dl>

 

 