---
title: Getpdingstartserverlist-Methode der Win32_RDSHServer-Klasse
description: Ruft eine Liste der Server ab, die auf den Start warten.
ms.assetid: 7af7a0e7-dc00-4e3a-8e0c-5987bd2bc3a2
ms.tgt_platform: multiple
keywords:
- Getpdingstartserverlist-Methode Remotedesktopdienste
- Getpdingstartserverlist-Methode Remotedesktopdienste, Win32_RDSHServer-Klasse
- Win32_RDSHServer-Klasse Remotedesktopdienste, getpdingstartserverlist-Methode
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetPendingStartServerList
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99b96453b33f931b18d89f13413513d3baf82bfb
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391961"
---
# <a name="getpendingstartserverlist-method-of-the-win32_rdshserver-class"></a><span data-ttu-id="9f9b8-106">Getpdingstartserverlist-Methode der Win32 \_ rdshserver-Klasse</span><span class="sxs-lookup"><span data-stu-id="9f9b8-106">GetPendingStartServerList method of the Win32\_RDSHServer class</span></span>

<span data-ttu-id="9f9b8-107">Ruft eine Liste der Server ab, die auf den Start warten.</span><span class="sxs-lookup"><span data-stu-id="9f9b8-107">Retrieves a list of server waiting to start.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f9b8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f9b8-108">Syntax</span></span>


```mof
uint32 GetPendingStartServerList(
  [in]  uint32 maxServers,
  [out] string ServerFQDNs[]
);
```



## <a name="parameters"></a><span data-ttu-id="9f9b8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9f9b8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f9b8-110">*maxservers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9f9b8-110">*maxServers* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9f9b8-111">Die maximale Anzahl von Servern, die in der Liste zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f9b8-111">The maximum number of servers to return in the list.</span></span>

</dd> <dt>

<span data-ttu-id="9f9b8-112">*Serverfqdns* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9f9b8-112">*ServerFQDNs* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9f9b8-113">Bei Erfolg enthält eine Auflistung der voll qualifizierten Domänen Namen der Server, die auf den Start warten.</span><span class="sxs-lookup"><span data-stu-id="9f9b8-113">On success, contains a collection of fully-qualified domain names of the servers waiting to start.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9f9b8-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9f9b8-114">Remarks</span></span>

<span data-ttu-id="9f9b8-115">Die Liste der Server wird nach jedem-Rückruf zurückgesetzt, sodass der nächste-Rückruf keinen doppelten Server erhält.</span><span class="sxs-lookup"><span data-stu-id="9f9b8-115">The list of servers is reset after every call, so that the next call will not get a duplicate server.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f9b8-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9f9b8-116">Requirements</span></span>



| <span data-ttu-id="9f9b8-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9f9b8-117">Requirement</span></span> | <span data-ttu-id="9f9b8-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9f9b8-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f9b8-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9f9b8-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9f9b8-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9f9b8-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="9f9b8-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9f9b8-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9f9b8-122">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="9f9b8-122">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="9f9b8-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="9f9b8-123">Namespace</span></span><br/>                | <span data-ttu-id="9f9b8-124">Root \\ CIMV2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="9f9b8-124">Root\\cimv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="9f9b8-125">MOF</span><span class="sxs-lookup"><span data-stu-id="9f9b8-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9f9b8-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9f9b8-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="9f9b8-127">DLL</span><span class="sxs-lookup"><span data-stu-id="9f9b8-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9f9b8-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9f9b8-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="9f9b8-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f9b8-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f9b8-130">**Win32- \_ rdshserver**</span><span class="sxs-lookup"><span data-stu-id="9f9b8-130">**Win32\_RDSHServer**</span></span>](win32-rdshserver.md)
</dt> </dl>

 

 





