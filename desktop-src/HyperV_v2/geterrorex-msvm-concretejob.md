---
description: 'GetErrorEx-Methode der Msvm_ConcreteJob Klasse: Ruft die Fehlerobjekte für den Auftrag ab, sofern vorhanden.'
ms.assetid: B4B4F60C-9221-4125-8D42-F0F1D32C3E79
title: GetErrorEx-Methode der Msvm_ConcreteJob-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteJob.GetErrorEx
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 67abbd06fdaae9c23cca53f5516586f45216f20d
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119348"
---
# <a name="geterrorex-method-of-the-msvm_concretejob-class"></a><span data-ttu-id="23567-103">GetErrorEx-Methode der Msvm \_ ConcreteJob-Klasse</span><span class="sxs-lookup"><span data-stu-id="23567-103">GetErrorEx method of the Msvm\_ConcreteJob class</span></span>

<span data-ttu-id="23567-104">Ruft die Fehlerobjekte für den Auftrag ab, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="23567-104">Retrieves the error objects for the job, if any exist.</span></span> <span data-ttu-id="23567-105">Wenn der Auftrag ausgeführt wird oder ohne Fehler beendet wurde, gibt diese Methode keine [**Msvm \_ Error-Instanz**](msvm-error.md) zurück.</span><span class="sxs-lookup"><span data-stu-id="23567-105">When the job is executing or has terminated without error, then this method returns no [**Msvm\_Error**](msvm-error.md) instance.</span></span> <span data-ttu-id="23567-106">Wenn der Auftrag jedoch aufgrund eines internen Problems fehlgeschlagen ist oder weil der Auftrag von einem Client beendet wurde, wird mindestens eine **Msvm \_ Error-Instanz** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="23567-106">However, if the job has failed because of some internal problem or because the job has been terminated by a client, then one or more **Msvm\_Error** instances are returned.</span></span>

## <a name="syntax"></a><span data-ttu-id="23567-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="23567-107">Syntax</span></span>


```mof
uint32 GetErrorEx(
  [out] string Errors[]
);
```



## <a name="parameters"></a><span data-ttu-id="23567-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="23567-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23567-109">*Fehler* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="23567-109">*Errors* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23567-110">Typ: **\[ \] Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="23567-110">Type: **string\[\]**</span></span>

<span data-ttu-id="23567-111">Wenn der Betriebsstatus des Auftrags nicht 2 (OK) ist, gibt diese Methode mindestens eine eingebettete Instanz der [**Msvm \_ Error-Klasse**](msvm-error.md) im CIM-XML-Format zurück, die die im Auftrag aufgetretenen Fehler darstellen.</span><span class="sxs-lookup"><span data-stu-id="23567-111">If the operational status of the job is not 2 (OK), this method returns one or more embedded instances of the [**Msvm\_Error**](msvm-error.md) class, in CIM-XML format, that represent the errors encountered in the job.</span></span> <span data-ttu-id="23567-112">Wenn der Betriebsstatus des Auftrags 2 (OK) ist, wird **NULL** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="23567-112">If the operational status of the job is 2 (OK), then **Null** is returned.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23567-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="23567-113">Return value</span></span>

<span data-ttu-id="23567-114">Typ: **uint32**</span><span class="sxs-lookup"><span data-stu-id="23567-114">Type: **uint32**</span></span>

<span data-ttu-id="23567-115">Diese Methode gibt einen der folgenden Werte zurück.</span><span class="sxs-lookup"><span data-stu-id="23567-115">This method returns one of the following values.</span></span>

<dl> <dt>

<span data-ttu-id="23567-116">**Abgeschlossen ohne Fehler** (0)</span><span class="sxs-lookup"><span data-stu-id="23567-116">**Completed with No Error** (0)</span></span>
</dt> <dt>

<span data-ttu-id="23567-117">**Fehler** (32768)</span><span class="sxs-lookup"><span data-stu-id="23567-117">**Failed** (32768)</span></span>
</dt> <dt>

<span data-ttu-id="23567-118">**Zugriff verweigert** (32769)</span><span class="sxs-lookup"><span data-stu-id="23567-118">**Access Denied** (32769)</span></span>
</dt> <dt>

<span data-ttu-id="23567-119">**Nicht unterstützt** (32770)</span><span class="sxs-lookup"><span data-stu-id="23567-119">**Not Supported** (32770)</span></span>
</dt> <dt>

<span data-ttu-id="23567-120">**Status ist unbekannt** (32771)</span><span class="sxs-lookup"><span data-stu-id="23567-120">**Status is unknown** (32771)</span></span>
</dt> <dt>

<span data-ttu-id="23567-121">**Timeout** (32772)</span><span class="sxs-lookup"><span data-stu-id="23567-121">**Timeout** (32772)</span></span>
</dt> <dt>

<span data-ttu-id="23567-122">**Ungültiger** Parameter (32773)</span><span class="sxs-lookup"><span data-stu-id="23567-122">**Invalid parameter** (32773)</span></span>
</dt> <dt>

<span data-ttu-id="23567-123">**System wird verwendet** (32774)</span><span class="sxs-lookup"><span data-stu-id="23567-123">**System is in used** (32774)</span></span>
</dt> <dt>

<span data-ttu-id="23567-124">**Ungültiger Zustand für diesen Vorgang** (32775)</span><span class="sxs-lookup"><span data-stu-id="23567-124">**Invalid state for this operation** (32775)</span></span>
</dt> <dt>

<span data-ttu-id="23567-125">**Falscher Datentyp** (32776)</span><span class="sxs-lookup"><span data-stu-id="23567-125">**Incorrect data type** (32776)</span></span>
</dt> <dt>

<span data-ttu-id="23567-126">**System ist nicht verfügbar** (32777)</span><span class="sxs-lookup"><span data-stu-id="23567-126">**System is not available** (32777)</span></span>
</dt> <dt>

<span data-ttu-id="23567-127">**Nicht genügend Arbeitsspeicher** (32778)</span><span class="sxs-lookup"><span data-stu-id="23567-127">**Out of memory** (32778)</span></span>
</dt> </dl>

## <a name="remarks"></a><span data-ttu-id="23567-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23567-128">Remarks</span></span>

<span data-ttu-id="23567-129">Der Zugriff auf die [**Msvm \_ ConcreteJob-Klasse**](msvm-concretejob.md) kann durch die UAC-Filterung eingeschränkt werden.</span><span class="sxs-lookup"><span data-stu-id="23567-129">Access to the [**Msvm\_ConcreteJob**](msvm-concretejob.md) class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="23567-130">Weitere Informationen finden Sie unter [Benutzerkontensteuerung und WMI.](/windows/desktop/WmiSdk/user-account-control-and-wmi)</span><span class="sxs-lookup"><span data-stu-id="23567-130">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="23567-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23567-131">Requirements</span></span>



| <span data-ttu-id="23567-132">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="23567-132">Requirement</span></span> | <span data-ttu-id="23567-133">Wert</span><span class="sxs-lookup"><span data-stu-id="23567-133">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23567-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="23567-134">Minimum supported client</span></span><br/> | <span data-ttu-id="23567-135">nur Windows 8 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23567-135">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="23567-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="23567-136">Minimum supported server</span></span><br/> | <span data-ttu-id="23567-137">Nur Windows Server \[ 2012-Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="23567-137">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="23567-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="23567-138">Namespace</span></span><br/>                | <span data-ttu-id="23567-139">Root \\ Virtualization \\ V2</span><span class="sxs-lookup"><span data-stu-id="23567-139">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="23567-140">MOF</span><span class="sxs-lookup"><span data-stu-id="23567-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="23567-141"><dt>WindowsVirtualization.V2.mof</dt></span><span class="sxs-lookup"><span data-stu-id="23567-141"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="23567-142">DLL</span><span class="sxs-lookup"><span data-stu-id="23567-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="23567-143"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="23567-143"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="23567-144">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="23567-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23567-145">**Msvm \_ ConcreteJob**</span><span class="sxs-lookup"><span data-stu-id="23567-145">**Msvm\_ConcreteJob**</span></span>](msvm-concretejob.md)
</dt> </dl>

 

