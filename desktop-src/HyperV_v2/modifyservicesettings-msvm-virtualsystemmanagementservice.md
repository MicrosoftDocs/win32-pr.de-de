---
description: 'ModifyServiceSettings-Methode der Msvm_VirtualSystemManagementService-Klasse: Ändert die Einstellungsdaten für den Dienst.'
ms.assetid: 1CA49922-894D-4AA1-B741-6A0DC9F5654E
title: ModifyServiceSettings-Methode der Msvm_VirtualSystemManagementService-Klasse
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
ms.openlocfilehash: ee4e8ae904292bae06770f23cf6c853d5e5448bd
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112168"
---
# <a name="modifyservicesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="f909d-103">ModifyServiceSettings-Methode der Msvm \_ VirtualSystemManagementService-Klasse</span><span class="sxs-lookup"><span data-stu-id="f909d-103">ModifyServiceSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="f909d-104">Ändert die Einstellungsdaten für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="f909d-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="f909d-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="f909d-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="f909d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f909d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f909d-107">*SettingData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="f909d-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f909d-108">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="f909d-108">Type: **string**</span></span>

<span data-ttu-id="f909d-109">Eine eingebettete Instanz der [**Msvm \_ VirtualSystemManagementServiceSettingData-Klasse,**](msvm-virtualsystemmanagementservicesettingdata.md) die die geänderten Aspekte des vorhandenen Diensts enthält.</span><span class="sxs-lookup"><span data-stu-id="f909d-109">An embedded instance of the [**Msvm\_VirtualSystemManagementServiceSettingData**](msvm-virtualsystemmanagementservicesettingdata.md) class that contains the modified aspects of the existing service.</span></span>

</dd> <dt>

<span data-ttu-id="f909d-110">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="f909d-110">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f909d-111">Typ: **[ **CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span><span class="sxs-lookup"><span data-stu-id="f909d-111">Type: **[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))**</span></span>

<span data-ttu-id="f909d-112">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein objekt, das von [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))abgeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="f909d-112">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f909d-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f909d-113">Return value</span></span>

<span data-ttu-id="f909d-114">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="f909d-114">Type: **uint32**</span></span>

<span data-ttu-id="f909d-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="f909d-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="f909d-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="f909d-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-117">**Methodenparameter überprüft** – Auftrag gestartet (4096)</span><span class="sxs-lookup"><span data-stu-id="f909d-117">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-118">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="f909d-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="f909d-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="f909d-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-121">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="f909d-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="f909d-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="f909d-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="f909d-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-125">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="f909d-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-126">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="f909d-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-127">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="f909d-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="f909d-128">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="f909d-128">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="f909d-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f909d-129">Remarks</span></span>

<span data-ttu-id="f909d-130">Der Zugriff auf die [**Msvm \_ VirtualSystemManagementService-Klasse**](msvm-virtualsystemmanagementservice.md) kann durch UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="f909d-130">Access to the [**Msvm\_VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f909d-131">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="f909d-131">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f909d-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f909d-132">Requirements</span></span>



| <span data-ttu-id="f909d-133">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f909d-133">Requirement</span></span> | <span data-ttu-id="f909d-134">Wert</span><span class="sxs-lookup"><span data-stu-id="f909d-134">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f909d-135">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f909d-135">Minimum supported client</span></span><br/> | <span data-ttu-id="f909d-136">Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f909d-136">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f909d-137">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f909d-137">Minimum supported server</span></span><br/> | <span data-ttu-id="f909d-138">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f909d-138">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f909d-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="f909d-139">Namespace</span></span><br/>                | <span data-ttu-id="f909d-140">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="f909d-140">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f909d-141">MOF</span><span class="sxs-lookup"><span data-stu-id="f909d-141">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f909d-142"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="f909d-142"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f909d-143">DLL</span><span class="sxs-lookup"><span data-stu-id="f909d-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f909d-144"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f909d-144"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f909d-145">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="f909d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f909d-146">**ModifyServiceSettings (V1)**</span><span class="sxs-lookup"><span data-stu-id="f909d-146">**ModifyServiceSettings (V1)**</span></span>](/previous-versions/windows/desktop/virtual/modifyservicesettings-msvm-virtualsystemmanagementservice)
</dt> <dt>

[<span data-ttu-id="f909d-147">**Msvm \_ VirtualSystemManagementService**</span><span class="sxs-lookup"><span data-stu-id="f909d-147">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> <dt>

<span data-ttu-id="f909d-148">[**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f909d-148">[**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85))</span></span>
</dt> </dl>

 

