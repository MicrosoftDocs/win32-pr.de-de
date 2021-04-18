---
title: Barrierefreiheits Parameter
description: Das System verwaltet eine Reihe von Barrierefreiheits Parametern, die angeben, ob der Benutzer besondere Anforderungen oder Einstellungen hat, die erfordern, dass Anwendungen sein Standardverhalten ändern.
ms.assetid: efa289bb-5965-4002-93df-116ab2621efc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5f089b28d36ffa982ca6568996126a812263af9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341320"
---
# <a name="accessibility-parameters"></a>Barrierefreiheits Parameter

Das System verwaltet eine Reihe von Barrierefreiheits Parametern, die angeben, ob der Benutzer besondere Anforderungen oder Einstellungen hat, die erfordern, dass Anwendungen sein Standardverhalten ändern. Der Benutzer steuert den Zustand dieser Parameter, üblicherweise mithilfe der Easy of Access Center in der Systemsteuerung. System Steuerungsanwendungen oder andere Programme, die es dem Benutzer ermöglichen, die Umgebung anzupassen, können die [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion verwenden, um die Barrierefreiheits Parameter festzulegen.

Wenn ein Benutzer diese Parameter ändert, sendet die Systemsteuerung die " [**WM \_ settingchange**](/windows/desktop/winmsg/wm-settingchange) "-Meldung. Anwendungen sollten auf diese Meldung reagieren und mithilfe von [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) den Status der Barrierefreiheits Parameter ermitteln. Wenn ein Barrierefreiheits Parameter aktiviert ist, sollte die Anwendung ggf. die Benutzeroberfläche ändern, um die Einstellungen des Benutzers zu berücksichtigen.

Windows unterstützt die folgenden Barrierefreiheits Parameter.



| Parameter                                                                    | BESCHREIBUNG                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Color Blind Friendly](high-contrast-parameter.md) (Für Farbenblinde)                                 | Gibt an, dass Anwendungen einen hohen Kontrast zwischen Vordergrund-und Hintergrund visuellen Elementen bieten sollen.                                                                            |
| [Tastatur Präferenz](keyboard-preference-parameter.md)                     | Gibt an, dass in Anwendungen Tastatur Schnittstellen angezeigt werden sollen, die andernfalls ausgeblendet werden.                                                                                 |
| [Bildschirmleser](screen-reader-parameter.md)                                 | Gibt an, dass Anwendungen Textinformationen in Situationen bereitstellen sollten, in denen Sie die Informationen andernfalls grafisch darstellen würden.                                     |
| [Sounds anzeigen (und audiobeschreibungs-Flag)](showsounds-parameter.md) | Gibt an, dass Anwendungen auch eine visuelle Warnung oder einen Hinweis bereitstellen sollten, wenn Sound zum vermitteln wichtiger Informationen verwendet wird, oder eine Audiobeschreibung für visuelle Elemente bereitstellen. |
| [Animation des Client Bereichs](client-area-animation.md)                           | Gibt an, dass Anwendungen die Benutzereinstellungen für die Anzeige von Animationen im Client Bereich berücksichtigen sollen.                                                                       |
| [Nachrichten Dauer](message-duration.md)                                     | Gibt an, dass Anwendungen, die Popup Benachrichtigungen bereitstellen, Flags zur Nachrichten Dauer überwachen und deren Benachrichtigungs Länge anpassen müssen.                                  |



 

Die folgenden Systemparameter sind nützlich für Barrierefreiheits Anwendungen. Weitere Informationen finden Sie unter [**SystemParametersInfo**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) -Funktion.



| Parameter Gruppe      | Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Desktop Parameter   | SPI- \_ getworkarea, SPI- \_ setworkarea                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Eingabeparameter     | SPI \_ getkeyboardcues, SPI \_ getkeyboarddelay, SPI \_ getkeyboardpref, SPI \_ getkeyboardspeed, SPI \_ getmessageduration, SPI \_ getmouse, SPI \_ getmousehoverheight, SPI \_ getmousehovertime, SPI \_ getmousehoverwidth, SPI \_ getmousespeed, SPI \_ getmousetrails, SPI \_ geznaptredefbutton, SPI \_ getwheelscrolllines, SPI \_ setdoubleclicktime, SPI \_ setdoubleclkheight, SPI \_ setdoubleclkwidth, SPI \_ setkeyboardcues, SPI \_ setkeyboarddelay, SPI \_ setkeyboardpref, SPI \_ setkeyboardspeed, SPI \_ setmouse, SPI \_ setmousehoverheight, SPI \_ setmousehovertime, SPI \_ setmousehoverwidth, SPI \_ setmousespeed, SPI \_ setmousetrails, SPI \_ seznapondefbutton, SPI \_ setwheelscrolllines |
| Parameter der UI-Auswirkung | SPI \_ getmenustrichen, SPI \_ setmenustrichen                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Fenster Parameter    | SPI \_ getcaretwidth, SPI \_ getforegroundflash count, SPI \_ getforegroundlocktimeout, SPI \_ setcaretwidth, SPI \_ setdragheight, SPI \_ setdragwidth, SPI \_ setforegroundflash count, SPI \_ setforegroundlocktimeout                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zu Windows-Barrierefreiheits Features](about-windows-accessibility-features.md)
</dt> </dl>

 

 