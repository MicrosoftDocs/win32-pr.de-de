---
description: Ab Windows Server 2008 und Windows Vista wurde die WinHTTP-API um die folgenden Features erweitert.
ms.assetid: b47a2e38-67bd-4d43-936c-8781641cb7f6
title: Neues in Windows Server 2008 und Windows Vista
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e474bbfa32d8f82737df4be6f537ca0a6f1bc870e2028d7dcdb1f418adb7120
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120071700"
---
# <a name="whats-new-in-windows-server-2008-and-windows-vista"></a>Neues in Windows Server 2008 und Windows Vista

Ab Windows Server 2008 und Windows Vista wurde die WinHTTP-API um die folgenden Features erweitert.

## <a name="greater-than-4-gb-upload"></a>Mehr als 4 GB Hochladen.

[**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) kann aufgrund von Einschränkungen bei der Größe des DWORD-Parameters für die Gesamtlänge nur 4 GB Daten senden. Damit Anwendungen mehr als 4 GB an Daten senden können, wird der Content-Length-Header der Anforderung hinzugefügt, der Daten so groß wie eine GROßE GANZE ZAHL \_ (2^64 Bytes) angibt. Weitere Informationen finden Sie unter **WinHttpSendRequest**. Dieses Feature wird für das [**COM-Objekt IWinHttpRequest**](iwinhttprequest-interface.md) nicht unterstützt.

## <a name="transfer-encoding-header"></a>Transfer-Encoding Header

Der Transfer-Encoding-Header ermöglicht Es Anwendungen, blockierte Daten an den Server zu senden. Wenn der Transfer-Encoding-Header in der Anforderung vorhanden ist, sendet die Anwendung die Anforderung mit einem Entitätskörper der Länge 0 (null) im Aufruf von [**WinHttpSendRequest.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) Der Entitätskörper wird in nachfolgenden Aufrufen von [**WinHttpWriteData gesendet.**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpwritedata) Dieses Feature wird für das [**COM-Objekt IWinHttpRequest**](iwinhttprequest-interface.md) nicht unterstützt.

## <a name="ssl-client-certificate-issuer-list-retrieval"></a>Abrufen der Liste der SSL-Clientzertifikataussteller

Die Anwendung kann die Ausstellerliste des SSL-Clientzertifikats abrufen, wenn [**WinHttpSendRequest**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) mit dem FEHLER **\_ WINHTTP \_ CLIENT \_ AUTH \_ CERT \_ NEEDED fehlschlägt.** Mit der neuen Option **WINHTTP \_ OPTION CLIENT \_ \_ CERT ISSUER \_ \_ LIST** können Anwendungen die Zertifikatausstellerliste abrufen und die Liste nach dem optimalen Zertifikat filtern. Weitere Informationen finden Sie in den Themen [**Optionsflags**](option-flags.md) und [Ausstellerlistenabruf für die SSL-Clientauthentifizierung.](ssl-in-winhttp.md) Dieses Feature wird für das [**COM-Objekt IWinHttpRequest**](iwinhttprequest-interface.md) nicht unterstützt.

## <a name="optional-client-certificates"></a>Optionale Clientzertifikate

Wenn [**WinHttpSendRequest mit**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpsendrequest) dem FEHLER **\_ WINHTTP CLIENT \_ \_ \_ AUTH CERT \_ NEEDED** fehlschlägt, benötigt der Server möglicherweise nicht das SSL-Clientzertifikat. Der Server kann möglicherweise auf eine andere Form der Authentifizierung zurückverwenden oder dem Client erlauben, mit anonymen Zugriffen fortzufahren. Die Anwendung legt die **OPTION WINHTTP \_ OPTION CLIENT \_ \_ CERT CONTEXT \_ fest** und gibt ein Makro an, mit dem WinHttp bestimmt, ob das Clientzertifikat erforderlich ist. Weitere Informationen finden Sie unter [**Optionsflags**](option-flags.md). Dieses Feature wird für das [**COM-Objekt IWinHttpRequest**](iwinhttprequest-interface.md) nicht unterstützt.

## <a name="source-and-destination-ip-addresses"></a>Quell- und Ziel-IP-Adressen

Nach [**Abschluss von WinHttpReceiveResponse**](/windows/desktop/api/Winhttp/nf-winhttp-winhttpreceiveresponse) kann die Anwendung die Quell- und Ziel-IP-Adresse und den Port der Anforderung abrufen, die die Antwort generiert hat. Eine neue -Struktur wird bereitgestellt, um die Quell- und Zieladressen zu empfangen, wenn die **OPTION WINHTTP \_ OPTION CONNECTION \_ \_ INFO** festgelegt ist. Weitere Informationen finden Sie unter [**Optionsflags**](option-flags.md). Dieses Feature wird für das [**COM-Objekt IWinHttpRequest**](iwinhttprequest-interface.md) nicht unterstützt.

## <a name="additional-ssl-client-authentication-errors"></a>Zusätzliche SSL-Clientauthentifizierungsfehler

Zusätzliche SSL-Clientauthentifizierungsfehler enthalten weitere Informationen zum SSL-Clientzertifikat. **FEHLER \_ WinHTTP \_ CLIENT \_ CERT NO PRIVATE \_ \_ \_ KEY** and **ERROR \_ WINHTTP \_ CERT NO ACCESS PRIVATE \_ \_ \_ \_ KEY** client certificate errors are new for Windows Server 2008 and Windows Vista. Das [**COM-Objekt IWinHttpRequest**](iwinhttprequest-interface.md) gibt diese Fehler in einem HRESULT zurück.

 

 



