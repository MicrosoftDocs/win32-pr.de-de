---
description: Pseudo blockierende Pseudo Blockierungs Vorgänge in Windows Sockets (Winsock).
ms.assetid: fa8f29f1-bb4f-4814-ab8a-52d3c83232bb
title: Pseudo Blockierung und echte Blockierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 082992aba884aebec30d35bc65d2cb6c49e29051
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347073"
---
# <a name="pseudo-blocking-and-true-blocking"></a>Pseudo Blockierung und echte Blockierung

In 16 Windows-Umgebungen wird eine echte Blockierung vom Betriebssystem nicht unterstützt. Daher wird ein blockierender Vorgang, der nicht sofort abgeschlossen werden kann, wie folgt behandelt:

-   Der Dienstanbieter initiiert den Vorgang und gibt dann eine Schleife ein, in der alle Windows-Meldungen gesendet werden (falls erforderlich, wenn der Prozessor einem anderen Thread bereit steht).
-   Anschließend wird überprüft, ob die Windows Sockets-Funktion abgeschlossen ist.
-   Wenn die Funktion abgeschlossen wurde oder [**wspcancelblockingcallaufgerufen**](/previous-versions/windows/desktop/legacy/ms742269(v=vs.85)) wurde, wird die Schleife beendet, und die blockierende Funktion wird mit einem entsprechenden Ergebnis abgeschlossen.

Dies ist der Begriff "Pseudo Blockierung", und die oben erwähnte Schleife wird als standardmäßiger blockierender Hook bezeichnet.

 

 
