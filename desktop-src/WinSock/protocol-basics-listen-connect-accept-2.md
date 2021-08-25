---
description: Die Protokollgrund grundlagen von WSPListen, WSPAccept und WSPConnect zum Herstellen einer Socketverbindung mit Windows Sockets (Winsock).
ms.assetid: b1b4d6b9-36db-4000-9c6b-662765b6d091
title: 'Protokollgrund grundlagen: Lauschen, Verbinden, Akzeptieren'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db73ea4bca5a709ff6d030fcbb44661c6181e552955d02b67d8eb2bcf680bf92
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119857920"
---
# <a name="protocol-basics-listen-connect-accept"></a>Protokollgrund grundlagen: Lauschen, Verbinden, Akzeptieren

Die grundlegenden Vorgänge, die mit dem Herstellen einer Socketverbindung verbunden sind, lassen sich am bequemsten im Hinblick auf das Client-Server-Paradigma erklären.

Die Serverseite erstellt zunächst einen Socket, bindet ihn an eine bekannte lokale Adresse (damit der Client sie finden kann) und setzt den Socket über [**WSPListen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85))in den Lauschmodus, um sich auf eingehende Verbindungsanforderungen vorzubereiten und die Länge der Verbindungsrückstandwarteschlange anzugeben. Dienstanbieter halten ausstehende Verbindungsanforderungen in einer Backlogwarteschlange, bis sie vom Server ausgeführt oder (aufgrund eines Time out) vom Client zurückgenommen werden. Ein Dienstanbieter kann Anforderungen ignorieren, um die Größe der Backlogwarteschlange über eine vom Anbieter definierte Obergrenze hinaus zu erweitern.

Wenn nun ein blockierender Socket verwendet wird, kann die Serverseite [**sofort WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) aufrufen, wodurch blockiert wird, bis eine Verbindungsanforderung aussteht. Umgekehrt kann der Server auch einen der zuvor erläuterten Mechanismen zur Netzwerkereignisanzeige verwenden, um Benachrichtigungen über eingehende Verbindungsanforderungen zu erstellen. Abhängig vom ausgewählten Benachrichtigungsmechanismus gibt der Anbieter entweder eine Windows aus oder signalisiert ein Ereignisobjekt, wenn Verbindungsanforderungen eintreffen. Informationen [zum Registrieren für das](notification-of-network-events-2.md) FD ACCEPT-Netzwerkereignis finden Sie unter Benachrichtigung über \_ Netzwerkereignisse.

Die Clientseite erstellt einen entsprechenden Socket und initiiert die Verbindung, indem [**WSPConnect unter**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))Angabe der bekannten Serveradresse aufruft. Clients führen in der [](/windows/desktop/api/winsock/nf-winsock-bind) Regel vor dem Initiieren einer Verbindung keinen expliziten Bindungsvorgang aus, sodass der Dienstanbieter eine implizite Bindung in ihrem Namen ausführen kann. Wenn sich der Socket im Blockierungsmodus befindet, wird **WSPConnect** blockiert, bis der Server die Verbindungsanforderung empfangen und ausgeführt hat (oder bis ein Time out auftritt). Andernfalls sollte der Client einen der zuvor erläuterten Mechanismen zur Netzwerkereignisanzeige verwenden, um eine Benachrichtigung über das Herstellen einer neuen Verbindung zu erhalten. Je nach ausgewähltem Benachrichtigungsmechanismus gibt der Anbieter dies entweder über eine Windows oder durch Signalisieren eines Ereignisobjekts an.

Wenn die Serverseite [**WSPAccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)aufruft, ruft der Dienstanbieter die von der Anwendung bereitgestellte Bedingungsfunktion auf und verwendet Funktionsparameter, um die Serverinformationen vom obersten Eintrag in der Backlogwarteschlange für Verbindungsanforderungen an die Serverinformationen zu übergeben. Zu diesen Informationen gehören beispielsweise die Adresse des Host, der eine Verbindung herstellen soll, alle verfügbaren Benutzerdaten und alle verfügbaren QoS-Informationen. Anhand dieser Informationen bestimmt die Bedingungsfunktion des Servers, ob die Anforderung akzeptiert, abgelehnt oder eine Entscheidung auf einen späteren Zeitpunkt zurück gestellt werden soll. Diese Entscheidung wird durch den Rückgabewert der Bedingungsfunktion angegeben. Informationen [zum Registrieren für das](notification-of-network-events-2.md) FD CONNECT-Netzwerkereignis finden Sie unter Benachrichtigung über \_ Netzwerkereignisse.

Wenn der Server entscheidet, die Anforderung zu akzeptieren, muss der Anbieter einen neuen Socket mit allen Attributen und Ereignisregistrierungen erstellen, die auch der lauschende Socket enthält. Der ursprüngliche Socket verbleibt im Lauschenzustand, sodass nachfolgende Verbindungsanforderungen empfangen werden können. Durch Ausgabeparameter der Bedingungsfunktion kann der Server auch alle Antwortbenutzerdaten angeben und QoS-Parameter zuweisen (vorausgesetzt, diese Vorgänge werden vom Dienstanbieter unterstützt).

 

 
