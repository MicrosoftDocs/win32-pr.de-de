---
description: Die issrkauthcompatible-Methode der Win32- \_ TPM-Klasse gibt an, ob die SRK-Autorisierung (Storage Root Key) mit dem von Windows Vista erwarteten Wert kompatibel ist.
ms.assetid: ce6d05b8-673a-40ab-a1d7-3fedfd099306
title: Issrkauthcompatible-Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsSrkAuthCompatible
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: f5250f8d3f9ad38f9d4c46350e06e0fe32f756dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866956"
---
# <a name="issrkauthcompatible-method-of-the-win32_tpm-class"></a><span data-ttu-id="98958-103">Issrkauthcompatible-Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="98958-103">IsSrkAuthCompatible method of the Win32\_Tpm class</span></span>

<span data-ttu-id="98958-104">Die **issrkauthcompatible** -Methode der [**Win32- \_ TPM**](win32-tpm.md) -Klasse gibt an, ob die SRK-Autorisierung (Storage Root Key) mit dem von Windows Vista erwarteten Wert kompatibel ist.</span><span class="sxs-lookup"><span data-stu-id="98958-104">The **IsSrkAuthCompatible** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether the Storage Root Key (SRK) authorization is compatible with the value expected by Windows Vista.</span></span>

## <a name="syntax"></a><span data-ttu-id="98958-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="98958-105">Syntax</span></span>


```mof
uint32 IsSrkAuthCompatible(
  [out] boolean IsSrkAuthCompatible
);
```



## <a name="parameters"></a><span data-ttu-id="98958-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="98958-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="98958-107">*Issrkauthcompatible* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="98958-107">*IsSrkAuthCompatible* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="98958-108">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="98958-108">Type: **boolean**</span></span>

<span data-ttu-id="98958-109">**True** gibt an, dass der SRK-Autorisierungs Wert den Wert 0 (null) aufweist.</span><span class="sxs-lookup"><span data-stu-id="98958-109">If **true**, the SRK authorization value has a value of zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="98958-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="98958-110">Return value</span></span>

<span data-ttu-id="98958-111">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="98958-111">Type: **uint32**</span></span>

<span data-ttu-id="98958-112">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="98958-112">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="98958-113">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="98958-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="98958-114">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="98958-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="98958-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="98958-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="98958-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="98958-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="98958-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="98958-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="98958-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="98958-118">Remarks</span></span>

<span data-ttu-id="98958-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="98958-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="98958-120">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="98958-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="98958-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="98958-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="98958-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="98958-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="98958-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="98958-123">Requirements</span></span>



| <span data-ttu-id="98958-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="98958-124">Requirement</span></span> | <span data-ttu-id="98958-125">Wert</span><span class="sxs-lookup"><span data-stu-id="98958-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="98958-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="98958-126">Minimum supported client</span></span><br/> | <span data-ttu-id="98958-127">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98958-127">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="98958-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="98958-128">Minimum supported server</span></span><br/> | <span data-ttu-id="98958-129">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="98958-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="98958-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="98958-130">Namespace</span></span><br/>                | <span data-ttu-id="98958-131">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="98958-131">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="98958-132">MOF</span><span class="sxs-lookup"><span data-stu-id="98958-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="98958-133"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="98958-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="98958-134">DLL</span><span class="sxs-lookup"><span data-stu-id="98958-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="98958-135"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="98958-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="98958-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="98958-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="98958-137">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="98958-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
