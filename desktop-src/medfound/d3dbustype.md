---
description: Gibt den Typ des E/A-Bus an, der vom Grafikadapter verwendet wird.
ms.assetid: 11bb7e0e-8d49-45f2-89aa-7583dd925edf
title: D3DBUSTYPE-Enumeration (D3d9types.h)
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
ms.openlocfilehash: cece215946406bedcca2cbfdd2b64bfdb5df00208b2d84cf2aa90fdb89b516bc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119828380"
---
# <a name="d3dbustype-enumeration"></a>D3DBUSTYPE-Enumeration

Gibt den Typ des E/A-Bus an, der vom Grafikadapter verwendet wird.

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

<span id="D3DBUSTYPE_OTHER"></span><span id="d3dbustype_other"></span>**D3DBUSTYPE \_ OTHER**
</dt> <dd>

Gibt einen anderen Bustyp als die hier aufgeführten Typen an.

</dd> <dt>

<span id="D3DBUSTYPE_PCI"></span><span id="d3dbustype_pci"></span>**D3DBUSTYPE \_ PCI**
</dt> <dd>

PCI-Bus.

</dd> <dt>

<span id="D3DBUSTYPE_PCIX"></span><span id="d3dbustype_pcix"></span>**D3DBUSTYPE \_ PCIX**
</dt> <dd>

PCI-X-Bus.

</dd> <dt>

<span id="D3DBUSTYPE_PCIEXPRESS"></span><span id="d3dbustype_pciexpress"></span>**D3DBUSTYPE \_ PCIEXPRESS**
</dt> <dd>

PCI Express Bus.

</dd> <dt>

<span id="D3DBUSTYPE_AGP"></span><span id="d3dbustype_agp"></span>**D3DBUSTYPE \_ AGP**
</dt> <dd>

Accelerated Graphics Port (AGP)-Bus.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_INSIDE_OF_CHIPSET"></span><span id="d3dbusimpl_modifier_inside_of_chipset"></span>**\_D3DBUSIMPL-MODIFIZIERER \_ INNERHALB \_ VON \_ CHIPS**
</dt> <dd>

Die Implementierung für den Grafikadapter befindet sich in der Nord-Brücke eines Hauptplatinen-Gerüsts. Dieses Flag impliziert, dass Daten nie über einen Erweiterungsbus (z. B. PCI oder AGP) übertragen werden, wenn sie aus dem Hauptspeicher an den Grafikadapter übertragen werden.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_CHIP"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_chip"></span>**\_D3DBUSIMPL-MODIFIZIERER \_ VERFOLGT AUF \_ DER \_ \_ PLATINE NACH \_ \_ CHIP**
</dt> <dd>

Gibt an, dass der Grafikkarte über Spuren auf der Hauptplatine mit der Nord-Bridge eines Hauptplatinen-Adapters verbunden ist und alle Chips des Grafikadapters an die Hauptplatine gelöt werden. Dieses Flag impliziert, dass Daten nie über einen Erweiterungsbus (z. B. PCI oder AGP) übertragen werden, wenn sie aus dem Hauptspeicher an den Grafikadapter übertragen werden.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_TRACKS_ON_MOTHER_BOARD_TO_SOCKET"></span><span id="d3dbusimpl_modifier_tracks_on_mother_board_to_socket"></span>**\_D3DBUSIMPL-MODIFIZIERER \_ VERFOLGT DIE SPUREN AUF DEM BOARDS AN \_ \_ \_ \_ \_ SOCKET**
</dt> <dd>

Der Grafikkarte ist über Spuren auf der Hauptplatine mit der Nord-Bridge eines Hauptplatinen-Adapters verbunden, und alle Chips des Grafikadapters werden über Sockets mit der Hauptplatine verbunden.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR"></span><span id="d3dbusimpl_modifier_daughter_board_connector"></span>**\_D3DBUSIMPL-MODIFIZIERER- \_ UND \_ -PLATINENCONNECTOR \_**
</dt> <dd>

Der Grafikadapter ist über einen Platinenconnector mit der Hauptplatine verbunden.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_DAUGHTER_BOARD_CONNECTOR_INSIDE_OF_NUAE"></span><span id="d3dbusimpl_modifier_daughter_board_connector_inside_of_nuae"></span>**\_D3DBUSIMPL-MODIFIZIERER- \_ UND \_ VERBINDEBOARDCONNECTOR \_ IN \_ \_ \_ NUAE**
</dt> <dd>

Der Grafikadapter ist über einen Platinenconnector mit der Hauptplatine verbunden, und der Grafikadapter befindet sich in einem Gehäuse, auf das der Benutzer nicht zugreifen kann.

</dd> <dt>

<span id="D3DBUSIMPL_MODIFIER_NON_STANDARD"></span><span id="d3dbusimpl_modifier_non_standard"></span>**\_D3DBUSIMPL-MODIFIZIERER \_ UNGLEICH \_ STANDARD**
</dt> <dd>

Eines der \_ \_ Xxx-Flags des MODIFIZIERERMODIFIZIERER D3DBUSIMPL \_ ist festgelegt.

</dd> </dl>

## <a name="remarks"></a>Hinweise

Es können bis zu drei Flags festgelegt werden. Flags im Bereich 0x00 bis 0x04 (**D3DBUSTYPE \_ Xxx**) stellen den grundlegenden Bustyp bereit. Flags im Bereich 0x10000 bis 0x50000 (**D3DBUSIMPL \_ MODIFIER \_ Xxx**) ändern die grundlegende Beschreibung. Der Treiber legt ein Bustypflag fest und kann null oder ein Modifiziererflag festlegen. Wenn der Treiber ein Modifiziererflag festlegt, legt er auch das **D3DBUSIMPL \_ MODIFIER \_ NON \_ STANDARD-Flag** fest. Flags werden mit einem bitweisen **OR** kombiniert.

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | nur Windows 7 \[ Desktop-Apps\]<br/>                                                              |
| Unterstützte Mindestversion (Server)<br/> | Windows Nur Server 2008 \[ R2-Desktop-Apps\]<br/>                                                 |
| Header<br/>                   | <dl> <dt>D3d9types.h (einschließlich D3d9.h)</dt> </dl> |



## <a name="see-also"></a>Weitere Informationen

<dl> <dt>

[Direct3D-Videoenumerationen](direct3d-video-enumerations.md)
</dt> </dl>

 

 




