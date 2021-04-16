---
description: Die isowned-Methode der Win32- \_ TPM-Klasse gibt an, ob das Gerät über einen Besitzer verfügt. Dieser Wert wird von der TakeOwnership-Methode geändert.
ms.assetid: 04a9394f-98de-43e3-8a19-7a8f409823b8
title: Isowned-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwned
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 6ad2d7d03059d8f96fe726d50ea18c2a70db64f4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525676"
---
# <a name="isowned-method-of-the-win32_tpm-class"></a><span data-ttu-id="72ab9-104">Isowned-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="72ab9-104">IsOwned method of the Win32\_Tpm class</span></span>

<span data-ttu-id="72ab9-105">Die **isowned** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob das Gerät über einen Besitzer verfügt.</span><span class="sxs-lookup"><span data-stu-id="72ab9-105">The **IsOwned** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device has an owner.</span></span> <span data-ttu-id="72ab9-106">Dieser Wert wird von der [**TakeOwnership**](takeownership-win32-tpm.md) -Methode geändert.</span><span class="sxs-lookup"><span data-stu-id="72ab9-106">This value is changed by the [**TakeOwnership**](takeownership-win32-tpm.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="72ab9-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="72ab9-107">Syntax</span></span>


```mof
uint32 IsOwned(
  [out] boolean IsOwned
);
```



## <a name="parameters"></a><span data-ttu-id="72ab9-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="72ab9-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72ab9-109">*Isowned* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="72ab9-109">*IsOwned* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="72ab9-110">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="72ab9-110">Type: **boolean**</span></span>

<span data-ttu-id="72ab9-111">**True** gibt an, dass das Gerät über einen Besitzer verfügt.</span><span class="sxs-lookup"><span data-stu-id="72ab9-111">If **true**, the device has an owner.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72ab9-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="72ab9-112">Return value</span></span>

<span data-ttu-id="72ab9-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="72ab9-113">Type: **uint32**</span></span>

<span data-ttu-id="72ab9-114">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="72ab9-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="72ab9-115">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="72ab9-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="72ab9-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="72ab9-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="72ab9-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="72ab9-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="72ab9-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="72ab9-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="72ab9-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="72ab9-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="72ab9-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72ab9-120">Remarks</span></span>

<span data-ttu-id="72ab9-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="72ab9-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="72ab9-122">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="72ab9-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="72ab9-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="72ab9-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="72ab9-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="72ab9-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="72ab9-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="72ab9-125">Requirements</span></span>



| <span data-ttu-id="72ab9-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="72ab9-126">Requirement</span></span> | <span data-ttu-id="72ab9-127">Wert</span><span class="sxs-lookup"><span data-stu-id="72ab9-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="72ab9-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="72ab9-128">Minimum supported client</span></span><br/> | <span data-ttu-id="72ab9-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72ab9-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="72ab9-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="72ab9-130">Minimum supported server</span></span><br/> | <span data-ttu-id="72ab9-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="72ab9-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="72ab9-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="72ab9-132">Namespace</span></span><br/>                | <span data-ttu-id="72ab9-133">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="72ab9-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="72ab9-134">MOF</span><span class="sxs-lookup"><span data-stu-id="72ab9-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="72ab9-135"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="72ab9-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="72ab9-136">DLL</span><span class="sxs-lookup"><span data-stu-id="72ab9-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72ab9-137"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72ab9-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72ab9-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="72ab9-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72ab9-139">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="72ab9-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
