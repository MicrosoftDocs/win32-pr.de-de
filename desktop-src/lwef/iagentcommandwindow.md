---
title: IAgentCommandWindow
description: IAgentCommandWindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80509efbe4f9d6391b3ac6ffbdf5cb02580826fd1aa7a94f1536ba5706322606
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119105178"
---
# <a name="iagentcommandwindow"></a>IAgentCommandWindow

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht mehr verfügbar.\]

**IAgentCommandWindow** definiert eine Schnittstelle, mit der Anwendungen die Eigenschaften des Fensters "Sprachbefehle" festlegen und abfragen können. Das Fenster "Sprachbefehle" ist eine freigegebene Ressource, die in erster Linie benutzern ermöglicht wird, sprachaktivierte Befehle anzuzeigen. Wenn die Spracherkennung deaktiviert ist, wird das Fenster "Sprachbefehle" weiterhin mit dem Text "Spracheingabe deaktiviert" (in der Sprache des Zeichens) angezeigt. Wenn keine Sprach-Engine installiert ist, die der Spracheinstellung des Zeichens entspricht, wird im Fenster "Speech input not available" (Spracheingabe nicht verfügbar) angezeigt. Wenn der eingabeaktive Client keine Sprachparameter für seine Befehle definiert und globale Sprachbefehle deaktiviert hat, wird im Fenster "Keine Sprachbefehle" angezeigt. Sie können auch die Eigenschaften des Fensters für Sprachbefehle abfragen, unabhängig davon, ob die Spracheingabe deaktiviert oder eine kompatible Sprach-Engine installiert ist.

**Methoden in Vtable-Reihenfolge**



| IAgentCommandWindow-Methoden                             | Beschreibung                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**Setvisible**](iagentcommandwindow--setvisible.md)   | Legt den Wert der [**Visible-Eigenschaft**](visible-property.md) des Sprachbefehlsfensters fest.    |
| [**Getvisible**](iagentcommandwindow--getvisible.md)   | Gibt den Wert der [**Visible-Eigenschaft**](visible-property.md) des Sprachbefehlsfensters zurück. |
| [**Getposition**](iagentcommandwindow--getposition.md) | Gibt die Position des Fensters "Sprachbefehle" zurück.                                                  |
| [**GetSize**](iagentcommandwindow--getsize.md)         | Gibt die Größe des Fensters "Sprachbefehle" zurück.                                                      |



 

 

 




