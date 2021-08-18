---
title: IVMHostInfo-Schnittstelle (VPCCOMInterfaces.h)
description: Ruft Informationen zum Hostcomputer ab. Ein IVMHostInfo-Objekt wird von der IVMVirtualPC-HostInfo-Eigenschaft zurückgegeben.
ms.assetid: f30fa377-2067-4e03-bc6e-2ada62fc56b4
keywords:
- IVMHostInfo-Schnittstelle Virtueller PC
- IVMHostInfo-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMHostInfo
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da45459379c468839b0bf48ae134db1885ea25acce5ac3befa289ae15ee6fe8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119974260"
---
# <a name="ivmhostinfo-interface"></a>IVMHostInfo-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Ruft Informationen zum Hostcomputer ab. Ein **IVMHostInfo-Objekt** wird von der [**IVMVirtualPC::HostInfo-Eigenschaft**](ivmvirtualpc-hostinfo.md) zurückgegeben.

## <a name="members"></a>Member

Die **IVMHostInfo-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMHostInfo** verfügt auch über diese Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **IVMHostInfo-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                                  | Zugriffstyp          | BESCHREIBUNG                                                                                        |
|:------------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**DVDDrives**](ivmhostinfo-dvddrives.md)<br/>                                     | Schreibgeschützt<br/> | Die Laufwerkbuchstaben, die Host-CD- und DVD-Geräten zugeordnet sind.<br/>                              |
| [**FloppyDrives**](ivmhostinfo-floppydrives.md)<br/>                               | Schreibgeschützt<br/> | Die Laufwerkbuchstaben, die Host-Diskettenlaufwerken zugeordnet sind.<br/>                                   |
| [**LogicalProcessorCount**](ivmhostinfo-logicalprocessorcount.md)<br/>             | Schreibgeschützt<br/> | Die Anzahl der logischen Prozessoren auf dem Hostcomputer.<br/>                                   |
| [**Speicher**](ivmhostinfo-memory.md)<br/>                                           | Schreibgeschützt<br/> | Die Gesamtmenge des physischen Arbeitsspeichers auf dem Hostcomputer in Megabyte.<br/>                  |
| [**MemoryAvail**](ivmhostinfo-memoryavail.md)<br/>                                 | Schreibgeschützt<br/> | Die Menge des verfügbaren physischen Arbeitsspeichers auf dem Hostcomputer in Megabyte.<br/>              |
| [**MemoryAvailString**](ivmhostinfo-memoryavailstring.md)<br/>                     | Schreibgeschützt<br/> | Die Menge des verfügbaren physischen Arbeitsspeichers auf dem Hostcomputer in Megabyte als Zeichenfolge.<br/> |
| [**MemoryTotalString**](ivmhostinfo-memorytotalstring.md)<br/>                     | Schreibgeschützt<br/> | Die Gesamtmenge des physischen Arbeitsspeichers auf dem Hostcomputer in Megabyte als Zeichenfolge.<br/>     |
| [**Mmx**](ivmhostinfo-mmx.md)<br/>                                                 | Schreibgeschützt<br/> | Gibt an, ob der Prozessor den MMX-Anweisungssatz unterstützt.<br/>                       |
| [**NetworkAdapters**](ivmhostinfo-networkadapters.md)<br/>                         | Schreibgeschützt<br/> | Eine aufzählbare Sammlung von NICs auf dem Hostcomputer.<br/>                                   |
| [**NetworkAddresses**](ivmhostinfo-networkaddresses.md)<br/>                       | Schreibgeschützt<br/> | Eine aufzählbare Auflistung von TCP/IP-Adressen auf dem Hostcomputer.<br/>                       |
| [**Operatingsystem**](ivmhostinfo-operatingsystem.md)<br/>                         | Schreibgeschützt<br/> | Das Betriebssystem, das auf dem Hostcomputer ausgeführt wird.<br/>                                       |
| [**OSMajorVersion**](ivmhostinfo-osmajorversion.md)<br/>                           | Schreibgeschützt<br/> | Die Hauptversion des Betriebssystems, das auf dem Hostcomputer ausgeführt wird.<br/>                  |
| [**OSMinorVersion**](ivmhostinfo-osminorversion.md)<br/>                           | Schreibgeschützt<br/> | Die Nebenversion des Betriebssystems, das auf dem Hostcomputer ausgeführt wird.<br/>                  |
| [**OSServicePackString**](ivmhostinfo-osservicepackstring.md)<br/>                 | Schreibgeschützt<br/> | Die Service Pack-Informationen des Betriebssystems, das auf dem Hostcomputer ausgeführt wird.<br/>       |
| [**OSVersionString**](ivmhostinfo-osversionstring.md)<br/>                         | Schreibgeschützt<br/> | Die Betriebssystemversion, die auf dem Hostcomputer ausgeführt wird.<br/>                               |
| [**ParallelPort**](ivmhostinfo-parallelport.md)<br/>                               | Schreibgeschützt<br/> | Der parallele Hostport, der an den Gast angefügt werden kann.<br/>                               |
| [**PhysicalProcessorCount**](ivmhostinfo-physicalprocessorcount.md)<br/>           | Schreibgeschützt<br/> | Die Anzahl der physischen Prozessoren auf dem Hostcomputer.<br/>                                  |
| [**ProcessorFeaturesString**](ivmhostinfo-processorfeaturesstring.md)<br/>         | Schreibgeschützt<br/> | Die Liste der vom Hostprozessor unterstützten Features.<br/>                                   |
| [**ProcessorManufacturerString**](ivmhostinfo-processormanufacturerstring.md)<br/> | Schreibgeschützt<br/> | Der Hersteller des Hostprozessors.<br/>                                                 |
| [**ProcessorSpeed**](ivmhostinfo-processorspeed.md)<br/>                           | Schreibgeschützt<br/> | Die Geschwindigkeit des Hostprozessors in Megahertz (MHz) oder Gigahertz (GHz).<br/>                 |
| [**ProcessorSpeedString**](ivmhostinfo-processorspeedstring.md)<br/>               | Schreibgeschützt<br/> | Die Geschwindigkeit des Hostprozessors in Megahertz oder Gigahertz als Zeichenfolge.<br/>                |
| [**ProcessorVersionString**](ivmhostinfo-processorversionstring.md)<br/>           | Schreibgeschützt<br/> | Die Version des Hostprozessors.<br/>                                                      |
| [**SerialPorts**](ivmhostinfo-serialports.md)<br/>                                 | Schreibgeschützt<br/> | Die seriellen Portnamen, die seriellen Hostports zugeordnet sind.<br/>                                |
| [**SSE**](ivmhostinfo-sse.md)<br/>                                                 | Schreibgeschützt<br/> | Gibt an, ob der Prozessor den SSE-Anweisungssatz unterstützt.<br/>                       |
| [**SSE2**](ivmhostinfo-sse2.md)<br/>                                               | Schreibgeschützt<br/> | Gibt an, ob der Prozessor den SSE2-Anweisungssatz unterstützt.<br/>                      |
| [**ThreeDNow**](ivmhostinfo-threednow.md)<br/>                                     | Schreibgeschützt<br/> | Gibt an, ob der Prozessor den 3DNow-Anweisungssatz unterstützt.<br/>                     |
| [**UTCTime**](ivmhostinfo-utctime.md)<br/>                                         | Schreibgeschützt<br/> | Die UTC-Zeit auf dem Hostcomputer.<br/>                                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMHostInfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.<br/>                |



 

