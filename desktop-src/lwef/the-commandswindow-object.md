---
title: Das commandswindow-Objekt
description: Das commandswindow-Objekt
ms.assetid: f7f37499-f16b-47fb-85d1-23a68171bf0b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 574f803c12779f5ea9e690ca9c7a586d9d5df50e
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/19/2020
ms.locfileid: "106337215"
---
# <a name="the-commandswindow-object"></a>Das commandswindow-Objekt

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

Das [**commandswindow**](/windows/desktop/lwef/the-commandswindow-object) -Objekt ermöglicht den Zugriff auf Eigenschaften des Fensters "Sprachbefehle". Das Fenster "Sprachbefehle" ist eine freigegebene Ressource, die in erster Linie so konzipiert ist, dass Benutzer sprach fähige Befehle anzeigen können. Wenn die Spracherkennung deaktiviert ist, wird das Fenster für die Sprachbefehle weiterhin angezeigt, und der Text "Spracheingabe ist deaktiviert" (in der Sprache des Zeichens). Wenn keine Sprach-Engine installiert ist, die der Spracheinstellung des Zeichens entspricht, zeigt das Fenster an, dass die Spracheingabe nicht verfügbar ist. Wenn der Input-Active Client keine sprach Parameter für seine Befehle definiert hat und die globalen Sprachbefehle deaktiviert sind, wird im Fenster "keine Sprachbefehle" angezeigt. Sie können auch die Eigenschaften des Fensters "Sprachbefehle" Abfragen, unabhängig davon, ob die Spracheingabe deaktiviert ist oder eine kompatible Sprach-Engine installiert ist.

-   [Commandswindow-Eigenschaften](commandswindow-properties.md)

 

 