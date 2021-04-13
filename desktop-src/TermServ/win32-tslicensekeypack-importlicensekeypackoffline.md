---
title: Importlicenabkeypackoffline-Methode der Win32_TSLicenseKeyPack-Klasse
description: Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste License Key Pack, das eine Lizenz-ID verwendet, die über das Internet oder das Telefon empfangen wurde.
ms.assetid: 69D65917-8B82-4C24-AFFA-BBE529D3883C
ms.tgt_platform: multiple
keywords:
- Importlicenabkeypackoffline-Methode Remotedesktopdienste
- Importlicenabkeypackoffline-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, importlicenabkeypackoffline-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ImportLicenseKeyPackOffline
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0de474cce6eb91cdc605588f7f4a63d97f985769
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517870"
---
# <a name="importlicensekeypackoffline-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="25998-106">Importlicenabkeypackoffline-Methode der Win32-Klasse "-Klasse". \_</span><span class="sxs-lookup"><span data-stu-id="25998-106">ImportLicenseKeyPackOffline method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="25998-107">Importe von einem anderen Remotedesktop Lizenzserver, ein Remotedesktopdienste License Key Pack, das eine Lizenz-ID verwendet, die über das Internet oder das Telefon empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="25998-107">Imports, from another Remote Desktop license server, a Remote Desktop Services license key pack that uses a license identifier that was received over the Internet or the phone.</span></span>

## <a name="syntax"></a><span data-ttu-id="25998-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="25998-108">Syntax</span></span>


```mof
uint32 ImportLicenseKeyPackOffline(
  [in]  string sLicenseKeyPackId,
  [in]  string sSourceLSName,
  [in]  string sSourceLSProductId,
  [out] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="25998-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="25998-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="25998-110">*slicenabkeypackid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25998-110">*sLicenseKeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25998-111">Enthält den Lizenzcode mit 35 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="25998-111">Contains the 35-character license code.</span></span> <span data-ttu-id="25998-112">Nur die alphanumerische Zeichenfolge mit 35 Zeichen muss als Eingabe angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="25998-112">Only the 35-character alphanumeric character string should be given as input.</span></span> <span data-ttu-id="25998-113">Es sollten keine Bindestriche hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="25998-113">No hyphens should be added.</span></span>

</dd> <dt>

<span data-ttu-id="25998-114">*ssourcelsname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25998-114">*sSourceLSName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25998-115">Der Name der Quelle Remotedesktop Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="25998-115">The name of the source Remote Desktop license server.</span></span> <span data-ttu-id="25998-116">Dies ist entweder der voll qualifizierte Distinguished Name oder die IP-Adresse des Servers.</span><span class="sxs-lookup"><span data-stu-id="25998-116">This is either the fully qualified distinguished name or the IP address of the server.</span></span>

</dd> <dt>

<span data-ttu-id="25998-117">*ssourcelsproductid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="25998-117">*sSourceLSProductId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="25998-118">Der Bezeichner des Remotedesktop-Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="25998-118">The Remote Desktop license server identifier.</span></span> <span data-ttu-id="25998-119">Bei handelt es sich um eine alphanumerische Zeichenfolge mit 35 Zeichen, die keine Bindestriche enthalten kann.</span><span class="sxs-lookup"><span data-stu-id="25998-119">The is a 35-character alphanumeric string that cannot include hyphens.</span></span>

</dd> <dt>

<span data-ttu-id="25998-120">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="25998-120">*KeyPackId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="25998-121">Empfängt den Key Pack-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="25998-121">Receives the key pack identifier.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="25998-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="25998-122">Return value</span></span>

<span data-ttu-id="25998-123">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="25998-123">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="25998-124">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="25998-124">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="25998-125">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="25998-125">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="25998-126">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="25998-126">Requirements</span></span>



| <span data-ttu-id="25998-127">Anforderung</span><span class="sxs-lookup"><span data-stu-id="25998-127">Requirement</span></span> | <span data-ttu-id="25998-128">Wert</span><span class="sxs-lookup"><span data-stu-id="25998-128">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="25998-129">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="25998-129">Minimum supported client</span></span><br/> | <span data-ttu-id="25998-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="25998-130">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="25998-131">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="25998-131">Minimum supported server</span></span><br/> | <span data-ttu-id="25998-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25998-132">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="25998-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="25998-133">Namespace</span></span><br/>                | <span data-ttu-id="25998-134">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="25998-134">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="25998-135">MOF</span><span class="sxs-lookup"><span data-stu-id="25998-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25998-136"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="25998-136"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="25998-137">DLL</span><span class="sxs-lookup"><span data-stu-id="25998-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25998-138"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25998-138"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25998-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25998-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25998-140">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="25998-140">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





