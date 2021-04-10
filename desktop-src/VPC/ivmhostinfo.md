---
title: Ivmhostinfo-Schnittstelle (vpccominterfaces. h)
description: Ruft Informationen über den Host Computer ab. Ein ivmhostinfo-Objekt wird von der ivmvirtualpc-Hostinfo-Eigenschaft zurückgegeben.
ms.assetid: f30fa377-2067-4e03-bc6e-2ada62fc56b4
keywords:
- Ivmhostinfo Interface Virtual PC
- Virtueller Computer ivmhostinfo Interface, beschrieben
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
ms.openlocfilehash: d4ca5f296dd4a7437ea136dbaee0d04c68a93efc
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103594"
---
# <a name="ivmhostinfo-interface"></a>Ivmhostinfo-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Ruft Informationen über den Host Computer ab. Ein **ivmhostinfo** -Objekt wird von der [**ivmvirtualpc:: Hostinfo**](ivmvirtualpc-hostinfo.md) -Eigenschaft zurückgegeben.

## <a name="members"></a>Member

Die **ivmhostinfo** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmhostinfo** verfügt auch über die folgenden Typen von Membern:

-   [Eigenschaften](#properties)

### <a name="properties"></a>Eigenschaften

Die **ivmhostinfo** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                                  | Zugriffstyp          | BESCHREIBUNG                                                                                        |
|:------------------------------------------------------------------------------------------|:---------------------|:---------------------------------------------------------------------------------------------------|
| [**Dvddrives**](ivmhostinfo-dvddrives.md)<br/>                                     | Schreibgeschützt<br/> | Die Laufwerk Buchstaben, die Host-CD-und DVD-Geräten zugeordnet sind.<br/>                              |
| [**Floppydrives**](ivmhostinfo-floppydrives.md)<br/>                               | Schreibgeschützt<br/> | Die den Host Disketten zugeordneten Laufwerk Buchstaben.<br/>                                   |
| [**Logicalprocessorcount**](ivmhostinfo-logicalprocessorcount.md)<br/>             | Schreibgeschützt<br/> | Die Anzahl der logischen Prozessoren auf dem Host Computer.<br/>                                   |
| [**Arbeitsspeicher**](ivmhostinfo-memory.md)<br/>                                           | Schreibgeschützt<br/> | Die Gesamtmenge an physischem Arbeitsspeicher auf dem Host Computer (in Megabyte).<br/>                  |
| [**Memorynütz**](ivmhostinfo-memoryavail.md)<br/>                                 | Schreibgeschützt<br/> | Die Menge des verfügbaren physischen Speichers auf dem Host Computer (in Megabyte).<br/>              |
| [**Memoryavailstring**](ivmhostinfo-memoryavailstring.md)<br/>                     | Schreibgeschützt<br/> | Die Menge des verfügbaren physischen Speichers auf dem Host Computer (in Megabyte) als Zeichenfolge.<br/> |
| [**Memorytotalstring**](ivmhostinfo-memorytotalstring.md)<br/>                     | Schreibgeschützt<br/> | Die Gesamtmenge an physischem Arbeitsspeicher auf dem Host Computer (in Megabyte) als Zeichenfolge.<br/>     |
| [**MMX**](ivmhostinfo-mmx.md)<br/>                                                 | Schreibgeschützt<br/> | Gibt an, ob der Prozessor den MMX-Anweisungs Satz unterstützt.<br/>                       |
| [**Netzwerkadapter**](ivmhostinfo-networkadapters.md)<br/>                         | Schreibgeschützt<br/> | Eine Aufzähl Bare Auflistung von NICs auf dem Host Computer.<br/>                                   |
| [**"Networkaddresses"**](ivmhostinfo-networkaddresses.md)<br/>                       | Schreibgeschützt<br/> | Eine Aufzähl Bare Auflistung von TCP/IP-Adressen auf dem Host Computer.<br/>                       |
| [**OperatingSystem**](ivmhostinfo-operatingsystem.md)<br/>                         | Schreibgeschützt<br/> | Das Betriebssystem, das auf dem Host Computer ausgeführt wird.<br/>                                       |
| [**OSMajorVersion**](ivmhostinfo-osmajorversion.md)<br/>                           | Schreibgeschützt<br/> | Die Hauptversion des Betriebssystems, das auf dem Host Computer ausgeführt wird.<br/>                  |
| [**OSMinorVersion**](ivmhostinfo-osminorversion.md)<br/>                           | Schreibgeschützt<br/> | Die neben Version des Betriebssystems, das auf dem Host Computer ausgeführt wird.<br/>                  |
| [**Osservicepackstring**](ivmhostinfo-osservicepackstring.md)<br/>                 | Schreibgeschützt<br/> | Die Service Pack Informationen des Betriebssystems, das auf dem Host Computer ausgeführt wird.<br/>       |
| [**Osversionstring**](ivmhostinfo-osversionstring.md)<br/>                         | Schreibgeschützt<br/> | Die Betriebssystemversion, die auf dem Host Computer ausgeführt wird.<br/>                               |
| [**ParallelPort**](ivmhostinfo-parallelport.md)<br/>                               | Schreibgeschützt<br/> | Der parallele Port des Hosts, der an den Gast angefügt werden kann.<br/>                               |
| [**Physicalprocessorcount**](ivmhostinfo-physicalprocessorcount.md)<br/>           | Schreibgeschützt<br/> | Die Anzahl der physischen Prozessoren auf dem Host Computer.<br/>                                  |
| [**Processorfeaturesstring**](ivmhostinfo-processorfeaturesstring.md)<br/>         | Schreibgeschützt<br/> | Die Liste der vom Host Prozessor unterstützten Funktionen.<br/>                                   |
| [**Processormanufacturerstring**](ivmhostinfo-processormanufacturerstring.md)<br/> | Schreibgeschützt<br/> | Der Hersteller des Host Prozessors.<br/>                                                 |
| [**ProcessorSpeed**](ivmhostinfo-processorspeed.md)<br/>                           | Schreibgeschützt<br/> | Die Geschwindigkeit des Host Prozessors in Megahertz (MHz) oder Gigahertz (GHz).<br/>                 |
| [**Processorspeedstring**](ivmhostinfo-processorspeedstring.md)<br/>               | Schreibgeschützt<br/> | Die Geschwindigkeit des Host Prozessors in Megahertz oder Gigahertz als Zeichenfolge.<br/>                |
| [**Processorversionstring**](ivmhostinfo-processorversionstring.md)<br/>           | Schreibgeschützt<br/> | Die Version des Host Prozessors.<br/>                                                      |
| [**SerialPorts**](ivmhostinfo-serialports.md)<br/>                                 | Schreibgeschützt<br/> | Die seriellen Anschluss Namen, die den seriellen Ports des Hosts zugeordnet sind.<br/>                                |
| [**SSE**](ivmhostinfo-sse.md)<br/>                                                 | Schreibgeschützt<br/> | Gibt an, ob der Prozessor den SSE-Anweisungs Satz unterstützt.<br/>                       |
| [**SSE2**](ivmhostinfo-sse2.md)<br/>                                               | Schreibgeschützt<br/> | Gibt an, ob der Prozessor den SSE2-Anweisungs Satz unterstützt.<br/>                      |
| [**Threednow**](ivmhostinfo-threednow.md)<br/>                                     | Schreibgeschützt<br/> | Gibt an, ob der Prozessor den 3DNow-Anweisungs Satz unterstützt.<br/>                     |
| [**UtcTime**](ivmhostinfo-utctime.md)<br/>                                         | Schreibgeschützt<br/> | Die UTC-Zeit auf dem Host Computer.<br/>                                                       |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmhostinfo ist als 5b5cf343-05ad-453b-be99-adf4e27b2ebc definiert.<br/>                |



 

