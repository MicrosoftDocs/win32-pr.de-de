---
title: SetName-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Legt den Namen des Plug-ins fest.
ms.assetid: 8af4abca-f147-4027-91fb-4d669b58caa4
ms.tgt_platform: multiple
keywords:
- SetName-Methode Remotedesktopdienste
- SetName-Methode Remotedesktopdienste, Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste, SetName-Methode
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetName
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2dc9902e8d5931f0800dc6c62d36815f4f78db73
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104340667"
---
# <a name="setname-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="46fe4-106">SetName-Methode der Win32- \_ Klasse "sessiondirectoryvmmplugin"</span><span class="sxs-lookup"><span data-stu-id="46fe4-106">SetName method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="46fe4-107">Legt den Namen des Plug-ins fest.</span><span class="sxs-lookup"><span data-stu-id="46fe4-107">Sets the name of the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="46fe4-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="46fe4-108">Syntax</span></span>


```mof
uint32 SetName(
  [in] string sName
);
```



## <a name="parameters"></a><span data-ttu-id="46fe4-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="46fe4-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46fe4-110">*sname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46fe4-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46fe4-111">Der Name des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="46fe4-111">The name of the plug-in.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46fe4-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46fe4-112">Return value</span></span>

<span data-ttu-id="46fe4-113">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46fe4-113">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="46fe4-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="46fe4-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="46fe4-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46fe4-115">Requirements</span></span>



| <span data-ttu-id="46fe4-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46fe4-116">Requirement</span></span> | <span data-ttu-id="46fe4-117">Wert</span><span class="sxs-lookup"><span data-stu-id="46fe4-117">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="46fe4-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46fe4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="46fe4-119">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="46fe4-119">None supported</span></span><br/>                                                              |
| <span data-ttu-id="46fe4-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46fe4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="46fe4-121">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="46fe4-121">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="46fe4-122">Namespace</span><span class="sxs-lookup"><span data-stu-id="46fe4-122">Namespace</span></span><br/>                | <span data-ttu-id="46fe4-123">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="46fe4-123">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="46fe4-124">MOF</span><span class="sxs-lookup"><span data-stu-id="46fe4-124">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46fe4-125"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="46fe4-125"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="46fe4-126">DLL</span><span class="sxs-lookup"><span data-stu-id="46fe4-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46fe4-127"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46fe4-127"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46fe4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46fe4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46fe4-129">**Win32 \_ sessiondirector yvmmplugin**</span><span class="sxs-lookup"><span data-stu-id="46fe4-129">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





