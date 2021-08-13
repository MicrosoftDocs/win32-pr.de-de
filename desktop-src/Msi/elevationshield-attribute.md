---
description: Dieses Attribut fügt dem PushButton-Steuerelement das Rechteerweiterungssymbol (Shield-Symbol) der Benutzerkontensteuerung (User Account Control, UAC) hinzu.
ms.assetid: ec52d660-eb83-4f27-b640-ea89156260aa
title: ElevationShield-Attribut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ce4c5da7133a7216386be56328c0e21e2e365129caa185e045984cb5e89b7d95
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118637490"
---
# <a name="elevationshield-attribute"></a>ElevationShield-Attribut

Dieses Attribut fügt dem [PushButton-Steuerelement](pushbutton-control.md)das Rechteerweiterungssymbol (Shield-Symbol) der Benutzerkontensteuerung (User [*Account Control,*](u-gly.md) UAC) hinzu.

Wenn dieses Bit festgelegt ist und die Installation noch nicht mit [*erhöhten*](e-gly.md) Rechten ausgeführt wird, wird das Pushbutton-Steuerelement [*mithilfe*](u-gly.md) des UAC-Rechteerweiterungssymbols (Shield-Symbol) erstellt.

Wenn dieses Bit festgelegt ist und die Installation bereits mit [*erhöhten*](e-gly.md) Rechten ausgeführt wird, wird das Pushbutton-Steuerelement mit den anderen Symbolattributen erstellt.

Wenn dieses Bit nicht festgelegt ist, wird das Pushbutton-Steuerelement mit den anderen Symbolattributen erstellt.

## <a name="valid-controls"></a>Gültige Steuerelemente

[Pushbutton](pushbutton-control.md)

## <a name="value"></a>Wert



| Decimal | Hexadezimal | Konstante                                  |
|---------|-------------|-------------------------------------------|
| 8388608 | 0x00800000  | **msidbControlAttributesElevationShield** |



 

 

 



