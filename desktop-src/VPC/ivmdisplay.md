---
title: Ivmdisplay-Schnittstelle (vpccominterfaces. h)
description: Steuert die Anzeigeeinstellungen eines virtuellen Computers. Die ivmdisplay-Schnittstelle für eine virtuelle Maschine kann mithilfe der Anzeige Eigenschaft ivmvirtualmachine abgerufen werden.
ms.assetid: b2eafd86-459c-4807-aa77-8b9125bce53e
keywords:
- Ivmdisplay Interface Virtual PC
- Virtueller Computer für ivmdisplay Interface, beschrieben
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
ms.openlocfilehash: 2c0f410e49682d2fa9f5f8511d96e3b9ce9a1094
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103956847"
---
# <a name="ivmdisplay-interface"></a>Ivmdisplay-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Steuert die Anzeigeeinstellungen eines virtuellen Computers. Die **ivmdisplay** -Schnittstelle für eine virtuelle Maschine kann mithilfe der [**ivmvirtualmachine::D isplay**](ivmvirtualmachine-display.md) -Eigenschaft abgerufen werden.

## <a name="members"></a>Member

Die **ivmdisplay** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmdisplay** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmdisplay** -Schnittstelle verfügt über diese Methoden.



| Methode                                                       | BESCHREIBUNG                                                                                             |
|:-------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------|
| [**\_GenerateThumbnail**](ivmdisplay--generatethumbnail.md) | Ruft ein Array von Pixeln ab, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt.<br/> |
| [**Setdimensions**](ivmdisplay-setdimensions.md)            | Legt die Höhe und Breite der Anzeige des virtuellen Computers in Pixel fest.<br/>                       |



 

### <a name="properties"></a>Eigenschaften

Die **ivmdisplay** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                             | Zugriffstyp          | BESCHREIBUNG                                                                                   |
|:-----------------------------------------------------|:---------------------|:----------------------------------------------------------------------------------------------|
| [**CanResize**](ivmdisplay-canresize.md)<br/> | Schreibgeschützt<br/> | Gibt an, ob der Gast Auflösungs Änderungen zulässt.<br/>                             |
| [**Höhe**](ivmdisplay-height.md)<br/>       | Schreibgeschützt<br/> | Die Höhe der Anzeige des virtuellen Computers in Pixel.<br/>                            |
| [**Miniaturansicht**](ivmdisplay-thumbnail.md)<br/> | Schreibgeschützt<br/> | Ein Array von Pixeln, das ein Miniaturbild des Bildschirms der virtuellen Maschine darstellt.<br/> |
| [**Videomode**](ivmdisplay-videomode.md)<br/> | Schreibgeschützt<br/> | Der aktuelle Videomodus (Text, VGA, SVGA usw.).<br/>                               |
| [**Breite**](ivmdisplay-width.md)<br/>         | Schreibgeschützt<br/> | Die Breite der Anzeige des virtuellen Computers in Pixel.<br/>                             |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmdisplay ist als 960895e9-f 743-4498-96aa-261f 867e7fc5 definiert.<br/>                 |



 

