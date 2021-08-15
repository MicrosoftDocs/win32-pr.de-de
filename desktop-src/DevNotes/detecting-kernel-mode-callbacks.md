---
description: Wenn ein Thread auf den Abschluss eines Rückrufs im Kernelmodus wartet, verzögert sich die Benutzermodusseite des Threads bei einem Aufruf der ZwCallbackReturn-Funktion.
ms.assetid: 6d6d4f94-0e8c-4469-b905-731be6c4083d
title: Erkennen Kernel-Mode Rückrufe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029ecf7d5b1f9220de51c2ecffe4bdf30da4cbd088d9d251fd0d24bab04934e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119691450"
---
# <a name="detecting-kernel-mode-callbacks"></a>Erkennen Kernel-Mode Rückrufe

Der größte Teil des Codes für Windows Betriebssystem wird im Kernelmodus ausgeführt. Der Prozessormodus wechselt vom Benutzermodus in den Kernelmodus, wenn ein Anwendungsthread eine Funktion von der Windows-API aufruft, die wiederum eine interne Systemfunktion aufruft, die im Kernelmodus ausgeführt werden muss. Der Prozessormodus kehrt in den Benutzermodus zurück, bevor die Steuerung zur Funktion zurückkehrt, damit die Systemdaten geschützt werden.

Wenn ein Thread auf den Abschluss eines Rückrufs im Kernelmodus wartet, verzögert sich die Benutzermodusseite des Threads bei einem Aufruf der **ZwCallbackReturn-Funktion.**

 

 



