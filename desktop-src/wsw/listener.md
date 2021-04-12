---
title: Listener
description: Ein Listener wird vom Client verwendet, um einen eingehenden Kanal von einem Dienst zu akzeptieren.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Listenerweb Dienste für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e372f3fa9109647e009f0258c059cc4c2065f6bc
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/04/2020
ms.locfileid: "104391247"
---
# <a name="listener"></a>Listener

Ein Listener wird vom Client verwendet, um einen eingehenden [Kanal](channel.md) von einem Dienst zu akzeptieren.

Zum Erstellen eines listners geben Sie den Kanaltyp als Enumerationswert für den [**WS- \_ \_ Kanaltyp**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) , die [Bindungs](binding.md) Informationen und die zu überwachende [URL](url.md) an.


Um mit dem lauschen an der URL zu beginnen, müssen Sie die [**wsopenlistener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) -Funktion aufzurufen.

Um eingehende Verbindungen zu akzeptieren, wenden Sie [**wsaccept-Channel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)an.

Zum Abbrechen ausstehender e/a-Vorgänge für einen Listener rufen Sie [**wsabortlistener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)auf.

Informationen zu den Status Übergängen für einen Listener finden Sie in der [**WS-listenerstatusenumeration \_ \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state) .

Die folgenden Rückrufe sind Teil des-Listener:

-   [**WS- \_ Abbruch- \_ Listener- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**WS \_ Accept \_ Channel- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**WS \_ Close \_ Listener \_ Callback**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ Create \_ Channel \_ für \_ \_ listenerrückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**WS \_ Create \_ Listener- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**WS- \_ freier \_ Listener- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**WS \_ get \_ Listener- \_ Eigenschaften \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**WS \_ Open \_ Listener- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**WS-rücksetzungs \_ \_ \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**WS- \_ Satz \_ Listener- \_ Eigenschaften \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

Die folgenden Enumerationen sind Teil des-Listener:

-   [**WS \_ -IP- \_ Version**](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [**WS- \_ Listener- \_ Eigenschaften- \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [**WS \_ - \_ listenerstatus**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

Die folgenden Funktionen sind Teil des-Listener:

-   [**Wsabortlistener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [**Wsakzeptchannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [**Wscloselistener**](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [**Wscreatelistener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [**Wsfreelistener**](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [**Wsgetlistenerproperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [**Wsopumlistener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [**Wsresetlistener**](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [**Wssetlistenerproperty**](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

Das folgende Handle ist Teil des-Listener:

-   [WS- \_ Listener](ws-listener.md)

Die folgenden Strukturen sind Teil des-Listener:

-   [**WS \_ Custom \_ Listener \_ -Rückrufe**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [**nicht zulässige WS-Teil Zeichenfolgen des \_ \_ Benutzer- \_ Agents \_**](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [**WS \_ - \_ Hostnamen**](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [**WS \_ - \_ Listenereigenschaften**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [**WS \_ - \_ Listenereigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




