---
description: In diesem Thema werden die Arbeitsspeicher Grenzwerte für unterstützte Windows-und Windows Server-Releases beschrieben.
ms.assetid: de09c8af-0ed8-4fd4-b8e8-2c921aafe6f2
title: Grenzwerte für den Arbeitsspeicher für Versionen von Windows und Windows Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d09db7d303468247794807629d3a56e786c4ada6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106366242"
---
# <a name="memory-limits-for-windows-and-windows-server-releases"></a>Grenzwerte für den Arbeitsspeicher für Versionen von Windows und Windows Server

In diesem Thema werden die Arbeitsspeicher Grenzwerte für unterstützte Windows-und Windows Server-Releases beschrieben.

-   [Speicher-und Adressraum Limits](#memory-limits-for-windows-and-windows-server-releases)
-   [Grenzwerte für den physischen Speicher: Windows 10](#physical-memory-limits-windows-10)
-   [Grenzwerte für den physischen Speicher: Windows Server 2016](#physical-memory-limits-windows-server-2016)
-   [Grenzwerte für den physischen Speicher: Windows 8](#physical-memory-limits-windows-8)
-   [Grenzwerte für den physischen Speicher: Windows Server 2012](#physical-memory-limits-windows-server-2012)
-   [Grenzwerte für den physischen Speicher: Windows 7](#physical-memory-limits-windows-7)
-   [Grenzwerte für den physischen Speicher: Windows Server 2008 R2](#physical-memory-limits-windows-server-2008-r2)
-   [Grenzwerte für den physischen Speicher: Windows Server 2008](#physical-memory-limits-windows-server-2008-r2)
-   [Grenzwerte für den physischen Speicher: Windows Vista](#physical-memory-limits-windows-vista)
-   [Grenzwerte für den physischen Speicher: Windows Home Server](#physical-memory-limits-windows-home-server)
-   [Grenzwerte für den physischen Speicher: Windows Server 2003 R2](#physical-memory-limits-windows-server-2003-r2)
-   [Grenzwerte für den physischen Speicher: Windows Server 2003 mit Service Pack 2 (SP2)](#physical-memory-limits-windows-server-2003-with-service-pack-2-sp2)
-   [Grenzwerte für den physischen Speicher: Windows Server 2003 mit Service Pack 1 (SP1)](#physical-memory-limits-windows-server-2003-with-service-pack-1-sp1)
-   [Grenzwerte für den physischen Speicher: Windows Server 2003](#physical-memory-limits-windows-server-2003-r2)
-   [Grenzwerte für den physischen Speicher: Windows XP](#physical-memory-limits-windows-xp)
-   [Grenzwerte für den physischen Speicher: Windows Embedded](#physical-memory-limits-windows-embedded)
-   [Auswirkungen von Grafikkarten und anderen Geräten auf Arbeitsspeicher Grenzwerte](#how-graphics-cards-and-other-devices-affect-memory-limits)
-   [Zugehörige Themen](#related-topics)

Die Grenzwerte für den Arbeitsspeicher und den Adressraum variieren je nach Plattform, Betriebssystem und nach dem Wert, ob die **Abbild Datei, die \_ \_ große \_ Adressen \_** unterstützt, den Wert der [**geladenen \_ Image**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) Struktur und [4-Gigabyte](4-gigabyte-tuning.md) -Optimierung (4GT) verwendet wird. **Bild \_ Die Datei " \_ große \_ Adresse \_** " wird mit der [/LARGEADDRESSAWARE](/cpp/build/reference/largeaddressaware-handle-large-addresses?view=vs-2019) -Linkeroption festgelegt oder gelöscht.

die 4-Gigabyte-Optimierung (4GT), auch bekannt als Anwendungs Speicher Optimierung oder der/3GB-Switch, ist eine Technologie (gilt nur für 32-Bit-Systeme), die den Umfang des für Benutzermodusanwendungen verfügbaren virtuellen Adressraums ändert. Wenn Sie diese Technologie aktivieren, verringert sich die Gesamtgröße des virtuellen System Adressraums und somit die Maximums der Systemressourcen. Weitere Informationen finden Sie unter [Was ist 4GT]( /previous-versions/windows/it-pro/windows-server-2003/cc786709(v=ws.10)).

Die Grenzwerte für den physischen Speicher für 32-Bit-Plattformen hängen auch von der [physischen Adress Erweiterung](physical-address-extension.md) (PE) ab, mit der 32-Bit-Windows-Systeme mehr als 4 GB physischen Arbeitsspeicher verwenden können.

## <a name="memory-and-address-space-limits"></a>Speicher-und Adressraum Limits

In der folgenden Tabelle sind die Grenzwerte für den Arbeitsspeicher und den Adressraum für unterstützte Versionen von Windows angegeben. Sofern nicht anders angegeben, gelten die Grenzwerte in dieser Tabelle für alle unterstützten Releases.



| Arbeitsspeichertyp                                                                                   | Limit für x86                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Limit in 64-Bit-Fenstern                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Virtueller Adressraum im Benutzermodus für jeden 32-Bit-Prozess<br/>                            | 2 GB<br/> Bis zu 3 GB mit **Abbild \_ Datei für \_ große \_ Adressen \_** und 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2 GB mit abgelöschter **Abbild \_ Datei \_ \_ \_** (Standard)<br/> 4 GB mit abgeleggelegt- **Abbild \_ Datei für \_ große \_ Adressen \_**<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Virtueller Adressraum im Benutzermodus für jeden 64-Bit-Prozess<br/>                            | Nicht verfügbar<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Mit Image \_ Datei \_ für \_ großen \_ Adress** Satz (Standard):<br/> **x64: Windows 8.1 und Windows Server 2012 R2 oder höher:** 128 TB<br/> **x64: Windows 8 und Windows Server 2012 oder früher** 8 TB<br/> **Intel Itanium-basierte Systeme:** 7 TB<br/> <br/> 2 GB mit abgelöschter **Abbild \_ Datei \_ \_ \_**<br/>                                                                                                                                                                                              |
| Virtueller Adressraum im Kernelmodus<br/>                                                  | 2 GB<br/> Zwischen 1 GB und maximal 2 GB mit 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Windows 8.1 und Windows Server 2012 R2 oder höher:** 128 TB<br/> **Windows 8 und Windows Server 2012 oder früher** 8 TB <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Auslagerungs Pool<br/>                                                                         | 384 GB oder systemcommit-Limit, je nachdem, welcher Wert kleiner ist. **Windows 8.1 und Windows Server 2012 R2:** 15,5 TB oder systemcommit-Limit, je nachdem, welcher Wert kleiner ist. <br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Beschränkt durch den verfügbaren virtuellen Adressraum im Kernel Modus. Ab Windows Vista mit Service Pack 1 (SP1) kann der ausgelagerten Pool auch durch den Registrierungsschlüssel Wert " [pgedpoollimit](memory-management-registry-keys.md) " eingeschränkt werden.<br/> **Windows Home Server und Windows Server 2003:** 530 MB<br/> **Windows XP:** 490 MB<br/> <br/>                                                                                                 | 384 GB oder systemcommit-Limit, je nachdem, welcher Wert kleiner ist **Windows 8.1 und Windows Server 2012 R2:** 15,5 TB oder systemcommit-Limit, je nachdem, welcher Wert kleiner ist. <br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** 128 GB oder systemcommit-Limit, je nachdem, welcher Wert kleiner ist.<br/> **Windows Server 2003 und Windows XP:** Bis zu 128 GB, je nach Konfiguration und RAM.<br/> <br/>                                                                                |
| Nicht Auslagerungs Pool<br/>                                                                      | 75% RAM oder 2 GB, je nachdem, welcher Wert kleiner ist. **Windows 8.1 und Windows Server 2012 R2:** RAM oder 16 TB, je nachdem, welcher Wert kleiner ist (Adressraum ist auf 2 x RAM beschränkt).<br/> **Windows Vista:** Nur durch den virtuellen Adressraum im Kernel Modus und den physischen Arbeitsspeicher beschränkt. Ab Windows Vista mit SP1 kann der nicht Auslagerungs Pool auch durch den Registrierungsschlüssel Wert " [nonteipoollimit](memory-management-registry-keys.md) " eingeschränkt werden.<br/> **Windows Home Server, Windows Server 2003 und Windows XP:** 256 MB oder 128 MB mit 4GT.<br/> <br/>                                                                                                                                                 | RAM oder 128 GB, je nachdem, welcher Wert kleiner ist (Adressraum ist auf 2 x RAM beschränkt) **Windows 8.1 und Windows Server 2012 R2:** RAM oder 16 TB, je nachdem, welcher Wert kleiner ist (Adressraum ist auf 2 x RAM beschränkt).<br/> **Windows Server 2008 R2, Windows 7 und Windows Server 2008:** 75% RAM bis maximal 128 GB<br/> **Windows Vista:** 40% RAM bis maximal 128 GB.<br/> **Windows Server 2003 und Windows XP:** Bis zu 128 GB, je nach Konfiguration und RAM.<br/> <br/> |
| Virtueller Adressraum des System Caches (physische Größe nur durch physischen Speicher beschränkt)<br/> | Beschränkt durch den verfügbaren virtuellen Adressraum für den Kernel Modus oder den Registrierungsschlüssel Wert " [systemcachelimit](memory-management-registry-keys.md) ".<br/> **Windows 8.1 und Windows Server 2012 R2:** 16 TB.<br/> **Windows Vista:** Beschränkt auf den virtuellen Adressraum im Kernel Modus. Ab Windows Vista mit SP1 kann der virtuelle Adressraum des System Caches auch durch den Registrierungsschlüssel Wert " [systemcachelimit](memory-management-registry-keys.md) " eingeschränkt werden.<br/> **Windows Home Server, Windows Server 2003 und Windows XP:** 860 MB mit dem Registrierungs Schlüsselsatz [LargeSystemCache](/previous-versions/windows/it-pro/windows-server-2003/cc784562(v=ws.10)) und ohne 4GT; bis zu 448 MB mit 4GT.<br/> <br/> | Immer 1 TB, unabhängig von physischem RAM **Windows 8.1 und Windows Server 2012 R2:** 16 TB.<br/> **Windows Server 2003 und Windows XP:** Bis zu 1 TB abhängig von Konfiguration und RAM.<br/> <br/>                                                                                                                                                                                                                                                                                            |



 

## <a name="physical-memory-limits-windows-10"></a>Grenzwerte für den physischen Speicher: Windows 10

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows 10 angegeben.



| Version               | Limit für x86    | Limit für x64     |
|-----------------------|-----------------|------------------|
| Windows 10 Enterprise | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Education  | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Pro for Workstations  | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Pro        | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Home       | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2016"></a>Grenzwerte für den physischen Speicher: Windows Server 2016

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2016 angegeben.



| Version                        | Limit für x64     |
|--------------------------------|------------------|
| Windows Server 2016 Datacenter | 24 TB<br/> |
| Windows Server 2016 Standard   | 24 TB<br/> |



 

## <a name="physical-memory-limits-windows-8"></a>Grenzwerte für den physischen Speicher: Windows 8

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows 8 aufgeführt.



| Version                | Limit für x86    | Limit für x64      |
|------------------------|-----------------|-------------------|
| Windows 8 Enterprise   | 4 GB<br/> | 512 GB<br/> |
| Windows 8 Professional | 4 GB<br/> | 512 GB<br/> |
| Windows 8              | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2012"></a>Grenzwerte für den physischen Speicher: Windows Server 2012

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2012 angegeben. Windows Server 2012 ist nur in x64-Editionen verfügbar.



| Version                               | Limit für x64     |
|---------------------------------------|------------------|
| Windows Server 2012 Datacenter        | 4 TB<br/>  |
| Windows Server 2012 Standard          | 4 TB<br/>  |
| Windows Server 2012 Essentials        | 64 GB<br/> |
| Windows Server 2012 Foundation        | 32 GB<br/> |
| Windows Storage Server 2012 Workgroup | 32 GB<br/> |
| Windows Storage Server 2012 Standard  | 4 TB<br/>  |
| Hyper-V Server 2012                   | 4 TB<br/>  |



 

## <a name="physical-memory-limits-windows-7"></a>Grenzwerte für den physischen Speicher: Windows 7

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows 7 aufgeführt.



| Version                | Limit für x86    | Limit für x64      |
|------------------------|-----------------|-------------------|
| Windows 7 Ultimate     | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Enterprise   | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Professional | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows 7 Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows 7 Starter      | 2 GB<br/> | –<br/>    |



 

## <a name="physical-memory-limits-windows-server-2008-r2"></a>Grenzwerte für den physischen Speicher: Windows Server 2008 R2

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2008 R2 angegeben. Windows Server 2008 R2 ist nur in 64-Bit-Editionen verfügbar.



| Version                                          | Limit für x64      | Limit für ia64   |
|--------------------------------------------------|-------------------|-----------------|
| Windows Server 2008 R2 Datacenter                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 Enterprise                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 für Itanium-basierte Systeme |                   | 2 TB<br/> |
| Windows Server 2008 R2 Foundation                | 8 GB<br/>   |                 |
| Windows Server 2008 R2 Standard                  | 32 GB<br/>  |                 |
| Windows HPC Server 2008 R2                       | 128 GB<br/> |                 |
| Windows Web Server 2008 R2                       | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-server-2008"></a>Grenzwerte für den physischen Speicher: Windows Server 2008

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2008 angegeben. Bei Grenz [Werten, die](physical-address-extension.md) größer als 4 GB für 32-Bit-Windows sind, wird davon ausgegangen, dass die Option



| Version                                       | Limit für x86     | Limit für x64      | Limit für ia64   |
|-----------------------------------------------|------------------|-------------------|-----------------|
| Windows Server 2008 Datacenter                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 Enterprise                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 HPC Edition               |                  | 128 GB<br/> |                 |
| Windows Server 2008 Standard                  | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Server 2008 für Itanium-basierte Systeme |                  |                   | 2 TB<br/> |
| Windows Small Business Server 2008            | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Web Server 2008                       | 4 GB<br/>  | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-vista"></a>Grenzwerte für den physischen Speicher: Windows Vista

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Vista aufgeführt.



| Version                    | Limit für x86    | Limit für x64      |
|----------------------------|-----------------|-------------------|
| Windows Vista Ultimate     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Enterprise   | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Business     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows Vista Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows Vista Starter      | 1 GB<br/> |                   |



 

## <a name="physical-memory-limits-windows-home-server"></a>Grenzwerte für den physischen Speicher: Windows Home Server

Windows Home Server ist nur in einer 32-Bit-Edition verfügbar. Das Limit für den physischen Speicher beträgt 4 GB.

## <a name="physical-memory-limits-windows-server-2003-r2"></a>Grenzwerte für den physischen Speicher: Windows Server 2003 R2

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2003 R2 angegeben. Bei Grenzwerten von mehr als 4 GB für 32-Bit-Windows wird davon ausgegangen, dass die [Option für die](physical-address-extension.md)



| Version                                              | Limit für x86                                 | Limit für x64     |
|------------------------------------------------------|----------------------------------------------|------------------|
| Windows Server 2003 R2 Datacenter Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Enterprise Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-2-sp2"></a>Grenzwerte für den physischen Speicher: Windows Server 2003 mit Service Pack 2 (SP2)

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2003 mit Service Pack 2 (SP2) angegeben. Bei Grenzwerten von mehr als 4 GB für 32-Bit-Windows wird davon ausgegangen, dass die [Option für die](physical-address-extension.md)



| Version                                                                      | Limit für x86                                 | Limit für x64     | Limit für ia64   |
|------------------------------------------------------------------------------|----------------------------------------------|------------------|-----------------|
| Windows Server 2003 mit Service Pack 2 (SP2), Datacenter Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 mit Service Pack 2 (SP2), Enterprise Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 mit Service Pack 2 (SP2), Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |                 |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-1-sp1"></a>Grenzwerte für den physischen Speicher: Windows Server 2003 mit Service Pack 1 (SP1)

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2003 mit Service Pack 1 (SP1) aufgeführt. Bei Grenzwerten von mehr als 4 GB für 32-Bit-Windows wird davon ausgegangen, dass die [Option für die](physical-address-extension.md)



| Version                                                                      | Limit für x86                                 | Limit für x64        | Limit für ia64   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------|-----------------|
| Windows Server 2003 mit Service Pack 1 (SP1), Datacenter Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 mit Service Pack 1 (SP1), Enterprise Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 mit Service Pack 1 (SP1), Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/>    |                 |



 

## <a name="physical-memory-limits-windows-server-2003"></a>Grenzwerte für den physischen Speicher: Windows Server 2003

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2003 angegeben. Bei Grenzwerten von mehr als 4 GB für 32-Bit-Windows wird davon ausgegangen, dass die [Option für die](physical-address-extension.md)



| Version                                                    | Limit für x86                                 | Limit für ia64     |
|------------------------------------------------------------|----------------------------------------------|-------------------|
| Windows Server 2003 Datacenter Edition<br/>         | 64 GB<br/> (16 GB mit 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003 Enterprise Edition<br/>         | 64 GB<br/> (16 GB mit 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003 Standard Edition<br/>           | 4 GB<br/>                              |                   |
| Windows Server 2003 Web Edition<br/>                | 2 GB<br/>                              |                   |
| Windows Small Business Server 2003<br/>              | 4 GB<br/>                              |                   |
| Windows Compute Cluster Server 2003<br/>             |                                              | 32 GB<br/>  |
| Windows Storage Server 2003, Enterprise Edition<br/> | 8 GB<br/>                              |                   |
| Windows Storage Server 2003<br/>                     | 4 GB<br/>                              |                   |



 

## <a name="physical-memory-limits-windows-xp"></a>Grenzwerte für den physischen Speicher: Windows XP

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows XP aufgeführt.



| Version                    | Limit für x86      | Limit für x64      | Limit für ia64                     |
|----------------------------|-------------------|-------------------|-----------------------------------|
| Windows XP                 | 4 GB<br/>   | 128 GB<br/> | 128 GB (nicht unterstützt)<br/> |
| Windows XP Starter Edition | 512 MB<br/> | –<br/>    | –<br/>                    |



 

## <a name="physical-memory-limits-windows-embedded"></a>Grenzwerte für den physischen Speicher: Windows Embedded

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Embedded aufgeführt.



| Version                                   | Limit für x86    | Limit für x64      |
|-------------------------------------------|-----------------|-------------------|
| Windows XP Embedded<br/>            | 4 GB<br/> |                   |
| Windows Embedded Standard 2009<br/> | 4 GB<br/> |                   |
| Windows Embedded Standard 7<br/>    | 4 GB<br/> | 192 GB<br/> |



 

## <a name="how-graphics-cards-and-other-devices-affect-memory-limits"></a>Auswirkungen von Grafikkarten und anderen Geräten auf Arbeitsspeicher Grenzwerte

Geräte müssen Ihren Arbeitsspeicher unterhalb von 4 GB zuordnen, um die Kompatibilität mit nicht-eindimensionalen Windows-Releases zu unterstützen. Wenn das System über 4 GB RAM verfügt, ist es daher entweder deaktiviert oder wird durch das BIOS über 4 GB neu zugeordnet. Wenn der Arbeitsspeicher neu zugeordnet wird, kann dieser Arbeitsspeicher von x64-Fenstern verwendet werden. X86-Client Versionen von Windows unterstützen keinen physischen Speicher oberhalb der 4-GB-Markierung, sodass Sie nicht auf diese neu zugeordnete Bereiche zugreifen können. Alle x64-Windows-oder x86-Server Releases sind möglich.

X86-Client Versionen mit aktiviertem aktiviertem paar verfügen über einen verwendbaren physischen Adressraum von 37-Bit (128 GB). Der Grenzwert, den diese Versionen erzwingen, ist die höchste zulässige physische RAM-Adresse, nicht die Größe des e/a-Speicherplatzes. Dies bedeutet, dass die von einem Benutzer abhängigen Treiber bei Bedarf tatsächlich physischen Speicherplatz über 4 GB verwenden können. Beispielsweise könnten Treiber die "verlorenen" Speicherbereiche, die oberhalb von 4 GB liegen, zuordnen und diesen Speicher als RAM-Datenträger verfügbar machen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[4-Gigabyte-Optimierung](4-gigabyte-tuning.md)
</dt> <dt>

[**Bild \_ Datei mit \_ hoher \_ Adresse \_**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image)
</dt> <dt>

[Physical Address Extension](physical-address-extension.md)
</dt> </dl>

 

 
