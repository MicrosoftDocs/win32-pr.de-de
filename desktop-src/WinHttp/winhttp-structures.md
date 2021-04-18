---
description: In diesem Thema werden die Strukturen beschrieben, die von WinHTTP verwendet werden.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: WinHTTP-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5f09615e721b9d34243bd20074e83837e48a6803
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214610"
---
# <a name="winhttp-structures"></a>WinHTTP-Strukturen

WinHTTP verwendet die folgenden Strukturen:

<dl> <dt>

[**HTTP_VERSION_INFO**](/windows/win32/api/winhttp/ns-winhttp-http_version_info)
</dt> <dd>

Enthält die globale HTTP-Version.

</dd> <dt>

[**URL_COMPONENTS**](/windows/win32/api/winhttp/ns-winhttp-url_components)
</dt> <dd>

Enthält die Bestandteile einer URL. Diese Struktur wird mit den Funktionen [**winhttpknackurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) und [**winhttpkreateurl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) verwendet.

</dd> <dt>

[**WINHTTP_ASYNC_RESULT**](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

Enthält das Ergebnis eines Aufrufes einer asynchronen Funktion. Diese Struktur wird mit dem [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) Prototyp verwendet.

</dd> <dt>

[**WINHTTP_AUTOPROXY_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

Wird verwendet, um der [**WinHttpGetProxyForUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) -Funktion anzugeben, ob die URL der PAC-Datei (Proxy Auto-Configuration) angegeben werden soll oder ob die URL mit DHCP-oder DNS-Abfragen automatisch im Netzwerk gefunden werden soll.

</dd> <dt>

[**WINHTTP_CERTIFICATE_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

Enthält Zertifikat Informationen, die vom Server zurückgegeben werden. Diese Struktur wird von der [**WinHttpQueryOption**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) -Funktion verwendet.

</dd> <dt>

[**WINHTTP_CONNECTION_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

Enthält die Quell-und Ziel-IP-Adresse der Anforderung, die die Antwort generiert hat.

</dd> <dt>

[**WINHTTP_CREDS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

Enthält Benutzer Anmelde Informationen, die für die Server-und Proxy Authentifizierung verwendet werden.

> [!Note]
> Diese Struktur ist veraltet. Stattdessen wird die Verwendung der [**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) Struktur empfohlen.

</dd> <dt>

[**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

Enthält Benutzer Anmelde Informationen, die für die Server-und Proxy Authentifizierung verwendet werden.

</dd> <dt>

[**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

Enthält die Internet Explorer-Proxy Konfigurationsinformationen.

</dd> <dt>

[**WINHTTP_PROXY_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

Enthält die Sitzungs-oder Standard Proxykonfiguration.

</dd> <dt>

[**WINHTTP_PROXY_RESULT**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

Eine Auflistung von Proxy Ergebnis Einträgen, die von [**winhttpgetproxyresult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)bereitgestellt werden.

</dd> <dt>

[**WINHTTP_PROXY_RESULT_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

Ein Ergebniseintrag aus einem Aufrufen von [**winhttpgetproxyresult**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult).

</dd> <dt>

[**WINHTTP_REQUEST_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

Enthält Statistiken für eine Anforderung.

</dd> <dt>

[**WINHTTP_REQUEST_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

Enthält Zeit Steuerungsinformationen für eine Anforderung.

</dd> <dt>

[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

Enthält SChannel-Verbindung und Chiffre Informationen für eine Anforderung.

</dd> <dt>

[**WINHTTP_WEB_SOCKET_ASYNC_RESULT**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

Ergebnis Status eines WebSocket-Vorgangs.

</dd> <dt>

[**WINHTTP_WEB_SOCKET_STATUS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

Status eines WebSocket-Vorgangs.

</dd> </dl>
