---
description: Um die IPv6-fähigen Funktionen nutzen zu können, müssen IT-Administratoren in ihrem WPAD-Skript eine Funktion namens FindProxyForURLEx (url, host) definieren, die die ältere FindProxyForUrl-Funktion (url, host) ersetzt.
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: IPv6-Aware proxy helper API Definitions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2bdf7c36b0f0d29f84a0dfc0eb7c21cb577ef1b9ef75cb69cec34a7f7858e7a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119052078"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a>IPv6-Aware proxy helper API Definitions

Um die IPv6-fähigen Funktionen nutzen zu können, müssen IT-Administratoren in ihrem WPAD-Skript eine Funktion namens FindProxyForURLEx (url, host) definieren, die die ältere FindProxyForUrl-Funktion (url, host) ersetzt. Nur über die neue FindProxyForURLEx-Funktion können Administratoren die neuen Funktionen ausführen.

Wir haben auch versucht, die Arbeit für Entwickler zu vereinfachen, indem wir unsere Funktionen so ausrichten, dass verschiedene Arten von IP-Adressen in der gleichen Reihenfolge wie andere Netzwerkkomponenten zurückgeben, insbesondere IPv6-Adressen gefolgt von IPv4-Adressen (d. h. aktuelles Verhalten für die getaddrinfo(..)-Funktion von Winsock).

Die folgenden Funktionen sind Erweiterungen der [Pac-Dateiformatspezifikation (Navigator Proxy Auto-Config),](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) um WPAD-Skripts für die Handhabung von IPv6-fähigen Netzwerken zu ermöglichen.

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a>Vordefinierte Funktionen und Umgebung für die JavaScript-Funktion FindProxyforURLEx

Hostnamebasierte Bedingungen

<dl> <dt>

[**isResolvableEx**](isresolvableex.md)
</dt> <dd>

Bestimmt, ob eine bestimmte Hostzeichenfolge in eine IP-Adresse auflösen kann.

</dd> <dt>

[**isInNetEx**](isinnetex.md)
</dt> <dd>

Bestimmt, ob sich eine IP-Adresse in einem bestimmten Subnetz befindet.

</dd> </dl>

Verwandte Hilfsfunktionen

<dl> <dt>

[**dnsResolveEx**](dnsresolveex.md)
</dt> <dd>

Lösen Sie eine Hostzeichenfolge in ihre IP-Adresse auf.

</dd> <dt>

[**myIPAddressEx**](myipaddressex.md)
</dt> <dd>

Sucht alle IP-Adressen für localhost.

</dd> <dt>

[**sortIpAddressList**](sortipaddresslist.md)
</dt> <dd>

Sortiert eine Liste von IP-Adressen.

</dd> <dt>

[**getClientVersion**](getclientversion.md)
</dt> <dd>

Ruft die Version der WPAD-Verarbeitungs-Engine ab.

</dd> </dl>

> [!Note]  
> Diese Funktionalität erfordert Windows Internet Explorer 7 oder höher.

 

 

 



