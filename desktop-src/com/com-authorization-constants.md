---
title: Autorisierungs Konstanten (rpcdce. h)
description: Definiert, was der Server autorisiert.
ms.assetid: a0bc9337-b7e4-41c5-ae36-4843fa7d98ce
topic_type:
- apiref
api_name:
- RPC_C_AUTHZ_NONE
- RPC_C_AUTHZ_NAME
- RPC_C_AUTHZ_DCE
- RPC_C_AUTHZ_DEFAULT
api_location:
- RpcDce.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ed2c46ad729e02fd63eb9b8088d31f05515c2ef8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743712"
---
# <a name="authorization-constants"></a><span data-ttu-id="f4de0-103">Autorisierungs Konstanten</span><span class="sxs-lookup"><span data-stu-id="f4de0-103">Authorization Constants</span></span>

<span data-ttu-id="f4de0-104">Definiert, was der Server autorisiert.</span><span class="sxs-lookup"><span data-stu-id="f4de0-104">Defines what the server authorizes.</span></span>



| <span data-ttu-id="f4de0-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="f4de0-105">Constant/value</span></span>                                                                                                                                                                                                                                    | <span data-ttu-id="f4de0-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f4de0-106">Description</span></span>                                                                                                                                                                                                                                                                                       |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RPC_C_AUTHZ_NONE"></span><span id="rpc_c_authz_none"></span><dl> <span data-ttu-id="f4de0-107"><dt>**RPC \_ C \_ Authz \_ None**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="f4de0-107"><dt>**RPC\_C\_AUTHZ\_NONE**</dt> <dt>0</dt></span></span> </dl>                   | <span data-ttu-id="f4de0-108">Der Server führt keine Autorisierung aus.</span><span class="sxs-lookup"><span data-stu-id="f4de0-108">The server performs no authorization.</span></span> <span data-ttu-id="f4de0-109">Derzeit verwenden RPC \_ c \_ authn \_ Winnt, RPC \_ c \_ authn \_ GSS \_ SChannel und RPC \_ c \_ authn \_ GSS \_ Kerberos nur RPC \_ c \_ Authz \_ None.</span><span class="sxs-lookup"><span data-stu-id="f4de0-109">Currently, RPC\_C\_AUTHN\_WINNT, RPC\_C\_AUTHN\_GSS\_SCHANNEL, and RPC\_C\_AUTHN\_GSS\_KERBEROS all use only RPC\_C\_AUTHZ\_NONE.</span></span><br/>                                                                                                                |
| <span id="RPC_C_AUTHZ_NAME"></span><span id="rpc_c_authz_name"></span><dl> <span data-ttu-id="f4de0-110"><dt>**RPC \_ C- \_ Authz- \_ Name**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="f4de0-110"><dt>**RPC\_C\_AUTHZ\_NAME**</dt> <dt>1</dt></span></span> </dl>                   | <span data-ttu-id="f4de0-111">Der Server führt die Autorisierung basierend auf dem Prinzipal Namen des Clients aus.</span><span class="sxs-lookup"><span data-stu-id="f4de0-111">The server performs authorization based on the client's principal name.</span></span> <br/>                                                                                                                                                                                                               |
| <span id="RPC_C_AUTHZ_DCE"></span><span id="rpc_c_authz_dce"></span><dl> <span data-ttu-id="f4de0-112"><dt>**RPC \_ C \_ Authz \_ DCE**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="f4de0-112"><dt>**RPC\_C\_AUTHZ\_DCE**</dt> <dt>2</dt></span></span> </dl>                      | <span data-ttu-id="f4de0-113">Der Server führt die Autorisierungs Überprüfung mithilfe der Informationen des DCE Privilege Attribute Certificate (PAC) des Clients durch, die an den Server gesendet wird, wobei jeder Remote Prozedur Rückruf mit dem Bindungs handle erfolgt.</span><span class="sxs-lookup"><span data-stu-id="f4de0-113">The server performs authorization checking using the client's DCE privilege attribute certificate (PAC) information, which is sent to the server with each remote procedure call made using the binding handle.</span></span> <span data-ttu-id="f4de0-114">Im Allgemeinen wird der Zugriff auf DCE-Zugriffs Steuerungs Listen (ACLs) überprüft.</span><span class="sxs-lookup"><span data-stu-id="f4de0-114">Generally, access is checked against DCE access control lists (ACLs).</span></span> <br/> |
| <span id="RPC_C_AUTHZ_DEFAULT"></span><span id="rpc_c_authz_default"></span><dl> <span data-ttu-id="f4de0-115"><dt>**RPC \_ C \_ Authz \_ Standard**</dt> <dt>0xFFFFFFFF</dt></span><span class="sxs-lookup"><span data-stu-id="f4de0-115"><dt>**RPC\_C\_AUTHZ\_DEFAULT**</dt> <dt>0xffffffff</dt></span></span> </dl> | <span data-ttu-id="f4de0-116">Die Autorisierungs Ebene kann von DCOM mithilfe des normalen Algorithmus für die Sicherheits-und-Aushandlung ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="f4de0-116">DCOM can choose the authorization level using its normal security blanket negotiation algorithm.</span></span> <span data-ttu-id="f4de0-117">Weitere Informationen finden Sie unter [sicherheitspauschere Aushandlung](security-blanket-negotiation.md).</span><span class="sxs-lookup"><span data-stu-id="f4de0-117">For more information, see [Security Blanket Negotiation](security-blanket-negotiation.md).</span></span><br/>                                                                                           |



## <a name="remarks"></a><span data-ttu-id="f4de0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f4de0-118">Remarks</span></span>

<span data-ttu-id="f4de0-119">Diese Konstanten werden von Methoden der [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) -Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="f4de0-119">These constants are used by methods of the [**IClientSecurity**](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity) interface.</span></span> <span data-ttu-id="f4de0-120">Sie werden in der [**einzigen \_ Authentifizierungs \_ Dienst**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) Struktur verwendet, die von der [**coqueryauthenticationservices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) -Funktion abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="f4de0-120">They are used in the [**SOLE\_AUTHENTICATION\_SERVICE**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service) structure, which is retrieved by the [**CoQueryAuthenticationServices**](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices) function.</span></span> <span data-ttu-id="f4de0-121">Sie werden auch in der [**einzigen \_ Authentifizierungs \_ Informations**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) Struktur verwendet, die wiederum Mitglied der [**einzigen \_ Authentifizierungs \_ Listen**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) Struktur ist.</span><span class="sxs-lookup"><span data-stu-id="f4de0-121">They are also used in the [**SOLE\_AUTHENTICATION\_INFO**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info) structure, which in turn is a member of the [**SOLE\_AUTHENTICATION\_LIST**](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_list) structure.</span></span> <span data-ttu-id="f4de0-122">Diese Struktur, bei der es sich um eine Liste der Authentifizierungsdienste, die von Ihnen ausgeführten Autorisierungs Dienste und die Authentifizierungsinformationen für jeden Dienst handelt, wird an die [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) -Funktion und die [**IClientSecurity:: setblanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) -Methode übermittelt.</span><span class="sxs-lookup"><span data-stu-id="f4de0-122">This structure, which is a list of authentication services, the authorization services they perform, and the authentication information for each service, is passed to the [**CoInitializeSecurity**](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity) function and the [**IClientSecurity::SetBlanket**](/windows/win32/api/objidl/nf-objidl-iclientsecurity-setblanket) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="f4de0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f4de0-123">Requirements</span></span>



| <span data-ttu-id="f4de0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f4de0-124">Requirement</span></span> | <span data-ttu-id="f4de0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f4de0-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f4de0-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f4de0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f4de0-127">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4de0-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="f4de0-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f4de0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f4de0-129">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f4de0-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f4de0-130">Header</span><span class="sxs-lookup"><span data-stu-id="f4de0-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="f4de0-131"><dt>Rpcdce. h</dt></span><span class="sxs-lookup"><span data-stu-id="f4de0-131"><dt>RpcDce.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f4de0-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f4de0-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f4de0-133">**CoInitializeSecurity**</span><span class="sxs-lookup"><span data-stu-id="f4de0-133">**CoInitializeSecurity**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coinitializesecurity)
</dt> <dt>

[<span data-ttu-id="f4de0-134">**Coqueryauthenticationservices**</span><span class="sxs-lookup"><span data-stu-id="f4de0-134">**CoQueryAuthenticationServices**</span></span>](/windows/desktop/api/combaseapi/nf-combaseapi-coqueryauthenticationservices)
</dt> <dt>

[<span data-ttu-id="f4de0-135">**IClientSecurity**</span><span class="sxs-lookup"><span data-stu-id="f4de0-135">**IClientSecurity**</span></span>](/windows/desktop/api/ObjIdl/nn-objidl-iclientsecurity)
</dt> <dt>

[<span data-ttu-id="f4de0-136">**Informationen zur alleinigen \_ Authentifizierung \_**</span><span class="sxs-lookup"><span data-stu-id="f4de0-136">**SOLE\_AUTHENTICATION\_INFO**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_info)
</dt> <dt>

[<span data-ttu-id="f4de0-137">**einziger \_ Authentifizierungs \_ Dienst**</span><span class="sxs-lookup"><span data-stu-id="f4de0-137">**SOLE\_AUTHENTICATION\_SERVICE**</span></span>](/windows/win32/api/objidlbase/ns-objidlbase-sole_authentication_service)
</dt> </dl>

 

