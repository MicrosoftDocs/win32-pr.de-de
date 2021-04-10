---
title: Rückruf Funktionen für Windows-Webdienste
description: Rückrufe ermöglichen einer Anwendung, eine Funktion aufzurufen, die auf einer anderen Ebene oder Ebene definiert ist.
ms.assetid: 7398ec42-388a-494c-9fe4-5bd62aa009cb
keywords:
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a385ca21d00e8845f89bda0d9b04221a922ba421
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104100622"
---
# <a name="windows-web-services-callback-functions"></a>Rückruf Funktionen für Windows-Webdienste

Rückrufe ermöglichen einer Anwendung, eine Funktion aufzurufen, die auf einer anderen Ebene oder Ebene definiert ist. Die Anwendung registriert das Funktions Argument als Handler, der zu einem späteren Zeitpunkt nach Bedarf asynchron aufgerufen werden soll. Der Rückruf wird aufgerufen, wenn die Funktion asynchron mit der Funktion Erfolg oder Fehler abgeschlossen wird. Der Rückruf wird nicht aufgerufen, wenn der Vorgang synchron abgeschlossen wird.

Die Windows-Webdienste-API umfasst die folgenden Rückruf Funktionen:

-   [**WS-Abbruch \_ \_ Nachrichten \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_abandon_message_callback)
-   [**WS- \_ Abbruch \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_channel_callback)
-   [**WS- \_ Abbruch- \_ Listener- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_abort_listener_callback)
-   [**WS \_ Accept \_ Channel- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_accept_channel_callback)
-   [**WS \_ Async- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_async_callback)
-   [**WS \_ Async- \_ Funktion**](/windows/desktop/api/WebServices/nc-webservices-ws_async_function)
-   [**\_ \_ \_ \_ Benachrichtigungs Rückruf für WS CERT-Ausstellerliste \_**](/windows/desktop/api/WebServices/nc-webservices-ws_cert_issuer_list_notification_callback)
-   [**WS- \_ Zertifikats \_ Validierungs \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_certificate_validation_callback)
-   [**WS- \_ Schluss \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_close_channel_callback)
-   [**WS \_ Close \_ Listener \_ Callback**](/windows/desktop/api/WebServices/nc-webservices-ws_close_listener_callback)
-   [**WS \_ Create \_ Channel- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_callback)
-   [**WS \_ Create \_ Channel \_ für \_ \_ listenerrückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_create_channel_for_listener_callback)
-   [**WS-Erstellungs \_ \_ Decoder- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_create_decoder_callback)
-   [**WS \_ - \_ \_ codierungsrückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_create_encoder_callback)
-   [**WS \_ Create \_ Listener- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_create_listener_callback)
-   [**WS \_ - \_ decoderdecodierungsrückruf \_**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_decode_callback)
-   [**WS \_ - \_ decoderende- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_end_callback)
-   [**WS- \_ Decoder \_ get- \_ \_ Inhaltstyp \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_get_content_type_callback)
-   [**WS \_ - \_ decoderstart \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_decoder_start_callback)
-   [**WS \_ Duration- \_ Vergleichs \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_duration_comparison_callback)
-   [**WS- \_ dynamischer \_ Zeichen folgen \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_dynamic_string_callback)
-   [**WS- \_ Encoder-Codierungs \_ \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_encode_callback)
-   [**WS- \_ Encoder- \_ End- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_end_callback)
-   [**WS- \_ Encoder \_ get- \_ \_ Inhaltstyp \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_get_content_type_callback)
-   [**WS- \_ Encoder- \_ Start \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_encoder_start_callback)
-   [**WS \_ - \_ freier \_ channelrückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_free_channel_callback)
-   [**WS- \_ freier \_ Decoder- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_free_decoder_callback)
-   [**WS \_ Free \_ Encoder- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_free_encoder_callback)
-   [**WS- \_ freier \_ Listener- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_free_listener_callback)
-   [**WS \_ get \_ CERT- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_get_cert_callback)
-   [**Rückruf für WS- \_ get- \_ Kanal \_ Eigenschaft \_**](/windows/desktop/api/WebServices/nc-webservices-ws_get_channel_property_callback)
-   [**WS \_ get \_ Listener- \_ Eigenschaften \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_get_listener_property_callback)
-   [**WS- \_ http- \_ Umleitungs \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_http_redirect_callback)
-   [**WS \_ ist der \_ Standard \_ Wert \_ Rückruf.**](/windows/desktop/api/WebServices/nc-webservices-ws_is_default_value_callback)
-   [**Rückruf für WS- \_ Nachricht \_ abgeschlossen \_**](/windows/desktop/api/WebServices/nc-webservices-ws_message_done_callback)
-   [**WS- \_ Open- \_ Channel- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_open_channel_callback)
-   [**WS \_ Open \_ Listener- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_open_listener_callback)
-   [**WS- \_ Vorgang \_ Abbruch \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_cancel_callback)
-   [**WS- \_ Vorgang, \_ freier \_ Zustands \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_operation_free_state_callback)
-   [**WS- \_ Proxy \_ Nachrichten \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_proxy_message_callback)
-   [**WS- \_ Pull- \_ Bytes- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_pull_bytes_callback)
-   [**WS- \_ Push- \_ Bytes- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_push_bytes_callback)
-   [**WS- \_ Lese \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_read_callback)
-   [**WS- \_ Lese \_ Nachrichten Ende- \_ \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_end_callback)
-   [**WS \_ - \_ lesenachrichten- \_ Start \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_read_message_start_callback)
-   [**WS \_ - \_ Lesetyp \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_read_type_callback)
-   [**WS-rücksetzungs \_ \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_channel_callback)
-   [**WS-rücksetzungs \_ \_ \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_reset_listener_callback)
-   [**WS- \_ Dienst \_ Annahme- \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_accept_channel_callback)
-   [**WS- \_ Dienst- \_ Schluss \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_close_channel_callback)
-   [**WS- \_ Dienst- \_ Nachrichten \_ Empfangs \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_message_receive_callback)
-   [**WS- \_ Dienst- \_ Sicherheits \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_security_callback)
-   [**WS- \_ Dienst- \_ Stub- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_service_stub_callback)
-   [**Rückruf für die WS- \_ Satz \_ Kanal \_ Eigenschaft \_**](/windows/desktop/api/WebServices/nc-webservices-ws_set_channel_property_callback)
-   [**WS- \_ Satz \_ Listener- \_ Eigenschaften \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_set_listener_property_callback)
-   [**WS \_ - \_ Sitzungs \_ Kanal \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_shutdown_session_channel_callback)
-   [**WS \_ Validate \_ password \_ Callback**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_password_callback)
-   [**WS-Überprüfungs- \_ \_ SAML- \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_validate_saml_callback)
-   [**WS- \_ Schreib \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_write_callback)
-   [**WS- \_ Write- \_ Nachrichten Ende- \_ \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_end_callback)
-   [**WS- \_ Schreib \_ Nachrichten Start- \_ \_ Rückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_write_message_start_callback)
-   [**WS \_ - \_ Schreib \_ typrückruf**](/windows/desktop/api/WebServices/nc-webservices-ws_write_type_callback)

 

 




