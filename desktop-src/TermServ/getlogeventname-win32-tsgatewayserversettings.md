---
title: Getlogeventname-Methode der Win32_TSGatewayServerSettings-Klasse
description: Gibt den Protokoll Ereignis Namen für den angegebenen Protokoll Ereignis Index zurück.
ms.assetid: ca31ef8e-ab84-4132-a6d2-232b1e69230a
ms.tgt_platform: multiple
keywords:
- Getlogeventname-Methode Remotedesktopdienste
- Getlogeventname-Methode Remotedesktopdienste, Win32_TSGatewayServerSettings-Klasse
- Win32_TSGatewayServerSettings-Klasse Remotedesktopdienste, getlogeventname-Methode
topic_type:
- apiref
api_name:
- Win32_TSGatewayServerSettings.GetLogEventName
api_location:
- AagWmi.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e3e9c608b7a12d3de48d75ecd5651df94d0267fc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106338746"
---
# <a name="getlogeventname-method-of-the-win32_tsgatewayserversettings-class"></a><span data-ttu-id="d4c1a-106">Getlogeventname-Methode der Win32- \_ Klasse "tgatewayserversettings"</span><span class="sxs-lookup"><span data-stu-id="d4c1a-106">GetLogEventName method of the Win32\_TSGatewayServerSettings class</span></span>

<span data-ttu-id="d4c1a-107">Gibt den Protokoll Ereignis Namen für den angegebenen Protokoll Ereignis Index zurück.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-107">Returns the log event name for the specified log event index.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4c1a-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="d4c1a-108">Syntax</span></span>


```mof
uint32 GetLogEventName(
  [in]  uint32 EventIndex,
  [out] string EventName
);
```



## <a name="parameters"></a><span data-ttu-id="d4c1a-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d4c1a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d4c1a-110">*Eventindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="d4c1a-110">*EventIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1a-111">Der Index des Protokoll Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-111">Index of the log event.</span></span> <span data-ttu-id="d4c1a-112">Der Wert muss zwischen 0 (null) und dem Wert der **maxlogevents** -Eigenschaft liegen.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-112">The value must be between zero and the value of the **MaxLogEvents** property.</span></span>

</dd> <dt>

<span data-ttu-id="d4c1a-113">*EventName* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="d4c1a-113">*EventName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d4c1a-114">Der Name des angegebenen Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-114">Name of the specified event.</span></span> <span data-ttu-id="d4c1a-115">In der folgenden Liste werden die möglichen Werte angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-115">The following list displays the possible values.</span></span>

<dt>

<span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>

<span data-ttu-id="d4c1a-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**Logchanneldisconnect**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-116"><span id="LogChannelDisconnect"></span><span id="logchanneldisconnect"></span><span id="LOGCHANNELDISCONNECT"></span>**LogChannelDisconnect**</span></span>


</dt> <dd>

<span data-ttu-id="d4c1a-117">Der Benutzer hat die Verbindungen mit der Ressource erfolgreich getrennt.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-117">User successfully disconnected from the resource.</span></span>

</dd> <dt>

<span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>

<span data-ttu-id="d4c1a-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**Logfailurechannelconnect**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-118"><span id="LogFailureChannelConnect"></span><span id="logfailurechannelconnect"></span><span id="LOGFAILURECHANNELCONNECT"></span>**LogFailureChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="d4c1a-119">Der Benutzer konnte keine Verbindung mit der Ressource herstellen.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-119">User failed to connect to the resource.</span></span>

</dd> <dt>

<span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="d4c1a-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**Logfailureconnectionauthorizationcheck**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-120"><span id="LogFailureConnectionAuthorizationCheck"></span><span id="logfailureconnectionauthorizationcheck"></span><span id="LOGFAILURECONNECTIONAUTHORIZATIONCHECK"></span>**LogFailureConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="d4c1a-121">Fehler bei der Verbindungs Autorisierung des Benutzers</span><span class="sxs-lookup"><span data-stu-id="d4c1a-121">User failed connection authorization.</span></span>

</dd> <dt>

<span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="d4c1a-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**Logfailureresourceauthorizationcheck**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-122"><span id="LogFailureResourceAuthorizationCheck"></span><span id="logfailureresourceauthorizationcheck"></span><span id="LOGFAILURERESOURCEAUTHORIZATIONCHECK"></span>**LogFailureResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="d4c1a-123">Fehler beim Autorisieren der Ressource.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-123">User failed resource authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>

<span data-ttu-id="d4c1a-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**Logsuccess-channelconnect**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-124"><span id="LogSuccessfulChannelConnect"></span><span id="logsuccessfulchannelconnect"></span><span id="LOGSUCCESSFULCHANNELCONNECT"></span>**LogSuccessfulChannelConnect**</span></span>


</dt> <dd>

<span data-ttu-id="d4c1a-125">Der Benutzer hat erfolgreich eine Verbindung mit der Ressource hergestellt.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-125">User successfully connected to the resource.</span></span>

</dd> <dt>

<span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>

<span data-ttu-id="d4c1a-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**Logsuccess fulconnectionauthorizationcheck**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-126"><span id="LogSuccessfulConnectionAuthorizationCheck"></span><span id="logsuccessfulconnectionauthorizationcheck"></span><span id="LOGSUCCESSFULCONNECTIONAUTHORIZATIONCHECK"></span>**LogSuccessfulConnectionAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="d4c1a-127">Der Benutzer hat die Verbindungs Autorisierung erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-127">User successfully passed connection authorization.</span></span>

</dd> <dt>

<span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>

<span data-ttu-id="d4c1a-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**Logsuccess fulresourceauthorizationcheck**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-128"><span id="LogSuccessfulResourceAuthorizationCheck"></span><span id="logsuccessfulresourceauthorizationcheck"></span><span id="LOGSUCCESSFULRESOURCEAUTHORIZATIONCHECK"></span>**LogSuccessfulResourceAuthorizationCheck**</span></span>


</dt> <dd>

<span data-ttu-id="d4c1a-129">Der Benutzer hat die Ressourcen Autorisierung erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-129">User successfully passed resource authorization.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d4c1a-130">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d4c1a-130">Return value</span></span>

<span data-ttu-id="d4c1a-131">Wenn die Methode erfolgreich ist, gibt Sie 0 (null) zurück.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-131">If the method succeeds, it returns zero.</span></span> <span data-ttu-id="d4c1a-132">Wenn die Methode nicht erfolgreich ist, wird ein Wert ungleich 0 (null) zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-132">If the method is unsuccessful, it returns a nonzero value.</span></span> <span data-ttu-id="d4c1a-133">Eine Liste der Fehlercodes finden Sie unter [Remotedesktopdienste Fehlercodes des WMI-Anbieters](terminal-services-wmi-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="d4c1a-133">For a list of error codes, see [Remote Desktop Services WMI Provider Error Codes](terminal-services-wmi-provider-error-codes.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="d4c1a-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4c1a-134">Remarks</span></span>

<span data-ttu-id="d4c1a-135">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-135">You must be a member of the Administrators group to call this method.</span></span>

<span data-ttu-id="d4c1a-136">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-136">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="d4c1a-137">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-137">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="d4c1a-138">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="d4c1a-138">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="d4c1a-139">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="d4c1a-139">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="d4c1a-140">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d4c1a-140">Requirements</span></span>



| <span data-ttu-id="d4c1a-141">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d4c1a-141">Requirement</span></span> | <span data-ttu-id="d4c1a-142">Wert</span><span class="sxs-lookup"><span data-stu-id="d4c1a-142">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d4c1a-143">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d4c1a-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d4c1a-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="d4c1a-144">None supported</span></span><br/>                                                                |
| <span data-ttu-id="d4c1a-145">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d4c1a-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d4c1a-146">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4c1a-146">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="d4c1a-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4c1a-147">Namespace</span></span><br/>                | <span data-ttu-id="d4c1a-148">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="d4c1a-148">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="d4c1a-149">MOF</span><span class="sxs-lookup"><span data-stu-id="d4c1a-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d4c1a-150"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="d4c1a-150"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="d4c1a-151">DLL</span><span class="sxs-lookup"><span data-stu-id="d4c1a-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d4c1a-152"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4c1a-152"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="d4c1a-153">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4c1a-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d4c1a-154">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-154">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="d4c1a-155">**Enablelogevent**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-155">**EnableLogEvent**</span></span>](enablelogevent-win32-tsgatewayserversettings.md)
</dt> <dt>

[<span data-ttu-id="d4c1a-156">**Islogeventaktivierte**</span><span class="sxs-lookup"><span data-stu-id="d4c1a-156">**IsLogEventEnabled**</span></span>](islogeventenabled-win32-tsgatewayserversettings.md)
</dt> </dl>

 

