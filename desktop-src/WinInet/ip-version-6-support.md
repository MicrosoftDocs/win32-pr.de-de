---
title: Unterstützung für IP-Version 6
description: Ab IE7 und höher unterstützt WinINet IPv6-Literale im Hostnamen und die Autoritätskomponente des URI.
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- Unterstützung für IP-Version 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a024c792995780769a078c84b0493b7abba8647189fa2cee835d93dcb83770
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118113630"
---
# <a name="ip-version-6-support"></a>Unterstützung für IP-Version 6

Ab IE7 und höher unterstützt WinINet IPv6-Literale im Hostnamen und die Autoritätskomponente des URI. WinINet unterstützt auch die Verwendung von IPv6-Literalen in relevanten Teilen des HTTP-Protokolls, z. B. im Location-Header.

## <a name="hostname-ipv6-literals-and-uri-components"></a>Hostname IPv6-Literale und URI-Komponenten

WinINet implementiert IPv6-Literale gemäß den Spezifikationen in RFC 3513. Wie in diesem RFC angegeben, müssen IPv6-Literale in einem URI in Klammern eingeschlossen werden. Beispielsweise ist https:// ::1 / ein gültiger \[ \] IPv6-URI. Das Formular ohne eckige Klammern ( https://::1/) ist ungültig. Hostname-IPv6-Literale, die nicht Teil des URI sind, müssen jedoch nicht in die Klammern eingeschlossen werden. beide Formen sind für WinINet akzeptabel. Beispielsweise sind sowohl "::1" als auch " ::1 " zulässige Formen von \[ \] IPv6-Hostnamenliteralen. Andere APIs, z. B. die WinSock-API, akzeptieren ebenfalls beide Formulare. Daher sollten Anwendungen darauf vorbereitet sein, beide Formen von IPv6-Hostnamenliteralen zu verarbeiten.

## <a name="scope-id"></a>Bereichs-ID

Die IPv6-Literaladresse im URI kann eine Bereichs-ID enthalten. Eine Bereichs-ID kann eine Schnittstellen-ID wie \[ FE80::1%1 \] sein. Der in RFC 3986 dokumentierte URI-Standard definiert nicht die Syntax für die Bereichs-ID, und der URI wird als nicht einheitlich betrachtet, wenn die Bereichs-ID vorhanden ist. WinINet akzeptiert jedoch eine Bereichs-ID in der Autoritätskomponente des URI und im IPv6-Literal des Hostnamens.

Das Prozentzeichen (%) in der IPv6-Literaladresse muss als Prozentzeichen mit Escapezeichen verwendet werden, wenn es im URI vorhanden ist. Beispielsweise muss die Bereichs-ID FE80::2%3 im URI als "https:// \[ FE80::2%253 /" angezeigt werden, wobei %25 das hexadezimal codierte Prozentzeichen \] (%) ist. Wenn die Anwendung den URI aus einer Unicode-API abruft, z. B. der Winsock [**WSAAddressToString-API,**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) muss die Anwendung im Hostnamen des URI die version mit Escapezeichen des Prozentzeichens (%) hinzufügen. Um die version des URI mit Escapestrichen zu erstellen, rufen Anwendungen [**InternetCreateUrl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) auf, und legen Sie dabei den *Parameter dwFlags* auf **ICU \_ ESCAPE \_ AUTHORITY** und den IPv6-Hostnamen fest, der in der URL-Komponentenstruktur angegeben ist, die im *lpUrlComponents-Parameter* angegeben ist.

Für alle Socketvorgänge verwendet WinINet die Bereichs-ID. Da die Bereichs-ID jedoch nur eine lokale Host-Bedeutung hat, wird sie nicht als Teil der HTTP-Protokollheader in der Anforderung gesendet. Beispielsweise wird der Aufruf von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) mit der folgenden URL im *lpszUrl-Parameter* aufgerufen.

``` syntax
https://[fec0::2%251]:80/path.htm
```

Der Bereich-ID-Teil der URL wird von WinINet entfernt, wenn die HTTP-Anforderung für diese URL gesendet wird. Die Anforderung enthält die folgenden Header:

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> WinINet unterstützt keine Serverimplementierung. Darüber hinaus sollte sie nicht von einem Dienst verwendet werden. Verwenden Sie für Serverimplementierungen oder -dienste [Microsoft Windows HTTP Services (WinHTTP).](/windows/desktop/WinHttp/winhttp-start-page)

 

 

 