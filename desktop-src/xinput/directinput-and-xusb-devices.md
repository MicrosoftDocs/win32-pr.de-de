---
title: DirectInput-und xusb-Geräte
description: Der Treiber für die Xbox Common Controller Class (xusb) unter Windows implementiert die kernelmodusschnittstelle für die xinput-dll.
ms.assetid: 8bf47b07-a1b6-7721-2136-3853e72c71ad
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5b2b6d2857502c0e0209d94fb6d933618c180fd2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316329"
---
# <a name="directinput-and-xusb-devices"></a>DirectInput-und xusb-Geräte

Der Treiber für die Xbox Common Controller Class (xusb) unter Windows implementiert die kernelmodusschnittstelle für die xinput-dll. Um eine gute Oberfläche für ältere Titel bereitzustellen, die die [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) -API mit dem gemeinsamen Controller Gerät verwenden, exportiert der Treiber auch eine Eingabegeräte (HID) Class-Schnittstelle, die von DirectInput abgerufen wird. Wir haben die Zuordnung von xusb zu HID basierend auf dem typischen Verhalten in einem Satz von Spiele Anwendungen für die ursprüngliche xinput-Version gewählt und die Zuordnung für neuere Untertypen aktualisiert. In diesem Thema wird die Zuordnung beschrieben.

## <a name="human-interface-device-hid"></a>Eingabegerät (Human Interface Device, HID)

HID Standard ist ein Standard aus dem von Microsoft ursprünglich von Microsoft vorgeschlagenen, von Microsoft vorgeschlagenen Universal Serial Bus (Universal Serial Bus) zum generalisieren von Protokollen für Eingabegeräte. Sie besteht aus einer Byte Code Beschreibungssprache und kann Gamepads, Mäuse, Joysticks, Drosselungs-und Rudder-Steuerelemente und Multiachsen-Controller Ausdrücken. Da dieser Standard so generalisiert ist, haben Sie möglicherweise Schwierigkeiten beim Schreiben von Software, die Eingaben von beliebigen Geräten verarbeitet. Daher haben wir für die Spiel zentrierte [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) -API eine bestimmte unter Zuordnung von Typen entwickelt, um Hardwarehersteller bei der Unterstützung durch ihre Treiber zu unterstützen.

- [USB-Geräteklassen Definition für HID v 1.11](https://www.usb.org/document-library/device-class-definition-hid-111)

> [!Important]
> Sie können auch über die [rawinput-API](../inputdev/about-raw-input.md) auf versteckte Eingabegeräte zugreifen und Eingabe Berichte über die Low-Level- [HID-API](/windows-hardware/drivers/hid/introduction-to-hid-concepts) verarbeiten, aber das Vibrationsfeedback funktioniert nicht wie bei [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)).

## <a name="mappings"></a>Zuordnungen

Der xusb-Treiber implementiert sowohl eine xusb-Klassen Schnittstelle als auch eine HID-Klassen Schnittstelle für Geräte, um die Verwendung von XInput und [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) zu unterstützen. Diese Zuordnung basiert auf den Informationen zum xusb-Untertyp. Der Treiber implementiert vier verschiedene Gruppen von Zuordnungen.

| Xusb-Untertyp                                      | Zuordnung                     |
|---------------------------------------------------|-----------------------------|
| Xinput \_ devsubtype \_ Gamepad (Untertyp 1)           | Gamepad                     |
| Xinput \_ devsubtype \_ Wheel (Untertyp 2)             | Wheel                       |
| Xinput \_ devsubtype \_ - \_ browserstick (Untertyp 3)     | Pad-Pad/-polarpad     |
| Xinput \_ devsubtype \_ - \_ flugstick (Untertyp 4)     | Flugstick                |
| Xinput \_ devsubtype \_ - \_ Tanzpad (Untertyp 5)        | Standard für jeden neuen Untertyp |
| Xinput \_ devsubtype- \_ Gitarre (Untertyp 6)            | La                      |
| Xinput \_ devsubtype- \_ Gitarren \_ Alternative (Untertyp 7) |                             |
| Xinput \_ devsubtype \_ - \_ Drumkit (Untertyp 8)         |                             |
| Xinput \_ devsubtype- \_ Gitarren- \_ Bass (Untertyp 11)     |                             |
| Xinput \_ devsubtype \_ - \_ browserpad (Untertyp 19)      |                             |

> [!Note]  
> Die folgenden HID-Zuordnungen sind statisch. Dies bedeutet, dass selbst dann, wenn der Bericht "Gerätefunktionen" anzeigt, dass eine bestimmte Schaltfläche oder Achse nicht unterstützt wird, die Zuordnung jedoch weiterhin enthalten ist, aber immer einen Off-Status oder-Mittelwert meldet.

## <a name="gamepad"></a>Gamepad

Dies ist die Standard Zuordnung, die für das standardmäßige Xbox Common Controller Gamepad entwickelt wurde und als *Gamepad* -verlastungstyp verfügbar gemacht wird.

| Control                      | Name der HID-Verwendung | Seite "Verwendung" | Nutzungs-ID   |
|------------------------------|----------------|------------|------------|
| Linker Stick                   | X, Y           | 0x01       | 0x30, 0x31 |
| Rechter Stick                  | RX, Ry         | 0x01       | 0x33, 0x34 |
| Linker-und rechter-Auslösers | Z\*            | 0x01       | 0x32       |
| D: Auffüllung nach oben, unten, Links, rechts  | Hat-Schalter     | 0x01       | 0x39       |
| A                            | Schaltfläche 1       | 0x09       | 0x01       |
| B                            | Schaltfläche 2       | 0x09       | 0x02       |
| X                            | Schaltfläche 3       | 0x09       | 0x03       |
| J                            | Schaltfläche 4       | 0x09       | 0x04       |
| LB (linker-Stoßfänger)             | Schaltfläche 5       | 0x09       | 0x05       |
| RB (Rechte Stoßstange)            | Schaltfläche 6       | 0x09       | 0x06       |
| Zurück                         | Schaltfläche 7       | 0x09       | 0x07       |
| START                        | Schaltfläche 8       | 0x09       | 0x08       |
| LSB (Schaltfläche für den linken Strich)      | Schaltfläche 9       | 0x09       | 0x09       |
| RSB (Schaltfläche rechts Strich)     | Schaltfläche 10      | 0x09       | 0x0A       |

> [!Note]  
> ( \* ): Dies wird kombiniert, sodass Z das von den meisten Titeln erwartete ceningverhalten für die Rotation anzeigt. Dies bedeutet, dass es nicht möglich ist, alle möglichen Werte der Auslöse Kombination über [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85)) und HID anzuzeigen.

## <a name="arcade-stickarcade-pad"></a>Pad-Pad/-polarpad

Dabei handelt es sich um die Zuordnung, die für den Arcade-Stick-Controller entwickelt wurde und der als *Gamepad* -versteckungstyp verfügbar gemacht wird Das Arkaden Pad ähnelt einem anderen, aber in einem kleineren Formfaktor. Diese Entwürfe ersetzen den analogen linken und den rechten-Auslösers durch digitale Schaltflächen, die den minimalen und maximalen Achsen Wert melden.

| Control                     | Name der HID-Verwendung | Seite "Verwendung" | Nutzungs-ID |
|-----------------------------|----------------|------------|----------|
| D: Auffüllung nach oben, unten, Links, rechts | Hat-Schalter     | 0x01       | 0x39     |
| A                           | Schaltfläche 1       | 0x09       | 0x01     |
| B                           | Schaltfläche 2       | 0x09       | 0x02     |
| X                           | Schaltfläche 3       | 0x09       | 0x03     |
| J                           | Schaltfläche 4       | 0x09       | 0x04     |
| LB (linker-Stoßfänger)            | Schaltfläche 5       | 0x09       | 0x05     |
| RB (Rechte Stoßstange)           | Schaltfläche 6       | 0x09       | 0x06     |
| Zurück                        | Schaltfläche 7       | 0x09       | 0x07     |
| START                       | Schaltfläche 8       | 0x09       | 0x08     |
| Linker-Auslösung                | Schaltfläche 9       | 0x09       | 0x09     |
| Rechter Auslösers               | Schaltfläche 10      | 0x09       | 0x0A     |

Diese Geräte unterstützen möglicherweise zusätzliche Steuerelemente, aber Sie werden nicht durch die versteckte Zuordnung verfügbar gemacht: Linker, rechter Strich, LSB (Schaltfläche für den linken Strich) und RSB (Schaltfläche für den rechten Strich).

## <a name="wheel"></a>Wheel

Diese Zuordnung ist um das Xbox-Rennrad ausgelegt und wird als *Gamepad* -versteckungstyp verfügbar gemacht.

| Control                                                        | Name der HID-Verwendung | Seite "Verwendung" | Nutzungs-ID |
|----------------------------------------------------------------|----------------|------------|----------|
| Rad (linker Strich X)                                           | X              | 0x01       | 0x30     |
| Zugriffstaste (rechter Auslöse Taste) + Brems Taste (linker-Auslösung) | Z\*            | 0x01       | 0x32     |
| D: Auffüllung nach oben, unten, Links, rechts                                    | Hat-Schalter     | 0x01       | 0x39     |
| A                                                              | Schaltfläche 1       | 0x09       | 0x01     |
| B                                                              | Schaltfläche 2       | 0x09       | 0x02     |
| X                                                              | Schaltfläche 3       | 0x09       | 0x03     |
| J                                                              | Schaltfläche 4       | 0x09       | 0x04     |
| LB (linker-Stoßfänger)                                               | Schaltfläche 5       | 0x09       | 0x05     |
| RB (Rechte Stoßstange)                                              | Schaltfläche 6       | 0x09       | 0x06     |
| LSB (Schaltfläche für den linken Strich)                                        | Schaltfläche 7       | 0x09       | 0x07     |
| RSB (Schaltfläche rechts Strich)                                       | Schaltfläche 8       | 0x09       | 0x08     |
| Zurück                                                           | Schaltfläche 9       | 0x09       | 0x09     |
| START                                                          | Schaltfläche 10      | 0x09       | 0x0A     |

> [!Note]  
> ( \* ): Dies wird kombiniert, sodass Z das von den meisten Titeln erwartete cenboardingverhalten für die Brems-und Beschleunigungs Steuerelemente anzeigt. Dies bedeutet, dass es nicht möglich ist, alle möglichen Pedal Kombinations Werte durch [DirectInput](/previous-versions/windows/desktop/ee416842(v=vs.85))anzuzeigen.

## <a name="flight-stick"></a>Flugstick

Diese Zuordnung ist um den Xbox-Flight-Stick ausgelegt und wird als *Joystick* -Auslastungstyp verfügbar gemacht.

| Control                     | Verwendungs Name | Seite "Verwendung" | Nutzungs-ID   |
|-----------------------------|------------|------------|------------|
| Flugstick (Linker Stick)   | X, Y       | 0x01       | 0x30, 0x31 |
| POV hat (rechter Stick)       | RX, Ry     | 0x01       | 0x33, 0x34 |
| Drosselung (rechter Auslösung)    | Z          | 0x01       | 0x32       |
| Rudder (linker-Auslösung)       | Rz         | 0x01       | 0x35        |
| D: Auffüllung nach oben, unten, Links, rechts | Hat-Schalter | 0x01       | 0x39       |
| Primäre Waffe (A)          | Schaltfläche 1   | 0x09       | 0x01       |
| Sekundäre Waffe (B)        | Schaltfläche 2   | 0x09       | 0x02       |
| X                           | Schaltfläche 3   | 0x09       | 0x03       |
| J                           | Schaltfläche 4   | 0x09       | 0x04       |
| LB (linker-Stoßfänger)            | Schaltfläche 5   | 0x09       | 0x05       |
| RB (Rechte Stoßstange)           | Schaltfläche 6   | 0x09       | 0x06       |
| Zurück                        | Schaltfläche 7   | 0x09       | 0x07       |
| START                       | Schaltfläche 8   | 0x09       | 0x08       |
| LSB (Schaltfläche für den linken Strich)     | Schaltfläche 9   | 0x09       | 0x09       |
| RSB (Schaltfläche rechts Strich)    | Schaltfläche 10  | 0x09       | 0x0A       |

> [!Note]  
> Dies basiert auf dem endgültigen Entwurf des Flug stabsticks. Da dies sich von den frühen Flug Stick Definitionen unterscheidet, haben viele Geräte einen Modusschalter, der das alte und neue Modell unterstützt. Diese Zuordnung setzt das neue Modell voraus.