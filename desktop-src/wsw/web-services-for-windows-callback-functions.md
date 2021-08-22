---
title: Windows Webdienst-Rückruffunktionen
description: Rückrufe ermöglichen einer Anwendung das Aufrufen einer Funktion, die auf einer anderen Ebene oder Ebene definiert ist.
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a78bce5c4023d889748af103148088462cb4b267192b1c0b3845fc735fd1bb5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119926870"
---
# <a name="windows-web-services-callback-functions"></a>Windows Webdienst-Rückruffunktionen

Rückrufe ermöglichen einer Anwendung das Aufrufen einer Funktion, die auf einer anderen Ebene oder Ebene definiert ist. Die Anwendung registriert das Funktionsargument als Handler, der bei Bedarf zu einem späteren Zeitpunkt asynchron aufgerufen werden soll. Der Rückruf wird aufgerufen, wenn die Funktion asynchron abgeschlossen wird, was den Erfolg oder Fehler der Funktion angibt. Der Rückruf wird nicht aufgerufen, wenn der Vorgang synchron abgeschlossen wird.

Die Windows Web Services-API enthält die folgenden Rückruffunktionen:

-   [**WS \_ ABANDON \_ MESSAGE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [**WS \_ ABORT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [**WS \_ ABORT \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**WS \_ ACCEPT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**\_WS-ASYNCHRONER \_ RÜCKRUF**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [**\_WS-ASYNCHRONE \_ FUNKTION**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [**\_BENACHRICHTIGUNGSRÜCKRUF FÜR WS-ZERTIFIKATAUSSTELLERLISTE \_ \_ \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [**WS \_ CERTIFICATE \_ VALIDATION \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [**WS \_ CLOSE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [**WS \_ CLOSE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [**WS \_ CREATE \_ CHANNEL \_ FOR \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**WS \_ CREATE \_ DECODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [**WS \_ CREATE \_ ENCODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [**WS \_ CREATE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**\_ \_ WS-DECODER-DECODIERUNGSRÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [**\_ \_ \_ WS-DECODER-END-RÜCKRUF**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [**\_WS-DECODER \_ : RÜCKRUF \_ DES \_ \_ INHALTSTYPS**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [**\_WS-DECODER– \_ \_ STARTRÜCKRUF**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [**WS \_ DURATION \_ COMPARISON \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**WS \_ DYNAMIC \_ STRING \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**WS \_ \_ ENCODER-CODIERUNGSRÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [**WS \_ ENCODER \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [**WS \_ ENCODER \_ GET \_ CONTENT \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [**WS \_ ENCODER \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [**WS \_ FREE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [**WS \_ FREE \_ DECODER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [**WS \_ FREE \_ \_ ENCODER-RÜCKRUF**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [**WS \_ FREE \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**WS \_ GET \_ CERT \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [**WS \_ GET \_ CHANNEL \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [**WS \_ GET \_ LISTENER \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**\_ \_ WS-HTTP-UMLEITUNGSRÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [**WS \_ IS \_ DEFAULT \_ VALUE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [**WS \_ MESSAGE \_ \_ DONE-RÜCKRUF**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [**WS \_ OPEN \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [**WS \_ OPEN \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**RÜCKRUF ZUM \_ ABBRECHEN DES \_ WS-VORGANGS \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [**RÜCKRUF FÜR \_ DEN FREIEN ZUSTAND DES \_ WS-VORGANGS \_ \_**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [**\_ \_ WS-PROXYNACHRICHTENRÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [**WS \_ PULL \_ BYTES \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**\_ \_ WS-PUSHBYTE-RÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**WS \_ \_ READ-RÜCKRUF**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [**WS \_ READ \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [**WS \_ READ \_ MESSAGE \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [**WS \_ READ \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**WS \_ RESET \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [**WS \_ RESET \_ LISTENER \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**WS \_ SERVICE \_ ACCEPT \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [**WS \_ SERVICE \_ CLOSE \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [**WS \_ SERVICE \_ MESSAGE \_ RECEIVE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**\_ \_ \_ WS-DIENSTSICHERHEITSRÜCKRUF**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [**\_ \_ WS-DIENSTSTUBRÜCKRUF \_**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [**WS \_ SET \_ CHANNEL \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [**WS \_ SET \_ LISTENER \_ PROPERTY \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [**WS \_ SHUTDOWN \_ SESSION \_ CHANNEL \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [**WS \_ VALIDATE \_ PASSWORD \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [**WS \_ VALIDATE \_ SAML \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [**WS \_ WRITE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [**WS \_ WRITE \_ MESSAGE \_ END \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [**WS \_ WRITE \_ MESSAGE \_ START \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [**WS \_ WRITE \_ TYPE \_ CALLBACK**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 




