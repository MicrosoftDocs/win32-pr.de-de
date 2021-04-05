---
title: Removelsfromspecifiedlicenseserverlist-Methode der Win32_TerminalServiceSetting-Klasse
description: Entfernt den angegebenen Lizenzserver aus der Liste der angegebenen Lizenzserver.
ms.assetid: c25eebf9-3a21-41a0-bb7d-c3f909cd8087
ms.tgt_platform: multiple
keywords:
- Removelsfromspecifiedlicenseserverlist-Methode Remotedesktopdienste
- Removelsfromspecifiedlicenseserverlist-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, removelsfromspecifiedlicenseserverlist-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.RemoveLSFromSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 901c2676748e819290855df2de51e5d7936dc793
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858900"
---
# <a name="removelsfromspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="c631e-106">Removelsfromspecifiedlicenseserverlist-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="c631e-106">RemoveLSFromSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="c631e-107">Entfernt den angegebenen Lizenzserver aus der Liste der angegebenen Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="c631e-107">Removes the given license server from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="c631e-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="c631e-108">Syntax</span></span>


```mof
uint32 RemoveLSFromSpecifiedLicenseServerList(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="c631e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c631e-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c631e-110">*Licenseservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="c631e-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c631e-111">Der Name des zu entfernenden Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="c631e-111">The name of the license server to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c631e-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c631e-112">Return value</span></span>

<span data-ttu-id="c631e-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c631e-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="c631e-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="c631e-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="c631e-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="c631e-115">Requirements</span></span>



| <span data-ttu-id="c631e-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c631e-116">Requirement</span></span> | <span data-ttu-id="c631e-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c631e-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c631e-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c631e-118">Minimum supported client</span></span><br/> | <span data-ttu-id="c631e-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="c631e-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="c631e-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c631e-120">Minimum supported server</span></span><br/> | <span data-ttu-id="c631e-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="c631e-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="c631e-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="c631e-122">Namespace</span></span><br/>                | <span data-ttu-id="c631e-123">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="c631e-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="c631e-124">MOF</span><span class="sxs-lookup"><span data-stu-id="c631e-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c631e-125"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="c631e-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="c631e-126">DLL</span><span class="sxs-lookup"><span data-stu-id="c631e-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c631e-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c631e-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c631e-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c631e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c631e-129">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="c631e-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c631e-130">**Addlstospecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="c631e-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c631e-131">**Emptyspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="c631e-131">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c631e-132">**Getspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="c631e-132">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="c631e-133">**Setspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="c631e-133">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





