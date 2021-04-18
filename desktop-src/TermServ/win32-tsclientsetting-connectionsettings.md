---
title: Connectionsettings-Methode der Win32_TSClientSetting-Klasse
description: Die connectionsettings-Methode legt die Sitzungs Einstellungen fest, die für die Verbindung und den Anmeldeprozess gelten.
ms.assetid: 603807fe-f341-4358-a3b0-0300785cbdb1
ms.tgt_platform: multiple
keywords:
- Connectionsettings-Methode Remotedesktopdienste
- Connectionsettings-Methode Remotedesktopdienste, Win32_TSClientSetting-Klasse
- Win32_TSClientSetting-Klasse Remotedesktopdienste, connectionsettings-Methode
topic_type:
- apiref
api_name:
- Win32_TSClientSetting.ConnectionSettings
api_location:
- TSCfgWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec255f00656684751b750e92d7a3df8290e3573e
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517675"
---
# <a name="connectionsettings-method-of-the-win32_tsclientsetting-class"></a><span data-ttu-id="cf67f-106">Connectionsettings-Methode der Win32- \_ Klasse "tsclientsetting"</span><span class="sxs-lookup"><span data-stu-id="cf67f-106">ConnectionSettings method of the Win32\_TSClientSetting class</span></span>

<span data-ttu-id="cf67f-107">Die **connectionsettings** -Methode legt die Sitzungs Einstellungen fest, die für die Verbindung und den Anmeldeprozess gelten.</span><span class="sxs-lookup"><span data-stu-id="cf67f-107">The **ConnectionSettings** method sets the session settings that apply to the connection and logon process.</span></span>

## <a name="syntax"></a><span data-ttu-id="cf67f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf67f-108">Syntax</span></span>


```mof
uint32 ConnectionSettings(
  [in] uint32 ConnectClientDrivesAtLogon,
  [in] uint32 ConnectPrinterAtLogon,
  [in] uint32 DefaultToClientPrinter
);
```



## <a name="parameters"></a><span data-ttu-id="cf67f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="cf67f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cf67f-110">*Connectclientdrivesatlogon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf67f-110">*ConnectClientDrivesAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf67f-111">Flag zum Aktivieren oder Deaktivieren der **connectclientdrivesatlogon** -Eigenschaft, die angibt, ob die Laufwerke des Clients während des Anmeldevorgangs automatisch verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="cf67f-111">Flag enabling or disabling the **ConnectClientDrivesAtLogon** property which specifies whether the client's drives are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="cf67f-112"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="cf67f-112"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="cf67f-113">Die Laufwerke des Clients werden nicht automatisch verbunden.</span><span class="sxs-lookup"><span data-stu-id="cf67f-113">The client's drives are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="cf67f-114"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="cf67f-114"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="cf67f-115">Die Laufwerke des Clients werden automatisch verbunden.</span><span class="sxs-lookup"><span data-stu-id="cf67f-115">The client's drives are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cf67f-116">*Connectprinteratlogon* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf67f-116">*ConnectPrinterAtLogon* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf67f-117">Flag zum Aktivieren oder Deaktivieren der **connectprinteratlogon** -Eigenschaft, die angibt, ob alle zugeordneten lokalen Client Drucker während des Anmeldevorgangs automatisch verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="cf67f-117">Flag enabling or disabling the **ConnectPrinterAtLogon** property, which specifies whether all mapped local client printers are automatically connected during the logon procedure.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="cf67f-118"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="cf67f-118"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="cf67f-119">Alle zugeordneten lokalen Drucker sind nicht automatisch verbunden.</span><span class="sxs-lookup"><span data-stu-id="cf67f-119">All mapped local printers are not automatically connected.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="cf67f-120"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="cf67f-120"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="cf67f-121">Alle zugeordneten lokalen Drucker werden automatisch verbunden.</span><span class="sxs-lookup"><span data-stu-id="cf67f-121">All mapped local printers are automatically connected.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="cf67f-122">*Defaultdeclientprinter* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="cf67f-122">*DefaultToClientPrinter* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="cf67f-123">Flag zum Aktivieren oder Deaktivieren der **defaultdeclientprinter** -Eigenschaft, die angibt, ob Druckaufträge automatisch an den lokalen Drucker des Clients gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="cf67f-123">Flag enabling or disabling the **DefaultToClientPrinter** property which specifies whether print jobs are automatically sent to the client's local printer.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="cf67f-124"><span id="0"></span>**1,0**</span><span class="sxs-lookup"><span data-stu-id="cf67f-124"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="cf67f-125">Druckaufträge werden nicht automatisch gesendet.</span><span class="sxs-lookup"><span data-stu-id="cf67f-125">Print jobs are not automatically sent.</span></span>

</dd> <dt>

<span id="1"></span>

<span data-ttu-id="cf67f-126"><span id="1"></span>**1**</span><span class="sxs-lookup"><span data-stu-id="cf67f-126"><span id="1"></span>**1**</span></span>


</dt> <dd>

<span data-ttu-id="cf67f-127">Druckaufträge werden automatisch gesendet.</span><span class="sxs-lookup"><span data-stu-id="cf67f-127">Print jobs are automatically sent.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cf67f-128">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cf67f-128">Return value</span></span>

<span data-ttu-id="cf67f-129">Gibt bei Erfolg 0 zurück, andernfalls wird ein WMI-Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="cf67f-129">Returns 0 on success, otherwise returns a WMI error code.</span></span> <span data-ttu-id="cf67f-130">Eine Liste dieser Werte finden Sie unter [Remotedesktopdienste Fehler Codes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md) .</span><span class="sxs-lookup"><span data-stu-id="cf67f-130">Refer to [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md) for a list of these values.</span></span> <span data-ttu-id="cf67f-131">Die-Methode gibt einen Fehler zurück, wenn die Verbindungseinstellungen des Benutzers vom Server überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="cf67f-131">The method returns an error if the user's connection settings are overridden by the server.</span></span>

## <a name="remarks"></a><span data-ttu-id="cf67f-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf67f-132">Remarks</span></span>

<span data-ttu-id="cf67f-133">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="cf67f-133">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="cf67f-134">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="cf67f-134">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="cf67f-135">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="cf67f-135">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="cf67f-136">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="cf67f-136">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="cf67f-137">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cf67f-137">Requirements</span></span>



| <span data-ttu-id="cf67f-138">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cf67f-138">Requirement</span></span> | <span data-ttu-id="cf67f-139">Wert</span><span class="sxs-lookup"><span data-stu-id="cf67f-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cf67f-140">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="cf67f-140">Minimum supported client</span></span><br/> | <span data-ttu-id="cf67f-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cf67f-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cf67f-142">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="cf67f-142">Minimum supported server</span></span><br/> | <span data-ttu-id="cf67f-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cf67f-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cf67f-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="cf67f-144">Namespace</span></span><br/>                | <span data-ttu-id="cf67f-145">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="cf67f-145">Root\\CIMv2\\TerminalServices</span></span><br/>                                                |
| <span data-ttu-id="cf67f-146">MOF</span><span class="sxs-lookup"><span data-stu-id="cf67f-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cf67f-147"><dt>Tscsgwmi. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="cf67f-147"><dt>TSCfgWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="cf67f-148">DLL</span><span class="sxs-lookup"><span data-stu-id="cf67f-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf67f-149"><dt>TSCfgWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf67f-149"><dt>TSCfgWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf67f-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf67f-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf67f-151">**Win32- \_ tsclientsetting**</span><span class="sxs-lookup"><span data-stu-id="cf67f-151">**Win32\_TSClientSetting**</span></span>](win32-tsclientsetting.md)
</dt> </dl>

 

