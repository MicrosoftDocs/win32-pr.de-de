---
description: Erstellt eine virtuelle Festplatten Datei.
ms.assetid: 6c136000-1df2-4456-833c-094671408338
title: Die Methode "kreatevirtualharddisk" der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.CreateVirtualHardDisk
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: b80a309274eb51ad7aff768898a9c3bd211f37cb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355283"
---
# <a name="createvirtualharddisk-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="bcfbc-103">Die Methode "kreatevirtualharddisk" der Klasse "MSVM \_ imagemanagementservice"</span><span class="sxs-lookup"><span data-stu-id="bcfbc-103">CreateVirtualHardDisk method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="bcfbc-104">Erstellt eine virtuelle Festplatten Datei.</span><span class="sxs-lookup"><span data-stu-id="bcfbc-104">Creates a virtual hard disk file.</span></span>

## <a name="syntax"></a><span data-ttu-id="bcfbc-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="bcfbc-105">Syntax</span></span>


```mof
uint32 CreateVirtualHardDisk(
  [in]  string              VirtualDiskSettingData,
  [out] CIM_ConcreteJob REF Job
);
```



## <a name="parameters"></a><span data-ttu-id="bcfbc-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bcfbc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bcfbc-107">*Virtualdisksettingdata* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="bcfbc-107">*VirtualDiskSettingData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfbc-108">Eine Zeichenfolge, die eine eingebettete Instanz der [**MSVM \_ virtualharddisksettingdata**](msvm-virtualharddisksettingdata.md) -Klasse enthält, die verwendet wird, um Attribute der zu erstellenden virtuellen Festplatte zu definieren.</span><span class="sxs-lookup"><span data-stu-id="bcfbc-108">String that contains an embedded instance of the [**Msvm\_VirtualHardDiskSettingData**](msvm-virtualharddisksettingdata.md) class that is used to define attributes of the virtual hard disk to be created.</span></span>

</dd> <dt>

<span data-ttu-id="bcfbc-109">*Auftrag* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="bcfbc-109">*Job* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bcfbc-110">Ein Verweis auf den Auftrag (kann **null** sein, wenn die Aufgabe abgeschlossen ist).</span><span class="sxs-lookup"><span data-stu-id="bcfbc-110">A reference to the job (can be **Null** if the task is completed).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bcfbc-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bcfbc-111">Return value</span></span>

<span data-ttu-id="bcfbc-112">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="bcfbc-112">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="bcfbc-113">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="bcfbc-113">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-114">Über **prüfte Methoden Parameter-Auftrag gestartet** (4096)</span><span class="sxs-lookup"><span data-stu-id="bcfbc-114">**Method Parameters Checked - Job Started** (4096)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-115">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="bcfbc-115">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-116">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="bcfbc-116">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-117">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="bcfbc-117">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-118">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="bcfbc-118">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-119">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="bcfbc-119">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-120">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="bcfbc-120">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-121">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="bcfbc-121">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-122">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="bcfbc-122">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-123">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="bcfbc-123">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-124">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="bcfbc-124">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-125">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="bcfbc-125">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="bcfbc-126">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="bcfbc-126">**File not found** (32779)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="bcfbc-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bcfbc-127">Remarks</span></span>

<span data-ttu-id="bcfbc-128">Der Zugriff auf die [**MSVM \_ imagemanagementservice**](msvm-imagemanagementservice.md) -Klasse kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="bcfbc-128">Access to the [**Msvm\_ImageManagementService**](msvm-imagemanagementservice.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="bcfbc-129">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="bcfbc-129">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="bcfbc-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="bcfbc-130">Requirements</span></span>



| <span data-ttu-id="bcfbc-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bcfbc-131">Requirement</span></span> | <span data-ttu-id="bcfbc-132">Wert</span><span class="sxs-lookup"><span data-stu-id="bcfbc-132">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bcfbc-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bcfbc-133">Minimum supported client</span></span><br/> | <span data-ttu-id="bcfbc-134">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcfbc-134">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="bcfbc-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bcfbc-135">Minimum supported server</span></span><br/> | <span data-ttu-id="bcfbc-136">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bcfbc-136">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="bcfbc-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="bcfbc-137">Namespace</span></span><br/>                | <span data-ttu-id="bcfbc-138">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="bcfbc-138">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="bcfbc-139">MOF</span><span class="sxs-lookup"><span data-stu-id="bcfbc-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="bcfbc-140"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="bcfbc-140"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="bcfbc-141">DLL</span><span class="sxs-lookup"><span data-stu-id="bcfbc-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bcfbc-142"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="bcfbc-142"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="bcfbc-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bcfbc-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bcfbc-144">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="bcfbc-144">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

