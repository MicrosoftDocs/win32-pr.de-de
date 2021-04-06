---
title: Reinstallopenpurchaselicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Open License Remotedesktopdienste License Key Pack neu.
ms.assetid: 3E70711E-284A-466E-A733-1219F5E0B741
ms.tgt_platform: multiple
keywords:
- Reinstallopenpurchaselicenskeypack-Methode Remotedesktopdienste
- Reinstallopenpurchaselicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, reinstallopenpurchaselicenskeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d1eae765b74feed98760ef30c2b89a1090c4200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743272"
---
# <a name="reinstallopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="7ba1d-106">Reinstallopenpurchaselicenskeypack-Methode der Win32- \_ Klasse "plicenabkeypack"</span><span class="sxs-lookup"><span data-stu-id="7ba1d-106">ReinstallOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="7ba1d-107">Installiert ein Open License Remotedesktopdienste License Key Pack neu.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-107">Reinstalls an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ba1d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ba1d-108">Syntax</span></span>


```mof
uint32 ReinstallOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="7ba1d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ba1d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7ba1d-110">*slicensenum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba1d-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-111">numerische Zeichenfolge mit 8 Zeichen, die mit dem Lizenzschlüssel Paket bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="7ba1d-112">Der *slicensenreber* -Parameter darf keine Bindestriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="7ba1d-113">*sauthorizationnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba1d-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-114">eine alphanumerische Zeichenfolge mit 15 Zeichen, die mit dem Lizenzschlüssel bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="7ba1d-115">Der *sauthorizationnumber* -Parameter darf keine Bindestriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="7ba1d-116">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba1d-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-117">Die Produktversion.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-117">Product version.</span></span>

<dt>

<span data-ttu-id="7ba1d-118">0</span><span class="sxs-lookup"><span data-stu-id="7ba1d-118">0</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-119">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7ba1d-120">1</span><span class="sxs-lookup"><span data-stu-id="7ba1d-120">1</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-121">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="7ba1d-122">2</span><span class="sxs-lookup"><span data-stu-id="7ba1d-122">2</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ba1d-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7ba1d-124">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba1d-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-125">Produkttyp.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-125">Product type.</span></span>

<dt>

<span data-ttu-id="7ba1d-126">0</span><span class="sxs-lookup"><span data-stu-id="7ba1d-126">0</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-127">Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="7ba1d-128">Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="7ba1d-129">1</span><span class="sxs-lookup"><span data-stu-id="7ba1d-129">1</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-130">Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="7ba1d-131">Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="7ba1d-132">2</span><span class="sxs-lookup"><span data-stu-id="7ba1d-132">2</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-133">Der Produkttyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="7ba1d-134">*Lizenz Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7ba1d-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-135">Die Anzahl der zu installierenden Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-135">The number of licenses to install.</span></span>

</dd> <dt>

<span data-ttu-id="7ba1d-136">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="7ba1d-136">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7ba1d-137">Empfängt den Key Pack-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-137">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7ba1d-138">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7ba1d-138">Return value</span></span>

<span data-ttu-id="7ba1d-139">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-139">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="7ba1d-140">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7ba1d-140">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="7ba1d-141">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="7ba1d-141">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7ba1d-142">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7ba1d-142">Requirements</span></span>



| <span data-ttu-id="7ba1d-143">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ba1d-143">Requirement</span></span> | <span data-ttu-id="7ba1d-144">Wert</span><span class="sxs-lookup"><span data-stu-id="7ba1d-144">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ba1d-145">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7ba1d-145">Minimum supported client</span></span><br/> | <span data-ttu-id="7ba1d-146">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7ba1d-146">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="7ba1d-147">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7ba1d-147">Minimum supported server</span></span><br/> | <span data-ttu-id="7ba1d-148">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7ba1d-148">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="7ba1d-149">Namespace</span><span class="sxs-lookup"><span data-stu-id="7ba1d-149">Namespace</span></span><br/>                | <span data-ttu-id="7ba1d-150">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="7ba1d-150">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="7ba1d-151">MOF</span><span class="sxs-lookup"><span data-stu-id="7ba1d-151">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7ba1d-152"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7ba1d-152"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="7ba1d-153">DLL</span><span class="sxs-lookup"><span data-stu-id="7ba1d-153">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7ba1d-154"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7ba1d-154"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ba1d-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ba1d-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ba1d-156">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="7ba1d-156">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





