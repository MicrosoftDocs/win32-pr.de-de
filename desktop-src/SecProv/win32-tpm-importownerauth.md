---
description: Importiert die Besitzer Autorisierungs Informationen für ein TPM, das bereits in der Registrierung des Betriebssystems vorhanden ist.
ms.assetid: 9611D363-6F10-48B9-B417-97133E975257
title: 'Win32_Tpm:: importownerauth-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.ImportOwnerAuth
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: c74d99ab5cf101aa424dcf1921da774f53e21de6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958828"
---
# <a name="win32_tpmimportownerauth-method"></a><span data-ttu-id="15fed-103">Win32 \_ TPM:: importownerauth-Methode</span><span class="sxs-lookup"><span data-stu-id="15fed-103">Win32\_Tpm::ImportOwnerAuth method</span></span>

<span data-ttu-id="15fed-104">Importiert die Besitzer Autorisierungs Informationen für ein TPM, das bereits in der Registrierung des Betriebssystems vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="15fed-104">Imports the owner authorization information for a TPM that is already owned into the operating system registry.</span></span> <span data-ttu-id="15fed-105">Mit diesem Vorgang wird zuerst überprüft, ob die angegebenen Besitzer Autorisierungs Informationen korrekt sind.</span><span class="sxs-lookup"><span data-stu-id="15fed-105">This operation will first validate if the supplied owner authorization information is correct.</span></span> <span data-ttu-id="15fed-106">Wenn dies richtig ist, importiert die-Methode diese Informationen in die Registrierung.</span><span class="sxs-lookup"><span data-stu-id="15fed-106">If correct, the method imports this information to the registry.</span></span>

<span data-ttu-id="15fed-107">Diese Methode ist nur für lokale Administratoren zugänglich.</span><span class="sxs-lookup"><span data-stu-id="15fed-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="15fed-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="15fed-108">Syntax</span></span>


```C++
uint32 ImportOwnerAuth(
  [in] STRING OwnerAuth
);
```



## <a name="parameters"></a><span data-ttu-id="15fed-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="15fed-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="15fed-110">Besitzer *des Besitzers* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="15fed-110">*OwnerAuth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="15fed-111">Die gültigen Autorisierungs Informationen des Besitzers für das TPM.</span><span class="sxs-lookup"><span data-stu-id="15fed-111">The valid owner authorization information for the TPM.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="15fed-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="15fed-112">Return value</span></span>

<span data-ttu-id="15fed-113">Alle TPM-Fehler sowie Fehler, die für die [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="15fed-113">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="15fed-114">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="15fed-114">Common return codes are listed below.</span></span>



| <span data-ttu-id="15fed-115">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="15fed-115">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="15fed-116">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="15fed-116">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="15fed-117"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="15fed-117"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="15fed-118">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="15fed-118">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="15fed-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="15fed-119">Remarks</span></span>

<span data-ttu-id="15fed-120">Diese Methode ist besonders nützlich in Szenarien, in denen sich das TPM im Zustand "bereit mit eingeschränkter Funktionalität" befindet und erfordert, dass die Autorisierung des Besitzers vollständig bereit ist, oder in einem Dual-Boot-Szenario, in dem eines der Betriebssysteme im Besitz des TPM ist und die Autorisierungs Informationen für das TPM im anderen Betriebssystem nicht verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="15fed-120">This method is particularly useful in the scenarios where the TPM is in a "ready with reduced functionality state " and requires the importing of the owner authorization to be fully ready or in a dual-boot scenarios where one of the operating systems has owned the TPM and the owner authorization information for TPM is not available in the other operating system.</span></span>

<span data-ttu-id="15fed-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="15fed-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="15fed-122">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="15fed-122">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="15fed-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="15fed-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="15fed-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="15fed-124">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="15fed-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="15fed-125">Requirements</span></span>



| <span data-ttu-id="15fed-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="15fed-126">Requirement</span></span> | <span data-ttu-id="15fed-127">Wert</span><span class="sxs-lookup"><span data-stu-id="15fed-127">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="15fed-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="15fed-128">Minimum supported client</span></span><br/> | <span data-ttu-id="15fed-129">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15fed-129">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="15fed-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="15fed-130">Minimum supported server</span></span><br/> | <span data-ttu-id="15fed-131">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="15fed-131">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="15fed-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="15fed-132">Namespace</span></span><br/>                | <span data-ttu-id="15fed-133">\\\\.\\ root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="15fed-133">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="15fed-134">MOF</span><span class="sxs-lookup"><span data-stu-id="15fed-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="15fed-135"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="15fed-135"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="15fed-136">DLL</span><span class="sxs-lookup"><span data-stu-id="15fed-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="15fed-137"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="15fed-137"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="15fed-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15fed-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="15fed-139">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="15fed-139">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
