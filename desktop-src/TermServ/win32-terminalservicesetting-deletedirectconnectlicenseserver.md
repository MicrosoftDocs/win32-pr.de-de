---
title: Deletedirectconnectlicenseserver-Methode der Win32_TerminalServiceSetting-Klasse
description: Deletedirectconnectlicenseserver ist nicht mehr verfügbar.
ms.assetid: 190316ab-b8ed-4102-8346-42603d6451e6
ms.tgt_platform: multiple
keywords:
- Deletedirectconnectlicenseserver-Methode Remotedesktopdienste
- Deletedirectconnectlicenseserver-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, deletedirectconnectlicenseserver-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.DeleteDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1929ee4294040e80ec9bb633bd70d4709b3e56b0
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346529"
---
# <a name="deletedirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="452ac-106">Deletedirectconnectlicenseserver-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="452ac-106">DeleteDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="452ac-107">\[**Deletedirectconnectlicenseserver** ist nicht mehr für die Verwendung ab Windows Server 2008 R2 verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="452ac-107">\[**DeleteDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="452ac-108">**Windows Server 2008:** Entfernt einen Lizenzserver aus der Registrierung.</span><span class="sxs-lookup"><span data-stu-id="452ac-108">**Windows Server 2008:** Removes a license server from the registry.</span></span>

## <a name="syntax"></a><span data-ttu-id="452ac-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="452ac-109">Syntax</span></span>


```mof
uint32 DeleteDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="452ac-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="452ac-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="452ac-111">*Licenseservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="452ac-111">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="452ac-112">Der Name des zu entfernenden Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="452ac-112">Name of the license server to remove.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="452ac-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="452ac-113">Return value</span></span>

<span data-ttu-id="452ac-114">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="452ac-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="452ac-115">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="452ac-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="452ac-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="452ac-116">Remarks</span></span>

<span data-ttu-id="452ac-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="452ac-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="452ac-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="452ac-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="452ac-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="452ac-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="452ac-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="452ac-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="452ac-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="452ac-121">Requirements</span></span>



| <span data-ttu-id="452ac-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="452ac-122">Requirement</span></span> | <span data-ttu-id="452ac-123">Wert</span><span class="sxs-lookup"><span data-stu-id="452ac-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="452ac-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="452ac-124">Minimum supported client</span></span><br/> | <span data-ttu-id="452ac-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="452ac-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="452ac-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="452ac-126">Minimum supported server</span></span><br/> | <span data-ttu-id="452ac-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="452ac-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="452ac-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="452ac-128">End of client support</span></span><br/>    | <span data-ttu-id="452ac-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="452ac-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="452ac-130">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="452ac-130">End of server support</span></span><br/>    | <span data-ttu-id="452ac-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="452ac-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="452ac-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="452ac-132">Namespace</span></span><br/>                | <span data-ttu-id="452ac-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="452ac-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="452ac-134">MOF</span><span class="sxs-lookup"><span data-stu-id="452ac-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="452ac-135"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="452ac-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="452ac-136">DLL</span><span class="sxs-lookup"><span data-stu-id="452ac-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="452ac-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="452ac-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="452ac-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="452ac-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="452ac-139">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="452ac-139">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

