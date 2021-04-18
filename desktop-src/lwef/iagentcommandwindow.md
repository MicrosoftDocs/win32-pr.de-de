---
title: Iagentcommandwindow
description: Iagentcommandwindow
ms.assetid: 315b24b4-110e-4373-a1ee-0317531e6008
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 517f43bf482d043b4ca36ff749e3f496ba2988b7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106338600"
---
# <a name="iagentcommandwindow"></a>Iagentcommandwindow

\[Der Microsoft-Agent ist ab Windows 7 veraltet und in nachfolgenden Versionen von Windows möglicherweise nicht verfügbar.\]

**Iagentcommandwindow** definiert eine Schnittstelle, die es Anwendungen ermöglicht, die Eigenschaften des Fensters "Sprachbefehle" festzulegen und abzufragen. Das Fenster "Sprachbefehle" ist eine freigegebene Ressource, die in erster Linie so konzipiert ist, dass Benutzer sprach fähige Befehle anzeigen können. Wenn die Spracherkennung deaktiviert ist, wird das Fenster für die Sprachbefehle weiterhin angezeigt, und der Text "Spracheingabe ist deaktiviert" (in der Sprache des Zeichens). Wenn keine Sprach-Engine installiert ist, die mit der Spracheinstellung des Zeichens übereinstimmt, zeigt das Fenster an, dass die Spracheingabe nicht verfügbar ist. Wenn der Input-Active Client keine sprach Parameter für seine Befehle definiert hat und die globalen Sprachbefehle deaktiviert sind, wird im Fenster "keine Sprachbefehle" angezeigt. Sie können auch die Eigenschaften des Fensters "Sprachbefehle" Abfragen, unabhängig davon, ob die Spracheingabe deaktiviert ist oder eine kompatible Sprach-Engine installiert ist.

**Methoden in Vtable-Reihenfolge**



| Iagentcommandwindow-Methoden                             | BESCHREIBUNG                                                                                         |
|---------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [**SetVisible**](iagentcommandwindow--setvisible.md)   | Legt den Wert der [**Visible**](visible-property.md) -Eigenschaft des Sprachbefehle Fensters fest.    |
| [**GetVisible**](iagentcommandwindow--getvisible.md)   | Gibt den Wert der [**Visible**](visible-property.md) -Eigenschaft des Sprachbefehle Fensters zurück. |
| [**GetPosition**](iagentcommandwindow--getposition.md) | Gibt die Position des Sprachbefehle Fensters zurück.                                                  |
| [**GetSize**](iagentcommandwindow--getsize.md)         | Gibt die Größe des Sprachbefehle Fensters zurück.                                                      |



 

 

 




