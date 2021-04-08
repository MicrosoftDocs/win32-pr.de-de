---
description: Fügt der Konfiguration eines Ethernet-Switchports Funktionseinstellungen hinzu.
ms.assetid: 628a6546-cc78-4fde-be0c-533a2c3f9483
title: Addfeaturesettings-Methode der Msvm_VirtualEthernetSwitchManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualEthernetSwitchManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e3b46a26d3c67f5efce4944c8b2e874febced32e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959807"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualethernetswitchmanagementservice-class"></a><span data-ttu-id="499df-103">Addfeaturesettings-Methode der MSVM \_ virtualethernezwitchmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="499df-103">AddFeatureSettings method of the Msvm\_VirtualEthernetSwitchManagementService class</span></span>

<span data-ttu-id="499df-104">Fügt der Konfiguration eines Ethernet-Switchports Funktionseinstellungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="499df-104">Adds feature settings to the configuration of an Ethernet switch port.</span></span>

## <a name="syntax"></a><span data-ttu-id="499df-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="499df-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  CIM_SettingData         REF AffectedConfiguration,
  [in]  string                      FeatureSettings[],
  [out] Msvm_FeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob         REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="499df-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="499df-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="499df-107">*Affectedconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="499df-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499df-108">Ein Verweis auf eine von [**CIM \_ SettingData**](/previous-versions//cc136911(v=vs.85)) abgeleitete Klasse, die den betroffenen Ethernet-Switchport oder die Konfiguration des Ethernet-Switchs darstellt.</span><span class="sxs-lookup"><span data-stu-id="499df-108">A reference to a [**CIM\_SettingData**](/previous-versions//cc136911(v=vs.85)) derived class that represents the affected Ethernet switch port or Ethernet switch configuration.</span></span>

</dd> <dt>

<span data-ttu-id="499df-109">*Featuresettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="499df-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="499df-110">Ein Array von Zeichen folgen, die eine eingebettete Instanz einer von der [**MSVM \_ featuresettingdata**](msvm-featuresettingdata.md) -Klasse abgeleiteten Klasse enthalten, die die Funktionseinstellungen beschreibt, die der switchportkonfiguration hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="499df-110">An array of strings that contain an embedded instance of a class derived from the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class, that describes the feature settings to be added to the switch port configuration.</span></span>

</dd> <dt>

<span data-ttu-id="499df-111">*Resultingfeaturesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="499df-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="499df-112">Ein Array von Verweisen auf Instanzen der [**MSVM \_ featuresettingdata**](msvm-featuresettingdata.md) -Klasse, die die hinzugefügten Funktionseinstellungen darstellen.</span><span class="sxs-lookup"><span data-stu-id="499df-112">An array of references to instances of the [**Msvm\_FeatureSettingData**](msvm-featuresettingdata.md) class that represent the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="499df-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="499df-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="499df-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="499df-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="499df-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="499df-115">Return value</span></span>

<span data-ttu-id="499df-116">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="499df-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="499df-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="499df-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="499df-118">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="499df-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="499df-119">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="499df-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="499df-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="499df-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="499df-121">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="499df-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="499df-122">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="499df-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="499df-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="499df-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="499df-124">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="499df-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="499df-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="499df-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="499df-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="499df-126">Requirements</span></span>



| <span data-ttu-id="499df-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="499df-127">Requirement</span></span> | <span data-ttu-id="499df-128">Wert</span><span class="sxs-lookup"><span data-stu-id="499df-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="499df-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="499df-129">Minimum supported client</span></span><br/> | <span data-ttu-id="499df-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="499df-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="499df-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="499df-131">Minimum supported server</span></span><br/> | <span data-ttu-id="499df-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="499df-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="499df-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="499df-133">Namespace</span></span><br/>                | <span data-ttu-id="499df-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="499df-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="499df-135">MOF</span><span class="sxs-lookup"><span data-stu-id="499df-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="499df-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="499df-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="499df-137">DLL</span><span class="sxs-lookup"><span data-stu-id="499df-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="499df-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="499df-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="499df-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="499df-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="499df-140">**Modifyfeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="499df-140">**ModifyFeatureSettings**</span></span>](modifyfeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="499df-141">**Removefeaturesettings**</span><span class="sxs-lookup"><span data-stu-id="499df-141">**RemoveFeatureSettings**</span></span>](removefeaturesettings-msvm-virtualethernetswitchmanagementservice.md)
</dt> <dt>

[<span data-ttu-id="499df-142">**MSVM \_ virtualethernetzwitchmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="499df-142">**Msvm\_VirtualEthernetSwitchManagementService**</span></span>](msvm-virtualethernetswitchmanagementservice.md)
</dt> </dl>

 

