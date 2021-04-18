---
title: Konfigurationseinstellungen
description: Das Verhalten der Steuerungspunkt-API und der Geräte Host-API kann durch Ändern der Einstellungen in der Registrierung geändert werden.
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4107df31335da2f93fd4be669c8557b1f56d179e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106337352"
---
# <a name="configuration-settings"></a><span data-ttu-id="de323-103">Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="de323-103">Configuration Settings</span></span>

<span data-ttu-id="de323-104">Das Verhalten der [Steuerungspunkt-API](control-point-api.md) und der [Geräte Host-API](device-host-api.md) kann durch Ändern der Einstellungen in der Registrierung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="de323-104">The behavior of the [Control Point API](control-point-api.md) and [Device Host API](device-host-api.md) can be modified by changing settings in the registry.</span></span>

<span data-ttu-id="de323-105">Es gibt sieben Registrierungs Werte, die sich auf das Verhalten auswirken:</span><span class="sxs-lookup"><span data-stu-id="de323-105">There are seven registry values that affect behavior:</span></span>

-   <span data-ttu-id="de323-106">**Downloadbereich**</span><span class="sxs-lookup"><span data-stu-id="de323-106">**DownloadScope**</span></span>
-   <span data-ttu-id="de323-107">**Devicelifetime**</span><span class="sxs-lookup"><span data-stu-id="de323-107">**DeviceLifeTime**</span></span>
-   <span data-ttu-id="de323-108">\\**UPnP-Geräte Host** \\ **Dateigrößen Beschränkung**</span><span class="sxs-lookup"><span data-stu-id="de323-108">\\**UPnP Device Host**\\**File Size Limit**</span></span>
-   <span data-ttu-id="de323-109">\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Dateigrößen Beschränkung**</span><span class="sxs-lookup"><span data-stu-id="de323-109">\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
-   <span data-ttu-id="de323-110">**Maxcache**</span><span class="sxs-lookup"><span data-stu-id="de323-110">**MaxCache**</span></span>
-   <span data-ttu-id="de323-111">**TTL**</span><span class="sxs-lookup"><span data-stu-id="de323-111">**TTL**</span></span>
-   <span data-ttu-id="de323-112">**Receivescope**</span><span class="sxs-lookup"><span data-stu-id="de323-112">**ReceiveScope**</span></span>

<span data-ttu-id="de323-113">Es gibt zwei Registrierungs Werte namens **Dateigrößen Beschränkung**, eine für Beschreibungs Dokumente und die andere für Antworten, die SOAP (Simple Object Access Protocol) verwenden.</span><span class="sxs-lookup"><span data-stu-id="de323-113">There are two registry values called **File Size Limit**, one for description documents and the other for responses that use Simple Object Access Protocol (SOAP).</span></span>

<span data-ttu-id="de323-114">Der Speicherort der sieben Werte in der Registrierung lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="de323-114">The location of each of the seven values in the registry is as follows:</span></span>

```
HKEY_LOCAL_MACHINE
   SOFTWARE
      Microsoft
         UPnPControl Point
            DownloadScope
         UPnP Device Host
            Devices
               DeviceLifeTime
            File Size Limit
         Windows
            CurrentVersion
               UPnP
                  File Size Limit
   SYSTEM
      CurentControlSet
         Services
            SSDPSRV
               Parameters
                  MaxCache
                  TTL
                  ReceiveScope
```

## <a name="registry-value-descriptions"></a><span data-ttu-id="de323-115">Beschreibungen von Registrierungs Werten</span><span class="sxs-lookup"><span data-stu-id="de323-115">Registry Value Descriptions</span></span>

<span data-ttu-id="de323-116">Die Registrierungs Werte werden in der folgenden Liste erläutert.</span><span class="sxs-lookup"><span data-stu-id="de323-116">The registry values are explained in the following list.</span></span> <span data-ttu-id="de323-117">Jeder Registrierungs Wert ist ein **reg \_ DWORD** (eine 32-Bit-Ganzzahl).</span><span class="sxs-lookup"><span data-stu-id="de323-117">Each registry value is a **REG\_DWORD** (a 32-bit integer).</span></span> <span data-ttu-id="de323-118">Die Auswirkung der einzelnen Werte ist Global.</span><span class="sxs-lookup"><span data-stu-id="de323-118">The effect of each value is global.</span></span>

<dl> <dt>

<span data-ttu-id="de323-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**Downloadbereich**</span><span class="sxs-lookup"><span data-stu-id="de323-119"><span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**</span></span>
</dt> <dd>

<span data-ttu-id="de323-120">Gibt an, welche IP-Adressen für die Dokument-URL der Geräte Beschreibung gültig sind.</span><span class="sxs-lookup"><span data-stu-id="de323-120">Specifies which IP addresses are valid for the device description document URL.</span></span> <span data-ttu-id="de323-121">Wenn die IP-Adresse des Hosts, der in der Beschreibungs Dokument-URL angegeben ist, nicht innerhalb des durch **Download Scope** angegebenen Bereichs liegt, ist diese IP-Adresse ungültig, und das Geräte Objekt wird nicht erstellt.</span><span class="sxs-lookup"><span data-stu-id="de323-121">If the IP address of the host that is specified in the description document URL is not within the scope specified by **DownloadScope**, that IP address is not valid and the device object will not be created.</span></span>

<span data-ttu-id="de323-122">Die gültigen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="de323-122">The valid values are shown in the following table.</span></span> <span data-ttu-id="de323-123">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="de323-123">The default value is 1.</span></span>



| <span data-ttu-id="de323-124">Wert von **Download Scope**</span><span class="sxs-lookup"><span data-stu-id="de323-124">Value of **DownloadScope**</span></span> | <span data-ttu-id="de323-125">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="de323-125">Meaning</span></span>                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de323-126">0</span><span class="sxs-lookup"><span data-stu-id="de323-126">0</span></span>                          | <span data-ttu-id="de323-127">Die IP-Adresse des Hosts muss eine Subnetzadresse sein.</span><span class="sxs-lookup"><span data-stu-id="de323-127">Host's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="de323-128">1</span><span class="sxs-lookup"><span data-stu-id="de323-128">1</span></span>                          | <span data-ttu-id="de323-129">Die IP-Adresse des Hosts muss eine Subnetzadresse oder eine private Adresse (10) sein. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (gemäß RFC 1918) oder 169,254. *x*. *x* (entsprechend der Angabe in RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="de323-129">Host's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="de323-130">2</span><span class="sxs-lookup"><span data-stu-id="de323-130">2</span></span>                          | <span data-ttu-id="de323-131">Bei der Host-IP-Adresse muss es sich um eine Subnetzadresse, eine private Adresse oder eine Adresse handeln, die innerhalb der Gültigkeitsdauer (Time-to-Live, TTL) des Steuerungs Punkts liegt.</span><span class="sxs-lookup"><span data-stu-id="de323-131">Host's IP address must be a subnet address, private address, or an address that is within the time-to-live (TTL) hops from the control point.</span></span>                                                              |
| <span data-ttu-id="de323-132">3</span><span class="sxs-lookup"><span data-stu-id="de323-132">3</span></span>                          | <span data-ttu-id="de323-133">Die IP-Adresse des Hosts kann eine beliebige Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="de323-133">Host's IP address can be any address.</span></span>                                                                                                                                                                      |
| <span data-ttu-id="de323-134">>3</span><span class="sxs-lookup"><span data-stu-id="de323-134">>3</span></span>                      | <span data-ttu-id="de323-135">Identisch mit der für den Wert 0.</span><span class="sxs-lookup"><span data-stu-id="de323-135">Same as that for the value 0.</span></span>                                                                                                                                                                              |



 

</dd> <dt>

<span data-ttu-id="de323-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**Devicelifetime**</span><span class="sxs-lookup"><span data-stu-id="de323-136"><span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**</span></span>
</dt> <dd>

<span data-ttu-id="de323-137">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="de323-137">Optional.</span></span> <span data-ttu-id="de323-138">Gibt die Lebensdauer eines Geräts in Sekunden an, die den in der Ankündigungs Meldung des Geräts angegebenen Wert überschreibt.</span><span class="sxs-lookup"><span data-stu-id="de323-138">Specifies a device's lifetime, in seconds, which overrides the value provided in the device's announcement message.</span></span> <span data-ttu-id="de323-139">Wenn **devicelifetime** vorhanden ist, wird der in der Ankündigung des Geräts angegebene Wert ignoriert, und stattdessen wird der Registrierungs Wert verwendet.</span><span class="sxs-lookup"><span data-stu-id="de323-139">If **DeviceLifeTime** is present, the value specified in the device's announcement is ignored and the registry value is used instead.</span></span> <span data-ttu-id="de323-140">Dies gilt für alle Geräte.</span><span class="sxs-lookup"><span data-stu-id="de323-140">This applies to all devices.</span></span>

<span data-ttu-id="de323-141">Gültige Werte reichen von 900 bis **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="de323-141">Valid values range from 900 through **MAX\_DWORD**.</span></span> <span data-ttu-id="de323-142">Der Standardwert lautet 1800.</span><span class="sxs-lookup"><span data-stu-id="de323-142">The default value is 1800.</span></span> <span data-ttu-id="de323-143">Wenn **devicelifetime** auf 0 festgelegt ist, wird der Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="de323-143">If **DeviceLifeTime** is set to 0, the default value is used.</span></span>

</dd> <dt>

<span data-ttu-id="de323-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP-Geräte Host** \\ **Dateigrößen Beschränkung**</span><span class="sxs-lookup"><span data-stu-id="de323-144"><span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP Device Host**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="de323-145">Gibt die maximale Größe (in Bytes) der einzelnen Beschreibungs Dokumente an.</span><span class="sxs-lookup"><span data-stu-id="de323-145">Specifies the maximum size, in bytes, of each description document.</span></span> <span data-ttu-id="de323-146">Diese Einstellung kann in Windows-Versionen vor Windows XP Service Pack 2 nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="de323-146">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="de323-147">In den vorherigen Versionen ist diese Einstellung als 102400 hart codiert.</span><span class="sxs-lookup"><span data-stu-id="de323-147">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="de323-148">Gültige Werte reichen von 10240 bis **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="de323-148">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="de323-149">Der Standardwert ist 102400.</span><span class="sxs-lookup"><span data-stu-id="de323-149">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="de323-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Dateigrößen Beschränkung**</span><span class="sxs-lookup"><span data-stu-id="de323-150"><span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows**\\**CurrentVersion**\\**UPnP**\\**File Size Limit**</span></span>
</dt> <dd>

<span data-ttu-id="de323-151">Gibt die maximale Größe der SOAP-Antwort in Bytes an, die zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="de323-151">Specifies the maximum size, in bytes, of the SOAP response that is acceptable.</span></span> <span data-ttu-id="de323-152">Diese Einstellung kann in Windows-Versionen vor Windows XP Service Pack 2 nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="de323-152">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="de323-153">In den vorherigen Versionen ist diese Einstellung als 102400 hart codiert.</span><span class="sxs-lookup"><span data-stu-id="de323-153">In the previous versions, this setting is hard-coded as 102400.</span></span>

<span data-ttu-id="de323-154">Gültige Werte reichen von 10240 bis **Max \_ DWORD**.</span><span class="sxs-lookup"><span data-stu-id="de323-154">Valid values range from 10240 through **MAX\_DWORD**.</span></span> <span data-ttu-id="de323-155">Der Standardwert ist 102400.</span><span class="sxs-lookup"><span data-stu-id="de323-155">The default value is 102400.</span></span>

</dd> <dt>

<span data-ttu-id="de323-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**Maxcache**</span><span class="sxs-lookup"><span data-stu-id="de323-156"><span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**</span></span>
</dt> <dd>

<span data-ttu-id="de323-157">Gibt die maximale Anzahl von Einträgen an, die im SSDP-Cache (Simple Service Discovery-Protokoll) zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="de323-157">Specifies the maximum number of entries allowed in the Simple Service Discovery Protocol (SSDP) cache.</span></span>

<span data-ttu-id="de323-158">Gültige Werte liegen im Bereich von 10 bis 30000.</span><span class="sxs-lookup"><span data-stu-id="de323-158">Valid values range from 10 through 30000.</span></span> <span data-ttu-id="de323-159">Der Standardwert lautet „1000“.</span><span class="sxs-lookup"><span data-stu-id="de323-159">The default value is 1000.</span></span>

</dd> <dt>

<span data-ttu-id="de323-160"><span id="TTL"></span><span id="ttl"></span>**TTL**</span><span class="sxs-lookup"><span data-stu-id="de323-160"><span id="TTL"></span><span id="ttl"></span>**TTL**</span></span>
</dt> <dd>

<span data-ttu-id="de323-161">Gibt die Gültigkeitsdauer für ein SSDP-Paket an.</span><span class="sxs-lookup"><span data-stu-id="de323-161">Specifies the time-to-live for an SSDP packet.</span></span> <span data-ttu-id="de323-162">Das heißt, **TTL** gibt die Anzahl der Hops an, die für ein Paket zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="de323-162">That is, **TTL** specifies the number of hops allowed for a packet.</span></span>

<span data-ttu-id="de323-163">Gültige Werte liegen zwischen 1 und 255.</span><span class="sxs-lookup"><span data-stu-id="de323-163">Valid values range from 1 through 255.</span></span> <span data-ttu-id="de323-164">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="de323-164">The default value is 1.</span></span>

</dd> <dt>

<span data-ttu-id="de323-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**Receivescope**</span><span class="sxs-lookup"><span data-stu-id="de323-165"><span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**</span></span>
</dt> <dd>

<span data-ttu-id="de323-166">Gibt an, welche IP-Adressen gültige Quellen für eine Nachricht sind.</span><span class="sxs-lookup"><span data-stu-id="de323-166">Specifies which IP addresses are valid sources of a message.</span></span> <span data-ttu-id="de323-167">Wenn eine eingehende Nachricht von einer Adresse stammt, die nicht innerhalb des von **receivescope** angegebenen Bereichs liegt, wird die Nachricht ignoriert.</span><span class="sxs-lookup"><span data-stu-id="de323-167">If an incoming message originates from an address that is not within the scope specified by **ReceiveScope**, the message is ignored.</span></span> <span data-ttu-id="de323-168">Diese Einstellung kann in Windows-Versionen vor Windows XP Service Pack 2 nicht konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="de323-168">This setting is not configurable in versions of Windows preceding Windows XP Service Pack 2.</span></span> <span data-ttu-id="de323-169">In den vorherigen Versionen wird eine Nachricht ohne Rücksicht auf Ihre Quelle akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="de323-169">In the previous versions, a message is accepted without regard to its source.</span></span>

<span data-ttu-id="de323-170">Die gültigen Werte sind in der folgenden Tabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="de323-170">The valid values are shown in the following table.</span></span> <span data-ttu-id="de323-171">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="de323-171">The default value is 1.</span></span>



| <span data-ttu-id="de323-172">Wert von **receivescope**</span><span class="sxs-lookup"><span data-stu-id="de323-172">Value of **ReceiveScope**</span></span> | <span data-ttu-id="de323-173">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="de323-173">Meaning</span></span>                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="de323-174">0</span><span class="sxs-lookup"><span data-stu-id="de323-174">0</span></span>                         | <span data-ttu-id="de323-175">Die IP-Adresse des Absenders muss eine Subnetzadresse sein.</span><span class="sxs-lookup"><span data-stu-id="de323-175">Sender's IP address must be a subnet address.</span></span>                                                                                                                                                                |
| <span data-ttu-id="de323-176">1</span><span class="sxs-lookup"><span data-stu-id="de323-176">1</span></span>                         | <span data-ttu-id="de323-177">Die IP-Adresse des Absenders muss eine Subnetzadresse oder eine private Adresse sein, die einer von 10 ist. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (gemäß RFC 1918) oder 169,254. *x*. *x* (entsprechend der Angabe in RFC 3330).</span><span class="sxs-lookup"><span data-stu-id="de323-177">Sender's IP address must be a subnet address or a private address which is one of 10.*x*.*x*.*x*, 192.168.*x*.*x*, 172.16.*x*.*x* (as specified by RFC 1918), or 169.254.*x*.*x* (as specified by RFC 3330).</span></span> |
| <span data-ttu-id="de323-178">2</span><span class="sxs-lookup"><span data-stu-id="de323-178">2</span></span>                         | <span data-ttu-id="de323-179">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="de323-179">Not used.</span></span> <span data-ttu-id="de323-180">Wenn **receivescope** auf 2 festgelegt ist, wird der Standardwert verwendet.</span><span class="sxs-lookup"><span data-stu-id="de323-180">If **ReceiveScope** is set to 2, the default value is used.</span></span>                                                                                                                                        |
| <span data-ttu-id="de323-181">3</span><span class="sxs-lookup"><span data-stu-id="de323-181">3</span></span>                         | <span data-ttu-id="de323-182">Die IP-Adresse des Absenders kann eine beliebige Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="de323-182">Sender's IP address can be any address.</span></span>                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="de323-183">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="de323-183">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="de323-184">Übersicht über die UPnP-Architektur</span><span class="sxs-lookup"><span data-stu-id="de323-184">Overview of UPnP Architecture</span></span>](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




