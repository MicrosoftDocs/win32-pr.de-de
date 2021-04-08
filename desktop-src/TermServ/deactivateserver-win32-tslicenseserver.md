---
title: Deactivateserver-Methode der Win32_TSLicenseServer-Klasse
description: Deaktiviert den Remotedesktop Lizenzserver mithilfe eines Bestätigungs Codes, der über das Telefon empfangen wird.
ms.assetid: 84e069b7-9a4f-4843-b656-839f936ac727
ms.tgt_platform: multiple
keywords:
- Deactivateserver-Methode Remotedesktopdienste
- Deactivateserver-Methode Remotedesktopdienste, Win32_TSLicenseServer-Klasse
- Win32_TSLicenseServer-Klasse Remotedesktopdienste, deactivateserver-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseServer.DeactivateServer
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 23b851a8d8049c9194bce163afc4b7bad5d4aa15
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949509"
---
# <a name="deactivateserver-method-of-the-win32_tslicenseserver-class"></a><span data-ttu-id="8afb3-106">Deactivateserver-Methode der Win32- \_ Klasse "zlicenseserver"</span><span class="sxs-lookup"><span data-stu-id="8afb3-106">DeactivateServer method of the Win32\_TSLicenseServer class</span></span>

<span data-ttu-id="8afb3-107">Deaktiviert den Remotedesktop Lizenzserver mithilfe eines Bestätigungs Codes, der über das Telefon empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="8afb3-107">Deactivates the Remote Desktop license server by using a confirmation code that is received over the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="8afb3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8afb3-108">Syntax</span></span>


```mof
uint32 DeactivateServer(
  [in]  string sConfirmCode,
  [out] uint32 ActivationStatus
);
```



## <a name="parameters"></a><span data-ttu-id="8afb3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8afb3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8afb3-110">*sconfirmcode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8afb3-110">*sConfirmCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8afb3-111">Bestätigungscode.</span><span class="sxs-lookup"><span data-stu-id="8afb3-111">Confirmation code.</span></span>

</dd> <dt>

<span data-ttu-id="8afb3-112">*Activationstatus* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8afb3-112">*ActivationStatus* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8afb3-113">Der zurückgegebene Aktivierungs Status kann einer der folgenden sein.</span><span class="sxs-lookup"><span data-stu-id="8afb3-113">The activation status returned can be one of the following.</span></span>

<dt>

<span data-ttu-id="8afb3-114">0</span><span class="sxs-lookup"><span data-stu-id="8afb3-114">0</span></span>
</dt> <dd>

<span data-ttu-id="8afb3-115">Der Remotedesktop Lizenzserver wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8afb3-115">The Remote Desktop license server is activated.</span></span>

</dd> <dt>

<span data-ttu-id="8afb3-116">1</span><span class="sxs-lookup"><span data-stu-id="8afb3-116">1</span></span>
</dt> <dd>

<span data-ttu-id="8afb3-117">Der Remotedesktop Lizenzserver ist nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8afb3-117">The Remote Desktop license server is not activated.</span></span>

</dd> <dt>

<span data-ttu-id="8afb3-118">2</span><span class="sxs-lookup"><span data-stu-id="8afb3-118">2</span></span>
</dt> <dd>

<span data-ttu-id="8afb3-119">Es ist ein unbekannter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8afb3-119">An unknown error occurred.</span></span> <span data-ttu-id="8afb3-120">Es ist nicht bekannt, ob der Remotedesktopdienste Lizenzserver aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8afb3-120">It is not known whether the Remote Desktop Services license server is activated.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8afb3-121">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8afb3-121">Return value</span></span>

<span data-ttu-id="8afb3-122">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="8afb3-122">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8afb3-123">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8afb3-123">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8afb3-124">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8afb3-124">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8afb3-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8afb3-125">Remarks</span></span>

<span data-ttu-id="8afb3-126">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="8afb3-126">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="8afb3-127">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="8afb3-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="8afb3-128">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="8afb3-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="8afb3-129">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8afb3-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="8afb3-130">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="8afb3-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="8afb3-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8afb3-131">Requirements</span></span>



| <span data-ttu-id="8afb3-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8afb3-132">Requirement</span></span> | <span data-ttu-id="8afb3-133">Wert</span><span class="sxs-lookup"><span data-stu-id="8afb3-133">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8afb3-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8afb3-134">Minimum supported client</span></span><br/> | <span data-ttu-id="8afb3-135">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8afb3-135">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8afb3-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8afb3-136">Minimum supported server</span></span><br/> | <span data-ttu-id="8afb3-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8afb3-137">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="8afb3-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="8afb3-138">Namespace</span></span><br/>                | <span data-ttu-id="8afb3-139">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8afb3-139">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="8afb3-140">MOF</span><span class="sxs-lookup"><span data-stu-id="8afb3-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8afb3-141"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8afb3-141"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8afb3-142">DLL</span><span class="sxs-lookup"><span data-stu-id="8afb3-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8afb3-143"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8afb3-143"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8afb3-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8afb3-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8afb3-145">**Win32- \_ Lizenznehmer**</span><span class="sxs-lookup"><span data-stu-id="8afb3-145">**Win32\_TSLicenseServer**</span></span>](win32-tslicenseserver.md)
</dt> </dl>

 

