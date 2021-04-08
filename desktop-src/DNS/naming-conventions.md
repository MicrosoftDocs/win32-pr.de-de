---
title: Namenskonventionen
description: Benennungs Konventionen haben ein häufiges Ziel, einen Namen in eine Netzwerkadresse eindeutig aufzulösen, im Allgemeinen eine IP-Adresse. Der Unterschied zwischen Benennungs Konventionen liegt im eindeutigen Ansatz der einzelnen Konventionen zum Auflösen von Namen.
ms.assetid: 1ec96d2d-bb5a-4938-88c2-4d2802a326cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2091123ed2bf1022910231cd08cb0e6cccae51a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037247"
---
# <a name="naming-conventions"></a>Namenskonventionen

Benennungs Konventionen haben ein gemeinsames Ziel: eine eindeutige Auflösung eines Namens in eine Netzwerkadresse, im Allgemeinen eine IP-Adresse. Der Unterschied zwischen Benennungs Konventionen liegt im eindeutigen Ansatz der einzelnen Konventionen zum Auflösen von Namen.

Die folgenden Benennungs Konventionen dienen zum Identifizieren von Computern mit verschiedenen Methoden zur Auflösung von Systemnamen, einschließlich der Windows 2000-Methode:

-   [Computer Name](#computer-name)
-   [Hostname](#host-name)
-   [Vollqualifizierter Domänenname (FQDN)](#fully-qualified-domain-name)
-   [Relativer definierter Name](#relative-distinguished-name)

## <a name="computer-name"></a>Computername

Im flachen NetBIOS-Namespace löst ein einzelner Name einen Computernamen eindeutig in eine Netzwerkadresse auf. Dies ist der Name, den frühere Windows-Versionen in Browser-und Haupt Browser Listen gespeichert haben, sodass Peer-Windows-Netzwerke Ressourcen auf vernetzten Windows-Computern durchsuchen können. In diesem Szenario war der mit dem Computer verknüpfte Begriff " *Computername*". Die Registrierung des Computer namens hängt von Netzwerkübertragungen (und einem Haupt Browser) ab, die durch Wahlen ermittelt werden, die von späteren Windows-Versionsnummern oder der Windows NT-Verwendung oder einer Kombination gewonnen wurden. Dies war bei kleinen, Peer basierten Windows-Netzwerken nützlich, aber Netzwerke stiegen bald über die Verwendung von Übertragungen und einfache Browser Listen für Flatfiles hinaus.

## <a name="host-name"></a>Hostname

Danach kam Windows Internet Naming Service (WINS), das ein dynamisches und zentralisiertes Repository von NetBIOS-basierten Computernamen ermöglichte, die auf WINS-Servern gespeichert sind. Diese Depots können ein größeres Netzwerk bedienen. Mit dieser Entwicklung können namens Auflösungs Abfragen an einen WINS-Server weitergeleitet werden (statt übertragen), und Konflikte können zentral übermittelt werden. Mit WINS wurde der Begriff "Computername" beibehalten, aber der Begriff " *Hostname* " wurde ebenfalls angezeigt und ist austauschbar mit dem Computernamen. Zu diesem Zeitpunkt war WINS der Standardname-Resolver für Windows-Plattformen, aber DNS wurde mit der Beliebtheit und Verbreitung größerer und größerer Netzwerke gewonnen.

Netzwerke wuchsen, und WINS wurde weniger fähig, die wachsende Anzahl von Namen zu verarbeiten. Die absteigende Funktion von WINS zur Handhabung der namens Auflösungs Last war nicht auf die für die Auflösung erforderliche Verarbeitungsleistung zurückzuführen, sondern auf die Tatsache, dass das Erstellen eindeutiger Namen für viele Computer zu einer immer größeren Verwaltungs Belastung geworden ist.

## <a name="fully-qualified-domain-name"></a>Vollqualifizierter Domänenname

DNS ist eine bessere Lösung. mit dem hierarchischen Namespace werden eindeutige Computernamen in eine bestimmte Domäne isoliert, sodass ein Computername wie *Server1* an verschiedenen Domänen Standorten in derselben Hierarchie vorhanden sein muss. Mit der Möglichkeit, in verschiedenen Domänen denselben Hostnamen zu haben, ist die Notwendigkeit für einen Namen aufgetreten, der die DNS-Hierarchie ordnungsgemäß adressiert hat. Der Name muss nicht nur den Computernamen oder den Hostnamen enthalten, sondern auch einen Namen, mit dem dieser Computer in der gesamten DNS-Hierarchie eindeutig identifiziert oder voll qualifiziert werden kann. Dieser Name ist der [*voll qualifizierte Domänen Name (Fully Qualified Domain Name*](f-gly.md) , FQDN) – z. b. server1.widgets.Microsoft.com.

In bestimmten Situationen ist der Domänen Hierarchie-Teil des FQDN jedoch mühsam und ein lokaler Name für einen bestimmten Computer (oder einen anderen DNS-Host), der relativ zur DNS-Domäne ist, in der sich der Host befindet, ist erforderlich. Dieser Name ist der [*Relative Distinguished Name*](r-gly.md). Der Relative Distinguished Name ist einfach der einzige Hostname links neben dem äußersten äußersten linken Punkt im FQDN, sodass ein FQDN von Server1.widgets.Microsoft.com server1 als relativen Distinguished Name aufweist.

## <a name="relative-distinguished-name"></a>Relativer definierter Name

Anstatt neue Namen oder neue Benennungs Konventionen für Benutzer von NetBIOS-Namen zu erzwingen, verwendet DNS einfach den Computernamen (Hostname) als relativen Distinguished Name und fügt die DNS-Domänen Hierarchie an diesen Namen an, um den FQDN zu erstellen. In der folgenden Abbildung wird veranschaulicht, wie der Computername (oder der Hostname oder der Relative Distinguished Name) des FQDN identifiziert wird:

![RDN und DNS-Domänen Hierarchie kombinieren, um einen FQDN zu erstellen](images/fqdn.png)

 

 




