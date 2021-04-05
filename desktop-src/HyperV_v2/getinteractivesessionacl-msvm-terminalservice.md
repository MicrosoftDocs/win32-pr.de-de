---
description: Ruft die aktuelle DACL (diskreter Zugriffs Steuerungs Liste) ab, mit der der Zugriff auf die interaktive Sitzung eines virtuellen Computers gesteuert wird.
ms.assetid: 9b81f6d5-20fa-4277-b943-756d85359fd2
title: Getinteractivesessionacl-Methode der Msvm_TerminalService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_TerminalService.GetInteractiveSessionACL
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: f08c8514a2f65a08b4b9350b38988da8e49b4985
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752233"
---
# <a name="getinteractivesessionacl-method-of-the-msvm_terminalservice-class"></a><span data-ttu-id="c1cb3-103">Getinteractivesessionacl-Methode der MSVM \_ Terminalservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="c1cb3-103">GetInteractiveSessionACL method of the Msvm\_TerminalService class</span></span>

<span data-ttu-id="c1cb3-104">Ruft die aktuelle DACL ( *diskreter Zugriffs Steuerungs Liste* ) ab, mit der der Zugriff auf die interaktive Sitzung eines virtuellen Computers gesteuert wird.</span><span class="sxs-lookup"><span data-stu-id="c1cb3-104">Retrieves the current *discretionary access control list* (DACL) that controls access to the interactive session of a virtual machine.</span></span>

## <a name="syntax"></a><span data-ttu-id="c1cb3-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c1cb3-105">Syntax</span></span>


```mof
uint32 GetInteractiveSessionACL(
  [in]  CIM_ComputerSystem REF ComputerSystem,
  [out] string                 AccessControlList[]
);
```



## <a name="parameters"></a><span data-ttu-id="c1cb3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c1cb3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c1cb3-107">*Computersystem* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c1cb3-107">*ComputerSystem* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cb3-108">Ein Verweis auf eine Instanz der [**MSVM \_ Computersystem**](msvm-computersystem.md) -Klasse, die den virtuellen Computer darstellt, dessen DACL abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="c1cb3-108">A reference to an instance of the [**Msvm\_ComputerSystem**](msvm-computersystem.md) class that represents the virtual machine whose DACL will be retrieved.</span></span>

</dd> <dt>

<span data-ttu-id="c1cb3-109">*AccessControlList* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="c1cb3-109">*AccessControlList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c1cb3-110">Ein Array von Zeichen folgen, die jeweils eine eingebettete Instanz der [**MSVM \_ interactivesessionace**](msvm-interactivesessionace.md) -Klasse enthalten, die einen *Zugriffs Steuerungs Eintrag* (ACE) in der interaktiven Sitzungs-DACL der virtuellen Maschine darstellt.</span><span class="sxs-lookup"><span data-stu-id="c1cb3-110">An array of strings, each containing an embedded instance of the [**Msvm\_InteractiveSessionACE**](msvm-interactivesessionace.md) class that represents an *access control entry* (ACE) in the virtual machine interactive session DACL.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c1cb3-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c1cb3-111">Return value</span></span>

<span data-ttu-id="c1cb3-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="c1cb3-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="c1cb3-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="c1cb3-114">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="c1cb3-115">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="c1cb3-115">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="c1cb3-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="c1cb3-117">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-117">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="c1cb3-118">**Ungültiger Status** (5)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-118">**Invalid State** (5)</span></span>
</dt> <dt>

<span data-ttu-id="c1cb3-119">Nicht **kompatible Parameter** (6)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-119">**Incompatible Parameters** (6)</span></span>
</dt> <dt>

<span data-ttu-id="c1cb3-120">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="c1cb3-121">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-121">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="c1cb3-122">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-122">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="c1cb3-123">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-123">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="c1cb3-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c1cb3-124">Requirements</span></span>



| <span data-ttu-id="c1cb3-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c1cb3-125">Requirement</span></span> | <span data-ttu-id="c1cb3-126">Wert</span><span class="sxs-lookup"><span data-stu-id="c1cb3-126">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c1cb3-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-127">Minimum supported client</span></span><br/> | <span data-ttu-id="c1cb3-128">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1cb3-128">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="c1cb3-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c1cb3-129">Minimum supported server</span></span><br/> | <span data-ttu-id="c1cb3-130">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c1cb3-130">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c1cb3-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c1cb3-131">Namespace</span></span><br/>                | <span data-ttu-id="c1cb3-132">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="c1cb3-132">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="c1cb3-133">MOF</span><span class="sxs-lookup"><span data-stu-id="c1cb3-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c1cb3-134"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c1cb3-134"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="c1cb3-135">DLL</span><span class="sxs-lookup"><span data-stu-id="c1cb3-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c1cb3-136"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="c1cb3-136"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="c1cb3-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c1cb3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c1cb3-138">**MSVM \_ Terminalservice**</span><span class="sxs-lookup"><span data-stu-id="c1cb3-138">**Msvm\_TerminalService**</span></span>](msvm-terminalservice.md)
</dt> </dl>

 

 




