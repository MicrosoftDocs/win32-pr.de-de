---
description: Ruft die Besitzer Autorisierungs Informationen für ein TPM ab, sofern in der Registrierung eine verfügbar ist.
ms.assetid: 3E2C28C8-4154-4B1B-9C47-AEDFD5622979
title: 'Win32_Tpm:: getownerauth-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: a441b07af31758212152b657ccb033d8abdeebbb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525667"
---
# <a name="win32_tpmgetownerauth-method"></a><span data-ttu-id="872a0-103">Win32 \_ TPM:: getownerauth-Methode</span><span class="sxs-lookup"><span data-stu-id="872a0-103">Win32\_Tpm::GetOwnerAuth method</span></span>

<span data-ttu-id="872a0-104">Ruft die Besitzer Autorisierungs Informationen für ein TPM ab, sofern in der Registrierung eine verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="872a0-104">Gets the owner authorization information for a TPM if one is available in the registry.</span></span> <span data-ttu-id="872a0-105">Wenn ein TPM im Besitz von Windows 8 mit den Standardeinstellungen ist, werden die TPM-Besitzer Autorisierungs Informationen in der Registrierung gespeichert und können von dieser Methode verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="872a0-105">If a TPM is owned or provisioned in Windows 8 with the default settings, the TPM owner authorization information is stored in the registry and is available for use by this method.</span></span>

<span data-ttu-id="872a0-106">Diese Methode ist nur für lokale Administratoren zugänglich.</span><span class="sxs-lookup"><span data-stu-id="872a0-106">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="872a0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="872a0-107">Syntax</span></span>


```C++
uint32 GetOwnerAuth(
  [out] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="872a0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="872a0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="872a0-109">Besitzer *des Besitzers* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="872a0-109">*OwnerAuth* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="872a0-110">Die Besitzer Autorisierungs Informationen für ein TPM, sofern in der Registrierung eine verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="872a0-110">The owner authorization information for a TPM, if one is available in the registry.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="872a0-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="872a0-111">Return value</span></span>

<span data-ttu-id="872a0-112">Alle TPM-Fehler sowie Fehler, die für die [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="872a0-112">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="872a0-113">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="872a0-113">Common return codes are listed below.</span></span>



| <span data-ttu-id="872a0-114">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="872a0-114">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="872a0-115">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="872a0-115">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="872a0-116"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="872a0-116"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="872a0-117">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="872a0-117">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="872a0-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="872a0-118">Remarks</span></span>

<span data-ttu-id="872a0-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="872a0-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="872a0-120">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="872a0-120">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="872a0-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="872a0-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="872a0-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="872a0-122">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="872a0-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="872a0-123">Requirements</span></span>



| <span data-ttu-id="872a0-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="872a0-124">Requirement</span></span> | <span data-ttu-id="872a0-125">Wert</span><span class="sxs-lookup"><span data-stu-id="872a0-125">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="872a0-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="872a0-126">Minimum supported client</span></span><br/> | <span data-ttu-id="872a0-127">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="872a0-127">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="872a0-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="872a0-128">Minimum supported server</span></span><br/> | <span data-ttu-id="872a0-129">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="872a0-129">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="872a0-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="872a0-130">Namespace</span></span><br/>                | <span data-ttu-id="872a0-131">\\\\.\\ root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="872a0-131">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="872a0-132">MOF</span><span class="sxs-lookup"><span data-stu-id="872a0-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="872a0-133"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="872a0-133"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="872a0-134">DLL</span><span class="sxs-lookup"><span data-stu-id="872a0-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="872a0-135"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="872a0-135"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="872a0-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="872a0-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="872a0-137">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="872a0-137">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
