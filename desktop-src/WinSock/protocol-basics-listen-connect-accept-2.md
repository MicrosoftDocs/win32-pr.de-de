---
description: Protokoll Grundlagen von wsplauschen, wspaccept und wspconnect zum Einrichten einer Socketverbindung mit Windows Sockets (Winsock).
ms.assetid: b1b4d6b9-36db-4000-9c6b-662765b6d091
title: 'Grundlagen des Protokolls: lauschen, verbinden, annehmen'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d62ef290d71e571154b4d022c24c7e21f8fffa1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104129133"
---
# <a name="protocol-basics-listen-connect-accept"></a>Grundlagen des Protokolls: lauschen, verbinden, annehmen

Die grundlegenden Vorgänge, die beim Einrichten einer Socketverbindung beteiligt sind, können am häufigsten in Bezug auf das Client-Server-Paradigma erläutert werden.

Die Serverseite erstellt zunächst einen Socket, bindet Sie an eine bekannte lokale Adresse (sodass der Client Sie finden kann) und versetzt den Socket in den Empfangsmodus, über [**wsplauschen**](/previous-versions/windows/hardware/network/ff566297(v=vs.85)), um alle eingehenden Verbindungsanforderungen vorzubereiten und die Länge der Warteschlange für den Verbindungs Rückstand anzugeben. Dienstanbieter halten ausstehende Verbindungsanforderungen in einer backwarewarteschlange, bis Sie vom Server bearbeitet oder (aufgrund eines Timeouts) vom Client abgezogen werden. Ein Dienstanbieter kann Anforderungen im Hintergrund ignorieren, um die Größe der Rückstands Warteschlange über eine vom Anbieter definierte Obergrenze hinaus zu erweitern.

An diesem Punkt kann die Serverseite, wenn ein blockierender Socket verwendet wird, sofort [**wspaccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept) aufruft, der blockiert wird, bis eine Verbindungsanforderung aussteht. Umgekehrt kann der Server auch einen der zuvor beschriebenen Mechanismen zur Netzwerk Ereignisanzeige verwenden, um Benachrichtigungen über eingehende Verbindungsanforderungen anzuordnen. Je nach ausgewähltem Benachrichtigungs Mechanismus gibt der Anbieter entweder eine Windows-Meldung aus oder signalisiert ein Ereignis Objekt, wenn Verbindungsanforderungen eintreffen. Informationen zur Registrierung für das FD-Accept Network-Ereignis finden Sie unter [Benachrichtigung zu Netzwerk Ereignissen](notification-of-network-events-2.md) \_ .

Auf der Clientseite wird ein geeigneter Socket erstellt und die Verbindung initiiert, indem [**wspconnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85))aufgerufen wird und die bekannte Server Adresse angegeben wird. Clients führen in der Regel keinen expliziten [**Bindungs**](/windows/desktop/api/winsock/nf-winsock-bind) Vorgang aus, bevor Sie eine Verbindung initiieren, sodass der Dienstanbieter eine implizite Bindung in seinem Auftrag ausführen kann. Wenn sich der Socket im Blockierungs Modus befindet, wird **wspconnect** blockiert, bis der Server die Verbindungsanforderung empfangen und verarbeitet hat (oder bis ein Timeout auftritt). Andernfalls sollte der Client einen der zuvor beschriebenen Mechanismen zur Netzwerk Ereignisanzeige verwenden, um eine Benachrichtigung über eine neue Verbindung anzuordnen. Je nach ausgewähltem Benachrichtigungs Mechanismus gibt der Anbieter dies entweder über eine Windows-Meldung oder durch Signalisieren eines Ereignis Objekts an.

Wenn [**wspaccept**](/windows/desktop/api/Ws2spi/nc-ws2spi-lpwspaccept)von der Serverseite aufgerufen wird, ruft der Dienstanbieter die von der Anwendung bereitgestellte Bedingungs Funktion auf und verwendet Funktionsparameter, um die Server Informationen aus dem obersten Eintrag in der Warteschlange für Verbindungs Anforderungs Backlogs zu übergeben. Zu diesen Informationen gehören beispielsweise die Adresse der Verbindung zwischen Host, verfügbare Benutzerdaten und verfügbare QoS-Informationen. Mithilfe dieser Informationen bestimmt die Condition-Funktion des Servers, ob die Anforderung akzeptiert, abgelehnt oder die Entscheidung bis zu einem späteren Zeitpunkt zurückgesetzt werden soll. Diese Entscheidung wird durch den Rückgabewert der Condition-Funktion angegeben. Informationen zur Registrierung für das FD Connect Network-Ereignis finden Sie unter [Benachrichtigung zu Netzwerk Ereignissen](notification-of-network-events-2.md) \_ .

Wenn der Server beschließt, die Anforderung zu akzeptieren, muss der Anbieter einen neuen Socket mit allen Attributen und Ereignis Registrierungen erstellen, die dem Abhör Socket entsprechen. Der ursprüngliche Socket verbleibt im Status "lauschen", sodass nachfolgende Verbindungsanforderungen empfangen werden können. Durch Ausgabeparameter der Bedingungs Funktion kann der Server auch beliebige Benutzerdaten für die Antwort bereitstellen und QoS-Parameter zuweisen (vorausgesetzt, dass diese Vorgänge vom Dienstanbieter unterstützt werden).

 

 
