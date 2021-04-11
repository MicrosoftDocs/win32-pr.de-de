---
description: Dieses Attribut fügt dem PUSHBUTTON-Steuerelement das Symbol für die Rechte Erweiterung (User Account Control, UAC) (Schild Symbol) hinzu.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: Elevationshield-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c580beefd1d2c0a80b0ee63b7a44e58a2a2fae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104131789"
---
# <a name="elevationshield-attribute"></a>Elevationshield-Attribut

Dieses Attribut fügt dem [PUSHBUTTON-Steuer](pushbutton-control.md)Element das Symbol für die Rechte Erweiterung ( [*User Account Control*](u-gly.md) , UAC) (Schild Symbol) hinzu.

Wenn dieses Bit festgelegt ist und die Installation noch nicht mit [*erhöhten*](e-gly.md) Rechten ausgeführt wird, wird das PUSHBUTTON-Steuerelement mithilfe des Erweiterungs Symbols für die [*Benutzerkontensteuerung (User Account Control*](u-gly.md) , UAC) erstellt.

Wenn dieses Bit festgelegt ist und die Installation bereits mit [*erhöhten*](e-gly.md) Rechten ausgeführt wird, wird das PUSHBUTTON-Steuerelement mithilfe der anderen Symbol Attribute erstellt.

Wenn dieses Bit nicht festgelegt ist, wird das PUSHBUTTON-Steuerelement mithilfe der anderen Symbol Attribute erstellt.

## <a name="valid-controls"></a>Gültige Steuerelemente

[PUSHBUTTON](pushbutton-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                                  |
|---------|-------------|-------------------------------------------|
| 8388608 | 0x00800000  | **msidbcontrolattributeselevationshield** |



 

 

 



