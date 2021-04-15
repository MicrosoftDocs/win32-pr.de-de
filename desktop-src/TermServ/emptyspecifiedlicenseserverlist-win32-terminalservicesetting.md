---
title: Emptyspecifiedlicenseserverlist-Methode der Win32_TerminalServiceSetting-Klasse
description: Entfernt alle Lizenzserver aus der Liste der angegebenen Lizenzserver.
ms.assetid: de1633ca-3f0b-4540-8b45-44303a4e72fe
ms.tgt_platform: multiple
keywords:
- Emptyspecifiedlicenseserverlist-Methode Remotedesktopdienste
- Emptyspecifiedlicenseserverlist-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, emptyspecifiedlicenseserverlist-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.EmptySpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1392c05618860f742a13140167e423b312e49b0a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479320"
---
# <a name="emptyspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="46189-106">Emptyspecifiedlicenseserverlist-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="46189-106">EmptySpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="46189-107">Entfernt alle Lizenzserver aus der Liste der angegebenen Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="46189-107">Removes all license servers from the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="46189-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="46189-108">Syntax</span></span>


```mof
uint32 EmptySpecifiedLicenseServerList();
```



## <a name="parameters"></a><span data-ttu-id="46189-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="46189-109">Parameters</span></span>

<span data-ttu-id="46189-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="46189-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="46189-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46189-111">Return value</span></span>

<span data-ttu-id="46189-112">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46189-112">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="46189-113">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="46189-113">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="46189-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46189-114">Requirements</span></span>



| <span data-ttu-id="46189-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46189-115">Requirement</span></span> | <span data-ttu-id="46189-116">Wert</span><span class="sxs-lookup"><span data-stu-id="46189-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46189-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46189-117">Minimum supported client</span></span><br/> | <span data-ttu-id="46189-118">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="46189-118">None supported</span></span><br/>                                                               |
| <span data-ttu-id="46189-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46189-119">Minimum supported server</span></span><br/> | <span data-ttu-id="46189-120">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46189-120">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="46189-121">Namespace</span><span class="sxs-lookup"><span data-stu-id="46189-121">Namespace</span></span><br/>                | <span data-ttu-id="46189-122">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="46189-122">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="46189-123">MOF</span><span class="sxs-lookup"><span data-stu-id="46189-123">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46189-124"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="46189-124"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="46189-125">DLL</span><span class="sxs-lookup"><span data-stu-id="46189-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46189-126"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46189-126"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46189-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46189-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46189-128">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="46189-128">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="46189-129">**Addlstospecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="46189-129">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="46189-130">**Getspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="46189-130">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="46189-131">**Removelsfromspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="46189-131">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="46189-132">**Setspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="46189-132">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





