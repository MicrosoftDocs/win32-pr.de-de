---
title: Updatedirectconnectlicenseserver-Methode der Win32_TerminalServiceSetting-Klasse
description: Updatedirectconnectlicenseserver ist nicht mehr verfügbar.
ms.assetid: 0b6e0dba-e23b-4c8d-8021-93d802501359
ms.tgt_platform: multiple
keywords:
- Updatedirectconnectlicenseserver-Methode Remotedesktopdienste
- Updatedirectconnectlicenseserver-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, updatedirectconnectlicenseserver-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.UpdateDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d2249dd00b44955a4e2712b8b7bf746793e89d57
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106341390"
---
# <a name="updatedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="0694a-106">Updatedirectconnectlicenseserver-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="0694a-106">UpdateDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="0694a-107">\[**Updatedirectconnectlicenseserver** ist nicht mehr für die Verwendung ab Windows Server 2008 R2 verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="0694a-107">\[**UpdateDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="0694a-108">**Windows Server 2008:** Aktualisiert die Liste der Discovery-Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="0694a-108">**Windows Server 2008:** Updates the list of discovery license servers.</span></span> <span data-ttu-id="0694a-109">Die Serverliste wird durch Semikolons (";") getrennt.</span><span class="sxs-lookup"><span data-stu-id="0694a-109">The server list is delimited by semicolons (";").</span></span>

## <a name="syntax"></a><span data-ttu-id="0694a-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="0694a-110">Syntax</span></span>


```mof
uint32 UpdateDirectConnectLicenseServer(
  [in] string LicenseServerList
);
```



## <a name="parameters"></a><span data-ttu-id="0694a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="0694a-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0694a-112">*Licenseserverlist* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="0694a-112">*LicenseServerList* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0694a-113">Liste der Lizenzserver.</span><span class="sxs-lookup"><span data-stu-id="0694a-113">List of license servers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0694a-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0694a-114">Return value</span></span>

<span data-ttu-id="0694a-115">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0694a-115">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="0694a-116">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="0694a-116">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="0694a-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0694a-117">Remarks</span></span>

<span data-ttu-id="0694a-118">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="0694a-118">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="0694a-119">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="0694a-119">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="0694a-120">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="0694a-120">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="0694a-121">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="0694a-121">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="0694a-122">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0694a-122">Requirements</span></span>



| <span data-ttu-id="0694a-123">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0694a-123">Requirement</span></span> | <span data-ttu-id="0694a-124">Wert</span><span class="sxs-lookup"><span data-stu-id="0694a-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="0694a-125">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0694a-125">Minimum supported client</span></span><br/> | <span data-ttu-id="0694a-126">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0694a-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0694a-127">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0694a-127">Minimum supported server</span></span><br/> | <span data-ttu-id="0694a-128">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0694a-128">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0694a-129">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="0694a-129">End of client support</span></span><br/>    | <span data-ttu-id="0694a-130">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="0694a-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="0694a-131">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="0694a-131">End of server support</span></span><br/>    | <span data-ttu-id="0694a-132">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="0694a-132">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="0694a-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="0694a-133">Namespace</span></span><br/>                | <span data-ttu-id="0694a-134">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="0694a-134">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="0694a-135">MOF</span><span class="sxs-lookup"><span data-stu-id="0694a-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0694a-136"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="0694a-136"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="0694a-137">DLL</span><span class="sxs-lookup"><span data-stu-id="0694a-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0694a-138"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0694a-138"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0694a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0694a-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0694a-140">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="0694a-140">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

