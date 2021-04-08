---
title: Synchrone Vorgänge
description: Wenn "rasdial" als synchroner Vorgang aufgerufen wird, gibt die Funktion erst dann zurück, wenn die Verbindung hergestellt wurde oder ein Fehler auftritt.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2463e3112c3faac4d7601023ea73f0182e2d5b73
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037446"
---
# <a name="synchronous-operations"></a>Synchrone Vorgänge

Wenn " [**rasdial**](/windows/desktop/api/Ras/nf-ras-rasdiala) " als synchroner Vorgang aufgerufen wird, gibt die Funktion erst dann zurück, wenn die Verbindung hergestellt wurde oder ein Fehler auftritt. Der synchrone Modus ist eine einfache Möglichkeit für einen RAS-Client, eine Verbindung herzustellen. Der Client kann einfach " **rasdial**" aufrufen, warten, bis die Funktion zurückgegeben wird, und dann die Funktion " [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) " aufrufen, um zu bestimmen, ob der Verbindungsvorgang erfolgreich war. Nachdem die Verbindung hergestellt wurde, kann die Client Anwendung beendet werden, ohne dass die Verbindung unterbrochen wird. Wenn ein Fehler auftritt, muss die Client Anwendung [den Verbindungsvorgang](disconnecting.md) beenden, bevor Sie beendet wird.

Der Nachteil des synchronen Modus besteht darin, dass der Client keine Status Benachrichtigungen empfängt, während der Verbindungsvorgang fortgesetzt wird. Um diese fehlende Fortschritts Benachrichtigung zu umgehen, kann ein Client im synchronen Modus einen separaten Thread verwenden, der " [**rasgetconnectstatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) " aufruft, um den aktuellen Status abzurufen und anzuzeigen. Für RAS-Clients, die Statusinformationen empfangen möchten, empfiehlt es sich jedoch, den Vorgang [**asynchron**](/windows/desktop/api/Ras/nf-ras-rasdiala) aufzurufen.

 

 




