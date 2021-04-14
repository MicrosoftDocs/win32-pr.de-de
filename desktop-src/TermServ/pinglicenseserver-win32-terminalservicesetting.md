---
title: Pinglicenseserver-Methode der Win32_TerminalServiceSetting-Klasse
description: Pinglicenseserver ist nicht mehr verfügbar.
ms.assetid: d2a9f273-1ff9-4391-889b-a3b9c9f95c3b
ms.tgt_platform: multiple
keywords:
- Pinglicenseserver-Methode Remotedesktopdienste
- Pinglicenseserver-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, pinglicenseserver-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.PingLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2fe7277b3130c88c1aec7716c1a3bf560b81db64
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391870"
---
# <a name="pinglicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="9af3a-106">Pinglicenseserver-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="9af3a-106">PingLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="9af3a-107">\[**Pinglicenseserver** ist nicht mehr für die Verwendung ab Windows Server 2008 R2 verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="9af3a-107">\[**PingLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="9af3a-108">**Windows Server 2008:** Pings an den Lizenzserver, um zu ermitteln, ob es sich um einen gültigen Lizenzserver handelt.</span><span class="sxs-lookup"><span data-stu-id="9af3a-108">**Windows Server 2008:** Pings the license server to determine if it is a valid license server.</span></span>

## <a name="syntax"></a><span data-ttu-id="9af3a-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="9af3a-109">Syntax</span></span>


```mof
uint32 PingLicenseServer(
  [in] string ServerName
);
```



## <a name="parameters"></a><span data-ttu-id="9af3a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="9af3a-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9af3a-111">*Servername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="9af3a-111">*ServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9af3a-112">Der Name des Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="9af3a-112">Name of the license server.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9af3a-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9af3a-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="9af3a-114">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="9af3a-114">**S\_OK**</span></span>
</dt> <dd>

<span data-ttu-id="9af3a-115">Der Server ist ein gültiger Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="9af3a-115">The server is a valid license server.</span></span>

</dd> <dt>

<span data-ttu-id="9af3a-116">**S \_ false**</span><span class="sxs-lookup"><span data-stu-id="9af3a-116">**S\_FALSE**</span></span>
</dt> <dd>

<span data-ttu-id="9af3a-117">Der Lizenzserver ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="9af3a-117">The license server is not valid.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9af3a-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9af3a-118">Remarks</span></span>

<span data-ttu-id="9af3a-119">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="9af3a-119">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="9af3a-120">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="9af3a-120">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="9af3a-121">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9af3a-121">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="9af3a-122">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="9af3a-122">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="9af3a-123">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9af3a-123">Requirements</span></span>



| <span data-ttu-id="9af3a-124">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9af3a-124">Requirement</span></span> | <span data-ttu-id="9af3a-125">Wert</span><span class="sxs-lookup"><span data-stu-id="9af3a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9af3a-126">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="9af3a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="9af3a-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9af3a-127">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9af3a-128">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="9af3a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="9af3a-129">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9af3a-129">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9af3a-130">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="9af3a-130">End of client support</span></span><br/>    | <span data-ttu-id="9af3a-131">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="9af3a-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="9af3a-132">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="9af3a-132">End of server support</span></span><br/>    | <span data-ttu-id="9af3a-133">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9af3a-133">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9af3a-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="9af3a-134">Namespace</span></span><br/>                | <span data-ttu-id="9af3a-135">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="9af3a-135">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="9af3a-136">MOF</span><span class="sxs-lookup"><span data-stu-id="9af3a-136">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9af3a-137"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="9af3a-137"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="9af3a-138">DLL</span><span class="sxs-lookup"><span data-stu-id="9af3a-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9af3a-139"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9af3a-139"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9af3a-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9af3a-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9af3a-141">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="9af3a-141">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

