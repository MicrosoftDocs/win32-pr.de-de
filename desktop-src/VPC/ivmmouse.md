---
title: IVMMouse-Schnittstelle (VPCCOMInterfaces.h)
description: Steuert das Mausgerät innerhalb eines virtuellen Computers.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- IVMMouse-Schnittstelle Virtueller PC
- IVMMouse-Schnittstelle Virtueller PC , beschrieben
topic_type:
- apiref
api_name:
- IVMMouse
api_location:
- VPCCOMInterfaces.h
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 912365065b639f3c970390746c8e23ae1fc33648ecdf14278365290c503da26d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118998850"
---
# <a name="ivmmouse-interface"></a>IVMMouse-Schnittstelle

\[Windows Der virtuelle PC ist ab diesem Zeitraum nicht mehr Windows 8. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (V2).](/windows/desktop/HyperV_v2/windows-virtualization-portal)\]

Steuert das Mausgerät innerhalb eines virtuellen Computers (VM). Die **IVMMouse** für einen virtuellen Computer kann mithilfe der [**IVMVirtualMachine::Mouse-Eigenschaft abgerufen**](ivmvirtualmachine-mouse.md) werden. Koordinaten für das Mausgerät können entweder in absoluten Koordinaten oder in Deltakoordinaten dargestellt werden. Verwenden Sie [**die UsingAbsoluteCoordinates-Eigenschaft,**](ivmmouse-usingabsolutecoordinates.md) um zwischen den beiden Methoden der Koordinatendarstellung zu unterscheiden. Beachten Sie, dass das Abrufen der aktuellen Cursorposition und die Verwendung absoluter Koordinaten nur unterstützt werden, wenn auf dem Gastbetriebssystem die Integrationskomponenten installiert sind.

## <a name="members"></a>Member

Die **IVMMouse-Schnittstelle** erbt von der [**IDispatch-Schnittstelle.**](/windows/win32/api/oaidl/nn-oaidl-idispatch) **IVMMouse** verfügt auch über diese Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **IVMMouse-Schnittstelle** verfügt über diese Methoden.



| Methode                                  | BESCHREIBUNG                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [**Klicken**](ivmmouse-click.md)         | Simuliert einen Mausklick.<br/>                                         |
| [**GetButton**](ivmmouse-getbutton.md) | Ruft den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste ab.<br/> |
| [**SetButton**](ivmmouse-setbutton.md) | Legt den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste fest.<br/>      |



 

### <a name="properties"></a>Eigenschaften

Die **IVMMouse-Schnittstelle** verfügt über diese Eigenschaften.



| Eigenschaft                                                                         | Zugriffstyp           | BESCHREIBUNG                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [**HorizontalPosition**](ivmmouse-horizontalposition.md)<br/>             | Lesen/Schreiben<br/> | Die absolute x-Koordinate der Maus.<br/>                                         |
| [**ScrollWheelPosition**](ivmmouse-scrollwheelposition.md)<br/>           | Lesegeschützt<br/> | Die Z-Koordinate der Maus (nur relativ).<br/>                                  |
| [**UsingAbsoluteCoordinates**](ivmmouse-usingabsolutecoordinates.md)<br/> | Lesen/Schreiben<br/> | Gibt an, ob Mauskoordinaten absolute oder relative Koordinaten darstellen.<br/> |
| [**VerticalPosition**](ivmmouse-verticalposition.md)<br/>                 | Lesen/Schreiben<br/> | Die absolute y-Koordinate der Maus.<br/>                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Windows 7 \[ Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Product (Produkt)<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>VPCCOMInterfaces.h</dt> </dl> |
| IID<br/>                      | IID \_ IVMmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.<br/>                   |



 

