---
description: Die in der folgenden Tabelle aufgeführten Flags geben den Typ des E/A-Bus an, der vom Grafikadapter verwendet wird.
ms.assetid: 6c8ec020-5f12-453b-bbeb-3baabb1ca213
title: OPM Bus-Typflags (Opmapi.h)
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
| <span id="OPM_BUS_TYPE_PCI"></span><span id="opm_bus_type_pci"></span><dl> <dt>**OPM \_ \_BUS TYPE PCI \_ 0x00000001**</dt> <dt></dt> </dl>                                                                                                                                                                            | PCI-Bus.<br/>                                                                                                                                                                                                                                                                                                                                                                        |
| <span id="OPM_BUS_TYPE_PCIX"></span><span id="opm_bus_type_pcix"></span><dl> <dt>**OPM \_ \_BUS TYPE \_ PCIX**</dt> <dt>0x00000002</dt> </dl>                                                                                                                                                                         | PCI-X-Bus.<br/>                                                                                                                                                                                                                                                                                                                                                                      |
| <span id="OPM_BUS_TYPE_PCIEXPRESS"></span><span id="opm_bus_type_pciexpress"></span><dl> <dt>**OPM \_ BUS \_ TYPE \_ PCIEXPRESS**</dt> <dt>0x00000003</dt> </dl>                                                                                                                                                       | PCI Express Bus.<br/>                                                                                                                                                                                                                                                                                                                                                                |
| <span id="OPM_BUS_TYPE_AGP"></span><span id="opm_bus_type_agp"></span><dl> <dt>**OPM \_ BUS \_ TYPE \_ AGP**</dt> <dt>0x00000004</dt> </dl>                                                                                                                                                                            | Accelerated Graphics Port (AGP)-Bus.<br/>                                                                                                                                                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="opm_bus_implementation_modifier_inside_of_chipset"></span><dl> <dt>**OPM \_ \_ \_ BUSIMPLEMENTIERER \_ INNERHALB VON \_ \_ 0X00010000**</dt> <dt></dt> </dl>                                                                      | Die Implementierung für den Grafikadapter befindet sich in der Nord-Brücke eines Hauptplatinen-Gerüsts. Dieses Flag impliziert, dass Daten nie über einen Erweiterungsbus (z. B. PCI oder AGP) übertragen werden, wenn sie aus dem Hauptspeicher an den Grafikadapter übertragen werden. <br/>                                                                                                                                     |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_chip"></span><dl> <dt>**OPM \_ DER MODIFIZIERER FÜR DIE \_ \_ BUSIMPLEMENTIERUNGEN \_ VERFOLGT AUF DEM BOARD \_ \_ \_ \_ 0X00020000 \_**</dt> <dt></dt> </dl>                            | Der Grafikadapter ist über Spuren auf der Hauptplatine mit der Nord-Bridge eines Hauptplatinen-Adapters verbunden, und alle Chips des Grafikadapters (integrierte Leitungen) werden an die Hauptplatine gelöt. <br/>                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="opm_bus_implementation_modifier_tracks_on_mother_board_to_socket"></span><dl> <dt>**OPM \_ DER MODIFIZIERER FÜR DIE \_ \_ BUSIMPLEMENTIERUNGEN \_ VERFOLGT DAS BOARD AN \_ \_ \_ \_ \_ SOCKETS**</dt> <dt>0X00030000</dt> </dl>                      | Der Grafikkarte ist über Spuren auf der Hauptplatine mit der Nord-Bridge eines Hauptplatinen-Adapters verbunden, und alle Chips des Grafikadapters werden über Sockets mit der Hauptplatine verbunden.<br/>                                                                                                                                                                               |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="opm_bus_implementation_modifier_daughter_board_connector"></span><dl> <dt>**OPM \_ \_ \_ BUS-IMPLEMENTIERUNGSMODIFIZIERER \_ – \_ \_ 0X00040000**</dt> <dt></dt> </dl>                                                 | Der Grafikadapter ist über einen Platinenconnector mit der Hauptplatine verbunden.<br/>                                                                                                                                                                                                                                                                                         |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="opm_bus_implementation_modifier_daughter_board_connector_inside_of_nuae"></span><dl> <dt>**OPM \_ \_ \_ BUS-IMPLEMENTIERUNGSMODIFIZIERER \_ - CONNECTORS \_ IM \_ \_ \_ \_ NUAE-0x00050000**</dt> <dt></dt> </dl> | Der Grafikadapter ist über einen Totenboardconnector mit der Hauptplatine verbunden, und der Grafikkarte befindet sich in einem Gehäuse, auf das der Benutzer nicht zugreifen kann.<br/>                                                                                                                                                                                                            |
| <span id="OPM_BUS_IMPLEMENTATION_MODIFIER_NON_STANDARD"></span><span id="opm_bus_implementation_modifier_non_standard"></span><dl> <dt>**OPM \_ \_ \_ BUS-IMPLEMENTIERUNGSMODIFIZIERER, \_ DER NICHT \_ DEM STANDARD**</dt> <dt>0X80000000</dt> </dl>                                                                                      | Nicht standardmäßiger Modifizierer. (Optional.)<br/>                                                                                                                                                                                                                                                                                                                                               |
| <span id="OPM_COPP_COMPATIBLE_BUS_TYPE_INTEGRATED"></span><span id="opm_copp_compatible_bus_type_integrated"></span><dl> <dt>**OPM \_ \_ \_ \_ \_ INTEGRIERTER COPP-KOMPATIBLER BUSTYP**</dt> <dt>0X80000000</dt> </dl>                                                                                                     | Integrierter Bus. Dieses Flag wird nur im COPP-Emulationsmodus verwendet. Sie gibt an, dass die Befehls- und Statussignale zwischen dem Grafikadapter und anderen Subsystemen auf dem Computer nicht in einem Erweiterungsbus verfügbar sind, der über eine öffentliche Spezifikation und einen Standardconnectortyp verfügt, es sei denn, es handelt sich um einen Speicherbus. Dieses Flag kann mit einem **OPM \_ BUS TYPE \_ \_ Xxx-Flag** kombiniert werden.<br/> |



## <a name="remarks"></a>Hinweise

Bis zu drei Flags können mit einem bitweisen **OR** festgelegt werden. Flags im Bereich 0x00 bis 0x04 (**OPM \_ BUS \_ TYPE \_ Xxx**) geben den grundlegenden Bustyp an. Flags im Bereich 0x10000 bis 0x50000 (**OPM \_ BUS \_ IMPLEMENTATION \_ MODIFIER \_ Xxx**) ändern die grundlegende Beschreibung. Der Treiber legt ein Bustypflag fest und kann optional ein Modifiziererflag einrichten. Darüber hinaus kann der Treiber optional das **OPM \_ BUS IMPLEMENTATION \_ \_ MODIFIER NON \_ \_ STANDARD-Flag** festlegen.

Im COPP-Emulationsmodus verwendet der Treiber nicht die Modifiziererflags, aber möglicherweise wird das **OPM \_ COPP \_ COMPATIBLE BUS \_ TYPE \_ \_ INTEGRATED-Flag** festgelegt.

Die OPM \_ BUG \_ TYPE \_ Xxxx-Flags und das **OPM \_ COPP COMPATIBLE BUS TYPE \_ \_ \_ \_ INTEGRATED-Flag** entsprechen Den Werten der [**COPP \_ BusType-Enumeration,**](/windows/win32/api/dxva9typ/ne-dxva9typ-copp_bustype) die im Certified Output Protection Protocol (COPP) verwendet wird.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows \[Nur Vista-Desktop-Apps\]<br/>                                      |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server \[ 2008-Desktop-Apps\]<br/>                                |
| Header<br/>                   | <dl> <dt>Opmapi.h</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[OPM-Enumerationen](opm-enumerations.md)
</dt> </dl>

 

 
