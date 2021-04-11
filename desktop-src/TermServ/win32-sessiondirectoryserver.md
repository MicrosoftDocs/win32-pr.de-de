---
title: Win32_SessionDirectoryServer-Klasse
description: Stellt Eigenschaften zum Anzeigen der Eigenschaften eines Remotedesktopverbindung Broker-Servers (RD-Verbindungsbroker) bereit.
ms.assetid: 73017b71-eff9-4ef6-aba0-71ddb969491f
ms.tgt_platform: multiple
keywords:
- Win32_SessionDirectoryServer-Klasse Remotedesktopdienste
- Win32_SessionDirectoryServer Klasse Remotedesktopdienste, beschrieben
topic_type:
- apiref
api_name:
- Win32_SessionDirectoryServer
- Win32_SessionDirectoryServer.ServerName
- Win32_SessionDirectoryServer.ServerIPAddress
- Win32_SessionDirectoryServer.ClusterName
- Win32_SessionDirectoryServer.NumberOfSessions
- Win32_SessionDirectoryServer.SingleSessionMode
- Win32_SessionDirectoryServer.ServerWeight
- Win32_SessionDirectoryServer.NumPendRedir
- Win32_SessionDirectoryServer.LoadIndicator
api_location:
- TssdWmi.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b9e96efb19e4db56e582cd44d05f3e9865e5282c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103949735"
---
# <a name="win32_sessiondirectoryserver-class"></a><span data-ttu-id="3984c-105">Win32 \_ sessiondirectoryserver-Klasse</span><span class="sxs-lookup"><span data-stu-id="3984c-105">Win32\_SessionDirectoryServer class</span></span>

<span data-ttu-id="3984c-106">Stellt Eigenschaften zum Anzeigen der Eigenschaften eines Remotedesktopverbindung Broker-Servers (RD-Verbindungsbroker) bereit.</span><span class="sxs-lookup"><span data-stu-id="3984c-106">Provides properties for viewing the properties of a Remote Desktop Connection Broker (RD Connection Broker) server.</span></span>

> [!Note]  
> <span data-ttu-id="3984c-107">In Windows Server 2008 R2 wurde der Name des Terminal Dienste-Sitzungs Brokers (TS-Sitzungs Broker) in "RD-Verbindungsbroker" geändert.</span><span class="sxs-lookup"><span data-stu-id="3984c-107">In Windows Server 2008 R2, the name of Terminal Services Session Broker (TS Session Broker) was changed to RD Connection Broker.</span></span> <span data-ttu-id="3984c-108">Diese Eigenschaften gelten für alle unterstützten Betriebssysteme, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="3984c-108">These properties apply to all supported operating systems unless otherwise noted.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3984c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="3984c-109">Syntax</span></span>

``` syntax
[dynamic, provider("Win32_WIN32_SESSIONDIRECTORYSERVER_Prov"), AMENDMENT]
class Win32_SessionDirectoryServer
{
  string ServerName;
  string ServerIPAddress;
  string ClusterName;
  uint32 NumberOfSessions;
  uint32 SingleSessionMode;
  uint32 ServerWeight;
  uint32 NumPendRedir;
  uint32 LoadIndicator;
};
```

## <a name="members"></a><span data-ttu-id="3984c-110">Member</span><span class="sxs-lookup"><span data-stu-id="3984c-110">Members</span></span>

<span data-ttu-id="3984c-111">Die Win32-Klasse " **\_ sessiondirectoryserver** " verfügt über diese Typen von Membern:</span><span class="sxs-lookup"><span data-stu-id="3984c-111">The **Win32\_SessionDirectoryServer** class has these types of members:</span></span>

-   [<span data-ttu-id="3984c-112">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3984c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3984c-113">Eigenschaften</span><span class="sxs-lookup"><span data-stu-id="3984c-113">Properties</span></span>

<span data-ttu-id="3984c-114">Die Win32-Klasse " **\_ sessiondirectoryserver** " verfügt über diese Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="3984c-114">The **Win32\_SessionDirectoryServer** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3984c-115">**ClusterName**</span><span class="sxs-lookup"><span data-stu-id="3984c-115">**ClusterName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3984c-116">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3984c-116">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3984c-117">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3984c-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3984c-118">Der Name der Farm, in der der Server enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3984c-118">Name of the farm that includes the server.</span></span>

</dd> <dt>

<span data-ttu-id="3984c-119">**Loadindicator**</span><span class="sxs-lookup"><span data-stu-id="3984c-119">**LoadIndicator**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3984c-120">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3984c-120">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3984c-121">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3984c-121">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3984c-122">Eine relative Zahl, die die RD-Sitzungshost Serverlast darstellt, wenn der standardmäßige Lasten Ausgleichs Algorithmus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3984c-122">A relative number that represents the RD Session Host server load when the default load-balancing algorithm is used.</span></span> <span data-ttu-id="3984c-123">Der *loadindicator* -Eigenschafts Wert basiert auf der Anzahl der Sitzungen, der Anzahl ausstehender Umleitungs Anforderungen und dem Server Gewichtungswert.</span><span class="sxs-lookup"><span data-stu-id="3984c-123">The *LoadIndicator* property value is based on the number of sessions, the number of pending redirection requests, and the server weight value.</span></span>

</dd> <dt>

<span data-ttu-id="3984c-124">**Anzahl von Sitzungen**</span><span class="sxs-lookup"><span data-stu-id="3984c-124">**NumberOfSessions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3984c-125">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3984c-125">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3984c-126">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3984c-126">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3984c-127">Anzahl der Sitzungen auf dem RD-Verbindungsbroker Server.</span><span class="sxs-lookup"><span data-stu-id="3984c-127">Number of sessions in the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="3984c-128">**Numloydredir**</span><span class="sxs-lookup"><span data-stu-id="3984c-128">**NumPendRedir**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3984c-129">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3984c-129">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3984c-130">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3984c-130">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3984c-131">Anzahl der ausstehenden Umleitungs Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="3984c-131">Number of pending redirection requests.</span></span>

</dd> <dt>

<span data-ttu-id="3984c-132">**ServerIPAddress**</span><span class="sxs-lookup"><span data-stu-id="3984c-132">**ServerIPAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3984c-133">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3984c-133">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3984c-134">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3984c-134">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3984c-135">Die IP-Adresse des RD-Verbindungsbroker Servers.</span><span class="sxs-lookup"><span data-stu-id="3984c-135">IP address of the RD Connection Broker server.</span></span> <span data-ttu-id="3984c-136">Wenn der Server sowohl für IPv4-als auch für IPv6-Adressen konfiguriert ist, enthält dieser die IPv4-Adresse.</span><span class="sxs-lookup"><span data-stu-id="3984c-136">If the server is configured for both IPv4 and IPv6 addresses, this will contain the IPv4 address.</span></span>

</dd> <dt>

<span data-ttu-id="3984c-137">**ServerName**</span><span class="sxs-lookup"><span data-stu-id="3984c-137">**ServerName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3984c-138">Datentyp: **Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="3984c-138">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="3984c-139">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3984c-139">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3984c-140">Qualifizierer: [ **Schlüssel**](/windows/desktop/WmiSdk/key-qualifier)</span><span class="sxs-lookup"><span data-stu-id="3984c-140">Qualifiers: [**key**](/windows/desktop/WmiSdk/key-qualifier)</span></span>
</dt> </dl>

<span data-ttu-id="3984c-141">Der Name des RD-Verbindungsbroker Servers.</span><span class="sxs-lookup"><span data-stu-id="3984c-141">Name of the RD Connection Broker server.</span></span>

</dd> <dt>

<span data-ttu-id="3984c-142">**Serverweight**</span><span class="sxs-lookup"><span data-stu-id="3984c-142">**ServerWeight**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3984c-143">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3984c-143">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3984c-144">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3984c-144">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3984c-145">Der Server Gewichtungswert, der beim Lastenausgleich verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3984c-145">Server weight value, used in load balancing.</span></span>

</dd> <dt>

<span data-ttu-id="3984c-146">**Singlesessionmode**</span><span class="sxs-lookup"><span data-stu-id="3984c-146">**SingleSessionMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3984c-147">Datentyp: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="3984c-147">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="3984c-148">Zugriffstyp: Schreibgeschützt</span><span class="sxs-lookup"><span data-stu-id="3984c-148">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="3984c-149">Die Einstellung für den einzelsitzungmodus des RD-Verbindungsbroker Servers.</span><span class="sxs-lookup"><span data-stu-id="3984c-149">Single session mode setting of the RD Connection Broker server.</span></span>

<dt>

<span data-ttu-id="3984c-150">0</span><span class="sxs-lookup"><span data-stu-id="3984c-150">0</span></span>
</dt> <dd>

<span data-ttu-id="3984c-151">Die Farm befindet sich nicht im Einzel Sitzungs Modus.</span><span class="sxs-lookup"><span data-stu-id="3984c-151">The farm is not in single session mode.</span></span>

</dd> <dt>

<span data-ttu-id="3984c-152">1</span><span class="sxs-lookup"><span data-stu-id="3984c-152">1</span></span>
</dt> <dd>

<span data-ttu-id="3984c-153">Die Farm in befindet sich im Einzel Sitzungs Modus.</span><span class="sxs-lookup"><span data-stu-id="3984c-153">The farm in is in single session mode.</span></span>

</dd> </dl>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3984c-154">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3984c-154">Remarks</span></span>

<span data-ttu-id="3984c-155">Managed Object Format-Dateien (MOF) enthalten die Definitionen für Windows-Verwaltungsinstrumentation (WMI)-Klassen.</span><span class="sxs-lookup"><span data-stu-id="3984c-155">Managed Object Format (MOF) files contain the definitions for Windows Management Instrumentation (WMI) classes.</span></span> <span data-ttu-id="3984c-156">MOF-Dateien werden nicht als Teil des Microsoft Windows Software Development Kit (SDK) installiert.</span><span class="sxs-lookup"><span data-stu-id="3984c-156">MOF files are not installed as part of the Microsoft Windows Software Development Kit (SDK).</span></span> <span data-ttu-id="3984c-157">Sie werden auf dem Server installiert, wenn Sie die zugehörige Rolle mithilfe der Server-Manager hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="3984c-157">They are installed on the server when you add the associated role by using the Server Manager.</span></span> <span data-ttu-id="3984c-158">Weitere Informationen zu MOF-Dateien finden Sie unter [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span><span class="sxs-lookup"><span data-stu-id="3984c-158">For more information about MOF files, see [Managed Object Format (MOF)](/windows/desktop/WmiSdk/managed-object-format--mof-).</span></span>

## <a name="requirements"></a><span data-ttu-id="3984c-159">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3984c-159">Requirements</span></span>



| <span data-ttu-id="3984c-160">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3984c-160">Requirement</span></span> | <span data-ttu-id="3984c-161">Wert</span><span class="sxs-lookup"><span data-stu-id="3984c-161">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="3984c-162">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3984c-162">Minimum supported client</span></span><br/> | <span data-ttu-id="3984c-163">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="3984c-163">None supported</span></span><br/>                                                              |
| <span data-ttu-id="3984c-164">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3984c-164">Minimum supported server</span></span><br/> | <span data-ttu-id="3984c-165">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3984c-165">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="3984c-166">Namespace</span><span class="sxs-lookup"><span data-stu-id="3984c-166">Namespace</span></span><br/>                | <span data-ttu-id="3984c-167">Root\\CIMv2</span><span class="sxs-lookup"><span data-stu-id="3984c-167">Root\\CIMv2</span></span><br/>                                                                 |
| <span data-ttu-id="3984c-168">MOF</span><span class="sxs-lookup"><span data-stu-id="3984c-168">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3984c-169"><dt>"Tssdwmi. mof"</dt></span><span class="sxs-lookup"><span data-stu-id="3984c-169"><dt>TssdWmi.mof</dt></span></span> </dl> |
| <span data-ttu-id="3984c-170">DLL</span><span class="sxs-lookup"><span data-stu-id="3984c-170">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3984c-171"><dt>TssdWmi.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3984c-171"><dt>TssdWmi.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3984c-172">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3984c-172">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3984c-173">**Win32 \_ sessiondirectoriycluster**</span><span class="sxs-lookup"><span data-stu-id="3984c-173">**Win32\_SessionDirectoryCluster**</span></span>](win32-sessiondirectorycluster.md)
</dt> <dt>

[<span data-ttu-id="3984c-174">**Win32 \_ sessiondirectoriysession**</span><span class="sxs-lookup"><span data-stu-id="3984c-174">**Win32\_SessionDirectorySession**</span></span>](win32-sessiondirectorysession.md)
</dt> </dl>

 

