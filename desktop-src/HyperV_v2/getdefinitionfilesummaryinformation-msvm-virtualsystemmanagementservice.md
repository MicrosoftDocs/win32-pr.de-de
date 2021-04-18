---
description: Gibt Informationen zur Zusammenfassung der virtuellen Computer für die angegebenen Definitions Dateien der virtuellen Maschine zurück.
ms.assetid: 5a3d7f2c-3b89-4dd6-909d-4452afc3705f
title: GetDefinitionFileSummaryInformation-Methode der Msvm_VirtualSystemManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.GetDefinitionFileSummaryInformation
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: a46daedd282d07c2367931a9f20a7fbfa1849f9e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106357370"
---
# <a name="getdefinitionfilesummaryinformation-method-of-the-msvm_virtualsystemmanagementservice-class"></a><span data-ttu-id="142aa-103">GetDefinitionFileSummaryInformation-Methode der MSVM \_ virtualsystemmanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="142aa-103">GetDefinitionFileSummaryInformation method of the Msvm\_VirtualSystemManagementService class</span></span>

<span data-ttu-id="142aa-104">Gibt Informationen zur Zusammenfassung der virtuellen Computer für die angegebenen Definitions Dateien der virtuellen Maschine zurück.</span><span class="sxs-lookup"><span data-stu-id="142aa-104">Returns virtual machine summary information for the specified virtual machine definition files.</span></span>

## <a name="syntax"></a><span data-ttu-id="142aa-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="142aa-105">Syntax</span></span>


```mof
uint32 GetDefinitionFileSummaryInformation(
  [in]  string                      DefinitionFiles[],
  [out] Msvm_SummaryInformationBase SummaryInformation[]
);
```



## <a name="parameters"></a><span data-ttu-id="142aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="142aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="142aa-107">*DefinitionFiles* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="142aa-107">*DefinitionFiles* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="142aa-108">Ein Array von Pfaden zu XML-Konfigurationsdateien, für die Zusammenfassungs Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="142aa-108">An array of paths to XML configuration files for which to return summary information.</span></span>

</dd> <dt>

<span data-ttu-id="142aa-109">*SummaryInformation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="142aa-109">*SummaryInformation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="142aa-110">Ein Array von [**MSVM- \_ summaryinformationbase**](msvm-summaryinformation.md) -Instanzen, die die angeforderten Informationen für die virtuellen Computer und/oder Momentaufnahmen enthalten, die im *DefinitionFiles* -Array angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="142aa-110">An array of [**Msvm\_SummaryInformationBase**](msvm-summaryinformation.md) instances containing the requested information for the virtual machines and/or snapshots specified in the *DefinitionFiles* array.</span></span> <span data-ttu-id="142aa-111">Nur die Eigenschaften **Name**, **ElementName**, **kreationtime** und **Notes** werden zurückgegeben, alle anderen Eigenschaften sind **null**.</span><span class="sxs-lookup"><span data-stu-id="142aa-111">Only the **Name**, **ElementName**, **CreationTime**, and **Notes** properties are returned, all other properties will be **Null**.</span></span>

> [!Note]  

 

<span data-ttu-id="142aa-112">Vor Windows 10, Version 1703, war Datentyp [**MSVM \_ SummaryInformation**](msvm-summaryinformation.md).</span><span class="sxs-lookup"><span data-stu-id="142aa-112">Prior to Windows 10, version 1703, datatype was [**Msvm\_SummaryInformation**](msvm-summaryinformation.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="142aa-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="142aa-113">Return value</span></span>

<span data-ttu-id="142aa-114">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="142aa-114">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="142aa-115">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="142aa-115">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-116">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="142aa-116">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="142aa-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="142aa-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="142aa-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="142aa-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="142aa-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="142aa-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="142aa-123">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="142aa-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="142aa-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="142aa-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="142aa-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="142aa-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="142aa-128">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="142aa-128">Requirements</span></span>



| <span data-ttu-id="142aa-129">Anforderung</span><span class="sxs-lookup"><span data-stu-id="142aa-129">Requirement</span></span> | <span data-ttu-id="142aa-130">Wert</span><span class="sxs-lookup"><span data-stu-id="142aa-130">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="142aa-131">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="142aa-131">Minimum supported client</span></span><br/> | <span data-ttu-id="142aa-132">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="142aa-132">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="142aa-133">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="142aa-133">Minimum supported server</span></span><br/> | <span data-ttu-id="142aa-134">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="142aa-134">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="142aa-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="142aa-135">Namespace</span></span><br/>                | <span data-ttu-id="142aa-136">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="142aa-136">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="142aa-137">MOF</span><span class="sxs-lookup"><span data-stu-id="142aa-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="142aa-138"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="142aa-138"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="142aa-139">DLL</span><span class="sxs-lookup"><span data-stu-id="142aa-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="142aa-140"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="142aa-140"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="142aa-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="142aa-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="142aa-142">**MSVM \_ virtualsystemmanagementservice**</span><span class="sxs-lookup"><span data-stu-id="142aa-142">**Msvm\_VirtualSystemManagementService**</span></span>](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

 




