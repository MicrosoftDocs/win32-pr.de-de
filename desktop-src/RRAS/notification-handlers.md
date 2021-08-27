---
title: Benachrichtigungshandler
description: Ein asynchroner RasDial-Aufruf muss einen Benachrichtigungshandler angeben.
ms.assetid: 6d23d6ac-08ad-4fe2-a4af-021e4d384079
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: af7210072e0542eeb63e3de6116d61995ef2363ca7b43e7a9e2c309165c0e862
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074030"
---
# <a name="notification-handlers"></a>Benachrichtigungshandler

Ein [**asynchroner RasDial-Aufruf**](/windows/desktop/api/Ras/nf-ras-rasdiala) muss einen Benachrichtigungshandler angeben. Während eines asynchronen Verbindungsvorgang verwendet die Remotezugriffs-Verbindungs-Manager den [](connection-states.md) Benachrichtigungshandler, um den RAS-Client zu informieren, wenn sich der Verbindungsstatus ändert oder ein Fehler auftritt.

Die von einem Benachrichtigungshandler ausgeführten Aktionen können in die folgenden Kategorien unterteilt werden:

-   [Behandeln von Fehlern](handling-ras-errors.md).
-   Senden von Feedback an den Benutzer, während der Verbindungsvorgang die verschiedenen Verbindungszustände durchläuft. Weitere Informationen [finden Sie unter Informationsbenachrichtigungen.](informational-notifications.md)
-   Behandeln [angehaltener Zustände.](paused-states.md)
-   Signalisieren der RAS-Clientanwendung, wenn der Verbindungsvorgang abgeschlossen wurde. Weitere Informationen [finden Sie unter Vervollständigungsbenachrichtigungen.](completion-notifications.md)

Es gibt drei Arten von Benachrichtigungshandlern, von denen jeder die gleichen grundlegenden Informationen empfängt: den aktuellen Verbindungsstatus und einen Fehlercode, der nur dann ungleich 0 (null) ist, wenn ein Fehler aufgetreten ist.



| Wert                                | Definition                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
|--------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**RasDialFunc**](/windows/desktop/api/Ras/nc-ras-rasdialfunc)   | Ein Rückruffunktionsprototyp, der nur den aktuellen Verbindungsstatus und Fehlercodeinformationen empfängt.                                                                                                                                                                                                                                                                                                                                                                                    |
| [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) | Ein Rückruffunktionsprototyp, der zusätzlich zu den grundlegenden Informationen das **HR MRTNN-Verbindungshand** handle und erweiterte Fehlerinformationen empfängt. Der Verbindungshandleparameter macht [**RasDialFunc1**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) für Clientanwendungen nützlich, die mehrere gleichzeitige Verbindungsvorgänge unterstützen. Dadurch kann der Client dieselbe Rückruffunktion für alle Vorgänge angeben, und die Rückruffunktion kann bestimmen, welche Verbindung den Status ändert. |
| [**RasDialFunc2**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) | Eine Rückruffunktion, die [**RasDialFunc1 ähnelt.**](/windows/desktop/api/Ras/nc-ras-rasdialfunc1) [**RasDialFunc2 wurde**](/windows/desktop/api/Ras/nc-ras-rasdialfunc2) jedoch erweitert, um Multilinkverbindungen zu unterstützen.                                                                                                                                                                                                                                                                                                                             |
| Fensterhand handle                        | Ein Fensterhandle, an das RAS [**WM \_ RASDIALEVENT-Meldungen**](wm-rasdialevent.md) sendet, die den aktuellen Verbindungsstatus und Fehlercodeinformationen enthalten. Verwenden Sie diese Methode, wenn Ihr Quellcode mit 16-Bit-Windows kompatibel sein muss, da 16-Bit-Windows keine der Rückruffunktionen unterstützt.                                                                                                                                                                            |



 

Der Remotezugriffsserver Verbindungs-Manager den Verbindungsvorgang an, bis der Benachrichtigungshandler zurückgegeben wird. Aus diesem Grund sollte der Handler so bald wie möglich zurückgeben, es sei denn, es ist ein Fehler aufgetreten.

Die [**RasDial-Funktion**](/windows/desktop/api/Ras/nf-ras-rasdiala) sollte nicht innerhalb eines Benachrichtigungshandlers aufgerufen werden. Die anderen Remotezugriffsfunktionen ( [**RasGetConnectStatus**](/windows/desktop/api/Ras/nf-ras-rasgetconnectstatusa), [**RasEnumEntries**](/windows/desktop/api/Ras/nf-ras-rasenumentriesa), [**RasEnumConnections**](/windows/desktop/api/Ras/nf-ras-rasenumconnectionsa), [**RasGetErrorString**](/windows/desktop/api/Ras/nf-ras-rasgeterrorstringa)und [**RasHangUp**](/windows/desktop/api/Ras/nf-ras-rashangupa)) können innerhalb eines Handlers aufgerufen werden.

 

 




