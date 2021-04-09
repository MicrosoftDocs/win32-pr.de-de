---
description: Verwendung blockierender e/a-Vorgänge, nicht blockierende e/a-Vorgänge mit asynchroner Benachrichtigung über Netzwerkereignisse und überlappende e/a-Vorgänge mit Abschluss Angabe in Windows Sockets 2 (Winsock).
ms.assetid: 07f34177-72bc-4b2a-b655-57e53d1742b0
title: Socket-e/a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efcd325a0a379671dd39709f37e2c6d2133ca27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129117"
---
# <a name="socket-io"></a>Socket-e/a

Es gibt drei Hauptmethoden zum Ausführen von e/a-Vorgängen in Windows Sockets 2:

-   Blockierende e/a.
-   Nicht blockierende e/a-Vorgänge sowie asynchrone Benachrichtigungen von Netzwerk Ereignissen.
-   Überlappende e/a-Vorgänge mit Abschluss Angabe.

In den folgenden Abschnitten werden die einzelnen Methoden beschrieben. Blockierende e/a-Vorgänge sind das Standardverhalten, der nicht Blockierungs Modus kann für jeden Socket verwendet werden, der in den nicht blockierenden Modus versetzt wird. überlappende e/a-Vorgänge können nur bei Sockets auftreten, die mit dem überlappenden Attribut erstellt werden. Beachten Sie außerdem, dass die beiden Aufrufe zum Senden von: [**wspsend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) und [**wspsendto**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) und die beiden Aufrufe zum Empfangen von: [**wsprecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) und [**wsprecvfrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) jeweils alle drei e/a-Methoden implementieren. Dienstanbieter bestimmen, wie der e/a-Vorgang auf der Grundlage von Socketmodi, Attributen und Eingabeparameter Werten durchgeführt werden soll.

 

 
