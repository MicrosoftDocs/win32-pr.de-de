---
title: Konfigurationseinstellungen
description: Das Verhalten der Steuerungspunkt-API und der Gerätehost-API kann durch Ändern der Einstellungen in der Registrierung geändert werden.
ms.assetid: 81893cde-d28f-41ec-a6c1-159b3eb84274
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68438f6eb425da253aa7f59af3b7d060bacacadb865d4546ddbc0f37fecd9ed2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120008110"
---
# <a name="configuration-settings"></a>Konfigurationseinstellungen

Das Verhalten der [Steuerungspunkt-API](control-point-api.md) und [der Gerätehost-API](device-host-api.md) kann durch Ändern der Einstellungen in der Registrierung geändert werden.

Es gibt sieben Registrierungswerte, die sich auf das Verhalten auswirken:

-   **DownloadScope**
-   **DeviceLifeTime**
-   \\**UPnP-Gerätehost** \\ **Dateigrößenbeschränkung**
-   \\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Dateigrößenbeschränkung**
-   **MaxCache**
-   **TTL**
-   **ReceiveScope**

Es gibt zwei Registrierungswerte namens **Dateigrößenbeschränkung,** einen für Beschreibungsdokumente und den anderen für Antworten, die SOAP (Simple Object Access Protocol) verwenden.

Der Speicherort jedes der sieben Werte in der Registrierung lautet wie folgt:

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

## <a name="registry-value-descriptions"></a>Beschreibungen von Registrierungswerten

Die Registrierungswerte werden in der folgenden Liste erläutert. Jeder Registrierungswert ist ein **\_ REG-DWORD** (eine 32-Bit-Ganzzahl). Die Auswirkung jedes Werts ist global.

<dl> <dt>

<span id="DownloadScope"></span><span id="downloadscope"></span><span id="DOWNLOADSCOPE"></span>**DownloadScope**
</dt> <dd>

Gibt an, welche IP-Adressen für die Dokument-URL der Gerätebeschreibung gültig sind. Wenn die IP-Adresse des Hosts, der in der Beschreibungsdokument-URL angegeben ist, nicht innerhalb des von **DownloadScope** angegebenen Bereichs liegt, ist diese IP-Adresse ungültig, und das Geräteobjekt wird nicht erstellt.

Die gültigen Werte werden in der folgenden Tabelle angezeigt. Der Standardwert ist 1.



| Wert von **DownloadScope** | Bedeutung                                                                                                                                                                                                    |
|----------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                          | Die IP-Adresse des Hosts muss eine Subnetzadresse sein.                                                                                                                                                                |
| 1                          | Die IP-Adresse des Hosts muss eine Subnetzadresse oder eine private Adresse sein, die eine von 10 ist. *x*. *x*. *x*, 192.168. *x*. *x*, 172.16. *x*. *x* (gemäß RFC 1918) oder 169.254. *x*. *x* (gemäß RFC 3330). |
| 2                          | Die IP-Adresse des Hosts muss eine Subnetzadresse, eine private Adresse oder eine Adresse sein, die innerhalb der Gültigkeitsdauer (Time-to-Live, TTL) vom Steuerungspunkt liegt.                                                              |
| 3                          | Die IP-Adresse des Hosts kann eine beliebige Adresse sein.                                                                                                                                                                      |
| >3                      | Entspricht dem Wert 0.                                                                                                                                                                              |



 

</dd> <dt>

<span id="DeviceLifeTime"></span><span id="devicelifetime"></span><span id="DEVICELIFETIME"></span>**DeviceLifeTime**
</dt> <dd>

Optional. Gibt die Lebensdauer eines Geräts in Sekunden an, wodurch der in der Ankündigungsmeldung des Geräts angegebene Wert überschrieben wird. Wenn **DeviceLifeTime** vorhanden ist, wird der in der Ankündigung des Geräts angegebene Wert ignoriert, und stattdessen wird der Registrierungswert verwendet. Dies gilt für alle Geräte.

Gültige Werte liegen zwischen 900 und **MAX \_ DWORD.** Der Standardwert lautet 1800. Wenn **DeviceLifeTime** auf 0 festgelegt ist, wird der Standardwert verwendet.

</dd> <dt>

<span id="_UPnP_Device_HostFile_Size_Limit"></span><span id="_upnp_device_hostfile_size_limit"></span><span id="_UPNP_DEVICE_HOSTFILE_SIZE_LIMIT"></span>\\**UPnP-Gerätehost** \\ **Dateigrößenbeschränkung**
</dt> <dd>

Gibt die maximale Größe jedes Beschreibungsdokuments in Bytes an. Diese Einstellung ist in Versionen von Windows vor Windows XP Service Pack 2 nicht konfigurierbar. In den vorherigen Versionen ist diese Einstellung als 102400 hart codiert.

Gültige Werte liegen zwischen 10240 und **MAX \_ DWORD.** Der Standardwert ist 102400.

</dd> <dt>

<span id="_WindowsCurrentVersionUPnPFile_Size_Limit"></span><span id="_windowscurrentversionupnpfile_size_limit"></span><span id="_WINDOWSCURRENTVERSIONUPNPFILE_SIZE_LIMIT"></span>\\**Windows** \\ **CurrentVersion** \\ **UPnP** \\ **Dateigrößenbeschränkung**
</dt> <dd>

Gibt die maximal zulässige Größe der SOAP-Antwort in Bytes an. Diese Einstellung ist in Versionen von Windows vor Windows XP Service Pack 2 nicht konfigurierbar. In den vorherigen Versionen ist diese Einstellung als 102400 hart codiert.

Gültige Werte liegen zwischen 10240 und **MAX \_ DWORD.** Der Standardwert ist 102400.

</dd> <dt>

<span id="MaxCache"></span><span id="maxcache"></span><span id="MAXCACHE"></span>**MaxCache**
</dt> <dd>

Gibt die maximale Anzahl von Einträgen an, die im SSDP-Cache (Simple Service Discovery Protocol) zulässig sind.

Gültige Werte liegen zwischen 10 und 30000. Der Standardwert lautet „1000“.

</dd> <dt>

<span id="TTL"></span><span id="ttl"></span>**Ttl**
</dt> <dd>

Gibt die Lebensdauer für ein SSDP-Paket an. Das heißt, die **Gültigkeitsdauer** gibt die Anzahl der hops an, die für ein Paket zulässig sind.

Gültige Werte liegen zwischen 1 und 255. Der Standardwert ist 1.

</dd> <dt>

<span id="ReceiveScope"></span><span id="receivescope"></span><span id="RECEIVESCOPE"></span>**ReceiveScope**
</dt> <dd>

Gibt an, welche IP-Adressen gültige Quellen einer Nachricht sind. Wenn eine eingehende Nachricht von einer Adresse stammt, die sich nicht innerhalb des von **ReceiveScope** angegebenen Bereichs befindet, wird die Nachricht ignoriert. Diese Einstellung ist in Versionen von Windows vor Windows XP Service Pack 2 nicht konfigurierbar. In den vorherigen Versionen wird eine Nachricht ohne Berücksichtigung ihrer Quelle akzeptiert.

Die gültigen Werte werden in der folgenden Tabelle angezeigt. Der Standardwert ist 1.



| Wert von **ReceiveScope** | Bedeutung                                                                                                                                                                                                      |
|---------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 0                         | Die IP-Adresse des Absenders muss eine Subnetzadresse sein.                                                                                                                                                                |
| 1                         | Die IP-Adresse des Absenders muss eine Subnetzadresse oder eine private Adresse sein, die eine von 10 ist. *x*. *x*. *x*, 192.168. *x*. *x*, 172.16. *x*. *x* (gemäß RFC 1918) oder 169.254. *x*. *x* (gemäß RFC 3330). |
| 2                         | Wird nicht verwendet. Wenn **ReceiveScope** auf 2 festgelegt ist, wird der Standardwert verwendet.                                                                                                                                        |
| 3                         | Die IP-Adresse des Absenders kann eine beliebige Adresse sein.                                                                                                                                                                      |



 

</dd> </dl>

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Übersicht über die UPnP-Architektur](overview-of-universal-plug-and-play.md)
</dt> </dl>

 

 




