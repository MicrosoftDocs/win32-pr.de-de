---
title: Getactivationstatus-Methode der Win32_TSLicenseServer-Klasse
description: Ruft den aktuellen Aktivierungs Status des Remotedesktop Lizenzservers ab.
ms.assetid: 1148ffc5-33c1-41f1-b477-78a5293333d1
ms.tgt_platform: multiple
keywords:
- Getactivationstatus-Methode Remotedesktopdienste
- Getactivationstatus-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, getactivationstatus-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.GetActivationStatus
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 882f6209cd13c2372316e6a9606a3bc4fcd60fdc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104337"
---
# <a name="getactivationstatus-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="3a0bd-106">Getactivationstatus-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="3a0bd-106">GetActivationStatus method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="3a0bd-107">Ruft den aktuellen Aktivierungs Status des Remotedesktop Lizenzservers ab.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-107">Retrieves the current activation status of the Remote Desktop license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a0bd-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a0bd-108">Syntax</span></span>


```mof
uint32 GetActivationStatus(
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="3a0bd-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a0bd-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3a0bd-110">*Activationstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="3a0bd-110">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3a0bd-111">Der zurückgegebene Aktivierungs Status kann einer der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-111">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="3a0bd-112">0</span><span class="sxs-lookup"><span data-stu-id="3a0bd-112">0</span></span>
</dt> <dd>

<span data-ttu-id="3a0bd-113">Der Remotedesktop Lizenzserver wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-113">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="3a0bd-114">1</span><span class="sxs-lookup"><span data-stu-id="3a0bd-114">1</span></span>
</dt> <dd>

<span data-ttu-id="3a0bd-115">Der Remotedesktop Lizenzserver ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-115">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="3a0bd-116">2</span><span class="sxs-lookup"><span data-stu-id="3a0bd-116">2</span></span>
</dt> <dd>

<span data-ttu-id="3a0bd-117">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-117">An unknown error occurred.</span></span> <span data-ttu-id="3a0bd-118">Es ist nicht bekannt, ob der Remotedesktop Lizenzserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-118">It is not known whether the Remote Desktop license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3a0bd-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a0bd-119">Return value</span></span>

<span data-ttu-id="3a0bd-120">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-120">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="3a0bd-121">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-121">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="3a0bd-122">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="3a0bd-122">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="3a0bd-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a0bd-123">Remarks</span></span>

<span data-ttu-id="3a0bd-124">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-124">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="3a0bd-125">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-125">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3a0bd-126">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-126">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3a0bd-127">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3a0bd-127">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3a0bd-128">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3a0bd-128">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3a0bd-129">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3a0bd-129">Requirements</span></span>



| <span data-ttu-id="3a0bd-130">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a0bd-130">Requirement</span></span> | <span data-ttu-id="3a0bd-131">Wert</span><span class="sxs-lookup"><span data-stu-id="3a0bd-131">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a0bd-132">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a0bd-132">Minimum supported client</span></span><br/> | <span data-ttu-id="3a0bd-133">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3a0bd-133">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="3a0bd-134">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a0bd-134">Minimum supported server</span></span><br/> | <span data-ttu-id="3a0bd-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3a0bd-135">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="3a0bd-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="3a0bd-136">Namespace</span></span><br/>                | <span data-ttu-id="3a0bd-137">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3a0bd-137">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="3a0bd-138">MOF</span><span class="sxs-lookup"><span data-stu-id="3a0bd-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3a0bd-139"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="3a0bd-139"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="3a0bd-140">DLL</span><span class="sxs-lookup"><span data-stu-id="3a0bd-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a0bd-141"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3a0bd-141"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a0bd-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3a0bd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a0bd-143">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="3a0bd-143">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

