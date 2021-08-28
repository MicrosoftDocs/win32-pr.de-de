---
title: Dienstverbindungspunkte für replizierte, hostbasierte und Datenbankdienste
description: Wenn Sie einen Dienst mithilfe eines Dienstverbindungspunkts (Service Connection Point, SCP) veröffentlichen, überlegen Sie, wie Clients den SCP für Ihren Dienst finden.
ms.assetid: 944e8ecd-f8ea-4506-992c-bbbfc82d11f3
ms.tgt_platform: multiple
keywords:
- Dienstverbindungspunkte für replizierte, hostbasierte und Database Services AD-Dienste
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a7658cc60704dbfc37009272e5f14f997d213ea993054fa22c1c5e0c307794b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119024898"
---
# <a name="service-connection-points-for-replicated-host-based-and-database-services"></a>Dienstverbindungspunkte für replizierte, hostbasierte und Datenbankdienste

Wenn Sie einen Dienst mithilfe eines Dienstverbindungspunkts (Service Connection Point, SCP) veröffentlichen, überlegen Sie, wie Clients den SCP für Ihren Dienst finden. Wenn mehrere Instanzen des Diensts vorhanden sind, überlegen Sie, wie Clients den Dienst mit den gewünschten Features von ähnlichen Diensten mit unterschiedlichen Features unterscheiden. Wenn Sie einen replizierten Dienst veröffentlichen, überlegen Sie, wie ein Client ein Replikat auswählt. In diesem Thema werden diese Probleme für verschiedene Arten von Diensten erläutert.

## <a name="replicable-services"></a>Replizieren von Diensten

Für einen replizierbaren Dienst kann es eine oder mehrere Instanzen oder Replikate des Diensts geben, und clients ist es nicht wichtig, mit welchem Replikat sie eine Verbindung herstellen, da jede denselben Dienst bietet. Active Directory Domain Services sind Beispiele für replizierte Dienste: Alle Domänencontroller für eine bestimmte Domäne enthalten identische Daten, unterliegen der Replikationslatenz und stellen identische Dienste zur Verfügung.

Replizieren von Diensten kann die SCPs und andere dienstspezifische Objekte für mehrere Replikate in einem einzelnen Container speichern. Die Setupanwendung für das erste Replikat kann den Container als untergeordnetes Replikat des Systemcontainers der lokalen Domäne erstellen. Weitere Informationen finden Sie unter [Veröffentlichen in einem Domänensystemcontainer.](publishing-in-a-domain-system-container.md) Stellen Sie sicher, dass die Sicherheitsbeschreibung für Ihren Container es den Setupprogrammen für nachfolgende Replikate ermöglicht, ihre Objekte im gleichen Container zu erstellen. Erteilen Sie dem installierenden Administrator Berechtigungen, um die Benutzer oder Gruppen anzugeben, die Objekte im Container erstellen oder ändern können.

Eine Strategie für einen replizierbaren Dienst besteht in der Erstellung eines SCP für jedes Replikat. Wenn ein Client die Produkt-GUID oder ein anderes identifizierende Schlüsselwort des Diensts abfragt, findet er die SCP-Objekte für alle Replikate und wählt eines nach dem Zufallsprinzip oder mithilfe eines Lastenausgleichsalgorithmus aus. Beispielsweise könnte ein Administrator Prioritäts- und Lastenausgleichsdaten für jedes Replikat angeben, ähnlich den Prioritäts- und Gewichtungsfeldern eines DNS-SRV-Eintrags. Die Setupanwendung des Diensts kann diese Daten im **serviceBindingInformation-Attribut** des SCP jedes Replikats speichern. Clients rufen die Daten von jedem SCP ab und verwenden sie, um ein Replikat auszuwählen.

Eine weitere Strategie besteht in der Erstellung eines einzelnen SCP für alle Replikate und dem Festlegen des SCP **serviceDNSName-Attributs** auf den Namen eines DNS-SRV-Eintrags. Anschließend registriert die Setupanwendung für jedes Replikat einen SRV-Eintrag mit diesem Namen. Wenn ein Client den 1. SCP des Diensts identifiziert, ruft der Client den Namen des SRV-Eintrags ab und verwendet die [**DnsQuery-Funktion,**](/windows/desktop/api/windns/nf-windns-dnsquery_a) um das Array von SRV-Einträgen für die Replikate abzurufen. Jeder SRV-Eintrag enthält den Namen eines Hostcomputers und zusätzliche Daten, die der Client zum Auswählen eines Replikats verwenden kann.

## <a name="database-services"></a>Datenbankdienste

Unterschiedliche Instanzen eines Datenbankdiensts können völlig unterschiedliche Daten enthalten, obwohl sie alle dieselbe Art von Dienst sind, die in der Regel als Dienstklasse bezeichnet wird. Um diese Art von  Dienst zu veröffentlichen, kann das Schlüsselwortattribut des SCP sowohl die Dienstklasse als auch die spezifische Datenbank identifizieren. Ein allgemeiner Client, der nur die GUID der Dienstklasse kennt, kann alle von dieser Dienstklasse veröffentlichten Datenbanken abfragen und dann eine Benutzeroberfläche präsentieren, damit der Benutzer eine auswählen kann. Für einen Client, der speziell für die Zieldatenbank entwickelt wurde, können Sie die Datenbank-GUID hart im Clientcode codieren.

## <a name="host-based-services"></a>Hostbasierte Dienste

Hostbasierte Dienste sind Dienste, die eng an einen einzelnen Hostcomputer gebunden sind. Sie können Instanzen der Dienstklasse auf vielen Computern installieren, und jede Instanz stellt Dienste zur Verfügung, die mit ihrem Hostcomputer identifiziert werden.

Jede Instanz eines hostbasierten Diensts sollte einen eigenen SCP unter dem Computerobjekt seines Hosts erstellen. Clients, die eine Produkt-GUID verwenden, um nach dem SCP eines hostbasierten Diensts zu suchen, finden in der Regel viele Instanzen der Dienstklasse in der gesamten Unternehmensgestruktur. Clients können dann das **serviceDNSName-Attribut** der SCPs verwenden, um den SCP für die Dienstinstanz auf dem gewünschten Hostcomputer zu finden.

 

 