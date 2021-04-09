---
title: Reinstalllicenankeypackoffline-Methode der Win32_TSLicenseKeyPack-Klasse
description: Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das die über das Internet oder das Telefon empfangene Lizenz-ID verwendet.
ms.assetid: CFDB4C3B-C7C1-4670-BC87-92727057A500
ms.tgt_platform: multiple
keywords:
- Reinstalllicenabkeypackoffline-Methode Remotedesktopdienste
- Reinstalllicenankeypackoffline-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, reinstalllicenabkeypackoffline-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ReinstallLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7e805521ea750c018ab2e7965e7fbfba05a92d8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858698"
---
# <a name="reinstalllicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="e6d79-106">Reinstalllicenankeypackoffline-Methode der Win32-Klasse "Klasse". \_</span><span class="sxs-lookup"><span data-stu-id="e6d79-106">ReinstallLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="e6d79-107">Installiert ein Remotedesktopdienste Lizenzschlüssel Paket, das die über das Internet oder das Telefon empfangene Lizenz-ID verwendet.</span><span class="sxs-lookup"><span data-stu-id="e6d79-107">Reinstalls a Remote Desktop Services license key pack that uses the license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6d79-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e6d79-108">Syntax</span></span>


```mof
uint32 ReinstallLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="e6d79-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6d79-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e6d79-110">*slicenabkeypackid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e6d79-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d79-111">Enthält den Lizenzcode mit 35 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="e6d79-111">Contains the 35-character license code.</span></span> <span data-ttu-id="e6d79-112">Nur die alphanumerische Zeichenfolge mit 35 Zeichen muss als Eingabe angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e6d79-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="e6d79-113">Es sollten keine Bindestriche hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="e6d79-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="e6d79-114">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e6d79-114">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e6d79-115">Empfängt den Key Pack-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="e6d79-115">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e6d79-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e6d79-116">Return value</span></span>

<span data-ttu-id="e6d79-117">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="e6d79-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e6d79-118">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e6d79-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e6d79-119">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e6d79-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e6d79-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e6d79-120">Requirements</span></span>



| <span data-ttu-id="e6d79-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e6d79-121">Requirement</span></span> | <span data-ttu-id="e6d79-122">Wert</span><span class="sxs-lookup"><span data-stu-id="e6d79-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6d79-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e6d79-123">Minimum supported client</span></span><br/> | <span data-ttu-id="e6d79-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e6d79-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e6d79-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e6d79-125">Minimum supported server</span></span><br/> | <span data-ttu-id="e6d79-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e6d79-126">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e6d79-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="e6d79-127">Namespace</span></span><br/>                | <span data-ttu-id="e6d79-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e6d79-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e6d79-129">MOF</span><span class="sxs-lookup"><span data-stu-id="e6d79-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e6d79-130"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e6d79-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e6d79-131">DLL</span><span class="sxs-lookup"><span data-stu-id="e6d79-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e6d79-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e6d79-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6d79-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6d79-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6d79-134">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="e6d79-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





