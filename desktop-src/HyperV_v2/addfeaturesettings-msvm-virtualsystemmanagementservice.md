---
description: Fügt der Konfiguration einer Ethernet-Verbindung mit einem virtuellen Computer Ethernet-Funktionseinstellungen hinzu.
ms.assetid: f233bf2f-5201-4b02-8384-bb7e2d1e7dee
title: Addfeaturesettings-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.AddFeatureSettings
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5e9acbaaf6ff1da6439dcb243869e09133e0031e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104345559"
---
# <a name="addfeaturesettings-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="2a36b-103">Addfeaturesettings-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="2a36b-103">AddFeatureSettings method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="2a36b-104">Fügt der Konfiguration einer Ethernet-Verbindung mit einem virtuellen Computer Ethernet-Funktionseinstellungen hinzu.</span><span class="sxs-lookup"><span data-stu-id="2a36b-104">Adds Ethernet feature settings to the configuration of a virtual machine Ethernet connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a36b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a36b-105">Syntax</span></span>


```mof
uint32 AddFeatureSettings(
  [in]  Msvm_EthernetPortAllocationSettingData    REF AffectedConfiguration,
  [in]  string                                        FeatureSettings[],
  [out] Msvm_EthernetSwitchPortFeatureSettingData REF ResultingFeatureSettings[],
  [out] CIM_ConcreteJob                           REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="2a36b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a36b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a36b-107">*Affectedconfiguration* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a36b-107">*AffectedConfiguration* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a36b-108">Verweis auf eine Instanz der [**MSVM-Klasse " \_ ethernetportzuweisung**](msvm-ethernetportallocationsettingdata.md) ", die die betroffene Ethernet-Verbindung darstellt.</span><span class="sxs-lookup"><span data-stu-id="2a36b-108">Reference to an instance of the [**Msvm\_EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) class that represents the affected Ethernet connection.</span></span>

</dd> <dt>

<span data-ttu-id="2a36b-109">*Featuresettings* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="2a36b-109">*FeatureSettings* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a36b-110">Ein Array von Zeichen folgen, das eine eingebettete Instanz der [**MSVM \_ ethertesettingdata**](msvm-ethernetswitchfeaturesettingdata.md) -Klasse enthält, die die Funktionseinstellungen beschreibt, die der Verbindungs Konfiguration hinzugefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2a36b-110">An array of strings that contain one embedded instance of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchfeaturesettingdata.md) class that describes the feature settings to be added to the connection configuration.</span></span>

</dd> <dt>

<span data-ttu-id="2a36b-111">*Resultingfeaturesettings* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2a36b-111">*ResultingFeatureSettings* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a36b-112">Ein Array von Verweisen auf Instanzen der [**MSVM \_ ethertesettingdata**](msvm-ethernetswitchportfeaturesettingdata.md) -Klasse, die die hinzugefügten Funktionseinstellungen darstellt.</span><span class="sxs-lookup"><span data-stu-id="2a36b-112">An array of references to instances of the [**Msvm\_EthernetSwitchFeatureSettingData**](msvm-ethernetswitchportfeaturesettingdata.md) class that represents the added feature settings.</span></span>

</dd> <dt>

<span data-ttu-id="2a36b-113">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="2a36b-113">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a36b-114">Wenn der Vorgang asynchron ausgeführt wird, gibt diese Methode 4096 zurück, und dieser Parameter enthält einen Verweis auf ein Objekt, das von [**CIM \_ concretejob**](/previous-versions//cc136808(v=vs.85))abgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="2a36b-114">If the operation is performed asynchronously, this method will return 4096, and this parameter will contain a reference to an object derived from [**CIM\_ConcreteJob**](/previous-versions//cc136808(v=vs.85)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a36b-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="2a36b-115">Return value</span></span>

<span data-ttu-id="2a36b-116">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="2a36b-116">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="2a36b-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="2a36b-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="2a36b-118">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="2a36b-118">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="2a36b-119">Fehler **(2** )</span><span class="sxs-lookup"><span data-stu-id="2a36b-119">**Failed** (2)</span></span>
</dt> <dt>

<span data-ttu-id="2a36b-120">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="2a36b-120">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="2a36b-121">**Ungültiger Parameter** (4)</span><span class="sxs-lookup"><span data-stu-id="2a36b-121">**Invalid Parameter** (4)</span></span>
</dt> <dt>

<span data-ttu-id="2a36b-122">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="2a36b-122">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="2a36b-123">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="2a36b-123">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="2a36b-124">**Reservierte Methode** (4097.32767)</span><span class="sxs-lookup"><span data-stu-id="2a36b-124">**Method Reserved** (4097..32767)</span></span>
</dt> <dt>

<span data-ttu-id="2a36b-125">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="2a36b-125">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="2a36b-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="2a36b-126">Requirements</span></span>



| <span data-ttu-id="2a36b-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="2a36b-127">Requirement</span></span> | <span data-ttu-id="2a36b-128">Wert</span><span class="sxs-lookup"><span data-stu-id="2a36b-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a36b-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="2a36b-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2a36b-130">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a36b-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="2a36b-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="2a36b-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2a36b-132">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="2a36b-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="2a36b-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="2a36b-133">Namespace</span></span><br/>                | <span data-ttu-id="2a36b-134">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="2a36b-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="2a36b-135">MOF</span><span class="sxs-lookup"><span data-stu-id="2a36b-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2a36b-136"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="2a36b-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="2a36b-137">DLL</span><span class="sxs-lookup"><span data-stu-id="2a36b-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2a36b-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="2a36b-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="2a36b-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a36b-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a36b-140">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="2a36b-140">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

