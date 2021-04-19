---
title: Getjoinednodecount-Methode der Win32_RDMSJoinedNode-Klasse
description: Gibt die Anzahl der Server an, auf denen die angegebenen Rollen installiert sind.
ms.assetid: ed2ae0b5-5cbc-4c11-a2ad-065f88dd5842
ms.tgt_platform: multiple
keywords:
- Getjoinednodecount-Methode Remotedesktopdienste
- Getjoinednodecount-Methode Remotedesktopdienste, Win32_RDMSJoinedNode-Klasse
- Win32_RDMSJoinedNode-Klasse Remotedesktopdienste, getjoinednodecount-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.GetJoinedNodeCount
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73ecc5c388814873aa690e9af5adda5081aad4d6
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337925"
---
# <a name="getjoinednodecount-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="75434-106">Getjoinednodecount-Methode der Win32 \_ rdmsjoinednode-Klasse</span><span class="sxs-lookup"><span data-stu-id="75434-106">GetJoinedNodeCount method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="75434-107">Gibt die Anzahl der Server an, auf denen die angegebenen Rollen installiert sind.</span><span class="sxs-lookup"><span data-stu-id="75434-107">Get number of servers that have the specified roles installed.</span></span>

## <a name="syntax"></a><span data-ttu-id="75434-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="75434-108">Syntax</span></span>


```mof
uint32 GetJoinedNodeCount(
  [in]  uint32 roleType,
  [out] uint32 Count
);
```



## <a name="parameters"></a><span data-ttu-id="75434-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="75434-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75434-110">*RoleType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="75434-110">*roleType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75434-111">Ein Bitfeld, das die Rollen Typen angibt.</span><span class="sxs-lookup"><span data-stu-id="75434-111">A bitfield that specifies the role types.</span></span>

<dt>

<span data-ttu-id="75434-112">0</span><span class="sxs-lookup"><span data-stu-id="75434-112">0</span></span>
</dt> <dd>

<span data-ttu-id="75434-113">All</span><span class="sxs-lookup"><span data-stu-id="75434-113">All</span></span>

</dd> <dt>

<span data-ttu-id="75434-114">1</span><span class="sxs-lookup"><span data-stu-id="75434-114">1</span></span>
</dt> <dd>

<span data-ttu-id="75434-115">Remotedesktopverbindung Broker (RDCB)</span><span class="sxs-lookup"><span data-stu-id="75434-115">Remote Desktop Connection Broker (RDCB)</span></span>

</dd> <dt>

<span data-ttu-id="75434-116">2</span><span class="sxs-lookup"><span data-stu-id="75434-116">2</span></span>
</dt> <dd>

<span data-ttu-id="75434-117">Remotedesktop-Sitzungshost (RDSH)</span><span class="sxs-lookup"><span data-stu-id="75434-117">Remote Desktop Session Host (RDSH)</span></span>

</dd> <dt>

<span data-ttu-id="75434-118">4</span><span class="sxs-lookup"><span data-stu-id="75434-118">4</span></span>
</dt> <dd>

<span data-ttu-id="75434-119">Remotedesktop-Virtualisierungshost (RDVH)</span><span class="sxs-lookup"><span data-stu-id="75434-119">Remote Desktop Virtualization Host (RDVH)</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="75434-120">*Anzahl* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="75434-120">*Count* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75434-121">Bei Erfolg wird die Anzahl der Server mit den angegebenen installierten Rollen zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75434-121">On success, returns the number of servers with the specified roles installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75434-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="75434-122">Return value</span></span>

<span data-ttu-id="75434-123">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="75434-123">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="75434-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="75434-124">Requirements</span></span>



| <span data-ttu-id="75434-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="75434-125">Requirement</span></span> | <span data-ttu-id="75434-126">Wert</span><span class="sxs-lookup"><span data-stu-id="75434-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="75434-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="75434-127">Minimum supported client</span></span><br/> | <span data-ttu-id="75434-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="75434-128">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="75434-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="75434-129">Minimum supported server</span></span><br/> | <span data-ttu-id="75434-130">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="75434-130">Windows Server 2016</span></span><br/>                                                              |
| <span data-ttu-id="75434-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="75434-131">Namespace</span></span><br/>                | <span data-ttu-id="75434-132">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="75434-132">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="75434-133">MOF</span><span class="sxs-lookup"><span data-stu-id="75434-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="75434-134"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="75434-134"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="75434-135">DLL</span><span class="sxs-lookup"><span data-stu-id="75434-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="75434-136"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="75434-136"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="75434-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75434-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75434-138">**Win32 \_ rdmsjoinednode**</span><span class="sxs-lookup"><span data-stu-id="75434-138">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





