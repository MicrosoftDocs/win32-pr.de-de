---
title: Die "stenabled"-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Aktiviert oder deaktiviert das Plug-in.
ms.assetid: 25ce0614-5c3b-4a79-9174-1a9de1eb6c33
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode ""
- Remotedesktopdienste der Methode "" der Klasse "Win32_SessionDirectoryVMMPlugin"
- Win32_SessionDirectoryVMMPlugin Klasse Remotedesktopdienste, Methode "".
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.SetEnabled
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef7089a21f143b6f3b27fe9fe58563e6777bf2f4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103743609"
---
# <a name="setenabled-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="7f7ee-106">Die "stenabled"-Methode der Win32- \_ Klasse "sessiondirectoryvmmplugin"</span><span class="sxs-lookup"><span data-stu-id="7f7ee-106">SetEnabled method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="7f7ee-107">Aktiviert oder deaktiviert das Plug-in.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-107">Enables or disables the plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="7f7ee-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="7f7ee-108">Syntax</span></span>


```mof
uint32 SetEnabled(
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="7f7ee-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="7f7ee-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7f7ee-110">*Aktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7f7ee-110">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7f7ee-111">Gibt an, ob das Plug-in aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-111">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="7f7ee-112">**True** , wenn das Plug-in aktiviert ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="7f7ee-112">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7f7ee-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7f7ee-113">Return value</span></span>

<span data-ttu-id="7f7ee-114">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="7f7ee-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="7f7ee-115">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="7f7ee-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f7ee-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7f7ee-116">Requirements</span></span>



| <span data-ttu-id="7f7ee-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f7ee-117">Requirement</span></span> | <span data-ttu-id="7f7ee-118">Wert</span><span class="sxs-lookup"><span data-stu-id="7f7ee-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7f7ee-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7f7ee-119">Minimum supported client</span></span><br/> | <span data-ttu-id="7f7ee-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="7f7ee-120">None supported</span></span><br/>                                                              |
| <span data-ttu-id="7f7ee-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7f7ee-121">Minimum supported server</span></span><br/> | <span data-ttu-id="7f7ee-122">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="7f7ee-122">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="7f7ee-123">Namespace</span><span class="sxs-lookup"><span data-stu-id="7f7ee-123">Namespace</span></span><br/>                | <span data-ttu-id="7f7ee-124">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="7f7ee-124">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="7f7ee-125">MOF</span><span class="sxs-lookup"><span data-stu-id="7f7ee-125">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7f7ee-126"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="7f7ee-126"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="7f7ee-127">DLL</span><span class="sxs-lookup"><span data-stu-id="7f7ee-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7f7ee-128"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7f7ee-128"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7f7ee-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7f7ee-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7f7ee-130">**Win32 \_ sessiondirector yvmmplugin**</span><span class="sxs-lookup"><span data-stu-id="7f7ee-130">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





