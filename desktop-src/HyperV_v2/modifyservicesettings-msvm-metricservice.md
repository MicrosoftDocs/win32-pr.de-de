---
description: 'ModifyServiceSettings-Methode der Msvm_MetricService Klasse: Ändert die Einstellungsdaten für den Dienst.'
ms.assetid: E6133DA7-A137-42FA-A523-5B93E9C6DB79
title: ModifyServiceSettings-Methode der Msvm_MetricService Klasse
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
ms.openlocfilehash: 088aec001dd63de7344256fd9e114b6ff73e4425
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108112178"
---
# <a name="modifyservicesettings-method-of-the-msvm_metricservice-class"></a><span data-ttu-id="ed828-103">ModifyServiceSettings-Methode der Msvm \_ MetricService-Klasse</span><span class="sxs-lookup"><span data-stu-id="ed828-103">ModifyServiceSettings method of the Msvm\_MetricService class</span></span>

<span data-ttu-id="ed828-104">Ändert die Einstellungsdaten für den Dienst.</span><span class="sxs-lookup"><span data-stu-id="ed828-104">Modifies the setting data for the service.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed828-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ed828-105">Syntax</span></span>


```mof
uint32 ModifyServiceSettings(
  [in]  string              SettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="ed828-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ed828-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ed828-107">*SettingData* \[ In\]</span><span class="sxs-lookup"><span data-stu-id="ed828-107">*SettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ed828-108">Enthält eine eingebettete Instanz der [**Msvm \_ MetricServiceSettingData-Klasse,**](msvm-metricservicesettingdata.md) die die geänderten Einstellungsdaten für den Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="ed828-108">Contains an embedded instance of the [**Msvm\_MetricServiceSettingData**](msvm-metricservicesettingdata.md) class that contains the modified setting data for the service.</span></span>

</dd> <dt>

<span data-ttu-id="ed828-109">*Auftrag* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="ed828-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ed828-110">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ ConcreteJob abgeleitet wurde.**](/previous-versions//cc136808(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="ed828-110">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ed828-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ed828-111">Return value</span></span>

<span data-ttu-id="ed828-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="ed828-112">This method returns one of the following values.</span></span>



| <span data-ttu-id="ed828-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="ed828-113">Return code/value</span></span>                                                                                                                                                                | <span data-ttu-id="ed828-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed828-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="ed828-115"><dt>**Abgeschlossen ohne Fehler**</dt> <dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-115"><dt>**Completed with No Error**</dt> <dt>0</dt></span></span> </dl>                    | <span data-ttu-id="ed828-116">Erfolg.</span><span class="sxs-lookup"><span data-stu-id="ed828-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="ed828-117"><dt>**Überprüfte Methodenparameter – Auftrag gestartet**</dt> <dt>4096</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-117"><dt>**Method Parameters Checked - Job Started**</dt> <dt>4096</dt></span></span> </dl> | <span data-ttu-id="ed828-118">Methodenparameter überprüft, Auftrag gestartet.</span><span class="sxs-lookup"><span data-stu-id="ed828-118">Method parameters checked, job started.</span></span><br/> |
| <dl> <span data-ttu-id="ed828-119"><dt>**Fehler**</dt> <dt>32768</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-119"><dt>**Failed**</dt> <dt>32768</dt></span></span> </dl>                                 | <span data-ttu-id="ed828-120">Fehler.</span><span class="sxs-lookup"><span data-stu-id="ed828-120">Failed.</span></span><br/>                                 |
| <dl> <span data-ttu-id="ed828-121"><dt>**Zugriff verweigert**</dt> <dt>32769</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-121"><dt>**Access Denied**</dt> <dt>32769</dt></span></span> </dl>                          | <span data-ttu-id="ed828-122">Der Zugriff wurde verweigert.</span><span class="sxs-lookup"><span data-stu-id="ed828-122">Access denied.</span></span><br/>                          |
| <dl> <span data-ttu-id="ed828-123"><dt>**Nicht unterstützt**</dt> <dt>32770</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-123"><dt>**Not Supported**</dt> <dt>32770</dt></span></span> </dl>                          | <span data-ttu-id="ed828-124">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ed828-124">Not supported.</span></span><br/>                          |
| <dl> <span data-ttu-id="ed828-125"><dt>**Der Status ist unbekannt**</dt> <dt>32771.</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-125"><dt>**Status is unknown**</dt> <dt>32771</dt></span></span> </dl>                      | <span data-ttu-id="ed828-126">Der Status ist unbekannt.</span><span class="sxs-lookup"><span data-stu-id="ed828-126">Status is unknown.</span></span><br/>                      |
| <dl> <span data-ttu-id="ed828-127"><dt>**Timeout**</dt> <dt>32772</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-127"><dt>**Timeout**</dt> <dt>32772</dt></span></span> </dl>                                | <span data-ttu-id="ed828-128">Time out.</span><span class="sxs-lookup"><span data-stu-id="ed828-128">Time-out.</span></span><br/>                               |
| <dl> <span data-ttu-id="ed828-129"><dt>**Ungültiger Parameter**</dt> <dt>32773</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-129"><dt>**Invalid parameter**</dt> <dt>32773</dt></span></span> </dl>                      | <span data-ttu-id="ed828-130">Ungültiger Parameter.</span><span class="sxs-lookup"><span data-stu-id="ed828-130">Invalid parameter.</span></span><br/>                      |
| <dl> <span data-ttu-id="ed828-131"><dt>**System wird verwendet**</dt> <dt>32774</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-131"><dt>**System is in use**</dt> <dt>32774</dt></span></span> </dl>                       | <span data-ttu-id="ed828-132">Das System wird verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed828-132">System is in use.</span></span><br/>                       |
| <dl> <span data-ttu-id="ed828-133"><dt>**Ungültiger Zustand für diesen Vorgang**</dt> <dt>32775</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-133"><dt>**Invalid state for this operation**</dt> <dt>32775</dt></span></span> </dl>       | <span data-ttu-id="ed828-134">Ungültiger Zustand für diesen Vorgang.</span><span class="sxs-lookup"><span data-stu-id="ed828-134">Invalid state for this operation.</span></span><br/>       |
| <dl> <span data-ttu-id="ed828-135"><dt>**Falscher Datentyp**</dt> <dt>32776</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-135"><dt>**Incorrect data type**</dt> <dt>32776</dt></span></span> </dl>                    | <span data-ttu-id="ed828-136">Falscher Datentyp.</span><span class="sxs-lookup"><span data-stu-id="ed828-136">Incorrect data type.</span></span><br/>                    |
| <dl> <span data-ttu-id="ed828-137"><dt>**System ist nicht verfügbar**</dt> <dt>32777</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-137"><dt>**System is not available**</dt> <dt>32777</dt></span></span> </dl>                | <span data-ttu-id="ed828-138">Das System ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ed828-138">System is not available.</span></span><br/>                |
| <dl> <span data-ttu-id="ed828-139"><dt>**Nicht genügend Arbeitsspeicher**</dt> <dt>32778</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-139"><dt>**Out of memory**</dt> <dt>32778</dt></span></span> </dl>                          | <span data-ttu-id="ed828-140">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="ed828-140">Out of memory.</span></span><br/>                          |



 

## <a name="requirements"></a><span data-ttu-id="ed828-141">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed828-141">Requirements</span></span>



| <span data-ttu-id="ed828-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ed828-142">Requirement</span></span> | <span data-ttu-id="ed828-143">Wert</span><span class="sxs-lookup"><span data-stu-id="ed828-143">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed828-144">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ed828-144">Minimum supported client</span></span><br/> | <span data-ttu-id="ed828-145">nur Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed828-145">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="ed828-146">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ed828-146">Minimum supported server</span></span><br/> | <span data-ttu-id="ed828-147">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ed828-147">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ed828-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="ed828-148">Namespace</span></span><br/>                | <span data-ttu-id="ed828-149">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="ed828-149">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="ed828-150">MOF</span><span class="sxs-lookup"><span data-stu-id="ed828-150">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ed828-151"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-151"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ed828-152">DLL</span><span class="sxs-lookup"><span data-stu-id="ed828-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ed828-153"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ed828-153"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ed828-154">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ed828-154">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed828-155">**Msvm \_ MetricService**</span><span class="sxs-lookup"><span data-stu-id="ed828-155">**Msvm\_MetricService**</span></span>](msvm-metricservice.md)
</dt> </dl>

 

