---
title: Listener
description: Ein Listener wird vom Client verwendet, um einen eingehenden Kanal von einem Dienst zu akzeptieren.
ms.assetid: fffda587-23f5-4c7a-93c5-f03d9d3fafb2
keywords:
- Listenerwebdienste für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26a2f9951dedefd5fb686de7935a76ce3b6ef24dcea140d5414b713e89ad1f1d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026378"
---
# <a name="listener"></a>Listener

Ein Listener wird vom Client verwendet, um einen eingehenden Kanal [von](channel.md) einem Dienst zu akzeptieren.

Um einen Listner zu erstellen, geben Sie den Kanaltyp [](binding.md) als [**WS \_ CHANNEL \_ TYPE-Enumerationswert,**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_type) die Bindungsinformationen und die [URL](url.md) an, die lauschen soll.


Um mit dem Lauschen auf die URL zu beginnen, rufen Sie [**die WsOpenListener-Funktion**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener) auf.

Um eingehende Kommunikationen zu akzeptieren, rufen [**Sie WsAcceptChannel auf.**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)

Um ausstehende E/A für einen Listener abzubruchen, rufen [**Sie WsAbortListener auf.**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)

Informationen zu den Zustandsübergängen für einen Listener finden Sie unter [**der WS \_ LISTENER \_ STATE-Enumeration.**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

Die folgenden Rückrufe sind Teil des Listeners:

-   [**WS \_ ABORT \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**WS \_ ACCEPT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**WS \_ CLOSE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ FOR \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**WS \_ CREATE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**WS \_ FREE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**WS \_ GET \_ LISTENER \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**WS \_ OPEN \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**WS \_ RESET \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**WS \_ SET \_ LISTENER \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)

Die folgenden Enumerationen sind Teil des Listeners:

-   [**\_WS-IP-VERSION \_**](/windows/desktop/api/WebServices/ne-webservices-ws_ip_version)
-   [**\_ \_ WS-LISTENER-EIGENSCHAFTEN-ID \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_property_id)
-   [**\_WS-LISTENERZUSTAND \_**](/windows/desktop/api/WebServices/ne-webservices-ws_listener_state)

Die folgenden Funktionen sind Teil des Listeners:

-   [**WsAbortListener**](/windows/desktop/api/WebServices/nf-webservices-wsabortlistener)
-   [**WsAcceptChannel**](/windows/desktop/api/WebServices/nf-webservices-wsacceptchannel)
-   [**WsCloseListener**](/windows/desktop/api/WebServices/nf-webservices-wscloselistener)
-   [**WsCreateListener**](/windows/desktop/api/WebServices/nf-webservices-wscreatelistener)
-   [**WsFreeListener**](/windows/desktop/api/WebServices/nf-webservices-wsfreelistener)
-   [**WsGetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wsgetlistenerproperty)
-   [**WsOpenListener**](/windows/desktop/api/WebServices/nf-webservices-wsopenlistener)
-   [**WsResetListener**](/windows/desktop/api/WebServices/nf-webservices-wsresetlistener)
-   [**WsSetListenerProperty**](/windows/desktop/api/WebServices/nf-webservices-wssetlistenerproperty)

Das folgende Handle ist Teil des Listeners:

-   [\_WS-LISTENER](ws-listener.md)

Die folgenden Strukturen sind Teil des Listeners:

-   [**BENUTZERDEFINIERTE \_ \_ WS-LISTENERRÜCKRUFE \_**](/windows/desktop/api/WebServices/ns-webservices-ws_custom_listener_callbacks)
-   [**\_WS: UNTERGEORDNETE \_ ZEICHENFOLGEN DES \_ BENUTZER-AGENTS \_ NICHT VERFÜGBAR**](/windows/desktop/api/WebServices/ns-webservices-ws_disallowed_user_agent_substrings)
-   [**\_WS-HOSTNAMEN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_host_names)
-   [**\_WS-LISTENEREIGENSCHAFTEN \_**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_properties)
-   [**\_ \_ WS-LISTENER-EIGENSCHAFT**](/windows/desktop/api/WebServices/ns-webservices-ws_listener_property)

 

 




