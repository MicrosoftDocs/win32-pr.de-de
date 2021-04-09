---
title: Queryofflineinformation-Methode der Win32_TSVm-Klasse
description: Ruft die Eigenschaften des aktuellen virtuellen Desktop Servers (VDS) ab, jedoch nur, wenn der Server offline ist.
ms.assetid: f6ce74cb-a4a4-4e05-a0a7-bac0b7f52c45
ms.tgt_platform: multiple
keywords:
- Queryofflineinformation-Methode Remotedesktopdienste
- Queryofflineinformation-Methode Remotedesktopdienste, Win32_TSVm-Klasse
- Win32_TSVm-Klasse Remotedesktopdienste, queryofflineinformation-Methode
topic_type:
- apiref
api_name:
- Win32_TSVm.QueryOfflineInformation
api_location:
- TSVmHostWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4750ebdb82b08ae1ed0350e1ac448d9aca4003b2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859030"
---
# <a name="queryofflineinformation-method-of-the-win32_tsvm-class"></a><span data-ttu-id="13b86-106">Queryofflineinformation-Methode der Win32- \_ Klasse "ZVM"</span><span class="sxs-lookup"><span data-stu-id="13b86-106">QueryOfflineInformation method of the Win32\_TSVm class</span></span>

<span data-ttu-id="13b86-107">Ruft die Eigenschaften des aktuellen virtuellen Desktop Servers (VDS) ab, jedoch nur, wenn der Server offline ist.</span><span class="sxs-lookup"><span data-stu-id="13b86-107">Retrieves the properties of the current virtual desktop server (VDS), but only when the server is offline.</span></span>

## <a name="syntax"></a><span data-ttu-id="13b86-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="13b86-108">Syntax</span></span>


```mof
uint32 QueryOfflineInformation(
  [out] string  Build,
  [out] string  CurrentVersion,
  [out] string  InstallationType,
  [out] string  EditionId,
  [out] string  SysPrepImageState,
  [out] string  SysPrepMode,
  [out] sint32  ProcArch,
  [out] boolean fIsVmbusCapable,
  [out] boolean fIsRdvIcInstalled
);
```



## <a name="parameters"></a><span data-ttu-id="13b86-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="13b86-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13b86-110">*Build* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13b86-110">*Build* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b86-111">Bei erfolgreicher Ausführung wird die Buildversion der VDS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13b86-111">On a success, returns the build version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="13b86-112">*CurrentVersion* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13b86-112">*CurrentVersion* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b86-113">Bei erfolgreicher Ausführung wird die aktuelle Version der VDS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13b86-113">On a success, returns the current version of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="13b86-114">*Installationstyp* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13b86-114">*InstallationType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b86-115">Bei erfolgreicher Ausführung wird der Installationstyp der VDS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13b86-115">On a success, returns the installation type of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="13b86-116">*EditionID* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13b86-116">*EditionId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b86-117">Bei erfolgreicher Ausführung wird die Editions-ID der VDS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13b86-117">On a success, returns the edition ID of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="13b86-118">*Sygeopimagestate* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13b86-118">*SysPrepImageState* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b86-119">Bei Erfolg wird der Status des System prep-Images der VDS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13b86-119">On success, returns the system prep image state of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="13b86-120">*Systreupmode* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13b86-120">*SysPrepMode* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b86-121">Bei erfolgreicher Ausführung wird der System Vorbereitungsmodus der VDS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13b86-121">On a success, returns the system prep mode of the VDS.</span></span>

</dd> <dt>

<span data-ttu-id="13b86-122">*Procarch* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13b86-122">*ProcArch* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b86-123">Bei erfolgreicher Ausführung wird ein Wert zurückgegeben, der die Prozessorarchitektur angibt.</span><span class="sxs-lookup"><span data-stu-id="13b86-123">On a success, returns a value indicating the processor architecture.</span></span>

<dt>

<span data-ttu-id="13b86-124">0</span><span class="sxs-lookup"><span data-stu-id="13b86-124">0</span></span>
</dt> <dd>

<span data-ttu-id="13b86-125">x86</span><span class="sxs-lookup"><span data-stu-id="13b86-125">x86</span></span>

</dd> <dt>

<span data-ttu-id="13b86-126">1</span><span class="sxs-lookup"><span data-stu-id="13b86-126">1</span></span>
</dt> <dd>

<span data-ttu-id="13b86-127">amd64</span><span class="sxs-lookup"><span data-stu-id="13b86-127">amd64</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="13b86-128">*fisvmbuscapable* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13b86-128">*fIsVmbusCapable* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b86-129">gibt bei Erfolg an, ob das System VMBus-fähig ist.</span><span class="sxs-lookup"><span data-stu-id="13b86-129">on a success, indicates whether the system is VMBus-capable.</span></span>

</dd> <dt>

<span data-ttu-id="13b86-130">*fisrdvicinstallierte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="13b86-130">*fIsRdvIcInstalled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="13b86-131">Bei erfolgreicher Ausführung wird angegeben, ob rdvic installiert ist.</span><span class="sxs-lookup"><span data-stu-id="13b86-131">On a success, indicates if RDVIC is installed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13b86-132">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13b86-132">Return value</span></span>

<span data-ttu-id="13b86-133">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13b86-133">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="13b86-134">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="13b86-134">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="13b86-135">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13b86-135">Requirements</span></span>



| <span data-ttu-id="13b86-136">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13b86-136">Requirement</span></span> | <span data-ttu-id="13b86-137">Wert</span><span class="sxs-lookup"><span data-stu-id="13b86-137">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="13b86-138">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13b86-138">Minimum supported client</span></span><br/> | <span data-ttu-id="13b86-139">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="13b86-139">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="13b86-140">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13b86-140">Minimum supported server</span></span><br/> | <span data-ttu-id="13b86-141">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="13b86-141">Windows Server 2012</span></span><br/>                                                             |
| <span data-ttu-id="13b86-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="13b86-142">Namespace</span></span><br/>                | <span data-ttu-id="13b86-143">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="13b86-143">Root\\CIMv2\\TerminalServices</span></span><br/>                                                   |
| <span data-ttu-id="13b86-144">MOF</span><span class="sxs-lookup"><span data-stu-id="13b86-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13b86-145"><dt>"Zvmhost. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="13b86-145"><dt>TSVmHost.mof</dt></span></span> </dl>    |
| <span data-ttu-id="13b86-146">DLL</span><span class="sxs-lookup"><span data-stu-id="13b86-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13b86-147"><dt>TSVmHostWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13b86-147"><dt>TSVmHostWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13b86-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13b86-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13b86-149">**Win32- \_ VM**</span><span class="sxs-lookup"><span data-stu-id="13b86-149">**Win32\_TSVm**</span></span>](win32-tsvm.md)
</dt> </dl>

 

 





