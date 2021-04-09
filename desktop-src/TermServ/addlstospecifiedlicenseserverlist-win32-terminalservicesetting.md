---
title: Addlstospecifiedlicenseserverlist-Methode der Win32_TerminalServiceSetting-Klasse
description: Fügt den angegebenen Lizenzserver am Ende der Liste der angegebenen Lizenzserver hinzu.
ms.assetid: 2aebe7c0-5ec2-4c2d-9887-7ecd2d6ec02a
ms.tgt_platform: multiple
keywords:
- Addlstospecifiedlicenseserverlist-Methode Remotedesktopdienste
- Addlstospecifiedlicenseserverlist-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, addlstospecifiedlicenseserverlist-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddLSToSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1c53a5279523405b760addabb03e381507775e6a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949633"
---
# <a name="addlstospecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="365a5-106">Addlstospecifiedlicenseserverlist-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="365a5-106">AddLSToSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="365a5-107">Fügt den angegebenen Lizenzserver am Ende der Liste der angegebenen Lizenzserver hinzu.</span><span class="sxs-lookup"><span data-stu-id="365a5-107">Adds the given license server to the end of the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="365a5-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="365a5-108">Syntax</span></span>


```mof
uint32 AddLSToSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="365a5-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="365a5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="365a5-110">*Licenseservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="365a5-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="365a5-111">Der Name des hinzu zufügenden Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="365a5-111">The name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="365a5-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="365a5-112">Return value</span></span>

<span data-ttu-id="365a5-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="365a5-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="365a5-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="365a5-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="365a5-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="365a5-115">Requirements</span></span>



| <span data-ttu-id="365a5-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="365a5-116">Requirement</span></span> | <span data-ttu-id="365a5-117">Wert</span><span class="sxs-lookup"><span data-stu-id="365a5-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="365a5-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="365a5-118">Minimum supported client</span></span><br/> | <span data-ttu-id="365a5-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="365a5-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="365a5-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="365a5-120">Minimum supported server</span></span><br/> | <span data-ttu-id="365a5-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="365a5-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="365a5-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="365a5-122">Namespace</span></span><br/>                | <span data-ttu-id="365a5-123">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="365a5-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="365a5-124">MOF</span><span class="sxs-lookup"><span data-stu-id="365a5-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="365a5-125"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="365a5-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="365a5-126">DLL</span><span class="sxs-lookup"><span data-stu-id="365a5-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="365a5-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="365a5-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="365a5-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="365a5-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="365a5-129">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="365a5-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="365a5-130">**Emptyspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="365a5-130">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="365a5-131">**Getspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="365a5-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="365a5-132">**Removelsfromspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="365a5-132">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="365a5-133">**Setspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="365a5-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





