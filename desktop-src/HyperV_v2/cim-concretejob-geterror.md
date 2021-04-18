---
description: Ruft einen Fehler aufgrund eines fehlgeschlagenen Auftrags ab.
ms.assetid: d499eb91-e1cc-4792-b32d-5a8875eebbb7
title: GetError-Methode der CIM_ConcreteJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: aa9ed87f2d484286d91d14c4183d2ce3b6f41cfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345166"
---
# <a name="geterror-method-of-the-cim_concretejob-class"></a><span data-ttu-id="ca046-103">GetError-Methode der CIM- \_ Klasse "concretejob"</span><span class="sxs-lookup"><span data-stu-id="ca046-103">GetError method of the CIM\_ConcreteJob class</span></span>

<span data-ttu-id="ca046-104">Ruft einen Fehler aufgrund eines fehlgeschlagenen Auftrags ab.</span><span class="sxs-lookup"><span data-stu-id="ca046-104">Retrieves an error due to a failed job.</span></span> <span data-ttu-id="ca046-105">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode keine [**CIM- \_ Fehler**](cim-error.md) Instanz zurück.</span><span class="sxs-lookup"><span data-stu-id="ca046-105">When the job is executing or has terminated without error, then this method returns no [**CIM\_Error**](cim-error.md) instance.</span></span> <span data-ttu-id="ca046-106">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder der Auftrag von einem Client beendet wurde, wird eine **CIM- \_ Fehler** Instanz zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca046-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca046-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca046-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="ca046-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca046-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca046-109">*Fehler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ca046-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ca046-110">Gibt eine [**CIM- \_ Fehler**](cim-error.md) Instanz zurück, wenn der **OperationalStatus** für den Auftrag nicht "OK" ist; andernfalls wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca046-110">Returns a [**CIM\_Error**](cim-error.md) instance if the **OperationalStatus** on the Job is not "OK"; otherwise, returns **null**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca046-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca046-111">Return value</span></span>

<span data-ttu-id="ca046-112">Gibt bei Erfolg 0 (null) zurück. Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ca046-112">Returns a 0 on success; otherwise, returns an error.</span></span>

<dl> <dt>

<span data-ttu-id="ca046-113">**Erfolg** (0)</span><span class="sxs-lookup"><span data-stu-id="ca046-113">**Success** (0)</span></span>
</dt> <dt>

<span data-ttu-id="ca046-114">**Nicht unterstützt** (1)</span><span class="sxs-lookup"><span data-stu-id="ca046-114">**Not Supported** (1)</span></span>
</dt> <dt>

<span data-ttu-id="ca046-115">**Nicht spezifizierter Fehler** (2)</span><span class="sxs-lookup"><span data-stu-id="ca046-115">**Unspecified Error** (2)</span></span>
</dt> <dt>

<span data-ttu-id="ca046-116">**Timeout** (3)</span><span class="sxs-lookup"><span data-stu-id="ca046-116">**Timeout** (3)</span></span>
</dt> <dt>

<span data-ttu-id="ca046-117">Fehler **(4** )</span><span class="sxs-lookup"><span data-stu-id="ca046-117">**Failed** (4)</span></span>
</dt> <dt>

<span data-ttu-id="ca046-118">**Ungültiger Parameter** (5)</span><span class="sxs-lookup"><span data-stu-id="ca046-118">**Invalid Parameter** (5)</span></span>
</dt> <dt>

<span data-ttu-id="ca046-119">**Zugriff verweigert** (6)</span><span class="sxs-lookup"><span data-stu-id="ca046-119">**Access Denied** (6)</span></span>
</dt> <dt>

<span data-ttu-id="ca046-120">**DMTF reserviert** (..)</span><span class="sxs-lookup"><span data-stu-id="ca046-120">**DMTF Reserved** (..)</span></span>
</dt> <dt>

<span data-ttu-id="ca046-121">**Hersteller spezifisch** (32768.65535)</span><span class="sxs-lookup"><span data-stu-id="ca046-121">**Vendor Specific** (32768..65535)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="ca046-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca046-122">Requirements</span></span>



| <span data-ttu-id="ca046-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca046-123">Requirement</span></span> | <span data-ttu-id="ca046-124">Wert</span><span class="sxs-lookup"><span data-stu-id="ca046-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca046-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ca046-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ca046-126">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="ca046-126">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="ca046-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ca046-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ca046-128">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="ca046-128">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="ca046-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="ca046-129">Namespace</span></span><br/>                | <span data-ttu-id="ca046-130">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="ca046-130">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="ca046-131">MOF</span><span class="sxs-lookup"><span data-stu-id="ca046-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ca046-132"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ca046-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="ca046-133">DLL</span><span class="sxs-lookup"><span data-stu-id="ca046-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ca046-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="ca046-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="ca046-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca046-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca046-136">**CIM- \_ concretejob**</span><span class="sxs-lookup"><span data-stu-id="ca046-136">**CIM\_ConcreteJob**</span></span>](cim-concretejob.md)
</dt> </dl>

 

 




