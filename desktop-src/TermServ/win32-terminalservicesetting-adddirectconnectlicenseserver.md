---
title: Adddirectconnectlicenseserver-Methode der Win32_TerminalServiceSetting-Klasse
description: Adddirectconnectlicenseserver ist nicht mehr verfügbar.
ms.assetid: 7920fd28-0fa3-4f96-bec3-d9e37c97920c
ms.tgt_platform: multiple
keywords:
- Adddirectconnectlicenseserver-Methode Remotedesktopdienste
- Adddirectconnectlicenseserver-Methode Remotedesktopdienste, Win32_TerminalServiceSetting-Klasse
- Win32_TerminalServiceSetting-Klasse Remotedesktopdienste, adddirectconnectlicenseserver-Methode
topic_type:
- apiref
api_name:
- Win32_TerminalServiceSetting.AddDirectConnectLicenseServer
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: be9bba23f5c0bfc69b4c8d7951ab38eac6690b84
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104392161"
---
# <a name="adddirectconnectlicenseserver-method-of-the-win32_terminalservicesetting-class"></a><span data-ttu-id="cfcbc-106">Adddirectconnectlicenseserver-Methode der Win32 \_ terminalservicesetts-Klasse</span><span class="sxs-lookup"><span data-stu-id="cfcbc-106">AddDirectConnectLicenseServer method of the Win32\_TerminalServiceSetting class</span></span>

<span data-ttu-id="cfcbc-107">\[**Adddirectconnectlicenseserver** ist nicht mehr für die Verwendung ab Windows Server 2008 R2 verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="cfcbc-107">\[**AddDirectConnectLicenseServer** is no longer available for use as of Windows Server 2008 R2.\]</span></span>

<span data-ttu-id="cfcbc-108">**Windows Server 2008:** Konfiguriert einen neuen Lizenzserver und fügt den Lizenzserver zur Ermittlung durch Remotedesktop-Sitzungshost (RD-Sitzungshost)-Servern zur Registrierung hinzu.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-108">**Windows Server 2008:** Configures a new license server and adds the license server to the registry for discovery by Remote Desktop Session Host (RD Session Host) servers.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfcbc-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="cfcbc-109">Syntax</span></span>


```mof
uint32 AddDirectConnectLicenseServer(
  [in] string LicenseServerName
);
```



## <a name="parameters"></a><span data-ttu-id="cfcbc-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="cfcbc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfcbc-111">*Licenseservername* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cfcbc-111">*LicenseServerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cfcbc-112">Der Name des hinzu zufügenden Lizenzservers.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-112">Name of the license server to add.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfcbc-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cfcbc-113">Return value</span></span>

<span data-ttu-id="cfcbc-114">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-114">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="cfcbc-115">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="cfcbc-115">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfcbc-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cfcbc-116">Remarks</span></span>

<span data-ttu-id="cfcbc-117">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-117">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cfcbc-118">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-118">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cfcbc-119">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cfcbc-119">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cfcbc-120">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cfcbc-120">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cfcbc-121">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cfcbc-121">Requirements</span></span>



| <span data-ttu-id="cfcbc-122">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cfcbc-122">Requirement</span></span> | <span data-ttu-id="cfcbc-123">Wert</span><span class="sxs-lookup"><span data-stu-id="cfcbc-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cfcbc-124">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cfcbc-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cfcbc-125">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cfcbc-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="cfcbc-126">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cfcbc-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cfcbc-127">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfcbc-127">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cfcbc-128">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="cfcbc-128">End of client support</span></span><br/>    | <span data-ttu-id="cfcbc-129">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="cfcbc-129">None supported</span></span><br/>                                                               |
| <span data-ttu-id="cfcbc-130">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="cfcbc-130">End of server support</span></span><br/>    | <span data-ttu-id="cfcbc-131">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cfcbc-131">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cfcbc-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="cfcbc-132">Namespace</span></span><br/>                | <span data-ttu-id="cfcbc-133">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cfcbc-133">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cfcbc-134">MOF</span><span class="sxs-lookup"><span data-stu-id="cfcbc-134">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cfcbc-135"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cfcbc-135"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cfcbc-136">DLL</span><span class="sxs-lookup"><span data-stu-id="cfcbc-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cfcbc-137"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cfcbc-137"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfcbc-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cfcbc-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfcbc-139">**Win32 \_ terminalservicesetts**</span><span class="sxs-lookup"><span data-stu-id="cfcbc-139">**Win32\_TerminalServiceSetting**</span></span>](win32-terminalservicesetting.md)
</dt> </dl>

 

