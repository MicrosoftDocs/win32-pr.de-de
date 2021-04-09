---
title: SetPriority-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Legt die Priorität des Plug-ins fest.
ms.assetid: ddcf30cd-b87c-4869-80fc-ec92092e0df3
ms.tgt_platform: multiple
keywords:
- SetPriority-Methode Remotedesktopdienste
- SetPriority-Methode Remotedesktopdienste, Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste, SetPriority-Methode
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetPriority
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5d20dbc4af332d0c658f819f8e47f5b3eb4e95b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957151"
---
# <a name="setpriority-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="a19c3-106">SetPriority-Methode der Win32- \_ Klasse "sessiondirectoryvmmplugin"</span><span class="sxs-lookup"><span data-stu-id="a19c3-106">SetPriority method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="a19c3-107">Legt die Priorität des Plug-ins fest.</span><span class="sxs-lookup"><span data-stu-id="a19c3-107">Sets the priority of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="a19c3-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a19c3-108">Syntax</span></span>


```mof
uint32 SetPriority(
  [in] sint32 Priority
);
```



## <a name="parameters"></a><span data-ttu-id="a19c3-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a19c3-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a19c3-110">*Priorität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a19c3-110">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a19c3-111">Die Priorität des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="a19c3-111">The priority of the plug-in.</span></span> <span data-ttu-id="a19c3-112">Je höher der Wert ist, desto höher ist die Priorität des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="a19c3-112">The higher the value, the higher the priority of the plug-in.</span></span> <span data-ttu-id="a19c3-113">Der Standardwert ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="a19c3-113">The priority is zero by default.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a19c3-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a19c3-114">Return value</span></span>

<span data-ttu-id="a19c3-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a19c3-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a19c3-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a19c3-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="a19c3-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a19c3-117">Requirements</span></span>



| <span data-ttu-id="a19c3-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a19c3-118">Requirement</span></span> | <span data-ttu-id="a19c3-119">Wert</span><span class="sxs-lookup"><span data-stu-id="a19c3-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a19c3-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a19c3-120">Minimum supported client</span></span><br/> | <span data-ttu-id="a19c3-121">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="a19c3-121">None supported</span></span><br/>                                                              |
| <span data-ttu-id="a19c3-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a19c3-122">Minimum supported server</span></span><br/> | <span data-ttu-id="a19c3-123">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="a19c3-123">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="a19c3-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="a19c3-124">Namespace</span></span><br/>                | <span data-ttu-id="a19c3-125">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a19c3-125">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="a19c3-126">MOF</span><span class="sxs-lookup"><span data-stu-id="a19c3-126">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a19c3-127"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="a19c3-127"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a19c3-128">DLL</span><span class="sxs-lookup"><span data-stu-id="a19c3-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a19c3-129"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a19c3-129"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a19c3-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a19c3-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a19c3-131">**Win32 \_ sessiondirector yvmmplugin**</span><span class="sxs-lookup"><span data-stu-id="a19c3-131">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





