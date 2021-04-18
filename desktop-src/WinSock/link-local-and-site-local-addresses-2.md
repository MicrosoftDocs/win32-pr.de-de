---
description: IPv6-Verbindungs-und Standort lokale Adressen werden als Bereichs bezogene Adressen bezeichnet.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: IPv6-Verbindungs lokale und Standort lokale Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb80b8e201adf382b10dd31fe5607de903d6c588
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343295"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a>IPv6-Verbindungs lokale und Standort lokale Adressen

IPv6-Verbindungs-und Standort lokale Adressen werden als Bereichs bezogene Adressen bezeichnet. Die Windows Sockets (Winsock)-API unterstützt das **sin6 \_ Scope \_ ID** -Element in der [**sockaddr \_ IN6**](sockaddr-2.md) -Struktur zur Verwendung mit Bereichs bezogenen Adressen. Bei IPv6-Verbindungs lokalen Adressen (FE80::/10-Präfix) ist das **sin6 \_ Scope- \_ ID** -Element in der **sockaddr \_ IN6** -Struktur die Schnittstellen Nummer. Für IPv6-Site-Local-Adressen (FEC0::/10-Präfix) ist das **sin6 \_ Scope- \_ ID** -Element in der **sockaddr \_ IN6** -Struktur ein Site Bezeichner.

Ein Beispiel für eine Link-Local-IPv6-Adresse für Schnittstelle \# 5 ist Folgendes:

``` syntax
fe80::208:74ff:feda:625c%5
```

Der folgende Befehl ist unter Windows XP mit Service Pack 1 (SP1) und höher zum Abfragen und Konfigurieren von IPv6 auf einem lokalen Computer verfügbar:

-   [Netsh.exe](netsh-exe.md)

Konfigurationsänderungen, die mithilfe der Netsh.exe Befehle vorgenommen werden, sind permanent und gehen nicht verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wird.

Vor Windows XP mit Service Pack 1 (SP1) verwendeten die IPv6-Konfiguration und-Verwaltung mehrere ältere Befehlszeilen Tools (Net.exe, Ipv6.exe und Ipsec6.exe) zum Konfigurieren und Verwalten von IPv6. Wenn Sie diese älteren Tools verwenden, sind die IPv6-Änderungen nicht permanent und gehen verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wurde. Diese älteren Befehlszeilen Tools werden nur unter Windows XP unterstützt.

Unter Windows XP mit SP1 wird mit dem folgenden Befehl die Liste der IPv6-Schnittstellen auf einem lokalen Computer angezeigt, einschließlich des Schnittstellen Indexes, des Schnittstellen namens und verschiedener anderer Schnittstelleneigenschaften.

**Netsh Interface IPv6 Show Interface**

Unter Windows XP mit SP1 ändert der folgende Befehl den einem Schnittstellen Index zugeordneten Site Bezeichner.

**Netsh Interface IPv6 Set Interface <InterfaceIndex or Name> siteid = Value**

Unter Windows XP ändert der folgende ältere Befehl auch den Standort Bezeichner, der einer Standort lokalen Adresse zugeordnet ist, auf 3.

**IPv6-RTU-FEC0::/10 3**

Wenn Sie eine Bereichs bezogene Adresse senden oder verbinden, kann das **sin6 Scope- \_ \_ ID** -Element in der [**sockaddr \_ IN6**](sockaddr-2.md) -Struktur nicht angegeben (null) bleiben, was eine mehrdeutige Bereichs bezogene Adresse darstellt. Die folgende Link-Local-Adresse ist z. b. mehrdeutig:

``` syntax
fe80::10
```

Wenn Sie eine Bindung an eine Bereichs bezogene Adresse durchlaufen, muss das **sin6 \_ Scope \_ ID** -Element in der [**sockaddr \_ IN6**](sockaddr-2.md) -Struktur einen Wert ungleich 0 (null) enthalten, der eine gültige Schnittstellen Nummer für eine Link-Local-Adresse oder einen Site Bezeichner für eine Site-Local-Adresse angibt.

## <a name="ambiguous-scoped-addresses"></a>Mehrdeutige Bereichs bezogene Adressen

Wenn Sie eine Bereichs bezogene Adresse senden oder verbinden und das **sin6 \_ Scope- \_ ID** -Element nicht in der [**sockaddr \_ IN6**](sockaddr-2.md) -Struktur angegeben haben, ist die Bereichs bezogene Adresse mehrdeutig. Um dieses Problem zu beheben, bestimmt das IPv6-Protokoll zuerst, ob Sie den Socket an eine Quelladresse gebunden haben. Wenn dies der Fall ist, löst die gebundene Quelladresse die Mehrdeutigkeit durch Bereitstellen einer Schnittstellen Nummer oder eines Website Bezeichners auf.

Wenn Sie eine Bereichs bezogene Adresse senden oder verbinden und weder das **sin6 \_ Scope \_ ID** -Element noch eine Quelladresse angegeben haben, prüft das IPv6-Protokoll die Routing Tabelle. Mit dem folgenden Befehl wird beispielsweise die IPv6-Routing Tabelle auf einem lokalen Computer angezeigt:

**„netsh interface ipv6 show route“**

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

Dies gibt an, dass Link-Local-Adressen standardmäßig als Links zu Schnittstelle \# 13 und 14 behandelt werden \# .

Die Mehrdeutigkeit ergibt sich, wenn ein lokaler Computer über mehrere Netzwerkadapter verfügt. Der obige Befehl **netsh** zeigt beispielsweise an, dass zwei Netzwerkschnittstellen vorhanden sind (LAN-Verbindung und drahtlose Netzwerkverbindung). Wenn eine Anwendung eine Ziel-Link-Local-Adresse (z. b. FE80:: 10) ohne Bereichs-ID angibt, ist nicht klar, welcher Adapter zum Senden des Pakets verwendet werden soll. Nur ein Link-Local-Unicast (FE80::/64) oder eine Verknüpfungs Bereichs-Multicast-IPv6-Zieladresse (FF00::/8) kann beim Senden eines Pakets keine Bereichs-ID aufweisen.

## <a name="neighbor-discovery"></a>Nachbarsuche

Wenn Sie das **sin6 \_ Scope \_ ID** -Element nicht in der [**sockaddr \_ IN6**](sockaddr-2.md) -Struktur angegeben, keine Quelladresse gebunden haben und keine Route für Link-Local-Adressen angegeben haben, versucht das IPv6-Protokoll die Nachbar Ermittlung, um die Ziel Link-Local-Adresse aufzulösen. Für ein bestimmtes Paket, das gesendet wird, wird eine Schnittstelle ausprobiert. Diese erste versuchte Schnittstelle wird als bevorzugte Schnittstelle betrachtet. Wenn die Nachbar Ermittlung die Link-Local-Adresse auf einer Schnittstelle nicht auflösen kann, wird das zu sendende Paket gelöscht, und das System speichert, dass die Adresse des Zielverbindungs-lokalen über diese Schnittstelle nicht erreichbar ist. Beim nächsten Paket, das unter allen gleichen Bedingungen gesendet werden soll, wird eine andere Oberfläche für die Nachbar Ermittlung ausprobiert. Dieser Prozess wird durch die einzelnen Schnittstellen auf einem lokalen Computer für jedes neue Paket fortgesetzt, bis die Nachbar Ermittlung auf die Ziel Link-Local-Adresse antwortet oder alle möglichen Schnittstellen fehlgeschlagen sind. Jedes Mal, wenn der Versuch, den Nachbar aufzulösen, fehlschlägt, wird für diesen Nachbarn eine Schnittstelle entfernt.

Wenn die Ziel Link-Local-Adresse aufgelöst wird, wird diese Schnittstelle verwendet, um das aktuelle Paket zu senden. Diese Schnittstelle wird auch für alle nachfolgenden, eindeutig beschränkten Pakete verwendet, die an dieselbe Verbindungs lokale Zieladresse gesendet werden.

Wenn bei der Nachbar Ermittlung die Ziel Link-Local-Adresse für alle Schnittstellen nicht aufgelöst werden kann, versucht das System, das Paket an der am häufigsten bevorzugten Schnittstelle (die erste versuchte Schnittstelle) zu senden. Der Netzwerk Stapel versucht immer, die Ziel Link-Local-Adresse auf der bevorzugten Schnittstelle aufzulösen. Nach einem bestimmten Zeitraum, nachdem die Nachbar Ermittlung an allen Schnittstellen fehlgeschlagen ist, startet der Netzwerk Stapel den Prozess erneut und versucht, die Ziel-Link-Local-Adresse auf allen Schnittstellen aufzulösen. Derzeit beträgt dieses Zeitintervall, in dem die Nachbar Ermittlung wieder auf allen Schnittstellen versucht wird, 60 Sekunden. Dieses Zeitintervall kann sich jedoch in Windows-Versionen ändern und sollte nicht von einer Anwendung angenommen werden.

> [!Note]  
> Wenn eine Anwendung dieselbe Link-Local-Adresse an eine andere Schnittstelle bindet, nachdem die Nachbar Ermittlung die Link-Local-Adresse aufgelöst hat, wird die Schnittstelle mit der von der Nachbar Ermittlung zurückgegebenen Verbindungs lokalen Zieladresse nicht überschrieben.

 

Weitere Informationen zur Nachbar Ermittlung für IP-Version 6 finden Sie unter [RFC4861](https://tools.ietf.org/html/rfc4861) veröffentlicht von IETF.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Site Präfixe](site-prefixes-2.md)
</dt> <dt>

[Ipv6.exe](ipv6-exe-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> <dt>

[Verwenden von IPv6](using-ipv6-2.md)
</dt> </dl>

 

 



