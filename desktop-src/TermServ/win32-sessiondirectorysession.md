---
title: Win32_SessionDirectorySession-Klasse
description: Stellt Eigenschaften zum Anzeigen der Eigenschaften einer Remotedesktopverbindung Broker-Sitzung (RD-Verbindungsbroker) bereit.
ms.assetid: 34b5a898-3952-493c-ba62-dd0d298b0600
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectorySession-Klasse Remotedesktopdienste
- Win32_SessionDirectorySession Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionDirectorySession
- Win32_SessionDirectorySession.ServerName
- Win32_SessionDirectorySession.SessionID
- Win32_SessionDirectorySession.UserName
- Win32_SessionDirectorySession.DomainName
- Win32_SessionDirectorySession.ServerIPAddress
- Win32_SessionDirectorySession.TSProtocol
- Win32_SessionDirectorySession.ApplicationType
- Win32_SessionDirectorySession.ResolutionWidth
- Win32_SessionDirectorySession.ResolutionHeight
- Win32_SessionDirectorySession.ColorDepth
- Win32_SessionDirectorySession.CreateTime
- Win32_SessionDirectorySession.DisconnectTime
- Win32_SessionDirectorySession.SessionState
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fba8fdbdffc764c3bdcc1a8f5bc53aa479f318d4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104391657"
---
# <a name="win32_sessiondirectorysession-class"></a><span data-ttu-id="82f26-105">Win32 \_ sessiondirectorysession-Klasse</span><span class="sxs-lookup"><span data-stu-id="82f26-105">Win32\_SessionDirectorySession class</span></span>

<span data-ttu-id="82f26-106">Stellt Eigenschaften zum Anzeigen der Eigenschaften einer Remotedesktopverbindung Broker-Sitzung (RD-Verbindungsbroker) bereit.</span><span class="sxs-lookup"><span data-stu-id="82f26-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) session.</span></span>

> [!Note]  
> <span data-ttu-id="82f26-107">In Windows Server 2008 R2 wurde der Name des Terminal Dienste-Sitzungs Brokers (TS-Sitzungs Broker) in "RD-Verbindungsbroker" geändert.</span><span class="sxs-lookup"><span data-stu-id="82f26-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="82f26-108">Diese Eigenschaften gelten für alle unterstützten Betriebssysteme, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="82f26-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="82f26-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="82f26-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSESSION_Prov"), AMENDMENT]
class Win32_SessionDirectorySession
{
  string   ServerName;
  uint32   SessionID;
  string   UserName;
  string   DomainName;
  string   ServerIPAddress;
  uint32   TSProtocol;
  string   ApplicationType;
  uint32   ResolutionWidth;
  uint32   ResolutionHeight;
  uint32   ColorDepth;
  DateTime CreateTime;
  DateTime DisconnectTime;
  uint32   SessionState;
};
```

## <a name="members"></a><span data-ttu-id="82f26-110">Member</span><span class="sxs-lookup"><span data-stu-id="82f26-110">Members</span></span>

<span data-ttu-id="82f26-111">Die Win32-Klasse " **\_ sessiondirectorysession** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="82f26-111">The **Win32\_SessionDirectorySession** class has these types of members:</span></span>

-   [<span data-ttu-id="82f26-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82f26-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="82f26-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="82f26-113">Properties</span></span>

<span data-ttu-id="82f26-114">Die Win32-Klasse " **\_ sessiondirectorysession** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="82f26-114">The **Win32\_SessionDirectorySession** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="82f26-115">**ApplicationType**</span><span class="sxs-lookup"><span data-stu-id="82f26-115">**ApplicationType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82f26-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82f26-118">Die Anwendung wurde mit dieser Sitzung gestartet.</span><span class="sxs-lookup"><span data-stu-id="82f26-118">Application started with this session.</span></span> <span data-ttu-id="82f26-119">Dies entspricht der **Start Program** -Eigenschaft von [**imstscsecuredsettings**](imstscsecuredsettings-interface.md).</span><span class="sxs-lookup"><span data-stu-id="82f26-119">This is the same as the **StartProgram** property of [**IMsTscSecuredSettings**](imstscsecuredsettings-interface.md).</span></span>

</dd> <dt>

<span data-ttu-id="82f26-120">**ColorDepth**</span><span class="sxs-lookup"><span data-stu-id="82f26-120">**ColorDepth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-121">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82f26-121">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-122">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82f26-123">Farbtiefe der Sitzung, gemessen in Bits pro Pixel.</span><span class="sxs-lookup"><span data-stu-id="82f26-123">Color depth of the session, measured in bits per pixel.</span></span>

</dd> <dt>

<span data-ttu-id="82f26-124">**CreateTime**</span><span class="sxs-lookup"><span data-stu-id="82f26-124">**CreateTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-125">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="82f26-125">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82f26-127">Datum und Uhrzeit der Erstellung der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="82f26-127">Date and time the session was created.</span></span> <span data-ttu-id="82f26-128">Dieser Wert wird nicht zurückgesetzt, wenn eine Sitzung getrennt und die Verbindung wieder hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="82f26-128">This value is not reset when a session is disconnected and reconnected.</span></span>

</dd> <dt>

<span data-ttu-id="82f26-129">**Disconnecttime**</span><span class="sxs-lookup"><span data-stu-id="82f26-129">**DisconnectTime**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-130">**Datentyp: DateTime**</span><span class="sxs-lookup"><span data-stu-id="82f26-130">Data type: **DateTime**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-131">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82f26-132">Datum und Uhrzeit, zu der die Sitzung getrennt wurde (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="82f26-132">Date and time the session was disconnected (if applicable).</span></span>

</dd> <dt>

<span data-ttu-id="82f26-133">**DomainName**</span><span class="sxs-lookup"><span data-stu-id="82f26-133">**DomainName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-134">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82f26-134">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-135">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-135">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82f26-136">Der Domänen Name des Benutzers, der bei dieser Sitzung angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="82f26-136">Domain name of the user logged on to this session.</span></span>

</dd> <dt>

<span data-ttu-id="82f26-137">**Resolutionheight**</span><span class="sxs-lookup"><span data-stu-id="82f26-137">**ResolutionHeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-138">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82f26-138">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-139">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82f26-140">Höhe der Sitzung in Pixel für diese Sitzung.</span><span class="sxs-lookup"><span data-stu-id="82f26-140">Height of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="82f26-141">**Resolutionwidth**</span><span class="sxs-lookup"><span data-stu-id="82f26-141">**ResolutionWidth**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-142">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82f26-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-143">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-143">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82f26-144">Breite der Sitzung in Pixel für diese Sitzung.</span><span class="sxs-lookup"><span data-stu-id="82f26-144">Width of the session, in pixels, for this session.</span></span>

</dd> <dt>

<span data-ttu-id="82f26-145">**ServerIPAddress**</span><span class="sxs-lookup"><span data-stu-id="82f26-145">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-146">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82f26-146">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-147">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-147">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82f26-148">Die IP-Adresse des RD-Verbindungsbroker Servers für diese Sitzung.</span><span class="sxs-lookup"><span data-stu-id="82f26-148">IP address of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="82f26-149">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="82f26-149">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-150">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82f26-150">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-151">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82f26-152">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="82f26-152">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="82f26-153">Der Name des RD-Verbindungsbroker Servers für diese Sitzung.</span><span class="sxs-lookup"><span data-stu-id="82f26-153">Name of the RD Connection Broker server for this session.</span></span>

</dd> <dt>

<span data-ttu-id="82f26-154">**SessionID**</span><span class="sxs-lookup"><span data-stu-id="82f26-154">**SessionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-155">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82f26-155">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-156">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="82f26-157">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="82f26-157">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="82f26-158">Sitzungs-ID für diese Sitzung.</span><span class="sxs-lookup"><span data-stu-id="82f26-158">Session ID for this session.</span></span>

</dd> <dt>

<span data-ttu-id="82f26-159">**SessionState**</span><span class="sxs-lookup"><span data-stu-id="82f26-159">**SessionState**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-160">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82f26-160">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-161">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-161">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82f26-162">Der Status dieser Sitzung.</span><span class="sxs-lookup"><span data-stu-id="82f26-162">State of this session.</span></span>

<dt>

<span data-ttu-id="82f26-163">0</span><span class="sxs-lookup"><span data-stu-id="82f26-163">0</span></span>
</dt> <dd>

<span data-ttu-id="82f26-164">Die Sitzung ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="82f26-164">The session is active.</span></span>

</dd> <dt>

<span data-ttu-id="82f26-165">1</span><span class="sxs-lookup"><span data-stu-id="82f26-165">1</span></span>
</dt> <dd>

<span data-ttu-id="82f26-166">Die Sitzung wird getrennt.</span><span class="sxs-lookup"><span data-stu-id="82f26-166">The session is disconnected.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="82f26-167">**Tsproycol**</span><span class="sxs-lookup"><span data-stu-id="82f26-167">**TSProtocol**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-168">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="82f26-168">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-169">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82f26-170">Protokoll für diese Sitzung.</span><span class="sxs-lookup"><span data-stu-id="82f26-170">Protocol for this session.</span></span>

<dt>

<span data-ttu-id="82f26-171">0</span><span class="sxs-lookup"><span data-stu-id="82f26-171">0</span></span>
</dt> <dd>

<span data-ttu-id="82f26-172">Diese Sitzung wird in einer physischen Konsole ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="82f26-172">This session is running on a physical console.</span></span>

</dd> <dt>

<span data-ttu-id="82f26-173">1</span><span class="sxs-lookup"><span data-stu-id="82f26-173">1</span></span>
</dt> <dd>

<span data-ttu-id="82f26-174">Für diese Sitzung wird ein proprietäres Protokoll von Drittanbietern verwendet.</span><span class="sxs-lookup"><span data-stu-id="82f26-174">A proprietary third-party protocol is used for this session.</span></span>

</dd> <dt>

<span data-ttu-id="82f26-175">2</span><span class="sxs-lookup"><span data-stu-id="82f26-175">2</span></span>
</dt> <dd>

<span data-ttu-id="82f26-176">Für diese Sitzung wird Remotedesktopprotokoll (RDP) verwendet.</span><span class="sxs-lookup"><span data-stu-id="82f26-176">Remote Desktop Protocol (RDP) is used for this session.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="82f26-177">**UserName**</span><span class="sxs-lookup"><span data-stu-id="82f26-177">**UserName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="82f26-178">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="82f26-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="82f26-179">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="82f26-179">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="82f26-180">Der Benutzername des Benutzers, der bei dieser Sitzung angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="82f26-180">User name of the user logged on to this session.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="82f26-181">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="82f26-181">Remarks</span></span>

<span data-ttu-id="82f26-182">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="82f26-182">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="82f26-183">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="82f26-183">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="82f26-184">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="82f26-184">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="82f26-185">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="82f26-185">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="82f26-186">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="82f26-186">Requirements</span></span>



| <span data-ttu-id="82f26-187">Anforderung</span><span class="sxs-lookup"><span data-stu-id="82f26-187">Requirement</span></span> | <span data-ttu-id="82f26-188">Wert</span><span class="sxs-lookup"><span data-stu-id="82f26-188">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="82f26-189">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="82f26-189">Minimum supported client</span></span><br/> | <span data-ttu-id="82f26-190">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="82f26-190">None supported</span></span><br/>                                                              |
| <span data-ttu-id="82f26-191">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="82f26-191">Minimum supported server</span></span><br/> | <span data-ttu-id="82f26-192">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="82f26-192">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="82f26-193">Namespace</span><span class="sxs-lookup"><span data-stu-id="82f26-193">Namespace</span></span><br/>                | <span data-ttu-id="82f26-194">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="82f26-194">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="82f26-195">MOF</span><span class="sxs-lookup"><span data-stu-id="82f26-195">MOF</span></span><br/>                      | <dl> <span data-ttu-id="82f26-196"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="82f26-196"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="82f26-197">DLL</span><span class="sxs-lookup"><span data-stu-id="82f26-197">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82f26-198"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82f26-198"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82f26-199">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="82f26-199">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82f26-200">**Win32 \_ sessiondirectoriycluster**</span><span class="sxs-lookup"><span data-stu-id="82f26-200">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="82f26-201">**Win32 \_ sessiondirectoriyserver**</span><span class="sxs-lookup"><span data-stu-id="82f26-201">**Win32\_SessionDirectoryServer**</span></span>](win32-sessiondirectoryserver.md)
</dt> </dl>

 

