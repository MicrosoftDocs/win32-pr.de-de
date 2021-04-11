---
title: Dienstautorisierung
description: Eine Anwendung kann eine benutzerdefinierte Autorisierung für eingehende Nachrichten auf einem Dienst Host implementieren.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Dienst Autorisierungs-Webdienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c296dc6b4900bd20df7d1e70631e758599a0028d
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104102558"
---
# <a name="service-authorization"></a>Dienstautorisierung

Eine Anwendung kann eine benutzerdefinierte Autorisierung für eingehende Nachrichten auf einem Dienst Host implementieren.


Ein Dienst Host empfängt einen Sicherheits Rückruf- [**WS- \_ Dienst- \_ Sicherheits \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) als Teil des [**WS- \_ Dienst \_ Endpunkts**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) , der an die [**wscreateservicehost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) -Funktion übergeben wird. Dieser Rückruf wird aufgerufen, wenn die [WS- \_ Nachricht](ws-message.md) empfangen wird.

Die Anwendung kann sich auf diesen Rückruf stützen, um eine benutzerdefinierte Autorisierung für eingehende Nachrichten auf dem Dienst Host zu implementieren. Wenn die Autorisierung fehlschlägt, gibt die Sicherheits Rückruffunktion einen Fehler HR zurück, und der Dienst Host bricht den Channel ab.

Eine Beispiel Implementierung finden Sie unter Beispiel für Benutzername über SSL, [httpcalculatorwithusernameoversslserviceexample](httpcalculatorwithusernameoversslserviceexample.md).

 

 




