---
description: Legt die IPX-Netzwerk Nummer/-Frame Paare für diesen Netzwerkadapter fest.
ms.assetid: 8190564f-7d9f-4b05-9949-2e732ce36dba
ms.tgt_platform: multiple
title: Die Methode "setxframetypetworkpairs" der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXFrameTypeNetworkPairs
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: e4d53ec7b5600a767505e517a02fbf87b5a43d13
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104127472"
---
# <a name="setipxframetypenetworkpairs-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="7a010-103">Die Methode "setxframetypetworkpaars" der Win32- \_ Klasse "networkadapterconfiguration"</span><span class="sxs-lookup"><span data-stu-id="7a010-103">SetIPXFrameTypeNetworkPairs method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="7a010-104">Legt die IPX-Netzwerk Nummer/-Frame Paare für diesen Netzwerkadapter fest.</span><span class="sxs-lookup"><span data-stu-id="7a010-104">Sets the Internetworking Packet Exchange (IPX) network number/frame pairs for this network adapter.</span></span>

<span data-ttu-id="7a010-105">Windows 2000 und Windows NT 3,51 und höher verwenden eine IPX-Netzwerk Nummer für Routing Zwecke.</span><span class="sxs-lookup"><span data-stu-id="7a010-105">Windows 2000 and Windows NT 3.51 and higher use an IPX network number for routing purposes.</span></span> <span data-ttu-id="7a010-106">Sie wird den einzelnen konfigurierten Frame Typen/Netzwerkadaptern auf dem Computersystem zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7a010-106">It is assigned to each configured frame type/network adapter combination on your computer system.</span></span> <span data-ttu-id="7a010-107">Diese Zahl wird manchmal auch als "externe Netzwerk Nummer" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7a010-107">This number is sometimes referred to as the "external network number."</span></span> <span data-ttu-id="7a010-108">Er muss für jedes Netzwerksegment eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7a010-108">It must be unique for each network segment.</span></span> <span data-ttu-id="7a010-109">Wenn der Frame-Typ auf "Auto" festgelegt ist, muss die Netzwerk Nummer 0 (null) lauten.</span><span class="sxs-lookup"><span data-stu-id="7a010-109">If the frame type is set to AUTO, the network number should to zero.</span></span>

## <a name="syntax"></a><span data-ttu-id="7a010-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="7a010-110">Syntax</span></span>


```mof
uint32 SetIPXFrameTypeNetworkPairs(
  [in] string IPXNetworkNumber[],
  [in] uint32 IPXFrameType[]
);
```



## <a name="parameters"></a><span data-ttu-id="7a010-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7a010-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7a010-112">*IPXNetworkNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a010-112">*IPXNetworkNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a010-113">Ein Array von Zeichen, die einen Adapter im Computersystem eindeutig identifizieren.</span><span class="sxs-lookup"><span data-stu-id="7a010-113">An array of characters that uniquely identify an adapter on the computer system.</span></span> <span data-ttu-id="7a010-114">Der IPX/SPX-kompatible Transport (NetWare Link) in Windows 2000 und Windows NT 3,51 oder höher verwendet zwei unterschiedliche Arten von Netzwerk Nummern.</span><span class="sxs-lookup"><span data-stu-id="7a010-114">The NetWare Link (NWLink) IPX/SPX-compatible transport in Windows 2000 and Windows NT 3.51 or higher, uses two different types of network numbers.</span></span> <span data-ttu-id="7a010-115">Diese Zahl wird mitunter auch als externe Netzwerk Nummer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7a010-115">This number is sometimes referred to as the External Network Number.</span></span> <span data-ttu-id="7a010-116">Er muss für jedes Netzwerksegment eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="7a010-116">It must be unique for each network segment.</span></span> <span data-ttu-id="7a010-117">Die Werte in dieser Zeichen folgen Liste müssen über einen entsprechenden Wert im IPXFrameType-Parameter verfügen, der den für dieses Netzwerk verwendeten Pakettyp identifiziert.</span><span class="sxs-lookup"><span data-stu-id="7a010-117">The values in this string list must have a corresponding value in the IPXFrameType parameter identifying the packet frame type used for this network.</span></span>

</dd> <dt>

<span data-ttu-id="7a010-118">*IPXFrameType* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="7a010-118">*IPXFrameType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7a010-119">Ein ganzzahliges Array von Frame-typbezeichgern.</span><span class="sxs-lookup"><span data-stu-id="7a010-119">An integer array of frame type identifiers.</span></span> <span data-ttu-id="7a010-120">Die Werte in diesem Array entsprechen den Elementen im *IPXNetworkNumber* -Parameter.</span><span class="sxs-lookup"><span data-stu-id="7a010-120">The values in this array correspond to the elements in the *IPXNetworkNumber* parameter.</span></span>

<dt>

<span id="Ethernet_II"></span><span id="ethernet_ii"></span><span id="ETHERNET_II"></span>

<span data-ttu-id="7a010-121">**Ethernet II** (0)</span><span class="sxs-lookup"><span data-stu-id="7a010-121">**Ethernet II** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="7a010-122">**Ethernet 802,3** (1)</span><span class="sxs-lookup"><span data-stu-id="7a010-122">**Ethernet 802.3** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_802.2"></span><span id="ethernet_802.2"></span><span id="ETHERNET_802.2"></span>

<span data-ttu-id="7a010-123">**Ethernet 802,2** (2)</span><span class="sxs-lookup"><span data-stu-id="7a010-123">**Ethernet 802.2** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_SNAP"></span><span id="ethernet_snap"></span><span id="ETHERNET_SNAP"></span>

<span data-ttu-id="7a010-124">**Ethernet-Snap** (3)</span><span class="sxs-lookup"><span data-stu-id="7a010-124">**Ethernet SNAP** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="AUTO"></span><span id="auto"></span>

<span data-ttu-id="7a010-125">**Auto** (255)</span><span class="sxs-lookup"><span data-stu-id="7a010-125">**AUTO** (255)</span></span>


<span data-ttu-id="7a010-126"></dt> <dd></dd> </dl> </dd> </dl></span><span class="sxs-lookup"><span data-stu-id="7a010-126"></dt> <dd></dd> </dl> </dd> </dl></span></span>

## <a name="return-value"></a><span data-ttu-id="7a010-127">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7a010-127">Return value</span></span>

<dl> <dt>

<span data-ttu-id="7a010-128">**Erfolgreicher Abschluss, kein Neustart erforderlich** (0)</span><span class="sxs-lookup"><span data-stu-id="7a010-128">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-129">**Erfolgreicher Abschluss, Neustart erforderlich** (1)</span><span class="sxs-lookup"><span data-stu-id="7a010-129">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-130">**Methode wird auf dieser Plattform nicht unterstützt** (64).</span><span class="sxs-lookup"><span data-stu-id="7a010-130">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-131">**Unbekannter Fehler** (65).</span><span class="sxs-lookup"><span data-stu-id="7a010-131">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-132">**Ungültige Subnetzmaske** (66).</span><span class="sxs-lookup"><span data-stu-id="7a010-132">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-133">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde** (67).</span><span class="sxs-lookup"><span data-stu-id="7a010-133">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-134">**Ungültiger Eingabeparameter** (68)</span><span class="sxs-lookup"><span data-stu-id="7a010-134">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-135">**Es wurden mehr als 5 Gateways angegeben** (69).</span><span class="sxs-lookup"><span data-stu-id="7a010-135">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-136">**Ungültige IP-Adresse** (70)</span><span class="sxs-lookup"><span data-stu-id="7a010-136">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-137">**Ungültige Gateway-IP-Adresse** (71)</span><span class="sxs-lookup"><span data-stu-id="7a010-137">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-138">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen** (72).</span><span class="sxs-lookup"><span data-stu-id="7a010-138">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-139">**Ungültiger Domänen Name** (73).</span><span class="sxs-lookup"><span data-stu-id="7a010-139">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-140">**Ungültiger Hostname** (74).</span><span class="sxs-lookup"><span data-stu-id="7a010-140">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-141">**Kein primärer/sekundärer WINS-Server definiert** (75)</span><span class="sxs-lookup"><span data-stu-id="7a010-141">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-142">**Ungültige Datei** (76)</span><span class="sxs-lookup"><span data-stu-id="7a010-142">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-143">**Ungültiger Systempfad** (77).</span><span class="sxs-lookup"><span data-stu-id="7a010-143">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-144">Fehler beim **Kopieren der Datei** (78).</span><span class="sxs-lookup"><span data-stu-id="7a010-144">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-145">**Ungültiger Sicherheitsparameter** (79).</span><span class="sxs-lookup"><span data-stu-id="7a010-145">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-146">Der **TCP/IP-Dienst kann nicht konfiguriert** werden (80).</span><span class="sxs-lookup"><span data-stu-id="7a010-146">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-147">**DHCP-Dienst kann nicht konfiguriert** werden (81).</span><span class="sxs-lookup"><span data-stu-id="7a010-147">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-148">**DHCP-Lease kann nicht erneuert** werden (82).</span><span class="sxs-lookup"><span data-stu-id="7a010-148">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-149">**DHCP-Lease kann nicht frei** gegeben werden (83).</span><span class="sxs-lookup"><span data-stu-id="7a010-149">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-150">Die **IP ist auf dem Adapter nicht aktiviert** (84).</span><span class="sxs-lookup"><span data-stu-id="7a010-150">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-151">**IPX ist auf dem Adapter nicht aktiviert** (85).</span><span class="sxs-lookup"><span data-stu-id="7a010-151">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-152">**Fehler bei Frame/Netzwerk Nummer** (86)</span><span class="sxs-lookup"><span data-stu-id="7a010-152">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-153">**Ungültiger Frame-Typ** (87).</span><span class="sxs-lookup"><span data-stu-id="7a010-153">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-154">**Ungültige Netzwerk Nummer** (88).</span><span class="sxs-lookup"><span data-stu-id="7a010-154">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-155">**Doppelte Netzwerk Nummer** (89)</span><span class="sxs-lookup"><span data-stu-id="7a010-155">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-156">**Parameter außerhalb des** gültigen Bereichs (90)</span><span class="sxs-lookup"><span data-stu-id="7a010-156">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-157">**Zugriff verweigert** (91)</span><span class="sxs-lookup"><span data-stu-id="7a010-157">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-158">**Nicht** genügend Arbeitsspeicher (92)</span><span class="sxs-lookup"><span data-stu-id="7a010-158">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-159">**Bereits vorhanden** (93)</span><span class="sxs-lookup"><span data-stu-id="7a010-159">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-160">Der **Pfad, die Datei oder das Objekt wurde nicht gefunden** (94).</span><span class="sxs-lookup"><span data-stu-id="7a010-160">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-161">Der **Dienst kann nicht benachrichtigt** werden (95).</span><span class="sxs-lookup"><span data-stu-id="7a010-161">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-162">Der **DNS-Dienst kann nicht benachrichtigt** werden (96).</span><span class="sxs-lookup"><span data-stu-id="7a010-162">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-163">**Schnittstelle nicht konfigurierbar** (97)</span><span class="sxs-lookup"><span data-stu-id="7a010-163">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-164">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden** (98).</span><span class="sxs-lookup"><span data-stu-id="7a010-164">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-165">**DHCP ist auf dem Adapter nicht aktiviert** (100).</span><span class="sxs-lookup"><span data-stu-id="7a010-165">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="7a010-166">**Sonstige** (101 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="7a010-166">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="7a010-167">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7a010-167">Requirements</span></span>



| <span data-ttu-id="7a010-168">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7a010-168">Requirement</span></span> | <span data-ttu-id="7a010-169">Wert</span><span class="sxs-lookup"><span data-stu-id="7a010-169">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7a010-170">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7a010-170">Minimum supported client</span></span><br/> | <span data-ttu-id="7a010-171">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7a010-171">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7a010-172">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7a010-172">Minimum supported server</span></span><br/> | <span data-ttu-id="7a010-173">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7a010-173">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7a010-174">Namespace</span><span class="sxs-lookup"><span data-stu-id="7a010-174">Namespace</span></span><br/>                | <span data-ttu-id="7a010-175">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="7a010-175">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7a010-176">MOF</span><span class="sxs-lookup"><span data-stu-id="7a010-176">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7a010-177"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="7a010-177"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7a010-178">DLL</span><span class="sxs-lookup"><span data-stu-id="7a010-178">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7a010-179"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7a010-179"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7a010-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7a010-180">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7a010-181">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="7a010-181">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




