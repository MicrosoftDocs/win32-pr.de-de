---
title: Authentication-Level Konstanten (rpcdce. h)
description: Die Konstanten auf Authentifizierungs Ebene stellen Authentifizierungs Ebenen dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden.
ms.assetid: b8bb2517-e1a0-4607-a672-259f8686fc3e
topic_type:
- apiref
api_name:
- RPC_C_AUTHN_LEVEL_DEFAULT
- RPC_C_AUTHN_LEVEL_NONE
- RPC_C_AUTHN_LEVEL_CONNECT
- RPC_C_AUTHN_LEVEL_CALL
- RPC_C_AUTHN_LEVEL_PKT
- RPC_C_AUTHN_LEVEL_PKT_INTEGRITY
- RPC_C_AUTHN_LEVEL_PKT_PRIVACY
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 114e5624b2cbc8af0b86a29daff2c1761f6fee39
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518728"
---
# <a name="authentication-level-constants"></a><span data-ttu-id="6c9ed-103">Konstanten auf Authentifizierungsebene</span><span class="sxs-lookup"><span data-stu-id="6c9ed-103">Authentication-Level Constants</span></span>

<span data-ttu-id="6c9ed-104">Die Konstanten auf Authentifizierungs Ebene stellen Authentifizierungs Ebenen dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-104">The authentication-level constants represent authentication levels passed to various run-time functions.</span></span> <span data-ttu-id="6c9ed-105">Diese Ebenen werden in der Reihenfolge der Erhöhung der Authentifizierung aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-105">These levels are listed in order of increasing authentication.</span></span> <span data-ttu-id="6c9ed-106">Jede neue Ebene erhöht die Authentifizierung, die von der vorherigen Ebene bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-106">Each new level adds to the authentication provided by the previous level.</span></span> <span data-ttu-id="6c9ed-107">Wenn die RPC-Lauf Zeit Bibliothek die angegebene Ebene nicht unterstützt, wird automatisch ein Upgrade auf die nächsthöhere unterstützte Ebene durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-107">If the RPC run-time library does not support the specified level, it automatically upgrades to the next higher supported level.</span></span>



| <span data-ttu-id="6c9ed-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="6c9ed-108">Constant</span></span>                                                                                                                                                                                                                | <span data-ttu-id="6c9ed-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6c9ed-109">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHN_LEVEL_DEFAULT"></span><span id="rpc_c_authn_level_default"></span><dl> <span data-ttu-id="6c9ed-110"><dt>**Standardwert für RPC- \_ C- \_ authn \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c9ed-110"><dt>**RPC\_C\_AUTHN\_LEVEL\_DEFAULT**</dt></span></span> </dl>                    | <span data-ttu-id="6c9ed-111">Verwendet die Standardauthentifizierungsebene für den angegebenen Authentifizierungsdienst.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-111">Uses the default authentication level for the specified authentication service.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                    |
| <span id="RPC_C_AUTHN_LEVEL_NONE"></span><span id="rpc_c_authn_level_none"></span><dl> <span data-ttu-id="6c9ed-112"><dt>**RPC- \_ C- \_ authn- \_ Ebene \_ None**</dt></span><span class="sxs-lookup"><span data-stu-id="6c9ed-112"><dt>**RPC\_C\_AUTHN\_LEVEL\_NONE**</dt></span></span> </dl>                             | <span data-ttu-id="6c9ed-113">Führt keine Authentifizierung durch.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-113">Performs no authentication.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="RPC_C_AUTHN_LEVEL_CONNECT"></span><span id="rpc_c_authn_level_connect"></span><dl> <span data-ttu-id="6c9ed-114"><dt>**RPC- \_ C \_ authn \_ Level \_ Connect**</dt></span><span class="sxs-lookup"><span data-stu-id="6c9ed-114"><dt>**RPC\_C\_AUTHN\_LEVEL\_CONNECT**</dt></span></span> </dl>                    | <span data-ttu-id="6c9ed-115">Führt nur eine Authentifizierung aus, wenn der Client eine Beziehung zu einem Server herstellt.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-115">Authenticates only when the client establishes a relationship with a server.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                       |
| <span id="RPC_C_AUTHN_LEVEL_CALL"></span><span id="rpc_c_authn_level_call"></span><dl> <span data-ttu-id="6c9ed-116"><dt>**RPC- \_ C \_ authn-Ebene- \_ \_ Aufruf**</dt></span><span class="sxs-lookup"><span data-stu-id="6c9ed-116"><dt>**RPC\_C\_AUTHN\_LEVEL\_CALL**</dt></span></span> </dl>                             | <span data-ttu-id="6c9ed-117">Authentifiziert sich nur zu Beginn jedes Remote Prozedur Aufrufes, wenn der Server die Anforderung empfängt.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-117">Authenticates only at the beginning of each remote procedure call when the server receives the request.</span></span> <span data-ttu-id="6c9ed-118">Gilt nicht für Remote Prozedur Aufrufe, die mit den verbindungsbasierten Protokoll Sequenzen durchgeführt werden (solche, die mit dem Präfix "ncacn" beginnen).</span><span class="sxs-lookup"><span data-stu-id="6c9ed-118">Does not apply to remote procedure calls made using the connection-based protocol sequences (those that start with the prefix "ncacn").</span></span> <span data-ttu-id="6c9ed-119">Wenn die Protokoll Sequenz in einem Bindungs handle eine Verbindungs basierte Protokoll Sequenz ist und Sie diese Ebene angeben, verwendet diese Routine stattdessen die Pkt-Konstante der RPC- \_ C- \_ authn- \_ Ebene \_ .</span><span class="sxs-lookup"><span data-stu-id="6c9ed-119">If the protocol sequence in a binding handle is a connection-based protocol sequence and you specify this level, this routine instead uses the RPC\_C\_AUTHN\_LEVEL\_PKT constant.</span></span><br/> |
| <span id="RPC_C_AUTHN_LEVEL_PKT"></span><span id="rpc_c_authn_level_pkt"></span><dl> <span data-ttu-id="6c9ed-120"><dt>**Pkt der RPC- \_ C- \_ authn- \_ Ebene \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c9ed-120"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT**</dt></span></span> </dl>                                | <span data-ttu-id="6c9ed-121">Authentifiziert nur, dass alle empfangenen Daten vom erwarteten Client stammen.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-121">Authenticates only that all data received is from the expected client.</span></span> <span data-ttu-id="6c9ed-122">Überprüft nicht die Daten selbst.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-122">Does not validate the data itself.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_INTEGRITY"></span><span id="rpc_c_authn_level_pkt_integrity"></span><dl> <span data-ttu-id="6c9ed-123"><dt>**\_Pkt-Integrität der RPC C- \_ authn- \_ Ebene \_ \_**</dt></span><span class="sxs-lookup"><span data-stu-id="6c9ed-123"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_INTEGRITY**</dt></span></span> </dl> | <span data-ttu-id="6c9ed-124">Authentifiziert und überprüft, ob keine der zwischen Client und Server übertragenen Daten geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-124">Authenticates and verifies that none of the data transferred between client and server has been modified.</span></span><br/>                                                                                                                                                                                                                                                                                                                          |
| <span id="RPC_C_AUTHN_LEVEL_PKT_PRIVACY"></span><span id="rpc_c_authn_level_pkt_privacy"></span><dl> <span data-ttu-id="6c9ed-125"><dt>**\_ \_ \_ \_ Pkt- \_ Datenschutz auf RPC-C-Ebene**</dt></span><span class="sxs-lookup"><span data-stu-id="6c9ed-125"><dt>**RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY**</dt></span></span> </dl>       | <span data-ttu-id="6c9ed-126">Schließt alle vorherigen Ebenen ein und stellt sicher, dass Klartext-Daten nur vom Absender und Empfänger angezeigt werden können.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-126">Includes all previous levels, and ensures clear text data can only be seen by the sender and the receiver.</span></span> <span data-ttu-id="6c9ed-127">Im lokalen Fall umfasst dies die Verwendung eines sicheren Kanals.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-127">In the local case, this involves using a secure channel.</span></span> <span data-ttu-id="6c9ed-128">Im Remote Fall ist dies das Verschlüsseln des Argument Werts jedes Remote Prozedur Aufrufes.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-128">In the remote case, this involves encrypting the argument value of each remote procedure call.</span></span><br/>                                                                                                                                                                 |



## <a name="remarks"></a><span data-ttu-id="6c9ed-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c9ed-129">Remarks</span></span>

<span data-ttu-id="6c9ed-130">Unabhängig von dem durch die Konstante angegebenen Wert verwendet **Ncalrpc** immer die \_ \_ \_ \_ Pkt- \_ Datenschutzebene der RPC-C-authn-Ebene.</span><span class="sxs-lookup"><span data-stu-id="6c9ed-130">Regardless of the value specified by the constant, **ncalrpc** always uses RPC\_C\_AUTHN\_LEVEL\_PKT\_PRIVACY.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c9ed-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c9ed-131">Requirements</span></span>



| <span data-ttu-id="6c9ed-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c9ed-132">Requirement</span></span> | <span data-ttu-id="6c9ed-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6c9ed-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6c9ed-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c9ed-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6c9ed-135">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c9ed-135">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6c9ed-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c9ed-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6c9ed-137">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6c9ed-137">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6c9ed-138">Header</span><span class="sxs-lookup"><span data-stu-id="6c9ed-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c9ed-139"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c9ed-139"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c9ed-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c9ed-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c9ed-141">**Rpcbindinginqauthinfo**</span><span class="sxs-lookup"><span data-stu-id="6c9ed-141">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="6c9ed-142">**Rpcbindingsetauthinfo**</span><span class="sxs-lookup"><span data-stu-id="6c9ed-142">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="6c9ed-143">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="6c9ed-143">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> <dt>

[<span data-ttu-id="6c9ed-144">**Rpcbindinginqauthclient**</span><span class="sxs-lookup"><span data-stu-id="6c9ed-144">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="6c9ed-145">**Rpcbindinginqauthcliumtex**</span><span class="sxs-lookup"><span data-stu-id="6c9ed-145">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="6c9ed-146">**Rpcbindingsetauthinfoex**</span><span class="sxs-lookup"><span data-stu-id="6c9ed-146">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="6c9ed-147">**Rpcbindinginqauthinfoex**</span><span class="sxs-lookup"><span data-stu-id="6c9ed-147">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> </dl>

 

 





