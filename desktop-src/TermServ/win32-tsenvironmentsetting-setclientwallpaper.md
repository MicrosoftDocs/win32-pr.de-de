---
title: Setclientwallpaper-Methode der Win32_TSEnvironmentSetting-Klasse
description: Die setclientwallpaper-Methode legt die ClientWallPaper-Eigenschaft fest.
ms.assetid: 08c41df4-5a3c-4799-bb64-61f414814d0c
ms.tgt_platform: multiple
keywords:
- Setclientwallpaper-Methode Remotedesktopdienste
- Setclientwallpaper-Methode Remotedesktopdienste, Win32_TSEnvironmentSetting-Klasse
- Win32_TSEnvironmentSetting-Klasse Remotedesktopdienste, setclientwallpaper-Methode
topic_type:
- apiref
api_name:
- Win32_TSEnvironmentSetting.SetClientWallPaper
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04ae476134cf526602a059b4714cded6fd6c990e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103741257"
---
# <a name="setclientwallpaper-method-of-the-win32_tsenvironmentsetting-class"></a><span data-ttu-id="46ed1-106">Setclientwallpaper-Methode der Win32- \_ Klasse "tsenvironmentsetting"</span><span class="sxs-lookup"><span data-stu-id="46ed1-106">SetClientWallPaper method of the Win32\_TSEnvironmentSetting class</span></span>

<span data-ttu-id="46ed1-107">Die **setclientwallpaper** -Methode legt die **ClientWallPaper** -Eigenschaft fest.</span><span class="sxs-lookup"><span data-stu-id="46ed1-107">The **SetClientWallPaper** method sets the **ClientWallPaper** property.</span></span>

## <a name="syntax"></a><span data-ttu-id="46ed1-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="46ed1-108">Syntax</span></span>


```mof
uint32 SetClientWallPaper(
  [in] uint32 ClientWallPaper
);
```



## <a name="parameters"></a><span data-ttu-id="46ed1-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="46ed1-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46ed1-110">*ClientWallPaper* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="46ed1-110">*ClientWallPaper* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="46ed1-111">Flag zum Deaktivieren oder Aktivieren der **ClientWallPaper** -Eigenschaft, die angibt, ob das Hintergrundbild (oder Hintergrundbild) auf dem Client angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="46ed1-111">Flag disabling or enabling the **ClientWallPaper** property, which specifies whether the background (or wallpaper) image is displayed on the client.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="46ed1-112"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="46ed1-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="46ed1-113">Das Hintergrundbild (oder Hintergrundbild) wird auf dem Client nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46ed1-113">The background (or wallpaper) image is not displayed on the client.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="46ed1-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="46ed1-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="46ed1-115">Das Hintergrundbild (oder Hintergrundbild) wird auf dem Client angezeigt.</span><span class="sxs-lookup"><span data-stu-id="46ed1-115">The background (or wallpaper) image is displayed on the client.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46ed1-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="46ed1-116">Return value</span></span>

<span data-ttu-id="46ed1-117">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="46ed1-117">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="46ed1-118">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="46ed1-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="46ed1-119">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="46ed1-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="46ed1-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46ed1-120">Remarks</span></span>

<span data-ttu-id="46ed1-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="46ed1-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="46ed1-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="46ed1-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="46ed1-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="46ed1-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="46ed1-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="46ed1-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="46ed1-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="46ed1-125">Requirements</span></span>



| <span data-ttu-id="46ed1-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="46ed1-126">Requirement</span></span> | <span data-ttu-id="46ed1-127">Wert</span><span class="sxs-lookup"><span data-stu-id="46ed1-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="46ed1-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="46ed1-128">Minimum supported client</span></span><br/> | <span data-ttu-id="46ed1-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="46ed1-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="46ed1-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="46ed1-130">Minimum supported server</span></span><br/> | <span data-ttu-id="46ed1-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="46ed1-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="46ed1-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="46ed1-132">Namespace</span></span><br/>                | <span data-ttu-id="46ed1-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="46ed1-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="46ed1-134">MOF</span><span class="sxs-lookup"><span data-stu-id="46ed1-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="46ed1-135"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="46ed1-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="46ed1-136">DLL</span><span class="sxs-lookup"><span data-stu-id="46ed1-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="46ed1-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="46ed1-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="46ed1-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46ed1-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="46ed1-139">**Win32- \_ tsenvironmentsetting**</span><span class="sxs-lookup"><span data-stu-id="46ed1-139">**Win32\_TSEnvironmentSetting**</span></span>](win32-tsenvironmentsetting.md)
</dt> </dl>

 

