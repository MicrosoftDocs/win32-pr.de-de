---
title: Synchrone Vorgänge
description: Wenn RasDial als synchroner Vorgang aufgerufen wird, gibt die Funktion erst dann zurück, wenn die Verbindung hergestellt wurde oder ein Fehler auftritt.
ms.assetid: 5333ca88-bcec-48bc-88d2-3c6c0701802e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80c923a22758e7d6b9563cde9e4c9b2ce6036afa47f85116c0c18ed523996e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120025610"
---
# <a name="synchronous-operations"></a>Synchrone Vorgänge

Wenn [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) als synchroner Vorgang aufgerufen wird, gibt die Funktion erst dann zurück, wenn die Verbindung hergestellt wurde oder ein Fehler auftritt. Der synchrone Modus bietet einem RAS-Client eine einfache Möglichkeit, eine Verbindung herzustellen. Der Client kann einfach **RasDial** aufrufen, warten, bis die Funktion zurückgegeben wird, und dann die [**RasGetConnectStatus-Funktion**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) aufrufen, um zu bestimmen, ob der Verbindungsvorgang erfolgreich war. Nachdem die Verbindung hergestellt wurde, kann die Clientanwendung beendet werden, ohne die Verbindung zu beenden. Wenn ein Fehler auftritt, muss die Clientanwendung den Verbindungsvorgang vor dem Beenden [herunterfahren.](disconnecting.md)

Der Nachteil des synchronen Modus ist, dass der Client keine Statusbenachrichtigungen empfängt, während der Verbindungsvorgang fortgesetzt wird. Als Problemumgehung für dieses Fehlen von Statusbenachrichtigungen kann ein Client im synchronen Modus einen separaten Thread verwenden, der [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa) aufruft, um den aktuellen Status abzufragen und anzuzeigen. Für RAS-Clients, die Statusinformationen erhalten möchten, besteht die bevorzugte Technik jedoch darin, [**RasDial**](/windows/desktop/api/Ras/nf-ras-rasdiala) asynchron aufzurufen.

 

 




