---
description: Ändert die Einstellungsdaten für den Dienst.
ms.assetid: 1CA49922-894D-4AA1-B741-6A0DC9F5654E
title: Modifyservicesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e93d86c454de4f214c72a6ed95a414d184419c80
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103867059"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="20fd8-103">Modifyservicesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="20fd8-103">ModifyServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="20fd8-104">Ändert die Einstellungsdaten für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="20fd8-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="20fd8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="20fd8-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="20fd8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="20fd8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="20fd8-107">*SettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="20fd8-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="20fd8-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="20fd8-108">Type: **string**</span></span>

<span data-ttu-id="20fd8-109">Eine eingebettete Instanz der [**MSVM \_ virtualsystemmanagementservicesettingdata**](msvm-virtualsystemmanagementservicesettingdata.md) -Klasse, die die geänderten Aspekte des vorhandenen Dienstanbieter enthält.</span><span class="sxs-lookup"><span data-stu-id="20fd8-109">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the modified aspects of the existing service.</span></span>

</dd> <dt>

<span data-ttu-id="20fd8-110">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="20fd8-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="20fd8-111">Typ: **[ **CIM \_ bettejob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="20fd8-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="20fd8-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="20fd8-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="20fd8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="20fd8-113">Return value</span></span>

<span data-ttu-id="20fd8-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="20fd8-114">Type: **uint32**</span></span>

<span data-ttu-id="20fd8-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="20fd8-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="20fd8-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="20fd8-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-117">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="20fd8-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="20fd8-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="20fd8-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="20fd8-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="20fd8-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="20fd8-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="20fd8-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="20fd8-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="20fd8-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="20fd8-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="20fd8-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="20fd8-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="20fd8-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="20fd8-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="20fd8-129">Remarks</span></span>

<span data-ttu-id="20fd8-130">Der Zugriff auf die [**MSVM \_ virtualsystemmanagementservice**](msvm-virtualsystemmanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="20fd8-130">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="20fd8-131">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="20fd8-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="20fd8-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="20fd8-132">Requirements</span></span>



| <span data-ttu-id="20fd8-133">Anforderung</span><span class="sxs-lookup"><span data-stu-id="20fd8-133">Requirement</span></span> | <span data-ttu-id="20fd8-134">Wert</span><span class="sxs-lookup"><span data-stu-id="20fd8-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="20fd8-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="20fd8-135">Minimum supported client</span></span><br/> | <span data-ttu-id="20fd8-136">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20fd8-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="20fd8-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="20fd8-137">Minimum supported server</span></span><br/> | <span data-ttu-id="20fd8-138">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="20fd8-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="20fd8-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="20fd8-139">Namespace</span></span><br/>                | <span data-ttu-id="20fd8-140">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="20fd8-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="20fd8-141">MOF</span><span class="sxs-lookup"><span data-stu-id="20fd8-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="20fd8-142"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="20fd8-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="20fd8-143">DLL</span><span class="sxs-lookup"><span data-stu-id="20fd8-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="20fd8-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="20fd8-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="20fd8-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20fd8-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20fd8-146">**Modifyservicesettings (v1)**</span><span class="sxs-lookup"><span data-stu-id="20fd8-146">**ModifyServiceSettings (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyservicesettings-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="20fd8-147">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="20fd8-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="20fd8-148">[**CIM- \_ concretejob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="20fd8-148">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> </dl>

 

