---
title: Uninstalllicenerkeypack-Methode der Win32_TSLicenseKeyPack-Klasse
description: Deinstalliert ein Remotedesktopdienste License Key Pack.
ms.assetid: AF429AD7-C0DB-40AC-A4C6-591699FBF7E7
ms.tgt_platform: multiple
keywords:
- Uninstalllicenskeypack-Methode Remotedesktopdienste
- Uninstalllicenskeypack-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, uninstalllicenerkeypack-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPack
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 64754ea9ef2a32676b36821cf20c4f6871396415
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391560"
---
# <a name="uninstalllicensekeypack-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="93311-106">Uninstalllicenerkeypack-Methode der Win32- \_ Klasse "zlicenskeypack"</span><span class="sxs-lookup"><span data-stu-id="93311-106">UninstallLicenseKeyPack method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="93311-107">Deinstalliert ein Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="93311-107">Uninstalls a Remote Desktop Services license key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="93311-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="93311-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPack(
  [in] unit32 ProductVersion,
  [in] unit32 ProductType,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="93311-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="93311-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="93311-110">*ProductVersion* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93311-110">*ProductVersion* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93311-111">Die Produkt Versions Kennung für das Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="93311-111">Product version identifier for the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="93311-112">0</span><span class="sxs-lookup"><span data-stu-id="93311-112">0</span></span>
</dt> <dd>

<span data-ttu-id="93311-113">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93311-113">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="93311-114">1</span><span class="sxs-lookup"><span data-stu-id="93311-114">1</span></span>
</dt> <dd>

<span data-ttu-id="93311-115">Wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="93311-115">Not supported.</span></span>

</dd> <dt>

<span data-ttu-id="93311-116">2</span><span class="sxs-lookup"><span data-stu-id="93311-116">2</span></span>
</dt> <dd>

<span data-ttu-id="93311-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93311-117">Windows Server 2008</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="93311-118">*ProductType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93311-118">*ProductType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93311-119">Der Produkttyp des Remotedesktopdienste License Key Pack.</span><span class="sxs-lookup"><span data-stu-id="93311-119">Product type of the Remote Desktop Services license key pack.</span></span>

<dt>

<span data-ttu-id="93311-120">0</span><span class="sxs-lookup"><span data-stu-id="93311-120">0</span></span>
</dt> <dd>

<span data-ttu-id="93311-121">Der Produkttyp Remotedesktopdienste License Key Pack ist pro Gerät.</span><span class="sxs-lookup"><span data-stu-id="93311-121">The Remote Desktop Services license key pack product type is per device.</span></span> <span data-ttu-id="93311-122">Daher muss jedes Gerät, das eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="93311-122">Therefore, each device that connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="93311-123">1</span><span class="sxs-lookup"><span data-stu-id="93311-123">1</span></span>
</dt> <dd>

<span data-ttu-id="93311-124">Der Product Type für Remotedesktopdienste License Key Pack ist pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="93311-124">The Remote Desktop Services license key pack product type is per user.</span></span> <span data-ttu-id="93311-125">Daher muss jeder Benutzer, der eine Verbindung mit dem RD-Sitzungshost Server herstellt, über eine Lizenz verfügen.</span><span class="sxs-lookup"><span data-stu-id="93311-125">Therefore, each user who connects to the RD Session Host server must have a license.</span></span>

</dd> <dt>

<span data-ttu-id="93311-126">2</span><span class="sxs-lookup"><span data-stu-id="93311-126">2</span></span>
</dt> <dd>

<span data-ttu-id="93311-127">Der Produkttyp ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="93311-127">This product type is not valid.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="93311-128">*Lizenz Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="93311-128">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="93311-129">Die Anzahl der zu deinstallierenden Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="93311-129">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="93311-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="93311-130">Return value</span></span>

<span data-ttu-id="93311-131">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="93311-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="93311-132">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="93311-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="93311-133">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="93311-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="93311-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="93311-134">Requirements</span></span>



| <span data-ttu-id="93311-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="93311-135">Requirement</span></span> | <span data-ttu-id="93311-136">Wert</span><span class="sxs-lookup"><span data-stu-id="93311-136">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="93311-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="93311-137">Minimum supported client</span></span><br/> | <span data-ttu-id="93311-138">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="93311-138">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="93311-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="93311-139">Minimum supported server</span></span><br/> | <span data-ttu-id="93311-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="93311-140">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="93311-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="93311-141">Namespace</span></span><br/>                | <span data-ttu-id="93311-142">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="93311-142">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="93311-143">MOF</span><span class="sxs-lookup"><span data-stu-id="93311-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="93311-144"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="93311-144"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="93311-145">DLL</span><span class="sxs-lookup"><span data-stu-id="93311-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="93311-146"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="93311-146"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93311-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="93311-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93311-148">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="93311-148">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





