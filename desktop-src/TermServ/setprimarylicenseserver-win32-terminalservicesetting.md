---
title: Setprimarylicenseserver-Methode der Win32_TerminalServiceSetting-Klasse
description: Legt den angegebenen Lizenzserver als ersten Eintrag in der Liste der angegebenen Lizenzserver fest.
ms.assetid: 8921e861-3b9a-49c5-a691-ded7be18ca0a
ms.tgt_platform: multiple
keywords:
- Setprimarylicenseserver-Methode Remotedesktopdienste
- Setprimarylicenseserver-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, setprimarylicenseserver-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetPrimaryLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 61d73212230d1ca69e0a0809c48b8f2985920045
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103858734"
---
# <a name="setprimarylicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="13722-106">Setprimarylicenseserver-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="13722-106">SetPrimaryLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="13722-107">Legt den angegebenen Lizenzserver als ersten Eintrag in der Liste der angegebenen Lizenzserver fest.</span><span class="sxs-lookup"><span data-stu-id="13722-107">Sets the given license server as the first entry in the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="13722-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="13722-108">Syntax</span></span>


```mof
uint32 SetPrimaryLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="13722-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="13722-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13722-110">*Licenseservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="13722-110">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13722-111">Der Name des Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="13722-111">The name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13722-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="13722-112">Return value</span></span>

<span data-ttu-id="13722-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="13722-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="13722-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="13722-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="13722-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="13722-115">Requirements</span></span>



| <span data-ttu-id="13722-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="13722-116">Requirement</span></span> | <span data-ttu-id="13722-117">Wert</span><span class="sxs-lookup"><span data-stu-id="13722-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="13722-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="13722-118">Minimum supported client</span></span><br/> | <span data-ttu-id="13722-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="13722-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="13722-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="13722-120">Minimum supported server</span></span><br/> | <span data-ttu-id="13722-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="13722-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="13722-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="13722-122">Namespace</span></span><br/>                | <span data-ttu-id="13722-123">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="13722-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="13722-124">MOF</span><span class="sxs-lookup"><span data-stu-id="13722-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="13722-125"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="13722-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="13722-126">DLL</span><span class="sxs-lookup"><span data-stu-id="13722-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="13722-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="13722-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="13722-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13722-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13722-129">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="13722-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





