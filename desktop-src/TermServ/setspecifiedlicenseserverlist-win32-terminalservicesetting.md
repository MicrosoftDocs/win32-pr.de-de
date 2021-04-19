---
title: Setspecifiedlicenseserverlist-Methode der Win32_TerminalServiceSetting-Klasse
description: Aktualisiert die Liste der angegebenen Lizenzserver, wobei alle vorhandenen angegebenen Lizenzserver ersetzt werden.
ms.assetid: afd7ca11-9db5-4cf3-9706-3c6984789ecd
ms.tgt_platform: multiple
keywords:
- Setspecifiedlicenseserverlist-Methode Remotedesktopdienste
- Setspecifiedlicenseserverlist-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, setspecifiedlicenseserverlist-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d10fde34e490f26c287e63dcddae3c62761670bc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342843"
---
# <a name="setspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="24704-106">Setspecifiedlicenseserverlist-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="24704-106">SetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="24704-107">Aktualisiert die Liste der angegebenen Lizenzserver, wobei alle vorhandenen angegebenen Lizenzserver ersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="24704-107">Updates the list of specified license servers, replacing any existing specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="24704-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="24704-108">Syntax</span></span>


```mof
uint32 SetSpecifiedLicenseServerList(
  [in] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="24704-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="24704-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="24704-110">*Spezifiedlslist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="24704-110">*SpecifiedLSList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="24704-111">Ein Zeichen folgen Array, das die neue Liste der angegebenen Lizenzserver enthält.</span><span class="sxs-lookup"><span data-stu-id="24704-111">A string array that contains the new list of specified license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="24704-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="24704-112">Return value</span></span>

<span data-ttu-id="24704-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="24704-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="24704-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="24704-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="24704-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="24704-115">Requirements</span></span>



| <span data-ttu-id="24704-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="24704-116">Requirement</span></span> | <span data-ttu-id="24704-117">Wert</span><span class="sxs-lookup"><span data-stu-id="24704-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="24704-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="24704-118">Minimum supported client</span></span><br/> | <span data-ttu-id="24704-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="24704-119">None supported</span></span><br/>                                                               |
| <span data-ttu-id="24704-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="24704-120">Minimum supported server</span></span><br/> | <span data-ttu-id="24704-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="24704-121">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="24704-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="24704-122">Namespace</span></span><br/>                | <span data-ttu-id="24704-123">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="24704-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="24704-124">MOF</span><span class="sxs-lookup"><span data-stu-id="24704-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="24704-125"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="24704-125"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="24704-126">DLL</span><span class="sxs-lookup"><span data-stu-id="24704-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="24704-127"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="24704-127"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24704-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24704-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24704-129">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="24704-129">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="24704-130">**Addlstospecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="24704-130">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="24704-131">**Getspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="24704-131">**GetSpecifiedLicenseServerList**</span></span>](getspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="24704-132">**Emptyspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="24704-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="24704-133">**Removelsfromspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="24704-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





