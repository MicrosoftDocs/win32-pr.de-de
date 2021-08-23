---
description: Erfahren Sie mehr über Schnittstellen, die bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet werden, die vom Druckspooler gehostet werden.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Schnittstellen für asynchrone Druckbenachrichtigungen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 357610b30d01b89ed8fd7e2fe7354f727a44c8f04b41d71d846af622113aa435
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119720220"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Schnittstellen für asynchrone Druckbenachrichtigungen

Die folgenden Schnittstellen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druckspooler gehostet werden, z. B. Druckertreiber und Portmonitore.

## <a name="in-this-section"></a>In diesem Abschnitt



| Schnittstelle                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Erstellt und verwaltet einen Kommunikationskanal, der von Anwendungen und Komponenten verwendet wird, die vom Druckspooler gehostet werden.<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Stellt einen Kommunikationskanal dar, den komponenten, die vom Druckspooler gehostet werden, zum Senden von Benachrichtigungen an Anwendungen verwenden. Wenn der Kanal bidirektional ist, können Anwendungen denselben Kanal verwenden, um Antworten zurück an die Komponente zu senden.<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Kapselt die in einem Benachrichtigungskanal gesendeten Daten. <br/>                                                                                                                                                                                             |



 

 

 




