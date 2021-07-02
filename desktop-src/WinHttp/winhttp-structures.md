---
description: In diesem Thema werden die Von WinHTTP verwendeten Strukturen identifiziert.
ms.assetid: e1567393-162e-48d4-8e6b-7620e351136c
title: WinHTTP-Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7ecf91702a2f49e2c0a754fcc69d9d34febf229
ms.sourcegitcommit: 8e3d8594fa073a9c43eb5dcc7babea03ea30f10f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/01/2021
ms.locfileid: "113174985"
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

Enthält die Bestandteile einer URL. Diese Struktur wird mit den [**Funktionen WinHttpCrackUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcrackurl) und [**WinHttpCreateUrl**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpcreateurl) verwendet.

</dd> <dt>

[**WINHTTP_ASYNC_RESULT**](/windows/win32/api/winhttp/ns-winhttp-winhttp_async_result)
</dt> <dd>

Enthält das Ergebnis eines Aufrufs einer asynchronen Funktion. Diese Struktur wird mit dem [**WINHTTP_STATUS_CALLBACK**](/windows/win32/api/winhttp/nc-winhttp-winhttp_status_callback) verwendet.

</dd> <dt>

[**WINHTTP_AUTOPROXY_OPTIONS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_autoproxy_options)
</dt> <dd>

Wird verwendet, um der [**WinHttpGetProxyForURL-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyforurl) anzugeben, ob die URL der PAC-Datei (Proxy Auto-Configuration) angegeben oder die URL mit DHCP- oder DNS-Abfragen an das Netzwerk automatisch gefunden werden soll.

</dd> <dt>

[**WINHTTP_CERTIFICATE_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_certificate_info)
</dt> <dd>

Enthält zertifikatsinformationen, die vom Server zurückgegeben werden. Diese Struktur wird von der [**WinHttpQueryOption-Funktion**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpqueryoption) verwendet.

</dd> <dt>

[**WINHTTP_CONNECTION_GROUP**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_connection_group)
</dt> <dd>

Stellt eine Verbindungsgruppe dar.

</dd> <dt>

[**WINHTTP_CONNECTION_INFO**](/windows/desktop/api/Winhttp/ns-winhttp-winhttp_connection_info)
</dt> <dd>

Enthält die Quell- und Ziel-IP-Adresse der Anforderung, die die Antwort generiert hat.

</dd> <dt>

[**WINHTTP_CREDS**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds)
</dt> <dd>

Enthält Informationen zu Benutzer-Anmeldeinformationen, die für die Server- und Proxyauthentifizierung verwendet werden.

> [!Note]
> Diese Struktur ist veraltet. Stattdessen wird die Verwendung [**der**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex) WINHTTP_CREDS_EX empfohlen.

</dd> <dt>

[**WINHTTP_CREDS_EX**](/windows/win32/api/winhttp/ns-winhttp-winhttp_creds_ex)
</dt> <dd>

Enthält Informationen zu Benutzer-Anmeldeinformationen, die für die Server- und Proxyauthentifizierung verwendet werden.

</dd> <dt>

[**WINHTTP_CURRENT_USER_IE_PROXY_CONFIG**](/windows/win32/api/winhttp/ns-winhttp-winhttp_current_user_ie_proxy_config)
</dt> <dd>

Enthält die Internet Explorer Proxykonfigurationsinformationen.

</dd> <dt>

[**WINHTTP_EXTENDED_HEADER**](/windows/win32/api/winhttp/ns-winhttp-winhttp_extended_header)
</dt> <dd>

Stellt einen HTTP-Anforderungsheader als Name-Wert-Zeichenfolgenpaar dar.

</dd> <dt>

[**WINHTTP_HEADER_NAME**](/windows/win32/api/winhttp/ns-winhttp-winhttp_header_name)
</dt> <dd>

Stellt einen HTTP-Anforderungsheadernamen dar.

</dd> <dt>

[**WINHTTP_HOST_CONNECTION_GROUP**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_host_connection_group)
</dt> <dd>

Stellt eine Auflistung von Verbindungsgruppen dar.

</dd> <dt>

[**WINHTTP_MATCH_CONNECTION_GUID**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_match_connection_group)
</dt> <dd>

Stellt die GUID einer Verbindung für den Verbindungsabgleich dar.

</dd> <dt>

[**WINHTTP_PROXY_INFO**](/windows/win32/api/winhttp/ns-winhttp-winhttp_proxy_info)
</dt> <dd>

Enthält die Sitzungs- oder Standardproxykonfiguration.

</dd> <dt>

[**WINHTTP_PROXY_RESULT**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result)
</dt> <dd>

Eine Auflistung von Proxyergebniseinträgen, die von [**WinHttpGetProxyResult bereitgestellt werden.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)

</dd> <dt>

[**WINHTTP_PROXY_RESULT_ENTRY**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_proxy_result_entry)
</dt> <dd>

Ein Ergebniseintrag aus einem Aufruf von [**WinHttpGetProxyResult.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpgetproxyresult)

</dd> <dt>

[**WINHTTP_QUERY_CONNECTION_GROUP_RESULT**](/windows/win32/api/Winhttp/ns-winhttp-winhttp_query_connection_group_result)
</dt> <dd>

Stellt eine Beschreibung des aktuellen Zustands der WinHttp-Verbindungen dar.

</dd> <dt>

[**WINHTTP_REQUEST_STATS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_stats)
</dt> <dd>

Enthält Statistiken für eine Anforderung.

</dd> <dt>

[**WINHTTP_REQUEST_TIMES**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_request_times)
</dt> <dd>

Enthält Zeitsteuerungsinformationen für eine Anforderung.

</dd> <dt>

[**WINHTTP_SECURITY_INFO**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_security_info)
</dt> <dd>

Enthält SChannel-Verbindungs- und Verschlüsselungsinformationen für eine Anforderung.

</dd> <dt>

[**WINHTTP_WEB_SOCKET_ASYNC_RESULT**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_async_result)
</dt> <dd>

Ergebnisstatus eines WebSocket-Vorgangs.

</dd> <dt>

[**WINHTTP_WEB_SOCKET_STATUS**](/windows/desktop/api/winhttp/ns-winhttp-winhttp_web_socket_status)
</dt> <dd>

Status eines WebSocket-Vorgangs.

</dd> </dl>
