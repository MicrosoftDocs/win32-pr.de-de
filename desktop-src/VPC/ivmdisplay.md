---
title: IVMDisplay-Schnittstelle (VPCCOMInterfaces.h)
description: Steuert die Anzeigeeinstellungen eines virtuellen Computers. Die IVMDisplay-Schnittstelle für einen virtuellen Computer kann mithilfe der IVMVirtualMachine Display-Eigenschaft abgerufen werden.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- IVMDisplay-Schnittstelle Virtueller PC
- IVMDisplay-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMDisplay
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6239747477cdddf0ecbcf3acac90e33e61c0f5f4c9dd327b80eb6a33cb113c32
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119654140"
---
# <a name="ivmdisplay-interface"></a>IVMDisplay-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Steuert die Anzeigeeinstellungen eines virtuellen Computers. Die **IVMDisplay-Schnittstelle** für einen virtuellen Computer kann mithilfe der [**IVMVirtualMachine::D isplay-Eigenschaft abgerufen**](ivmvirtualmachine-display.md) werden.

## <a name="members"></a>Member

Die **IVMDisplay-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMDisplay** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMDisplay-Schnittstelle** verfügt über diese Methoden.



| Methode                                                       | Beschreibung                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) | Ruft ein Array von Pixeln ab, die ein Miniaturbild des Bildschirms des virtuellen Computers darstellen.<br/> |
| [**SetDimensions**](ivmdisplay-setdimensions.md)            | Legt die Höhe und Breite der Anzeige des virtuellen Computers in Pixel fest.<br/>                       |



 

### <a name="properties"></a>Eigenschaften

Die **IVMDisplay-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                             | Zugriffstyp          | Beschreibung                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**CanResize**](ivmdisplay-canresize.md)<br/> | Schreibgeschützt<br/> | Gibt an, ob der Gast Auflösungsänderungen zulässt.<br/>                             |
| [**Height**](ivmdisplay-height.md)<br/>       | Schreibgeschützt<br/> | Die Höhe der Anzeige des virtuellen Computers in Pixel.<br/>                            |
| [**Miniaturansicht**](ivmdisplay-thumbnail.md)<br/> | Schreibgeschützt<br/> | Ein Array von Pixeln, das ein Miniaturbild des Bildschirms des virtuellen Computers darstellt.<br/> |
| [**VideoMode**](ivmdisplay-videomode.md)<br/> | Schreibgeschützt<br/> | Der aktuelle Videomodus (Text, VGA, SVGA und so weiter).<br/>                               |
| [**Width**](ivmdisplay-width.md)<br/>         | Schreibgeschützt<br/> | Die Breite der Anzeige des virtuellen Computers in Pixel.<br/>                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMDisplay ist als 960895e9-f743-4498-96aa-261f867e7fc5 definiert.<br/>                 |



 

