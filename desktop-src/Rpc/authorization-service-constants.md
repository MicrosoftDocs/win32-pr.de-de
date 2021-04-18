---
title: Authorization-Service Konstanten (rpcdce. h)
description: Die Autorisierungs Dienst Konstanten stellen die Autorisierungs Dienste dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden.
ms.assetid: b773bb51-7af0-4eb3-9438-fe3ef9a350db
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- Rpcdce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a0394163e97a822126e71eeda3cf8382f1dcc20
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104519263"
---
# <a name="authorization-service-constants"></a><span data-ttu-id="a4c75-103">Authorization-Service Konstanten</span><span class="sxs-lookup"><span data-stu-id="a4c75-103">Authorization-Service Constants</span></span>

<span data-ttu-id="a4c75-104">Die Autorisierungs Dienst Konstanten stellen die Autorisierungs Dienste dar, die an verschiedene Lauf Zeitfunktionen übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="a4c75-104">The authorization service constants represent the authorization services passed to various run-time functions.</span></span>

<span data-ttu-id="a4c75-105">Die folgenden Konstanten sind gültige Werte für den *authzsvc* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="a4c75-105">The following constants are valid values for the *AuthzSvc* parameter.</span></span> <span data-ttu-id="a4c75-106">Die meisten Anwendungen finden RPC \_ C \_ Authz \_ nicht ausreichend.</span><span class="sxs-lookup"><span data-stu-id="a4c75-106">Most applications find RPC\_C\_AUTHZ\_NON sufficient.</span></span>



| <span data-ttu-id="a4c75-107">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="a4c75-107">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="a4c75-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a4c75-108">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="a4c75-109"><dt>**RPC \_ C \_ Authz \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="a4c75-109"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="a4c75-110">Der Server führt keine Autorisierung aus.</span><span class="sxs-lookup"><span data-stu-id="a4c75-110">Server performs no authorization.</span></span><br/>                                                                                                                                                                                                                                                                 |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="a4c75-111"><dt>**RPC \_ C- \_ Authz- \_ Name**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="a4c75-111"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="a4c75-112">Der Server führt die Autorisierung basierend auf dem Prinzipal Namen des Clients aus.</span><span class="sxs-lookup"><span data-stu-id="a4c75-112">Server performs authorization based on the client's principal name.</span></span><br/>                                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="a4c75-113"><dt>**RPC \_ C \_ Authz \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="a4c75-113"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="a4c75-114">Der Server führt die Autorisierungs Überprüfung mithilfe der Informationen des DCE Privilege Attribute Certificate (PAC) des Clients durch, die an den Server gesendet wird, wobei jeder Remote Prozedur Rückruf mit dem Bindungs handle erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a4c75-114">Server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="a4c75-115">Im Allgemeinen wird der Zugriff auf DCE-Zugriffs Steuerungs Listen ([ACLs](/windows/desktop/api/winnt/ns-winnt-acl)) überprüft.</span><span class="sxs-lookup"><span data-stu-id="a4c75-115">Generally, access is checked against DCE access control lists ([ACLs](/windows/desktop/api/winnt/ns-winnt-acl)).</span></span><br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="a4c75-116"><dt>**RPC \_ C \_ Authz \_ Standard**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="a4c75-116"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="a4c75-117">Der Server verwendet den Standard Autorisierungs Dienst für den aktuellen SSP.</span><span class="sxs-lookup"><span data-stu-id="a4c75-117">Server uses the default authorization service for the current SSP.</span></span><br/>                                                                                                                                                                                                                                |



## <a name="requirements"></a><span data-ttu-id="a4c75-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a4c75-118">Requirements</span></span>



| <span data-ttu-id="a4c75-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a4c75-119">Requirement</span></span> | <span data-ttu-id="a4c75-120">Wert</span><span class="sxs-lookup"><span data-stu-id="a4c75-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c75-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a4c75-121">Minimum supported client</span></span><br/> | <span data-ttu-id="a4c75-122">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4c75-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="a4c75-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a4c75-123">Minimum supported server</span></span><br/> | <span data-ttu-id="a4c75-124">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="a4c75-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="a4c75-125">Header</span><span class="sxs-lookup"><span data-stu-id="a4c75-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="a4c75-126"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="a4c75-126"><dt>Rpcdce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a4c75-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4c75-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a4c75-128">**Rpcbindinginqauthinfo**</span><span class="sxs-lookup"><span data-stu-id="a4c75-128">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="a4c75-129">**Rpcbindingsetauthinfo**</span><span class="sxs-lookup"><span data-stu-id="a4c75-129">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> <dt>

[<span data-ttu-id="a4c75-130">**Rpcbindinginqauthclient**</span><span class="sxs-lookup"><span data-stu-id="a4c75-130">**RpcBindingInqAuthClient**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclient)
</dt> <dt>

[<span data-ttu-id="a4c75-131">**Rpcbindinginqauthcliumtex**</span><span class="sxs-lookup"><span data-stu-id="a4c75-131">**RpcBindingInqAuthClientEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthclientex)
</dt> <dt>

[<span data-ttu-id="a4c75-132">**Rpcbindingsetauthinfoex**</span><span class="sxs-lookup"><span data-stu-id="a4c75-132">**RpcBindingSetAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfoexa)
</dt> <dt>

[<span data-ttu-id="a4c75-133">**Rpcbindinginqauthinfoex**</span><span class="sxs-lookup"><span data-stu-id="a4c75-133">**RpcBindingInqAuthInfoEx**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfoexa)
</dt> <dt>

[<span data-ttu-id="a4c75-134">**RpcMgmtInqDefaultProtectLevel**</span><span class="sxs-lookup"><span data-stu-id="a4c75-134">**RpcMgmtInqDefaultProtectLevel**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqdefaultprotectlevel)
</dt> </dl>

 

