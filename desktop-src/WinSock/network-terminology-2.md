---
description: Metriken werden verwendet, um Aspekte der Netzwerk-und Protokoll Leistung zu messen.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Netzwerkterminologie (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b04e84621cdaec2638762d54f67e5aca7e3d55ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103751417"
---
# <a name="network-terminology-windows-sockets-2"></a>Netzwerkterminologie (Windows Sockets 2)

Metriken werden verwendet, um Aspekte der Netzwerk-und Protokoll Leistung zu messen. Die Werte für solche Metriken in verschiedenen Szenarien geben die Leistungs Ebene einer Netzwerk Anwendung an. In diesem Abschnitt werden Begriffe und Metriken definiert, die branchenweit zum Messen der Leistung von Netzwerkanwendungen verwendet werden. Diese Begriffe werden im weiteren Verlauf dieses Handbuchs verwendet.

-   Roundtripzeit (RTT)

    Zeit (in Millisekunden) für eine Anforderung, eine Fahrt von einem Quellcomputer zu einem Zielcomputer durchführen zu können, und wieder zurück. Niedrigere Werte weisen auf eine bessere Leistung hin. Vorwärts-und Rückgabe Pfad Zeiten sind nicht notwendigerweise gleich.

    RTT-Werte sind von der Netzwerkinfrastruktur, der Entfernung zwischen Knoten, den Netzwerkbedingungen und der Paketgröße betroffen. Die Paketgröße, die Überlastung und die Nutzlast der Nutzlast beeinflussen RTT, wenn Sie auf langsamen Verknüpfungen wie DFÜ-Verbindungen gemessen werden. Andere Faktoren wirken sich auf RTT aus, einschließlich der Forward-Fehlerkorrektur und der Datenkomprimierung, durch die Puffer und Warteschlangen eingeführt werden, die RTT erhöhen

-   Goodput

    Das Measure der nützlichen Anwendungsdaten, die vom Empfänger erfolgreich verarbeitet wurden (in Bits pro Sekunde). Goodput ermöglicht die Messung des effektiven oder nützlichen Durchsatzes und umfasst nur Anwendungsdaten. Paket-, Protokoll-und Medien Header werden als mehr Aufwand angesehen und sind nicht Teil von goodput.

-   Protokoll Aufwand

    Nicht Anwendungs bytes, einschließlich Protokoll und Medien Rahmen, dividiert durch die Gesamtzahl der übertragenen Bytes. Der Wert wird als Prozentsatz ausgedrückt. Höhere Werte weisen auf eine schlechtere Leistung hin.

    Der Aufwand wird in diesem Handbuch für beide Richtungen berechnet, kann jedoch für jede Richtung separat berechnet werden.

-   Bandwidth-Delay Produkt

    Produkt der Bits-pro-Sekunde-Bandbreite des Netzwerks und RTT (in Sekunden). Dieser Wert entspricht der Anzahl von Bits, die benötigt wird, um die verfügbare Netzwerkbandbreite auszufüllen. Wenn der Wert für das Produkt "Bandbreiten Verzögerung" hoch ist, muss der TCP/IP-Stapel große Mengen nicht bestätigter Daten verarbeiten, um die Pipeline vollständig zu halten. Das Produkt für die Bandbreiten Verzögerung ist eine zentrale End-to-End-Metrik für Streaminganwendungen.

 

 



