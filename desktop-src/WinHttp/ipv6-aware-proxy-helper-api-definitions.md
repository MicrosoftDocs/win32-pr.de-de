---
description: Um die von IPv6 aktivierten Funktionen nutzen zu können, müssen IT-Administratoren innerhalb Ihres WPAD-Skripts definieren, eine Funktion mit dem Namen "findproxyforurlex (URL, Host)", die die Legacy Funktion "FindProxyForURL (URL, Host)" ersetzt.
ms.assetid: e531a66d-5c50-4065-a12a-783fd4d1d310
title: API-Definitionen für IPv6-Aware Proxy-Hilfsprogramme
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79b1ff5a0c287327593e65e29a0b03cfb59269f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106349631"
---
# <a name="ipv6-aware-proxy-helper-api-definitions"></a>API-Definitionen für IPv6-Aware Proxy-Hilfsprogramme

Um die von IPv6 aktivierten Funktionen nutzen zu können, müssen IT-Administratoren innerhalb Ihres WPAD-Skripts definieren, eine Funktion mit dem Namen "findproxyforurlex (URL, Host)", die die Legacy Funktion "FindProxyForURL (URL, Host)" ersetzt. Nur aus der neuen findproxyforurlex-Funktion können Administratoren die neuen Funktionen ausführen.

Wir haben auch versucht, die Arbeit für Entwickler zu vereinfachen, indem wir unsere Funktionen so ausrichten, dass verschiedene Typen von IP-Adressen in derselben Reihenfolge wie andere Netzwerkkomponenten zurückgegeben werden, insbesondere IPv6-Adressen, gefolgt von IPv4-Adressen (d.h. Aktuelles Verhalten für die getaddrinfo (..)-Funktion von Winsock).

Die folgenden Funktionen sind Erweiterungen der [PAC-Datei Format Spezifikation (Navigator Proxy Auto-config)](https://web.archive.org/web/20060424005037/wp.netscape.com/eng/mozilla/2.0/relnotes/demo/proxy-live.html) , um WPAD-Skripts das Verarbeiten von IPv6-fähigen Netzwerken zu ermöglichen.

## <a name="predefined-functions-and-environment-for-the-javascript-function-findproxyforurlex"></a>Vordefinierte Funktionen und Umgebung für die JavaScript-Funktion findproxyforurlex

Hostname-basierte Bedingungen

<dl> <dt>

[**isresolvableex**](isresolvableex.md)
</dt> <dd>

Bestimmt, ob eine angegebene Host Zeichenfolge in eine IP-Adresse aufgelöst werden kann.

</dd> <dt>

[**isinnettex**](isinnetex.md)
</dt> <dd>

Bestimmt, ob sich eine IP-Adresse in einem bestimmten Subnetz befindet.

</dd> </dl>

Zugehörige Utility-Funktionen

<dl> <dt>

[**dnsresolveex**](dnsresolveex.md)
</dt> <dd>

Auflösen einer Host Zeichenfolge in die zugehörige IP-Adresse.

</dd> <dt>

[**myIPAddressEx**](myipaddressex.md)
</dt> <dd>

Sucht alle IP-Adressen für localhost.

</dd> <dt>

[**"menpaddresslist"**](sortipaddresslist.md)
</dt> <dd>

Sortiert eine Liste von IP-Adressen.

</dd> <dt>

[**GetClientVersion**](getclientversion.md)
</dt> <dd>

Ruft die Version der WPAD-Verarbeitungs-Engine ab.

</dd> </dl>

> [!Note]  
> Diese Funktionalität erfordert Windows Internet Explorer 7 oder höher.

 

 

 



