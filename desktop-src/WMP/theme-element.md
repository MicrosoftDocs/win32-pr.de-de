---
title: Design-Element
description: Design-Element
ms.assetid: fe7e793e-1774-412c-aed2-721ed2cf1bb3
keywords:
- Windows Media Player Skins, Theme-Element
- Skins, Theme-Element
- Design-Element
- Verweis für Skins, Theme-Element
- Elemente, Design
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8cd0d40b4b020cf5416569417401af9e4f3a33b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855760"
---
# <a name="theme-element"></a>Design-Element

Das **Designelement ist das Element** auf der übergeordneten Ebene eines Skin und enthält mindestens ein **Ansichts** Element, das wiederum alle anderen Elemente in einer Skin enthält. Innerhalb von Skriptcode wird **auf das Design** Element über das **globale Design** -Attribut und nicht über einen durch ein **ID** -Attribut angegebenen Namen zugegriffen, der vom Design **-Element nicht** unterstützt wird.

Das **Theme** -Element unterstützt die folgenden Attribute.



| Attribut                                | BESCHREIBUNG                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [Schrift](theme-author.md)               | Gibt den Namen des Autors der Skin an oder ruft ihn ab.                                                                      |
| [authorversion](theme-authorversion.md) | Gibt die vom Autor zugewiesene Versionsnummer der Skin an oder ruft diese ab.                                                |
| [Copyright](theme-copyright.md)         | Gibt die Copyright Zeichenfolge für die Skin an oder ruft Sie ab.                                                                       |
| [currentViewID](theme-currentviewid.md) | Gibt die aktuell angezeigte **Ansicht** an oder ruft Sie ab.                                                                        |
| [title](theme-title.md)                 | Gibt den Titel der Skin an oder ruft ihn ab.                                                                                   |
| [version](theme-version.md)             | Gibt die Windows Media Player-Versionsnummer an, für die die Skin erstellt wurde, oder ruft Sie ab. Kann nur zur Entwurfszeit festgelegt werden. |



 

Das **Theme** -Element unterstützt die folgenden Methoden.



| Methode                                         | BESCHREIBUNG                                                                                                     |
|------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [Close View](theme-closeview.md)               | Schließt eine geöffnete **Ansicht**.                                                                                        |
| [loadpreference](theme-loadpreference.md)     | Lädt eine Präferenz aus der Registrierung.                                                                           |
| [logstring](theme-logstring.md)               | Protokolliert eine benutzerdefinierte Zeichenfolge in der Fehler Datei, wenn die Protokollierung aktiviert ist.                                            |
| [OpenDialog](theme-opendialog.md)             | Öffnet ein Datei Dialogfeld.                                                                                        |
| [OpenView –](theme-openview.md)                 | Öffnet eine **Ansicht** in einem neuen Fenster.                                                                               |
| [openviewrelative](theme-openviewrelative.md) | Öffnet eine **Ansicht** in einem neuen Fenster an einer angegebenen Anfangsposition relativ zur oberen linken Ecke der Skin. |
| [PlaySound](theme-playsound.md)               | Gibt die angegebene Audiodatei wieder.                                                                                 |
| [savepreference](theme-savepreference.md)     | Speichert eine Einstellung in der Registrierung.                                                                             |
| [showerrordialog](theme-showerrordialog.md)   | Zeigt das Dialogfeld Standardfehler an.                                                                         |



 

Das **Theme** -Element unterstützt keine Ereignishandler.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Referenz zur Skin-Programmierung**](skin-programming-reference.md)
</dt> </dl>

 

 




