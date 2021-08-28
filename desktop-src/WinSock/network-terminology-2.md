---
description: Metriken werden verwendet, um Aspekte der Netzwerk- und Protokollleistung zu messen.
ms.assetid: ee5faaf6-e230-4084-9829-e8cae8759587
title: Netzwerkterminologie (Windows Sockets 2)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a3d0c5fc67932b5c756ae52b9a7ffefef0f18c2728f2b2773de3741d0e5b7d41
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119794770"
---
# <a name="network-terminology-windows-sockets-2"></a>Netzwerkterminologie (Windows Sockets 2)

Metriken werden verwendet, um Aspekte der Netzwerk- und Protokollleistung zu messen. Die Werte für solche Metriken in verschiedenen Szenarien geben die Leistungsstufe einer Netzwerkanwendung an. In diesem Abschnitt werden Begriffe und Metriken definiert, die branchenweit zum Messen der Leistung von Netzwerkanwendung verwendet werden. Diese Begriffe werden im restlichen Teil dieses Handbuchs verwendet.

-   Roundtripzeit (RTT)

    Zeit in Millisekunden für eine Anforderung, eine Fahrt von einem Quellcomputer zu einem Zielcomputer und wieder zurück zu unternehmen. Niedrigere Werte weisen auf eine bessere Leistung hin. Vorwärts- und Rückgabepfadzeiten sind nicht unbedingt gleich.

    RTT-Werte werden von der Netzwerkinfrastruktur, der Entfernung zwischen Knoten, den Netzwerkbedingungen und der Paketgröße beeinflusst. Paketgröße, Überlastung und Nutzlastkomprimierung wirken sich auf rtt aus, wenn sie an langsamen Links gemessen werden, z. B. DFÜ-Verbindungen. Andere Faktoren wirken sich auf rtt aus, z. B. Forward-Fehlerkorrektur und Datenkomprimierung, die Puffer und Warteschlangen einführen, die RTT erhöhen und somit die Leistung verringern.

-   Goodput

    Maß für nützliche Anwendungsdaten, die vom Empfänger erfolgreich verarbeitet wurden (in Bits pro Sekunde). Goodput ermöglicht die Messung des effektiven oder nützlichen Durchsatzes und schließt nur Anwendungsdaten ein. Paket-, Protokoll- und Medienheader werden als Mehraufwand betrachtet und sind nicht Teil von Goodput.

-   Protokollaufwand

    Bytes ohne Anwendung, einschließlich Protokoll- und Medienrahmen, dividiert durch die Gesamtzahl der übertragenen Bytes. Der Wert wird als Prozentsatz ausgedrückt. Höhere Werte weisen auf eine schlechtere Leistung hin.

    Der Mehraufwand wird für beide Richtungen in dieser Anleitung berechnet, kann jedoch für jede Richtung separat berechnet werden.

-   Bandwidth-Delay Produkt

    Produkt der Bits-pro-Sekunde-Bandbreite des Netzwerks und der RTT (in Sekunden). Dieser Wert entspricht der Anzahl von Bits, die zum Füllen der verfügbaren Netzwerkbandbreite benötigt werden. Wenn der Wert für das Produkt bandbreitenverzögerung hoch ist, muss der TCP/IP-Stapel große Mengen nicht bekannter Daten verarbeiten, um die Pipeline voll zu halten. Das Produkt bandbreitenverzögerung ist eine wichtige End-to-End-Metrik für Streaminganwendungen.

 

 



