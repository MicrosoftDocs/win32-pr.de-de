---
title: Getspecifiedlicenseserverlist-Methode der Win32_TerminalServiceSetting-Klasse
description: Ruft die Liste der angegebenen Lizenzserver ab.
ms.assetid: 800be0ce-1002-48e1-be4e-88db22590f12
ms.tgt_platform: multiple
keywords:
- Getspecifiedlicenseserverlist-Methode Remotedesktopdienste
- Getspecifiedlicenseserverlist-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, getspecifiedlicenseserverlist-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.GetSpecifiedLicenseServerList
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1f70c50281cad7072d420082db0e6916a631e2b1
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391607"
---
# <a name="getspecifiedlicenseserverlist-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="e81c2-106">Getspecifiedlicenseserverlist-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="e81c2-106">GetSpecifiedLicenseServerList method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="e81c2-107">Ruft die Liste der angegebenen Lizenzserver ab.</span><span class="sxs-lookup"><span data-stu-id="e81c2-107">Retrieves the list of specified license servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="e81c2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="e81c2-108">Syntax</span></span>


```mof
uint32 GetSpecifiedLicenseServerList(
  [out] string SpecifiedLSList[]
);
```



## <a name="parameters"></a><span data-ttu-id="e81c2-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="e81c2-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e81c2-110">*Spezifiedlslist* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="e81c2-110">*SpecifiedLSList* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e81c2-111">Ein Zeichen folgen Array, das die Liste der Lizenzserver empfängt.</span><span class="sxs-lookup"><span data-stu-id="e81c2-111">A string array that receives the list of license servers.</span></span> <span data-ttu-id="e81c2-112">Wenn keine Lizenzserver vorhanden sind, ist dieses Array leer.</span><span class="sxs-lookup"><span data-stu-id="e81c2-112">If there are no license servers, this array will be empty.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e81c2-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e81c2-113">Return value</span></span>

<span data-ttu-id="e81c2-114">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e81c2-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="e81c2-115">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="e81c2-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="e81c2-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e81c2-116">Requirements</span></span>



| <span data-ttu-id="e81c2-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e81c2-117">Requirement</span></span> | <span data-ttu-id="e81c2-118">Wert</span><span class="sxs-lookup"><span data-stu-id="e81c2-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e81c2-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e81c2-119">Minimum supported client</span></span><br/> | <span data-ttu-id="e81c2-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="e81c2-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="e81c2-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e81c2-121">Minimum supported server</span></span><br/> | <span data-ttu-id="e81c2-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="e81c2-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="e81c2-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="e81c2-123">Namespace</span></span><br/>                | <span data-ttu-id="e81c2-124">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="e81c2-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="e81c2-125">MOF</span><span class="sxs-lookup"><span data-stu-id="e81c2-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e81c2-126"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="e81c2-126"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="e81c2-127">DLL</span><span class="sxs-lookup"><span data-stu-id="e81c2-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e81c2-128"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e81c2-128"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e81c2-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e81c2-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e81c2-130">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="e81c2-130">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="e81c2-131">**Addlstospecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="e81c2-131">**AddLSToSpecifiedLicenseServerList**</span></span>](addlstospecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="e81c2-132">**Emptyspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="e81c2-132">**EmptySpecifiedLicenseServerList**</span></span>](emptyspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="e81c2-133">**Removelsfromspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="e81c2-133">**RemoveLSFromSpecifiedLicenseServerList**</span></span>](removelsfromspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> <dt>

[<span data-ttu-id="e81c2-134">**Setspecifiedlicenseserverlist**</span><span class="sxs-lookup"><span data-stu-id="e81c2-134">**SetSpecifiedLicenseServerList**</span></span>](setspecifiedlicenseserverlist-win32-terminalservicesetting.md)
</dt> </dl>

 

 





