---
description: Die isownershipallowed-Methode der Win32- \_ TPM-Klasse gibt an, ob die Möglichkeit zum Installieren eines Besitzers für das Gerät zulässig ist.
ms.assetid: dfeb5afe-4169-470b-b5e4-cf1e5781271e
title: Isownershipallowed-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnershipAllowed
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c818d5a4e4eb16ac637372f0c7ed0f2e9211ef88
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214511"
---
# <a name="isownershipallowed-method-of-the-win32_tpm-class"></a><span data-ttu-id="84169-103">Isownershipallowed-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="84169-103">IsOwnershipAllowed method of the Win32\_Tpm class</span></span>

<span data-ttu-id="84169-104">Die **isownershipallowed** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob die Möglichkeit zum Installieren eines Besitzers für das Gerät zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="84169-104">The **IsOwnershipAllowed** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the ability to install an owner for the device is permitted.</span></span>

## <a name="syntax"></a><span data-ttu-id="84169-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84169-105">Syntax</span></span>


```mof
uint32 IsOwnershipAllowed(
  [out] boolean IsOwnershipAllowed
);
```



## <a name="parameters"></a><span data-ttu-id="84169-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84169-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84169-107">*Isownershipallowed* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="84169-107">*IsOwnershipAllowed* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84169-108">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="84169-108">Type: **boolean**</span></span>

<span data-ttu-id="84169-109">**True** gibt an, dass die Möglichkeit zum Installieren eines Besitzers für das Gerät zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="84169-109">If **true**, the ability to install an owner for the device is permitted.</span></span> <span data-ttu-id="84169-110">Wenn der Wert **false** ist, kann die Methode " [**Take Ownership**](takeownership-win32-tpm.md) " keinen Besitzer für das Gerät installieren.</span><span class="sxs-lookup"><span data-stu-id="84169-110">If **false**, the method [**TakeOwnership**](takeownership-win32-tpm.md) will fail to install an owner for the device.</span></span>

<span data-ttu-id="84169-111">Dieser Wert kann mit der [**setphysicalpresencerequest**](setphysicalpresencerequest-win32-tpm.md) -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="84169-111">This value can be changed with the [**SetPhysicalPresenceRequest**](setphysicalpresencerequest-win32-tpm.md) method.</span></span> <span data-ttu-id="84169-112">Der Wert wird nach dem Ausführen der [**Clear**](clear-win32-tpm.md) -Methode auf **true** zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="84169-112">The value is reset to **true** after the [**Clear**](clear-win32-tpm.md) method is run.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84169-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84169-113">Return value</span></span>

<span data-ttu-id="84169-114">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="84169-114">Type: **uint32**</span></span>

<span data-ttu-id="84169-115">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="84169-115">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="84169-116">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="84169-116">Common return codes are listed below.</span></span>



| <span data-ttu-id="84169-117">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="84169-117">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="84169-118">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="84169-118">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="84169-119"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="84169-119"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="84169-120">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="84169-120">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="84169-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84169-121">Remarks</span></span>

<span data-ttu-id="84169-122">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="84169-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="84169-123">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="84169-123">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="84169-124">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="84169-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="84169-125">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="84169-125">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="84169-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84169-126">Requirements</span></span>



| <span data-ttu-id="84169-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84169-127">Requirement</span></span> | <span data-ttu-id="84169-128">Wert</span><span class="sxs-lookup"><span data-stu-id="84169-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="84169-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84169-129">Minimum supported client</span></span><br/> | <span data-ttu-id="84169-130">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84169-130">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="84169-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84169-131">Minimum supported server</span></span><br/> | <span data-ttu-id="84169-132">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84169-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="84169-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="84169-133">Namespace</span></span><br/>                | <span data-ttu-id="84169-134">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="84169-134">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="84169-135">MOF</span><span class="sxs-lookup"><span data-stu-id="84169-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="84169-136"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="84169-136"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="84169-137">DLL</span><span class="sxs-lookup"><span data-stu-id="84169-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84169-138"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84169-138"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84169-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84169-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84169-140">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="84169-140">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
