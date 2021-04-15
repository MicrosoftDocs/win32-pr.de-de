---
title: Win32_TSGatewayRADIUSServer-Klasse
description: Beschreibt einen Remote Authentication Dial-in User Service Server (RADIUS), der über eine Reihe von Remotedesktopdienste Verbindungs Autorisierungs Richtlinien (RD \ 160; Caps).
ms.assetid: 40254354-f446-4e17-b7ec-649c98dd94f9
ms.tgt_platform: multiple
keywords:
- Win32_TSGatewayRADIUSServer-Klasse Remotedesktopdienste
- Win32_TSGatewayRADIUSServer Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_TSGatewayRADIUSServer
- Win32_TSGatewayRADIUSServer.Name
- Win32_TSGatewayRADIUSServer.Priority
- Win32_TSGatewayRADIUSServer.SharedSecret
api_location:
- AagWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4157d89dc942a1c2f8ff7d778f9f8048971902ba
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104476386"
---
# <a name="win32_tsgatewayradiusserver-class"></a><span data-ttu-id="3878e-105">Win32-Klasse "t- \_ gatewayradiusserver"</span><span class="sxs-lookup"><span data-stu-id="3878e-105">Win32\_TSGatewayRADIUSServer class</span></span>

<span data-ttu-id="3878e-106">Beschreibt einen Remote Authentication Dial-in User Service Server (RADIUS), der über eine Reihe von Remotedesktopdienste Verbindungs Autorisierungs Richtlinien (RD-CAPs) verfügt.</span><span class="sxs-lookup"><span data-stu-id="3878e-106">Describes a Remote Authentication Dial-In User Service (RADIUS) server, which has a set of Remote Desktop Services connection authorization policies (RD CAPs).</span></span>

<span data-ttu-id="3878e-107">RADIUS ist ein Industriestandard Protokoll, das zum Übertragen von Authentifizierung, Autorisierung und Konfigurationsinformationen zwischen einem Server Computer und einem authentifizier enden Server, der als RADIUS-Server bezeichnet wird, mit einer Datenbank verwendet wird, in der Benutzerinformationen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="3878e-107">RADIUS is an industry-standard protocol that is used to transmit authentication, authorization, and configuration information between a server computer and an authenticating server, called a RADIUS server, with a database that stores user information.</span></span> <span data-ttu-id="3878e-108">Weitere Informationen finden Sie unter [RADIUS-Protokoll](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span><span class="sxs-lookup"><span data-stu-id="3878e-108">For more information, see [RADIUS Protocol](/previous-versions/windows/it-pro/windows-server-2003/cc781821(v=ws.10)).</span></span>

## <a name="syntax"></a><span data-ttu-id="3878e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3878e-109">Syntax</span></span>

``` syntax
[dynamic, provider("AAGProvider"), AMENDMENT]
class Win32_TSGatewayRADIUSServer
{
  string Name;
  uint32 Priority;
  string SharedSecret;
};
```

## <a name="members"></a><span data-ttu-id="3878e-110">Member</span><span class="sxs-lookup"><span data-stu-id="3878e-110">Members</span></span>

<span data-ttu-id="3878e-111">Die Win32-Klasse " **\_ zgatewayradiusserver** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3878e-111">The **Win32\_TSGatewayRADIUSServer** class has these types of members:</span></span>

-   [<span data-ttu-id="3878e-112">Methoden</span><span class="sxs-lookup"><span data-stu-id="3878e-112">Methods</span></span>](#methods)
-   [<span data-ttu-id="3878e-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3878e-113">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="3878e-114">Methoden</span><span class="sxs-lookup"><span data-stu-id="3878e-114">Methods</span></span>

<span data-ttu-id="3878e-115">Die Win32-Klasse " **\_ zgatewayradiusserver** " verfügt über diese Methoden.</span><span class="sxs-lookup"><span data-stu-id="3878e-115">The **Win32\_TSGatewayRADIUSServer** class has these methods.</span></span>



| <span data-ttu-id="3878e-116">Methode</span><span class="sxs-lookup"><span data-stu-id="3878e-116">Method</span></span>                                                                 | <span data-ttu-id="3878e-117">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="3878e-117">Description</span></span>                                                                  |
|:-----------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| [<span data-ttu-id="3878e-118">**Eren**</span><span class="sxs-lookup"><span data-stu-id="3878e-118">**Add**</span></span>](win32-tsgatewayradiusserver-add.md)                         | <span data-ttu-id="3878e-119">Fügt einen neuen RADIUS-Server hinzu.</span><span class="sxs-lookup"><span data-stu-id="3878e-119">Adds a new RADIUS server.</span></span><br/>                                         |
| [<span data-ttu-id="3878e-120">**Nach unten**</span><span class="sxs-lookup"><span data-stu-id="3878e-120">**MoveDown**</span></span>](movedown-win32-tsgatewayradiusserver.md)               | <span data-ttu-id="3878e-121">Verschiebt diesen RADIUS-Server in der Prioritäts Reihenfolge um eine Position nach unten.</span><span class="sxs-lookup"><span data-stu-id="3878e-121">Moves this RADIUS server one position down in the priority order.</span></span><br/> |
| [<span data-ttu-id="3878e-122">**MoveUp**</span><span class="sxs-lookup"><span data-stu-id="3878e-122">**MoveUp**</span></span>](moveup-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="3878e-123">Verschiebt diesen RADIUS-Server in der Prioritäts Reihenfolge um eine Position nach oben.</span><span class="sxs-lookup"><span data-stu-id="3878e-123">Moves this RADIUS server one position up in the priority order.</span></span><br/>   |
| [<span data-ttu-id="3878e-124">**Aufgeh**</span><span class="sxs-lookup"><span data-stu-id="3878e-124">**Remove**</span></span>](win32-tsgatewayradiusserver-remove.md)                   | <span data-ttu-id="3878e-125">Entfernt den aktuellen RADIUS-Server.</span><span class="sxs-lookup"><span data-stu-id="3878e-125">Removes the current RADIUS server.</span></span><br/>                                |
| [<span data-ttu-id="3878e-126">**SetName**</span><span class="sxs-lookup"><span data-stu-id="3878e-126">**SetName**</span></span>](setname-win32-tsgatewayradiusserver.md)                 | <span data-ttu-id="3878e-127">Legt die **Name** -Eigenschaft für diesen RADIUS-Server fest.</span><span class="sxs-lookup"><span data-stu-id="3878e-127">Sets the **Name** property for this RADIUS server.</span></span><br/>                |
| [<span data-ttu-id="3878e-128">**Setsharedsecret**</span><span class="sxs-lookup"><span data-stu-id="3878e-128">**SetSharedSecret**</span></span>](setsharedsecret-win32-tsgatewayradiusserver.md) | <span data-ttu-id="3878e-129">Legt die **sharedsecret** -Eigenschaft für diesen RADIUS-Server fest.</span><span class="sxs-lookup"><span data-stu-id="3878e-129">Sets the **SharedSecret** property for this RADIUS server.</span></span><br/>        |
| [<span data-ttu-id="3878e-130">**Aktualisieren**</span><span class="sxs-lookup"><span data-stu-id="3878e-130">**Update**</span></span>](update-win32-tsgatewayradiusserver.md)                   | <span data-ttu-id="3878e-131">Aktualisiert den aktuellen RADIUS-Server.</span><span class="sxs-lookup"><span data-stu-id="3878e-131">Updates the current RADIUS server.</span></span><br/>                                |



 

### <a name="properties"></a><span data-ttu-id="3878e-132">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3878e-132">Properties</span></span>

<span data-ttu-id="3878e-133">Die Win32-Klasse "t- **\_ gatewayradiusserver** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3878e-133">The **Win32\_TSGatewayRADIUSServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3878e-134">**Name**</span><span class="sxs-lookup"><span data-stu-id="3878e-134">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3878e-135">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3878e-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3878e-136">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3878e-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3878e-137">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3878e-137">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3878e-138">Der Name des RADIUS-Servers.</span><span class="sxs-lookup"><span data-stu-id="3878e-138">Name of the RADIUS server.</span></span> <span data-ttu-id="3878e-139">Diese Eigenschaft kann mit der [**SetName**](setname-win32-tsgatewayradiusserver.md) -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3878e-139">This property can be changed with the [**SetName**](setname-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="3878e-140">**Priority**</span><span class="sxs-lookup"><span data-stu-id="3878e-140">**Priority**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3878e-141">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3878e-141">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3878e-142">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3878e-142">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3878e-143">Priorität des RADIUS-Servers.</span><span class="sxs-lookup"><span data-stu-id="3878e-143">Priority of the RADIUS server.</span></span> <span data-ttu-id="3878e-144">Der RD-Gateway Server sucht nach RD-CAPs auf RADIUS-Servern basierend auf der Priorität.</span><span class="sxs-lookup"><span data-stu-id="3878e-144">The RD Gateway server looks for RD CAPs on RADIUS servers based on the priority.</span></span> <span data-ttu-id="3878e-145">Diese Eigenschaft kann mit den Methoden [**moveUp**](moveup-win32-tsgatewayradiusserver.md), [**muvedown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md)und [**Remove**](win32-tsgatewayradiusserver-remove.md) geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3878e-145">This property can be changed with the [**MoveUp**](moveup-win32-tsgatewayradiusserver.md), [**MoveDown**](movedown-win32-tsgatewayradiusserver.md), [**Add**](win32-tsgatewayradiusserver-add.md), and [**Remove**](win32-tsgatewayradiusserver-remove.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="3878e-146">**SharedSecret**</span><span class="sxs-lookup"><span data-stu-id="3878e-146">**SharedSecret**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3878e-147">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3878e-147">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3878e-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3878e-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3878e-149">Gemeinsamer geheimer Schlüssel für den RADIUS-Server.</span><span class="sxs-lookup"><span data-stu-id="3878e-149">Shared secret for the RADIUS server.</span></span> <span data-ttu-id="3878e-150">Diese Eigenschaft kann mit der [**setsharedsecret**](setsharedsecret-win32-tsgatewayradiusserver.md) -Methode geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3878e-150">This property can be changed with the [**SetSharedSecret**](setsharedsecret-win32-tsgatewayradiusserver.md) method.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3878e-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3878e-151">Remarks</span></span>

<span data-ttu-id="3878e-152">Sie müssen Mitglied der Gruppe "Administratoren" sein, um diese Klasse verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="3878e-152">You must be a member of the Administrators group to use this class.</span></span>

<span data-ttu-id="3878e-153">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3878e-153">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3878e-154">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="3878e-154">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3878e-155">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3878e-155">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3878e-156">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3878e-156">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3878e-157">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3878e-157">Requirements</span></span>



| <span data-ttu-id="3878e-158">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3878e-158">Requirement</span></span> | <span data-ttu-id="3878e-159">Wert</span><span class="sxs-lookup"><span data-stu-id="3878e-159">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3878e-160">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3878e-160">Minimum supported client</span></span><br/> | <span data-ttu-id="3878e-161">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3878e-161">None supported</span></span><br/>                                                                |
| <span data-ttu-id="3878e-162">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3878e-162">Minimum supported server</span></span><br/> | <span data-ttu-id="3878e-163">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3878e-163">Windows Server 2008</span></span><br/>                                                           |
| <span data-ttu-id="3878e-164">Namespace</span><span class="sxs-lookup"><span data-stu-id="3878e-164">Namespace</span></span><br/>                | <span data-ttu-id="3878e-165">Root \\ CIMv2 \\ TerminalServices</span><span class="sxs-lookup"><span data-stu-id="3878e-165">Root\\CIMv2\\TerminalServices</span></span><br/>                                                 |
| <span data-ttu-id="3878e-166">MOF</span><span class="sxs-lookup"><span data-stu-id="3878e-166">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3878e-167"><dt>"T-Gateway. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="3878e-167"><dt>TSGateway.mof</dt></span></span> </dl> |
| <span data-ttu-id="3878e-168">DLL</span><span class="sxs-lookup"><span data-stu-id="3878e-168">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3878e-169"><dt>AagWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3878e-169"><dt>AagWmi.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="3878e-170">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3878e-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3878e-171">**Win32-"- \_ gatewayconnection"**</span><span class="sxs-lookup"><span data-stu-id="3878e-171">**Win32\_TSGatewayConnection**</span></span>](win32-tsgatewayconnection.md)
</dt> <dt>

[<span data-ttu-id="3878e-172">**Win32- \_ faigatewayconnectionauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="3878e-172">**Win32\_TSGatewayConnectionAuthorizationPolicy**</span></span>](win32-tsgatewayconnectionauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="3878e-173">**Win32-"t- \_ gatewayloadbalancer"**</span><span class="sxs-lookup"><span data-stu-id="3878e-173">**Win32\_TSGatewayLoadBalancer**</span></span>](win32-tsgatewayloadbalancer.md)
</dt> <dt>

[<span data-ttu-id="3878e-174">**Win32- \_ faigatewayresourceauthorizationpolicy**</span><span class="sxs-lookup"><span data-stu-id="3878e-174">**Win32\_TSGatewayResourceAuthorizationPolicy**</span></span>](win32-tsgatewayresourceauthorizationpolicy.md)
</dt> <dt>

[<span data-ttu-id="3878e-175">**Win32-Datei " \_ zgatewayresourcegroup"**</span><span class="sxs-lookup"><span data-stu-id="3878e-175">**Win32\_TSGatewayResourceGroup**</span></span>](win32-tsgatewayresourcegroup.md)
</dt> <dt>

[<span data-ttu-id="3878e-176">**Win32-Datei- \_ gatewayserversettings**</span><span class="sxs-lookup"><span data-stu-id="3878e-176">**Win32\_TSGatewayServerSettings**</span></span>](win32-tsgatewayserversettings.md)
</dt> </dl>

 

