---
title: Benutzerdefiniertes Zeichnen
description: Benutzerdefiniertes Zeichnen ist kein gängiges Steuerelement. es ist ein Dienst, den viele gängige Steuerelemente bereitstellen.
ms.assetid: vs|controls|~\controls\custdraw\custdraw.htm
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 16271e915a942e21f3f3763237a25c37a8b934fc1a44a016bb7e3938491a3c66
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118413178"
---
# <a name="custom-draw"></a>Benutzerdefiniertes Zeichnen

Benutzerdefiniertes Zeichnen ist kein gängiges Steuerelement. es ist ein Dienst, den viele gängige Steuerelemente bereitstellen. Der benutzerdefinierte Zeichnen-Dienst ermöglicht einer Anwendung mehr Flexibilität beim Anpassen der Darstellung eines Steuerelements. Ihre Anwendung kann benutzerdefinierte Zeichnen-Benachrichtigungen nutzen, um die Schriftart, die zum Anzeigen von Elementen verwendet wird, einfach zu ändern oder ein Element manuell zu zeichnen, ohne dass ein vollständiges Zeichnen des Besitzers durchgeführt werden muss.

Dieser Abschnitt enthält Informationen zu den Programmierelementen, die mit dem benutzerdefinierten Zeichnen verwendet werden.

## <a name="overviews"></a>Übersichten



| Thema                                      | Inhalte                                                                                                                                                               |
|--------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Informationen zum benutzerdefinierten Zeichnen](about-custom-draw.md) | Dieser Abschnitt enthält allgemeine Informationen zur benutzerdefinierten Zeichnen-Funktionalität und bietet eine konzeptionelle Übersicht darüber, wie eine Anwendung benutzerdefiniertes Zeichnen unterstützen kann.<br/> |
| [Verwenden von benutzerdefiniertem Zeichnen](using-custom-draw.md) | Dieser Abschnitt enthält Beispiele, die veranschaulichen, wie benutzerdefiniertes Zeichnen implementiert wird. <br/>                                                                              |



 

## <a name="notifications"></a>Benachrichtigungen



| Thema                               | Inhalte                                                                                                                                                                 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [NM \_ CUSTOMDRAW](nm-customdraw.md) | Benachrichtigt das übergeordnete Fenster eines Steuerelements über benutzerdefinierte Zeichnungsvorgänge. Dieser Benachrichtigungscode wird in Form einer [**WM \_ NOTIFY-Nachricht**](wm-notify.md) gesendet. <br/> |



 

## <a name="structures"></a>Strukturen



| Thema                                | Inhalte                                                                                              |
|--------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**NMCUSTOMDRAW**](/windows/win32/api/commctrl/ns-commctrl-nmcustomdraw) | Enthält spezifische Informationen zu einem [NM \_ CUSTOMDRAW-Benachrichtigungscode.](nm-customdraw.md)<br/> |



 

 

 





