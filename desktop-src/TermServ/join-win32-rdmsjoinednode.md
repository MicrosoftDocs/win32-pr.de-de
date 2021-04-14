---
title: Joinmethode der Win32_RDMSJoinedNode-Klasse
description: Fügt Remotedesktop Verwaltungsdienste (RDMs) einen Knoten hinzu.
ms.assetid: 7451d12a-ace2-4564-bf6d-fb0169be967f
ms.tgt_platform: multiple
keywords:
- Joinmethode Remotedesktopdienste
- Joinmethode Remotedesktopdienste, Win32_RDMSJoinedNode-Klasse
- Win32_RDMSJoinedNode-Klasse Remotedesktopdienste, Join-Methode
topic_type:
- apiref
api_name:
- Win32_RDMSJoinedNode.Join
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 587e68758971453e8c4e307ccb37ce6cede262f7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391660"
---
# <a name="join-method-of-the-win32_rdmsjoinednode-class"></a><span data-ttu-id="89c2e-106">Joinmethode der Win32 \_ rdmsjoinednode-Klasse</span><span class="sxs-lookup"><span data-stu-id="89c2e-106">Join method of the Win32\_RDMSJoinedNode class</span></span>

<span data-ttu-id="89c2e-107">Fügt Remotedesktop Verwaltungsdienste (RDMs) einen Knoten hinzu.</span><span class="sxs-lookup"><span data-stu-id="89c2e-107">Adds a node to Remote Desktop Management Services (RDMS).</span></span>

## <a name="syntax"></a><span data-ttu-id="89c2e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="89c2e-108">Syntax</span></span>


```mof
uint32 Join(
  [in] string NodeFQDN,
  [in] string NodeSID
);
```



## <a name="parameters"></a><span data-ttu-id="89c2e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="89c2e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="89c2e-110">*Nodefqdn* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89c2e-110">*NodeFQDN* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c2e-111">Der voll qualifizierte Domänen Name des Knotens.</span><span class="sxs-lookup"><span data-stu-id="89c2e-111">The fully qualified domain name of the node.</span></span>

</dd> <dt>

<span data-ttu-id="89c2e-112">*Nodesid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="89c2e-112">*NodeSID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="89c2e-113">Die Sicherheits-ID (SID) des Knotens.</span><span class="sxs-lookup"><span data-stu-id="89c2e-113">The security identifier (SID) of the node.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="89c2e-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="89c2e-114">Return value</span></span>

<span data-ttu-id="89c2e-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="89c2e-115">Returns 0 on success, otherwise returns a WMI error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="89c2e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="89c2e-116">Requirements</span></span>



| <span data-ttu-id="89c2e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="89c2e-117">Requirement</span></span> | <span data-ttu-id="89c2e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="89c2e-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="89c2e-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="89c2e-119">Minimum supported client</span></span><br/> | <span data-ttu-id="89c2e-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="89c2e-120">None supported</span></span><br/>                                                                   |
| <span data-ttu-id="89c2e-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="89c2e-121">Minimum supported server</span></span><br/> | <span data-ttu-id="89c2e-122">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="89c2e-122">Windows Server 2012</span></span><br/>                                                              |
| <span data-ttu-id="89c2e-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="89c2e-123">Namespace</span></span><br/>                | <span data-ttu-id="89c2e-124">Root \\ CIMv2 \\ RDMs</span><span class="sxs-lookup"><span data-stu-id="89c2e-124">Root\\CIMv2\\rdms</span></span><br/>                                                                |
| <span data-ttu-id="89c2e-125">MOF</span><span class="sxs-lookup"><span data-stu-id="89c2e-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="89c2e-126"><dt>Rdmanagement. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="89c2e-126"><dt>RDManagement.mof</dt></span></span> </dl> |
| <span data-ttu-id="89c2e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="89c2e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="89c2e-128"><dt>RDMS.dll</dt></span><span class="sxs-lookup"><span data-stu-id="89c2e-128"><dt>RDMS.dll</dt></span></span> </dl>         |



## <a name="see-also"></a><span data-ttu-id="89c2e-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="89c2e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="89c2e-130">**Win32 \_ rdmsjoinednode**</span><span class="sxs-lookup"><span data-stu-id="89c2e-130">**Win32\_RDMSJoinedNode**</span></span>](win32-rdmsjoinednode.md)
</dt> </dl>

 

 





