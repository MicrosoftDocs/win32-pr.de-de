---
title: Importretailpurchaselicenskeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen einzelhandelskanal gekauft wurde.
ms.assetid: B45C3263-216E-4284-89A1-BE2ADE3A8E84
ms.tgt_platform: multiple
keywords:
- Importretailpurchaselicenskeypack-Methode Remotedesktopdienste
- Importretailpurchaselicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, importretailpurchaselicenskeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportRetailPurchaseLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2699d1f96827f9ace0f111a4c95adb64d5f8467e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741768"
---
# <a name="importretailpurchaselicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="8b866-106">Importretailpurchaselicenskeypack-Methode der Win32- \_ Klasse "zlicenabkeypack"</span><span class="sxs-lookup"><span data-stu-id="8b866-106">ImportRetailPurchaseLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="8b866-107">Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste Lizenzschlüssel Paket, das über einen einzelhandelskanal gekauft wurde.</span><span class="sxs-lookup"><span data-stu-id="8b866-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that was purchased through a retail channel.</span></span>

## <a name="syntax"></a><span data-ttu-id="8b866-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="8b866-108">Syntax</span></span>


```mof
uint32 ImportRetailPurchaseLicenseKeyPack(
  [in]  string sLicenseCode,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="8b866-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="8b866-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8b866-110">*slicensecode* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b866-110">*sLicenseCode* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b866-111">Enthält den 25-stelligen Lizenzcode.</span><span class="sxs-lookup"><span data-stu-id="8b866-111">Contains the 25-character license code.</span></span> <span data-ttu-id="8b866-112">Nur die alphanumerische Zeichenfolge mit 25 Zeichen muss als Eingabe angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="8b866-112">Only the 25-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="8b866-113">Es sollten keine Bindestriche hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="8b866-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="8b866-114">*ssourcelsname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b866-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b866-115">Der Name der Quelle Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="8b866-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="8b866-116">Dies ist entweder der voll qualifizierte Distinguished Name oder die IP-Adresse des Servers.</span><span class="sxs-lookup"><span data-stu-id="8b866-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="8b866-117">*ssourcelsproductid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="8b866-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8b866-118">Der Bezeichner des Remotedesktop-Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="8b866-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="8b866-119">Bei handelt es sich um eine alphanumerische Zeichenfolge mit 35 Zeichen, die keine Bindestriche enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="8b866-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="8b866-120">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="8b866-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8b866-121">Empfängt den Key Pack-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="8b866-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8b866-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="8b866-122">Return value</span></span>

<span data-ttu-id="8b866-123">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="8b866-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="8b866-124">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8b866-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="8b866-125">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8b866-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8b866-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8b866-126">Requirements</span></span>



| <span data-ttu-id="8b866-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8b866-127">Requirement</span></span> | <span data-ttu-id="8b866-128">Wert</span><span class="sxs-lookup"><span data-stu-id="8b866-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="8b866-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8b866-129">Minimum supported client</span></span><br/> | <span data-ttu-id="8b866-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="8b866-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="8b866-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8b866-131">Minimum supported server</span></span><br/> | <span data-ttu-id="8b866-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="8b866-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="8b866-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="8b866-133">Namespace</span></span><br/>                | <span data-ttu-id="8b866-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="8b866-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="8b866-135">MOF</span><span class="sxs-lookup"><span data-stu-id="8b866-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="8b866-136"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="8b866-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="8b866-137">DLL</span><span class="sxs-lookup"><span data-stu-id="8b866-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="8b866-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8b866-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8b866-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b866-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8b866-140">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="8b866-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





