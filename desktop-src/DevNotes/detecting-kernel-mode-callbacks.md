---
description: Wenn ein Thread darauf wartet, dass ein Kernel Modus-Rückruf ausgeführt wird, verzögert sich die benutzermodusseite des Threads bei einem Aufruf der zwcallbackreturn-Funktion.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Erkennen von Kernel-Mode Rückrufen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c899615be416b266779236ea8bc36978a517b7ed
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958494"
---
# <a name="detecting-kernel-mode-callbacks"></a>Erkennen von Kernel-Mode Rückrufen

Der größte Teil des Codes für das Windows-Betriebssystem wird im Kernel Modus ausgeführt. Der Prozessor Modus wechselt vom Benutzermodus in den Kernel Modus, wenn ein Anwendungs Thread eine Funktion von der Windows-API aufruft, die wiederum eine interne Systemfunktion aufruft, die im Kernel Modus ausgeführt werden muss. Der Prozessor Modus kehrt in den Benutzermodus zurück, bevor die Steuerung an die Funktion zurückgegeben wird, sodass die Systemdaten geschützt sind.

Wenn ein Thread darauf wartet, dass ein Kernel Modus-Rückruf ausgeführt wird, verzögert sich die benutzermodusseite des Threads bei einem Aufruf der **zwcallbackreturn** -Funktion.

 

 



