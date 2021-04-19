---
description: Die isownercleardeaktiviert-Methode der Win32 \_ TPM-Klasse gibt an, ob der Gerätebesitzer das Löschen des Geräts einschränkt.
ms.assetid: 04f98e9b-c1a0-4828-b7cb-67b32d7470ea
title: Isownercleardeaktiviert-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsOwnerClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 13e8b7de707cb1b1af4d4ccdb1208c6391e26987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357926"
---
# <a name="isownercleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="5ee43-103">Isownercleardeaktiviert-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="5ee43-103">IsOwnerClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="5ee43-104">Die **isownercleardeaktiviert** -Methode der [**Win32 \_ TPM**](win32-tpm.md) -Klasse gibt an, ob der Gerätebesitzer das Löschen des Geräts einschränkt.</span><span class="sxs-lookup"><span data-stu-id="5ee43-104">The **IsOwnerClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the device owner is restricted from clearing the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="5ee43-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="5ee43-105">Syntax</span></span>


```mof
uint32 IsOwnerClearDisabled(
  [out] boolean IsOwnerClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="5ee43-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="5ee43-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5ee43-107">*Isownercleardeaktiviert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="5ee43-107">*IsOwnerClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5ee43-108">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="5ee43-108">Type: **boolean**</span></span>

<span data-ttu-id="5ee43-109">**True** gibt an, dass der Gerätebesitzer das Gerät nicht löschen kann.</span><span class="sxs-lookup"><span data-stu-id="5ee43-109">If **true**, the device owner is unable to clear the device.</span></span> <span data-ttu-id="5ee43-110">Das Gerät kann nur von einem physisch vorhandenen Benutzer gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="5ee43-110">Only a physically present user may be able to clear the device.</span></span> <span data-ttu-id="5ee43-111">Wenn der Wert **false** ist, kann der Gerätebesitzer das Gerät löschen.</span><span class="sxs-lookup"><span data-stu-id="5ee43-111">If **false**, the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5ee43-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="5ee43-112">Return value</span></span>

<span data-ttu-id="5ee43-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="5ee43-113">Type: **uint32**</span></span>

<span data-ttu-id="5ee43-114">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="5ee43-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="5ee43-115">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="5ee43-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="5ee43-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="5ee43-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="5ee43-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5ee43-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="5ee43-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="5ee43-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="5ee43-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="5ee43-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5ee43-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5ee43-120">Remarks</span></span>

<span data-ttu-id="5ee43-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="5ee43-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="5ee43-122">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="5ee43-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="5ee43-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="5ee43-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="5ee43-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="5ee43-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="5ee43-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="5ee43-125">Requirements</span></span>



| <span data-ttu-id="5ee43-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="5ee43-126">Requirement</span></span> | <span data-ttu-id="5ee43-127">Wert</span><span class="sxs-lookup"><span data-stu-id="5ee43-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="5ee43-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="5ee43-128">Minimum supported client</span></span><br/> | <span data-ttu-id="5ee43-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ee43-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="5ee43-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="5ee43-130">Minimum supported server</span></span><br/> | <span data-ttu-id="5ee43-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="5ee43-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="5ee43-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="5ee43-132">Namespace</span></span><br/>                | <span data-ttu-id="5ee43-133">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="5ee43-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="5ee43-134">MOF</span><span class="sxs-lookup"><span data-stu-id="5ee43-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="5ee43-135"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="5ee43-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="5ee43-136">DLL</span><span class="sxs-lookup"><span data-stu-id="5ee43-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5ee43-137"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5ee43-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5ee43-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5ee43-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5ee43-139">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="5ee43-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
