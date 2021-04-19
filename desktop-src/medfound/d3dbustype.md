---
description: Gibt den Typ des e/a-Busses an, der vom Grafikadapter verwendet wird.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: D3DBUSTYPE-Enumeration (D3d9types. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DBUSTYPE
api_type:
- HeaderDef
api_location:
- d3d9types.h
ms.openlocfilehash: 807e5a57c4abbf57c241643a3e7fea47606fbf75
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344232"
---
# <a name="d3dbustype-enumeration"></a>D3DBUSTYPE-Enumeration

Gibt den Typ des e/a-Busses an, der vom Grafikadapter verwendet wird.

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  D3DBUSTYPE_OTHER                                             = 0x00000000,
  D3DBUSTYPE_PCI                                               = 0x00000001,
  D3DBUSTYPE_PCIX                                              = 0x00000002,
  D3DBUSTYPE_PCIEXPRESS                                        = 0x00000003,
  D3DBUSTYPE_AGP                                               = 0x00000004,
  D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET                        = 0x00010000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP           = 0x00020000,
  D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET         = 0x00030000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR                 = 0x00040000,
  D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE  = 0x00050000,
  D3DBUSIMPL_MODIFIER_NON_STANDARD                             = 0x80000000
} D3DBUSTYPE;
```



## <a name="constants"></a>Konstanten

<dl> <dt>

<span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ andere**
</dt> <dd>

Gibt einen Typ von einem anderen Bus als den hier aufgeführten Typen an.

</dd> <dt>

<span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**
</dt> <dd>

PCI-Bus.

</dd> <dt>

<span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIx**
</dt> <dd>

PCI-X-Bus.

</dd> <dt>

<span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIExpress**
</dt> <dd>

PCI-Express-Bus.

</dd> <dt>

<span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE- \_ AGP**
</dt> <dd>

AGP-Bus (Accelerated Graphics Port).

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**D3DBUSIMPL- \_ Modifizierer \_ innerhalb \_ des \_ Chipsets**
</dt> <dd>

Die Implementierung für den Grafikadapter befindet sich in der North Bridge eines Motherboard-Chipsatzes. Dieses Flag impliziert, dass Daten nie über einen Erweiterungsbus (z. b. PCI oder AGP) übertragen werden, wenn Sie vom Hauptspeicher zum Grafikadapter übertragen werden.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**D3DBUSIMPL- \_ \_ modifizierertitel \_ auf der \_ Mutter \_ Platine \_ in den \_ Chip**
</dt> <dd>

Gibt an, dass der Grafikadapter mithilfe der Nachverfolgung auf der Hauptplatine mit der Nordbrücke eines Motherboard-Chipsatzes verbunden ist und alle Chips des Grafikadapters an die Platine soltet werden. Dieses Flag impliziert, dass Daten nie über einen Erweiterungsbus (z. b. PCI oder AGP) übertragen werden, wenn Sie vom Hauptspeicher zum Grafikadapter übertragen werden.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**D3DBUSIMPL- \_ \_ modifizierertitel \_ auf \_ \_ dem Mutter Board \_ in \_ Socket**
</dt> <dd>

Der Grafikadapter ist mit der Nordbrücke eines Motherboard-Chipsatzes durch Nachverfolgung auf der Hauptplatine verbunden, und alle Chips des Grafikadapters sind über Sockets mit dem Motherboard verbunden.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**D3DBUSIMPL- \_ modifiziererboard- \_ \_ \_ Connector**
</dt> <dd>

Der Grafikadapter ist über einen Daughterboard-Connector mit dem Motherboard verbunden.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**D3DBUSIMPL- \_ modifiziererboard- \_ \_ \_ Connector \_ innerhalb \_ von \_ nuae**
</dt> <dd>

Der Grafikadapter ist über einen Daughterboard-Connector mit dem Motherboard verbunden, und der Grafikadapter befindet sich in einem Gehäuse, das nicht vom Benutzer zugänglich ist.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**D3DBUSIMPL- \_ Modifizierer \_ nicht \_ Standard**
</dt> <dd>

Einer der D3DBUSIMPL-Modifizierer \_ \_ \_ xxx-Flags ist festgelegt.

</dd> </dl>

## <a name="remarks"></a>Bemerkungen

Es können bis zu drei Flags festgelegt werden. Flags im Bereich von 0x00 bis 0x04 (**D3DBUSTYPE \_ xxx**) stellen den grundlegenden Bustyp bereit. Flags im Bereich von 0x10000 bis 0x50000 (**D3DBUSIMPL \_ Modifier \_ xxx**) ändern die grundlegende Beschreibung. Der Treiber legt ein Flag für einen Bustyp fest und kann NULL oder ein modifiziererflag festlegen. Wenn der Treiber ein modifiziererflag festlegt, wird auch das Flag " **D3DBUSIMPL \_ Modifizierer \_ Non \_ Standard** " festgelegt. Flags werden mit einem bitweisen **or** kombiniert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Nur Windows Server 2008 R2 \[ -Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types. h (Include d3d9. h)</dt> </dl> |



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[Direct3D-videoenumerationen](direct3d-video-enumerations.md)
</dt> </dl>

 

 




