---
description: Deaktiviert die automatische Bereitstellung von TPM, sofern diese derzeit aktiviert ist.
ms.assetid: 30CC2581-9C16-4A11-92F1-625992F2AF20
title: Win32_Tpm::D der Methode "isableautoprovisioning"
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.DisableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5387e744ec5f02bf448a997cfe1c8c83342903a6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349523"
---
# <a name="win32_tpmdisableautoprovisioning-method"></a><span data-ttu-id="494c8-103">Win32- \_ TPM::D-Methode "isableautoprovisioning"</span><span class="sxs-lookup"><span data-stu-id="494c8-103">Win32\_Tpm::DisableAutoProvisioning method</span></span>

<span data-ttu-id="494c8-104">Deaktiviert die automatische Bereitstellung von TPM, sofern diese derzeit aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="494c8-104">Disables auto provisioning of the TPM if it is currently enabled.</span></span> <span data-ttu-id="494c8-105">Der Vorgang hat keine Auswirkung, wenn die automatische Bereitstellung bereits deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="494c8-105">The operation has no effect if auto provisioning is already disabled.</span></span> <span data-ttu-id="494c8-106">Standardmäßig ist die automatische Bereitstellung für Windows 8 und Windows Server 2012 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="494c8-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="494c8-107">Diese Methode ist nur für lokale Administratoren zugänglich.</span><span class="sxs-lookup"><span data-stu-id="494c8-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="494c8-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="494c8-108">Syntax</span></span>


```C++
uint32 DisableAutoProvisioning(
  [in, optional] BOOL OnlyForNextBoot
);
```



## <a name="parameters"></a><span data-ttu-id="494c8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="494c8-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="494c8-110">*Onlyfornextboot* \[ in, optional\]</span><span class="sxs-lookup"><span data-stu-id="494c8-110">*OnlyForNextBoot* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="494c8-111">Wenn diese Option auf **true** festgelegt ist, wird die automatische Bereitstellung nur für den nächsten Start deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="494c8-111">If set to **TRUE**, auto provisioning is disabled for only the next boot.</span></span> <span data-ttu-id="494c8-112">Wenn der Wert auf **false** festgelegt oder nicht angegeben wird, wird die automatische Bereitstellung dauerhaft deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="494c8-112">If set to **FALSE** or not specified, auto provisioning is permanently disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="494c8-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="494c8-113">Return value</span></span>

<span data-ttu-id="494c8-114">Alle TPM-Fehler sowie Fehler, die für die [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="494c8-114">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="494c8-115">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="494c8-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="494c8-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="494c8-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="494c8-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="494c8-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="494c8-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="494c8-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="494c8-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="494c8-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="494c8-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="494c8-120">Remarks</span></span>

<span data-ttu-id="494c8-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="494c8-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="494c8-122">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="494c8-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="494c8-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="494c8-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="494c8-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="494c8-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="494c8-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="494c8-125">Requirements</span></span>



| <span data-ttu-id="494c8-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="494c8-126">Requirement</span></span> | <span data-ttu-id="494c8-127">Wert</span><span class="sxs-lookup"><span data-stu-id="494c8-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="494c8-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="494c8-128">Minimum supported client</span></span><br/> | <span data-ttu-id="494c8-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="494c8-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="494c8-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="494c8-130">Minimum supported server</span></span><br/> | <span data-ttu-id="494c8-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="494c8-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="494c8-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="494c8-132">Namespace</span></span><br/>                | <span data-ttu-id="494c8-133">\\\\.\\ root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="494c8-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="494c8-134">MOF</span><span class="sxs-lookup"><span data-stu-id="494c8-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="494c8-135"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="494c8-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="494c8-136">DLL</span><span class="sxs-lookup"><span data-stu-id="494c8-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="494c8-137"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="494c8-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="494c8-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="494c8-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="494c8-139">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="494c8-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
