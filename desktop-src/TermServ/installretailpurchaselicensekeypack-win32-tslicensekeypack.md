---
title: Installretailpurchaselicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen einzelhandelskanal gekauft wurde.
ms.assetid: cd33c785-7aa1-4e30-8155-4176b6f4c037
ms.tgt_platform: multiple
keywords:
- Installretailpurchaselicenskeypack-Methode Remotedesktopdienste
- Installretailpurchaselicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, installretailpurchaselicensskeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.InstallRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7523e2106a68284d6b9b376d47608114f940c194
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106337304"
---
# <a name="installretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="00a8a-106">Installretailpurchaselicensskeypack-Methode der Win32-Klasse "-Klasse". \_</span><span class="sxs-lookup"><span data-stu-id="00a8a-106">InstallRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="00a8a-107">Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen einzelhandelskanal gekauft wurde.</span><span class="sxs-lookup"><span data-stu-id="00a8a-107">Installs a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="00a8a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="00a8a-108">Syntax</span></span>


```mof
uint32 InstallRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="00a8a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="00a8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00a8a-110">*slicensecode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="00a8a-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00a8a-111">Enthält den 25-stelligen Lizenzcode.</span><span class="sxs-lookup"><span data-stu-id="00a8a-111">Contains the 25-character license code.</span></span> <span data-ttu-id="00a8a-112">Nur die alphanumerische Zeichenfolge mit 25 Zeichen muss als Eingabe angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="00a8a-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="00a8a-113">Es sollten keine Bindestriche hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="00a8a-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="00a8a-114">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="00a8a-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="00a8a-115">Empfängt den Key Pack-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="00a8a-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00a8a-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00a8a-116">Return value</span></span>

<span data-ttu-id="00a8a-117">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="00a8a-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="00a8a-118">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00a8a-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="00a8a-119">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="00a8a-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="00a8a-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00a8a-120">Remarks</span></span>

<span data-ttu-id="00a8a-121">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="00a8a-121">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="00a8a-122">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="00a8a-122">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="00a8a-123">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="00a8a-123">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="00a8a-124">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="00a8a-124">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="00a8a-125">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="00a8a-125">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="00a8a-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="00a8a-126">Requirements</span></span>



| <span data-ttu-id="00a8a-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="00a8a-127">Requirement</span></span> | <span data-ttu-id="00a8a-128">Wert</span><span class="sxs-lookup"><span data-stu-id="00a8a-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="00a8a-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="00a8a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="00a8a-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="00a8a-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="00a8a-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="00a8a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="00a8a-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="00a8a-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="00a8a-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="00a8a-133">Namespace</span></span><br/>                | <span data-ttu-id="00a8a-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="00a8a-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="00a8a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="00a8a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="00a8a-136"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="00a8a-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="00a8a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="00a8a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="00a8a-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="00a8a-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00a8a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00a8a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00a8a-140">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="00a8a-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

