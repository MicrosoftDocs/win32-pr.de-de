---
description: Aktiviert die automatische Bereitstellung des TPM, wenn es derzeit deaktiviert ist.
ms.assetid: 70F56A4C-F936-4CB6-83F6-F3B691F43B98
title: 'Win32_Tpm:: enableautoprovisioning-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.EnableAutoProvisioning
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 5288be5c9822b7e76b0cb25b60ee68dacc36d5e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104343068"
---
# <a name="win32_tpmenableautoprovisioning-method"></a><span data-ttu-id="1b03e-103">Win32 \_ TPM:: enableautoprovisioning-Methode</span><span class="sxs-lookup"><span data-stu-id="1b03e-103">Win32\_Tpm::EnableAutoProvisioning method</span></span>

<span data-ttu-id="1b03e-104">Aktiviert die automatische Bereitstellung des TPM, wenn es derzeit deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1b03e-104">Enables auto provisioning of the TPM if it is currently disabled.</span></span> <span data-ttu-id="1b03e-105">Der Vorgang hat keine Auswirkung, wenn die automatische Bereitstellung bereits aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="1b03e-105">The operation has no effect if auto provisioning is already enabled.</span></span> <span data-ttu-id="1b03e-106">Standardmäßig ist die automatische Bereitstellung für Windows 8 und Windows Server 2012 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="1b03e-106">By default, auto provisioning is enabled for Windows 8 and Windows Server 2012.</span></span>

<span data-ttu-id="1b03e-107">Diese Methode ist nur für lokale Administratoren zugänglich.</span><span class="sxs-lookup"><span data-stu-id="1b03e-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b03e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="1b03e-108">Syntax</span></span>


```C++
uint32 EnableAutoProvisioning();
```



## <a name="parameters"></a><span data-ttu-id="1b03e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="1b03e-109">Parameters</span></span>

<span data-ttu-id="1b03e-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="1b03e-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1b03e-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1b03e-111">Return value</span></span>

<span data-ttu-id="1b03e-112">Alle TPM-Fehler sowie Fehler, die für die [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1b03e-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="1b03e-113">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b03e-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="1b03e-114">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="1b03e-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="1b03e-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b03e-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1b03e-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1b03e-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="1b03e-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1b03e-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1b03e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1b03e-118">Remarks</span></span>

<span data-ttu-id="1b03e-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="1b03e-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1b03e-120">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="1b03e-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1b03e-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1b03e-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1b03e-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1b03e-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1b03e-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1b03e-123">Requirements</span></span>



| <span data-ttu-id="1b03e-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1b03e-124">Requirement</span></span> | <span data-ttu-id="1b03e-125">Wert</span><span class="sxs-lookup"><span data-stu-id="1b03e-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1b03e-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1b03e-126">Minimum supported client</span></span><br/> | <span data-ttu-id="1b03e-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b03e-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="1b03e-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1b03e-128">Minimum supported server</span></span><br/> | <span data-ttu-id="1b03e-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1b03e-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1b03e-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="1b03e-130">Namespace</span></span><br/>                | <span data-ttu-id="1b03e-131">\\\\.\\ root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="1b03e-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="1b03e-132">MOF</span><span class="sxs-lookup"><span data-stu-id="1b03e-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1b03e-133"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1b03e-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="1b03e-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1b03e-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1b03e-135"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1b03e-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1b03e-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1b03e-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b03e-137">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="1b03e-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
