---
title: Importopenpurchaselicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Importe von einem anderen Remotedesktop Lizenzserver, einem Open License Remotedesktopdienste License Key Pack.
ms.assetid: FE1923FF-5292-4080-AB51-88B8A6B2322C
ms.tgt_platform: multiple
keywords:
- Importopenpurchaselicenskeypack-Methode Remotedesktopdienste
- Importopenpurchaselicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, importopenpurchaselicenskeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportOpenPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 944bb1ce63150caece2cbc247af24542fde2d4f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106339597"
---
# <a name="importopenpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="39c92-106">Importopenpurchaselicenskeypack-Methode der Win32-Klasse "Klasse". \_</span><span class="sxs-lookup"><span data-stu-id="39c92-106">ImportOpenPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="39c92-107">Importe von einem anderen Remotedesktop Lizenzserver, einem Open License Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="39c92-107">Imports, from another Remote Desktop license server, an Open License Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="39c92-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="39c92-108">Syntax</span></span>


```mof
uint32 ImportOpenPurchaseLicenseKeyPack(
  [in]  string sLicenseNumber,
  [in]  string sAuthorizationNumber,
  [in]  uint32 ProductVersion,
  [in]  uint32 ProductType,
  [in]  uint32 LicenseCount,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="39c92-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="39c92-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="39c92-110">*slicensenum* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39c92-110">*sLicenseNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39c92-111">numerische Zeichenfolge mit 8 Zeichen, die mit dem Lizenzschlüssel Paket bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="39c92-111">8-character numeric string that is provided with the license key pack.</span></span> <span data-ttu-id="39c92-112">Der *slicensenreber* -Parameter darf keine Bindestriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="39c92-112">The *sLicenseNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="39c92-113">*sauthorizationnumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39c92-113">*sAuthorizationNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39c92-114">eine alphanumerische Zeichenfolge mit 15 Zeichen, die mit dem Lizenzschlüssel bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="39c92-114">15-character alphanumeric string that is provided with the license key.</span></span> <span data-ttu-id="39c92-115">Der *sauthorizationnumber* -Parameter darf keine Bindestriche enthalten.</span><span class="sxs-lookup"><span data-stu-id="39c92-115">The *sAuthorizationNumber* parameter cannot contain hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="39c92-116">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39c92-116">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39c92-117">Die Produktversion.</span><span class="sxs-lookup"><span data-stu-id="39c92-117">Product version.</span></span>

<dt>

<span data-ttu-id="39c92-118">0</span><span class="sxs-lookup"><span data-stu-id="39c92-118">0</span></span>
</dt> <dd>

<span data-ttu-id="39c92-119">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39c92-119">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="39c92-120">1</span><span class="sxs-lookup"><span data-stu-id="39c92-120">1</span></span>
</dt> <dd>

<span data-ttu-id="39c92-121">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39c92-121">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="39c92-122">2</span><span class="sxs-lookup"><span data-stu-id="39c92-122">2</span></span>
</dt> <dd>

<span data-ttu-id="39c92-123">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39c92-123">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="39c92-124">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39c92-124">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39c92-125">Produkttyp.</span><span class="sxs-lookup"><span data-stu-id="39c92-125">Product type.</span></span>

<dt>

<span data-ttu-id="39c92-126">0</span><span class="sxs-lookup"><span data-stu-id="39c92-126">0</span></span>
</dt> <dd>

<span data-ttu-id="39c92-127">Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät.</span><span class="sxs-lookup"><span data-stu-id="39c92-127">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="39c92-128">Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="39c92-128">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="39c92-129">1</span><span class="sxs-lookup"><span data-stu-id="39c92-129">1</span></span>
</dt> <dd>

<span data-ttu-id="39c92-130">Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="39c92-130">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="39c92-131">Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="39c92-131">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="39c92-132">2</span><span class="sxs-lookup"><span data-stu-id="39c92-132">2</span></span>
</dt> <dd>

<span data-ttu-id="39c92-133">Der Produkttyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="39c92-133">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="39c92-134">*Lizenz Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39c92-134">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39c92-135">Die Anzahl der zu importierenden Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="39c92-135">The number of licenses to import</span></span>

</dd> <dt>

<span data-ttu-id="39c92-136">*ssourcelsname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39c92-136">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39c92-137">Der Name der Quelle Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="39c92-137">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="39c92-138">Dies ist entweder der voll qualifizierte Distinguished Name oder die IP-Adresse des Servers.</span><span class="sxs-lookup"><span data-stu-id="39c92-138">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="39c92-139">*ssourcelsproductid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="39c92-139">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="39c92-140">Der Bezeichner des Remotedesktop-Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="39c92-140">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="39c92-141">Bei handelt es sich um eine alphanumerische Zeichenfolge mit 35 Zeichen, die keine Bindestriche enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="39c92-141">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="39c92-142">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="39c92-142">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="39c92-143">Empfängt den Key Pack-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="39c92-143">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="39c92-144">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="39c92-144">Return value</span></span>

<span data-ttu-id="39c92-145">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="39c92-145">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="39c92-146">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="39c92-146">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="39c92-147">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="39c92-147">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="39c92-148">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="39c92-148">Requirements</span></span>



| <span data-ttu-id="39c92-149">Anforderung</span><span class="sxs-lookup"><span data-stu-id="39c92-149">Requirement</span></span> | <span data-ttu-id="39c92-150">Wert</span><span class="sxs-lookup"><span data-stu-id="39c92-150">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="39c92-151">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="39c92-151">Minimum supported client</span></span><br/> | <span data-ttu-id="39c92-152">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="39c92-152">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="39c92-153">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="39c92-153">Minimum supported server</span></span><br/> | <span data-ttu-id="39c92-154">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="39c92-154">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="39c92-155">Namespace</span><span class="sxs-lookup"><span data-stu-id="39c92-155">Namespace</span></span><br/>                | <span data-ttu-id="39c92-156">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="39c92-156">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="39c92-157">MOF</span><span class="sxs-lookup"><span data-stu-id="39c92-157">MOF</span></span><br/>                      | <dl> <span data-ttu-id="39c92-158"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="39c92-158"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="39c92-159">DLL</span><span class="sxs-lookup"><span data-stu-id="39c92-159">DLL</span></span><br/>                      | <dl> <span data-ttu-id="39c92-160"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="39c92-160"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="39c92-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39c92-161">See also</span></span>

<dl> <dt>

[<span data-ttu-id="39c92-162">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="39c92-162">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





