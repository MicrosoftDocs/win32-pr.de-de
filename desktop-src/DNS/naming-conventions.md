---
title: Namenskonventionen
description: Namenskonventionen haben ein gemeinsames Ziel, einen Namen eindeutig in eine Netzwerkadresse aufzulösen, in der Regel eine IP-Adresse. Der Unterschied zwischen Benennungskonventionen liegt in der unterschiedlichen Vorgehensweise der einzelnen Konventionen zum Auflösen von Namen.
ms.assetid: 1ec96d2d-bb5a-4938-88c2-4d2802a326cd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b378f9383f773cb24fb47c81cb92a066094a4ce528d7f3710212c6bb7cac0d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119076588"
---
# <a name="naming-conventions"></a>Namenskonventionen

Namenskonventionen haben ein gemeinsames Ziel: einen Namen eindeutig in eine Netzwerkadresse aufzulösen, in der Regel eine IP-Adresse. Der Unterschied zwischen Benennungskonventionen liegt in der unterschiedlichen Vorgehensweise der einzelnen Konventionen zum Auflösen von Namen.

Die folgenden Namenskonventionen werden verwendet, um Computer in verschiedenen Methoden zur Namensauflösung des Systems zu identifizieren, einschließlich der Windows 2000-Methode:

-   [Computername](#computer-name)
-   [Hostname](#host-name)
-   [Vollqualifizierter Domänenname (FQDN)](#fully-qualified-domain-name)
-   [Relativer Distinguished Name](#relative-distinguished-name)

## <a name="computer-name"></a>Computername

Im flachen NetBIOS-Namensraum löst ein einzelner Name eindeutig einen Computernamen in eine Netzwerkadresse auf. Dies ist der Name, den Windows Versionen in Browser- und Masterbrowserlisten gespeichert haben, sodass Peer-Windows-Netzwerke Ressourcen auf Netzwerkcomputern Windows durchsuchen können. In diesem Szenario war der dem Computer zugeordnete Begriff *Computername.* Die Registrierung des Computernamens hängt von Netzwerkübertragungen ab (und einem Masterbrowser, der durch spätere Windows-Versionsnummern oder Windows NT-Nutzung oder eine Kombination gewonnen wird). Dies war nützlich für kleine peerbasierte Windows-Netzwerke, aber netzwerke wurden bald größer als die Verwendung von Broadcasts und einfachen Flatdatei-Masterbrowserlisten.

## <a name="host-name"></a>Hostname

Als Nächstes wurde die Windows Internet Naming Service (WINS) veröffentlicht, die ein dynamisches und zentralisiertes Repository von NetBIOS-basierten Computernamen aktiviert hat, die auf WINS-Servern gespeichert sind. Diese Repositorys können für ein größeres Netzwerk verwendet werden. Mit dieser Entwicklung könnten Namensauflösungsabfragen an einen WINS-Server geleitet werden (anstatt übertragen zu werden), und Konflikte könnten zentral gebrochen werden. Bei WINS wurde der Begriff Computername beibehalten, aber auch der Begriff *Hostname* wurde synonym mit dem Computernamen verwendet. Zu diesem Zeitpunkt war WINS der Standardnamensrelöser für Windows-Plattformen, aber DNS wurde mit der Beliebtheit und Verbreitung größerer und größerer Netzwerke immer beliebter.

Die Netzwerke wurden größer, und WINS wurde weniger in der Lage, die wachsende Anzahl von Namen zu behandeln. Die abnehmende Fähigkeit von WINS, die Namensauflösungslast zu bewältigen, ist nicht auf die Verarbeitungsleistung für die Auflösung, sondern auf die Tatsache, dass die Generierung eindeutiger Namen für viele Computer zu einer ständig wachsenden Verwaltungslast geworden ist.

## <a name="fully-qualified-domain-name"></a>Vollqualifizierter Domänenname

DNS ist eine bessere Lösung. mit dem hierarchischen Namensraum ist die Notwendigkeit eindeutiger Computernamen in einer bestimmten Domäne isoliert, sodass ein Computername wie *server1* an verschiedenen Domänenspeicherorten in derselben Hierarchie vorhanden sein kann. Mit der Möglichkeit, den gleichen Hostnamen in verschiedenen Domänen zu verwenden, ist es notwendig, einen Namen zu verwenden, der die DNS-Hierarchie ordnungsgemäß adressiert hat. Der Name muss nicht nur den Computernamen oder Hostnamen enthalten, sondern auch einen Namen, der diesen Computer innerhalb der gesamten DNS-Hierarchie eindeutig identifizieren oder vollständig qualifizieren konnte. Dieser Name ist [*der vollqualifizierte Domänenname*](f-gly.md) (Fully Qualified Domain Name, FQDN), z. B. server1.widgets.microsoft.com.

In bestimmten Situationen ist der Domänenhierarchieteil des FQDN jedoch umständlich, und ein lokaler Name für einen bestimmten Computer (oder einen anderen DNS-Host), der relativ zur DNS-Domäne ist, in der sich der Host befindet, ist erforderlich. Dieser Name ist der [*relative Distinguished Name.*](r-gly.md) Der relative Distinguished Name ist einfach der einzelne Hostname links vom linken Punkt im FQDN, damit ein FQDN von server1.widgets.microsoft.com server1 als relativen Distinguished Name hat.

## <a name="relative-distinguished-name"></a>Relativer Distinguished Name

Anstatt neue Namen oder neue Namenskonventionen für Benutzer von NetBIOS-Namen zu benennen, verwendet DNS einfach den Computernamen (Hostnamen) als relativen Distinguished Name und fügt die DNS-Domänenhierarchie an diesen Namen an, um den FQDN zu erstellen. Die folgende Abbildung veranschaulicht, wie Der Computername (oder Hostname oder relativer Distinguished Name) des FQDN identifiziert wird:

![Rdn- und DNS-Domänenhierarchie werden kombiniert, um einen FQDN zu erstellen](images/fqdn.png)

 

 




