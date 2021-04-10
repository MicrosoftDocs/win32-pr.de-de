---
title: Setfallbackprintdrivertype-Methode der Win32_TerminalServiceSetting-Klasse
description: Die setfallbackprintdrivertype-Methode legt die fallbackprintdrivertype-Eigenschaft für die-Klasse fest.
ms.assetid: be738134-199a-41a6-b2f8-cccfa14fa02b
ms.tgt_platform: multiple
keywords:
- Setfallbackprintdrivertype-Methode Remotedesktopdienste
- Setfallbackprintdrivertype-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, setfallbackprintdrivertype-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetFallbackPrintDriverType
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16e445fef86970e89d5b0f09abebecd40f49ab7f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104040930"
---
# <a name="setfallbackprintdrivertype-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="a140d-106">Setfallbackprintdrivertype-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="a140d-106">SetFallbackPrintDriverType method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="a140d-107">Die **setfallbackprintdrivertype** -Methode legt die **fallbackprintdrivertype** -Eigenschaft für die-Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="a140d-107">The **SetFallbackPrintDriverType** method sets the **FallbackPrintDriverType** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="a140d-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="a140d-108">Syntax</span></span>


```mof
uint32 SetFallbackPrintDriverType(
  [in] uint32 FallbackPrintDriverType
);
```



## <a name="parameters"></a><span data-ttu-id="a140d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a140d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a140d-110">*Fallbackprintdrivertype* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="a140d-110">*FallbackPrintDriverType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a140d-111">Legt die **fallbackprintdrivertype** -Eigenschaft fest, die neue Remotedesktopdienste Verbindungen zulässt oder ablehnt.</span><span class="sxs-lookup"><span data-stu-id="a140d-111">Sets the **FallbackPrintDriverType** property which allows or denies new Remote Desktop Services connections.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="a140d-112"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="a140d-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="a140d-113">Keine Fall Back Treiber.</span><span class="sxs-lookup"><span data-stu-id="a140d-113">No fallback drivers.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="a140d-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="a140d-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="a140d-115">Beste Schätzung.</span><span class="sxs-lookup"><span data-stu-id="a140d-115">Best guess.</span></span>

</dd> <dt>

<span id="2"></span>

<span data-ttu-id="a140d-116"><span id="2"></span>**2**</span><span class="sxs-lookup"><span data-stu-id="a140d-116"><span id="2"></span>**2**</span></span>


</dt> <dd>

<span data-ttu-id="a140d-117">Beste Schätzung.</span><span class="sxs-lookup"><span data-stu-id="a140d-117">Best guess.</span></span> <span data-ttu-id="a140d-118">Wenn keine Entsprechung gefunden wird, Fall Back auf Hewlett-Packard-druckersteuerungsprache (PCL).</span><span class="sxs-lookup"><span data-stu-id="a140d-118">If no match is found, fallback to Hewlett-Packard Printer Control Language (PCL).</span></span>

</dd> <dt>

<span id="3"></span>

<span data-ttu-id="a140d-119"><span id="3"></span>**€**</span><span class="sxs-lookup"><span data-stu-id="a140d-119"><span id="3"></span>**3**</span></span>


</dt> <dd>

<span data-ttu-id="a140d-120">Beste Schätzung.</span><span class="sxs-lookup"><span data-stu-id="a140d-120">Best guess.</span></span> <span data-ttu-id="a140d-121">Wenn keine Entsprechung gefunden wird, Fall Back auf PostScript (PS).</span><span class="sxs-lookup"><span data-stu-id="a140d-121">If no match is found, fallback to Postscript (PS).</span></span>

</dd> <dt>

<span id="4"></span>

<span data-ttu-id="a140d-122"><span id="4"></span>**4**</span><span class="sxs-lookup"><span data-stu-id="a140d-122"><span id="4"></span>**4**</span></span>


</dt> <dd>

<span data-ttu-id="a140d-123">Beste Schätzung.</span><span class="sxs-lookup"><span data-stu-id="a140d-123">Best guess.</span></span> <span data-ttu-id="a140d-124">Wenn keine Entsprechung gefunden wird, zeigen Sie sowohl PS-als auch PCL-Treiber an.</span><span class="sxs-lookup"><span data-stu-id="a140d-124">If no match is found, show both PS and PCL drivers.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a140d-125">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a140d-125">Return value</span></span>

<span data-ttu-id="a140d-126">Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a140d-126">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="a140d-127">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="a140d-127">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="a140d-128">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="a140d-128">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="a140d-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a140d-129">Remarks</span></span>

<span data-ttu-id="a140d-130">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="a140d-130">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="a140d-131">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="a140d-131">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="a140d-132">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="a140d-132">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="a140d-133">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="a140d-133">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="a140d-134">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="a140d-134">Requirements</span></span>



| <span data-ttu-id="a140d-135">Anforderung</span><span class="sxs-lookup"><span data-stu-id="a140d-135">Requirement</span></span> | <span data-ttu-id="a140d-136">Wert</span><span class="sxs-lookup"><span data-stu-id="a140d-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a140d-137">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="a140d-137">Minimum supported client</span></span><br/> | <span data-ttu-id="a140d-138">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a140d-138">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a140d-139">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="a140d-139">Minimum supported server</span></span><br/> | <span data-ttu-id="a140d-140">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a140d-140">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a140d-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="a140d-141">Namespace</span></span><br/>                | <span data-ttu-id="a140d-142">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="a140d-142">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="a140d-143">MOF</span><span class="sxs-lookup"><span data-stu-id="a140d-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a140d-144"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="a140d-144"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="a140d-145">DLL</span><span class="sxs-lookup"><span data-stu-id="a140d-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a140d-146"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a140d-146"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a140d-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a140d-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a140d-148">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="a140d-148">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

