---
description: Erfahren Sie mehr über Schnittstellen, die in der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet werden, die vom Druckspooler gehostet werden.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Benachrichtigungsschnittstellen für asynchrones Drucken
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ecfe0de2cf8510b1bb039907067b62fce08a4145
ms.sourcegitcommit: 91530c19d26ba4c57a6af1f37b57f211f580464e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112396095"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Benachrichtigungsschnittstellen für asynchrones Drucken

Die folgenden Schnittstellen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druckspooler gehostet werden, z. B. Druckertreiber und Portmonitore.

## <a name="in-this-section"></a>In diesem Abschnitt



| Schnittstelle                                                                     | Beschreibung                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IPrintAsyncNotifyCallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Erstellt und verwaltet einen Kommunikationskanal, der von Anwendungen und Komponenten verwendet wird, die vom Druckspooler gehostet werden.<br/>                                                                                                                              |
| [**IPrintAsyncNotifyChannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Stellt einen Kommunikationskanal dar, den komponenten, die vom Druckspooler gehostet werden, zum Senden von Benachrichtigungen an Anwendungen verwenden. Wenn der Kanal bidirektional ist, können Anwendungen denselben Kanal verwenden, um Antworten zurück an die Komponente zu senden.<br/> |
| [**IPrintAsyncNotifyDataObject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Kapselt die in einem Benachrichtigungskanal gesendeten Daten. <br/>                                                                                                                                                                                             |



 

 

 




