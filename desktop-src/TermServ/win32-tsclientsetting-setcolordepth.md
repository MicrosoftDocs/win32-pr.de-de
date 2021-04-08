---
title: Setcolortiefe-Methode der Win32_TSClientSetting-Klasse
description: Die setcolortiefe-Methode legt die colortiefe-Eigenschaft für die-Klasse fest.
ms.assetid: 1ab8ac41-cbbf-4077-b91e-692856ccba42
ms.tgt_platform: multiple
keywords:
- Setcolortiefe-Methode Remotedesktopdienste
- Setcolortiefe-Methode Remotedesktopdienste, Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste, setcolortiefe-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepth
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 97f2b05c6b8ff02b78f48ff45751bdc8e57ef46a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103957055"
---
# <a name="setcolordepth-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="f9a9b-106">Setcolortiefe-Methode der Win32- \_ Klasse tsclientsetting</span><span class="sxs-lookup"><span data-stu-id="f9a9b-106">SetColorDepth method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="f9a9b-107">Die **setcolortiefe** -Methode legt die **colortiefe** -Eigenschaft für die-Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-107">The **SetColorDepth** method sets the **ColorDepth** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="f9a9b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f9a9b-108">Syntax</span></span>


```mof
uint32 SetColorDepth(
  [in] uint32 ColorDepth
);
```



## <a name="parameters"></a><span data-ttu-id="f9a9b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9a9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f9a9b-110">*Colortiefe* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="f9a9b-110">*ColorDepth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f9a9b-111">Der neue Wert für die **colortiefe** -Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-111">The new value for the **ColorDepth** property.</span></span>

<dt>

<span id="1"></span>

<span data-ttu-id="f9a9b-112"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="f9a9b-112"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="f9a9b-113">8 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="f9a9b-113">8 bits per pixel</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="f9a9b-114"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="f9a9b-114"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="f9a9b-115">15 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="f9a9b-115">15 bits per pixel</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="f9a9b-116"><span id="3"></span>**€**</span><span class="sxs-lookup"><span data-stu-id="f9a9b-116"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="f9a9b-117">16 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="f9a9b-117">16 bits per pixel</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="f9a9b-118"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="f9a9b-118"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="f9a9b-119">24 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="f9a9b-119">24 bits per pixel</span></span>

</dd> <dt>

<span id="5"></span>

<span data-ttu-id="f9a9b-120"><span id="5"></span>**5@@**</span><span class="sxs-lookup"><span data-stu-id="f9a9b-120"><span id="5"></span>**5**</span></span>


</dt> <dd>

<span data-ttu-id="f9a9b-121">32 Bits pro Pixel</span><span class="sxs-lookup"><span data-stu-id="f9a9b-121">32 bits per pixel</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f9a9b-122">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9a9b-122">Return value</span></span>

<span data-ttu-id="f9a9b-123">Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-123">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="f9a9b-124">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="f9a9b-124">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="f9a9b-125">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-125">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="f9a9b-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9a9b-126">Remarks</span></span>

<span data-ttu-id="f9a9b-127">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-127">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="f9a9b-128">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-128">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="f9a9b-129">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f9a9b-129">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="f9a9b-130">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="f9a9b-130">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="f9a9b-131">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="f9a9b-131">Requirements</span></span>



| <span data-ttu-id="f9a9b-132">Anforderung</span><span class="sxs-lookup"><span data-stu-id="f9a9b-132">Requirement</span></span> | <span data-ttu-id="f9a9b-133">Wert</span><span class="sxs-lookup"><span data-stu-id="f9a9b-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f9a9b-134">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="f9a9b-134">Minimum supported client</span></span><br/> | <span data-ttu-id="f9a9b-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f9a9b-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f9a9b-136">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="f9a9b-136">Minimum supported server</span></span><br/> | <span data-ttu-id="f9a9b-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f9a9b-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f9a9b-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9a9b-138">Namespace</span></span><br/>                | <span data-ttu-id="f9a9b-139">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="f9a9b-139">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="f9a9b-140">MOF</span><span class="sxs-lookup"><span data-stu-id="f9a9b-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f9a9b-141"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="f9a9b-141"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="f9a9b-142">DLL</span><span class="sxs-lookup"><span data-stu-id="f9a9b-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f9a9b-143"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f9a9b-143"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f9a9b-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9a9b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f9a9b-145">**Win32- \_ tsclientsetting**</span><span class="sxs-lookup"><span data-stu-id="f9a9b-145">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

