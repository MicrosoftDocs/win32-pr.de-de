---
description: Die folgenden Schnittstellen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druck Spooler gehostet werden, z. b. Druckertreiber und Port Monitore.
ms.assetid: 7e98e63f-616c-4cd1-a8aa-482d27529b8c
title: Asynchrone Druck Benachrichtigungsfunktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72fa7b0b61de15af9f7117e7c36104eb51abbb7c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106369033"
---
# <a name="asynchronous-printing-notification-functions"></a>Asynchrone Druck Benachrichtigungsfunktionen

Die folgenden Schnittstellen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druck Spooler gehostet werden, z. b. Druckertreiber und Port Monitore.

## <a name="in-this-section"></a>In diesem Abschnitt



| Funktion                                                                                        | BESCHREIBUNG                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**"Kreateprintasyncnotifychannel"**](/windows/desktop/api/prnasnot/nf-prnasnot-createprintasyncnotifychannel)<br/>               | Erstellt einen Kommunikationskanal zwischen einer Druckerspooler-gehosteten Druckkomponente, z. b. einem Druckertreiber oder Port Monitor, und einer Anwendung, die Benachrichtigungen von der Komponente empfängt.<br/> |
| [**Registerforprintasyncbenachrichtigungen**](/windows/desktop/api/prnasnot/nf-prnasnot-registerforprintasyncnotifications)<br/>     | Ermöglicht einer Anwendung das Registrieren für Benachrichtigungen von Druckerspooler-gehosteten Druckkomponenten wie Druckertreibern, Druck Prozessoren und Port Monitoren.<br/>                              |
| [**Unregisterforprintasyncnotification**](/windows/desktop/api/prnasnot/nf-prnasnot-unregisterforprintasyncnotifications)<br/> | Ermöglicht es einer Anwendung, die registriert hat, Benachrichtigungen von Druckkomponenten des Druck Spoolers zu empfangen, um die Registrierung aufzuheben.<br/>                                                              |



 

 

 




