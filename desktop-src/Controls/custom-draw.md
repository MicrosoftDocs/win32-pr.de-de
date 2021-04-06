---
title: Benutzerdefiniertes Zeichnen
description: Das benutzerdefinierte Zeichnen ist kein gängiges Steuerelement. Es handelt sich um einen Dienst, den viele gängige Steuerelemente bereitstellen.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5184d06dbb8e04185bf12a43c6c71dd96b933a6a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103947517"
---
# <a name="custom-draw"></a>Benutzerdefiniertes Zeichnen

Das benutzerdefinierte Zeichnen ist kein gängiges Steuerelement. Es handelt sich um einen Dienst, den viele gängige Steuerelemente bereitstellen. Der benutzerdefinierte Draw-Dienst ermöglicht einer Anwendung eine größere Flexibilität beim Anpassen der Darstellung eines Steuer Elements. Die Anwendung kann benutzerdefinierte Zeichnungs Benachrichtigungen nutzen, um die Schriftart, die zum Anzeigen von Elementen verwendet wird, zu ändern oder ein Element manuell zu zeichnen, ohne dass ein vollständiger Besitzer gezeichnet werden muss.

Dieser Abschnitt enthält Informationen zu den Programmier Elementen, die mit benutzerdefiniertem Zeichnen verwendet werden.

## <a name="overviews"></a>Übersichten



| Thema                                      | Inhalte                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zum benutzerdefinierten Zeichnen](about-custom-draw.md) | Dieser Abschnitt enthält allgemeine Informationen über benutzerdefinierte Zeichnungsfunktionen und bietet eine konzeptionelle Übersicht darüber, wie eine Anwendung benutzerdefiniertes Zeichnen unterstützen kann.<br/> |
| [Verwenden benutzerdefinierter zeichnen](using-custom-draw.md) | Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie benutzerdefiniertes Zeichnen implementiert wird. <br/>                                                                              |



 

## <a name="notifications"></a>Benachrichtigungen



| Thema                               | Inhalte                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ customdraw](nm-customdraw.md) | Benachrichtigt das übergeordnete Fenster eines Steuer Elements über benutzerdefinierte Zeichnungsvorgänge. Dieser Benachrichtigungs Code wird in Form einer WM- [**\_ Benachrichtigungs**](wm-notify.md) Meldung gesendet. <br/> |



 

## <a name="structures"></a>Strukturen



| Thema                                | Inhalte                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**Nmcustomdraw**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | Enthält Informationen, die für einen [nm \_ customdraw](nm-customdraw.md) -Benachrichtigungs Code spezifisch sind.<br/> |



 

 

 





