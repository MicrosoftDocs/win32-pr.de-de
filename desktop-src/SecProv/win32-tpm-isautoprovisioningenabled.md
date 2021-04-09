---
description: Gibt an, ob die automatische Bereitstellung des TPM aktiviert ist.
ms.assetid: C908673C-8BDB-4541-85C6-65FED1EBB535
title: 'Win32_Tpm:: isautoprovisioningenabled-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsAutoProvisioningEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: cb269247292646464c6126a2588a50d77b19db9f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866947"
---
# <a name="win32_tpmisautoprovisioningenabled-method"></a><span data-ttu-id="f9ec9-103">Win32 \_ TPM:: isautoprovisioningenabled-Methode</span><span class="sxs-lookup"><span data-stu-id="f9ec9-103">Win32\_Tpm::IsAutoProvisioningEnabled method</span></span>

<span data-ttu-id="f9ec9-104">Gibt an, ob die automatische Bereitstellung des TPM aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-104">Indicates if auto provisioning of the TPM is enabled.</span></span> <span data-ttu-id="f9ec9-105">Standardmäßig ist die automatische Bereitstellung für Windows 8 und Windows Server 2012 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-105">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="f9ec9-106">Diese Methode ist nur für lokale Administratoren zugänglich.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9ec9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9ec9-107">Syntax</span></span>


```C++
uint32 IsAutoProvisioningEnabled(
  [out] BOOL IsAutoProvisioningEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="f9ec9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9ec9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9ec9-109">*Isautoprovisioningenabled* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="f9ec9-109">*IsAutoProvisioningEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f9ec9-110">Legen Sie diese Einstellung auf **true** fest, wenn die automatische TPM-Bereitstellung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-110">Set to **TRUE** if the TPM auto provisioning is enabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9ec9-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9ec9-111">Return value</span></span>

<span data-ttu-id="f9ec9-112">Alle TPM-Fehler sowie Fehler, die für die [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="f9ec9-113">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="f9ec9-114">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="f9ec9-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="f9ec9-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f9ec9-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="f9ec9-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="f9ec9-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="f9ec9-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="f9ec9-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9ec9-118">Remarks</span></span>

<span data-ttu-id="f9ec9-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f9ec9-120">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="f9ec9-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f9ec9-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f9ec9-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="f9ec9-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9ec9-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9ec9-123">Requirements</span></span>



| <span data-ttu-id="f9ec9-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9ec9-124">Requirement</span></span> | <span data-ttu-id="f9ec9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="f9ec9-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="f9ec9-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9ec9-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f9ec9-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9ec9-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="f9ec9-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9ec9-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f9ec9-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="f9ec9-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="f9ec9-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9ec9-130">Namespace</span></span><br/>                | <span data-ttu-id="f9ec9-131">\\\\.\\ root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="f9ec9-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="f9ec9-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f9ec9-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9ec9-133"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f9ec9-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9ec9-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f9ec9-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9ec9-135"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9ec9-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9ec9-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9ec9-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9ec9-137">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="f9ec9-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
