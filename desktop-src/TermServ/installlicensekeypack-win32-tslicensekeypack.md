---
title: Installlicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das die über das Internet oder das Telefon empfangene Lizenz-ID verwendet.
ms.assetid: 1e545186-cc01-4700-857f-9390e1b73923
ms.tgt_platform: multiple
keywords:
- Installlicenskeypack-Methode Remotedesktopdienste
- Installlicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, installlicenerkeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5bee5e03de19783a20eeafa3f652dd60b99e871c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949561"
---
# <a name="installlicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="abd39-106">Installlicenskeypack-Methode der Win32-Klasse "-Klasse". \_</span><span class="sxs-lookup"><span data-stu-id="abd39-106">InstallLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="abd39-107">Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das die über das Internet oder das Telefon empfangene Lizenz-ID verwendet.</span><span class="sxs-lookup"><span data-stu-id="abd39-107">Installs a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="abd39-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="abd39-108">Syntax</span></span>


```mof
uint32 InstallLicenseKeyPack(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="abd39-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="abd39-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="abd39-110">*slicenabkeypackid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="abd39-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="abd39-111">Enthält den Lizenzcode mit 35 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="abd39-111">Contains the 35-character license code.</span></span> <span data-ttu-id="abd39-112">Nur die alphanumerische Zeichenfolge mit 35 Zeichen muss als Eingabe angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="abd39-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="abd39-113">Es sollten keine Bindestriche hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="abd39-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="abd39-114">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="abd39-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="abd39-115">Empfängt den Key Pack-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="abd39-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="abd39-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="abd39-116">Return value</span></span>

<span data-ttu-id="abd39-117">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="abd39-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="abd39-118">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="abd39-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="abd39-119">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="abd39-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="abd39-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="abd39-120">Remarks</span></span>

<span data-ttu-id="abd39-121">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="abd39-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="abd39-122">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="abd39-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="abd39-123">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="abd39-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="abd39-124">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="abd39-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="abd39-125">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="abd39-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="abd39-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="abd39-126">Requirements</span></span>



| <span data-ttu-id="abd39-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="abd39-127">Requirement</span></span> | <span data-ttu-id="abd39-128">Wert</span><span class="sxs-lookup"><span data-stu-id="abd39-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="abd39-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="abd39-129">Minimum supported client</span></span><br/> | <span data-ttu-id="abd39-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="abd39-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="abd39-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="abd39-131">Minimum supported server</span></span><br/> | <span data-ttu-id="abd39-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="abd39-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="abd39-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="abd39-133">Namespace</span></span><br/>                | <span data-ttu-id="abd39-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="abd39-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="abd39-135">MOF</span><span class="sxs-lookup"><span data-stu-id="abd39-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="abd39-136"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="abd39-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="abd39-137">DLL</span><span class="sxs-lookup"><span data-stu-id="abd39-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="abd39-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="abd39-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="abd39-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="abd39-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="abd39-140">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="abd39-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

