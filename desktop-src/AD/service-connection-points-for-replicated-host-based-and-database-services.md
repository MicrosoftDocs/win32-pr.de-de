---
title: Dienst Verbindungspunkte für replizierte, Host basierte und Datenbankdienste
description: Wenn Sie einen Dienst mithilfe eines Dienst Verbindungs Punkts (Service Connection Point, SCP) veröffentlichen, sollten Sie überprüfen, wie Clients den Dienst Verbindungspunkt für Ihren Dienst finden.
ms.assetid: 944e8ecd-f8ea-4506-992c-bbbfc82d11f3
ms.tgt_platform: multiple
keywords:
- Dienst Verbindungspunkte für replizierte, Host basierte und Datenbankdienste AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63b69491dd84a9367f8fd05e9d23ca771551dfbb
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038731"
---
# <a name="service-connection-points-for-replicated-host-based-and-database-services"></a>Dienst Verbindungspunkte für replizierte, Host basierte und Datenbankdienste

Wenn Sie einen Dienst mithilfe eines Dienst Verbindungs Punkts (Service Connection Point, SCP) veröffentlichen, sollten Sie überprüfen, wie Clients den Dienst Verbindungspunkt für Ihren Dienst finden. Wenn mehrere Instanzen des Diensts vorhanden sind, sollten Sie in Erwägung gezogen werden, wie Clients den Dienst mit den gewünschten Features von ähnlichen Diensten mit unterschiedlichen Funktionen unterscheiden. Wenn Sie einen replizierten Dienst veröffentlichen, sollten Sie Bedenken, wie ein Client ein Replikat auswählen soll. Dieses Thema behandelt diese Probleme für verschiedene Dienst Typen.

## <a name="replicable-services"></a>Replizierungsdienste

Bei einem replizierbaren Dienst können eine oder mehrere Instanzen oder Replikate des Dienstanbieter vorhanden sein, und Clients sind nicht darauf achten, dass das Replikat, mit dem Sie verbunden sind, den gleichen Dienst bereitstellt. Active Directory Domain Services Beispiele für replizierte Dienste: alle Domänen Controller für eine bestimmte Domäne enthalten identische Daten, unterliegen der Replikations Latenz und stellen identische Dienste bereit.

Replizierungsdienste können SCPs und andere Dienst spezifische Objekte für mehrere Replikate in einem einzelnen Container speichern. Die Setup Anwendung für das erste Replikat kann den Container als untergeordnetes Element des System Containers der lokalen Domäne erstellen. Weitere Informationen finden Sie unter [Veröffentlichen in einem Domänen System Container](publishing-in-a-domain-system-container.md). Stellen Sie sicher, dass die Sicherheits Beschreibung für den Container es den Setup Programmen für nachfolgende Replikate ermöglicht, Ihre Objekte im gleichen Container zu erstellen. Erteilen Sie Berechtigungen für den Installations Administrator, um die Benutzer oder Gruppen anzugeben, die Objekte im Container erstellen oder ändern können.

Eine Strategie für einen replizierbaren Dienst besteht darin, einen Dienst Verbindungspunkt für jedes Replikat zu erstellen. Wenn ein Client nach der Produkt-GUID oder einem anderen identifizierenden Schlüsselwort fragt, sucht es nach den SCP-Objekten für alle Replikate und wählt eine nach dem Zufallsprinzip oder mithilfe eines Lasten Ausgleichs Algorithmus aus. Ein Administrator kann z. b. für jedes Replikat, ähnlich den Feldern Priorität und Gewichtung eines DNS-SRV-Einsatzes, Prioritäts-und Lasten Ausgleichs Daten angeben. Die Setup Anwendung des Dienstanbieter kann diese Daten im **serviceBindingInformation** -Attribut jedes Replikat-Dienst Prinzipals speichern. Clients rufen die Daten von jedem SCP ab und verwenden Sie zum Auswählen eines Replikats.

Eine andere Strategie ist die Erstellung eines einzelnen Dienst Verbindungs Punkts für alle Replikate und das Festlegen des SCP **servicednsname** -Attributs auf den Namen eines DNS-SRV-Einsatzes. Anschließend registriert die Setup Anwendung für jedes Replikat einen SRV-Datensatz mit diesem Namen. Wenn ein Client den Lone SCP des dienstanders identifiziert, ruft der Client den Namen des SRV-Eintrags ab und verwendet die [**DNSQuery**](/windows/desktop/api/windns/nf-windns-dnsquery_a) -Funktion, um das Array der SRV-Einträge für die Replikate abzurufen. Jeder SRV-Datensatz enthält den Namen eines Host Computers und zusätzliche Daten, die der Client zum Auswählen eines Replikats verwenden kann.

## <a name="database-services"></a>Datenbankdienste

Unterschiedliche Instanzen eines Daten Bank Dienstanbieter enthalten möglicherweise ganz andere Daten, auch wenn es sich um dieselbe Art von Dienst handelt, die in der Regel als Dienstklasse bezeichnet wird. Um diese Art von Dienst zu veröffentlichen, kann das **Keywords** -Attribut des Dienst Verbindungs Punkts sowohl die Dienstklasse als auch die bestimmte Datenbank identifizieren. Ein allgemeiner Client, der nur die GUID der Dienstklasse kennt, kann Abfragen für alle Datenbanken durch diese Dienstklasse durchsuchen und dann eine Benutzeroberfläche präsentieren, die dem Benutzer ermöglicht, einen auszuwählen. Für einen Client, der speziell für die Zieldatenbank entworfen wurde, können Sie die Datenbank-GUID im Client Code hart codieren.

## <a name="host-based-services"></a>Host basierte Dienste

Host basierte Dienste sind Dienste, die eng an einen einzelnen Host Computer gebunden sind. Sie können Instanzen der Dienstklasse auf vielen Computern installieren, und jede Instanz bietet Dienste, die mit Ihrem Host Computer identifiziert werden.

Jede Instanz eines Host basierten Diensts sollte einen eigenen Dienst Verbindungspunkt unter dem Computer Objekt des Hosts erstellen. Clients, die eine Produkt-GUID für die Suche nach dem SCP eines Host basierten Diensts verwenden, finden in der Regel viele Instanzen der Dienstklasse in der gesamten Unternehmens Gesamtstruktur. Clients können dann das **servicednsname** -Attribut der SCPs verwenden, um den Dienst Verbindungspunkt für die Dienst Instanz auf dem gewünschten Host Computer zu finden.

 

 