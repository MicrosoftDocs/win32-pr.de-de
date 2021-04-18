---
title: Setcolordepthpolicy-Methode der Win32_TSClientSetting-Klasse
description: Die setcolordepthpolicy-Methode legt die ColorDepthPolicy-Eigenschaft für die-Klasse fest.
ms.assetid: 7a8c2b51-5f7a-4188-aae0-0b2d47d043bd
ms.tgt_platform: multiple
keywords:
- Setcolordepthpolicy-Methode Remotedesktopdienste
- Setcolordepthpolicy-Methode Remotedesktopdienste, Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste, setcolordepthpolicy-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.SetColorDepthPolicy
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f2d47280ce303e7eeba401e0eb34c7f7fa5a7bec
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391851"
---
# <a name="setcolordepthpolicy-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="67e99-106">Setcolordepthpolicy-Methode der Win32- \_ Klasse tsclientsetting</span><span class="sxs-lookup"><span data-stu-id="67e99-106">SetColorDepthPolicy method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="67e99-107">Die **setcolordepthpolicy** -Methode legt die **ColorDepthPolicy** -Eigenschaft für die-Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="67e99-107">The **SetColorDepthPolicy** method sets the **ColorDepthPolicy** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="67e99-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="67e99-108">Syntax</span></span>


```mof
uint32 SetColorDepthPolicy(
  [in] uint32 ColorDepthPolicy
);
```



## <a name="parameters"></a><span data-ttu-id="67e99-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="67e99-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67e99-110">*ColorDepthPolicy* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="67e99-110">*ColorDepthPolicy* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67e99-111">Flag zum Deaktivieren oder Aktivieren der **setcolordepthpolicy** -Eigenschaft, die angibt, ob die Einstellung für die maximale Farbe des Benutzers überschrieben werden soll.</span><span class="sxs-lookup"><span data-stu-id="67e99-111">Flag disabling or enabling the **SetColorDepthPolicy** property, which specifies whether to override the user's maximum color setting.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="67e99-112"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="67e99-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="67e99-113">Aktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="67e99-113">Enable the property.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="67e99-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="67e99-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="67e99-115">Deaktivieren Sie die-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="67e99-115">Disable the property.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="67e99-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="67e99-116">Return value</span></span>

<span data-ttu-id="67e99-117">Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="67e99-117">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="67e99-118">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="67e99-118">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="67e99-119">Die-Methode gibt einen Fehler zurück, wenn die Einstellung Untergruppen Richtlinien Steuerung liegt.</span><span class="sxs-lookup"><span data-stu-id="67e99-119">The method returns an error if the setting is under group policy control.</span></span>

## <a name="remarks"></a><span data-ttu-id="67e99-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="67e99-120">Remarks</span></span>

<span data-ttu-id="67e99-121">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="67e99-121">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="67e99-122">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="67e99-122">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="67e99-123">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="67e99-123">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="67e99-124">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="67e99-124">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="67e99-125">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="67e99-125">Requirements</span></span>



| <span data-ttu-id="67e99-126">Anforderung</span><span class="sxs-lookup"><span data-stu-id="67e99-126">Requirement</span></span> | <span data-ttu-id="67e99-127">Wert</span><span class="sxs-lookup"><span data-stu-id="67e99-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="67e99-128">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="67e99-128">Minimum supported client</span></span><br/> | <span data-ttu-id="67e99-129">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="67e99-129">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="67e99-130">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="67e99-130">Minimum supported server</span></span><br/> | <span data-ttu-id="67e99-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="67e99-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="67e99-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="67e99-132">Namespace</span></span><br/>                | <span data-ttu-id="67e99-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="67e99-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="67e99-134">MOF</span><span class="sxs-lookup"><span data-stu-id="67e99-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="67e99-135"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="67e99-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="67e99-136">DLL</span><span class="sxs-lookup"><span data-stu-id="67e99-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="67e99-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="67e99-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="67e99-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="67e99-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="67e99-139">**Win32- \_ tsclientsetting**</span><span class="sxs-lookup"><span data-stu-id="67e99-139">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

