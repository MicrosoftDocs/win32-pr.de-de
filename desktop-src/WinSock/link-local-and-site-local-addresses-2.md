---
description: Lokale IPv6-Linkadressen und standortspezifische Adressen werden als bereichsspezifische Adressen bezeichnet.
ms.assetid: d31882f6-b747-47c7-83cb-a9a03fe11cb8
title: Lokale und standortbasierte IPv6-Adressen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22220adb2c1b0338462f7ed87b3937a97c3d0b8a8b0aa2d9858d5c5efc8b4f54
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794780"
---
# <a name="ipv6-link-local-and-site-local-addresses"></a>Lokale und standortbasierte IPv6-Adressen

Lokale IPv6-Linkadressen und standortspezifische Adressen werden als bereichsspezifische Adressen bezeichnet. Die Windows Sockets (Winsock)-API unterstützt den **\_ Sin6-Bereichs-ID-Member \_** in der [**sockaddr \_ in6-Struktur**](sockaddr-2.md) für die Verwendung mit bereichsbe bereichsbeladenen Adressen. Für lokale IPv6-Linkadressen (Präfix fe80::/10) ist der **member sin6 \_ scope \_ id** in der **sockaddr \_ in6-Struktur** die Schnittstellennummer. Bei lokalen IPv6-Adressen (Präfix fec0::/10) ist das id-Member des **sin6-Bereichs \_ \_** in der **sockaddr \_ in6-Struktur** ein Standortbezeichner.

Ein Beispiel für eine link-lokale IPv6-Adresse auf Schnittstelle \# 5 ist:

``` syntax
fe80::208:74ff:feda:625c%5
```

Der folgende Befehl ist auf Windows XP mit Service Pack 1 (SP1) und höher verfügbar, um IPv6 auf einem lokalen Computer abfragen und konfigurieren zu können:

-   [Netsh.exe](netsh-exe.md)

Konfigurationsänderungen, die mithilfe Netsh.exe Befehlen vorgenommen werden, sind dauerhaft und gehen nicht verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wird.

Vor Windows XP mit Service Pack 1 (SP1) wurden für die IPv6-Konfiguration und -Verwaltung mehrere ältere Befehlszeilentools (Net.exe, Ipv6.exe und Ipsec6.exe) verwendet, um IPv6 zu konfigurieren und zu verwalten. Bei Verwendung dieser älteren Tools sind die IPv6-Änderungen nicht dauerhaft und gehen verloren, wenn der Computer oder das IPv6-Protokoll neu gestartet wurde. Diese älteren Befehlszeilentools werden nur auf Windows XP unterstützt.

Auf Windows XP mit SP1 zeigt der folgende Befehl die Liste der IPv6-Schnittstellen auf einem lokalen Computer an, einschließlich des Schnittstellenindexes, des Schnittstellennamens und verschiedener anderer Schnittstelleneigenschaften.

**netsh interface ipv6 show interface**

Bei Windows XP mit SP1 ändert der folgende Befehl den Standortbezeichner, der einem Schnittstellenindex zugeordnet ist.

**netsh interface ipv6 set interface <InterfaceIndex or Name> siteid=value**

Unter Windows XP ändert der folgende ältere Befehl auch den Standortbezeichner, der einer standortbasierten Adresse zugeordnet ist, in 3.

**ipv6 rtu fec0::/10 3**

Wenn Sie eine bereichsspezifische Adresse senden oder eine Verbindung mit dieser herstellen, kann der **Sin6-Bereichs-ID-Member \_ \_** in der [**sockaddr \_ in6-Struktur**](sockaddr-2.md) nicht angegeben werden (null), was eine mehrdeutige bereichsspezifische Adresse darstellt. Die folgende lokale Linkadresse ist beispielsweise mehrdeutig:

``` syntax
fe80::10
```

Wenn Sie eine Bindung an eine bereichsspezifische Adresse erstellen, muss der **sin6-Bereichs-ID-Member \_ \_** in der [**sockaddr \_ in6-Struktur**](sockaddr-2.md) einen Wert ungleich 0 (null) enthalten, der eine gültige Schnittstellennummer für eine link-local-Adresse oder einen Standortbezeichner für eine standortbasierte Adresse angibt.

## <a name="ambiguous-scoped-addresses"></a>Mehrdeutige Bereichsadressen

Wenn Sie eine Bereichsadresse senden oder eine Verbindung mit dieser herstellen und in der [**sockaddr \_ in6-Struktur**](sockaddr-2.md) keinen **sin6-Bereichs-ID-Member \_ \_** angegeben haben, ist die bereichsumfangsierte Adresse mehrdeutig. Um dies zu beheben, bestimmt das IPv6-Protokoll zunächst, ob Sie den Socket an eine Quelladresse gebunden haben. Wenn dies der Wert ist, löst die gebundene Quelladresse die Mehrdeutigkeit auf, indem eine Schnittstellennummer oder ein Standortbezeichner angegeben wird.

Wenn Sie eine bereichsgebundene Adresse senden oder eine Verbindung mit dieser herstellen und weder den **Sin6-Bereichs-ID-Member \_ \_** angegeben noch eine Quelladresse gebunden haben, überprüft das IPv6-Protokoll die Routingtabelle. Der folgende Befehl zeigt beispielsweise die IPv6-Routingtabelle auf einem lokalen Computer an:

**„netsh interface ipv6 show route“**

``` syntax
No   Manual   256  fe80::/64      13  Local Area Connection
No   Manual   256  fe80::/64      14  Wireless Network Connection
```

Dies gibt an, dass lokale Linkadressen standardmäßig als On-Link-Adressen mit Schnittstelle \# 13 und \# 14 behandelt werden.

Mehrdeutigkeit entsteht, wenn ein lokaler Computer über mehrere Netzwerkadapter verfügt. Der obige **Netsh-Befehl** gibt beispielsweise an, dass zwei Netzwerkschnittstellen (Local Area Connection und Wireless Network Connection) verfügbar sind. Wenn eine Anwendung eine lokale Zielverbindungsadresse (z. B. fe80::10) ohne Bereichs-ID angibt, ist nicht klar, welcher Adapter zum Senden des Pakets verwendet werden soll. Nur bei einem link-lokalen Unicast (fe80::/64) oder einer IPv6-Zieladresse im Linkbereich (ff00::/8) kann beim Senden eines Pakets keine Bereichs-ID enthalten sein.

## <a name="neighbor-discovery"></a>Nachbarsuche

Wenn Sie den member **sin6 \_ scope \_ id** in der [**sockaddr \_ in6-Struktur**](sockaddr-2.md) nicht angegeben haben, keine Quelladresse gebunden und keine Route für link-local-Adressen angegeben haben, versucht das IPv6-Protokoll Neighbor Discovery, um die lokale Zielverbindungsadresse aufzulösen. Für ein bestimmtes Paket, das gesendet wird, wird eine Schnittstelle versucht. Diese erste Schnittstelle, die ausprobiert wird, wird als die bevorzugte Schnittstelle betrachtet. Wenn neighbor Discovery die lokale Linkadresse auf einer Schnittstelle nicht auflösen kann, wird das zu sendende Paket gelöscht, und das System weiß, dass die lokale Zielverbindungsadresse über diese Schnittstelle nicht erreichbar ist. Beim nächsten Paket, das unter den gleichen Bedingungen gesendet werden soll, wird eine andere Schnittstelle für die Nachbarermittlung versucht. Dieser Prozess wird für jedes neue Paket durch jede der Schnittstellen auf einem lokalen Computer fortgesetzt, bis die Nachbarermittlung auf die lokale Zielverbindungsadresse antwortet oder alle möglichen Schnittstellen versucht wurden und fehlgeschlagen sind. Jedes Mal, wenn ein Versuch, den Nachbarn aufzulösen, fehlschlägt, wird eine Schnittstelle für diesen Nachbarn entfernt.

Wenn die lokale Zielverbindungsadresse auflöset, wird diese Schnittstelle verwendet, um das aktuelle Paket zu senden. Diese Schnittstelle wird auch für alle nachfolgenden pakete mit mehrdeutigem Gültigkeitsbereich verwendet, die an dieselbe lokale Linkzieladresse gesendet werden.

Wenn neighbor Discovery die lokale Zielverbindungsadresse auf allen Schnittstellen nicht auflösen kann, versucht das System, das Paket an die bevorzugte Schnittstelle zu senden (die erste Schnittstelle hat versucht). Der Netzwerkstapel versucht weiterhin, die lokale Zielverbindungsadresse auf der bevorzugten Schnittstelle aufzulösen. Nach einem Zeitraum nach dem Fehler bei der Nachbarermittlung auf allen Schnittstellen startet der Netzwerkstapel den Prozess erneut und versucht, die lokale Zielverbindungsadresse auf allen Schnittstellen aufzulösen. Derzeit beträgt dieses Zeitintervall, in dem die Nachbarermittlung erneut auf allen Schnittstellen versucht wird, 60 Sekunden. Dieses Zeitintervall kann sich jedoch bei Versionen von Windows und sollte nicht von einer Anwendung angenommen werden.

> [!Note]  
> Wenn eine Anwendung dieselbe lokale Linkadresse an eine andere Schnittstelle bindet, nachdem neighbor discovery die lokale Linkadresse aufgelöst hat, wird die Schnittstelle nicht mit der von neighbor Discovery zurückgegebenen lokalen Zieladresse überschrieben.

 

Weitere Informationen zur Nachbarermittlung für IP-Version 6 finden Sie unter [RFC4861,](https://tools.ietf.org/html/rfc4861) veröffentlicht von der IETF.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[IPv6-Standortpräfixe](site-prefixes-2.md)
</dt> <dt>

[Ipv6.exe](ipv6-exe-2.md)
</dt> <dt>

[Netsh.exe](netsh-exe.md)
</dt> <dt>

[Verwenden von IPv6](using-ipv6-2.md)
</dt> </dl>

 

 



