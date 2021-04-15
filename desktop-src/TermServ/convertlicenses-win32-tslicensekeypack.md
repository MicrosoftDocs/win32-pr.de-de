---
title: Convertlicenses-Methode der Win32_TSLicenseKeyPack-Klasse
description: Konvertiert die Lizenzen im aktuellen Schlüssel Paket.
ms.assetid: 38600144-8fa2-4f9a-b7a4-7fafc304e7cb
ms.tgt_platform: multiple
keywords:
- Convertlicenses-Methode Remotedesktopdienste
- Convertlicenses-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, convertlicenses-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.ConvertLicenses
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 54f37b1d9804c5f14f89a7ff6b48f5f8fcbdc60b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391623"
---
# <a name="convertlicenses-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="4bbf3-106">Convertlicenses-Methode der Win32- \_ Klasse "zlicenabkeypack"</span><span class="sxs-lookup"><span data-stu-id="4bbf3-106">ConvertLicenses method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="4bbf3-107">Konvertiert die Lizenzen im aktuellen Schlüssel Paket.</span><span class="sxs-lookup"><span data-stu-id="4bbf3-107">Converts the licenses in the current key pack.</span></span> <span data-ttu-id="4bbf3-108">Wenn die Lizenz eine benutzerspezifische Lizenz ist, wird Sie in eine pro-Gerät-Lizenz konvertiert.</span><span class="sxs-lookup"><span data-stu-id="4bbf3-108">If the license is a per-user license, it is converted to a per-device license.</span></span> <span data-ttu-id="4bbf3-109">Wenn die Lizenz eine pro-Gerät-Lizenz ist, wird Sie in eine benutzerspezifische Lizenz konvertiert.</span><span class="sxs-lookup"><span data-stu-id="4bbf3-109">If the license is a per-device license, it is converted to a per-user license.</span></span>

## <a name="syntax"></a><span data-ttu-id="4bbf3-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="4bbf3-110">Syntax</span></span>


```mof
uint32 ConvertLicenses(
  [in]  uint32 Count,
  [out] uint32 KeypackID
);
```



## <a name="parameters"></a><span data-ttu-id="4bbf3-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="4bbf3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bbf3-112">*Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="4bbf3-112">*Count* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bbf3-113">Die Anzahl der zu konvertierenden Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="4bbf3-113">The number of licenses to be converted.</span></span>

</dd> <dt>

<span data-ttu-id="4bbf3-114">*Keypackid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="4bbf3-114">*KeypackID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="4bbf3-115">Der Bezeichner des resultierenden Schlüssel Pakets.</span><span class="sxs-lookup"><span data-stu-id="4bbf3-115">The identifier of the resultant key pack.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bbf3-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4bbf3-116">Return value</span></span>

<span data-ttu-id="4bbf3-117">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="4bbf3-117">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="4bbf3-118">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4bbf3-118">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="4bbf3-119">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="4bbf3-119">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bbf3-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4bbf3-120">Requirements</span></span>



| <span data-ttu-id="4bbf3-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4bbf3-121">Requirement</span></span> | <span data-ttu-id="4bbf3-122">Wert</span><span class="sxs-lookup"><span data-stu-id="4bbf3-122">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4bbf3-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4bbf3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="4bbf3-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="4bbf3-124">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="4bbf3-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4bbf3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="4bbf3-126">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="4bbf3-126">Windows Server 2012</span></span><br/>                                                            |
| <span data-ttu-id="4bbf3-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="4bbf3-127">Namespace</span></span><br/>                | <span data-ttu-id="4bbf3-128">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="4bbf3-128">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="4bbf3-129">MOF</span><span class="sxs-lookup"><span data-stu-id="4bbf3-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="4bbf3-130"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="4bbf3-130"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="4bbf3-131">DLL</span><span class="sxs-lookup"><span data-stu-id="4bbf3-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bbf3-132"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bbf3-132"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bbf3-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4bbf3-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bbf3-134">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="4bbf3-134">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





