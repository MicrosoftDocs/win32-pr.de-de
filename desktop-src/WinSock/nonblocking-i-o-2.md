---
description: Wenn sich ein Socket im nicht blockierenden Modus befindet, muss jeder e/a-Vorgang entweder sofort abgeschlossen werden oder den Fehlercode "WSAEWOULDBLOCK" zurückgeben, der angibt, dass der Vorgang nicht sofort abgeschlossen werden kann.
ms.assetid: badd279b-ec71-4761-9066-d501aa2485c2
title: Nicht blockierende Eingabe/Ausgabe
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df9f6fec896c8daf1998e71a20a23a296b7b5a72
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104526129"
---
# <a name="nonblocking-inputoutput"></a>Nicht blockierende Eingabe/Ausgabe

Wenn sich ein Socket im nicht blockierenden Modus befindet, muss jeder e/a-Vorgang entweder sofort abgeschlossen werden oder den Fehlercode "WSAEWOULDBLOCK" zurückgeben, der angibt, dass der Vorgang nicht sofort abgeschlossen werden kann. Im letzteren Fall ist ein Mechanismus erforderlich, um zu ermitteln, wann es sinnvoll ist, den Vorgang erneut auszuführen, und es wird davon ausgegangen, dass der Vorgang erfolgreich ausgeführt werden kann. Zu diesem Zweck wurde eine Gruppe von Netzwerk Ereignissen definiert. Diese Ereignisse können mithilfe von [**wspselect**](/previous-versions/windows/desktop/legacy/ms742289(v=vs.85))abgerufen oder gewartet werden, oder Sie können für die asynchrone Übermittlung durch Aufrufen von [**wspasyncselect**](/previous-versions/windows/desktop/legacy/ms742267(v=vs.85)) oder [**wspeventselect**](/previous-versions/windows/hardware/network/ff566287(v=vs.85))registriert werden. Weitere Informationen finden Sie [unter Benachrichtigung zu Netzwerk Ereignissen](notification-of-network-events-2.md) .

 

 
