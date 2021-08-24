---
description: Erfahren Sie mehr über Funktionen, die bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet werden, die vom Druckspooler gehostet werden.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Asynchrone Druckbenachrichtigungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e7d533ad1a3d1a8201e5a2d91946a66daee6cecd796e7bcc8e9c14d2c593542c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720240"
---
# <a name="asynchronous-printing-notification-functions"></a>Asynchrone Druckbenachrichtigungsfunktionen

Die folgenden Funktionen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druckspooler gehostet werden, z. B. Druckertreiber und Portmonitore.

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion                                                                                        | Beschreibung                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | Erstellt einen Kommunikationskanal zwischen einer Druckspooler-gehosteten Druckkomponente, z. B. einem Druckertreiber oder Portmonitor, und einer Anwendung, die Benachrichtigungen von der Komponente empfängt.<br/> |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | Ermöglicht es einer Anwendung, sich für Benachrichtigungen von Druckspooler-gehosteten Druckkomponenten wie Druckertreibern, Druckprozessoren und Portmonitoren zu registrieren.<br/>                              |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | Ermöglicht einer Anwendung, die für den Empfang von Benachrichtigungen von Druckspooler-gehosteten Druckkomponenten registriert wurde, das Aufheben der Registrierung.<br/>                                                              |



 

 

 




