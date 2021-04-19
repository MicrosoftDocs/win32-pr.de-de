---
title: RAS_PORT_1 Struktur (rassapi. h)
description: Die Struktur des RAS- \_ Ports \_ 1 enthält Informationen zu einem RAS-Port.
ms.assetid: f226ef16-feb4-41e0-ba60-ddb2f0acd305
keywords:
- RAS_PORT_1 Struktur-RAS
- PRAS_PORT_1-Struktur Zeiger RAS
topic_type:
- apiref
api_name:
- RAS_PORT_1
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d73fe450e5ea5f8ceee48436dbbe05570d0d818a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106346721"
---
# <a name="ras_port_1-structure"></a><span data-ttu-id="77c5e-105">RAS- \_ Port \_ 1-Struktur</span><span class="sxs-lookup"><span data-stu-id="77c5e-105">RAS\_PORT\_1 structure</span></span>

<span data-ttu-id="77c5e-106">\[Diese Version der RAS-Struktur von **\_ Port \_ 1** wird ab Windows Vista nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="77c5e-106">\[This version of the **RAS\_PORT\_1** structure is not supported as of Windows Vista.</span></span> <span data-ttu-id="77c5e-107">Verwenden Sie stattdessen den neueren [**RAS- \_ Port \_ 1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) , der in MPRAPI. h definiert ist.\]</span><span class="sxs-lookup"><span data-stu-id="77c5e-107">Use the newer [**RAS\_PORT\_1**](/windows/desktop/api/Mprapi/ns-mprapi-ras_port_1) defined in mprapi.h instead.\]</span></span>

<span data-ttu-id="77c5e-108">Die Struktur des **RAS- \_ Ports \_ 1** enthält Informationen zu einem RAS-Port.</span><span class="sxs-lookup"><span data-stu-id="77c5e-108">The **RAS\_PORT\_1** structure contains information about a RAS port.</span></span>

## <a name="syntax"></a><span data-ttu-id="77c5e-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="77c5e-109">Syntax</span></span>


```C++
typedef struct _RAS_PORT_1 {
  RAS_PORT_0                rasport0;
  DWORD                     LineCondition;
  DWORD                     HardwareCondition;
  DWORD                     LineSpeed;
  WORD                      NumStatistics;
  WORD                      NumMediaParms;
  DWORD                     SizeMediaParms;
  RAS_PPP_PROJECTION_RESULT ProjResult;
} RAS_PORT_1, *PRAS_PORT_1;
```



## <a name="members"></a><span data-ttu-id="77c5e-110">Member</span><span class="sxs-lookup"><span data-stu-id="77c5e-110">Members</span></span>

<dl> <dt>

<span data-ttu-id="77c5e-111">**rasport0**</span><span class="sxs-lookup"><span data-stu-id="77c5e-111">**rasport0**</span></span>
</dt> <dd>

<span data-ttu-id="77c5e-112">Gibt eine [**RAS- \_ Port \_ 0**](ras-port-0-str.md) -Struktur an, die Informationen über den Port enthält, z. b. den Namen des Ports, den Namen des Remote Benutzers, der mit dem Port verbunden ist, usw.</span><span class="sxs-lookup"><span data-stu-id="77c5e-112">Specifies a [**RAS\_PORT\_0**](ras-port-0-str.md) structure that contains information about the port, such as the name of the port, the name of the remote user connected to the port, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="77c5e-113">**Linecondition**</span><span class="sxs-lookup"><span data-stu-id="77c5e-113">**LineCondition**</span></span>
</dt> <dd>

<span data-ttu-id="77c5e-114">Gibt den Status des Ports an.</span><span class="sxs-lookup"><span data-stu-id="77c5e-114">Specifies the state of the port.</span></span> <span data-ttu-id="77c5e-115">Dieser Member kann einen der folgenden Werte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="77c5e-115">This member can be one of the following values.</span></span>



| <span data-ttu-id="77c5e-116">Wert</span><span class="sxs-lookup"><span data-stu-id="77c5e-116">Value</span></span>                                                                                                                                                                                            | <span data-ttu-id="77c5e-117">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="77c5e-117">Meaning</span></span>                                                                                                                                                                |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="RAS_PORT_NON_OPERATIONAL"></span><span id="ras_port_non_operational"></span><dl> <span data-ttu-id="77c5e-118"><dt>**RAS- \_ Port \_ nicht \_ betriebsbereit**</dt></span><span class="sxs-lookup"><span data-stu-id="77c5e-118"><dt>**RAS\_PORT\_NON\_OPERATIONAL**</dt></span></span> </dl> | <span data-ttu-id="77c5e-119">Der Port ist nicht funktionstüchtig.</span><span class="sxs-lookup"><span data-stu-id="77c5e-119">The port is not operational.</span></span> <span data-ttu-id="77c5e-120">Überprüfen Sie das Ereignisprotokoll auf Fehler, die vom Server gemeldet wurden.</span><span class="sxs-lookup"><span data-stu-id="77c5e-120">Check the event log for errors reported by the server.</span></span><br/>                                                                         |
| <span id="RAS_PORT_DISCONNECTED"></span><span id="ras_port_disconnected"></span><dl> <span data-ttu-id="77c5e-121"><dt>**RAS- \_ Port \_ getrennt**</dt></span><span class="sxs-lookup"><span data-stu-id="77c5e-121"><dt>**RAS\_PORT\_DISCONNECTED**</dt></span></span> </dl>           | <span data-ttu-id="77c5e-122">Der Port ist derzeit nicht getrennt.</span><span class="sxs-lookup"><span data-stu-id="77c5e-122">The port is currently disconnected.</span></span><br/>                                                                                                                         |
| <span id="RAS_PORT_CALLING_BACK"></span><span id="ras_port_calling_back"></span><dl> <span data-ttu-id="77c5e-123"><dt>**RAS \_ - \_ Port \_ Rückruf**</dt></span><span class="sxs-lookup"><span data-stu-id="77c5e-123"><dt>**RAS\_PORT\_CALLING\_BACK**</dt></span></span> </dl>          | <span data-ttu-id="77c5e-124">Der RAS-Server Ruft den RAS-Client zurück.</span><span class="sxs-lookup"><span data-stu-id="77c5e-124">The RAS server is calling back the RAS client.</span></span><br/>                                                                                                              |
| <span id="RAS_PORT_LISTENING"></span><span id="ras_port_listening"></span><dl> <span data-ttu-id="77c5e-125"><dt>**RAS- \_ Port Überwachung \_**</dt></span><span class="sxs-lookup"><span data-stu-id="77c5e-125"><dt>**RAS\_PORT\_LISTENING**</dt></span></span> </dl>                    | <span data-ttu-id="77c5e-126">Der Port wartet darauf, dass ein Client in aufruft.</span><span class="sxs-lookup"><span data-stu-id="77c5e-126">The port is waiting for a client to call in.</span></span><br/>                                                                                                                |
| <span id="RAS_PORT_AUTHENTICATING"></span><span id="ras_port_authenticating"></span><dl> <span data-ttu-id="77c5e-127"><dt>**RAS- \_ Port \_ Authentifizierung**</dt></span><span class="sxs-lookup"><span data-stu-id="77c5e-127"><dt>**RAS\_PORT\_AUTHENTICATING**</dt></span></span> </dl>     | <span data-ttu-id="77c5e-128">Der Server authentifiziert den Remote Client.</span><span class="sxs-lookup"><span data-stu-id="77c5e-128">The server is in the process of authenticating the remote client.</span></span><br/>                                                                                           |
| <span id="RAS_PORT_AUTHENTICATED"></span><span id="ras_port_authenticated"></span><dl> <span data-ttu-id="77c5e-129"><dt>**RAS- \_ Port \_ authentifiziert**</dt></span><span class="sxs-lookup"><span data-stu-id="77c5e-129"><dt>**RAS\_PORT\_AUTHENTICATED**</dt></span></span> </dl>        | <span data-ttu-id="77c5e-130">Der Remote Client ist jetzt authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="77c5e-130">The remote client is now authenticated.</span></span><br/>                                                                                                                     |
| <span id="RAS_PORT_INITIALIZING"></span><span id="ras_port_initializing"></span><dl> <span data-ttu-id="77c5e-131"><dt>**RAS- \_ Port \_ Initialisierung**</dt></span><span class="sxs-lookup"><span data-stu-id="77c5e-131"><dt>**RAS\_PORT\_INITIALIZING**</dt></span></span> </dl>           | <span data-ttu-id="77c5e-132">Das an den Port angefügte Gerät wird initialisiert.</span><span class="sxs-lookup"><span data-stu-id="77c5e-132">The device attached to the port is being initialized.</span></span> <span data-ttu-id="77c5e-133">\_ \_ Wenn die Initialisierung abgeschlossen ist, ändert sich der Status des Ports in den RAS-Port.</span><span class="sxs-lookup"><span data-stu-id="77c5e-133">The state of the port will change to RAS\_PORT\_LISTENING when the initialization has been completed.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="77c5e-134">**Hardwarecondition**</span><span class="sxs-lookup"><span data-stu-id="77c5e-134">**HardwareCondition**</span></span>
</dt> <dd>

<span data-ttu-id="77c5e-135">Gibt einen der folgenden Werte an, um den Status des Geräts anzugeben, das mit dem Port verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="77c5e-135">Specifies one of the following values to indicate the state of the device attached to the port.</span></span>



| <span data-ttu-id="77c5e-136">Wert</span><span class="sxs-lookup"><span data-stu-id="77c5e-136">Value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="77c5e-137">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="77c5e-137">Meaning</span></span>                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| <span id="RAS_MODEM_OPERATIONAL"></span><span id="ras_modem_operational"></span><dl> <span data-ttu-id="77c5e-138"><dt>**RAS- \_ Modem \_ betriebsbereit**</dt></span><span class="sxs-lookup"><span data-stu-id="77c5e-138"><dt>**RAS\_MODEM\_OPERATIONAL**</dt></span></span> </dl>                 | <span data-ttu-id="77c5e-139">Das an diesen Port angefügte Modem ist funktionstüchtig und bereit zum Empfangen von Client aufrufen.</span><span class="sxs-lookup"><span data-stu-id="77c5e-139">The modem attached to this port is operational and is ready to receive client calls.</span></span><br/> |
| <span id="RAS_MODEM_HARDWARE_FAILURE"></span><span id="ras_modem_hardware_failure"></span><dl> <span data-ttu-id="77c5e-140"><dt>**\_ \_ Hardware \_ Fehler des RAS-Modem**</dt></span><span class="sxs-lookup"><span data-stu-id="77c5e-140"><dt>**RAS\_MODEM\_HARDWARE\_FAILURE**</dt></span></span> </dl> | <span data-ttu-id="77c5e-141">Das an diesen Port angefügte Modem hat ein Hardwareproblem.</span><span class="sxs-lookup"><span data-stu-id="77c5e-141">The modem attached to this port has a hardware problem.</span></span><br/>                              |



 

</dd> <dt>

<span data-ttu-id="77c5e-142">**Linespeed**</span><span class="sxs-lookup"><span data-stu-id="77c5e-142">**LineSpeed**</span></span>
</dt> <dd>

<span data-ttu-id="77c5e-143">Gibt die Geschwindigkeit in Bits pro Sekunde an, mit der der Computer mit dem Port kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="77c5e-143">Specifies the speed, in bits per second, with which the computer can communicate with the port.</span></span>

</dd> <dt>

<span data-ttu-id="77c5e-144">**Numstatistics**</span><span class="sxs-lookup"><span data-stu-id="77c5e-144">**NumStatistics**</span></span>
</dt> <dd>

<span data-ttu-id="77c5e-145">Dieser Member wird nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="77c5e-145">This member is not used.</span></span> <span data-ttu-id="77c5e-146">Die RAS-Verwaltungsfunktionen, wie z. b. die [**rasadminportgetinfo**](rasadminportgetinfo.md) -Funktion, verwenden die Struktur der [**RAS- \_ Port \_ Statistik**](ras-port-statistics-str.md) , um Port Statistiken zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="77c5e-146">The RAS administration functions, such as the [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function, use the [**RAS\_PORT\_STATISTICS**](ras-port-statistics-str.md) structure to return port statistics.</span></span>

</dd> <dt>

<span data-ttu-id="77c5e-147">**Nummediaparms**</span><span class="sxs-lookup"><span data-stu-id="77c5e-147">**NumMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="77c5e-148">Gibt die Anzahl der medienspezifischen Parameter für diesen Port an.</span><span class="sxs-lookup"><span data-stu-id="77c5e-148">Specifies the number of media-specific parameters for this port.</span></span> <span data-ttu-id="77c5e-149">Bei seriellen Medien ist dies in der Regel die Anzahl der Werte, die in der SERIAL.INI-Datei angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="77c5e-149">For serial media this is typically the number of values that appear in the SERIAL.INI file.</span></span>

</dd> <dt>

<span data-ttu-id="77c5e-150">**Sizemediaparms**</span><span class="sxs-lookup"><span data-stu-id="77c5e-150">**SizeMediaParms**</span></span>
</dt> <dd>

<span data-ttu-id="77c5e-151">Gibt die Größe (in Bytes) des Puffers an, der für alle medienspezifischen Parameter benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="77c5e-151">Specifies the size, in bytes, of the buffer required for all media-specific parameters.</span></span> <span data-ttu-id="77c5e-152">Die [**rasadminportgetinfo**](rasadminportgetinfo.md) -Funktion gibt einen Puffer zurück, der ein Array von [**RAS- \_ Parameter**](ras-parameters-str.md) Strukturen mit den Medien Parametern und-Werten für den Port enthält.</span><span class="sxs-lookup"><span data-stu-id="77c5e-152">The [**RasAdminPortGetInfo**](rasadminportgetinfo.md) function returns a buffer that contains an array of [**RAS\_PARAMETERS**](ras-parameters-str.md) structures with the media parameters and values for the port.</span></span>

</dd> <dt>

<span data-ttu-id="77c5e-153">**Projresult**</span><span class="sxs-lookup"><span data-stu-id="77c5e-153">**ProjResult**</span></span>
</dt> <dd>

<span data-ttu-id="77c5e-154">Eine [**RAS- \_ PPP- \_ Projektions \_ Ergebnis**](ras-ppp-projection-result-str.md) Struktur, die die PPP-Projektionsinformationen für diesen Port angibt.</span><span class="sxs-lookup"><span data-stu-id="77c5e-154">A [**RAS\_PPP\_PROJECTION\_RESULT**](ras-ppp-projection-result-str.md) structure that specifies the PPP projection information for this port.</span></span> <span data-ttu-id="77c5e-155">Diese Struktur stellt Informationen für jedes Protokoll bereit, das verhandelt wird, wenn ein RAS-Client eine Verbindung mit einem Server herstellt.</span><span class="sxs-lookup"><span data-stu-id="77c5e-155">This structure provides information for each protocol that is negotiated when a RAS client connects to a server.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="77c5e-156">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="77c5e-156">Requirements</span></span>



| <span data-ttu-id="77c5e-157">Anforderung</span><span class="sxs-lookup"><span data-stu-id="77c5e-157">Requirement</span></span> | <span data-ttu-id="77c5e-158">Wert</span><span class="sxs-lookup"><span data-stu-id="77c5e-158">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="77c5e-159">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="77c5e-159">Minimum supported client</span></span><br/> | <span data-ttu-id="77c5e-160">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77c5e-160">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="77c5e-161">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="77c5e-161">Minimum supported server</span></span><br/> | <span data-ttu-id="77c5e-162">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="77c5e-162">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="77c5e-163">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="77c5e-163">End of client support</span></span><br/>    | <span data-ttu-id="77c5e-164">Windows XP</span><span class="sxs-lookup"><span data-stu-id="77c5e-164">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="77c5e-165">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="77c5e-165">End of server support</span></span><br/>    | <span data-ttu-id="77c5e-166">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="77c5e-166">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="77c5e-167">Header</span><span class="sxs-lookup"><span data-stu-id="77c5e-167">Header</span></span><br/>                   | <dl> <span data-ttu-id="77c5e-168"><dt>Rassapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="77c5e-168"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77c5e-169">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77c5e-169">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77c5e-170">Remote Zugriffs Dienst (RAS) (Übersicht)</span><span class="sxs-lookup"><span data-stu-id="77c5e-170">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="77c5e-171">RAS-Server-Verwaltungsstrukturen</span><span class="sxs-lookup"><span data-stu-id="77c5e-171">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="77c5e-172">**RAS- \_ Parameter**</span><span class="sxs-lookup"><span data-stu-id="77c5e-172">**RAS\_PARAMETERS**</span></span>](ras-parameters-str.md)
</dt> <dt>

[<span data-ttu-id="77c5e-173">**RAS- \_ Port \_ 0**</span><span class="sxs-lookup"><span data-stu-id="77c5e-173">**RAS\_PORT\_0**</span></span>](ras-port-0-str.md)
</dt> <dt>

[<span data-ttu-id="77c5e-174">**RAS- \_ Port \_ Statistik**</span><span class="sxs-lookup"><span data-stu-id="77c5e-174">**RAS\_PORT\_STATISTICS**</span></span>](ras-port-statistics-str.md)
</dt> <dt>

[<span data-ttu-id="77c5e-175">**Ergebnis der RAS- \_ PPP- \_ Projektion \_**</span><span class="sxs-lookup"><span data-stu-id="77c5e-175">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="77c5e-176">**Rasadminakzeptnewconnection**</span><span class="sxs-lookup"><span data-stu-id="77c5e-176">**RasAdminAcceptNewConnection**</span></span>](rasadminacceptnewconnection.md)
</dt> <dt>

[<span data-ttu-id="77c5e-177">**Rasadminconnectionhangupnotification**</span><span class="sxs-lookup"><span data-stu-id="77c5e-177">**RasAdminConnectionHangupNotification**</span></span>](rasadminconnectionhangupnotification.md)
</dt> <dt>

[<span data-ttu-id="77c5e-178">**Rasadminportgetinfo**</span><span class="sxs-lookup"><span data-stu-id="77c5e-178">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





