---
description: Die folgenden Schnittstellen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druck Spooler gehostet werden, z. b. Druckertreiber und Port Monitore.
ms.assetid: e96c957f-3972-4afc-9d76-a4725b8688f8
title: Asynchrone Druck Benachrichtigungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7da8d320b33224e81852542e39f435b45b6dab5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103759558"
---
# <a name="asynchronous-printing-notification-interfaces"></a>Asynchrone Druck Benachrichtigungs Schnittstellen

Die folgenden Schnittstellen werden bei der asynchronen Kommunikation zwischen Anwendungen und Komponenten verwendet, die vom Druck Spooler gehostet werden, z. b. Druckertreiber und Port Monitore.

## <a name="in-this-section"></a>In diesem Abschnitt



| Schnittstelle                                                                     | BESCHREIBUNG                                                                                                                                                                                                                                                   |
|-------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iprintasyncnotifycallback**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifycallback)<br/>     | Erstellt und verwaltet einen Kommunikationskanal, der von Anwendungen und Komponenten verwendet wird, die vom Druck Spooler gehostet werden.<br/>                                                                                                                              |
| [**Iprintasyncnotifychannel**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifychannel)<br/>       | Stellt einen Kommunikationskanal dar, den Komponenten, die vom Druck Spooler gehostet werden, zum Senden von Benachrichtigungen an Anwendungen verwenden. Wenn der Kanal bidirektional ist, können Anwendungen den gleichen Kanal verwenden, um Antworten zurück an die Komponente zu senden.<br/> |
| [**Iprintasyncnotifydataobject**](/windows/desktop/api/prnasnot/nn-prnasnot-iprintasyncnotifydataobject)<br/> | Kapselt die Daten, die in einem Benachrichtigungs Kanal gesendet werden. <br/>                                                                                                                                                                                             |



 

 

 




