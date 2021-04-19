---
description: Die isphysicalcleardeaktiviert-Methode der Win32- \_ TPM-Klasse gibt an, ob nur der Gerätebesitzer das Gerät löschen kann.
ms.assetid: b87f1c4f-8735-45c5-9256-53dbb9579f95
title: Isphysicalcleardeaktiviert-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalClearDisabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 9179aae2f4902ce29e2bab98b4c9c0b793804de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356919"
---
# <a name="isphysicalcleardisabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="0e235-103">Isphysicalcleardeaktiviert-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="0e235-103">IsPhysicalClearDisabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="0e235-104">Die **isphysicalcleardeaktiviert** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob nur der Gerätebesitzer das Gerät löschen kann.</span><span class="sxs-lookup"><span data-stu-id="0e235-104">The **IsPhysicalClearDisabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether only the device owner may be able to clear the device.</span></span>

## <a name="syntax"></a><span data-ttu-id="0e235-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0e235-105">Syntax</span></span>


```mof
uint32 IsPhysicalClearDisabled(
  [out] boolean IsPhysicalClearDisabled
);
```



## <a name="parameters"></a><span data-ttu-id="0e235-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0e235-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e235-107">*Isphysicalcleardeaktiviert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0e235-107">*IsPhysicalClearDisabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0e235-108">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="0e235-108">Type: **boolean**</span></span>

<span data-ttu-id="0e235-109">Wenn der Wert **true** ist, kann nur der Gerätebesitzer das Gerät löschen.</span><span class="sxs-lookup"><span data-stu-id="0e235-109">If **true**, only the device owner is able to clear the device.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0e235-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0e235-110">Return value</span></span>

<span data-ttu-id="0e235-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="0e235-111">Type: **uint32**</span></span>

<span data-ttu-id="0e235-112">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="0e235-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="0e235-113">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e235-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="0e235-114">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="0e235-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="0e235-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="0e235-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="0e235-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="0e235-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="0e235-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="0e235-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0e235-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0e235-118">Remarks</span></span>

<span data-ttu-id="0e235-119">Dieser Wert wird am Anfang jedes Start Zyklen auf **false** zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="0e235-119">This value is reset to **false** at the beginning of each startup cycle.</span></span>

<span data-ttu-id="0e235-120">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="0e235-120">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0e235-121">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="0e235-121">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="0e235-122">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0e235-122">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0e235-123">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="0e235-123">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0e235-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0e235-124">Requirements</span></span>



| <span data-ttu-id="0e235-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0e235-125">Requirement</span></span> | <span data-ttu-id="0e235-126">Wert</span><span class="sxs-lookup"><span data-stu-id="0e235-126">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e235-127">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0e235-127">Minimum supported client</span></span><br/> | <span data-ttu-id="0e235-128">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e235-128">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="0e235-129">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0e235-129">Minimum supported server</span></span><br/> | <span data-ttu-id="0e235-130">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0e235-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="0e235-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="0e235-131">Namespace</span></span><br/>                | <span data-ttu-id="0e235-132">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="0e235-132">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="0e235-133">MOF</span><span class="sxs-lookup"><span data-stu-id="0e235-133">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0e235-134"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0e235-134"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="0e235-135">DLL</span><span class="sxs-lookup"><span data-stu-id="0e235-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0e235-136"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0e235-136"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e235-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0e235-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e235-138">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="0e235-138">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
