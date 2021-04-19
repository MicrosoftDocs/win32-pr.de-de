---
description: Setzt die virtuelle Tastatur zurück.
ms.assetid: 6D4A9F02-53BD-47C2-9C09-F22C3630312F
title: Reset-Methode der Msvm_Keyboard-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Keyboard.Reset
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 4fe46657177789e49b49ec2c36f0e7a9dc95394f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349684"
---
# <a name="reset-method-of-the-msvm_keyboard-class"></a><span data-ttu-id="2a112-103">Reset-Methode der MSVM- \_ Tastatur Klasse</span><span class="sxs-lookup"><span data-stu-id="2a112-103">Reset method of the Msvm\_Keyboard class</span></span>

<span data-ttu-id="2a112-104">Setzt die virtuelle Tastatur zurück.</span><span class="sxs-lookup"><span data-stu-id="2a112-104">Resets the virtual keyboard.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a112-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a112-105">Syntax</span></span>


```mof
uint32 Reset();
```



## <a name="parameters"></a><span data-ttu-id="2a112-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a112-106">Parameters</span></span>

<span data-ttu-id="2a112-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="2a112-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2a112-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a112-108">Return value</span></span>

<span data-ttu-id="2a112-109">Der Rückgabewert 0 (null) gibt den Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="2a112-109">A return value of zero indicates success.</span></span> <span data-ttu-id="2a112-110">Der Rückgabewert 1 weist auf einen Fehler hin, weil die Methode nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="2a112-110">A return value of one indicates a failure because the method is not supported.</span></span>

<dl> <dt>

<span data-ttu-id="2a112-111">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="2a112-111">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2a112-112">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="2a112-112">**Not supported** (1)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2a112-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a112-113">Requirements</span></span>



| <span data-ttu-id="2a112-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a112-114">Requirement</span></span> | <span data-ttu-id="2a112-115">Wert</span><span class="sxs-lookup"><span data-stu-id="2a112-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a112-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a112-116">Minimum supported client</span></span><br/> | <span data-ttu-id="2a112-117">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="2a112-117">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="2a112-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a112-118">Minimum supported server</span></span><br/> | <span data-ttu-id="2a112-119">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a112-119">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="2a112-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a112-120">Namespace</span></span><br/>                | <span data-ttu-id="2a112-121">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2a112-121">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2a112-122">MOF</span><span class="sxs-lookup"><span data-stu-id="2a112-122">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a112-123"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2a112-123"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a112-124">DLL</span><span class="sxs-lookup"><span data-stu-id="2a112-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a112-125"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a112-125"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2a112-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a112-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a112-127">**MSVM- \_ Tastatur**</span><span class="sxs-lookup"><span data-stu-id="2a112-127">**Msvm\_Keyboard**</span></span>](msvm-keyboard.md)
</dt> </dl>

 

 




