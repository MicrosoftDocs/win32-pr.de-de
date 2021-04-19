---
description: Ruft den Speicher Stamm Schlüssel-Fingerabdruck für einen angegebenen Modulo des öffentlichen Teils des TPM-Speicher Stamm Schlüssels ab.
ms.assetid: 08CBEB19-ECF5-4E43-B4A4-0F35987173E1
title: 'Win32_Tpm:: gezrkadthumbprint-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_Tpm.GetSrkADThumbprint
api_type:
- COM
api_location:
- Win32_tpm.dll
ms.openlocfilehash: 81e1ec53596a3d5ce469d412e9bd7ca17e1ad8b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344423"
---
# <a name="win32_tpmgetsrkadthumbprint-method"></a><span data-ttu-id="db9a3-103">Win32 \_ TPM:: gezrkadthumbprint-Methode</span><span class="sxs-lookup"><span data-stu-id="db9a3-103">Win32\_Tpm::GetSrkADThumbprint method</span></span>

<span data-ttu-id="db9a3-104">Ruft den Speicher Stamm Schlüssel-Fingerabdruck für einen angegebenen Modulo des öffentlichen Teils des TPM-Speicher Stamm Schlüssels ab.</span><span class="sxs-lookup"><span data-stu-id="db9a3-104">Gets the Storage root key thumbprint for a given modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="db9a3-105">Der Fingerabdruck wird zum Indizieren der Speicher Stamm Schlüssel auf dem Active Directory Server verwendet, wenn die Active Directory Sicherung der TPM-Besitzer Autorisierungs Informationen durch Gruppenrichtlinie Einstellung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="db9a3-105">The thumbprint is used to index the Storage Root Keys on the Active Directory server if the Active Directory backup of TPM owner authorization information is enabled through Group Policy setting.</span></span>

> [!Note]  
> <span data-ttu-id="db9a3-106">Ab Windows 10, Version 1607, wird die TPM-Besitzer Autorisierung nie auf Active Directory gesichert.</span><span class="sxs-lookup"><span data-stu-id="db9a3-106">Beginning with Windows 10, version 1607, the TPM owner authorization is never backed up to Active Directory.</span></span>

 

<span data-ttu-id="db9a3-107">Diese Methode ist nur für lokale Administratoren zugänglich.</span><span class="sxs-lookup"><span data-stu-id="db9a3-107">This method is only accessible by local administrators.</span></span>

## <a name="syntax"></a><span data-ttu-id="db9a3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="db9a3-108">Syntax</span></span>


```C++
uint32 GetSrkADThumbprint(
  [in]  uint8 SrkPublicKeyModulus,
  [out] uint8 SrkADThumbprint
);
```



## <a name="parameters"></a><span data-ttu-id="db9a3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="db9a3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="db9a3-110">*Srkpublickeymodulus* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="db9a3-110">*SrkPublicKeyModulus* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="db9a3-111">Der Modulo des öffentlichen Teils des TPM-Speicher Stamm Schlüssels.</span><span class="sxs-lookup"><span data-stu-id="db9a3-111">The modulus of the public portion of the TPM Storage Root Key.</span></span> <span data-ttu-id="db9a3-112">Sie kann auch mithilfe der [**getrkpublickeymodulus**](win32-tpm-getsrkpublickeymodulus.md) -Methode der [Win32 \_ TPM](win32-tpm.md) -Klasse abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="db9a3-112">It can also be obtained using the [**GetSrkPublicKeyModulus**](win32-tpm-getsrkpublickeymodulus.md) method of the [Win32\_TPM](win32-tpm.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="db9a3-113">*Srkadthumbprint* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="db9a3-113">*SrkADThumbprint* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="db9a3-114">Gibt ein 20-Byte-Array zurück, das den Speicher Stamm Schlüssel-Fingerabdruck für den angegebenen Modulus enthält.</span><span class="sxs-lookup"><span data-stu-id="db9a3-114">Returns a 20-byte array containing the storage root key thumbprint for the given modulus.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="db9a3-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="db9a3-115">Return value</span></span>

<span data-ttu-id="db9a3-116">Alle TPM-Fehler sowie Fehler, die für die [TPM-Basisdienste](../tbs/tbs-return-codes.md) spezifisch sind, können zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="db9a3-116">All TPM errors as well as errors specific to [TPM Base Services](../tbs/tbs-return-codes.md) can be returned.</span></span>

<span data-ttu-id="db9a3-117">Allgemeine Rückgabecodes sind unten aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="db9a3-117">Common return codes are listed below.</span></span>



| <span data-ttu-id="db9a3-118">Rückgabecode/-wert</span><span class="sxs-lookup"><span data-stu-id="db9a3-118">Return code/value</span></span>                                                                                                                                 | <span data-ttu-id="db9a3-119">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="db9a3-119">Description</span></span>                           |
|---------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <span data-ttu-id="db9a3-120"><dt>**S \_ OK**</dt> <dt>0 (0x0)</dt></span><span class="sxs-lookup"><span data-stu-id="db9a3-120"><dt>**S\_OK**</dt> <dt>0 (0x0)</dt></span></span> </dl> | <span data-ttu-id="db9a3-121">Die Methode war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="db9a3-121">The method was successful.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="db9a3-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="db9a3-122">Remarks</span></span>

<span data-ttu-id="db9a3-123">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="db9a3-123">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="db9a3-124">MOF-Dateien werden nicht als Teil des Windows SDK installiert.</span><span class="sxs-lookup"><span data-stu-id="db9a3-124">MOF files are not installed as part of the Windows SDK.</span></span> <span data-ttu-id="db9a3-125">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="db9a3-125">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="db9a3-126">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span><span class="sxs-lookup"><span data-stu-id="db9a3-126">For more information about MOF files, see [Managed Object Format (MOF)](../wmisdk/managed-object-format--mof-.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="db9a3-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="db9a3-127">Requirements</span></span>



| <span data-ttu-id="db9a3-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="db9a3-128">Requirement</span></span> | <span data-ttu-id="db9a3-129">Wert</span><span class="sxs-lookup"><span data-stu-id="db9a3-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="db9a3-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="db9a3-130">Minimum supported client</span></span><br/> | <span data-ttu-id="db9a3-131">Nur Windows 8 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db9a3-131">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="db9a3-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="db9a3-132">Minimum supported server</span></span><br/> | <span data-ttu-id="db9a3-133">Nur Windows Server 2012 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="db9a3-133">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="db9a3-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="db9a3-134">Namespace</span></span><br/>                | <span data-ttu-id="db9a3-135">\\\\.\\ root \\ CIMV2 \\ Security- \\ mikrosofttpm</span><span class="sxs-lookup"><span data-stu-id="db9a3-135">\\\\.\\root\\CIMV2\\Security\\MicrosoftTpm</span></span><br/>                                     |
| <span data-ttu-id="db9a3-136">MOF</span><span class="sxs-lookup"><span data-stu-id="db9a3-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="db9a3-137"><dt>Win32- \_ TPM. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="db9a3-137"><dt>Win32\_tpm.mof</dt></span></span> </dl> |
| <span data-ttu-id="db9a3-138">DLL</span><span class="sxs-lookup"><span data-stu-id="db9a3-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="db9a3-139"><dt>Win32- \_tpm.dll</dt></span><span class="sxs-lookup"><span data-stu-id="db9a3-139"><dt>Win32\_tpm.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="db9a3-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db9a3-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="db9a3-141">**Win32- \_ TPM**</span><span class="sxs-lookup"><span data-stu-id="db9a3-141">**Win32\_Tpm**</span></span>](win32-tpm.md)
</dt> </dl>

 

 
