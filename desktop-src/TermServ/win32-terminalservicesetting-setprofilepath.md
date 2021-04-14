---
title: Setprofilepath-Methode der Win32_TerminalServiceSetting-Klasse
description: Die setprofilepath-Methode legt die ProfilePath-Eigenschaft für die-Klasse fest.
ms.assetid: a0dfe6a4-929c-45ec-bd31-7e0ffb6ce5de
ms.tgt_platform: multiple
keywords:
- Setprofilepath-Methode Remotedesktopdienste
- Setprofilepath-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, setprofilepath-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetProfilePath
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 434909471accc191e79c92287ab6e4ac427bf949
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391854"
---
# <a name="setprofilepath-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="9ec8a-106">Setprofilepath-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="9ec8a-106">SetProfilePath method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="9ec8a-107">Die **setprofilepath** -Methode legt die **ProfilePath** -Eigenschaft für die-Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-107">The **SetProfilePath** method sets the **ProfilePath** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="9ec8a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ec8a-108">Syntax</span></span>


```mof
uint32 SetProfilePath(
  [in] string ProfilePath
);
```



## <a name="parameters"></a><span data-ttu-id="9ec8a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ec8a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9ec8a-110">*Profilpfad* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9ec8a-110">*ProfilePath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9ec8a-111">Der neue Wert für die **ProfilePath** -Eigenschaft, die den Profilpfad des Computers angibt.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-111">The new value for the **ProfilePath** property, which specifies the profile path for the computer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9ec8a-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9ec8a-112">Return value</span></span>

<span data-ttu-id="9ec8a-113">Gibt bei Erfolg Erfolg zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-113">Returns Success on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="9ec8a-114">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="9ec8a-114">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="9ec8a-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ec8a-115">Remarks</span></span>

<span data-ttu-id="9ec8a-116">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9ec8a-117">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9ec8a-118">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9ec8a-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9ec8a-119">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9ec8a-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9ec8a-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9ec8a-120">Requirements</span></span>



| <span data-ttu-id="9ec8a-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9ec8a-121">Requirement</span></span> | <span data-ttu-id="9ec8a-122">Wert</span><span class="sxs-lookup"><span data-stu-id="9ec8a-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9ec8a-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9ec8a-123">Minimum supported client</span></span><br/> | <span data-ttu-id="9ec8a-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9ec8a-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9ec8a-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9ec8a-125">Minimum supported server</span></span><br/> | <span data-ttu-id="9ec8a-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9ec8a-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9ec8a-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="9ec8a-127">Namespace</span></span><br/>                | <span data-ttu-id="9ec8a-128">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9ec8a-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9ec8a-129">MOF</span><span class="sxs-lookup"><span data-stu-id="9ec8a-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9ec8a-130"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9ec8a-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9ec8a-131">DLL</span><span class="sxs-lookup"><span data-stu-id="9ec8a-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9ec8a-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9ec8a-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9ec8a-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9ec8a-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9ec8a-134">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="9ec8a-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

