---
title: THEME-Element
description: THEME-Element
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Windows Media Player Skins, THEME-Element
- skins,THEME-Element
- THEME-Element
- Referenz für Skins, THEME-Element
- elements,THEME
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c15091ffa93e3ae64a06979580931c27bdf4c1cd2e26c7acc206d76de8b0fc4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119507390"
---
# <a name="theme-element"></a>THEME-Element

Das **THEME-Element** ist das Element auf übergeordneter Ebene einer Skin und enthält mindestens ein **VIEW-Element,** das wiederum alle anderen Elemente in einer Skin enthält. Innerhalb des Skriptcodes erfolgt der Zugriff auf das **THEME-Element** über das globale **Designattribut** und nicht über einen Namen, der durch ein **ID-Attribut** angegeben wird, was vom **THEME-Element** nicht unterstützt wird.

Das **THEME-Element** unterstützt die folgenden Attribute.



| attribute                                | Beschreibung                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Autor](theme-author.md)               | Gibt den Namen des Erstellers der Skin an oder ruft den Namen ab.                                                                      |
| [authorVersion](theme-authorversion.md) | Gibt die Versionsnummer der Skin an, die vom Autor zugewiesen wurde, oder ruft sie ab.                                                |
| [Copyright](theme-copyright.md)         | Gibt die Copyrightzeichenfolge für die Skin an oder ruft sie ab.                                                                       |
| [currentViewID](theme-currentviewid.md) | Gibt die aktuell angezeigte **VIEW** an oder ruft sie ab.                                                                        |
| [title](theme-title.md)                 | Gibt den Titel der Skin an oder ruft sie ab.                                                                                   |
| [version](theme-version.md)             | Gibt die Windows Media Player Versionsnummer an, für die die Skin erstellt wurde, oder ruft sie ab. Kann nur zur Entwurfszeit festgelegt werden. |



 

Das **THEME-Element** unterstützt die folgenden Methoden.



| Methode                                         | Beschreibung                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [closeView](theme-closeview.md)               | Schließt eine geöffnete **VIEW -Ansicht.**                                                                                        |
| [loadPreference](theme-loadpreference.md)     | Lädt eine Einstellung aus der Registrierung.                                                                           |
| [logString](theme-logstring.md)               | Protokolliert eine benutzerdefinierte Zeichenfolge in der Fehlerdatei, wenn die Protokollierung aktiviert ist.                                            |
| [openDialog](theme-opendialog.md)             | Öffnet ein Dateidialogfeld.                                                                                        |
| [Openview](theme-openview.md)                 | Öffnet eine **ANSICHT** in einem neuen Fenster.                                                                               |
| [openViewRelative](theme-openviewrelative.md) | Öffnet eine **ANSICHT** in einem neuen Fenster an einer angegebenen Anfangsposition relativ zur oberen linken Ecke der Skin. |
| [Playsound](theme-playsound.md)               | Gibt die angegebene Sounddatei wieder.                                                                                 |
| [savePreference](theme-savepreference.md)     | Speichert eine Einstellung in der Registrierung.                                                                             |
| [showErrorDialog](theme-showerrordialog.md)   | Zeigt das Standardfehlerdialogfeld an.                                                                         |



 

Das **THEME-Element** unterstützt keine Ereignishandler.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skinprogrammierung**](skin-programming-reference.md)
</dt> </dl>

 

 




