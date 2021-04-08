---
title: Connections-Struktur (napforcementclient. h)
description: Enthält Informationen über die Liste der Verbindungen, die von einem-Enforcer verwaltet werden.
ms.assetid: 79466099-b567-4268-b9bf-d5e57f4d4900
keywords:
- Verbindungs Struktur-NAP
topic_type:
- apiref
api_name:
- Connections
api_location:
- NapEnforcementClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5e79add74830dfa8ca77fa24a5d3233542a7e553
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957233"
---
# <a name="connections-structure"></a><span data-ttu-id="37cd4-104">Verbindungs Struktur</span><span class="sxs-lookup"><span data-stu-id="37cd4-104">Connections structure</span></span>

> [!Note]  
> <span data-ttu-id="37cd4-105">Die Netzwerk Zugriffsschutz-Plattform ist ab Windows 10 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="37cd4-105">The Network Access Protection platform is not available starting with Windows 10</span></span>

 

<span data-ttu-id="37cd4-106">Die **Connections** -Struktur enthält Informationen über die Liste der Verbindungen, die von einem-Enforcer verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="37cd4-106">The **Connections** structure contains information about the list of connections maintained by an enforcer.</span></span>

## <a name="syntax"></a><span data-ttu-id="37cd4-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="37cd4-107">Syntax</span></span>


```C++
typedef struct tagConnections {
  UINT16                          count;
  INapEnforcementClientConnection **connections;
} Connections;
```



## <a name="members"></a><span data-ttu-id="37cd4-108">Member</span><span class="sxs-lookup"><span data-stu-id="37cd4-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="37cd4-109">**count**</span><span class="sxs-lookup"><span data-stu-id="37cd4-109">**count**</span></span>
</dt> <dd>

<span data-ttu-id="37cd4-110">Die Anzahl der aktiven Verbindungen, die zurzeit von einem-Enforcer innerhalb des Bereichs 0 (null) bis [**maxconnectionzähltperenforcer**](nap-type-constants.md)verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="37cd4-110">The number of active connections currently maintained by an enforcer within the range 0 (zero) to [**maxConnectionCountPerEnforcer**](nap-type-constants.md).</span></span>

</dd> <dt>

<span data-ttu-id="37cd4-111">**connections**</span><span class="sxs-lookup"><span data-stu-id="37cd4-111">**connections**</span></span>
</dt> <dd>

<span data-ttu-id="37cd4-112">Ein com-Zeiger auf eine Liste von [**inapenforcementclientconnection**](inapenforcementclientconnection.md) -Schnittstellen, die Clientverbindungen darstellen.</span><span class="sxs-lookup"><span data-stu-id="37cd4-112">A COM pointer to a list of [**INapEnforcementClientConnection**](inapenforcementclientconnection.md) interfaces that represent client connections.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="37cd4-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="37cd4-113">Requirements</span></span>



| <span data-ttu-id="37cd4-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="37cd4-114">Requirement</span></span> | <span data-ttu-id="37cd4-115">Wert</span><span class="sxs-lookup"><span data-stu-id="37cd4-115">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37cd4-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="37cd4-116">Minimum supported client</span></span><br/> | <span data-ttu-id="37cd4-117">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37cd4-117">Windows Vista \[desktop apps only\]</span></span><br/>                                                      |
| <span data-ttu-id="37cd4-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="37cd4-118">Minimum supported server</span></span><br/> | <span data-ttu-id="37cd4-119">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="37cd4-119">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="37cd4-120">Header</span><span class="sxs-lookup"><span data-stu-id="37cd4-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="37cd4-121"><dt>Napforcementclient. h</dt></span><span class="sxs-lookup"><span data-stu-id="37cd4-121"><dt>NapEnforcementClient.h</dt></span></span> </dl>   |
| <span data-ttu-id="37cd4-122">IDL</span><span class="sxs-lookup"><span data-stu-id="37cd4-122">IDL</span></span><br/>                      | <dl> <span data-ttu-id="37cd4-123"><dt>Napforcementclient. idl</dt></span><span class="sxs-lookup"><span data-stu-id="37cd4-123"><dt>NapEnforcementClient.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37cd4-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="37cd4-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37cd4-125">NAP-Referenz</span><span class="sxs-lookup"><span data-stu-id="37cd4-125">NAP Reference</span></span>](nap-reference.md)
</dt> <dt>

[<span data-ttu-id="37cd4-126">NAP-Strukturen</span><span class="sxs-lookup"><span data-stu-id="37cd4-126">NAP Structures</span></span>](nap-structures.md)
</dt> <dt>

[<span data-ttu-id="37cd4-127">**Inapenforcementclientconnection**</span><span class="sxs-lookup"><span data-stu-id="37cd4-127">**INapEnforcementClientConnection**</span></span>](inapenforcementclientconnection.md)
</dt> </dl>

 

 





