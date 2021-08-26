---
description: Das lokale Zwischenspeichern von Daten ist eine Technik, die verwendet wird, um den Netzwerkzugriff auf Datendateien zu beschleunigen. Dies umfasst nach Möglichkeit das Zwischenspeichern von Daten auf Clients und nicht auf Servern.
ms.assetid: a7eb24b3-7e23-4798-8584-30a171fa4f04
title: Lokales Zwischenspeichern
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f9d60fa71274bfcbf559ff57a3ab1a6fceba13d47315d80d9c3722a2a206b611
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119927620"
---
# <a name="local-caching"></a>Lokales Zwischenspeichern

*Das lokale Zwischenspeichern* von Daten ist eine Technik, die verwendet wird, um den Netzwerkzugriff auf Datendateien zu beschleunigen. Dies umfasst nach Möglichkeit das Zwischenspeichern von Daten auf Clients und nicht auf Servern.

Der Effekt der lokalen Zwischenspeicherung besteht in der Möglichkeit, mehrere Schreibvorgänge für den gleichen Bereich einer Datei zu einem Schreibvorgang im gesamten Netzwerk zu kombinieren. Die lokale Zwischenspeicherung reduziert den Netzwerkdatenverkehr, da die Daten einmal geschrieben werden. Diese Zwischenspeicherung verbessert die offensichtliche Antwortzeit von Anwendungen, da die Anwendungen nicht warten, bis die Daten über das Netzwerk an den Server gesendet werden.

Das lokale Zwischenspeichern der zu lesenden Daten kann dazu erscheinen, die Dinge durch Vorlesen zu beschleunigen. Ein einfaches Beispiel ist eine Anwendung, die sequenziell auf Daten zugreift, z. B. der Präprozessor eines Compilers. In solchen Fällen liest die Netzwerkschicht des Betriebssystems Daten über das Netzwerk, bevor die Anwendung die Daten anfing. Im Idealfall übermittelt das Netzwerk die Daten, bevor die Anwendung sie vom Dateisystem angibt, was zu einer nahezu sofortigen Antwort führt. In der Praxis geschieht dies selten, aber häufig beschleunigt das Lesen von Vorauslesen Anwendungen, indem die nächste Anforderung erwartet wird.

Die lokale Zwischenspeicherung kann auch dazu beitragen, den Netzwerkdatenverkehr zu reduzieren, indem ein Teil einer Datei einmal im Netzwerk gelesen und dann im lokalen Cache gespeichert wird. Nachfolgende Lesevorgänge für diesen Teil, die von der Anwendung aus dem lokalen Cache gelesen werden.

Eine Art von Anwendung, die von der lokalen Zwischenspeicherung profitieren kann, sind Batchdateien. Befehlsprozessoren lesen eine Batchdatei zeilenweise und führen sie aus. Für jede Zeile öffnet der Befehlsprozessor die Datei, sucht bis zum Anfang der Zeile, liest so viel wie sie benötigt, schließt die Datei und führt dann die Zeile aus. Jede Zeile führt zu viel Netzwerkdatenverkehr. Der Netzwerkdatenverkehr kann erheblich reduziert werden, indem die gesamte Batchdatei auf einem Client zwischenspeichert wird.

Die lokale Zwischenspeicherung hilft auch bei einem anderen Problem im Zusammenhang mit Netzwerken, insbesondere bei Netzwerken, die Arbeit über Modems und andere Thin Pipes durchführen: langsame Antwortzeit. Benutzer möchten nicht warten, während Daten über das Netzwerk abgerufen, geändert und dann zurückgeschrieben werden. Beim Vorlesen und dem Zwischenspeichern von Schreibzugriffen scheint es oft so, als ob diese Funktionen viel schneller funktionieren als tatsächlich.

Eine Gefahr der lokalen Zwischenspeicherung ist, dass geschriebene Daten nur so viel Integrität wie der Client selbst haben, solange die Daten auf dem Client zwischengespeichert werden. Im Allgemeinen sollten lokal zwischengespeicherte Daten so schnell wie möglich auf den Server geleert werden. Mit modernen Betriebssystemen und Hardwareunterstützung wie unterbrechungsfreie Stromversorgungen verringert sich das Risiko, lokal zwischengespeicherte Daten zu verlieren. Das Risiko besteht jedoch weiterhin, und Sie sollten sowohl den Abwäge zwischen Datenintegrität und offensichtlicher Reaktionsgeschwindigkeit als auch den Abwäge zwischen Datenintegrität und geringerem Netzwerkdatenverkehr berücksichtigen.

 

 



