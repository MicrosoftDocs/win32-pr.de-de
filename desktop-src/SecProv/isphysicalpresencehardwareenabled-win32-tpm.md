---
description: Die isphysicalpresencehardwareaktivierte-Methode der Win32 \_ TPM-Klasse gibt an, ob die physische Präsenz auf der Plattform mit einem Hardware Signal festgelegt werden kann.
ms.assetid: 65dabfa9-bfbe-4b9b-8e80-02269895c7ad
title: Isphysicalpresencehardwareaktivierte Methode der Win32_Tpm-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.IsPhysicalPresenceHardwareEnabled
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 674dcaa733d8ec70af172359e3dcde0578955dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104393493"
---
# <a name="isphysicalpresencehardwareenabled-method-of-the-win32_tpm-class"></a><span data-ttu-id="1025c-103">Isphysicalpresencehardwareaktivierte Methode der Win32- \_ TPM-Klasse</span><span class="sxs-lookup"><span data-stu-id="1025c-103">IsPhysicalPresenceHardwareEnabled method of the Win32\_Tpm class</span></span>

<span data-ttu-id="1025c-104">Die **isphysicalpresencehardwareaktivierte** -Methode der [**Win32 \_ TPM**](win32-tpm.md) -Klasse gibt an, ob die physische Präsenz auf der Plattform mit einem Hardware Signal festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1025c-104">The **IsPhysicalPresenceHardwareEnabled** method of the [**Win32\_Tpm**](win32-tpm.md) class indicates whether physical presence on the platform can be set with a hardware signal.</span></span> <span data-ttu-id="1025c-105">Dieser Wert wird vom Platt Form Hersteller basierend auf dem Entwurf der Plattform konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="1025c-105">This value is configured by the platform manufacturer based on the design of the platform.</span></span> <span data-ttu-id="1025c-106">Die Dokumentation des Platt Form Herstellers bietet möglicherweise weitere Informationen.</span><span class="sxs-lookup"><span data-stu-id="1025c-106">Documentation from the platform manufacturer may provide additional information.</span></span>

## <a name="syntax"></a><span data-ttu-id="1025c-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="1025c-107">Syntax</span></span>


```mof
uint32 IsPhysicalPresenceHardwareEnabled(
  [out] boolean IsPhysicalPresenceHardwareEnabled
);
```



## <a name="parameters"></a><span data-ttu-id="1025c-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="1025c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1025c-109">*Isphysicalpresencehardwareaktivierte* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="1025c-109">*IsPhysicalPresenceHardwareEnabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1025c-110">Typ: **booleschen**</span><span class="sxs-lookup"><span data-stu-id="1025c-110">Type: **boolean**</span></span>

<span data-ttu-id="1025c-111">**True** gibt an, dass die physische Präsenz auf der Plattform mit einem Hardware Signal festgelegt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1025c-111">If **true**, physical presence on the platform can be set with a hardware signal.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1025c-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1025c-112">Return value</span></span>

<span data-ttu-id="1025c-113">Typ: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1025c-113">Type: **uint32**</span></span>

<span data-ttu-id="1025c-114">Alle TPM-Fehler sowie Fehler, die für die TPM-Basisdienste spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1025c-114">All TPM errors as well as errors specific to TPM Base Services can be returned.</span></span>

<span data-ttu-id="1025c-115">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="1025c-115">Common return codes are listed below.</span></span>



| <span data-ttu-id="1025c-116">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="1025c-116">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="1025c-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1025c-117">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="1025c-118"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="1025c-118"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="1025c-119">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="1025c-119">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1025c-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1025c-120">Remarks</span></span>

<span data-ttu-id="1025c-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="1025c-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="1025c-122">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="1025c-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="1025c-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="1025c-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="1025c-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="1025c-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1025c-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="1025c-125">Requirements</span></span>



| <span data-ttu-id="1025c-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="1025c-126">Requirement</span></span> | <span data-ttu-id="1025c-127">Wert</span><span class="sxs-lookup"><span data-stu-id="1025c-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="1025c-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="1025c-128">Minimum supported client</span></span><br/> | <span data-ttu-id="1025c-129">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1025c-129">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1025c-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="1025c-130">Minimum supported server</span></span><br/> | <span data-ttu-id="1025c-131">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="1025c-131">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="1025c-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="1025c-132">Namespace</span></span><br/>                | <span data-ttu-id="1025c-133">Root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="1025c-133">Root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                            |
| <span data-ttu-id="1025c-134">MOF</span><span class="sxs-lookup"><span data-stu-id="1025c-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1025c-135"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="1025c-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="1025c-136">DLL</span><span class="sxs-lookup"><span data-stu-id="1025c-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1025c-137"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1025c-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1025c-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1025c-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1025c-139">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="1025c-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
