---
description: Stellt eine Auflistung dar, die Computerfunktionen bereitstellt und aus CIM \_ ManagedSystemElement-Objekten besteht.
ms.assetid: 410be43f-3368-4109-8b29-7b7cc2a3ec1b
title: CIM_ComputerSystem-Klasse (Hyper-V-Verwaltung)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ComputerSystem
- CIM_ComputerSystem.NameFormat
- CIM_ComputerSystem.Dedicated
- CIM_ComputerSystem.OtherDedicatedDescriptions
- CIM_ComputerSystem.ResetCapability
- CIM_ComputerSystem.PowerManagementCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 00a53d0c514113175c3c6ffb7ea40f8ef4e730d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369078"
---
# <a name="cim_computersystem-class-hyper-v-management"></a>CIM_ComputerSystem-Klasse (Hyper-V-Verwaltung)

Stellt eine Auflistung dar, die Computerfunktionen bereitstellt und aus [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md) -Objekten besteht.

## <a name="syntax"></a>Syntax

``` syntax
[Abstract, Version("2.24.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_ComputerSystem : CIM_System
{
  string NameFormat;
  uint16 Dedicated[];
  string OtherDedicatedDescriptions[];
  uint16 ResetCapability;
  uint16 PowerManagementCapabilities[];
};
```

## <a name="members"></a>Member

Die **CIM \_ Computersystem** -Klasse verfügt über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **CIM \_ Computersystem** -Klasse verfügt über diese Methoden.



| Methode                                                    | BESCHREIBUNG                                                                                                                                                                                                          |
|:----------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**SetPowerState**](cim-computersystem-setpowerstate.md) | Diese Methode ist als veraltet markiert. Verwenden Sie stattdessen die **requestpowerstatechange** -Methode in der **CIM- \_ powermanagementservice** -Klasse.<br/> **Veraltete Beschreibung:** Legt den Energiezustand des Computers fest.<br/> |



 

### <a name="properties"></a>Eigenschaften

Die **CIM \_ Computersystem** -Klasse verfügt über diese Eigenschaften.

<dl> <dt>

**Dediziert**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \|MIB-II.sysServices "," FC-GS. INCITS-T11 \| Platform \| PlatformType "), [**modelkorrespondenz**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Computersystem**.**Otherdedialisiedbeschreibungen**")
</dt> </dl>

Der Zweck und die Features des Computer Systems. Beispielsweise könnte ein für das Drucken dediziertes System "11" (Print) angeben. Ein allgemeines System mit Druckfunktionen kann auf "0" (nicht dediziert) und "11" (Drucken) festgelegt werden.

<dt>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>

<span id="Not_Dedicated"></span><span id="not_dedicated"></span><span id="NOT_DEDICATED"></span>**Nicht dediziert** (0)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unbekannt** (1)


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Sonstige** (2)


</dt> <dd></dd> <dt>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>

<span id="Storage"></span><span id="storage"></span><span id="STORAGE"></span>**Speicher** (3)


</dt> <dd></dd> <dt>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>

<span id="Router"></span><span id="router"></span><span id="ROUTER"></span>**Router** (4)


</dt> <dd></dd> <dt>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>

<span id="Switch"></span><span id="switch"></span><span id="SWITCH"></span>**Switch** (5)


</dt> <dd></dd> <dt>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>

<span id="Layer_3_Switch"></span><span id="layer_3_switch"></span><span id="LAYER_3_SWITCH"></span>**Layer 3-Schalter** (6)


</dt> <dd></dd> <dt>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>

<span id="Central_Office_Switch"></span><span id="central_office_switch"></span><span id="CENTRAL_OFFICE_SWITCH"></span>**Zentrale Niederlassung** (7)


</dt> <dd></dd> <dt>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>

<span id="Hub"></span><span id="hub"></span><span id="HUB"></span>**Hub** (8)


</dt> <dd></dd> <dt>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>

<span id="Access_Server"></span><span id="access_server"></span><span id="ACCESS_SERVER"></span>**Zugriffs Server** (9)


</dt> <dd></dd> <dt>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>

<span id="Firewall"></span><span id="firewall"></span><span id="FIREWALL"></span>**Firewall** (10)


</dt> <dd></dd> <dt>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>

<span id="Print"></span><span id="print"></span><span id="PRINT"></span>**Drucken** (11)


</dt> <dd></dd> <dt>

<span id="I_O"></span><span id="i_o"></span>

<span id="I_O"></span><span id="i_o"></span>E **/** a (12)


</dt> <dd></dd> <dt>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>

<span id="Web_Caching"></span><span id="web_caching"></span><span id="WEB_CACHING"></span>**Webcaching** (13)


</dt> <dd></dd> <dt>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>

<span id="Management"></span><span id="management"></span><span id="MANAGEMENT"></span>**Verwaltung** (14)


</dt> <dd>

Diese Instanz ist für das Hosting der System Verwaltungssoftware vorgesehen.

</dd> <dt>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>

<span id="Block_Server"></span><span id="block_server"></span><span id="BLOCK_SERVER"></span>**Block Server** (15)


</dt> <dd></dd> <dt>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>

<span id="File_Server"></span><span id="file_server"></span><span id="FILE_SERVER"></span>**Datei Server** (16)


</dt> <dd></dd> <dt>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>

<span id="Mobile_User_Device"></span><span id="mobile_user_device"></span><span id="MOBILE_USER_DEVICE"></span>**Mobiles Benutzergerät** (17)


</dt> <dd>

Ein Beispiel für ein dediziertes Benutzergerät ist ein Mobiltelefon oder ein Barcode Scanner in einem Geschäft, das über eine Radiofrequenz kommuniziert. Diese Systeme sind in der Funktionalität und Programmierbarkeit sehr eingeschränkt und werden nicht als "universell" eingestuft. Alternativ ist ein Beispiel für ein mobiles System, das "universell" (d. h. nicht dediziert) ist, ein Hand gehalteter Computer. Obwohl die Programmierbarkeit eingeschränkt ist, kann neue Software heruntergeladen und ihre Funktionalität vom Benutzer erweitert werden.

</dd> <dt>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>

<span id="Repeater"></span><span id="repeater"></span><span id="REPEATER"></span>**Repeater** (18)


</dt> <dd></dd> <dt>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>

<span id="Bridge_Extender"></span><span id="bridge_extender"></span><span id="BRIDGE_EXTENDER"></span>**Bridge/Extender** (19)


</dt> <dd></dd> <dt>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>

<span id="Gateway"></span><span id="gateway"></span><span id="GATEWAY"></span>**Gateway** (20)


</dt> <dd></dd> <dt>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>

<span id="Storage_Virtualizer"></span><span id="storage_virtualizer"></span><span id="STORAGE_VIRTUALIZER"></span>**Speichervirtualisierer** (21)


</dt> <dd></dd> <dt>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>

<span id="Media_Library"></span><span id="media_library"></span><span id="MEDIA_LIBRARY"></span>**Medienbibliothek** (22)


</dt> <dd></dd> <dt>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>

<span id="ExtenderNode"></span><span id="extendernode"></span><span id="EXTENDERNODE"></span>**Extendernode** (23)


</dt> <dd></dd> <dt>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>

<span id="NAS_Head"></span><span id="nas_head"></span><span id="NAS_HEAD"></span>**NAS-Head** (24)


</dt> <dd></dd> <dt>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>

<span id="Self-contained_NAS"></span><span id="self-contained_nas"></span><span id="SELF-CONTAINED_NAS"></span>**Eigenständiges NAS** (25)


</dt> <dd></dd> <dt>

<span id="UPS"></span><span id="ups"></span>

<span id="UPS"></span><span id="ups"></span>**UPS** (26)


</dt> <dd></dd> <dt>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>

<span id="IP_Phone"></span><span id="ip_phone"></span><span id="IP_PHONE"></span>**IP-Telefon** (27)


</dt> <dd></dd> <dt>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>

<span id="Management_Controller"></span><span id="management_controller"></span><span id="MANAGEMENT_CONTROLLER"></span>**Verwaltungs Controller** (28)


</dt> <dd>

Diese Instanz stellt spezielle Hardware dar, die für die Systemverwaltung vorgesehen ist (d. h. einen Baseboard-Verwaltungs Controller (BMC) oder einen Dienst Prozessor).

Der Verwaltungsbereich eines Verwaltungs Controllers ist in der Regel ein einzelnes verwaltetes System, in dem es enthalten ist.

</dd> <dt>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>

<span id="Chassis_Manager"></span><span id="chassis_manager"></span><span id="CHASSIS_MANAGER"></span>**Chassis-Manager** (29)


</dt> <dd>

Diese Instanz stellt ein System dar, das für die Verwaltung eines Blade Chassis und der darin enthaltenen Geräte vorgesehen ist. Dieser Wert wird verwendet, um einen Regal Controller darzustellen. Ein "Chassis-Manager" ist ein Aggregations Punkt für die Verwaltung und kann für die Verwaltung von Bestandteilen auf untergeordneten Verwaltungs Controllern beruhen.

</dd> <dt>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>

<span id="Host-based_RAID_controller"></span><span id="host-based_raid_controller"></span><span id="HOST-BASED_RAID_CONTROLLER"></span>**Host basierter RAID-Controller** (30)


</dt> <dd>

Diese Instanz stellt einen RAID-Speichercontroller dar, der in einem Host Computer enthalten ist.

</dd> <dt>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>

<span id="Storage_Device_Enclosure"></span><span id="storage_device_enclosure"></span><span id="STORAGE_DEVICE_ENCLOSURE"></span>**Speichergeräte Gehäuse** (31)


</dt> <dd>

Diese Instanz stellt ein Gehäuse dar, das Speichergeräte enthält.

</dd> <dt>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>

<span id="Desktop"></span><span id="desktop"></span><span id="DESKTOP"></span>**Desktop** (32)


</dt> <dd></dd> <dt>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>

<span id="Laptop"></span><span id="laptop"></span><span id="LAPTOP"></span>**Laptop** (33)


</dt> <dd></dd> <dt>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>

<span id="Virtual_Tape_Library"></span><span id="virtual_tape_library"></span><span id="VIRTUAL_TAPE_LIBRARY"></span>**Bibliothek für virtuelle Bänder** (34)


</dt> <dd>

Die Emulation einer Band Bibliothek durch ein virtuelles Bibliotheks System.

</dd> <dt>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>

<span id="Virtual_Library_System"></span><span id="virtual_library_system"></span><span id="VIRTUAL_LIBRARY_SYSTEM"></span>**Virtuelles Bibliotheks System** (35)


</dt> <dd>

Verwendung von Datenträger Speicher zum Emulieren von Bandbibliotheken

</dd> <dt>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>

<span id="Network_PC_Thin_Client"></span><span id="network_pc_thin_client"></span><span id="NETWORK_PC_THIN_CLIENT"></span>**Netzwerk-PC/Thin Client** (36)


</dt> <dd></dd> <dt>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>

<span id="FC_Switch"></span><span id="fc_switch"></span><span id="FC_SWITCH"></span>**FC-Schalter** (37)


</dt> <dd>

Dediziert zum Wechseln von Fibre Channel-Frames der Ebene 2.

</dd> <dt>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>

<span id="Ethernet_Switch"></span><span id="ethernet_switch"></span><span id="ETHERNET_SWITCH"></span>**Ethernet-Switch** (38)


</dt> <dd>

Dedizierter zum Wechseln von Layer 2-Ethernet-Frames

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF reserviert** (..)


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**Anbieter reserviert** (32568.65535)


</dt> <dd></dd> </dl>

</dd> <dt>

**NameFormat**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichenfolge**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NameFormat")
</dt> </dl>

Das Format des System namens des Computers.

<dt>



 ("Other")


</dt> <dd></dd> <dt>



 ("IP")


</dt> <dd></dd> <dt>



 ("Dial")


</dt> <dd></dd> <dt>



 ("HID")


</dt> <dd></dd> <dt>



 ("NWA")


</dt> <dd></dd> <dt>



 ("Hwa")


</dt> <dd></dd> <dt>



 ("X25")


</dt> <dd></dd> <dt>



 ("ISDN")


</dt> <dd></dd> <dt>



 ("IPX")


</dt> <dd></dd> <dt>



 ("DCC")


</dt> <dd></dd> <dt>



 ("ICD")


</dt> <dd></dd> <dt>



 ("E. 164")


</dt> <dd></dd> <dt>



 ("SNA")


</dt> <dd></dd> <dt>



 ("OID/OSI")


</dt> <dd></dd> <dt>



 ("WWN")


</dt> <dd></dd> <dt>



 ("Naa")


</dt> <dd></dd> </dl>

</dd> <dt>

**OtherDedicatedDescriptions**
</dt> <dd> <dl> <dt>

Datentyp: **Zeichen** folgen Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**arrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indiziert"), [**modelcorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ Computersystem**".**Dediziert**")
</dt> </dl>

Beschreibt, wie oder warum das System dediziert ist, wenn das **dedizierte** Array den Wert 2 (Sonstiges) enthält.

</dd> <dt>

**Powermanagementfunktionen**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16** Array
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**veraltet**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("CIM \_ powermanagementfunktionalitäten. Power-Funktionen"), [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF- \| System Energiesteuerung \| 001,2 ")
</dt> </dl>

Diese Eigenschaft ist veraltet. Verwenden Sie stattdessen die **powerchangefunktionalitäten** -Methode in der **CIM \_ powermanagementcapabilitiescim \_ powermanagementservice** -Klasse.

**Veraltete Beschreibung:** Die Energie Verwaltungsfunktionen des Systems.

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (0)


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

**Nicht unterstützt** (1)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (2)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (3)


</dt> <dd></dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

**Automatisch eingegebene Energiespar Modi** (4)


</dt> <dd></dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

**Einsetzbaren Energiezustand** (5)


</dt> <dd></dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

**Unterstützung für Power Cycling** (6)


</dt> <dd></dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

**Unterstützte Unterstützung** (7)


</dt> <dd></dd> </dl>

</dd> <dt>

**Resetcapability**
</dt> <dd> <dl> <dt>

Datentyp: **UInt16**
</dt> <dt>

Zugriffstyp: Schreibgeschützt
</dt> <dt>

Qualifizierer: [**mappingstrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF". DMTF \| System Hardware Security \| 001,4 ")
</dt> </dl>

Gibt an, ob das System den Hardware Zurücksetzungs Vorgang unterstützt.

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

**Sonstige** (1)


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

**Unbekannt** (2)


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

**Deaktiviert** (3)


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

**Aktiviert** (4)


</dt> <dd></dd> <dt>

<span id="Not_Implemented"></span><span id="not_implemented"></span><span id="NOT_IMPLEMENTED"></span>

**Nicht implementiert** (5)


</dt> <dd></dd> </dl>

</dd> </dl>

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 8<br/>                                                                                    |
| Unterstützte Mindestversion (Server)<br/> | Windows Server 2012<br/>                                                                          |
| Namespace<br/>                | \\Stammvirtualisierung \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>Windowsvirtualization. v2. MOF</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**CIM- \_ System**](cim-system.md)
</dt> </dl>

 

