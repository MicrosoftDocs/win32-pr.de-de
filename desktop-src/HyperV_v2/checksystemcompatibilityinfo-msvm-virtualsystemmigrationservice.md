---
description: Überprüft die Kompatibilitätsinformationen auf die Kompatibilität mit dem hostingcomputersystem.
ms.assetid: 1991c58e-2d0b-4fc3-a04a-c18f358451f6
title: Checksystemcompatibilityinfo-Methode der Msvm_VirtualSystemMigrationService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemMigrationService.CheckSystemCompatibilityInfo
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e47b72c6cac6e8a6061b4560b77b82cb0b845a8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862080"
---
# <a name="checksystemcompatibilityinfo-method-of-the-msvm_virtualsystemmigrationservice-class"></a><span data-ttu-id="aef42-103">Checksystemcompatibilityinfo-Methode der MSVM \_ virtualsystemmigrationservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="aef42-103">CheckSystemCompatibilityInfo method of the Msvm\_VirtualSystemMigrationService class</span></span>

<span data-ttu-id="aef42-104">Überprüft die Kompatibilitätsinformationen auf die Kompatibilität mit dem hostingcomputersystem.</span><span class="sxs-lookup"><span data-stu-id="aef42-104">Checks the compatibility information for compatibility with the hosting computer system.</span></span>

## <a name="syntax"></a><span data-ttu-id="aef42-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="aef42-105">Syntax</span></span>


```mof
uint32 CheckSystemCompatibilityInfo(
  [in]  uint8  CompatibilityInfo[],
  [out] string Reasons[]
);
```



## <a name="parameters"></a><span data-ttu-id="aef42-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="aef42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aef42-107">*Compatibilityinfo* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="aef42-107">*CompatibilityInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aef42-108">Ein BLOB von Daten, die durch Aufrufen der [**getsystemcompatibilityinfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) -Methode auf dem hostingcomputersystem abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="aef42-108">A blob of data obtained by calling the [**GetSystemCompatibilityInfo**](getsystemcompatibilityinfo-msvm-virtualsystemmigrationservice.md) method on the hosting computer system.</span></span>

</dd> <dt>

<span data-ttu-id="aef42-109">*Gründe* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="aef42-109">*Reasons* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aef42-110">Ein Array von Zeichen folgen, das die eingebetteten Instanzen der [**MSVM- \_ Fehler**](msvm-error.md) Klasse empfängt, die Warnungen oder Fehler darstellen.</span><span class="sxs-lookup"><span data-stu-id="aef42-110">An array of strings that receives the embedded instances of the [**Msvm\_Error**](msvm-error.md) class that represent any warnings or errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aef42-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="aef42-111">Return value</span></span>

<span data-ttu-id="aef42-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="aef42-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="aef42-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="aef42-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="aef42-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="aef42-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="aef42-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="aef42-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="aef42-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="aef42-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="aef42-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="aef42-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="aef42-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="aef42-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="aef42-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="aef42-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="aef42-126">**Nicht kompatibel** (32784)</span><span class="sxs-lookup"><span data-stu-id="aef42-126">**Not compatible** (32784)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="aef42-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aef42-127">Requirements</span></span>



| <span data-ttu-id="aef42-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aef42-128">Requirement</span></span> | <span data-ttu-id="aef42-129">Wert</span><span class="sxs-lookup"><span data-stu-id="aef42-129">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aef42-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aef42-130">Minimum supported client</span></span><br/> | <span data-ttu-id="aef42-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aef42-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="aef42-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aef42-132">Minimum supported server</span></span><br/> | <span data-ttu-id="aef42-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aef42-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="aef42-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="aef42-134">Namespace</span></span><br/>                | <span data-ttu-id="aef42-135">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="aef42-135">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="aef42-136">MOF</span><span class="sxs-lookup"><span data-stu-id="aef42-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aef42-137"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="aef42-137"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="aef42-138">DLL</span><span class="sxs-lookup"><span data-stu-id="aef42-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aef42-139"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="aef42-139"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="aef42-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aef42-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aef42-141">**MSVM \_ virtualsystemmigrationservice**</span><span class="sxs-lookup"><span data-stu-id="aef42-141">**Msvm\_VirtualSystemMigrationService**</span></span>](msvm-virtualsystemmigrationservice.md)
</dt> </dl>

 

 




