---
description: Ändert die Einstellungsdaten für den Dienst.
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: Modifyservicesettings-Methode der Msvm_MetricService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_MetricService.ModifyServiceSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b680f5f46d99d46f99094e05db653083fd7ae952
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103752224"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="03ee8-103">Modifyservicesettings-Methode der MSVM \_ metricservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="03ee8-103">ModifyServiceSettings method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="03ee8-104">Ändert die Einstellungsdaten für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="03ee8-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="03ee8-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="03ee8-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="03ee8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="03ee8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="03ee8-107">*SettingData* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="03ee8-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="03ee8-108">Enthält eine eingebettete Instanz der [**MSVM \_ metricservicesettingdata**](msvm-metricservicesettingdata.md) -Klasse, die die geänderten Einstellungsdaten für den Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="03ee8-108">Contains an embedded instance of the [**Msvm\_MetricServiceSettingData**](msvm-metricservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="03ee8-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="03ee8-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="03ee8-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="03ee8-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="03ee8-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="03ee8-111">Return value</span></span>

<span data-ttu-id="03ee8-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="03ee8-112">This method returns one of the following values.</span></span>



| <span data-ttu-id="03ee8-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="03ee8-113">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="03ee8-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="03ee8-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="03ee8-115"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-115"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="03ee8-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="03ee8-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="03ee8-117"><dt>**Methoden Parameter aktiviert-Auftrag gestartet**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-117"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="03ee8-118">Methoden Parameter aktiviert, Auftrag wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="03ee8-118">Method parameters checked, job started.</span></span><br/> |
| <dl> <span data-ttu-id="03ee8-119"><dt></dt> Fehler <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-119"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="03ee8-120">Fehler.</span><span class="sxs-lookup"><span data-stu-id="03ee8-120">Failed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="03ee8-121"><dt>**Zugriff verweigert**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-121"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="03ee8-122">Zugriff verweigert.</span><span class="sxs-lookup"><span data-stu-id="03ee8-122">Access denied.</span></span><br/>                          |
| <dl> <span data-ttu-id="03ee8-123"><dt>**Nicht unterstützt**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-123"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="03ee8-124">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="03ee8-124">Not supported.</span></span><br/>                          |
| <dl> <span data-ttu-id="03ee8-125"><dt>**Status ist unbekannt**</dt> <dt>32771</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-125"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="03ee8-126">Der Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="03ee8-126">Status is unknown.</span></span><br/>                      |
| <dl> <span data-ttu-id="03ee8-127"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-127"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="03ee8-128">Timeout.</span><span class="sxs-lookup"><span data-stu-id="03ee8-128">Time-out.</span></span><br/>                               |
| <dl> <span data-ttu-id="03ee8-129"><dt>**Ungültiger Parameter**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-129"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="03ee8-130">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="03ee8-130">Invalid parameter.</span></span><br/>                      |
| <dl> <span data-ttu-id="03ee8-131"><dt>**System wird verwendet**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-131"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       | <span data-ttu-id="03ee8-132">Das System wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="03ee8-132">System is in use.</span></span><br/>                       |
| <dl> <span data-ttu-id="03ee8-133"><dt>**Ungültiger Status für diesen Vorgang**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-133"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="03ee8-134">Ungültiger Status für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="03ee8-134">Invalid state for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="03ee8-135"><dt>**Falscher Datentyp**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-135"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="03ee8-136">Falscher Datentyp.</span><span class="sxs-lookup"><span data-stu-id="03ee8-136">Incorrect data type.</span></span><br/>                    |
| <dl> <span data-ttu-id="03ee8-137"><dt>**System ist nicht verfügbar**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-137"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="03ee8-138">Das System ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="03ee8-138">System is not available.</span></span><br/>                |
| <dl> <span data-ttu-id="03ee8-139"><dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-139"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="03ee8-140">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="03ee8-140">Out of memory.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="03ee8-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="03ee8-141">Requirements</span></span>



| <span data-ttu-id="03ee8-142">Anforderung</span><span class="sxs-lookup"><span data-stu-id="03ee8-142">Requirement</span></span> | <span data-ttu-id="03ee8-143">Wert</span><span class="sxs-lookup"><span data-stu-id="03ee8-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="03ee8-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="03ee8-144">Minimum supported client</span></span><br/> | <span data-ttu-id="03ee8-145">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03ee8-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="03ee8-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="03ee8-146">Minimum supported server</span></span><br/> | <span data-ttu-id="03ee8-147">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="03ee8-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="03ee8-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="03ee8-148">Namespace</span></span><br/>                | <span data-ttu-id="03ee8-149">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="03ee8-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="03ee8-150">MOF</span><span class="sxs-lookup"><span data-stu-id="03ee8-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="03ee8-151"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="03ee8-152">DLL</span><span class="sxs-lookup"><span data-stu-id="03ee8-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="03ee8-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="03ee8-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="03ee8-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03ee8-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="03ee8-155">**MSVM \_ metricservice**</span><span class="sxs-lookup"><span data-stu-id="03ee8-155">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

