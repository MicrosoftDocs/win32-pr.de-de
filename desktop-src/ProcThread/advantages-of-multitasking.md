---
description: Der Vorteil von Multitasking besteht darin, dass mehrere Anwendungen gleichzeitig geöffnet und funktionieren können. Ein Benutzer kann z. b. eine Datei mit einer Anwendung bearbeiten, während eine andere Anwendung eine Kalkulations Tabelle neu berechnet.
ms.assetid: 163291ce-78bd-43ee-98ca-564ce91c520c
title: Vorteile von Multitasking
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 119e327ba07a226a8422c61a100d6ff000b48ed9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106368744"
---
# <a name="advantages-of-multitasking"></a>Vorteile von Multitasking

Der Vorteil von Multitasking besteht darin, dass mehrere Anwendungen gleichzeitig geöffnet und funktionieren können. Ein Benutzer kann z. b. eine Datei mit einer Anwendung bearbeiten, während eine andere Anwendung eine Kalkulations Tabelle neu berechnet.

Der Vorteil von Multitasking besteht im Anwendungsentwickler in der Möglichkeit, Anwendungen zu erstellen, die mehr als einen Prozess verwenden, und Prozesse zu erstellen, die mehr als einen Ausführungs Thread verwenden. Ein Prozess kann z. b. über einen Benutzeroberflächen Thread verfügen, der Interaktionen mit dem Benutzer verwaltet (Tastatur-und Maus Eingaben), und Arbeitsthreads, die andere Aufgaben ausführen, während der Benutzeroberflächen Thread auf Benutzereingaben wartet. Wenn Sie dem Benutzeroberflächen Thread eine höhere Priorität geben, reagiert die Anwendung besser auf den Benutzer, während die Arbeitsthreads den Prozessor während der Zeiten, in denen keine Benutzereingaben vorhanden sind, effizient nutzen.

 

 



