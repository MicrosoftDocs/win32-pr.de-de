---
description: Pseudoblockierung von Pseudoblockierungsvorgängen in Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudoblockierung und true-Blockierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 371935a2f8984ebd080da48492807b3f5ffa9286b991b16b516244ccf26ee093
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117740942"
---
# <a name="pseudo-blocking-and-true-blocking"></a>Pseudoblockierung und true-Blockierung

In 16 Windows wird eine echte Blockierung vom Betriebssystem nicht unterstützt. Daher wird ein blockierende Vorgang, der nicht sofort abgeschlossen werden kann, wie folgt behandelt:

-   Der Dienstanbieter initiiert den Vorgang und gibt dann eine Schleife ein, in der er alle Windows-Nachrichten weitersendet (bei Bedarf wird der Prozessor an einen anderen Thread übermittelt).
-   Anschließend wird überprüft, ob die Sockets-Windows abgeschlossen ist.
-   Wenn die Funktion abgeschlossen wurde oder [**WSPCancelBlockingCall**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) aufgerufen wurde, wird die Schleife beendet, und die blockierende Funktion wird mit einem entsprechenden Ergebnis abgeschlossen.

Dies ist mit dem Begriff Pseudoblockierung gemeint, und die oben genannte Schleife wird als der standardmäßige blockierende Hook bezeichnet.

 

 
