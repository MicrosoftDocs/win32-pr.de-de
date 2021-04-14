---
description: Ab Windows Server 2008 und Windows Vista wurde die WinHTTP-API erweitert und umfasst die folgenden Features.
ms.assetid: b47a2e38-67bd-4d43-936c-8781641cb7f6
title: Neuerungen in Windows Server 2008 und Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fac0f274b45e1db79fb79340b7f490de96f57e8f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104484995"
---
# <a name="whats-new-in-windows-server-2008-and-windows-vista"></a>Neues in Windows Server 2008 und Windows Vista

Ab Windows Server 2008 und Windows Vista wurde die WinHTTP-API erweitert und umfasst die folgenden Features.

## <a name="greater-than-4-gb-upload"></a>Mehr als 4 GB hochgeladen.

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) kann aufgrund von Einschränkungen bei der Größe des Parameters "Total Length" von DWORD nur 4 GB Daten senden. Um es Anwendungen zu ermöglichen, mehr als 4 GB an Daten zu senden, wird der Inhalts Längen Header der Anforderung hinzugefügt, wobei Daten als große \_ Ganzzahl (2 ^ 64 Bytes) angegeben werden. Weitere Informationen finden Sie unter **WinHttpSendRequest**. Diese Funktion wird für das [**iwinhttprequest**](iwinhttprequest-interface.md) com-Objekt nicht unterstützt.

## <a name="transfer-encoding-header"></a>Transfer-Encoding-Header

Der Transfer-Encoding-Header ermöglicht es Anwendungen, segmentierte Daten an den Server zu senden. Wenn der Transfer-Encoding-Header in der Anforderung vorhanden ist, sendet die Anwendung die Anforderung mit einem Entitäts Text der Länge 0 (null) im [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest)-Befehl. Der Entitäts Text wird in nachfolgenden Aufrufen von " [**winhttpwrite tedata**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata)" gesendet. Diese Funktion wird für das [**iwinhttprequest**](iwinhttprequest-interface.md) com-Objekt nicht unterstützt.

## <a name="ssl-client-certificate-issuer-list-retrieval"></a>Abruf der Liste der SSL-Client Zertifikat Aussteller

Die Anwendung kann die Liste der Aussteller des SSL-Client Zertifikats abrufen, wenn [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) mit einem Fehler, der **\_ WinHTTP-Client Authentifizierungszertifikat \_ \_ \_ \_ benötigt**, fehlschlägt. Mit der neuen Option **WinHTTP- \_ Option \_ Client Zertifikat- \_ \_ Aussteller \_ Liste** können Anwendungen die Liste der Zertifikat Aussteller abrufen und die Liste nach dem optimalen Zertifikat filtern. Weitere Informationen finden Sie in den Themen zum Abrufen von [**Optionsflags**](option-flags.md) und [zum Abrufen der Ausstellerliste für SSL-Client Authentifizierung](ssl-in-winhttp.md) . Diese Funktion wird für das [**iwinhttprequest**](iwinhttprequest-interface.md) com-Objekt nicht unterstützt.

## <a name="optional-client-certificates"></a>Optionale Client Zertifikate

Wenn [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) einen Fehler erzeugt, bei dem WinHTTP-Client Authentifizierungszertifikat nicht **\_ \_ \_ \_ \_ benötigt** wird, benötigt der Server möglicherweise nicht das SSL-Client Zertifikat. Der Server kann möglicherweise in eine andere Form der Authentifizierung zurückkehren oder den Client den anonymen Zugriff fortsetzen. Die Anwendung legt die **\_ \_ Client \_ CERT- \_ Kontext Option WinHTTP-Option** fest und gibt ein Makro an, das von WinHTTP verwendet wird, um zu bestimmen, ob das Client Zertifikat erforderlich ist. Weitere Informationen finden Sie unter [**Optionsflags**](option-flags.md). Diese Funktion wird für das [**iwinhttprequest**](iwinhttprequest-interface.md) com-Objekt nicht unterstützt.

## <a name="source-and-destination-ip-addresses"></a>Quell-und Ziel-IP-Adressen

Wenn [**WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) abgeschlossen ist, kann die Anwendung die Quell-und Ziel-IP-Adresse und den Port der Anforderung abrufen, die die Antwort generiert hat. Zum Empfangen der Quell-und Zieladressen wird eine neue-Struktur bereitgestellt, wenn die Option " **\_ \_ Verbindungs \_ Informationen" der WinHTTP-Option** festgelegt ist. Weitere Informationen finden Sie unter [**Optionsflags**](option-flags.md). Diese Funktion wird für das [**iwinhttprequest**](iwinhttprequest-interface.md) com-Objekt nicht unterstützt.

## <a name="additional-ssl-client-authentication-errors"></a>Zusätzliche SSL-Client Authentifizierungsfehler

Weitere SSL-Client Authentifizierungsfehler bieten weitere Informationen zum SSL-Client Zertifikat. **Fehler \_ WinHTTP \_ Client \_ CERT \_ No \_ private \_ Key** und **Error \_ WinHTTP \_ CERT \_ No \_ Access \_ private \_ Key** Client Certificate Errors are New in Windows Server 2008 and Windows Vista. Das [**iwinhttprequest**](iwinhttprequest-interface.md) com-Objekt gibt diese Fehler in einem HRESULT zurück.

 

 



