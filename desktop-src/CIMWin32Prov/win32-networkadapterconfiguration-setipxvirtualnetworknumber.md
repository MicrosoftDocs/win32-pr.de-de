---
description: Legt die virtuelle IPX-Netzwerk Nummer (Internetworking Packet Exchange) auf dem Zielcomputer System fest.
ms.assetid: 52064250-b94f-4dc0-bf1a-8601cd135a90
ms.tgt_platform: multiple
title: Die Methode "stipxvirtualnetworknumber" der Win32_NetworkAdapterConfiguration-Klasse
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapterConfiguration.SetIPXVirtualNetworkNumber
api_type:
- COM
api_location:
- cimwin32.dll
ms.openlocfilehash: ed6e6802a17ef6ec4393d2ae0c5ec43f0e21d247
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344624"
---
# <a name="setipxvirtualnetworknumber-method-of-the-win32_networkadapterconfiguration-class"></a><span data-ttu-id="266c5-103">Die Methode "stipxvirtualnetworknumber" der Win32 \_ networkadapterconfiguration-Klasse</span><span class="sxs-lookup"><span data-stu-id="266c5-103">SetIPXVirtualNetworkNumber method of the Win32\_NetworkAdapterConfiguration class</span></span>

<span data-ttu-id="266c5-104">Legt die virtuelle IPX-Netzwerk Nummer (Internetworking Packet Exchange) auf dem Zielcomputer System fest.</span><span class="sxs-lookup"><span data-stu-id="266c5-104">Sets the Internetworking Packet Exchange (IPX) virtual network number on the target computer system.</span></span> <span data-ttu-id="266c5-105">Für Windows 2000 und Windows NT 3,51 oder höher wird eine interne Netzwerk Nummer für das interne Routing verwendet.</span><span class="sxs-lookup"><span data-stu-id="266c5-105">Windows 2000 and Windows NT 3.51 or greater uses an internal network number for internal routing.</span></span> <span data-ttu-id="266c5-106">Die interne Netzwerk Nummer wird auch als virtuelle Netzwerk Nummer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="266c5-106">The internal network number is also known as a virtual network number.</span></span> <span data-ttu-id="266c5-107">Das Computersystem im Netzwerk wird eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="266c5-107">It uniquely identifies the computer system on the network.</span></span> <span data-ttu-id="266c5-108">Die-Methode gibt einen ganzzahligen Wert zurück, der wie folgt interpretiert werden kann:</span><span class="sxs-lookup"><span data-stu-id="266c5-108">The method returns an integer value that can be interpretted as follows:</span></span>

## <a name="syntax"></a><span data-ttu-id="266c5-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="266c5-109">Syntax</span></span>


```mof
uint32 SetIPXVirtualNetworkNumber(
  [in] string IPXVirtualNetNumber
);
```



## <a name="parameters"></a><span data-ttu-id="266c5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="266c5-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="266c5-111">*IPXVirtualNetNumber* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="266c5-111">*IPXVirtualNetNumber* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="266c5-112">Die Nummer des virtuellen Netzwerks für dieses System.</span><span class="sxs-lookup"><span data-stu-id="266c5-112">The virtual network number for this system.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="266c5-113">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="266c5-113">Return value</span></span>

<dl> <dt>

<span data-ttu-id="266c5-114">**Erfolgreicher Abschluss, kein Neustart erforderlich** (0)</span><span class="sxs-lookup"><span data-stu-id="266c5-114">**Successful completion, no reboot required** (0)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-115">**Erfolgreicher Abschluss, Neustart erforderlich** (1)</span><span class="sxs-lookup"><span data-stu-id="266c5-115">**Successful completion, reboot required** (1)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-116">**Methode wird auf dieser Plattform nicht unterstützt** (64).</span><span class="sxs-lookup"><span data-stu-id="266c5-116">**Method not supported on this platform** (64)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-117">**Unbekannter Fehler** (65).</span><span class="sxs-lookup"><span data-stu-id="266c5-117">**Unknown failure** (65)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-118">**Ungültige Subnetzmaske** (66).</span><span class="sxs-lookup"><span data-stu-id="266c5-118">**Invalid subnet mask** (66)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-119">**Fehler beim Verarbeiten einer Instanz, die zurückgegeben wurde** (67).</span><span class="sxs-lookup"><span data-stu-id="266c5-119">**An error occurred while processing an Instance that was returned** (67)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-120">**Ungültiger Eingabeparameter** (68)</span><span class="sxs-lookup"><span data-stu-id="266c5-120">**Invalid input parameter** (68)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-121">**Es wurden mehr als 5 Gateways angegeben** (69).</span><span class="sxs-lookup"><span data-stu-id="266c5-121">**More than 5 gateways specified** (69)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-122">**Ungültige IP-Adresse** (70)</span><span class="sxs-lookup"><span data-stu-id="266c5-122">**Invalid IP address** (70)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-123">**Ungültige Gateway-IP-Adresse** (71)</span><span class="sxs-lookup"><span data-stu-id="266c5-123">**Invalid gateway IP address** (71)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-124">**Fehler beim Zugriff auf die Registrierung für die angeforderten Informationen** (72).</span><span class="sxs-lookup"><span data-stu-id="266c5-124">**An error occurred while accessing the Registry for the requested information** (72)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-125">**Ungültiger Domänen Name** (73).</span><span class="sxs-lookup"><span data-stu-id="266c5-125">**Invalid domain name** (73)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-126">**Ungültiger Hostname** (74).</span><span class="sxs-lookup"><span data-stu-id="266c5-126">**Invalid host name** (74)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-127">**Kein primärer/sekundärer WINS-Server definiert** (75)</span><span class="sxs-lookup"><span data-stu-id="266c5-127">**No primary/secondary WINS server defined** (75)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-128">**Ungültige Datei** (76)</span><span class="sxs-lookup"><span data-stu-id="266c5-128">**Invalid file** (76)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-129">**Ungültiger Systempfad** (77).</span><span class="sxs-lookup"><span data-stu-id="266c5-129">**Invalid system path** (77)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-130">Fehler beim **Kopieren der Datei** (78).</span><span class="sxs-lookup"><span data-stu-id="266c5-130">**File copy failed** (78)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-131">**Ungültiger Sicherheitsparameter** (79).</span><span class="sxs-lookup"><span data-stu-id="266c5-131">**Invalid security parameter** (79)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-132">Der **TCP/IP-Dienst kann nicht konfiguriert** werden (80).</span><span class="sxs-lookup"><span data-stu-id="266c5-132">**Unable to configure TCP/IP service** (80)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-133">**DHCP-Dienst kann nicht konfiguriert** werden (81).</span><span class="sxs-lookup"><span data-stu-id="266c5-133">**Unable to configure DHCP service** (81)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-134">**DHCP-Lease kann nicht erneuert** werden (82).</span><span class="sxs-lookup"><span data-stu-id="266c5-134">**Unable to renew DHCP lease** (82)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-135">**DHCP-Lease kann nicht frei** gegeben werden (83).</span><span class="sxs-lookup"><span data-stu-id="266c5-135">**Unable to release DHCP lease** (83)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-136">Die **IP ist auf dem Adapter nicht aktiviert** (84).</span><span class="sxs-lookup"><span data-stu-id="266c5-136">**IP not enabled on adapter** (84)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-137">**IPX ist auf dem Adapter nicht aktiviert** (85).</span><span class="sxs-lookup"><span data-stu-id="266c5-137">**IPX not enabled on adapter** (85)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-138">**Fehler bei Frame/Netzwerk Nummer** (86)</span><span class="sxs-lookup"><span data-stu-id="266c5-138">**Frame/network number bounds error** (86)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-139">**Ungültiger Frame-Typ** (87).</span><span class="sxs-lookup"><span data-stu-id="266c5-139">**Invalid frame type** (87)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-140">**Ungültige Netzwerk Nummer** (88).</span><span class="sxs-lookup"><span data-stu-id="266c5-140">**Invalid network number** (88)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-141">**Doppelte Netzwerk Nummer** (89)</span><span class="sxs-lookup"><span data-stu-id="266c5-141">**Duplicate network number** (89)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-142">**Parameter außerhalb des** gültigen Bereichs (90)</span><span class="sxs-lookup"><span data-stu-id="266c5-142">**Parameter out of bounds** (90)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-143">**Zugriff verweigert** (91)</span><span class="sxs-lookup"><span data-stu-id="266c5-143">**Access denied** (91)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-144">**Nicht** genügend Arbeitsspeicher (92)</span><span class="sxs-lookup"><span data-stu-id="266c5-144">**Out of memory** (92)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-145">**Bereits vorhanden** (93)</span><span class="sxs-lookup"><span data-stu-id="266c5-145">**Already exists** (93)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-146">Der **Pfad, die Datei oder das Objekt wurde nicht gefunden** (94).</span><span class="sxs-lookup"><span data-stu-id="266c5-146">**Path, file or object not found** (94)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-147">Der **Dienst kann nicht benachrichtigt** werden (95).</span><span class="sxs-lookup"><span data-stu-id="266c5-147">**Unable to notify service** (95)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-148">Der **DNS-Dienst kann nicht benachrichtigt** werden (96).</span><span class="sxs-lookup"><span data-stu-id="266c5-148">**Unable to notify DNS service** (96)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-149">**Schnittstelle nicht konfigurierbar** (97)</span><span class="sxs-lookup"><span data-stu-id="266c5-149">**Interface not configurable** (97)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-150">**Nicht alle DHCP-Leases konnten freigegeben/erneuert werden** (98).</span><span class="sxs-lookup"><span data-stu-id="266c5-150">**Not all DHCP leases could be released/renewed** (98)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-151">**DHCP ist auf dem Adapter nicht aktiviert** (100).</span><span class="sxs-lookup"><span data-stu-id="266c5-151">**DHCP not enabled on adapter** (100)</span></span>
</dt> <dt>

<span data-ttu-id="266c5-152">**Sonstige** (101 – 4294967295)</span><span class="sxs-lookup"><span data-stu-id="266c5-152">**Other** (101–4294967295)</span></span>
</dt> </dl>

## <a name="requirements"></a><span data-ttu-id="266c5-153">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="266c5-153">Requirements</span></span>



| <span data-ttu-id="266c5-154">Anforderung</span><span class="sxs-lookup"><span data-stu-id="266c5-154">Requirement</span></span> | <span data-ttu-id="266c5-155">Wert</span><span class="sxs-lookup"><span data-stu-id="266c5-155">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="266c5-156">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="266c5-156">Minimum supported client</span></span><br/> | <span data-ttu-id="266c5-157">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="266c5-157">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="266c5-158">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="266c5-158">Minimum supported server</span></span><br/> | <span data-ttu-id="266c5-159">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="266c5-159">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="266c5-160">Namespace</span><span class="sxs-lookup"><span data-stu-id="266c5-160">Namespace</span></span><br/>                | <span data-ttu-id="266c5-161">Root \\ CIMV2</span><span class="sxs-lookup"><span data-stu-id="266c5-161">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="266c5-162">MOF</span><span class="sxs-lookup"><span data-stu-id="266c5-162">MOF</span></span><br/>                      | <dl> <span data-ttu-id="266c5-163"><dt>Cimwin32. MOF</dt></span><span class="sxs-lookup"><span data-stu-id="266c5-163"><dt>CimWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="266c5-164">DLL</span><span class="sxs-lookup"><span data-stu-id="266c5-164">DLL</span></span><br/>                      | <dl> <span data-ttu-id="266c5-165"><dt>Cimwin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="266c5-165"><dt>Cimwin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="266c5-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="266c5-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="266c5-167">**Win32 \_ networkadapterconfiguration**</span><span class="sxs-lookup"><span data-stu-id="266c5-167">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
</dt> </dl>

 

 




