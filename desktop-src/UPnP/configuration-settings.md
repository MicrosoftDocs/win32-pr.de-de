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
# <a name="configuration-settings"></a>Konfigurationseinstellungen

Das Verhalten der [Steuerungspunkt-API](control-point-api.md) und der [Geräte Host-API](device-host-api.md) kann durch Ändern der Einstellungen in der Registrierung geändert werden.

Es gibt sieben Registrierungs Werte, die sich auf das Verhalten auswirken:

-   **Downloadbereich**
-   **Devicelifetime**
-   \\**UPnP-Geräte Host** \\ **Dateigrößen Beschränkung**
-   \\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Dateigrößen Beschränkung**
-   **Maxcache**
-   **TTL**
-   **Receivescope**

Es gibt zwei Registrierungs Werte namens **Dateigrößen Beschränkung**, eine für Beschreibungs Dokumente und die andere für Antworten, die SOAP (Simple Object Access Protocol) verwenden.

Der Speicherort der sieben Werte in der Registrierung lautet wie folgt:

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

## <a name="registry-value-descriptions"></a>Beschreibungen von Registrierungs Werten

Die Registrierungs Werte werden in der folgenden Liste erläutert. Jeder Registrierungs Wert ist ein **reg \_ DWORD** (eine 32-Bit-Ganzzahl). Die Auswirkung der einzelnen Werte ist Global.

<dl> <dt>

<span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**Downloadbereich**
</dt> <dd>

Gibt an, welche IP-Adressen für die Dokument-URL der Geräte Beschreibung gültig sind. Wenn die IP-Adresse des Hosts, der in der Beschreibungs Dokument-URL angegeben ist, nicht innerhalb des durch **Download Scope** angegebenen Bereichs liegt, ist diese IP-Adresse ungültig, und das Geräte Objekt wird nicht erstellt.

Die gültigen Werte sind in der folgenden Tabelle aufgeführt. Der Standardwert ist 1.



| Wert von **Download Scope** | Bedeutung                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                          | Die IP-Adresse des Hosts muss eine Subnetzadresse sein.                                                                                                                                                                |
| 1                          | Die IP-Adresse des Hosts muss eine Subnetzadresse oder eine private Adresse (10) sein. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (gemäß RFC 1918) oder 169,254. *x*. *x* (entsprechend der Angabe in RFC 3330). |
| 2                          | Bei der Host-IP-Adresse muss es sich um eine Subnetzadresse, eine private Adresse oder eine Adresse handeln, die innerhalb der Gültigkeitsdauer (Time-to-Live, TTL) des Steuerungs Punkts liegt.                                                              |
| 3                          | Die IP-Adresse des Hosts kann eine beliebige Adresse sein.                                                                                                                                                                      |
| >3                      | Identisch mit der für den Wert 0.                                                                                                                                                                              |



 

</dd> <dt>

<span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**Devicelifetime**
</dt> <dd>

Dies ist optional. Gibt die Lebensdauer eines Geräts in Sekunden an, die den in der Ankündigungs Meldung des Geräts angegebenen Wert überschreibt. Wenn **devicelifetime** vorhanden ist, wird der in der Ankündigung des Geräts angegebene Wert ignoriert, und stattdessen wird der Registrierungs Wert verwendet. Dies gilt für alle Geräte.

Gültige Werte reichen von 900 bis **Max \_ DWORD**. Der Standardwert lautet 1800. Wenn **devicelifetime** auf 0 festgelegt ist, wird der Standardwert verwendet.

</dd> <dt>

<span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP-Geräte Host** \\ **Dateigrößen Beschränkung**
</dt> <dd>

Gibt die maximale Größe (in Bytes) der einzelnen Beschreibungs Dokumente an. Diese Einstellung kann in Windows-Versionen vor Windows XP Service Pack 2 nicht konfiguriert werden. In den vorherigen Versionen ist diese Einstellung als 102400 hart codiert.

Gültige Werte reichen von 10240 bis **Max \_ DWORD**. Der Standardwert ist 102400.

</dd> <dt>

<span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Dateigrößen Beschränkung**
</dt> <dd>

Gibt die maximale Größe der SOAP-Antwort in Bytes an, die zulässig ist. Diese Einstellung kann in Windows-Versionen vor Windows XP Service Pack 2 nicht konfiguriert werden. In den vorherigen Versionen ist diese Einstellung als 102400 hart codiert.

Gültige Werte reichen von 10240 bis **Max \_ DWORD**. Der Standardwert ist 102400.

</dd> <dt>

<span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**Maxcache**
</dt> <dd>

Gibt die maximale Anzahl von Einträgen an, die im SSDP-Cache (Simple Service Discovery-Protokoll) zulässig sind.

Gültige Werte liegen im Bereich von 10 bis 30000. Der Standardwert lautet „1000“.

</dd> <dt>

<span id="TTL"></span><span id="ttl"></span>**TTL**
</dt> <dd>

Gibt die Gültigkeitsdauer für ein SSDP-Paket an. Das heißt, **TTL** gibt die Anzahl der Hops an, die für ein Paket zulässig sind.

Gültige Werte liegen zwischen 1 und 255. Der Standardwert ist 1.

</dd> <dt>

<span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**Receivescope**
</dt> <dd>

Gibt an, welche IP-Adressen gültige Quellen für eine Nachricht sind. Wenn eine eingehende Nachricht von einer Adresse stammt, die nicht innerhalb des von **receivescope** angegebenen Bereichs liegt, wird die Nachricht ignoriert. Diese Einstellung kann in Windows-Versionen vor Windows XP Service Pack 2 nicht konfiguriert werden. In den vorherigen Versionen wird eine Nachricht ohne Rücksicht auf Ihre Quelle akzeptiert.

Die gültigen Werte sind in der folgenden Tabelle aufgeführt. Der Standardwert ist 1.



| Wert von **receivescope** | Bedeutung                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                         | Die IP-Adresse des Absenders muss eine Subnetzadresse sein.                                                                                                                                                                |
| 1                         | Die IP-Adresse des Absenders muss eine Subnetzadresse oder eine private Adresse sein, die einer von 10 ist. *x*. *x*. *x*, 192,168. *x*. *x*, 172,16. *x*. *x* (gemäß RFC 1918) oder 169,254. *x*. *x* (entsprechend der Angabe in RFC 3330). |
| 2                         | Nicht verwendet. Wenn **receivescope** auf 2 festgelegt ist, wird der Standardwert verwendet.                                                                                                                                        |
| 3                         | Die IP-Adresse des Absenders kann eine beliebige Adresse sein.                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die UPnP-Architektur](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




