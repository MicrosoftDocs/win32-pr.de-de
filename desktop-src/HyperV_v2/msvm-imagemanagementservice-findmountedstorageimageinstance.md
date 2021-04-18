---
description: Sucht ein MSVM \_ mountedstorageimage-Objekt für einen angegebenen Datenträger-Bildpfad.
ms.assetid: 498ed285-2b5b-472b-b0ee-649c97b61274
title: Findmountedstorageimageinstance-Methode der Msvm_ImageManagementService-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ImageManagementService.FindMountedStorageImageInstance
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 80462fb57be8c3f89764774ea68e73a988f11643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526834"
---
# <a name="findmountedstorageimageinstance-method-of-the-msvm_imagemanagementservice-class"></a><span data-ttu-id="978e1-103">Findmountedstorageimageinstance-Methode der MSVM \_ imagemanagementservice-Klasse</span><span class="sxs-lookup"><span data-stu-id="978e1-103">FindMountedStorageImageInstance method of the Msvm\_ImageManagementService class</span></span>

<span data-ttu-id="978e1-104">Sucht ein [**MSVM \_ mountedstorageimage**](msvm-mountedstorageimage.md) -Objekt für einen angegebenen Datenträger-Bildpfad.</span><span class="sxs-lookup"><span data-stu-id="978e1-104">Finds an [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) object for a given disk image path.</span></span>

## <a name="syntax"></a><span data-ttu-id="978e1-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="978e1-105">Syntax</span></span>


```mof
uint32 FindMountedStorageImageInstance(
  [in]  string                       SelectionCriterion,
  [in]  uint16                       CriterionType,
  [out] Msvm_MountedStorageImage REF Image
);
```



## <a name="parameters"></a><span data-ttu-id="978e1-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="978e1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="978e1-107">*Selectionkriterium* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="978e1-107">*SelectionCriterion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="978e1-108">Ein voll qualifizierter Pfad, der den Speicherort einer Datenträger Image Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="978e1-108">A fully-qualified path that specifies the location of a disk image file.</span></span>

</dd> <dt>

<span data-ttu-id="978e1-109">*Kriteriontype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="978e1-109">*CriterionType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="978e1-110">Der Typ des Kriteriums, das beim Auffinden des Datenträger Images gesucht werden soll.</span><span class="sxs-lookup"><span data-stu-id="978e1-110">The type of criterion to look for when finding the disk image.</span></span>

<dt>

<span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="978e1-111">**unbekannt** (0)</span><span class="sxs-lookup"><span data-stu-id="978e1-111">**unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Path"></span><span id="path"></span><span id="PATH"></span>

<span data-ttu-id="978e1-112">**Pfad** (2)</span><span class="sxs-lookup"><span data-stu-id="978e1-112">**Path** (2)</span></span>


</dt> <dd></dd> </dl> </dd> <dt>

<span data-ttu-id="978e1-113">*Bild* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="978e1-113">*Image* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="978e1-114">Ein Verweis auf [**MSVM \_ mountedstorageimage**](msvm-mountedstorageimage.md) (kann NULL sein, wenn das Bild nicht eingebunden ist).</span><span class="sxs-lookup"><span data-stu-id="978e1-114">A reference to the [**Msvm\_MountedStorageImage**](msvm-mountedstorageimage.md) (can be null if the image is not mounted).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="978e1-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="978e1-115">Return value</span></span>

<span data-ttu-id="978e1-116">Diese Methode gibt einen der folgenden Werte zurück:</span><span class="sxs-lookup"><span data-stu-id="978e1-116">This method returns one of the following values:</span></span>

<dl> <dt>

<span data-ttu-id="978e1-117">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="978e1-117">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-118">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="978e1-118">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-119">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="978e1-119">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-120">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="978e1-120">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-121">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="978e1-121">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-122">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="978e1-122">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-123">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="978e1-123">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-124">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="978e1-124">**System is in use** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-125">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="978e1-125">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-126">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="978e1-126">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-127">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="978e1-127">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-128">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="978e1-128">**Out of memory** (32778)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-129">Die **Datei wurde nicht gefunden** (32779).</span><span class="sxs-lookup"><span data-stu-id="978e1-129">**File not found** (32779)</span></span>
</dt> <dt>

<span data-ttu-id="978e1-130">**Objekt nicht gefunden** (32789)</span><span class="sxs-lookup"><span data-stu-id="978e1-130">**Object not found** (32789)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="978e1-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="978e1-131">Requirements</span></span>



| <span data-ttu-id="978e1-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="978e1-132">Requirement</span></span> | <span data-ttu-id="978e1-133">Wert</span><span class="sxs-lookup"><span data-stu-id="978e1-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="978e1-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="978e1-134">Minimum supported client</span></span><br/> | <span data-ttu-id="978e1-135">Nur Windows 10 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="978e1-135">Windows 10 \[desktop apps only\]</span></span><br/>                                                             |
| <span data-ttu-id="978e1-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="978e1-136">Minimum supported server</span></span><br/> | <span data-ttu-id="978e1-137">Windows Server 2016</span><span class="sxs-lookup"><span data-stu-id="978e1-137">Windows Server 2016</span></span><br/>                                                                          |
| <span data-ttu-id="978e1-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="978e1-138">Namespace</span></span><br/>                | <span data-ttu-id="978e1-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="978e1-139">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="978e1-140">MOF</span><span class="sxs-lookup"><span data-stu-id="978e1-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="978e1-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="978e1-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="978e1-142">DLL</span><span class="sxs-lookup"><span data-stu-id="978e1-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="978e1-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="978e1-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="978e1-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="978e1-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="978e1-145">**MSVM \_ imagemanagementservice**</span><span class="sxs-lookup"><span data-stu-id="978e1-145">**Msvm\_ImageManagementService**</span></span>](msvm-imagemanagementservice.md)
</dt> </dl>

 

 




