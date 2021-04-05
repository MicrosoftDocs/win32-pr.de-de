---
title: Getcurrentvmmplugin-Methode der Win32_SessionDirectoryVMMPlugin-Klasse
description: Ruft das Plug-in mit der höchsten Priorität ab, das aktiviert ist.
ms.assetid: 7712573f-2252-4a3c-820c-b679be5dfd46
ms.tgt_platform: multiple
keywords:
- Getcurrentvmmplugin-Methode Remotedesktopdienste
- Getcurrentvmmplugin-Methode Remotedesktopdienste, Win32_SessionDirectoryVMMPlugin-Klasse
- Win32_SessionDirectoryVMMPlugin-Klasse Remotedesktopdienste, getcurrentvmmplugin-Methode
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryVMMPlugin.GetCurrentVMMPlugin
api_location:
- TssdWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7162322f4e5e3939309d64e27c93cf8d20da540c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859265"
---
# <a name="getcurrentvmmplugin-method-of-the-win32_sessiondirectoryvmmplugin-class"></a><span data-ttu-id="9324c-106">Getcurrentvmmplugin-Methode der Win32- \_ Klasse sessiondirectoryvmmplugin</span><span class="sxs-lookup"><span data-stu-id="9324c-106">GetCurrentVMMPlugin method of the Win32\_SessionDirectoryVMMPlugin class</span></span>

<span data-ttu-id="9324c-107">Ruft das Plug-in mit der höchsten Priorität ab, das aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9324c-107">Gets the highest priority plug-in that is enabled.</span></span>

## <a name="syntax"></a><span data-ttu-id="9324c-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9324c-108">Syntax</span></span>


```mof
uint32 GetCurrentVMMPlugin(
  [out] string  sName,
  [out] string  sProvider,
  [out] string  sServiceLocation,
  [out] string  sClassID,
  [out] sint32  Priority,
  [out] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="9324c-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9324c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9324c-110">*sname* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9324c-110">*sName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9324c-111">Der Name des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="9324c-111">The name of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="9324c-112">*sprovider* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9324c-112">*sProvider* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9324c-113">Der Name des Plug-in-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="9324c-113">The name of the plug-in provider.</span></span>

</dd> <dt>

<span data-ttu-id="9324c-114">*sservicelokation* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9324c-114">*sServiceLocation* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9324c-115">Der Dienst Speicherort, den das Plug-in kontaktieren soll.</span><span class="sxs-lookup"><span data-stu-id="9324c-115">The service location that the plug-in should contact.</span></span>

</dd> <dt>

<span data-ttu-id="9324c-116">*sclassid* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9324c-116">*sClassID* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9324c-117">Der Klassen Bezeichner des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="9324c-117">The class identifier of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="9324c-118">*Priorität* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9324c-118">*Priority* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9324c-119">Die Priorität des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="9324c-119">The priority of the plug-in.</span></span> <span data-ttu-id="9324c-120">Je höher der Wert ist, desto höher ist die Priorität des Plug-ins.</span><span class="sxs-lookup"><span data-stu-id="9324c-120">The higher the value, the higher the priority of the plug-in.</span></span>

</dd> <dt>

<span data-ttu-id="9324c-121">*Aktiviert* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="9324c-121">*Enabled* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9324c-122">Gibt an, ob das Plug-in aktiviert oder deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9324c-122">Indicates whether the plug-in is enabled or disabled.</span></span> <span data-ttu-id="9324c-123">**True** , wenn das Plug-in aktiviert ist, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="9324c-123">**True** if the plug-in is enabled or **false** otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9324c-124">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9324c-124">Return value</span></span>

<span data-ttu-id="9324c-125">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9324c-125">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9324c-126">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9324c-126">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="requirements"></a><span data-ttu-id="9324c-127">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9324c-127">Requirements</span></span>



| <span data-ttu-id="9324c-128">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9324c-128">Requirement</span></span> | <span data-ttu-id="9324c-129">Wert</span><span class="sxs-lookup"><span data-stu-id="9324c-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9324c-130">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9324c-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9324c-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9324c-131">None supported</span></span><br/>                                                              |
| <span data-ttu-id="9324c-132">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9324c-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9324c-133">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="9324c-133">Windows Server 2008 R2</span></span><br/>                                                      |
| <span data-ttu-id="9324c-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="9324c-134">Namespace</span></span><br/>                | <span data-ttu-id="9324c-135">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9324c-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                               |
| <span data-ttu-id="9324c-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9324c-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9324c-137"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="9324c-137"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9324c-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9324c-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9324c-139"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9324c-139"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9324c-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9324c-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9324c-141">**Win32 \_ sessiondirector yvmmplugin**</span><span class="sxs-lookup"><span data-stu-id="9324c-141">**Win32\_SessionDirectoryVMMPlugin**</span></span>](win32-sessiondirectoryvmmplugin.md)
</dt> </dl>

 

 





