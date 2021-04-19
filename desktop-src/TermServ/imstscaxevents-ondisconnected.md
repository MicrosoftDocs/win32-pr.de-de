---
title: Imstscaxevents (ongetrennte Methode)
description: Wird aufgerufen, wenn das Client Steuerelement vom Remotedesktop-Sitzungshost Server (RD-Sitzungshost) getrennt wurde.
ms.assetid: f01086e7-61d1-41df-ba0a-4eecfa57d492
ms.tgt_platform: multiple
keywords:
- Ongetrennte Methode Remotedesktopdienste
- Ongetrennte Methode Remotedesktopdienste, imstscaxevents-Schnittstelle
- Imstscaxevents-Schnittstelle Remotedesktopdienste, ongetrennte Methode
topic_type:
- apiref
api_name:
- IMsTscAxEvents.OnDisconnected
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 372ad98c73b1b0e90753891e01e46c61a78c23dd
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "106342221"
---
# <a name="imstscaxeventsondisconnected-method"></a><span data-ttu-id="61607-106">Imstscaxevents:: ongetrennte-Methode</span><span class="sxs-lookup"><span data-stu-id="61607-106">IMsTscAxEvents::OnDisconnected method</span></span>

<span data-ttu-id="61607-107">Wird aufgerufen, wenn das Client Steuerelement vom Remotedesktop-Sitzungshost Server (RD-Sitzungshost) getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="61607-107">Called when the client control has been disconnected from the Remote Desktop Session Host (RD Session Host) server.</span></span>

## <a name="syntax"></a><span data-ttu-id="61607-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="61607-108">Syntax</span></span>


```C++
void OnDisconnected(
  [in] long discReason
);
```



## <a name="parameters"></a><span data-ttu-id="61607-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="61607-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61607-110">*discreason* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="61607-110">*discReason* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="61607-111">Gibt den Grund für die Trennung der Verbindung an.</span><span class="sxs-lookup"><span data-stu-id="61607-111">Specifies the reason for the disconnection.</span></span> <span data-ttu-id="61607-112">Im folgenden finden Sie eine Liste der Fehlercodes.</span><span class="sxs-lookup"><span data-stu-id="61607-112">The following is a list of error codes.</span></span> <span data-ttu-id="61607-113">Einige dieser Fehlercodes sind in winkred. h definiert.</span><span class="sxs-lookup"><span data-stu-id="61607-113">Some of these error codes are defined in Wincred.h.</span></span>

<dt>

<span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>

<span data-ttu-id="61607-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnecbunonatclientwinsockf dclose** (2308 (0x904))</span><span class="sxs-lookup"><span data-stu-id="61607-114"><span id="disconnectReasonAtClientWinsockFDCLOSE"></span><span id="disconnectreasonatclientwinsockfdclose"></span><span id="DISCONNECTREASONATCLIENTWINSOCKFDCLOSE"></span>**disconnectReasonAtClientWinsockFDCLOSE** (2308 (0x904))</span></span>


</dt> <dd>

<span data-ttu-id="61607-115">Socket geschlossen.</span><span class="sxs-lookup"><span data-stu-id="61607-115">Socket closed.</span></span>

</dd> <dt>

<span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>

<span data-ttu-id="61607-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectybyserver** (3 (0x3))</span><span class="sxs-lookup"><span data-stu-id="61607-116"><span id="disconnectReasonByServer"></span><span id="disconnectreasonbyserver"></span><span id="DISCONNECTREASONBYSERVER"></span>**disconnectReasonByServer** (3 (0x3))</span></span>


</dt> <dd>

<span data-ttu-id="61607-117">Remote Unterbrechung durch den Server.</span><span class="sxs-lookup"><span data-stu-id="61607-117">Remote disconnection by server.</span></span> <span data-ttu-id="61607-118">Dies ist kein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="61607-118">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>

<span data-ttu-id="61607-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xc08))</span><span class="sxs-lookup"><span data-stu-id="61607-119"><span id="disconnectReasonClientDecompressionError"></span><span id="disconnectreasonclientdecompressionerror"></span><span id="DISCONNECTREASONCLIENTDECOMPRESSIONERROR"></span>**disconnectReasonClientDecompressionError** (3080 (0xC08))</span></span>


</dt> <dd>

<span data-ttu-id="61607-120">Fehler beim Komprimieren.</span><span class="sxs-lookup"><span data-stu-id="61607-120">Decompression error.</span></span>

</dd> <dt>

<span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>

<span data-ttu-id="61607-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectiononconnectiontimedout** (264 (0x108))</span><span class="sxs-lookup"><span data-stu-id="61607-121"><span id="disconnectReasonConnectionTimedOut"></span><span id="disconnectreasonconnectiontimedout"></span><span id="DISCONNECTREASONCONNECTIONTIMEDOUT"></span>**disconnectReasonConnectionTimedOut** (264 (0x108))</span></span>


</dt> <dd>

<span data-ttu-id="61607-122">„Verbindung wegen Zeitüberschreitung abgebrochen.“</span><span class="sxs-lookup"><span data-stu-id="61607-122">Connection timed out.</span></span>

</dd> <dt>

<span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>

<span data-ttu-id="61607-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnection-Fehler** (3078 (0xc06))</span><span class="sxs-lookup"><span data-stu-id="61607-123"><span id="disconnectReasonDecryptionError"></span><span id="disconnectreasondecryptionerror"></span><span id="DISCONNECTREASONDECRYPTIONERROR"></span>**disconnectReasonDecryptionError** (3078 (0xC06))</span></span>


</dt> <dd>

<span data-ttu-id="61607-124">Entschlüsselungs Fehler.</span><span class="sxs-lookup"><span data-stu-id="61607-124">Decryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>

<span data-ttu-id="61607-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnecbunondnslookupfailed** (260 (0x104))</span><span class="sxs-lookup"><span data-stu-id="61607-125"><span id="disconnectReasonDNSLookupFailed"></span><span id="disconnectreasondnslookupfailed"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED"></span>**disconnectReasonDNSLookupFailed** (260 (0x104))</span></span>


</dt> <dd>

<span data-ttu-id="61607-126">Fehler bei der DNS-Namenssuche.</span><span class="sxs-lookup"><span data-stu-id="61607-126">DNS name lookup failure.</span></span>

</dd> <dt>

<span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>

<span data-ttu-id="61607-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))</span><span class="sxs-lookup"><span data-stu-id="61607-127"><span id="disconnectReasonDNSLookupFailed2"></span><span id="disconnectreasondnslookupfailed2"></span><span id="DISCONNECTREASONDNSLOOKUPFAILED2"></span>**disconnectReasonDNSLookupFailed2** (1288 (0x508))</span></span>


</dt> <dd>

<span data-ttu-id="61607-128">Fehler bei der DNS-Suche.</span><span class="sxs-lookup"><span data-stu-id="61607-128">DNS lookup failed.</span></span>

</dd> <dt>

<span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>

<span data-ttu-id="61607-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnection-Verschlüsselungsfehler** (2822 (0xb06))</span><span class="sxs-lookup"><span data-stu-id="61607-129"><span id="disconnectReasonEncryptionError"></span><span id="disconnectreasonencryptionerror"></span><span id="DISCONNECTREASONENCRYPTIONERROR"></span>**disconnectReasonEncryptionError** (2822 (0xB06))</span></span>


</dt> <dd>

<span data-ttu-id="61607-130">Verschlüsselungs Fehler.</span><span class="sxs-lookup"><span data-stu-id="61607-130">Encryption error.</span></span>

</dd> <dt>

<span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>

<span data-ttu-id="61607-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnecbunongethostbynamefailed** (1540 (0x604))</span><span class="sxs-lookup"><span data-stu-id="61607-131"><span id="disconnectReasonGetHostByNameFailed"></span><span id="disconnectreasongethostbynamefailed"></span><span id="DISCONNECTREASONGETHOSTBYNAMEFAILED"></span>**disconnectReasonGetHostByNameFailed** (1540 (0x604))</span></span>


</dt> <dd>

<span data-ttu-id="61607-132">Fehler beim Aufrufen von " [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) " für Windows Sockets.</span><span class="sxs-lookup"><span data-stu-id="61607-132">Windows Sockets [**gethostbyname**](/windows/desktop/api/wsipv6ok/nf-wsipv6ok-gethostbyname) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>

<span data-ttu-id="61607-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnecationhostnotfound** (520 (0x208))</span><span class="sxs-lookup"><span data-stu-id="61607-133"><span id="disconnectReasonHostNotFound"></span><span id="disconnectreasonhostnotfound"></span><span id="DISCONNECTREASONHOSTNOTFOUND"></span>**disconnectReasonHostNotFound** (520 (0x208))</span></span>


</dt> <dd>

<span data-ttu-id="61607-134">Fehler "Host nicht gefunden".</span><span class="sxs-lookup"><span data-stu-id="61607-134">Host not found error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>

<span data-ttu-id="61607-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconneconioninternalerror** (1032 (0x408))</span><span class="sxs-lookup"><span data-stu-id="61607-135"><span id="disconnectReasonInternalError"></span><span id="disconnectreasoninternalerror"></span><span id="DISCONNECTREASONINTERNALERROR"></span>**disconnectReasonInternalError** (1032 (0x408))</span></span>


</dt> <dd>

<span data-ttu-id="61607-136">Interner Fehler.</span><span class="sxs-lookup"><span data-stu-id="61607-136">Internal error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>

<span data-ttu-id="61607-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconneconioninternalsecurityerror** (2310 (0x906))</span><span class="sxs-lookup"><span data-stu-id="61607-137"><span id="disconnectReasonInternalSecurityError"></span><span id="disconnectreasoninternalsecurityerror"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR"></span>**disconnectReasonInternalSecurityError** (2310 (0x906))</span></span>


</dt> <dd>

<span data-ttu-id="61607-138">Interner Sicherheitsfehler.</span><span class="sxs-lookup"><span data-stu-id="61607-138">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>

<span data-ttu-id="61607-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xa06))</span><span class="sxs-lookup"><span data-stu-id="61607-139"><span id="disconnectReasonInternalSecurityError2"></span><span id="disconnectreasoninternalsecurityerror2"></span><span id="DISCONNECTREASONINTERNALSECURITYERROR2"></span>**disconnectReasonInternalSecurityError2** (2566 (0xA06))</span></span>


</dt> <dd>

<span data-ttu-id="61607-140">Interner Sicherheitsfehler.</span><span class="sxs-lookup"><span data-stu-id="61607-140">Internal security error.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>

<span data-ttu-id="61607-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectionuninvalidencryption** (1286 (0x506))</span><span class="sxs-lookup"><span data-stu-id="61607-141"><span id="disconnectReasonInvalidEncryption"></span><span id="disconnectreasoninvalidencryption"></span><span id="DISCONNECTREASONINVALIDENCRYPTION"></span>**disconnectReasonInvalidEncryption** (1286 (0x506))</span></span>


</dt> <dd>

<span data-ttu-id="61607-142">Die angegebene Verschlüsselungsmethode ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="61607-142">The encryption method specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>

<span data-ttu-id="61607-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectypinvalidip** (2052 (0x804))</span><span class="sxs-lookup"><span data-stu-id="61607-143"><span id="disconnectReasonInvalidIP"></span><span id="disconnectreasoninvalidip"></span><span id="DISCONNECTREASONINVALIDIP"></span>**disconnectReasonInvalidIP** (2052 (0x804))</span></span>


</dt> <dd>

<span data-ttu-id="61607-144">Ungültige IP-Adresse angegeben.</span><span class="sxs-lookup"><span data-stu-id="61607-144">Bad IP address specified.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>

<span data-ttu-id="61607-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectypinvalidserversecurityinfo** (1542 (0x606))</span><span class="sxs-lookup"><span data-stu-id="61607-145"><span id="disconnectReasonInvalidServerSecurityInfo"></span><span id="disconnectreasoninvalidserversecurityinfo"></span><span id="DISCONNECTREASONINVALIDSERVERSECURITYINFO"></span>**disconnectReasonInvalidServerSecurityInfo** (1542 (0x606))</span></span>


</dt> <dd>

<span data-ttu-id="61607-146">Die Server Sicherheitsdaten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="61607-146">Server security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>

<span data-ttu-id="61607-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectypinvalidsecuritydata** (1030 (0x406))</span><span class="sxs-lookup"><span data-stu-id="61607-147"><span id="disconnectReasonInvalidSecurityData"></span><span id="disconnectreasoninvalidsecuritydata"></span><span id="DISCONNECTREASONINVALIDSECURITYDATA"></span>**disconnectReasonInvalidSecurityData** (1030 (0x406))</span></span>


</dt> <dd>

<span data-ttu-id="61607-148">Die Sicherheitsdaten sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="61607-148">Security data is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>

<span data-ttu-id="61607-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectypinvalidipaddr** (776 (0x308))</span><span class="sxs-lookup"><span data-stu-id="61607-149"><span id="disconnectReasonInvalidIPAddr"></span><span id="disconnectreasoninvalidipaddr"></span><span id="DISCONNECTREASONINVALIDIPADDR"></span>**disconnectReasonInvalidIPAddr** (776 (0x308))</span></span>


</dt> <dd>

<span data-ttu-id="61607-150">Die angegebene IP-Adresse ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="61607-150">The IP address specified is not valid.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>

<span data-ttu-id="61607-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconneconionlicensingfailed** (2056 (0x808))</span><span class="sxs-lookup"><span data-stu-id="61607-151"><span id="disconnectReasonLicensingFailed"></span><span id="disconnectreasonlicensingfailed"></span><span id="DISCONNECTREASONLICENSINGFAILED"></span>**disconnectReasonLicensingFailed** (2056 (0x808))</span></span>


</dt> <dd>

<span data-ttu-id="61607-152">Fehler bei der Lizenz Aushandlung.</span><span class="sxs-lookup"><span data-stu-id="61607-152">License negotiation failed.</span></span>

</dd> <dt>

<span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>

<span data-ttu-id="61607-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnecoutonlicensingtimeout** (2312 (0x908))</span><span class="sxs-lookup"><span data-stu-id="61607-153"><span id="disconnectReasonLicensingTimeout"></span><span id="disconnectreasonlicensingtimeout"></span><span id="DISCONNECTREASONLICENSINGTIMEOUT"></span>**disconnectReasonLicensingTimeout** (2312 (0x908))</span></span>


</dt> <dd>

<span data-ttu-id="61607-154">Lizenzierungs Timeout.</span><span class="sxs-lookup"><span data-stu-id="61607-154">Licensing time-out.</span></span>

</dd> <dt>

<span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>

<span data-ttu-id="61607-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnecbunonlocalnoterror** (1 (0x1))</span><span class="sxs-lookup"><span data-stu-id="61607-155"><span id="disconnectReasonLocalNotError"></span><span id="disconnectreasonlocalnoterror"></span><span id="DISCONNECTREASONLOCALNOTERROR"></span>**disconnectReasonLocalNotError** (1 (0x1))</span></span>


</dt> <dd>

<span data-ttu-id="61607-156">Lokale Trennung.</span><span class="sxs-lookup"><span data-stu-id="61607-156">Local disconnection.</span></span> <span data-ttu-id="61607-157">Dies ist kein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="61607-157">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>

<span data-ttu-id="61607-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnecbunonnoinfo** (0 (0x0))</span><span class="sxs-lookup"><span data-stu-id="61607-158"><span id="disconnectReasonNoInfo"></span><span id="disconnectreasonnoinfo"></span><span id="DISCONNECTREASONNOINFO"></span>**disconnectReasonNoInfo** (0 (0x0))</span></span>


</dt> <dd>

<span data-ttu-id="61607-159">Es sind keine Informationen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="61607-159">No information is available.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>

<span data-ttu-id="61607-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconneconionouto-Memory** (262 (0x106))</span><span class="sxs-lookup"><span data-stu-id="61607-160"><span id="disconnectReasonOutOfMemory"></span><span id="disconnectreasonoutofmemory"></span><span id="DISCONNECTREASONOUTOFMEMORY"></span>**disconnectReasonOutOfMemory** (262 (0x106))</span></span>


</dt> <dd>

<span data-ttu-id="61607-161">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="61607-161">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>

<span data-ttu-id="61607-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))</span><span class="sxs-lookup"><span data-stu-id="61607-162"><span id="disconnectReasonOutOfMemory2"></span><span id="disconnectreasonoutofmemory2"></span><span id="DISCONNECTREASONOUTOFMEMORY2"></span>**disconnectReasonOutOfMemory2** (518 (0x206))</span></span>


</dt> <dd>

<span data-ttu-id="61607-163">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="61607-163">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>

<span data-ttu-id="61607-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))</span><span class="sxs-lookup"><span data-stu-id="61607-164"><span id="disconnectReasonOutOfMemory3"></span><span id="disconnectreasonoutofmemory3"></span><span id="DISCONNECTREASONOUTOFMEMORY3"></span>**disconnectReasonOutOfMemory3** (774 (0x306))</span></span>


</dt> <dd>

<span data-ttu-id="61607-165">Nicht genügend Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="61607-165">Out of memory.</span></span>

</dd> <dt>

<span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>

<span data-ttu-id="61607-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectyremotebyuser** (2 (0x2))</span><span class="sxs-lookup"><span data-stu-id="61607-166"><span id="disconnectReasonRemoteByUser"></span><span id="disconnectreasonremotebyuser"></span><span id="DISCONNECTREASONREMOTEBYUSER"></span>**disconnectReasonRemoteByUser** (2 (0x2))</span></span>


</dt> <dd>

<span data-ttu-id="61607-167">Remote Unterbrechung durch Benutzer.</span><span class="sxs-lookup"><span data-stu-id="61607-167">Remote disconnection by user.</span></span> <span data-ttu-id="61607-168">Dies ist kein Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="61607-168">This is not an error code.</span></span>

</dd> <dt>

<span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>

<span data-ttu-id="61607-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnecbunonservercertificateunpackerr** (1798 (0x706))</span><span class="sxs-lookup"><span data-stu-id="61607-169"><span id="disconnectReasonServerCertificateUnpackErr"></span><span id="disconnectreasonservercertificateunpackerr"></span><span id="DISCONNECTREASONSERVERCERTIFICATEUNPACKERR"></span>**disconnectReasonServerCertificateUnpackErr** (1798 (0x706))</span></span>


</dt> <dd>

<span data-ttu-id="61607-170">Fehler beim Entpacken des Serverzertifikats.</span><span class="sxs-lookup"><span data-stu-id="61607-170">Failed to unpack server certificate.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>

<span data-ttu-id="61607-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnecbunonsocketconnectfailed** (516 (0x204))</span><span class="sxs-lookup"><span data-stu-id="61607-171"><span id="disconnectReasonSocketConnectFailed"></span><span id="disconnectreasonsocketconnectfailed"></span><span id="DISCONNECTREASONSOCKETCONNECTFAILED"></span>**disconnectReasonSocketConnectFailed** (516 (0x204))</span></span>


</dt> <dd>

<span data-ttu-id="61607-172">Fehler bei Windows Sockets [**Connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) .</span><span class="sxs-lookup"><span data-stu-id="61607-172">Windows Sockets [**connect**](/windows/desktop/api/winsock2/nf-winsock2-connect) failed.</span></span>

</dd> <dt>

<span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>

<span data-ttu-id="61607-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnecbunonsocketrecvfailed** (1028 (0x404))</span><span class="sxs-lookup"><span data-stu-id="61607-173"><span id="disconnectReasonSocketRecvFailed"></span><span id="disconnectreasonsocketrecvfailed"></span><span id="DISCONNECTREASONSOCKETRECVFAILED"></span>**disconnectReasonSocketRecvFailed** (1028 (0x404))</span></span>


</dt> <dd>

<span data-ttu-id="61607-174">Fehler beim Windows Sockets [**empfangener**](/windows/desktop/api/winsock/nf-winsock-recv) -Rückruf.</span><span class="sxs-lookup"><span data-stu-id="61607-174">Windows Sockets [**recv**](/windows/desktop/api/winsock/nf-winsock-recv) call failed.</span></span>

</dd> <dt>

<span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>

<span data-ttu-id="61607-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnecsurontimeoudeccurrred** (1796 (0x704))</span><span class="sxs-lookup"><span data-stu-id="61607-175"><span id="disconnectReasonTimeoutOccurred"></span><span id="disconnectreasontimeoutoccurred"></span><span id="DISCONNECTREASONTIMEOUTOCCURRED"></span>**disconnectReasonTimeoutOccurred** (1796 (0x704))</span></span>


</dt> <dd>

<span data-ttu-id="61607-176">Das Timeout ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="61607-176">Time-out occurred.</span></span>

</dd> <dt>

<span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>

<span data-ttu-id="61607-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconneclistontimererror** (1544 (0x608))</span><span class="sxs-lookup"><span data-stu-id="61607-177"><span id="disconnectReasonTimerError"></span><span id="disconnectreasontimererror"></span><span id="DISCONNECTREASONTIMERERROR"></span>**disconnectReasonTimerError** (1544 (0x608))</span></span>


</dt> <dd>

<span data-ttu-id="61607-178">Interner Timer-Fehler.</span><span class="sxs-lookup"><span data-stu-id="61607-178">Internal timer error.</span></span>

</dd> <dt>

<span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>

<span data-ttu-id="61607-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnecbunonwinsocksendfailed** (772 (0x304))</span><span class="sxs-lookup"><span data-stu-id="61607-179"><span id="disconnectReasonWinsockSendFailed"></span><span id="disconnectreasonwinsocksendfailed"></span><span id="DISCONNECTREASONWINSOCKSENDFAILED"></span>**disconnectReasonWinsockSendFailed** (772 (0x304))</span></span>


</dt> <dd>

<span data-ttu-id="61607-180">Fehler beim [**senden**](/windows/desktop/api/winsock2/nf-winsock2-send) von Windows-Sockets</span><span class="sxs-lookup"><span data-stu-id="61607-180">Windows Sockets [**send**](/windows/desktop/api/winsock2/nf-winsock2-send) call failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>

<span data-ttu-id="61607-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL \_ Err- \_ Konto \_ deaktiviert** (2823 (0xb07))</span><span class="sxs-lookup"><span data-stu-id="61607-181"><span id="SSL_ERR_ACCOUNT_DISABLED"></span><span id="ssl_err_account_disabled"></span>**SSL\_ERR\_ACCOUNT\_DISABLED** (2823 (0xB07))</span></span>


</dt> <dd>

<span data-ttu-id="61607-182">Das Konto ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="61607-182">The account is disabled.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>

<span data-ttu-id="61607-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL \_ Das Err- \_ Konto ist \_ abgelaufen** (3591 (0xe07)).</span><span class="sxs-lookup"><span data-stu-id="61607-183"><span id="SSL_ERR_ACCOUNT_EXPIRED"></span><span id="ssl_err_account_expired"></span>**SSL\_ERR\_ACCOUNT\_EXPIRED** (3591 (0xE07))</span></span>


</dt> <dd>

<span data-ttu-id="61607-184">Das Konto ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="61607-184">The account is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>

<span data-ttu-id="61607-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL \_ Err- \_ Konto \_ gesperrt \_** (3335 (0xd07))</span><span class="sxs-lookup"><span data-stu-id="61607-185"><span id="SSL_ERR_ACCOUNT_LOCKED_OUT"></span><span id="ssl_err_account_locked_out"></span>**SSL\_ERR\_ACCOUNT\_LOCKED\_OUT** (3335 (0xD07))</span></span>


</dt> <dd>

<span data-ttu-id="61607-186">Das Konto ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="61607-186">The account is locked out.</span></span>

</dd> <dt>

<span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>

<span data-ttu-id="61607-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL \_ Err- \_ Konto \_ Einschränkung** (3079 (0xc07))</span><span class="sxs-lookup"><span data-stu-id="61607-187"><span id="SSL_ERR_ACCOUNT_RESTRICTION"></span><span id="ssl_err_account_restriction"></span>**SSL\_ERR\_ACCOUNT\_RESTRICTION** (3079 (0xC07))</span></span>


</dt> <dd>

<span data-ttu-id="61607-188">Das Konto ist eingeschränkt.</span><span class="sxs-lookup"><span data-stu-id="61607-188">The account is restricted.</span></span>

</dd> <dt>

<span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>

<span data-ttu-id="61607-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL \_ Das Err- \_ Zertifikat ist \_ abgelaufen** (6919 (0x1b07)).</span><span class="sxs-lookup"><span data-stu-id="61607-189"><span id="SSL_ERR_CERT_EXPIRED"></span><span id="ssl_err_cert_expired"></span>**SSL\_ERR\_CERT\_EXPIRED** (6919 (0x1B07))</span></span>


</dt> <dd>

<span data-ttu-id="61607-190">Das empfangene Zertifikat ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="61607-190">The received certificate is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>

<span data-ttu-id="61607-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL \_ Err \_ - \_ Delegierungs Richtlinie** (5639 (0x1607))</span><span class="sxs-lookup"><span data-stu-id="61607-191"><span id="SSL_ERR_DELEGATION_POLICY"></span><span id="ssl_err_delegation_policy"></span>**SSL\_ERR\_DELEGATION\_POLICY** (5639 (0x1607))</span></span>


</dt> <dd>

<span data-ttu-id="61607-192">Die Richtlinie unterstützt nicht die Delegierung von Anmelde Informationen an den Zielserver.</span><span class="sxs-lookup"><span data-stu-id="61607-192">The policy does not support delegation of credentials to the target server.</span></span>

</dd> <dt>

<span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>

<span data-ttu-id="61607-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL \_ \_ \_ \_ \_ Von \_ Server erforderliches Err-** up (8455 (0x2107))</span><span class="sxs-lookup"><span data-stu-id="61607-193"><span id="SSL_ERR_FRESH_CRED_REQUIRED_BY_SERVER"></span><span id="ssl_err_fresh_cred_required_by_server"></span>**SSL\_ERR\_FRESH\_CRED\_REQUIRED\_BY\_SERVER** (8455 (0x2107))</span></span>


</dt> <dd>

<span data-ttu-id="61607-194">Die Richtlinie für die Server Authentifizierung lässt keine Verbindungsanforderungen zu, die gespeicherte Anmelde Informationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="61607-194">The server authentication policy does not allow connection requests using saved credentials.</span></span> <span data-ttu-id="61607-195">Der Benutzer muss neue Anmelde Informationen eingeben.</span><span class="sxs-lookup"><span data-stu-id="61607-195">The user must enter new credentials.</span></span>

</dd> <dt>

<span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>

<span data-ttu-id="61607-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL \_ \_ \_ Fehler** bei der ERR-Anmeldung (2055 (0x807))</span><span class="sxs-lookup"><span data-stu-id="61607-196"><span id="SSL_ERR_LOGON_FAILURE"></span><span id="ssl_err_logon_failure"></span>**SSL\_ERR\_LOGON\_FAILURE** (2055 (0x807))</span></span>


</dt> <dd>

<span data-ttu-id="61607-197">Fehler bei der Anmeldung.</span><span class="sxs-lookup"><span data-stu-id="61607-197">Login failed.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>

<span data-ttu-id="61607-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL \_ Err \_ keine \_ authentifizier Ende Zertifizierungs \_** Stelle (6151 (0x1807))</span><span class="sxs-lookup"><span data-stu-id="61607-198"><span id="SSL_ERR_NO_AUTHENTICATING_AUTHORITY"></span><span id="ssl_err_no_authenticating_authority"></span>**SSL\_ERR\_NO\_AUTHENTICATING\_AUTHORITY** (6151 (0x1807))</span></span>


</dt> <dd>

<span data-ttu-id="61607-199">Es konnte keine Autorität für die Authentifizierung kontaktiert werden.</span><span class="sxs-lookup"><span data-stu-id="61607-199">No authority could be contacted for authentication.</span></span> <span data-ttu-id="61607-200">Der Domänen Name der authentifizier enden Partei ist möglicherweise falsch, die Domäne kann nicht erreichbar sein, oder es ist ein Fehler bei der Vertrauensstellung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="61607-200">The domain name of the authenticating party could be wrong, the domain could be unreachable, or there might have been a trust relationship failure.</span></span>

</dd> <dt>

<span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>

<span data-ttu-id="61607-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL \_ Err \_ No \_ this \_ User** (2567 (0XA07))</span><span class="sxs-lookup"><span data-stu-id="61607-201"><span id="SSL_ERR_NO_SUCH_USER"></span><span id="ssl_err_no_such_user"></span>**SSL\_ERR\_NO\_SUCH\_USER** (2567 (0xA07))</span></span>


</dt> <dd>

<span data-ttu-id="61607-202">Der angegebene Benutzer hat kein Konto.</span><span class="sxs-lookup"><span data-stu-id="61607-202">The specified user has no account.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>

<span data-ttu-id="61607-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL \_ Das Err- \_ Kennwort ist \_ abgelaufen** (3847 (0xF)).</span><span class="sxs-lookup"><span data-stu-id="61607-203"><span id="SSL_ERR_PASSWORD_EXPIRED"></span><span id="ssl_err_password_expired"></span>**SSL\_ERR\_PASSWORD\_EXPIRED** (3847 (0xF07))</span></span>


</dt> <dd>

<span data-ttu-id="61607-204">Das Kennwort ist abgelaufen.</span><span class="sxs-lookup"><span data-stu-id="61607-204">The password is expired.</span></span>

</dd> <dt>

<span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>

<span data-ttu-id="61607-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL \_ Das Err- \_ Kennwort \_ muss \_ geändert** werden (4615 (0x1207)).</span><span class="sxs-lookup"><span data-stu-id="61607-205"><span id="SSL_ERR_PASSWORD_MUST_CHANGE"></span><span id="ssl_err_password_must_change"></span>**SSL\_ERR\_PASSWORD\_MUST\_CHANGE** (4615 (0x1207))</span></span>


</dt> <dd>

<span data-ttu-id="61607-206">Das Benutzer Kennwort muss geändert werden, bevor Sie sich zum ersten Mal anmelden.</span><span class="sxs-lookup"><span data-stu-id="61607-206">The user password must be changed before logging on for the first time.</span></span>

</dd> <dt>

<span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>

<span data-ttu-id="61607-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL \_ Err- \_ Richtlinie \_ \_ nur NTLM** (5895 (0x1707))</span><span class="sxs-lookup"><span data-stu-id="61607-207"><span id="SSL_ERR_POLICY_NTLM_ONLY"></span><span id="ssl_err_policy_ntlm_only"></span>**SSL\_ERR\_POLICY\_NTLM\_ONLY** (5895 (0x1707))</span></span>


</dt> <dd>

<span data-ttu-id="61607-208">Die Delegierung von Anmelde Informationen an den Zielserver ist nur zulässig, wenn eine gegenseitige Authentifizierung erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="61607-208">Delegation of credentials to the target server is not allowed unless mutual authentication has been achieved.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>

<span data-ttu-id="61607-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL \_ Err \_ Smartcard- \_ Karte \_ blockiert** (8711 (0x2207))</span><span class="sxs-lookup"><span data-stu-id="61607-209"><span id="SSL_ERR_SMARTCARD_CARD_BLOCKED"></span><span id="ssl_err_smartcard_card_blocked"></span>**SSL\_ERR\_SMARTCARD\_CARD\_BLOCKED** (8711 (0x2207))</span></span>


</dt> <dd>

<span data-ttu-id="61607-210">Die Smartcard ist blockiert.</span><span class="sxs-lookup"><span data-stu-id="61607-210">The smart card is blocked.</span></span>

</dd> <dt>

<span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>

<span data-ttu-id="61607-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL \_ \_Falsche falsche Smartcard- \_ \_ Pin** (7175 (0x1c07))</span><span class="sxs-lookup"><span data-stu-id="61607-211"><span id="SSL_ERR_SMARTCARD_WRONG_PIN"></span><span id="ssl_err_smartcard_wrong_pin"></span>**SSL\_ERR\_SMARTCARD\_WRONG\_PIN** (7175 (0x1C07))</span></span>


</dt> <dd>

<span data-ttu-id="61607-212">Der Smartcard wurde eine falsche PIN angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61607-212">An incorrect PIN was presented to the smart card.</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61607-213">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="61607-213">Return value</span></span>

<span data-ttu-id="61607-214">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="61607-214">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="61607-215">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61607-215">Remarks</span></span>

<span data-ttu-id="61607-216">Rufen Sie zum Abrufen einer Beschreibung des Trennungs Fehlers die [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) -Methode auf, und übergeben Sie Ihr den *discreason* -Parameter und die [**extendeddisconnecverrat**](imsrdpclient-extendeddisconnectreason.md) -Eigenschaft der [**imsrdpclient**](imsrdpclient-interface.md) -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="61607-216">To retrieve a description of the disconnect error, call the [**GetErrorDescription**](imsrdpclient5-geterrordescription.md) method and pass it the *discReason* parameter and the [**ExtendedDisconnectReason**](imsrdpclient-extendeddisconnectreason.md) property of the [**IMsRdpClient**](imsrdpclient-interface.md) interface.</span></span>

<span data-ttu-id="61607-217">Weitere Informationen zu Remotedesktop-Webverbindung finden Sie unter [Anforderungen für Remotedesktop-Webverbindung](requirements-for-remote-desktop-web-connection.md).</span><span class="sxs-lookup"><span data-stu-id="61607-217">For more information about Remote Desktop Web Connection, see [Requirements for Remote Desktop Web Connection](requirements-for-remote-desktop-web-connection.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61607-218">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="61607-218">Requirements</span></span>



| <span data-ttu-id="61607-219">Anforderung</span><span class="sxs-lookup"><span data-stu-id="61607-219">Requirement</span></span> | <span data-ttu-id="61607-220">Wert</span><span class="sxs-lookup"><span data-stu-id="61607-220">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="61607-221">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="61607-221">Minimum supported client</span></span><br/> | <span data-ttu-id="61607-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="61607-222">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="61607-223">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="61607-223">Minimum supported server</span></span><br/> | <span data-ttu-id="61607-224">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="61607-224">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="61607-225">Typbibliothek</span><span class="sxs-lookup"><span data-stu-id="61607-225">Type library</span></span><br/>             | <dl> <span data-ttu-id="61607-226"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61607-226"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="61607-227">DLL</span><span class="sxs-lookup"><span data-stu-id="61607-227">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61607-228"><dt>MsTscAx.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61607-228"><dt>MsTscAx.dll</dt></span></span> </dl> |
| <span data-ttu-id="61607-229">IID</span><span class="sxs-lookup"><span data-stu-id="61607-229">IID</span></span><br/>                      | <span data-ttu-id="61607-230">Imstscaxevents ist als 336d5562-efa8-482e-8cb3-c5c0fc7a7db6 definiert.</span><span class="sxs-lookup"><span data-stu-id="61607-230">IMsTscAxEvents is defined as 336d5562-efa8-482e-8cb3-c5c0fc7a7db6</span></span><br/>           |



## <a name="see-also"></a><span data-ttu-id="61607-231">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="61607-231">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61607-232">**Imstscaxevents**</span><span class="sxs-lookup"><span data-stu-id="61607-232">**IMsTscAxEvents**</span></span>](imstscaxevents-interface.md)
</dt> </dl>

 

