---
title: Die Methode "stallowdwm" der Win32_TSClientSetting-Klasse
description: Legt die allowdwm-Eigenschaft fest.
ms.assetid: c70d3dc9-c109-4d77-be50-20a0352282d6
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode "stallowdwm"
- Remotedesktopdienste der Methode "" der Klasse "Win32_TSClientSetting"
- Win32_TSClientSetting-Klasse Remotedesktopdienste,-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetAllowDwm
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 39441ba3244f206b057ba47c3cb6f765b5e80604
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341796"
---
# <a name="setallowdwm-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="30114-106">Die "Set-lowdwm"-Methode der Win32- \_ Klasse "tsclientsetting"</span><span class="sxs-lookup"><span data-stu-id="30114-106">SetAllowDwm method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="30114-107">Legt die **allowdwm** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="30114-107">Sets the **AllowDwm** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="30114-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="30114-108">Syntax</span></span>


```mof
uint32 SetAllowDwm(
  [in] uint32 AllowDwm
);
```



## <a name="parameters"></a><span data-ttu-id="30114-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="30114-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="30114-110">*Allowdwm* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="30114-110">*AllowDwm* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="30114-111">Der neue **allowdwm** -Eigenschafts Wert.</span><span class="sxs-lookup"><span data-stu-id="30114-111">The new **AllowDwm** property value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="30114-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="30114-112">Return value</span></span>

<span data-ttu-id="30114-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="30114-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="30114-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="30114-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="30114-115">Die-Methode gibt einen Fehler zurück, wenn die Verbindungseinstellungen des Benutzers vom Server überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="30114-115">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="requirements"></a><span data-ttu-id="30114-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="30114-116">Requirements</span></span>



| <span data-ttu-id="30114-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="30114-117">Requirement</span></span> | <span data-ttu-id="30114-118">Wert</span><span class="sxs-lookup"><span data-stu-id="30114-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="30114-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="30114-119">Minimum supported client</span></span><br/> | <span data-ttu-id="30114-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="30114-120">None supported</span></span><br/>                                                               |
| <span data-ttu-id="30114-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="30114-121">Minimum supported server</span></span><br/> | <span data-ttu-id="30114-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="30114-122">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="30114-123">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="30114-123">End of client support</span></span><br/>    | <span data-ttu-id="30114-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="30114-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="30114-125">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="30114-125">End of server support</span></span><br/>    | <span data-ttu-id="30114-126">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="30114-126">Windows Server 2008 R2</span></span><br/>                                                       |
| <span data-ttu-id="30114-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="30114-127">Namespace</span></span><br/>                | <span data-ttu-id="30114-128">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="30114-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="30114-129">MOF</span><span class="sxs-lookup"><span data-stu-id="30114-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="30114-130"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="30114-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="30114-131">DLL</span><span class="sxs-lookup"><span data-stu-id="30114-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="30114-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="30114-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30114-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30114-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30114-134">**Win32- \_ tsclientsetting**</span><span class="sxs-lookup"><span data-stu-id="30114-134">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

 





