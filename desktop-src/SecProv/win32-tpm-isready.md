---
description: Gibt an, ob das TPM einsatzbereit ist.
ms.assetid: 70E9EB90-DC13-4431-97E5-D77B4E345373
title: 'Win32_Tpm:: isReady-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsReady
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 37c9d579e424c89f8670838b09ed1c557514ca00
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525664"
---
# <a name="win32_tpmisready-method"></a><span data-ttu-id="741ec-103">Win32 \_ TPM:: isReady-Methode</span><span class="sxs-lookup"><span data-stu-id="741ec-103">Win32\_Tpm::IsReady method</span></span>

<span data-ttu-id="741ec-104">Gibt an, ob das TPM einsatzbereit ist.</span><span class="sxs-lookup"><span data-stu-id="741ec-104">Indicates whether the TPM is ready for use.</span></span>

<span data-ttu-id="741ec-105">Diese Methode ist nur für lokale Administratoren zugänglich.</span><span class="sxs-lookup"><span data-stu-id="741ec-105">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="741ec-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="741ec-106">Syntax</span></span>


```C++
uint32 IsReady(
  [out] BOOL IsReady
);
```



## <a name="parameters"></a><span data-ttu-id="741ec-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="741ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="741ec-108">*IsReady* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="741ec-108">*IsReady* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="741ec-109">Legen Sie diese Einstellung auf " **true** " fest, wenn TPM und System vollständig für die TPM-Verwendung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="741ec-109">Set to **TRUE** if the TPM and system are fully provisioned for TPM use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="741ec-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="741ec-110">Return value</span></span>

<span data-ttu-id="741ec-111">Alle TPM-Fehler sowie Fehler, die für die [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="741ec-111">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="741ec-112">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="741ec-112">Common return codes are listed below.</span></span>



| <span data-ttu-id="741ec-113">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="741ec-113">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="741ec-114">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="741ec-114">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="741ec-115"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="741ec-115"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="741ec-116">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="741ec-116">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="741ec-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="741ec-117">Remarks</span></span>

<span data-ttu-id="741ec-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="741ec-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="741ec-119">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="741ec-119">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="741ec-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="741ec-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="741ec-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="741ec-121">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="741ec-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="741ec-122">Requirements</span></span>



| <span data-ttu-id="741ec-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="741ec-123">Requirement</span></span> | <span data-ttu-id="741ec-124">Wert</span><span class="sxs-lookup"><span data-stu-id="741ec-124">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="741ec-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="741ec-125">Minimum supported client</span></span><br/> | <span data-ttu-id="741ec-126">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="741ec-126">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="741ec-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="741ec-127">Minimum supported server</span></span><br/> | <span data-ttu-id="741ec-128">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="741ec-128">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="741ec-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="741ec-129">Namespace</span></span><br/>                | <span data-ttu-id="741ec-130">\\\\.\\ root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="741ec-130">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="741ec-131">MOF</span><span class="sxs-lookup"><span data-stu-id="741ec-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="741ec-132"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="741ec-132"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="741ec-133">DLL</span><span class="sxs-lookup"><span data-stu-id="741ec-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="741ec-134"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="741ec-134"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="741ec-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="741ec-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="741ec-136">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="741ec-136">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
