---
title: RAS_PORT_0 Struktur (rassapi. h)
description: Die Struktur des RAS- \_ Ports \_ 0 enthält Informationen, die einen RAS-Port beschreiben.
ms.assetid: 750fc705-0770-427b-b7d6-7876b8b9118a
keywords:
- RAS_PORT_0 Struktur-RAS
- PRAS_PORT_0-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- RAS_PORT_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 80d66725415d86aea44138f23fb3748e3187820f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104517882"
---
# <a name="ras_port_0-structure"></a><span data-ttu-id="aacc9-105">RAS- \_ Port \_ 0-Struktur</span><span class="sxs-lookup"><span data-stu-id="aacc9-105">RAS\_PORT\_0 structure</span></span>

<span data-ttu-id="aacc9-106">\[Diese Version der **RAS- \_ Port \_ 0** -Struktur wird ab Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aacc9-106">\[This version of the **RAS\_PORT\_0** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="aacc9-107">Verwenden Sie stattdessen den neueren [**RAS- \_ Port \_ 0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) , der in MPRAPI. h definiert ist.\]</span><span class="sxs-lookup"><span data-stu-id="aacc9-107">Use the newer [**RAS\_PORT\_0**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_0) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="aacc9-108">Die Struktur des **RAS- \_ Ports \_ 0** enthält Informationen, die einen RAS-Port beschreiben.</span><span class="sxs-lookup"><span data-stu-id="aacc9-108">The **RAS\_PORT\_0** structure contains information that describes a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="aacc9-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="aacc9-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_0 {
  WCHAR wszPortName[RASSAPI_MAX_PORT_NAME];
  WCHAR wszDeviceType[RASSAPI_MAX_DEVICETYPE_NAME];
  WCHAR wszDeviceName[RASSAPI_MAX_DEVICE_NAME];
  WCHAR wszMediaName[RASSAPI_MAX_MEDIA_NAME];
  DWORD reserved;
  DWORD Flags;
  WCHAR wszUserName[UNLEN + 1];
  WCHAR wszComputer[NETBIOS_NAME_LEN];
  DWORD dwStartSessionTime;
  WCHAR wszLogonDomain[DNLEN + 1];
  BOOL  fAdvancedServer;
} RAS_PORT_0, *PRAS_PORT_0;
```



## <a name="members"></a><span data-ttu-id="aacc9-110">Member</span><span class="sxs-lookup"><span data-stu-id="aacc9-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="aacc9-111">**wszportname**</span><span class="sxs-lookup"><span data-stu-id="aacc9-111">**wszPortName**</span></span>
</dt> <dd>

<span data-ttu-id="aacc9-112">Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Ports angibt, z. b. "COM1".</span><span class="sxs-lookup"><span data-stu-id="aacc9-112">A null-terminated Unicode string that specifies the name of the port, such as "COM1".</span></span>

</dd> <dt>

<span data-ttu-id="aacc9-113">**wszde vicetype**</span><span class="sxs-lookup"><span data-stu-id="aacc9-113">**wszDeviceType**</span></span>
</dt> <dd>

<span data-ttu-id="aacc9-114">Eine NULL-terminierte Unicode-Zeichenfolge, die den Typ des Geräts angibt, auf dem die Verbindung hergestellt wurde (z. b. Modem oder ISDN).</span><span class="sxs-lookup"><span data-stu-id="aacc9-114">A null-terminated Unicode string that specifies the type of the device on which the connection was made, such as Modem or ISDN.</span></span> <span data-ttu-id="aacc9-115">Die Liste der Gerätetypen, die in diesem Mitglied angegeben werden können, umfasst alle auf dem Server installierten Gerätetypen, einschließlich der Geräte von Drittanbietern.</span><span class="sxs-lookup"><span data-stu-id="aacc9-115">The list of device types that might be specified in this member includes all the device types installed on the server, including third-party devices.</span></span>

</dd> <dt>

<span data-ttu-id="aacc9-116">**wszdevicename**</span><span class="sxs-lookup"><span data-stu-id="aacc9-116">**wszDeviceName**</span></span>
</dt> <dd>

<span data-ttu-id="aacc9-117">Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Geräts angibt, auf dem die Verbindung hergestellt wurde, z. b. "Hayes 9600" oder "PCIMACISDN1".</span><span class="sxs-lookup"><span data-stu-id="aacc9-117">A null-terminated Unicode string that specifies the name of the device on which the connection was made, such as "Hayes 9600" or "PCIMACISDN1".</span></span>

</dd> <dt>

<span data-ttu-id="aacc9-118">**wszmedianame**</span><span class="sxs-lookup"><span data-stu-id="aacc9-118">**wszMediaName**</span></span>
</dt> <dd>

<span data-ttu-id="aacc9-119">Gibt eine auf NULL endende Unicode-Zeichenfolge an, die den Namen des Mediums angibt, das für die Verbindung verwendet wird, z. b. *rasser* oder *RASTAPI*.</span><span class="sxs-lookup"><span data-stu-id="aacc9-119">Specifies a null-terminated Unicode string that specifies the name of the media used for the connection, such as *rasser* or *rastapi*.</span></span>

</dd> <dt>

<span data-ttu-id="aacc9-120">**bleiben**</span><span class="sxs-lookup"><span data-stu-id="aacc9-120">**reserved**</span></span>
</dt> <dd>

<span data-ttu-id="aacc9-121">Reserviert.</span><span class="sxs-lookup"><span data-stu-id="aacc9-121">Reserved.</span></span>

</dd> <dt>

<span data-ttu-id="aacc9-122">**Flags**</span><span class="sxs-lookup"><span data-stu-id="aacc9-122">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="aacc9-123">Gibt einen Satz von Bitflags an, die die Art der Verbindung angeben, die auf diesem Port hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="aacc9-123">Specifies a set of bit flags that specify the nature of the connection made on this port.</span></span> <span data-ttu-id="aacc9-124">Dieser Member kann eine Kombination der folgenden Flags sein.</span><span class="sxs-lookup"><span data-stu-id="aacc9-124">This member can be a combination of the following flags.</span></span>



| <span data-ttu-id="aacc9-125">Wert</span><span class="sxs-lookup"><span data-stu-id="aacc9-125">Value</span></span>                                                                                                                                                                        | <span data-ttu-id="aacc9-126">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="aacc9-126">Meaning</span></span>                                                                                                                                                                                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="GATEWAY_ACTIVE"></span><span id="gateway_active"></span><dl> <span data-ttu-id="aacc9-127"><dt>**Gateway \_ aktiv**</dt></span><span class="sxs-lookup"><span data-stu-id="aacc9-127"><dt>**GATEWAY\_ACTIVE**</dt></span></span> </dl>             | <span data-ttu-id="aacc9-128">Wenn dieses Flag festgelegt ist, ist das NetBIOS-Gateway auf dem Server aktiv.</span><span class="sxs-lookup"><span data-stu-id="aacc9-128">If this flag is set, the NetBIOS gateway is active on the server.</span></span><br/>                                                                                                                                                                                                                                                                                                               |
| <span id="MESSENGER_PRESENT"></span><span id="messenger_present"></span><dl> <span data-ttu-id="aacc9-129"><dt>**Messenger \_ vorhanden**</dt></span><span class="sxs-lookup"><span data-stu-id="aacc9-129"><dt>**MESSENGER\_PRESENT**</dt></span></span> </dl>    | <span data-ttu-id="aacc9-130">Wenn dieses Flag festgelegt ist, wird der Messenger-Dienst auf dem Remote Client ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="aacc9-130">If this flag is set, the messenger service is running on the remote client.</span></span><br/>                                                                                                                                                                                                                                                                                                     |
| <span id="PORT_MULTILINKED"></span><span id="port_multilinked"></span><dl> <span data-ttu-id="aacc9-131"><dt>**Port ( \_ multiverknüpft)**</dt></span><span class="sxs-lookup"><span data-stu-id="aacc9-131"><dt>**PORT\_MULTILINKED**</dt></span></span> </dl>       | <span data-ttu-id="aacc9-132">Wenn dieses Flag festgelegt ist, wird der Port mehrfach mit anderen Ports verknüpft.</span><span class="sxs-lookup"><span data-stu-id="aacc9-132">If this flag is set, the port is multilinked with other ports.</span></span> <span data-ttu-id="aacc9-133">Verwenden Sie diese Informationen, um den Verbindungsstatus als mehrfach verknüpften Port anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aacc9-133">Use this information to display the connection status as a multilinked port.</span></span> <br/> <span data-ttu-id="aacc9-134">Bei einem mehrfach verknüpften Port enthält die Struktur der [**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md) zwei Sätze von Statistiken: eine für den Port allein und eine für die kombinierten Ports in der Verbindung mit mehreren Links.</span><span class="sxs-lookup"><span data-stu-id="aacc9-134">For a multilinked port, the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure contains two sets of statistics: one for the port alone, and another for the combined ports in the multilink connection.</span></span><br/> |
| <span id="PPP_CLIENT"></span><span id="ppp_client"></span><dl> <span data-ttu-id="aacc9-135"><dt>**PPP- \_ Client**</dt></span><span class="sxs-lookup"><span data-stu-id="aacc9-135"><dt>**PPP\_CLIENT**</dt></span></span> </dl>                         | <span data-ttu-id="aacc9-136">Wenn dieses Flag festgelegt ist, stellt der Remote Client eine Verbindung mit PPP her.</span><span class="sxs-lookup"><span data-stu-id="aacc9-136">If this flag is set, the remote client connected using PPP.</span></span> <span data-ttu-id="aacc9-137">Wenn dieses Flag nicht festgelegt ist, ist der Remote Client über das AMB-Protokoll verbunden.</span><span class="sxs-lookup"><span data-stu-id="aacc9-137">If this flag is not set, the remote client connected using the AMB protocol.</span></span><br/>                                                                                                                                                                                                                                        |
| <span id="REMOTE_LISTEN"></span><span id="remote_listen"></span><dl> <span data-ttu-id="aacc9-138"><dt>**Remote \_ Überwachung**</dt></span><span class="sxs-lookup"><span data-stu-id="aacc9-138"><dt>**REMOTE\_LISTEN**</dt></span></span> </dl>                | <span data-ttu-id="aacc9-139">Wenn dieses Flag festgelegt ist, wird der remotelisten-Parameter des NetBIOS-Gateways auf dem Server auf 1 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="aacc9-139">If this flag is set, the RemoteListen parameter of the NetBIOS gateway is set to 1 on the server.</span></span><br/>                                                                                                                                                                                                                                                                               |
| <span id="USER_AUTHENTICATED"></span><span id="user_authenticated"></span><dl> <span data-ttu-id="aacc9-140"><dt>**Benutzer \_ authentifiziert**</dt></span><span class="sxs-lookup"><span data-stu-id="aacc9-140"><dt>**USER\_AUTHENTICATED**</dt></span></span> </dl> | <span data-ttu-id="aacc9-141">Wenn dieses Flag festgelegt ist, wird ein Remote Client mit dem Server verbunden, und der Benutzer wurde authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="aacc9-141">If this flag is set, a remote client is connected to the server and the user has been authenticated.</span></span> <span data-ttu-id="aacc9-142">Aktivieren Sie dieses Flag, um sicherzustellen, dass ein Client tatsächlich mit einem Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="aacc9-142">Check this flag to ensure that a client is actually connected to a port.</span></span><br/>                                                                                                                                                                                                   |



 

<span data-ttu-id="aacc9-143">\_ \_ \_ Verwenden Sie den Messenger-Dienst, um eine administrative Nachricht an den Remote Client zu senden, wenn der Messenger vorhanden ist, das Gateway aktiv ist und die remoteüberwachungsflags festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="aacc9-143">If the MESSENGER\_PRESENT, GATEWAY\_ACTIVE, and REMOTE\_LISTEN flags are set, use the messenger service to send an administrative message to the remote client.</span></span> <span data-ttu-id="aacc9-144">Wenn Messenger \_ vorhanden ist und Remote Überwachung \_ festgelegt ist, das Gateway jedoch \_ nicht aktiv ist, senden Sie Nachrichten nur von dem RAS-Server, mit dem der Client verbunden ist, an den Client.</span><span class="sxs-lookup"><span data-stu-id="aacc9-144">If MESSENGER\_PRESENT and REMOTE\_LISTEN are set, but GATEWAY\_ACTIVE is not, send messages to the client only from the RAS server to which the client is connected.</span></span>

</dd> <dt>

<span data-ttu-id="aacc9-145">**wszUserName**</span><span class="sxs-lookup"><span data-stu-id="aacc9-145">**wszUserName**</span></span>
</dt> <dd>

<span data-ttu-id="aacc9-146">Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Remote Benutzers angibt, der mit diesem Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="aacc9-146">A null-terminated Unicode string that specifies the name of the remote user connected to this port.</span></span>

</dd> <dt>

<span data-ttu-id="aacc9-147">**wszcomputer**</span><span class="sxs-lookup"><span data-stu-id="aacc9-147">**wszComputer**</span></span>
</dt> <dd>

<span data-ttu-id="aacc9-148">Eine NULL-terminierte Unicode-Zeichenfolge, die den Namen des Remote Client Computers angibt.</span><span class="sxs-lookup"><span data-stu-id="aacc9-148">A null-terminated Unicode string that specifies the name of the remote client computer.</span></span>

</dd> <dt>

<span data-ttu-id="aacc9-149">**dwstarungessiontime**</span><span class="sxs-lookup"><span data-stu-id="aacc9-149">**dwStartSessionTime**</span></span>
</dt> <dd>

<span data-ttu-id="aacc9-150">Gibt die Zeit in Sekunden ab dem 1. Januar 1970 an, die der Client mit dem RAS-Server auf diesem Port verbunden hat.</span><span class="sxs-lookup"><span data-stu-id="aacc9-150">Specifies the time, in seconds from January 1, 1970, that the client connected to the RAS server on this port.</span></span> <span data-ttu-id="aacc9-151">Verwenden Sie die Standardzeit Funktionen, um diesen Wert für die Anzeige zu formatieren.</span><span class="sxs-lookup"><span data-stu-id="aacc9-151">Use the standard time functions to format this value for display.</span></span>

</dd> <dt>

<span data-ttu-id="aacc9-152">**wszlogondomain**</span><span class="sxs-lookup"><span data-stu-id="aacc9-152">**wszLogonDomain**</span></span>
</dt> <dd>

<span data-ttu-id="aacc9-153">Gibt eine NULL-terminierte Unicode-Zeichenfolge an, die den Namen der Domäne angibt, in der der Remote Benutzer authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="aacc9-153">Specifies a null-terminated Unicode string that specifies the name of the domain on which the remote user was authenticated.</span></span> <span data-ttu-id="aacc9-154">Diese Zeichenfolge ist nur der Domänen Name und ohne das \\ \\ Präfix "".</span><span class="sxs-lookup"><span data-stu-id="aacc9-154">This string is the domain name only, with no "\\\\" prefix.</span></span>

</dd> <dt>

<span data-ttu-id="aacc9-155">**"f"-Server**</span><span class="sxs-lookup"><span data-stu-id="aacc9-155">**fAdvancedServer**</span></span>
</dt> <dd>

<span data-ttu-id="aacc9-156">Gibt ein Flag an, das ungleich 0 (null) ist, wenn der diesem Port zugeordnete RAS-Server ein erweiterter Server wie Windows 2000 Advanced Server ist.</span><span class="sxs-lookup"><span data-stu-id="aacc9-156">Specifies a flag that is nonzero if the RAS server associated with this port is an advanced server such as Windows 2000 Advanced Server.</span></span> <span data-ttu-id="aacc9-157">Verwenden Sie diese Informationen, um den Namen des Servers zu ermitteln, der über die Benutzerkonten Datenbank verfügt.</span><span class="sxs-lookup"><span data-stu-id="aacc9-157">Use this information to determine the name of the server that has the user account database.</span></span> <span data-ttu-id="aacc9-158">Wenn der RAS-Server ein erweiterter Server ist, erhalten Sie den Namen des Benutzerkonto Servers, indem Sie das Präfix "" mit dem Namen verketten, der \\ \\ im **wszlogondomain** -Member zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="aacc9-158">If the RAS server is an advanced server, get the name of the user account server by concatenating the prefix "\\\\" to the name returned in the **wszLogonDomain** member.</span></span> <span data-ttu-id="aacc9-159">Dies liegt daran, dass für einen erweiterten Server der Name der lokalen Anmelde Domäne mit dem Servernamen identisch ist.</span><span class="sxs-lookup"><span data-stu-id="aacc9-159">This is because for an advanced server the local logon domain name is the same as the server name.</span></span> <span data-ttu-id="aacc9-160">Wenn es sich bei dem RAS-Server um eine Arbeitsstation handelt, verwenden Sie die [**rasadmingetuseraccountserver**](rasadmingetuseraccountserver.md) -Funktion, um den Namen des Benutzerkonto Servers abzurufen.</span><span class="sxs-lookup"><span data-stu-id="aacc9-160">If the RAS server is a workstation, use the [**RasAdminGetUserAccountServer**](rasadmingetuseraccountserver.md) function to get the name of the user account server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="aacc9-161">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="aacc9-161">Requirements</span></span>



| <span data-ttu-id="aacc9-162">Anforderung</span><span class="sxs-lookup"><span data-stu-id="aacc9-162">Requirement</span></span> | <span data-ttu-id="aacc9-163">Wert</span><span class="sxs-lookup"><span data-stu-id="aacc9-163">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="aacc9-164">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="aacc9-164">Minimum supported client</span></span><br/> | <span data-ttu-id="aacc9-165">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aacc9-165">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="aacc9-166">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="aacc9-166">Minimum supported server</span></span><br/> | <span data-ttu-id="aacc9-167">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="aacc9-167">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="aacc9-168">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="aacc9-168">End of client support</span></span><br/>    | <span data-ttu-id="aacc9-169">Windows XP</span><span class="sxs-lookup"><span data-stu-id="aacc9-169">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="aacc9-170">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="aacc9-170">End of server support</span></span><br/>    | <span data-ttu-id="aacc9-171">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="aacc9-171">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="aacc9-172">Header</span><span class="sxs-lookup"><span data-stu-id="aacc9-172">Header</span></span><br/>                   | <dl> <span data-ttu-id="aacc9-173"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="aacc9-173"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aacc9-174">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aacc9-174">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aacc9-175">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="aacc9-175">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="aacc9-176">RAS-Server-Verwaltungsstrukturen</span><span class="sxs-lookup"><span data-stu-id="aacc9-176">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="aacc9-177">**RAS- \_ Port \_ 1**</span><span class="sxs-lookup"><span data-stu-id="aacc9-177">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="aacc9-178">**RAS- \_ Port \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="aacc9-178">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="aacc9-179">**Rasadmingetuseraccountserver**</span><span class="sxs-lookup"><span data-stu-id="aacc9-179">**RasAdminGetUserAccountServer**</span></span>](rasadmingetuseraccountserver.md)
</dt> <dt>

[<span data-ttu-id="aacc9-180">**Rasadminportenum**</span><span class="sxs-lookup"><span data-stu-id="aacc9-180">**RasAdminPortEnum**</span></span>](rasadminportenum.md)
</dt> </dl>

 

 





