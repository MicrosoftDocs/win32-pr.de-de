---
title: Uninstalllicenabkeypackwithid-Methode der Win32_TSLicenseKeyPack-Klasse
description: Deinstalliert das Remotedesktopdienste License Key Pack mit der angegebenen Key Pack-Kennung.
ms.assetid: ECB622AB-FAB4-4C5D-A007-E3ABA8E1D3E7
ms.tgt_platform: multiple
keywords:
- Uninstalllicenabkeypackwithid-Methode Remotedesktopdienste
- Uninstalllicenabkeypackwithid-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, uninstalllicenabkeypackwithid-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.UninstallLicenseKeyPackWithId
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 583c7d56f5aacde57a1b683e988646e7e30b62d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104475471"
---
# <a name="uninstalllicensekeypackwithid-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="e90e6-106">Uninstalllicenabkeypackwithid-Methode der Win32- \_ Klasse "keylicenabkeypack"</span><span class="sxs-lookup"><span data-stu-id="e90e6-106">UninstallLicenseKeyPackWithId method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="e90e6-107">Deinstalliert das Remotedesktopdienste License Key Pack mit der angegebenen Key Pack-Kennung.</span><span class="sxs-lookup"><span data-stu-id="e90e6-107">Uninstalls the Remote Desktop Services license key pack with the specified key pack identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="e90e6-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e90e6-108">Syntax</span></span>


```mof
uint32 UninstallLicenseKeyPackWithId(
  [in] uint32 KeyPackId
);
```



## <a name="parameters"></a><span data-ttu-id="e90e6-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e90e6-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e90e6-110">*Keypackid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="e90e6-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e90e6-111">Der Bezeichner des zu deinstallierenden Schlüssel Pakets.</span><span class="sxs-lookup"><span data-stu-id="e90e6-111">The identifier of the key pack to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e90e6-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e90e6-112">Return value</span></span>

<span data-ttu-id="e90e6-113">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="e90e6-113">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="e90e6-114">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e90e6-114">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="e90e6-115">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e90e6-115">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e90e6-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e90e6-116">Requirements</span></span>



| <span data-ttu-id="e90e6-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e90e6-117">Requirement</span></span> | <span data-ttu-id="e90e6-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e90e6-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="e90e6-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e90e6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e90e6-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e90e6-120">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="e90e6-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e90e6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e90e6-122">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e90e6-122">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="e90e6-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e90e6-123">Namespace</span></span><br/>                | <span data-ttu-id="e90e6-124">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="e90e6-124">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="e90e6-125">MOF</span><span class="sxs-lookup"><span data-stu-id="e90e6-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e90e6-126"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e90e6-126"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="e90e6-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e90e6-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e90e6-128"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e90e6-128"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e90e6-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e90e6-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e90e6-130">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="e90e6-130">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





