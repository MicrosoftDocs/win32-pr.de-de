---
title: Parameter für die Barrierefreiheit
description: Das System verwaltet eine Reihe von Barrierefreiheitsparametern, die angeben, ob der Benutzer besondere Anforderungen oder Einstellungen hat, die erfordern, dass Anwendungen ihr Standardverhalten ändern.
ms.assetid: efa289bb-5965-4002-93df-116ab2621efc
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a289162366f5d69c501ffbea55108167324c11a1c865184105afd587f36bcfd3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118327788"
---
# <a name="accessibility-parameters"></a>Parameter für die Barrierefreiheit

Das System verwaltet eine Reihe von Barrierefreiheitsparametern, die angeben, ob der Benutzer besondere Anforderungen oder Einstellungen hat, die erfordern, dass Anwendungen ihr Standardverhalten ändern. Der Benutzer steuert den Status dieser Parameter, in der Regel mithilfe der Center für erleicherte Bedienung in Systemsteuerung. Systemsteuerung Anwendungen oder andere Programme, die es dem Benutzer ermöglichen, die Umgebung anzupassen, können die Barrierefreiheitsparameter mithilfe der [**SystemParametersInfo-Funktion**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) festlegen.

Wenn ein Benutzer diese Parameter ändert, sendet Systemsteuerung [**WM \_ SETTINGCHANGE-Nachricht.**](/windows/desktop/winmsg/wm-settingchange) Anwendungen sollten auf diese Meldung reagieren und [**SystemParametersInfo verwenden,**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa) um den Status der Barrierefreiheitsparameter zu bestimmen. Wenn ein Barrierefreiheitsparameter aktiviert ist, sollte die Anwendung bei Bedarf die Benutzeroberfläche ändern, um die Einstellungen des Benutzers zu berücksichtigen.

Windows unterstützt die folgenden Parameter für die Barrierefreiheit.



| Parameter                                                                    | Beschreibung                                                                                                                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Color Blind Friendly](high-contrast-parameter.md) (Für Farbenblinde)                                 | Gibt an, dass Anwendungen einen hohen Kontrast zwischen Vordergrund- und Hintergrundvisu visuals bereitstellen sollen.                                                                            |
| [Tastaturpräferenz](keyboard-preference-parameter.md)                     | Gibt an, dass Anwendungen Tastaturschnittstellen anzeigen sollen, die andernfalls ausgeblendet wären.                                                                                 |
| [Sprachausgabe](screen-reader-parameter.md)                                 | Gibt an, dass Anwendungen Textinformationen in Situationen bereitstellen sollen, in denen sie die Informationen andernfalls grafisch präsentieren würden.                                     |
| [Anzeigen von Sounds (und Audiobeschreibungsflag)](showsounds-parameter.md) | Gibt an, dass Anwendungen auch eine visuelle Warnung oder einen Hinweis bereitstellen sollten, wenn sound verwendet wird, um wichtige Informationen zu übermitteln, oder eine Audiobeschreibung für visuelle Elemente bereitstellen soll. |
| [Clientbereichsanimation](client-area-animation.md)                           | Gibt an, dass Anwendungen Die Benutzereinstellungen zum Anzeigen von Animationen im Clientbereich berücksichtigen sollen.                                                                       |
| [Nachrichtendauer](message-duration.md)                                     | Gibt an, dass Anwendungen, die Popupbenachrichtigungen bereitstellen, Flags zur Nachrichtendauer überwachen und ihre Benachrichtigungslänge anpassen müssen.                                  |



 

Die folgenden Systemparameter sind für Barrierefreiheitsanwendungen nützlich. Weitere Informationen finden Sie unter [**SystemParametersInfo-Funktion.**](/windows/desktop/api/winuser/nf-winuser-systemparametersinfoa)



| Parametergruppe      | Parameter                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Desktopparameter   | SPI \_ GETWORKAREA, SPI \_ SETWORKAREA                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                |
| Eingabeparameter     | SPI \_ GETKEYBOARDCUES, SPI \_ GETKEYBOARDDELAY, SPI \_ GETKEYBOARDPREF, \_ SPI GETKEYBOARDSPEED, SPI \_ GETMESSAGEDURATION, SPI \_ GETMOUSE, SPI \_ GETMOUSEHOVERHEIGHT, SPI \_ GETMOUSEHOVERTIME, SPI \_ GETMOUSEHOVERWIDTH, SPI \_ GETMOUSESPEED, SPI \_ GETMOUSETRAILS, SPI \_ GETSNAMESSAGEDEFBUTTON, SPI \_ GETWHEELSCROLLLINES, SPI \_ SETDOUBLECLICKTIME, SPI \_ SETDOUBLECLKHEIGHT, SPI \_ SETDOUBLECLKWIDTH, SPI \_ SETKEYBOARDCUES, SPI \_ SETKEYBOARDDELAY, SPI \_ SETKEYBOARDPREF, SPI \_ SETKEYBOARDSPEED, SPI \_ SETMOUSE, SPI \_ SETMOUSEHOVERHEIGHT, SPI \_ SETMOUSEHOVERTIME, SPI \_ SETMOUSEHOVERWIDTH, SPI \_ SETMOUSESPEED, SPI \_ SETMOUSETRAILS, SPI \_ SETSNA SYMPTOMDEFBUTTON, SPI \_ SETWHEELSCROLLLINES |
| Benutzeroberflächeneffektparameter | SPI \_ GETMENUUNDERLINES, SPI \_ SETMENUUNDERLINES                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    |
| Fensterparameter    | SPI \_ GETCARETWIDTH, SPI \_ GETFOREGROUNDFLASHCOUNT, SPI \_ GETFOREGROUNDLOCKTIMEOUT, SPI \_ SETCARETWIDTH, SPI \_ SETDRALUGIGHT, SPI \_ SETDRAGWIDTH, SPI \_ SETFOREGROUNDFLASHCOUNT, SPI \_ SETFOREGROUNDLOCKTIMEOUT                                                                                                                                                                                                                                                                                                                                                                                                                                                           |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen Windows Barrierefreiheitsfeatures](about-windows-accessibility-features.md)
</dt> </dl>

 

 