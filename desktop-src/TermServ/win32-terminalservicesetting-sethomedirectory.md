---
title: Die Methode "" der Klasse "Win32_TerminalServiceSetting".
description: Legt die terminalserviceshomedirectory-Eigenschaft für die-Klasse fest.
ms.assetid: 8173cd5b-965e-41bc-97cf-70d8729b8cea
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste der Methode ""
- Methode Remotedesktopdienste der Methode Win32_TerminalServiceSetting Klasse
- Win32_TerminalServiceSetting Klasse Remotedesktopdienste, Methode "Methode"
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.SetHomeDirectory
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1be732cae76b0681afd77693a07f673ef37c4a12
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517678"
---
# <a name="sethomedirectory-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="099be-106">Setup Directory-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="099be-106">SetHomeDirectory method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="099be-107">Die **sethomedirectory** -Methode legt die **terminalserviceshomedirectory** -Eigenschaft für die-Klasse fest.</span><span class="sxs-lookup"><span data-stu-id="099be-107">The **SetHomeDirectory** method sets the **TerminalServicesHomeDirectory** property for the class.</span></span>

## <a name="syntax"></a><span data-ttu-id="099be-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="099be-108">Syntax</span></span>


```mof
uint32 SetHomeDirectory(
  [in] string HomeDirectory
);
```



## <a name="parameters"></a><span data-ttu-id="099be-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="099be-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="099be-110">*Homedirectory* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="099be-110">*HomeDirectory* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="099be-111">Der neue Wert für die **terminalserviceshomedirectory** -Eigenschaft, die das Stammverzeichnis des Computers angibt.</span><span class="sxs-lookup"><span data-stu-id="099be-111">The new value for the **TerminalServicesHomeDirectory** property, which specifies the computer's root directory.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="099be-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="099be-112">Return value</span></span>

<span data-ttu-id="099be-113">Gibt bei Erfolg Erfolg zurück. Andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="099be-113">Returns Success on success; otherwise, returns a WMI error code.</span></span> <span data-ttu-id="099be-114">Eine Liste der WMI-Fehlercodes finden Sie unter [Remotedesktopdienste WMI-Anbieter-Fehlercodes](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="099be-114">For a list of WMI error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="099be-115">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="099be-115">Remarks</span></span>

<span data-ttu-id="099be-116">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="099be-116">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="099be-117">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="099be-117">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="099be-118">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="099be-118">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="099be-119">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="099be-119">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="099be-120">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="099be-120">Requirements</span></span>



| <span data-ttu-id="099be-121">Anforderung</span><span class="sxs-lookup"><span data-stu-id="099be-121">Requirement</span></span> | <span data-ttu-id="099be-122">Wert</span><span class="sxs-lookup"><span data-stu-id="099be-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="099be-123">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="099be-123">Minimum supported client</span></span><br/> | <span data-ttu-id="099be-124">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="099be-124">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="099be-125">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="099be-125">Minimum supported server</span></span><br/> | <span data-ttu-id="099be-126">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="099be-126">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="099be-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="099be-127">Namespace</span></span><br/>                | <span data-ttu-id="099be-128">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="099be-128">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="099be-129">MOF</span><span class="sxs-lookup"><span data-stu-id="099be-129">MOF</span></span><br/>                      | <dl> <span data-ttu-id="099be-130"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="099be-130"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="099be-131">DLL</span><span class="sxs-lookup"><span data-stu-id="099be-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="099be-132"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="099be-132"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="099be-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="099be-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="099be-134">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="099be-134">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

