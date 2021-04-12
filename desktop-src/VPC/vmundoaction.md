---
title: Vmundoaction-Enumeration (vpccominterfaces. h)
description: Gibt an, was mit rückgängig-Laufwerken geschieht, wenn ein virtueller Computer heruntergefahren oder ausgeschaltet wird.
ms.assetid: f8f96fd3-0b2a-40ae-8b2e-b6bcc995dedd
keywords:
- Virtueller PC der vmundoaction-Enumeration
topic_type:
- apiref
api_name:
- VMUndoAction
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 10917a5fb8d00e16a28f4b175237484b977cf914
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104518905"
---
# <a name="vmundoaction-enumeration"></a><span data-ttu-id="b8ad7-104">Vmundoaction-Enumeration</span><span class="sxs-lookup"><span data-stu-id="b8ad7-104">VMUndoAction enumeration</span></span>

<span data-ttu-id="b8ad7-105">\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b8ad7-105">\[Windows Virtual PC is no longer available for use as of Windows 8.</span></span> <span data-ttu-id="b8ad7-106">Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span><span class="sxs-lookup"><span data-stu-id="b8ad7-106">Instead, use the [Hyper-V WMI provider (V2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]</span></span>

<span data-ttu-id="b8ad7-107">Gibt an, was mit rückgängig-Laufwerken geschieht, wenn ein virtueller Computer heruntergefahren oder ausgeschaltet wird.</span><span class="sxs-lookup"><span data-stu-id="b8ad7-107">Specifies what happens to undo drives when a virtual machine is shut down or turned off.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8ad7-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8ad7-108">Syntax</span></span>


```C++
typedef enum  { 
  vmUndoAction_Discard  = 0,
  vmUndoAction_Keep     = 1,
  vmUndoAction_Commit   = 2
} VMUndoAction;
```



## <a name="constants"></a><span data-ttu-id="b8ad7-109">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b8ad7-109">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b8ad7-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmundoaction \_ verwerfen**</span><span class="sxs-lookup"><span data-stu-id="b8ad7-110"><span id="vmUndoAction_Discard"></span><span id="vmundoaction_discard"></span><span id="VMUNDOACTION_DISCARD"></span>**vmUndoAction\_Discard**</span></span>
</dt> <dd>

<span data-ttu-id="b8ad7-111">Verwerfen der rückgängig-Laufwerke die übergeordneten Laufwerke bleiben unverändert.</span><span class="sxs-lookup"><span data-stu-id="b8ad7-111">Discard the undo drives; the parent drives remain unchanged.</span></span>

</dd> <dt>

<span data-ttu-id="b8ad7-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmundoaction \_ beibehalten**</span><span class="sxs-lookup"><span data-stu-id="b8ad7-112"><span id="vmUndoAction_Keep"></span><span id="vmundoaction_keep"></span><span id="VMUNDOACTION_KEEP"></span>**vmUndoAction\_Keep**</span></span>
</dt> <dd>

<span data-ttu-id="b8ad7-113">Behalten Sie die rückgängig-Laufwerke. die übergeordneten Laufwerke bleiben unverändert, Änderungen werden jedoch beim nächsten Start des virtuellen Computers beibehalten.</span><span class="sxs-lookup"><span data-stu-id="b8ad7-113">Keep the undo drives; the parent drives remain unchanged, but changes will be maintained the next time the virtual machine starts.</span></span>

</dd> <dt>

<span data-ttu-id="b8ad7-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmundoaction- \_ Commit**</span><span class="sxs-lookup"><span data-stu-id="b8ad7-114"><span id="vmUndoAction_Commit"></span><span id="vmundoaction_commit"></span><span id="VMUNDOACTION_COMMIT"></span>**vmUndoAction\_Commit**</span></span>
</dt> <dd>

<span data-ttu-id="b8ad7-115">Commit für Änderungen an den übergeordneten Laufwerken.</span><span class="sxs-lookup"><span data-stu-id="b8ad7-115">Commit changes to the parent drives.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b8ad7-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b8ad7-116">Requirements</span></span>



| <span data-ttu-id="b8ad7-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b8ad7-117">Requirement</span></span> | <span data-ttu-id="b8ad7-118">Wert</span><span class="sxs-lookup"><span data-stu-id="b8ad7-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8ad7-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b8ad7-119">Minimum supported client</span></span><br/> | <span data-ttu-id="b8ad7-120">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b8ad7-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="b8ad7-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b8ad7-121">Minimum supported server</span></span><br/> | <span data-ttu-id="b8ad7-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b8ad7-122">None supported</span></span><br/>                                                                     |
| <span data-ttu-id="b8ad7-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="b8ad7-123">End of client support</span></span><br/>    | <span data-ttu-id="b8ad7-124">Windows 7</span><span class="sxs-lookup"><span data-stu-id="b8ad7-124">Windows 7</span></span><br/>                                                                          |
| <span data-ttu-id="b8ad7-125">Produkt</span><span class="sxs-lookup"><span data-stu-id="b8ad7-125">Product</span></span><br/>                  | <span data-ttu-id="b8ad7-126">Windows Virtual PC</span><span class="sxs-lookup"><span data-stu-id="b8ad7-126">Windows Virtual PC</span></span><br/>                                                                 |
| <span data-ttu-id="b8ad7-127">Header</span><span class="sxs-lookup"><span data-stu-id="b8ad7-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="b8ad7-128"><dt>Vpccominterfaces. h</dt></span><span class="sxs-lookup"><span data-stu-id="b8ad7-128"><dt>VPCCOMInterfaces.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8ad7-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8ad7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8ad7-130">**Ivmvirtualmachine:: UndoAction**</span><span class="sxs-lookup"><span data-stu-id="b8ad7-130">**IVMVirtualMachine::UndoAction**</span></span>](ivmvirtualmachine-undoaction.md)
</dt> </dl>

 

