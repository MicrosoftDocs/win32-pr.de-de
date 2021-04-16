---
description: Die in der folgenden Tabelle aufgeführten Flags geben den Typ des e/a-Busses an, der vom Grafikadapter verwendet wird.
ms.assetid: 6c8ec020-5f12-453b-bbeb-3baabb1ca213
title: OPM-bustyps (opmapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae3e6988d6bcd33015b0efc5b12561ef3373a9e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527893"
---
# <a name="opm-bus-type-flags"></a>OPM-bustyps

Die in der folgenden Tabelle aufgeführten Flags geben den Typ des e/a-Busses an, der vom Grafikadapter verwendet wird.



| Konstante/Wert                                                                                                                                                                                                                                                                                                                                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_BUS_TYPE_OTHER"></span><span id="opm_bus_type_other"></span><dl> <dt>**OPM \_ \_Bustyp \_ sonstige**</dt> <dt>0x00000000</dt> </dl>                                                                                                                                                                      | Gibt einen Typ von einem anderen Bus als den hier aufgeführten Typen an.<br/>                                                                                                                                                                                                                                                                                                                       |
| <span id="OPM_BUS_TYPE_PCI"></span><span id="opm_bus_type_pci"></span><dl> <dt>**OPM \_ \_Bustyp \_ PCI**</dt> <dt>0x00000001</dt> </dl>                                                                                                                                                                            | PCI-Bus.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_BUS_TYPE_PCIX"></span><span id="opm_bus_type_pcix"></span><dl> <dt>**OPM \_ \_Bustyp \_ PCIx**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                                                         | PCI-X-Bus.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_BUS_TYPE_PCIEXPRESS"></span><span id="opm_bus_type_pciexpress"></span><dl> <dt>**OPM \_ \_Bustyp \_ PCIExpress**</dt> <dt>0x00000003</dt> </dl>                                                                                                                                                       | PCI-Express-Bus.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="OPM_BUS_TYPE_AGP"></span><span id="opm_bus_type_agp"></span><dl> <dt>**OPM \_ \_Bustyp \_ AGP**</dt> <dt>0x00000004</dt> </dl>                                                                                                                                                                            | AGP-Bus (Accelerated Graphics Port).<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="opm_bus_implementation_modifier_inside_of_chipset"></span><dl> <dt>**OPM \_ \_ \_ Bumplementierungsmodifizierer \_ innerhalb \_ von \_ Chipsatz**</dt> <dt>0x00010000 bis</dt> </dl>                                                                      | Die Implementierung für den Grafikadapter befindet sich in der North Bridge eines Motherboard-Chipsatzes. Dieses Flag impliziert, dass Daten nie über einen Erweiterungsbus (z. b. PCI oder AGP) übertragen werden, wenn Sie vom Hauptspeicher zum Grafikadapter übertragen werden. <br/>                                                                                                                                     |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_chip"></span><dl> <dt>**OPM \_ Bumplementierungsmodifizierer \_ \_ \_ \_ im \_ Mutter \_ Board \_ zu \_ Chip**</dt> <dt>0x00020000</dt> </dl>                            | Der Grafikadapter ist mit der Nordbrücke eines Motherboard-Chipsatzes durch Nachverfolgung auf der Hauptplatine verbunden, und alle Chips des Grafikadapters (integrierte Verbindungen) werden an die Hauptplatine soltet. <br/>                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_socket"></span><dl> <dt>**OPM \_ Bumplementierungsmodifizierer \_ \_ \_ verfolgt \_ auf dem \_ Mutter \_ Board \_ in \_ Socket**</dt> <dt>0x00030000</dt> </dl>                      | Der Grafikadapter ist mit der Nordbrücke eines Motherboard-Chipsatzes durch Nachverfolgung auf der Hauptplatine verbunden, und alle Chips des Grafikadapters sind über Sockets mit dem Motherboard verbunden.<br/>                                                                                                                                                                               |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="opm_bus_implementation_modifier_daughter_board_connector"></span><dl> <dt>**OPM \_ Bumplementierungsmodifizierer \_ \_ \_ \_ \_**</dt> <dt>0x00040000</dt> </dl>                                                 | Der Grafikadapter ist über einen Daughterboard-Connector mit dem Motherboard verbunden.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="opm_bus_implementation_modifier_daughter_board_connector_inside_of_nuae"></span><dl> <dt>**OPM \_ Bumplementierungsmodifizierer \_ \_ \_ in den \_ \_ \_ \_ \_ nuae**</dt> <dt>0x00050000</dt> </dl> | Der Grafikadapter ist über einen Daughterboard-Connector mit dem Motherboard verbunden, und der Grafikadapter befindet sich in einem Gehäuse, das nicht vom Benutzer zugänglich ist.<br/>                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_NON_STANDARD"></span><span id="opm_bus_implementation_modifier_non_standard"></span><dl> <dt>**OPM \_ \_Busimplementierungs \_ Modifizierer \_ nicht \_ Standard**</dt> <dt>0x80000000</dt> </dl>                                                                                      | Nicht Standardmodifizierer. (Optional.)<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="OPM_COPP_COMPATIBLE_BUS_TYPE_INTEGRATED"></span><span id="opm_copp_compatible_bus_type_integrated"></span><dl> <dt>**OPM \_ Kopp- \_ kompatibler \_ \_ Bustyp \_ integriert**</dt> ( <dt>0x80000000</dt> ) </dl>                                                                                                     | Integrierter Bus. Dieses Flag wird nur im COPP-Emulations Modus verwendet. Es zeigt an, dass die Befehls-und Statussignale zwischen dem Grafikadapter und anderen Subsystemen auf dem Computer nicht in einem Erweiterungsbus verfügbar sind, der über eine öffentliche Spezifikation und einen Standardverbindungstyp verfügt, es sei denn, es handelt sich um einen Speicherbus Dieses Flag kann mit einem **OPM- \_ \_ Bustyp \_ xxx** -Flag kombiniert werden.<br/> |



## <a name="remarks"></a>Bemerkungen

Bis zu drei Flags können mit einem bitweisen **or** festgelegt werden. Flags im Bereich von 0x00 bis 0x04 (**OPM \_ Bus \_ Type \_ xxx**) geben den basisbustyp an. Flags im Bereich von 0x10000 bis 0x50000 (**OPM \_ - \_ busimplementierungs \_ Modifizierer \_ xxx**) ändern die grundlegende Beschreibung. Der Treiber legt ein Flag für einen Bustyp fest und kann optional auf ein modifiziererflag festgelegt werden. Außerdem kann der Treiber optional das Flag " **OPM- \_ \_ busimplementierungs \_ Modifizierer \_ nicht \_ Standard** " festlegen.

Im COPP-Emulations Modus verwendet der Treiber nicht die Modifiziererflags, er kann jedoch das **OPM \_ COPP \_ - \_ kompatible \_ sType \_** -Flag festlegen.

Die OPM \_ \_ -Fehlertyp \_ -xxxx-Flags und das **OPM- \_ Kopp- \_ kompatible \_ \_ \_** bustypflag entsprechen den Werten aus der [**COPP \_ BusType**](/windows/win32/api/dxva9typ/ne-dxva9typ-copp_bustype) -Enumeration, die im Certified Output Protection Protocol (COPP) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows Vista \[ -Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 \[ -Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi. h</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[OPM-Enumerationen](opm-enumerations.md)
</dt> </dl>

 

 
