---
title: Das CommandsWindow-Objekt
description: Das CommandsWindow-Objekt
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 336bdff598a75a9b0b07adabb11c271a45ca84940f528ebe082de17841592d31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117882464"
---
# <a name="the-commandswindow-object"></a>Das CommandsWindow-Objekt

\[Microsoft Agent ist ab Version Windows 7 veraltet und in nachfolgenden Versionen von Windows.\]

Das [**CommandsWindow-Objekt**](/windows/desktop/lwef/the-commandswindow-object) ermöglicht den Zugriff auf Eigenschaften des Fensters für Sprachbefehle. Das Fenster "Sprachbefehle" ist eine freigegebene Ressource, die hauptsächlich dazu dient, Benutzern das Anzeigen sprachfähiger Befehle zu ermöglichen. Wenn die Spracherkennung deaktiviert ist, wird das Fenster "Sprachbefehle" weiterhin mit dem Text "Spracheingabe deaktiviert" (in der Sprache des Zeichens) angezeigt. Wenn keine Sprach-Engine installiert ist, die der Spracheinstellung des Zeichens entspricht, wird im Fenster "Spracheingabe nicht verfügbar" angezeigt. Wenn der eingabeaktive Client keine Sprachparameter für seine Befehle definiert und globale Sprachbefehle deaktiviert hat, wird im Fenster "No voice commands" (Keine Sprachbefehle) angezeigt. Sie können auch die Eigenschaften des Sprachbefehlsfensters abfragen, unabhängig davon, ob die Spracheingabe deaktiviert oder eine kompatible Sprach-Engine installiert ist.

-   [BefehleWindow-Eigenschaften](commandswindow-properties.md)

 

 