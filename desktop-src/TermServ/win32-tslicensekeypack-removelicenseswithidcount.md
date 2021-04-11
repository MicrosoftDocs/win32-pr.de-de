---
title: Removelicenseswithidcount-Methode der Win32_TSLicenseKeyPack-Klasse
description: Entfernt die angegebene Anzahl von Remotedesktopdienste Lizenzen aus dem angegebenen Schlüssel Paket.
ms.assetid: 36228659-7BE7-490A-A00C-A99FA66BFEB8
ms.tgt_platform: multiple
keywords:
- Removelicenseswithidcount-Methode Remotedesktopdienste
- Removelicenseswithidcount-Methode Remotedesktopdienste, Win32_TSLicenseKeyPack-Klasse
- Win32_TSLicenseKeyPack-Klasse Remotedesktopdienste, removelicenseswithidcount-Methode
topic_type:
- apiref
api_name:
- Win32_TSLicenseKeyPack.RemoveLicensesWithIdCount
api_location:
- TlsWmiProv.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3b2de1d1e0bfeed538e400436f8a88cd25ac563
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040198"
---
# <a name="removelicenseswithidcount-method-of-the-win32_tslicensekeypack-class"></a><span data-ttu-id="ea793-106">Removelicenseswithidcount-Methode der Win32- \_ Klasse "zlicenserkeypack"</span><span class="sxs-lookup"><span data-stu-id="ea793-106">RemoveLicensesWithIdCount method of the Win32\_TSLicenseKeyPack class</span></span>

<span data-ttu-id="ea793-107">Entfernt die angegebene Anzahl von Remotedesktopdienste Lizenzen aus dem angegebenen Schlüssel Paket.</span><span class="sxs-lookup"><span data-stu-id="ea793-107">Removes the specified number of Remote Desktop Services licenses from the specified key pack.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea793-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ea793-108">Syntax</span></span>


```mof
uint32 RemoveLicensesWithIdCount(
  [in] uint32 KeyPackId,
  [in] uint32 LicenseCount
);
```



## <a name="parameters"></a><span data-ttu-id="ea793-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ea793-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea793-110">*Keypackid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea793-110">*KeyPackId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea793-111">Der Bezeichner des Schlüssel Pakets, das die zu entfernenden Lizenzen enthält.</span><span class="sxs-lookup"><span data-stu-id="ea793-111">The identifier of the key pack that contains the licenses to remove.</span></span>

</dd> <dt>

<span data-ttu-id="ea793-112">*Lizenz Anzahl* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="ea793-112">*LicenseCount* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ea793-113">Die Anzahl der zu deinstallierenden Lizenzen.</span><span class="sxs-lookup"><span data-stu-id="ea793-113">The number of licenses to uninstall.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ea793-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ea793-114">Return value</span></span>

<span data-ttu-id="ea793-115">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="ea793-115">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="ea793-116">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ea793-116">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="ea793-117">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="ea793-117">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ea793-118">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ea793-118">Requirements</span></span>



| <span data-ttu-id="ea793-119">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ea793-119">Requirement</span></span> | <span data-ttu-id="ea793-120">Wert</span><span class="sxs-lookup"><span data-stu-id="ea793-120">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea793-121">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ea793-121">Minimum supported client</span></span><br/> | <span data-ttu-id="ea793-122">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ea793-122">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="ea793-123">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ea793-123">Minimum supported server</span></span><br/> | <span data-ttu-id="ea793-124">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ea793-124">Windows Server 2008</span></span><br/>                                                            |
| <span data-ttu-id="ea793-125">Namespace</span><span class="sxs-lookup"><span data-stu-id="ea793-125">Namespace</span></span><br/>                | <span data-ttu-id="ea793-126">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="ea793-126">Root\\CIMv2</span></span><br/>                                                                    |
| <span data-ttu-id="ea793-127">MOF</span><span class="sxs-lookup"><span data-stu-id="ea793-127">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ea793-128"><dt>Tltaumiprov. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ea793-128"><dt>TlsWmiProv.mof</dt></span></span> </dl> |
| <span data-ttu-id="ea793-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ea793-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ea793-130"><dt>TlsWmiProv.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ea793-130"><dt>TlsWmiProv.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea793-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ea793-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea793-132">**Win32-Schlüssel-Lizenz-Schlüssel \_ ACK**</span><span class="sxs-lookup"><span data-stu-id="ea793-132">**Win32\_TSLicenseKeyPack**</span></span>](win32-tslicensekeypack.md)
</dt> </dl>

 

 





