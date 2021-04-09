---
title: Ivmmouse-Schnittstelle (vpccominterfaces. h)
description: Steuert das Mausgerät innerhalb einer VM.
ms.assetid: 13bbf980-aafd-4c63-b1cb-60f00b738d1f
keywords:
- Ivmmouse Interface Virtual PC
- Virtueller Computer für ivmmouse Interface, beschrieben
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
ms.openlocfilehash: 7041b8a28b924ffedc8ff23edd2b04afdaa78be2
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/12/2020
ms.locfileid: "103859182"
---
# <a name="ivmmouse-interface"></a>Ivmmouse-Schnittstelle

\[Windows Virtual PC ist nicht mehr für die Verwendung ab Windows 8 verfügbar. Verwenden Sie stattdessen den [Hyper-V-WMI-Anbieter (v2)](/windows/desktop/HyperV_v2/windows-virtualization-portal).\]

Steuert das Mausgerät innerhalb eines virtuellen Computers (VM). Das **ivmmouse** für eine virtuelle Maschine kann mithilfe der [**ivmvirtualmachine:: Mouse**](ivmvirtualmachine-mouse.md) -Eigenschaft abgerufen werden. Koordinaten für das Mausgerät können entweder in absoluten Koordinaten oder in Delta Koordinaten dargestellt werden. Verwenden Sie die [**usingabsolutekoordinaten**](ivmmouse-usingabsolutecoordinates.md) -Eigenschaft, um zwischen den beiden Methoden der Koordinaten Darstellung zu unterscheiden. Beachten Sie, dass das Abrufen der aktuellen Cursorposition und der Verwendung absoluter Koordinaten nur unterstützt wird, wenn auf dem Gast Betriebssystem die-Integrations Komponenten installiert sind.

## <a name="members"></a>Member

Die **ivmmouse** -Schnittstelle erbt von der [**IDispatch**](/windows/win32/api/oaidl/nn-oaidl-idispatch) -Schnittstelle. **Ivmmouse** verfügt auch über die folgenden Typen von Membern:

-   [Methoden](#methods)
-   [Eigenschaften](#properties)

### <a name="methods"></a>Methoden

Die **ivmmouse** -Schnittstelle verfügt über diese Methoden.



| Methode                                  | BESCHREIBUNG                                                                        |
|:----------------------------------------|:-----------------------------------------------------------------------------------|
| [**Sie**](ivmmouse-click.md)         | Simuliert das Klicken auf die Maustaste.<br/>                                         |
| [**Getbutton**](ivmmouse-getbutton.md) | Ruft den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste ab.<br/> |
| [**Setbutton**](ivmmouse-setbutton.md) | Legt den aktuellen Zustand (nach oben oder unten) der angegebenen Maustaste fest.<br/>      |



 

### <a name="properties"></a>Eigenschaften

Die **ivmmouse** -Schnittstelle verfügt über diese Eigenschaften.



| Eigenschaft                                                                         | Zugriffstyp           | BESCHREIBUNG                                                                                |
|:---------------------------------------------------------------------------------|:----------------------|:-------------------------------------------------------------------------------------------|
| [**HorizontalPosition**](ivmmouse-horizontalposition.md)<br/>             | Lesen/Schreiben<br/> | Die absolute x-Koordinate der Maus.<br/>                                         |
| [**Scrollwheelposition**](ivmmouse-scrollwheelposition.md)<br/>           | Lesegeschützt<br/> | Die z-Koordinate der Maus (nur relativ).<br/>                                  |
| [**Usingabsolutekoordinaten**](ivmmouse-usingabsolutecoordinates.md)<br/> | Lesen/Schreiben<br/> | Gibt an, ob Maus Koordinaten absolute oder relative Koordinaten darstellen.<br/> |
| [**VerticalPosition**](ivmmouse-verticalposition.md)<br/>                 | Lesen/Schreiben<br/> | Die absolute y-Koordinate der Maus.<br/>                                         |



 

## <a name="requirements"></a>Anforderungen



| Anforderung | Wert |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| Unterstützte Mindestversion (Client)<br/> | Nur Windows 7 \[ -Desktop-Apps\]<br/>                                                    |
| Unterstützte Mindestversion (Server)<br/> | Nicht unterstützt<br/>                                                                     |
| Ende des Supports (Client)<br/>    | Windows 7<br/>                                                                          |
| Produkt<br/>                  | Windows Virtual PC<br/>                                                                 |
| Header<br/>                   | <dl> <dt>Vpccominterfaces. h</dt> </dl> |
| IID<br/>                      | IID \_ ivmmouse ist als ac903f6d-6346-4f29-8875-5d511a13895e definiert.<br/>                   |



 

