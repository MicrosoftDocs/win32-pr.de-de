---
description: Ändert die Einstellungsdaten für den synthetischen 3D-Dienst.
ms.assetid: 951ba829-2821-4621-800f-4e1a967b41f5
title: Modifyservicesettings-Methode der Msvm_Synthetic3DService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_Synthetic3DService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 76f6fe18dea67231c9d722352df516bf97c35ac0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485555"
---
# <a name="modifyservicesettings-method-of-the-msvm_synthetic3dservice-class"></a><span data-ttu-id="cf007-103">Modifyservicesettings-Methode der Synthetic3DService-Klasse von MSVM \_</span><span class="sxs-lookup"><span data-stu-id="cf007-103">ModifyServiceSettings method of the Msvm\_Synthetic3DService class</span></span>

<span data-ttu-id="cf007-104">Ändert die Einstellungsdaten für den synthetischen 3D-Dienst.</span><span class="sxs-lookup"><span data-stu-id="cf007-104">Modifies the setting data for the synthetic 3-D service.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf007-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf007-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="cf007-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf007-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf007-107">*SettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf007-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf007-108">Eine Zeichen folgen Darstellung der [**MSVM \_ Synthetic3DServiceSettingData**](msvm-synthetic3dservicesettingdata.md) -Klasse, die die geänderten Einstellungsdaten für den Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="cf007-108">A string representation of the [**Msvm\_Synthetic3DServiceSettingData**](msvm-synthetic3dservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="cf007-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="cf007-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="cf007-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="cf007-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf007-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf007-111">Return value</span></span>

<span data-ttu-id="cf007-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="cf007-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="cf007-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="cf007-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="cf007-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="cf007-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="cf007-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="cf007-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="cf007-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="cf007-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="cf007-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="cf007-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="cf007-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="cf007-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="cf007-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="cf007-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="cf007-125">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="cf007-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf007-126">Requirements</span></span>



| <span data-ttu-id="cf007-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf007-127">Requirement</span></span> | <span data-ttu-id="cf007-128">Wert</span><span class="sxs-lookup"><span data-stu-id="cf007-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf007-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf007-129">Minimum supported client</span></span><br/> | <span data-ttu-id="cf007-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf007-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="cf007-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf007-131">Minimum supported server</span></span><br/> | <span data-ttu-id="cf007-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="cf007-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="cf007-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf007-133">Namespace</span></span><br/>                | <span data-ttu-id="cf007-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="cf007-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="cf007-135">MOF</span><span class="sxs-lookup"><span data-stu-id="cf007-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf007-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cf007-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf007-137">DLL</span><span class="sxs-lookup"><span data-stu-id="cf007-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf007-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cf007-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cf007-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf007-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf007-140">**MSVM \_ Synthetic3DService**</span><span class="sxs-lookup"><span data-stu-id="cf007-140">**Msvm\_Synthetic3DService**</span></span>](msvm-synthetic3dservice.md)
</dt> </dl>

 

