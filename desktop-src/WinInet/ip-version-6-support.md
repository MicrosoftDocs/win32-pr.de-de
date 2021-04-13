---
title: Unterstützung von IP-Version 6
description: Ab IE7 und höher unterstützt WinInet IPv6-Literale im Hostnamen und die Autoritäts Komponente des URI.
ms.assetid: cbbb9f93-15b0-4017-ac39-8a396203532e
keywords:
- Unterstützung von IP-Version 6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5ed0857d9a0968bcd3e6c18e54623fb0c7d86cb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104390822"
---
# <a name="ip-version-6-support"></a>Unterstützung von IP-Version 6

Ab IE7 und höher unterstützt WinInet IPv6-Literale im Hostnamen und die Autoritäts Komponente des URI. WinInet unterstützt auch die Verwendung von IPv6-Literalen in relevanten Teilen des HTTP-Protokolls, z. b. im Location-Header.

## <a name="hostname-ipv6-literals-and-uri-components"></a>IPv6-Literale und URI-Komponenten des Hostnamens

WinInet implementiert IPv6-Literale gemäß den Spezifikationen in RFC 3513. Wie in dieser RFC angegeben, müssen IPv6-Literale in einem URI in eckige Klammern eingeschlossen werden. Beispielsweise ist https:// \[ :: 1 \] /ein gültiger IPv6-URI; das Formular ohne eckige Klammern ( https://::1/) ist ungültig. Hostname-IPv6-Literale, die nicht Teil des URI sind, müssen jedoch nicht in die eckigen Klammern eingeschlossen werden. beide Formen sind für WinInet zulässig. Beispielsweise sind ":: 1" und " \[ :: 1 \] " akzeptable Formen von IPv6-Hostnamen Literalen. Andere APIs, wie z. b. die Winsock-API, akzeptieren ebenfalls beide Formulare. Daher sollten Anwendungen darauf vorbereitet werden, beide Formen von IPv6-Hostnamen literalen zu verarbeiten.

## <a name="scope-id"></a>Bereichs-ID

Die IPv6-Literaladresse im URI kann eine Bereichs-ID enthalten. Eine Bereichs-ID kann eine Schnittstellen-ID sein, z \[ . b. FE80:: 1% 1 \] . Der in RFC 3986 dokumentierte URI-Standard definiert nicht die Syntax für die Bereichs-ID, und der URI wird als nicht einheitlich betrachtet, wenn die Bereichs-ID vorhanden ist. WinInet akzeptiert jedoch eine Bereichs-ID in der Autoritäts Komponente des URIs und im Hostnamen-IPv6-Literal.

Das Prozentzeichen (%). in ist die IPv6-Literaladresse in Prozent mit Escapezeichen versehen, wenn Sie im URI vorhanden ist Beispielsweise muss die Bereichs-ID FE80:: 2% 3 im URI als "https:// \[ FE80:: 2% 253 \] /" angezeigt werden, wobei "%25" das hexadezimal codierte Prozentzeichen (%) ist. Wenn die Anwendung den URI aus einer Unicode-API abruft, z. b. die Winsock [**wsaadresssstostring**](/windows/desktop/api/winsock2/nf-winsock2-wsaaddresstostringa) -API, muss die Anwendung die Escapeversion des Prozent Zeichens (%) hinzufügen. im Hostnamen des URI. Zum Erstellen der Escapeversion des URIs rufen Anwendungen [**internetpurateurl**](/windows/desktop/api/Wininet/nf-wininet-internetcreateurla) auf, wobei der *dwFlags* -Parameter auf **ICU \_ Escape \_ Authority** festgelegt ist, und den IPv6-Hostnamen, der in der URL-Komponenten Struktur angegeben ist, die im *lpurlcomponents* -Parameter angegeben ist.

Für alle Socketvorgänge verwendet Wininet die Bereichs-ID. Da die Bereichs-ID jedoch nur über lokale Host Bedeutung verfügt, wird Sie nicht als Teil der HTTP-Protokoll Header in der Anforderung gesendet. Der Aufruf von [**InternetOpenUrl**](/windows/desktop/api/Wininet/nf-wininet-internetopenurla) wird z. b. mit der folgenden URL im *lpszurl* -Parameter aufgerufen.

``` syntax
https://[fec0::2%251]:80/path.htm
```

Der Bereich-ID-Teil der URL wird durch Wininet entfernt, wenn die HTTP-Anforderung für diese URL gesendet wird. Die Anforderung enthält die folgenden Header:

``` syntax
GET path.htm HTTP/1.1
Host: [fec0::2]
```

> [!Note]  
> WinInet unterstützt keine Server Implementierungen. Außerdem sollte Sie nicht von einem Dienst verwendet werden. Verwenden Sie für Server Implementierungen oder-Dienste [Microsoft Windows HTTP-Dienste (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).

 

 

 