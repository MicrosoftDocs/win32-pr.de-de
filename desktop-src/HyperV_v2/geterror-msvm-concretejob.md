---
description: Ruft das Fehler Objekt für den Auftrag ab, sofern vorhanden.
ms.assetid: 7E810CBE-F18F-4EFA-B52E-631CD071D136
title: GetError-Methode der Msvm_ConcreteJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetError
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 63279d8bc08f0b9f1955f694470a3744defd8054
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106359872"
---
# <a name="geterror-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="6f7b7-103">GetError-Methode der MSVM- \_ Klasse "concretejob"</span><span class="sxs-lookup"><span data-stu-id="6f7b7-103">GetError method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="6f7b7-104">Ruft das Fehler Objekt für den Auftrag ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="6f7b7-104">Retrieves the error object for the job, if one exists.</span></span> <span data-ttu-id="6f7b7-105">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode kein [**CIM- \_ Fehler**](/previous-versions//cc150671(v=vs.85)) Objekt zurück.</span><span class="sxs-lookup"><span data-stu-id="6f7b7-105">When the job is executing or has terminated without error, then this method does not return a [**CIM\_Error**](/previous-versions//cc150671(v=vs.85)) object.</span></span> <span data-ttu-id="6f7b7-106">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder der Auftrag von einem Client beendet wurde, wird eine **CIM- \_ Fehler** Instanz zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6f7b7-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then a **CIM\_Error** instance is returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f7b7-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="6f7b7-107">Syntax</span></span>


```mof
uint32 GetError(
  [out] string Error
);
```



## <a name="parameters"></a><span data-ttu-id="6f7b7-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="6f7b7-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f7b7-109">*Fehler* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="6f7b7-109">*Error* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6f7b7-110">Typ: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="6f7b7-110">Type: **string**</span></span>

<span data-ttu-id="6f7b7-111">Wenn der Betriebsstatus des Auftrags nicht 2 (OK) ist, gibt diese Methode eine eingebettete Instanz der [**MSVM- \_ Fehler**](msvm-error.md) Klasse im CIM-XML-Format zurück.</span><span class="sxs-lookup"><span data-stu-id="6f7b7-111">If the operational status of the job is not 2 (OK), this method returns an embedded instance of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format.</span></span> <span data-ttu-id="6f7b7-112">Wenn der Betriebsstatus des Auftrags 2 (OK) ist, wird **null** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="6f7b7-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f7b7-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="6f7b7-113">Return value</span></span>

<span data-ttu-id="6f7b7-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6f7b7-114">Type: **uint32**</span></span>

<span data-ttu-id="6f7b7-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="6f7b7-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="6f7b7-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="6f7b7-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="6f7b7-117">Fehler **(32768** )</span><span class="sxs-lookup"><span data-stu-id="6f7b7-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="6f7b7-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="6f7b7-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="6f7b7-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="6f7b7-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="6f7b7-120">Der **Status ist "Unknown** " (32771).</span><span class="sxs-lookup"><span data-stu-id="6f7b7-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="6f7b7-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="6f7b7-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="6f7b7-122">**Ungültiger Parameter** (32773)</span><span class="sxs-lookup"><span data-stu-id="6f7b7-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="6f7b7-123">Das **System wird verwendet** (32774).</span><span class="sxs-lookup"><span data-stu-id="6f7b7-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="6f7b7-124">**Ungültiger Status für diesen Vorgang** (32775).</span><span class="sxs-lookup"><span data-stu-id="6f7b7-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="6f7b7-125">**Falscher Datentyp** (32776).</span><span class="sxs-lookup"><span data-stu-id="6f7b7-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="6f7b7-126">Das **System ist nicht verfügbar** (32777).</span><span class="sxs-lookup"><span data-stu-id="6f7b7-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="6f7b7-127">**Nicht** genügend Arbeitsspeicher (32778)</span><span class="sxs-lookup"><span data-stu-id="6f7b7-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="6f7b7-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f7b7-128">Remarks</span></span>

<span data-ttu-id="6f7b7-129">Der Zugriff auf die [**MSVM-Klasse " \_ concretejob**](msvm-concretejob.md) " kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="6f7b7-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="6f7b7-130">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="6f7b7-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="6f7b7-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6f7b7-131">Requirements</span></span>



| <span data-ttu-id="6f7b7-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6f7b7-132">Requirement</span></span> | <span data-ttu-id="6f7b7-133">Wert</span><span class="sxs-lookup"><span data-stu-id="6f7b7-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f7b7-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6f7b7-134">Minimum supported client</span></span><br/> | <span data-ttu-id="6f7b7-135">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f7b7-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="6f7b7-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6f7b7-136">Minimum supported server</span></span><br/> | <span data-ttu-id="6f7b7-137">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6f7b7-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6f7b7-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="6f7b7-138">Namespace</span></span><br/>                | <span data-ttu-id="6f7b7-139">\\Stammvirtualisierung \\ v2</span><span class="sxs-lookup"><span data-stu-id="6f7b7-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="6f7b7-140">MOF</span><span class="sxs-lookup"><span data-stu-id="6f7b7-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6f7b7-141"><dt>Windowsvirtualization. v2. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="6f7b7-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6f7b7-142">DLL</span><span class="sxs-lookup"><span data-stu-id="6f7b7-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6f7b7-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6f7b7-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6f7b7-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f7b7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f7b7-145">**MSVM- \_ concretejob**</span><span class="sxs-lookup"><span data-stu-id="6f7b7-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

