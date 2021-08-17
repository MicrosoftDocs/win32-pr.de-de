---
description: In diesem Thema werden die Arbeitsspeicherlimits für unterstützte Windows und Windows Serverversionen beschrieben.
ms.assetid: de09c8af-0ed8-4fd4-b8e8-2c921aafe6f2
title: Grenzwerte für den Arbeitsspeicher für Versionen von Windows und Windows Server
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8d2b11b636fcbcd3338986aa4ce88388f3b722045eee895e4acb1b62d5920eb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117992752"
---
# <a name="memory-limits-for-windows-and-windows-server-releases"></a>Grenzwerte für den Arbeitsspeicher für Versionen von Windows und Windows Server

In diesem Thema werden die Arbeitsspeicherlimits für unterstützte Windows und Windows Serverversionen beschrieben.

-   [Grenzwerte für Arbeitsspeicher und Adressraum](#memory-limits-for-windows-and-windows-server-releases)
-   [Grenzwerte für physischen Speicher: Windows 10](#physical-memory-limits-windows-10)
-   [Grenzwerte für physischen Speicher: Windows Server 2016](#physical-memory-limits-windows-server-2016)
-   [Grenzwerte für physischen Speicher: Windows 8](#physical-memory-limits-windows-8)
-   [Grenzwerte für physischen Speicher: Windows Server 2012](#physical-memory-limits-windows-server-2012)
-   [Grenzwerte für physischen Speicher: Windows 7](#physical-memory-limits-windows-7)
-   [Grenzwerte für physischen Arbeitsspeicher: Windows Server 2008 R2](#physical-memory-limits-windows-server-2008-r2)
-   [Grenzwerte für physischen Arbeitsspeicher: Windows Server 2008](#physical-memory-limits-windows-server-2008-r2)
-   [Grenzwerte für physischen Speicher: Windows Vista](#physical-memory-limits-windows-vista)
-   [Grenzwerte für physischen Speicher: Windows Home Server](#physical-memory-limits-windows-home-server)
-   [Grenzwerte für physischen Arbeitsspeicher: Windows Server 2003 R2](#physical-memory-limits-windows-server-2003-r2)
-   [Grenzwerte für physischen Windows Server 2003 mit Service Pack 2 (SP2)](#physical-memory-limits-windows-server-2003-with-service-pack-2-sp2)
-   [Grenzwerte für physischen Windows Server 2003 mit Service Pack 1 (SP1)](#physical-memory-limits-windows-server-2003-with-service-pack-1-sp1)
-   [Grenzwerte für physischen Arbeitsspeicher: Windows Server 2003](#physical-memory-limits-windows-server-2003-r2)
-   [Grenzwerte für physischen Speicher: Windows XP](#physical-memory-limits-windows-xp)
-   [Grenzwerte für physischen Speicher: Windows Embedded](#physical-memory-limits-windows-embedded)
-   [Auswirkungen von Grafikkarten und anderen Geräten auf Arbeitsspeicherlimits](#how-graphics-cards-and-other-devices-affect-memory-limits)
-   [Zugehörige Themen](#related-topics)

Die Grenzwerte für Arbeitsspeicher und Adressraum variieren je nach Plattform, Betriebssystem und davon, ob der **IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE-Wert** der [**LOADED \_ IMAGE-Struktur**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image) und die [4-Gigabyte-Optimierung](4-gigabyte-tuning.md) (4GT) verwendet werden. **IMAGE \_ FILE \_ LARGE \_ ADDRESS \_ AWARE** wird mithilfe der Linkeroption [/LARGEADDRESSAWARE](/cpp/build/reference/largeaddressaware-handle-large-addresses?view=vs-2019) festgelegt oder entfernt.

Die 4-Gigabyte-Optimierung (4GT), auch als Optimierung des Anwendungsspeichers oder des /3GB-Switches bezeichnet, ist eine Technologie (gilt nur für 32-Bit-Systeme), die die Menge des virtuellen Adressraums ändert, der für Benutzermodusanwendungen verfügbar ist. Durch die Aktivierung dieser Technologie wird die Gesamtgröße des virtuellen Adressraums des Systems und somit die Maximale anzahl von Systemressourcen reduziert. Weitere Informationen finden Sie unter [Was ist 4GT?]( /previous-versions/windows/it-pro/windows-server-2003/cc786709(v=ws.10))

Grenzwerte für physischen Speicher für 32-Bit-Plattformen hängen auch von der Physical [Address Extension](physical-address-extension.md) (PAE) ab, die es 32-Bit-Windows-Systemen ermöglicht, mehr als 4 GB physischen Speicher zu verwenden.

## <a name="memory-and-address-space-limits"></a>Grenzwerte für Arbeitsspeicher und Adressraum

In der folgenden Tabelle sind die Grenzwerte für Arbeitsspeicher und Adressraum für unterstützte Releases von Windows. Sofern nicht anders angegeben, gelten die Grenzwerte in dieser Tabelle für alle unterstützten Releases.



| Arbeitsspeichertyp                                                                                   | Limit für X86                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    | Limit in 64-Bit-Windows                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Virtueller Adressraum im Benutzermodus für jeden 32-Bit-Prozess<br/>                            | 2 GB<br/> Bis zu 3 GB mit **IMAGE FILE LARGE ADDRESS \_ \_ \_ \_ AWARE** und 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       | 2 GB mit **deaktivierter \_ \_ Bildverarbeitungsdatei (GROßE \_ ADRESSE) \_** (Standard)<br/> 4 GB mit **FESTGELEGTER \_ IMAGEDATEI \_ \_ (GROßE \_ ADRESSE)**<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| Virtueller Adressraum im Benutzermodus für jeden 64-Bit-Prozess<br/>                            | Nicht verfügbar<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Mit IMAGE \_ FILE \_ LARGE ADDRESS AWARE \_ \_ set** (Standardeinstellung):<br/> **x64: Windows 8.1 und Windows Server 2012 R2 oder höher:** 128 TB<br/> **x64: Windows 8 und Windows Server 2012 oder früher** 8 TB<br/> **Intel Itanium-basierte Systeme:** 7 TB<br/> <br/> 2 GB mit **2 GB, bei dem \_ IMAGEDATEI \_ \_ (GROßE \_ ADRESSE) nicht** mehr verfügbar ist<br/>                                                                                                                                                                                              |
| Virtueller Adressraum im Kernelmodus<br/>                                                  | 2 GB<br/> Von 1 GB bis maximal 2 GB mit 4GT<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              | **Windows 8.1 und Windows Server 2012 R2 oder höher:** 128 TB<br/> **Windows 8 und Windows Server 2012 oder früher** 8 TB <br/>                                                                                                                                                                                                                                                                                                                                                                                                                                 |
| Auspagepool<br/>                                                                         | 384 GB oder Grenzwert für System-Commits, je nach geringerer Größe. **Windows 8.1 und Windows Server 2012 R2:** 15,5 TB oder Grenzwert für System commit, je nach geringerer Größe. <br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** Begrenzt durch den verfügbaren virtuellen Adressraum im Kernelmodus. Ab Windows Vista mit Service Pack 1 (SP1) kann der ausgepackte Pool auch durch den [PagedPoolLimit-Registrierungsschlüsselwert](memory-management-registry-keys.md) eingeschränkt werden.<br/> **Windows Home Server und Windows Server 2003:** 530 MB<br/> **Windows XP:** 490 MB<br/> <br/>                                                                                                 | 384 GB oder Grenzwert für System-Commits, je nach kleinerem Windows 8.1 und **Windows Server 2012 R2:** 15,5 TB oder Grenzwert für System commit, je nach Größe. <br/> **Windows Server 2008 R2, Windows 7, Windows Server 2008 und Windows Vista:** 128 GB oder Grenzwert für System commit, je nach größe<br/> **Windows Server 2003 und Windows XP:** Je nach Konfiguration und RAM bis zu 128 GB.<br/> <br/>                                                                                |
| Nicht auspageer Pool<br/>                                                                      | 75 % ram oder 2 GB, je nach Größe. **Windows 8.1 und Windows Server 2012 R2:** RAM oder 16 TB, je nach Größe (Adressraum ist auf 2 x RAM beschränkt).<br/> **Windows Vista:** Beschränkt nur durch den virtuellen Adressraum und den physischen Speicher im Kernelmodus. Ab Windows Vista mit SP1 kann der nicht auspagete Pool auch durch den [Registrierungsschlüsselwert NonPagedPoolLimit](memory-management-registry-keys.md) eingeschränkt werden.<br/> **Windows Home Server, Windows Server 2003** und Windows XP: 256 MB oder 128 MB mit 4GT.<br/> <br/>                                                                                                                                                 | RAM oder 128 GB, je nach Größe (Adressraum ist auf 2 x RAM beschränkt) Windows 8.1 und **Windows Server 2012 R2:** RAM oder 16 TB, je nach Größe (Adressraum ist auf 2 x RAM beschränkt).<br/> **Windows Server 2008 R2, Windows 7 und Windows Server 2008:** 75 % ram bis maximal 128 GB<br/> **Windows Vista:** 40 % ram bis maximal 128 GB.<br/> **Windows Server 2003 und Windows XP:** Je nach Konfiguration und RAM bis zu 128 GB.<br/> <br/> |
| Virtueller Adressraum des Systemcaches (physische Größe ist nur durch physischen Arbeitsspeicher beschränkt)<br/> | Begrenzt durch den verfügbaren virtuellen Adressraum im Kernelmodus oder den [Registrierungsschlüsselwert SystemCacheLimit.](memory-management-registry-keys.md)<br/> **Windows 8.1 und Windows Server 2012 R2:** 16 TB.<br/> **Windows Vista:** Beschränkt nur durch den virtuellen Adressraum des Kernelmodus. Ab Windows Vista mit SP1 kann der virtuelle Adressraum des Systemcaches auch durch den [Registrierungsschlüsselwert SystemCacheLimit](memory-management-registry-keys.md) eingeschränkt werden.<br/> **Windows Home Server, Windows Server 2003** und Windows XP: 860 MB mit [festgelegten LargeSystemCache-Registrierungsschlüsseln](/previous-versions/windows/it-pro/windows-server-2003/cc784562(v=ws.10)) und ohne 4GT; bis zu 448 MB mit 4GT.<br/> <br/> | Immer 1 TB unabhängig vom physischen RAM **Windows 8.1 und Windows Server 2012 R2:** 16 TB.<br/> **Windows Server 2003 und Windows XP:** Je nach Konfiguration und RAM bis zu 1 TB.<br/> <br/>                                                                                                                                                                                                                                                                                            |



 

## <a name="physical-memory-limits-windows-10"></a>Grenzwerte für physischen Speicher: Windows 10

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows 10.



| Version               | Limit für X86    | Limit für X64     |
|-----------------------|-----------------|------------------|
| Windows 10 Enterprise | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Education  | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Pro for Workstations  | 4 GB<br/> | 6 TB<br/>   |
| Windows 10 Pro        | 4 GB<br/> | 2 TB<br/>   |
| Windows 10 Home       | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2016"></a>Grenzwerte für physischen Speicher: Windows Server 2016

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2016.



| Version                        | Limit für X64     |
|--------------------------------|------------------|
| Windows Server 2016 Datacenter | 24 TB<br/> |
| Windows Server 2016 Standard   | 24 TB<br/> |



 

## <a name="physical-memory-limits-windows-8"></a>Grenzwerte für physischen Speicher: Windows 8

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows 8.



| Version                | Limit für X86    | Limit für X64      |
|------------------------|-----------------|-------------------|
| Windows 8 Enterprise   | 4 GB<br/> | 512 GB<br/> |
| Windows 8 Professional | 4 GB<br/> | 512 GB<br/> |
| Windows 8              | 4 GB<br/> | 128 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2012"></a>Grenzwerte für physischen Speicher: Windows Server 2012

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2012. Windows Server 2012 ist nur in X64-Editionen verfügbar.



| Version                               | Limit für X64     |
|---------------------------------------|------------------|
| Windows Server 2012 Datacenter        | 4 TB<br/>  |
| Windows Server 2012 Standard          | 4 TB<br/>  |
| Windows Server 2012 Essentials        | 64 GB<br/> |
| Windows Server 2012 Foundation        | 32 GB<br/> |
| Windows Storage Server 2012 Workgroup | 32 GB<br/> |
| Windows Storage Server 2012 Standard  | 4 TB<br/>  |
| Hyper-V Server 2012                   | 4 TB<br/>  |



 

## <a name="physical-memory-limits-windows-7"></a>Grenzwerte für physischen Speicher: Windows 7

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows 7 angegeben.



| Version                | Limit für X86    | Limit für X64      |
|------------------------|-----------------|-------------------|
| Windows 7 Ultimate     | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Enterprise   | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Professional | 4 GB<br/> | 192 GB<br/> |
| Windows 7 Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows 7 Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows 7 Starter      | 2 GB<br/> | Nicht zutreffend<br/>    |



 

## <a name="physical-memory-limits-windows-server-2008-r2"></a>Grenzwerte für physischen Windows Server 2008 R2

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2008 R2 angegeben. Windows Server 2008 R2 ist nur in 64-Bit-Editionen verfügbar.



| Version                                          | Limit für X64      | Grenzwert für IA64   |
|--------------------------------------------------|-------------------|-----------------|
| Windows Server 2008 R2 Datacenter                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 Enterprise                | 2 TB<br/>   |                 |
| Windows Server 2008 R2 für Itanium-basierte Systeme |                   | 2 TB<br/> |
| Windows Server 2008 R2 Foundation                | 8 GB<br/>   |                 |
| Windows Server 2008 R2 Standard                  | 32 GB<br/>  |                 |
| Windows HPC Server 2008 R2                       | 128 GB<br/> |                 |
| Windows Web Server 2008 R2                       | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-server-2008"></a>Grenzwerte für physischen Arbeitsspeicher: Windows Server 2008

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2008 angegeben. Grenzwerte, die größer als 4 GB für 32-Bit-Windows, [dass PAE](physical-address-extension.md) aktiviert ist.



| Version                                       | Limit für X86     | Limit für X64      | Grenzwert für IA64   |
|-----------------------------------------------|------------------|-------------------|-----------------|
| Windows Server 2008 Datacenter                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 Enterprise                | 64 GB<br/> | 1 TB<br/>   |                 |
| Windows Server 2008 HPC Edition               |                  | 128 GB<br/> |                 |
| Windows Server 2008 Standard                  | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Server 2008 für Itanium-basierte Systeme |                  |                   | 2 TB<br/> |
| Windows Small Business Server 2008            | 4 GB<br/>  | 32 GB<br/>  |                 |
| Windows Web Server 2008                       | 4 GB<br/>  | 32 GB<br/>  |                 |



 

## <a name="physical-memory-limits-windows-vista"></a>Grenzwerte für physischen Speicher: Windows Vista

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Vista angegeben.



| Version                    | Limit für X86    | Limit für X64      |
|----------------------------|-----------------|-------------------|
| Windows Vista Ultimate     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Enterprise   | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Business     | 4 GB<br/> | 128 GB<br/> |
| Windows Vista Home Premium | 4 GB<br/> | 16 GB<br/>  |
| Windows Vista Home Basic   | 4 GB<br/> | 8 GB<br/>   |
| Windows Vista Starter      | 1 GB<br/> |                   |



 

## <a name="physical-memory-limits-windows-home-server"></a>Grenzwerte für physischen Speicher: Windows Home Server

Windows Home Server ist nur in einer 32-Bit-Edition verfügbar. Der Grenzwert für den physischen Arbeitsspeicher beträgt 4 GB.

## <a name="physical-memory-limits-windows-server-2003-r2"></a>Grenzwerte für physischen Arbeitsspeicher: Windows Server 2003 R2

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2003 R2 angegeben. Grenzwerte von mehr als 4 GB für 32-Bit-Windows, [dass PAE](physical-address-extension.md) aktiviert ist.



| Version                                              | Limit für X86                                 | Limit für X64     |
|------------------------------------------------------|----------------------------------------------|------------------|
| Windows Server 2003 R2 Datacenter Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Enterprise Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | 1 TB<br/>  |
| Windows Server 2003 R2 Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-2-sp2"></a>Grenzwerte für physischen Windows Server 2003 mit Service Pack 2 (SP2)

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2003 mit Service Pack 2 (SP2) angegeben. Grenzwerte von mehr als 4 GB für 32-Bit-Windows, [dass PAE](physical-address-extension.md) aktiviert ist.



| Version                                                                      | Limit für X86                                 | Limit für X64     | Grenzwert für IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|------------------|-----------------|
| Windows Server 2003 mit Service Pack 2 (SP2), Datacenter Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 mit Service Pack 2 (SP2), Enterprise Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | 1 TB<br/>  | 2 TB<br/> |
| Windows Server 2003 mit Service Pack 2 (SP2), Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/> |                 |



 

## <a name="physical-memory-limits-windows-server-2003-with-service-pack-1-sp1"></a>Grenzwerte für physischen Windows Server 2003 mit Service Pack 1 (SP1)

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2003 mit Service Pack 1 (SP1) angegeben. Grenzwerte von mehr als 4 GB für 32-Bit-Windows, [dass PAE](physical-address-extension.md) aktiviert ist.



| Version                                                                      | Limit für X86                                 | Limit für X64        | Grenzwert für IA64   |
|------------------------------------------------------------------------------|----------------------------------------------|---------------------|-----------------|
| Windows Server 2003 mit Service Pack 1 (SP1), Datacenter Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 mit Service Pack 1 (SP1), Enterprise Edition<br/> | 64 GB<br/> (16 GB mit 4GT)<br/> | X64 1 TB<br/> | 1 TB<br/> |
| Windows Server 2003 mit Service Pack 1 (SP1), Standard Edition<br/>   | 4 GB<br/>                              | 32 GB<br/>    |                 |



 

## <a name="physical-memory-limits-windows-server-2003"></a>Grenzwerte für physischen Arbeitsspeicher: Windows Server 2003

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Server 2003 angegeben. Grenzwerte von mehr als 4 GB für 32-Bit-Windows, [dass PAE](physical-address-extension.md) aktiviert ist.



| Version                                                    | Limit für X86                                 | Grenzwert für IA64     |
|------------------------------------------------------------|----------------------------------------------|-------------------|
| Windows Server 2003 Datacenter Edition<br/>         | 64 GB<br/> (16 GB mit 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003 Enterprise Edition<br/>         | 64 GB<br/> (16 GB mit 4GT)<br/> | 512 GB<br/> |
| Windows Server 2003 Standard Edition<br/>           | 4 GB<br/>                              |                   |
| Windows Server 2003 Web Edition<br/>                | 2 GB<br/>                              |                   |
| Windows Small Business Server 2003<br/>              | 4 GB<br/>                              |                   |
| Windows Compute Cluster Server 2003<br/>             |                                              | 32 GB<br/>  |
| Windows Storage Server 2003, Enterprise Edition<br/> | 8 GB<br/>                              |                   |
| Windows Storage Server 2003<br/>                     | 4 GB<br/>                              |                   |



 

## <a name="physical-memory-limits-windows-xp"></a>Grenzwerte für physischen Arbeitsspeicher: Windows XP

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows XP angegeben.



| Version                    | Limit für X86      | Limit für X64      | Grenzwert für IA64                     |
|----------------------------|-------------------|-------------------|-----------------------------------|
| Windows XP                 | 4 GB<br/>   | 128 GB<br/> | 128 GB (nicht unterstützt)<br/> |
| Windows XP Starter Edition | 512 MB<br/> | Nicht zutreffend<br/>    | Nicht zutreffend<br/>                    |



 

## <a name="physical-memory-limits-windows-embedded"></a>Grenzwerte für physischen Speicher: Windows Embedded

In der folgenden Tabelle sind die Grenzwerte für den physischen Speicher für Windows Embedded angegeben.



| Version                                   | Limit für X86    | Limit für X64      |
|-------------------------------------------|-----------------|-------------------|
| Windows XP Embedded<br/>            | 4 GB<br/> |                   |
| Windows Embedded Standard 2009<br/> | 4 GB<br/> |                   |
| Windows Embedded Standard 7<br/>    | 4 GB<br/> | 192 GB<br/> |



 

## <a name="how-graphics-cards-and-other-devices-affect-memory-limits"></a>Auswirkungen von Grafikkarten und anderen Geräten auf Arbeitsspeicherlimits

Geräte müssen ihren Arbeitsspeicher unter 4 GB zuordnen, um die Kompatibilität mit nicht PAE-orientierte Windows zu gewährleisten. Wenn das System also über 4 GB RAM verfügt, ist ein Teil davon entweder deaktiviert oder wird vom BIOS über 4 GB neu zugeordnet. Wenn der Arbeitsspeicher neu zugeordnet wird, können X64-Windows diesen Arbeitsspeicher verwenden. X86-Clientversionen von Windows unterstützen keinen physischen Speicher über der 4-GB-Marke, sodass sie nicht auf diese neu zugeordneten Regionen zugreifen können. Alle X64 Windows- oder X86-Serverversionen können dies.

X86-Clientversionen mit aktivierter PAE verfügen über einen nutzbaren physischen 37-Bit-Adressraum (128 GB). Der Grenzwert, den diese Versionen erlegen, ist die höchste zulässige physische RAM-Adresse, nicht die Größe des E/A-Speicherplatzes. Das bedeutet, dass PAE-orientierte Treiber tatsächlich physischen Speicherplatz über 4 GB verwenden können, wenn sie möchten. Treiber könnten beispielsweise die "verloren gegangenen" Speicherregionen zuordnen, die sich über 4 GB befinden, und diesen Arbeitsspeicher als RAM-Datenträger verfügbar machen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[4-Gigabyte-Optimierung](4-gigabyte-tuning.md)
</dt> <dt>

[**\_IMAGEDATEI, DIE GROßE ADRESSEN \_ \_ \_ KENNT**](/windows/win32/api/dbghelp/ns-dbghelp-loaded_image)
</dt> <dt>

[Physical Address Extension](physical-address-extension.md)
</dt> </dl>

 

 
