---
title: RPC_AUTH_IDENTITY_HANDLE (rpcdce. h)
description: Der \_ \_ Datentyp des RPC \_ -Authentifizierungs Identitäts Handles deklariert ein Handle, das auf eine Struktur verweist, die die Authentifizierungs-und Autorisierungs Anmelde Informationen des Clients enthält, die für Remote Prozedur Aufrufe angegeben wurden.
ms.assetid: 06e45348-a392-45be-9f8a-e77ef887f26c
keywords:
- RPC_AUTH_IDENTITY_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e86559e7852172d34898d48f13bb2975ed792d85
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106388"
---
# <a name="rpc_auth_identity_handle"></a><span data-ttu-id="9cdd2-104">RPC-Authentifizierungs- \_ \_ Identitäts \_ handle</span><span class="sxs-lookup"><span data-stu-id="9cdd2-104">RPC\_AUTH\_IDENTITY\_HANDLE</span></span>

<span data-ttu-id="9cdd2-105">Der Datentyp des RPC-Authentifizierungs **\_ \_ Identitäts \_ Handles** deklariert ein Handle, das auf eine Struktur verweist, die die Authentifizierungs-und Autorisierungs Anmelde Informationen des Clients enthält, die für Remote Prozedur Aufrufe angegeben wurden.</span><span class="sxs-lookup"><span data-stu-id="9cdd2-105">The **RPC\_AUTH\_IDENTITY\_HANDLE** data type declares a handle that points to a structure containing the client's authentication and authorization credentials specified for remote procedure calls.</span></span>


```C++
typedef void* RPC_AUTH_IDENTITY_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="9cdd2-106">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9cdd2-106">Requirements</span></span>



| <span data-ttu-id="9cdd2-107">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9cdd2-107">Requirement</span></span> | <span data-ttu-id="9cdd2-108">Wert</span><span class="sxs-lookup"><span data-stu-id="9cdd2-108">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cdd2-109">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9cdd2-109">Minimum supported client</span></span><br/> | <span data-ttu-id="9cdd2-110">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9cdd2-110">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="9cdd2-111">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9cdd2-111">Minimum supported server</span></span><br/> | <span data-ttu-id="9cdd2-112">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="9cdd2-112">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="9cdd2-113">Header</span><span class="sxs-lookup"><span data-stu-id="9cdd2-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="9cdd2-114"><dt>Rpcdce. h (Include RPC. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9cdd2-114"><dt>Rpcdce.h (include Rpc.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9cdd2-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9cdd2-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cdd2-116">**Rpcbindinginqauthinfo**</span><span class="sxs-lookup"><span data-stu-id="9cdd2-116">**RpcBindingInqAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindinginqauthinfo)
</dt> <dt>

[<span data-ttu-id="9cdd2-117">**Rpcbindingsetauthinfo**</span><span class="sxs-lookup"><span data-stu-id="9cdd2-117">**RpcBindingSetAuthInfo**</span></span>](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcbindingsetauthinfo)
</dt> </dl>

 

 





