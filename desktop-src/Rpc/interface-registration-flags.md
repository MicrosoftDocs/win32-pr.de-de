---
title: Schnittstellenregistrierungsflags (rpcdce. h)
description: Die folgenden Konstanten werden im flags-Parameter der RpcServerRegisterIf2-und RpcServerRegisterIfEx-Funktionen verwendet.
ms.assetid: 387311c0-13df-4497-a0ac-ce6aec0e726c
topic_type:
- apiref
api_name:
- RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH
- RPC_IF_ALLOW_LOCAL_ONLY
- RPC_IF_AUTOLISTEN
- RPC_IF_OLE
- RPC_IF_ALLOW_UNKNOWN_AUTHORITY
- RPC_IF_ALLOW_SECURE_ONLY
- RPC_IF_SEC_NO_CACHE
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8af938038d2bc7000d80268fb4cb00941f6b282b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104105699"
---
# <a name="interface-registration-flags"></a><span data-ttu-id="da252-103">Schnittstellenregistrierungsflags</span><span class="sxs-lookup"><span data-stu-id="da252-103">Interface Registration Flags</span></span>

<span data-ttu-id="da252-104">Die folgenden Konstanten werden im *Flags* -Parameter der [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) -und [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) -Funktionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="da252-104">The following constants are used in the *Flags* parameter of the [**RpcServerRegisterIf2**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterif2) and [**RpcServerRegisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterifex) functions.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th style="text-align: left;"><span data-ttu-id="da252-105">Konstante</span><span class="sxs-lookup"><span data-stu-id="da252-105">Constant</span></span></th>
<th style="text-align: left;"><span data-ttu-id="da252-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="da252-106">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td style="text-align: left;"><span id="0"></span><dl> <span data-ttu-id="da252-107"><dt><strong>1,0</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="da252-107"><dt><strong>0</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="da252-108">Standard Schnittstellen Semantik.</span><span class="sxs-lookup"><span data-stu-id="da252-108">Standard interface semantics.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH"></span><span id="rpc_if_allow_callbacks_with_no_auth"></span><dl> <span data-ttu-id="da252-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="da252-109"><dt><strong>RPC_IF_ALLOW_CALLBACKS_WITH_NO_AUTH</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="da252-110">Wenn dieses Schnittstellenflag registriert ist, ruft die RPC-Laufzeit den registrierten Sicherheits Rückruf für alle Aufrufe auf, unabhängig von der Identität, der Protokoll Sequenz oder der Authentifizierungs Ebene des Clients.</span><span class="sxs-lookup"><span data-stu-id="da252-110">When this interface flag is registered, the RPC runtime invokes the registered security callback for all calls, regardless of identity, protocol sequence, or authentication level of the client.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="da252-111">Dieses Flag ist ab Windows XP mit SP2 und Windows Server 2003 mit SP1 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="da252-111">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span> <span data-ttu-id="da252-112">Wenn dieses Flag nicht festgelegt ist, filtert RPC automatisch alle nicht authentifizierten Aufrufe, bevor Sie den Sicherheits Rückruf erreichen.</span><span class="sxs-lookup"><span data-stu-id="da252-112">When this flag is not set, RPC automatically filters all unauthenticated calls before they reach the security callback.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_LOCAL_ONLY"></span><span id="rpc_if_allow_local_only"></span><dl> <span data-ttu-id="da252-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="da252-113"><dt><strong>RPC_IF_ALLOW_LOCAL_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="da252-114">Wenn dieses Schnittstellenflag registriert ist, lehnt die RPC-Laufzeit Aufrufe von Remote Clients ab.</span><span class="sxs-lookup"><span data-stu-id="da252-114">When this interface flag is registered, the RPC runtime rejects calls made by remote clients.</span></span> <span data-ttu-id="da252-115">Alle lokalen Aufrufe, die ncadg_ \*-und ncacn_ \*-Protokoll Sequenzen verwenden, werden ebenfalls abgelehnt, mit Ausnahme von ncacn_np.</span><span class="sxs-lookup"><span data-stu-id="da252-115">All local calls using ncadg_\* and ncacn_\* protocol sequences are also rejected, with the exception of ncacn_np.</span></span> <span data-ttu-id="da252-116">RPC lässt ncacn_NP Aufrufe nur zu, wenn der Aufruf nicht von SRV stammt.</span><span class="sxs-lookup"><span data-stu-id="da252-116">RPC allows ncacn_NP calls only if the call does not come from SRV.</span></span> <span data-ttu-id="da252-117">Aufrufe von Ncalrpc werden immer verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="da252-117">Calls from ncalrpc are always processed.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="da252-118">Dieses Flag ist ab Windows XP mit SP2 und Windows Server 2003 mit SP1 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="da252-118">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_AUTOLISTEN"></span><span id="rpc_if_autolisten"></span><dl> <span data-ttu-id="da252-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="da252-119"><dt><strong>RPC_IF_AUTOLISTEN</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="da252-120">Dabei handelt es sich um eine Schnittstelle zum <strong>automatischen lauschen</strong> .</span><span class="sxs-lookup"><span data-stu-id="da252-120">This is an <strong>auto-listen</strong> interface.</span></span> <span data-ttu-id="da252-121">Die Laufzeit beginnt mit dem lauschen auf Anrufe, sobald die erste autolistening-Schnittstelle registriert ist, und beendet die Überwachung, wenn die Registrierung der letzten autolistening-Schnittstelle aufgehoben wird.</span><span class="sxs-lookup"><span data-stu-id="da252-121">The run time begins listening for calls as soon as the first autolisten interface is registered, and stops listening when the last autolisten interface is unregistered.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_OLE"></span><span id="rpc_if_ole"></span><dl> <span data-ttu-id="da252-122"><dt><strong>RPC_IF_OLE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="da252-122"><dt><strong>RPC_IF_OLE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="da252-123">Für OLE reserviert.</span><span class="sxs-lookup"><span data-stu-id="da252-123">Reserved for OLE.</span></span> <span data-ttu-id="da252-124">Verwenden Sie dieses Flag nicht.</span><span class="sxs-lookup"><span data-stu-id="da252-124">Do not use this flag.</span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_UNKNOWN_AUTHORITY"></span><span id="rpc_if_allow_unknown_authority"></span><dl> <span data-ttu-id="da252-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="da252-125"><dt><strong>RPC_IF_ALLOW_UNKNOWN_AUTHORITY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="da252-126">Derzeit nicht implementiert.</span><span class="sxs-lookup"><span data-stu-id="da252-126">Currently not implemented.</span></span><br/></td>
</tr>
<tr class="odd">
<td style="text-align: left;"><span id="RPC_IF_ALLOW_SECURE_ONLY"></span><span id="rpc_if_allow_secure_only"></span><dl> <span data-ttu-id="da252-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="da252-127"><dt><strong>RPC_IF_ALLOW_SECURE_ONLY</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="da252-128">Schränkt Verbindungen mit Clients ein, die eine Autorisierungs Ebene höher als RPC_C_AUTHN_LEVEL_NONE verwenden.</span><span class="sxs-lookup"><span data-stu-id="da252-128">Limits connections to clients that use an authorization level higher than RPC_C_AUTHN_LEVEL_NONE.</span></span> <span data-ttu-id="da252-129">Wenn dieses Flag angegeben wird, können Clients in der <strong>null</strong> -Sitzung durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="da252-129">Specifying this flag allows clients to come through on the <strong>NULL</strong> session.</span></span> <span data-ttu-id="da252-130">Unter Windows XP und Windows Server 2003 sind solche Clients nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="da252-130">On Windows XP and Windows Server 2003, such clients are not allowed.</span></span> <span data-ttu-id="da252-131">Clients, bei denen der RPC_IF_ALLOW_SECURE_ONLY Test fehlschlägt, erhalten einen RPC_S_ACCESS_DENIED Fehler.</span><span class="sxs-lookup"><span data-stu-id="da252-131">Clients that fail the RPC_IF_ALLOW_SECURE_ONLY test receive an RPC_S_ACCESS_DENIED error.</span></span> <span data-ttu-id="da252-132">Die Verwendung des RPC_IF_ALLOW_SECURE_ONLY-Flags impliziert oder garantiert keine hohe Berechtigungsebene für den Teil des aufrufenden Benutzers.</span><span class="sxs-lookup"><span data-stu-id="da252-132">Using the RPC_IF_ALLOW_SECURE_ONLY flag does not imply or guarantee a high level of privilege on the part of the calling user.</span></span> <span data-ttu-id="da252-133">RPC überprüft nur, ob der Benutzer über gültige Anmelde Informationen verfügt. der aufrufende Benutzer verwendet möglicherweise das Gastkonto oder andere Konten mit niedrigen Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="da252-133">RPC only checks that the user has valid credentials; the calling user may be using the guest account or other low privileged accounts.</span></span> <span data-ttu-id="da252-134">Nehmen Sie bei Verwendung von RPC_IF_ALLOW_SECURE_ONLY keine hohen Berechtigungen an.</span><span class="sxs-lookup"><span data-stu-id="da252-134">Do not assume high privilege when RPC_IF_ALLOW_SECURE_ONLY is used.</span></span><br/> <span data-ttu-id="da252-135"><strong>Windows NT 4,0 und Windows Me/98/95:  </strong></span><span class="sxs-lookup"><span data-stu-id="da252-135"><strong>Windows NT 4.0 and Windows Me/98/95:  </strong></span></span><br/></td>
</tr>
<tr class="even">
<td style="text-align: left;"><span id="RPC_IF_SEC_NO_CACHE"></span><span id="rpc_if_sec_no_cache"></span><dl> <span data-ttu-id="da252-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span><span class="sxs-lookup"><span data-stu-id="da252-136"><dt><strong>RPC_IF_SEC_NO_CACHE</strong></dt> </span></span></dl></td>
<td style="text-align: left;"><span data-ttu-id="da252-137">Deaktiviert das Zwischenspeichern des Sicherheits Rückrufs und erzwingt einen Sicherheits Rückruf für jeden RPC-Aufruf für eine bestimmte Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="da252-137">Disables security callback caching, forcing a security callback for each RPC call on a given interface.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="da252-138">Dieses Flag ist ab Windows XP mit SP2 und Windows Server 2003 mit SP1 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="da252-138">This flag is available starting with Windows XP with SP2 and Windows Server 2003 with SP1.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



## <a name="requirements"></a><span data-ttu-id="da252-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="da252-139">Requirements</span></span>



| <span data-ttu-id="da252-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="da252-140">Requirement</span></span> | <span data-ttu-id="da252-141">Wert</span><span class="sxs-lookup"><span data-stu-id="da252-141">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="da252-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="da252-142">Minimum supported client</span></span><br/> | <span data-ttu-id="da252-143">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da252-143">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="da252-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="da252-144">Minimum supported server</span></span><br/> | <span data-ttu-id="da252-145">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="da252-145">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="da252-146">Header</span><span class="sxs-lookup"><span data-stu-id="da252-146">Header</span></span><br/>                   | <dl> <span data-ttu-id="da252-147"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="da252-147"><dt>Rpcdce.h</dt></span></span> </dl> |



 

 





