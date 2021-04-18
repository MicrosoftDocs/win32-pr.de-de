---
title: Setloadbalancingstate-Methode der Win32_TSSessionDirectory-Klasse
description: Legt den Wert fest, mit dem angegeben wird, ob der Server am Remotedesktopverbindung Broker-Lastenausgleich (RD-Verbindungsbroker) beteiligt ist.
ms.assetid: 6368043c-1808-4757-9756-10b3800190b0
ms.tgt_platform: multiple
keywords:
- Setloadbalancingstate-Methode Remotedesktopdienste
- Setloadbalancingstate-Methode Remotedesktopdienste, Win32_TSSessionDirectory-Klasse
- Win32_TSSessionDirectory-Klasse Remotedesktopdienste, setloadbalancingstate-Methode
topic_type:
- apiref
api_name:
- Win32_TSSessionDirectory.SetLoadBalancingState
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88142f5a9c87b4af2688e06d2766ac38d7e234c0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341371"
---
# <a name="setloadbalancingstate-method-of-the-win32_tssessiondirectory-class"></a><span data-ttu-id="1ce2a-106">Setloadbalancingstate-Methode der Win32- \_ Klasse "tssessiondirectory"</span><span class="sxs-lookup"><span data-stu-id="1ce2a-106">SetLoadBalancingState method of the Win32\_TSSessionDirectory class</span></span>

<span data-ttu-id="1ce2a-107">Legt den Wert fest, mit dem angegeben wird, ob der Server am Remotedesktopverbindung Broker-Lastenausgleich (RD-Verbindungsbroker) beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="1ce2a-107">Sets the value to indicate whether the server will participate in Remote Desktop Connection Broker (RD Connection Broker) load balancing.</span></span>

## <a name="syntax"></a><span data-ttu-id="1ce2a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1ce2a-108">Syntax</span></span>


```mof
uint32 SetLoadBalancingState(
  [in] uint32 StateValue
);
```



## <a name="parameters"></a><span data-ttu-id="1ce2a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1ce2a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1ce2a-110">*Status* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="1ce2a-110">*StateValue* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1ce2a-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1ce2a-111">Type: **uint32**</span></span>

<span data-ttu-id="1ce2a-112">Gibt an, ob der Server an RD-Verbindungsbroker Lastenausgleich beteiligt ist.</span><span class="sxs-lookup"><span data-stu-id="1ce2a-112">Indicates whether the server will participate in RD Connection Broker load balancing.</span></span>

<dt>

<span data-ttu-id="1ce2a-113">0</span><span class="sxs-lookup"><span data-stu-id="1ce2a-113">0</span></span>
</dt> <dd>

<span data-ttu-id="1ce2a-114">Der Server wird nicht an RD-Verbindungsbroker Lastenausgleich beteiligt.</span><span class="sxs-lookup"><span data-stu-id="1ce2a-114">The server will not participate in RD Connection Broker load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="1ce2a-115">1</span><span class="sxs-lookup"><span data-stu-id="1ce2a-115">1</span></span>
</dt> <dd>

<span data-ttu-id="1ce2a-116">Der Server wird an RD-Verbindungsbroker Lastenausgleich beteiligt.</span><span class="sxs-lookup"><span data-stu-id="1ce2a-116">The server will participate in RD Connection Broker load balancing.</span></span>

</dd> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1ce2a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1ce2a-117">Remarks</span></span>

<span data-ttu-id="1ce2a-118">Der Server muss in RD-Verbindungsbroker einer Farm hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1ce2a-118">The server must be joined to a farm in RD Connection Broker.</span></span>

<span data-ttu-id="1ce2a-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="1ce2a-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1ce2a-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="1ce2a-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="1ce2a-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1ce2a-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1ce2a-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="1ce2a-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="1ce2a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1ce2a-123">Requirements</span></span>



| <span data-ttu-id="1ce2a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1ce2a-124">Requirement</span></span> | <span data-ttu-id="1ce2a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1ce2a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1ce2a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1ce2a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1ce2a-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="1ce2a-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="1ce2a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1ce2a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1ce2a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1ce2a-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1ce2a-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ce2a-130">Namespace</span></span><br/>                | <span data-ttu-id="1ce2a-131">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="1ce2a-131">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="1ce2a-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1ce2a-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1ce2a-133"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1ce2a-133"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="1ce2a-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1ce2a-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1ce2a-135"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1ce2a-135"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1ce2a-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ce2a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1ce2a-137">**Win32- \_ tssessiondirectory**</span><span class="sxs-lookup"><span data-stu-id="1ce2a-137">**Win32\_TSSessionDirectory**</span></span>](win32-tssessiondirectory.md)
</dt> </dl>

 

