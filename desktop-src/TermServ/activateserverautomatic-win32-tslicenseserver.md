---
title: Activateserverautomatic-Methode der Win32_TSLicenseServer-Klasse
description: Aktiviert den Remotedesktop Lizenzserver automatisch über das Internet.
ms.assetid: a33ba72f-3403-4bd2-94a9-0c5ef1cbb03e
ms.tgt_platform: multiple
keywords:
- Activateserverautomatic-Methode Remotedesktopdienste
- Activateserverautomatic-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, activateserverautomatic-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.ActivateServerAutomatic
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 68879dbc40cc4161edcfef631bf9bb4b72558df8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949634"
---
# <a name="activateserverautomatic-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="ee8a4-106">Activateserverautomatic-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="ee8a4-106">ActivateServerAutomatic method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="ee8a4-107">Aktiviert den Remotedesktop Lizenzserver automatisch über das Internet.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-107">Activates the Remote Desktop license server automatically over the Internet.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee8a4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee8a4-108">Syntax</span></span>


```mof
uint32 ActivateServerAutomatic(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="ee8a4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee8a4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee8a4-110">*Activationstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ee8a4-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee8a4-111">Der zurückgegebene Aktivierungs Status kann einer der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="ee8a4-112">0</span><span class="sxs-lookup"><span data-stu-id="ee8a4-112">0</span></span>
</dt> <dd>

<span data-ttu-id="ee8a4-113">Der Remotedesktop Lizenzserver wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="ee8a4-114">1</span><span class="sxs-lookup"><span data-stu-id="ee8a4-114">1</span></span>
</dt> <dd>

<span data-ttu-id="ee8a4-115">Der Remotedesktop Lizenzserver ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="ee8a4-116">2</span><span class="sxs-lookup"><span data-stu-id="ee8a4-116">2</span></span>
</dt> <dd>

<span data-ttu-id="ee8a4-117">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-117">An unknown error occurred.</span></span> <span data-ttu-id="ee8a4-118">Es ist nicht bekannt, ob der Remotedesktop Lizenzserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee8a4-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee8a4-119">Return value</span></span>

<span data-ttu-id="ee8a4-120">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ee8a4-121">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ee8a4-122">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ee8a4-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ee8a4-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ee8a4-123">Remarks</span></span>

<span data-ttu-id="ee8a4-124">Diese Methode schlägt fehl, es sei denn, die Eigenschaften **FirstName**, **LastName**, **Company** und **CountryRegion** sind festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-124">This method fails unless the **FirstName**, **LastName**, **Company**, and **CountryRegion** properties are set.</span></span>

<span data-ttu-id="ee8a4-125">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-125">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="ee8a4-126">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-126">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="ee8a4-127">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-127">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="ee8a4-128">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ee8a4-128">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="ee8a4-129">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="ee8a4-129">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="ee8a4-130">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee8a4-130">Requirements</span></span>



| <span data-ttu-id="ee8a4-131">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee8a4-131">Requirement</span></span> | <span data-ttu-id="ee8a4-132">Wert</span><span class="sxs-lookup"><span data-stu-id="ee8a4-132">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee8a4-133">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee8a4-133">Minimum supported client</span></span><br/> | <span data-ttu-id="ee8a4-134">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ee8a4-134">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ee8a4-135">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee8a4-135">Minimum supported server</span></span><br/> | <span data-ttu-id="ee8a4-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ee8a4-136">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ee8a4-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee8a4-137">Namespace</span></span><br/>                | <span data-ttu-id="ee8a4-138">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ee8a4-138">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ee8a4-139">MOF</span><span class="sxs-lookup"><span data-stu-id="ee8a4-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee8a4-140"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ee8a4-140"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee8a4-141">DLL</span><span class="sxs-lookup"><span data-stu-id="ee8a4-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee8a4-142"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee8a4-142"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee8a4-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee8a4-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee8a4-144">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="ee8a4-144">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

