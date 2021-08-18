---
description: Für den Benutzer besteht der Vorteil von Multitasking darin, dass mehrere Anwendungen geöffnet sind und gleichzeitig funktionieren. Beispielsweise kann ein Benutzer eine Datei mit einer Anwendung bearbeiten, während eine andere Anwendung eine Kalkulationstabelle neu berechnet.
ms.assetid: 163291ce-78bd-43ee-98ca-564ce91c520c
title: Vorteile von Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 811bab71242022babc2a555225a9d02b248f42a03db28cfe1f636f4feb8fb962
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119143143"
---
# <a name="advantages-of-multitasking"></a>Vorteile von Multitasking

Für den Benutzer besteht der Vorteil von Multitasking darin, dass mehrere Anwendungen geöffnet sind und gleichzeitig funktionieren. Beispielsweise kann ein Benutzer eine Datei mit einer Anwendung bearbeiten, während eine andere Anwendung eine Kalkulationstabelle neu berechnet.

Für den Anwendungsentwickler ist der Vorteil von Multitasking die Möglichkeit, Anwendungen zu erstellen, die mehr als einen Prozess verwenden, und Prozesse zu erstellen, die mehr als einen Ausführungsthread verwenden. Ein Prozess kann beispielsweise über einen Benutzeroberflächenthread verfügen, der Interaktionen mit dem Benutzer verwaltet (Tastatur- und Mauseingabe) und Arbeitsthreads, die andere Aufgaben ausführen, während der Benutzeroberflächenthread auf Benutzereingaben wartet. Wenn Sie dem Benutzeroberflächenthread eine höhere Priorität einräumen, reagiert die Anwendung besser auf den Benutzer, während die Arbeitsthreads den Prozessor effizient verwenden, wenn keine Benutzereingaben vorhanden sind.

 

 



