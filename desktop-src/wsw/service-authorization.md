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
# <a name="service-authorization"></a><span data-ttu-id="179a3-106">Dienstautorisierung</span><span class="sxs-lookup"><span data-stu-id="179a3-106">Service Authorization</span></span>

<span data-ttu-id="179a3-107">Eine Anwendung kann eine benutzerdefinierte Autorisierung für eingehende Nachrichten auf einem Dienst Host implementieren.</span><span class="sxs-lookup"><span data-stu-id="179a3-107">An application can implement custom authorization for incoming messages on a service host .</span></span>


<span data-ttu-id="179a3-108">Ein Dienst Host empfängt einen Sicherheits Rückruf- [**WS- \_ Dienst- \_ Sicherheits \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) als Teil des [**WS- \_ Dienst \_ Endpunkts**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) , der an die [**wscreateservicehost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) -Funktion übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="179a3-108">A service host receives a security callback [**WS\_SERVICE\_SECURITY\_CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback) as part of the [**WS\_SERVICE\_ENDPOINT**](/windows/desktop/api/WebServices/ns-webservices-ws_service_endpoint) which is passed to the [**WsCreateServiceHost**](/windows/desktop/api/WebServices/nf-webservices-wscreateservicehost) function.</span></span> <span data-ttu-id="179a3-109">Dieser Rückruf wird aufgerufen, wenn die [WS- \_ Nachricht](ws-message.md) empfangen wird.</span><span class="sxs-lookup"><span data-stu-id="179a3-109">This callback is invoked when the [WS\_MESSAGE](ws-message.md) is received.</span></span>

<span data-ttu-id="179a3-110">Die Anwendung kann sich auf diesen Rückruf stützen, um eine benutzerdefinierte Autorisierung für eingehende Nachrichten auf dem Dienst Host zu implementieren.</span><span class="sxs-lookup"><span data-stu-id="179a3-110">The application can rely on this callback to implement custom authorization for incoming messages on the service host.</span></span> <span data-ttu-id="179a3-111">Wenn die Autorisierung fehlschlägt, gibt die Sicherheits Rückruffunktion einen Fehler HR zurück, und der Dienst Host bricht den Channel ab.</span><span class="sxs-lookup"><span data-stu-id="179a3-111">If the authorization fails the security callback function returns a failure HR, and the service host aborts the channel.</span></span>

<span data-ttu-id="179a3-112">Eine Beispiel Implementierung finden Sie unter Beispiel für Benutzername über SSL, [httpcalculatorwithusernameoversslserviceexample](httpcalculatorwithusernameoversslserviceexample.md).</span><span class="sxs-lookup"><span data-stu-id="179a3-112">See the user name over SSL example, [HttpCalculatorWithUserNameOverSslServiceExample](httpcalculatorwithusernameoversslserviceexample.md), for an example implementation.</span></span>

 

 




