---
title: Enablelogevent-Methode der Win32_TSGatewayServerSettings-Klasse
description: Aktiviert oder deaktiviert die Protokollierung des angegebenen Ereignis Typs.
ms.assetid: e901ef51-2ae2-4123-902a-ac359f3eb959
ms.tgt_platform: multiple
keywords:
- Enablelogevent-Methode Remotedesktopdienste
- Enablelogevent-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, enablelogevent-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.EnableLogEvent
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e72f7cb8567c7f2d5c3ca79d241013e2bd64a5e2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104479317"
---
# <a name="enablelogevent-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="b57ff-106">Enablelogevent-Methode der Win32-Klasse "t- \_ gatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="b57ff-106">EnableLogEvent method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="b57ff-107">Aktiviert oder deaktiviert die Protokollierung des angegebenen Ereignis Typs.</span><span class="sxs-lookup"><span data-stu-id="b57ff-107">Enables or disables logging of the specified event type.</span></span>

## <a name="syntax"></a><span data-ttu-id="b57ff-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="b57ff-108">Syntax</span></span>


```mof
uint32 EnableLogEvent(
  [in] string  EventName,
  [in] boolean Enabled
);
```



## <a name="parameters"></a><span data-ttu-id="b57ff-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="b57ff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b57ff-110">*EventName* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b57ff-110">*EventName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b57ff-111">Name der Veranstaltung.</span><span class="sxs-lookup"><span data-stu-id="b57ff-111">Name of the event.</span></span> <span data-ttu-id="b57ff-112">Dieser Wert sollte mithilfe der [**getlogeventname**](getlogeventname-win32-tsgatewayserversettings.md) -Methode abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b57ff-112">This value should be retrieved by using the [**GetLogEventName**](getlogeventname-win32-tsgatewayserversettings.md) method.</span></span>

<dt>

<span data-ttu-id="b57ff-113">Logchanneldisconnect</span><span class="sxs-lookup"><span data-stu-id="b57ff-113">LogChannelDisconnect</span></span>
</dt> <dd>

<span data-ttu-id="b57ff-114">Der Benutzer hat die Verbindungen mit der Ressource erfolgreich getrennt.</span><span class="sxs-lookup"><span data-stu-id="b57ff-114">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span data-ttu-id="b57ff-115">Logfailedchannelconnect</span><span class="sxs-lookup"><span data-stu-id="b57ff-115">LogFailedChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="b57ff-116">Der Benutzer konnte keine Verbindung mit der Ressource herstellen.</span><span class="sxs-lookup"><span data-stu-id="b57ff-116">User failed to connect to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="b57ff-117">Logfailurumetworkaccesscheck</span><span class="sxs-lookup"><span data-stu-id="b57ff-117">LogFailureNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="b57ff-118">Fehler bei der Verbindungs Autorisierung des Benutzers</span><span class="sxs-lookup"><span data-stu-id="b57ff-118">User failed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="b57ff-119">Logfailureresourceaccesscheck</span><span class="sxs-lookup"><span data-stu-id="b57ff-119">LogFailureResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="b57ff-120">Fehler beim Autorisieren der Ressource.</span><span class="sxs-lookup"><span data-stu-id="b57ff-120">User failed resource authorization.</span></span>

</dd> <dt>

<span data-ttu-id="b57ff-121">Logerfolgreicher schannelconnect</span><span class="sxs-lookup"><span data-stu-id="b57ff-121">LogSuccessChannelConnect</span></span>
</dt> <dd>

<span data-ttu-id="b57ff-122">Der Benutzer hat erfolgreich eine Verbindung mit der Ressource hergestellt.</span><span class="sxs-lookup"><span data-stu-id="b57ff-122">User successfully connected to the resource.</span></span>

</dd> <dt>

<span data-ttu-id="b57ff-123">Logsuccess-networkaccesscheck</span><span class="sxs-lookup"><span data-stu-id="b57ff-123">LogSuccessfulNetworkAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="b57ff-124">Der Benutzer hat die Verbindungs Autorisierung erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b57ff-124">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span data-ttu-id="b57ff-125">Logsuccess fulresourceaccesscheck</span><span class="sxs-lookup"><span data-stu-id="b57ff-125">LogSuccessfulResourceAccessCheck</span></span>
</dt> <dd>

<span data-ttu-id="b57ff-126">Der Benutzer hat die Ressourcen Autorisierung erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="b57ff-126">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="b57ff-127">*Aktiviert* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="b57ff-127">*Enabled* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b57ff-128">Gibt an, ob das Ereignis aktiviert oder deaktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="b57ff-128">Specifies whether the event should be enabled or disabled.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b57ff-129">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b57ff-129">Return value</span></span>

<span data-ttu-id="b57ff-130">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="b57ff-130">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="b57ff-131">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b57ff-131">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="b57ff-132">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="b57ff-132">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="b57ff-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b57ff-133">Remarks</span></span>

<span data-ttu-id="b57ff-134">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="b57ff-134">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="b57ff-135">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="b57ff-135">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="b57ff-136">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="b57ff-136">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="b57ff-137">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="b57ff-137">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="b57ff-138">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="b57ff-138">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="b57ff-139">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b57ff-139">Requirements</span></span>



| <span data-ttu-id="b57ff-140">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b57ff-140">Requirement</span></span> | <span data-ttu-id="b57ff-141">Wert</span><span class="sxs-lookup"><span data-stu-id="b57ff-141">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b57ff-142">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b57ff-142">Minimum supported client</span></span><br/> | <span data-ttu-id="b57ff-143">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="b57ff-143">None supported</span></span><br/>                                                                |
| <span data-ttu-id="b57ff-144">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b57ff-144">Minimum supported server</span></span><br/> | <span data-ttu-id="b57ff-145">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b57ff-145">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="b57ff-146">Namespace</span><span class="sxs-lookup"><span data-stu-id="b57ff-146">Namespace</span></span><br/>                | <span data-ttu-id="b57ff-147">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="b57ff-147">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="b57ff-148">MOF</span><span class="sxs-lookup"><span data-stu-id="b57ff-148">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b57ff-149"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="b57ff-149"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="b57ff-150">DLL</span><span class="sxs-lookup"><span data-stu-id="b57ff-150">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b57ff-151"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b57ff-151"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="b57ff-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b57ff-152">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b57ff-153">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="b57ff-153">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="b57ff-154">**Getlogeventname**</span><span class="sxs-lookup"><span data-stu-id="b57ff-154">**GetLogEventName**</span></span>](getlogeventname-win32-tsgatewayserversettings.md)
</dt> </dl>

 

