---
description: Die in der folgenden Tabelle aufgeführten Flags geben den Typ des E/A-Bus an, der vom Grafikadapter verwendet wird.
ms.assetid: 6c8ec020-5f12-453b-bbeb-3baabb1ca213
title: OPM-Bustypflags (Opmapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 26e4989a91c308a7dc82bb15e9cd577a6facd89a0a6de9a32f0ef95f400917ce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118972999"
---
# <a name="opm-bus-type-flags"></a>OPM-Bustypflags

Die in der folgenden Tabelle aufgeführten Flags geben den Typ des E/A-Bus an, der vom Grafikadapter verwendet wird.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_BUS_TYPE_OTHER"></span><span id="opm_bus_type_other"></span><dl> <dt>**OPM \_ BUS \_ TYPE \_ OTHER**</dt> <dt>0x00000000</dt> </dl>                                                                                                                                                                      | Gibt einen anderen Bustyp als die hier aufgeführten Typen an.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="OPM_BUS_TYPE_PCI"></span><span id="opm_bus_type_pci"></span><dl> <dt>**OPM \_ BUS \_ TYPE \_ PCI**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                                                            | PCI-Bus:<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_BUS_TYPE_PCIX"></span><span id="opm_bus_type_pcix"></span><dl> <dt>**OPM \_ \_ \_ PCIX-0X00000002**</dt> <dt></dt> </dl>                                                                                                                                                                         | PCI-X-Bus.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_BUS_TYPE_PCIEXPRESS"></span><span id="opm_bus_type_pciexpress"></span><dl> <dt>**OPM \_ BUSTYP \_ \_ PCIEXPRESS-0x00000003**</dt> <dt></dt> </dl>                                                                                                                                                       | PCI Express Bus:<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="OPM_BUS_TYPE_AGP"></span><span id="opm_bus_type_agp"></span><dl> <dt>**OPM \_ BUS \_ TYPE \_ AGP**</dt> <dt>0x00000004</dt> </dl>                                                                                                                                                                            | AGP-Bus (Accelerated Graphics Port).<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="opm_bus_implementation_modifier_inside_of_chipset"></span><dl> <dt>**OPM \_ \_ \_ BUSIMPLEMENTIERUNGSMODIFIZIERER \_ \_ INNERHALB \_ 0X00010000**</dt> <dt></dt> </dl>                                                                      | Die Implementierung für den Grafikadapter befindet sich in der North-Bridge eines Hauptplatinen-Chipsatzes. Dieses Flag impliziert, dass Daten nie über einen Erweiterungsbus (z. B. PCI oder AGP) übertragen werden, wenn sie vom Hauptspeicher an den Grafikadapter übertragen werden. <br/>                                                                                                                                     |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_chip"></span><dl> <dt>**OPM \_ \_ \_ \_ BUSIMPLEMENTIERUNGSMODIFIZIERERSPUREN \_ AUF \_ \_ \_ BOARD-ZU-CHIP-0X00020000 \_**</dt> <dt></dt> </dl>                            | Die Grafikkarte ist über Spuren auf der Hauptplatine mit der Nord-Brücke eines Hauptplatinen-Chipsatzes verbunden, und alle Chips (integrierte Schaltungen) des Grafikadapters werden an die Hauptplatine gelötet. <br/>                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_socket"></span><dl> <dt>**OPM \_ \_ \_ BUSIMPLEMENTIERUNGSMODIFIZIERER \_ \_ VERFOLGT AUF \_ \_ BOARD-TO-SOCKET-0X00030000 \_ \_**</dt> <dt></dt> </dl>                      | Die Grafikkarte ist über Spuren auf der Hauptplatine mit der North-Bridge eines Hauptplatinen-Chipsatzes verbunden, und alle Chips des Grafikadapters sind über Sockets mit der Hauptplatine verbunden.<br/>                                                                                                                                                                               |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="opm_bus_implementation_modifier_daughter_board_connector"></span><dl> <dt>**OPM \_ \_ \_ \_ BUSIMPLEMENTIERUNGSMODIFIZIERER BOARD \_ CONNECTOR \_ 0X00040000**</dt> <dt></dt> </dl>                                                 | Der Grafikadapter ist über einen Konnektor mit der Hauptplatine verbunden.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="opm_bus_implementation_modifier_daughter_board_connector_inside_of_nuae"></span><dl> <dt>**OPM \_ \_ \_ \_ BUSIMPLEMENTIERUNGSMODIFIZIERER BOARD CONNECTOR \_ IN \_ \_ \_ \_ NUAE**</dt> <dt>0X00050000</dt> </dl> | Der Grafikadapter ist über einen 3d-Anschluss mit der Hauptplatine verbunden, und der Grafikadapter befindet sich in einem Gehäuse, auf das der Benutzer nicht zugegriffen werden kann.<br/>                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_NON_STANDARD"></span><span id="opm_bus_implementation_modifier_non_standard"></span><dl> <dt>**OPM \_ DER \_ \_ BUSIMPLEMENTIERUNGSMODIFIZIERER \_ ENTSPRICHT \_ 0X80000000**</dt> <dt></dt> </dl>                                                                                      | Nicht standardmäßiger Modifizierer. (Optional.)<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="OPM_COPP_COMPATIBLE_BUS_TYPE_INTEGRATED"></span><span id="opm_copp_compatible_bus_type_integrated"></span><dl> <dt>**OPM \_ \_COPP-KOMPATIBLER \_ \_ BUSTYP \_ 0X80000000**</dt> <dt></dt> </dl>                                                                                                     | Integrierter Bus. Dieses Flag wird nur im COPP-Emulationsmodus verwendet. Sie gibt an, dass der Befehl und die Statussignale zwischen der Grafikkarte und anderen Subsystemen auf dem Computer nicht auf einem Erweiterungsbus verfügbar sind, der über eine öffentliche Spezifikation und einen Standardconnectortyp verfügt, es sei denn, es handelt sich um einen Speicherbus. Dieses Flag kann mit einem **OPM \_ BUS TYPE \_ \_ Xxx-Flag kombiniert** werden.<br/> |



## <a name="remarks"></a>Hinweise

Bis zu drei Flags können mit einem bitweisem OR festgelegt **werden.** Flags im Bereich von 0x00 bis 0x04 (**OPM \_ BUS TYPE \_ \_ Xxx**) geben den grundlegenden Bustyp an. Flags im Bereich von 0x10000 bis 0x50000 (**OPM \_ BUS IMPLEMENTATION \_ \_ MODIFIER \_ Xxx**) ändern die grundlegende Beschreibung. Der Treiber legt ein Bustypflag fest und kann optional ein Modifiziererflag einrichten. Darüber hinaus kann der Treiber optional das **FLAG OPM \_ BUS IMPLEMENTATION \_ \_ MODIFIER NON \_ \_ STANDARD** festlegen.

Im COPP-Emulationsmodus verwendet der Treiber nicht die Modifiziererflags, aber er kann das **FLAG OPM \_ COPP \_ COMPATIBLE BUS \_ \_ TYPE \_ INTEGRATED** festlegen.

Die Flags OPM BUG TYPE Xxxx und \_ OPM COPP COMPATIBLE BUS TYPE INTEGRATED entsprechen Werten aus der COPP BusType-Enumeration, die \_ im Certified Output Protection Protocol \_ (COPP) verwendet wird. **\_ \_ \_ \_ \_** [**\_**](/windows/win32/api/dxva9typ/ne-dxva9typ-copp_bustype)

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows Nur \[ Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Enumerationen](opm-enumerations.md)
</dt> </dl>

 

 
