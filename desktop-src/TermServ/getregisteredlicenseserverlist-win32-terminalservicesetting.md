---
title: Getregisteredlicenseserverlist-Methode der Win32_TerminalServiceSetting-Klasse
description: Ruft die Liste der registrierten Lizenzserver ab.
ms.assetid: 32e06b4b-652f-4977-be1f-6d52983d2605
ms.tgt_platform: multiple
keywords:
- Getregisteredlicenseserverlist-Methode Remotedesktopdienste
- Getregisteredlicenseserverlist-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, getregisteredlicenseserverlist-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetRegisteredLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5336910956a0d281fbfc8fbc65e1d3b8d5018cb2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338789"
---
# <a name="getregisteredlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="ee255-106">Getregisteredlicenseserverlist-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="ee255-106">GetRegisteredLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="ee255-107">Ruft die Liste der registrierten Lizenzserver ab.</span><span class="sxs-lookup"><span data-stu-id="ee255-107">Gets the list of registered license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee255-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee255-108">Syntax</span></span>


```mof
uint32 GetRegisteredLicenseServerList(
  [out] string RegisteredLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="ee255-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee255-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee255-110">*Registeredlslist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="ee255-110">*RegisteredLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ee255-111">Ein Zeichen folgen Array, das die Liste der registrierten Lizenzserver empfängt.</span><span class="sxs-lookup"><span data-stu-id="ee255-111">A string array that receives the list of registered license servers.</span></span> <span data-ttu-id="ee255-112">Wenn keine registrierten Lizenzserver vorhanden sind, ist dieses Array leer.</span><span class="sxs-lookup"><span data-stu-id="ee255-112">If there are no registered license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee255-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ee255-113">Return value</span></span>

<span data-ttu-id="ee255-114">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ee255-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="ee255-115">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="ee255-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee255-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ee255-116">Requirements</span></span>



| <span data-ttu-id="ee255-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ee255-117">Requirement</span></span> | <span data-ttu-id="ee255-118">Wert</span><span class="sxs-lookup"><span data-stu-id="ee255-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ee255-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ee255-119">Minimum supported client</span></span><br/> | <span data-ttu-id="ee255-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ee255-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ee255-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ee255-121">Minimum supported server</span></span><br/> | <span data-ttu-id="ee255-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="ee255-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="ee255-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="ee255-123">Namespace</span></span><br/>                | <span data-ttu-id="ee255-124">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="ee255-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="ee255-125">MOF</span><span class="sxs-lookup"><span data-stu-id="ee255-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="ee255-126"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="ee255-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="ee255-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ee255-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ee255-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ee255-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee255-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ee255-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee255-130">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="ee255-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

 





