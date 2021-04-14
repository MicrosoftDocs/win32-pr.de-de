---
title: Registervmmplugin-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Registriert ein neues VMM-Plug-in.
ms.assetid: 8fa6109e-6320-4ad1-b313-f100d8383f85
ms.tgt_platform: multiple
keywords:
- Registervmmplugin-Methode Remotedesktopdienste
- Registervmmplugin-Methode Remotedesktopdienste, Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste, registervmmplugin-Methode
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.RegisterVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381be34f9398147b323fa99093479da48adfd480
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391722"
---
# <a name="registervmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="08abf-106">Registervmmplugin-Methode der Win32- \_ Klasse sessiondirectoryvmmplugin</span><span class="sxs-lookup"><span data-stu-id="08abf-106">RegisterVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="08abf-107">Registriert ein neues VMM-Plug-in.</span><span class="sxs-lookup"><span data-stu-id="08abf-107">Registers a new VMM plug-in.</span></span>

## <a name="syntax"></a><span data-ttu-id="08abf-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="08abf-108">Syntax</span></span>


```mof
uint32 RegisterVMMPlugin(
  [in] string  sName,
  [in] string  sProvider,
  [in] string  sServiceLocation,
  [in] string  sClassID,
  [in] sint32  Priority = ,
  [in] boolean Enabled = 
);
```



## <a name="parameters"></a><span data-ttu-id="08abf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="08abf-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="08abf-110">*sname* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08abf-110">*sName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08abf-111">Der Name des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="08abf-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="08abf-112">*sprovider* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08abf-112">*sProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08abf-113">Der Name des Plug-in-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="08abf-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="08abf-114">*sservicelokation* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08abf-114">*sServiceLocation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08abf-115">Der Dienst Speicherort, den das Plug-in kontaktieren soll.</span><span class="sxs-lookup"><span data-stu-id="08abf-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="08abf-116">*sclassid* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08abf-116">*sClassID* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08abf-117">Der Klassen Bezeichner des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="08abf-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="08abf-118">*Priorität* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08abf-118">*Priority* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08abf-119">Die Priorität des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="08abf-119">The priority of the plug-in.</span></span> <span data-ttu-id="08abf-120">Je höher der Wert ist, desto höher ist die Priorität des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="08abf-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="08abf-121">*Aktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="08abf-121">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="08abf-122">Gibt an, ob das Plug-in aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="08abf-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="08abf-123">**True** , wenn das Plug-in aktiviert ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="08abf-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="08abf-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="08abf-124">Return value</span></span>

<span data-ttu-id="08abf-125">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="08abf-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="08abf-126">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="08abf-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="08abf-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="08abf-127">Requirements</span></span>



| <span data-ttu-id="08abf-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="08abf-128">Requirement</span></span> | <span data-ttu-id="08abf-129">Wert</span><span class="sxs-lookup"><span data-stu-id="08abf-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="08abf-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="08abf-130">Minimum supported client</span></span><br/> | <span data-ttu-id="08abf-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="08abf-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="08abf-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="08abf-132">Minimum supported server</span></span><br/> | <span data-ttu-id="08abf-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="08abf-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="08abf-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="08abf-134">Namespace</span></span><br/>                | <span data-ttu-id="08abf-135">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="08abf-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="08abf-136">MOF</span><span class="sxs-lookup"><span data-stu-id="08abf-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="08abf-137"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="08abf-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="08abf-138">DLL</span><span class="sxs-lookup"><span data-stu-id="08abf-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="08abf-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="08abf-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="08abf-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="08abf-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="08abf-141">**Win32 \_ sessiondirector yvmmplugin**</span><span class="sxs-lookup"><span data-stu-id="08abf-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





