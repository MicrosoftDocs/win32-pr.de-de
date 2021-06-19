---
description: Erfahren Sie mehr über Funktionen, die in der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet werden, die vom Druckspooler gehostet werden.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Benachrichtigungsfunktionen für asynchrones Drucken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdc9a404d1675c8ee87be31c7c57dd14a370697c
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112394855"
---
# <a name="asynchronous-printing-notification-functions"></a>Benachrichtigungsfunktionen für asynchrones Drucken

Die folgenden Funktionen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druckspooler gehostet werden, z. B. Druckertreiber und Portmonitore.

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion                                                                                        | Beschreibung                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CreatePrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | Erstellt einen Kommunikationskanal zwischen einer druckspoolergehosteten Druckkomponente, z. B. einem Druckertreiber oder Portmonitor, und einer Anwendung, die Benachrichtigungen von der Komponente empfängt.<br/> |
| [**RegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | Ermöglicht es einer Anwendung, sich für Benachrichtigungen von druckspoolergehosteten Druckkomponenten wie Druckertreibern, Druckprozessoren und Portmonitoren zu registrieren.<br/>                              |
| [**UnRegisterForPrintAsyncNotifications**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | Aktiviert eine Anwendung, die registriert wurde, um Benachrichtigungen von druckspoolergehosteten Druckkomponenten zu empfangen, um die Registrierung zu aufheben.<br/>                                                              |



 

 

 




