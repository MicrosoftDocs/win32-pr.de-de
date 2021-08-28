---
title: Dienstautorisierung
description: Eine Anwendung kann eine benutzerdefinierte Autorisierung für eingehende Nachrichten auf einem Diensthost implementieren.
ms.assetid: 75bcf051-3983-48fc-8121-0984ac9cdcb9
keywords:
- Webdienste zur Dienstautorisierung für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b84b9947d088d5f594ac11f0ee83cc03925f8a3bbc9aeceae0bc7d5cb120477
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120109840"
---
# <a name="service-authorization"></a>Dienstautorisierung

Eine Anwendung kann eine benutzerdefinierte Autorisierung für eingehende Nachrichten auf einem Diensthost implementieren.


Ein Diensthost empfängt einen Sicherheitsrückruf [**WS \_ SERVICE SECURITY \_ \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) als Teil des [**\_ WS-DIENSTENDPUNKTs, \_**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) der an die [**WsCreateServiceHost-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) übergeben wird. Dieser Rückruf wird aufgerufen, wenn die [WS \_ MESSAGE](ws-message.md) empfangen wird.

Die Anwendung kann sich auf diesen Rückruf verlassen, um eine benutzerdefinierte Autorisierung für eingehende Nachrichten auf dem Diensthost zu implementieren. Wenn bei der Autorisierung ein Fehler auftritt, gibt die Sicherheitsrückruffunktion einen Hr-Fehler zurück, und der Diensthost bricht den Kanal ab.

Eine Beispielimplementierungen finden Sie im Beispiel benutzername über SSL, [HttpCalculatorWithUserNameOverSslServiceExample.](httpcalculatorwithusernameoversslserviceexample.md)

 

 




