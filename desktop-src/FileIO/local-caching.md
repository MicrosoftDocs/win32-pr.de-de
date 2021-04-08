---
description: Das lokale Zwischenspeichern von Daten ist eine Technik, mit der der Netzwerk Zugriff auf Datendateien beschleunigt werden kann. Dies umfasst das Zwischenspeichern von Daten auf Clients und nicht auf Servern, wenn dies möglich ist.
ms.assetid: a7eb24b3-7e23-4798-8584-30a171fa4f04
title: Lokales Caching
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c8132bc51831db752422de1e3071ee3ef0b33a1b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868235"
---
# <a name="local-caching"></a>Lokales Caching

Das *lokale Zwischenspeichern* von Daten ist eine Technik, mit der der Netzwerk Zugriff auf Datendateien beschleunigt werden kann. Dies umfasst das Zwischenspeichern von Daten auf Clients und nicht auf Servern, wenn dies möglich ist.

Die Auswirkung der lokalen Zwischenspeicherung besteht darin, dass mehrere Schreibvorgänge in derselben Region einer Datei in einem Schreibvorgang über das Netzwerk kombiniert werden können. Das lokale Zwischenspeichern reduziert den Netzwerkverkehr, da die Daten einmal geschrieben werden. Diese Zwischenspeicherung verbessert die offensichtliche Reaktionszeit von Anwendungen, da die Anwendungen nicht darauf warten, dass die Daten über das Netzwerk an den Server gesendet werden.

Das lokale Zwischenspeichern von Daten, die gelesen werden sollen, kann mit Lesevorgängen beschleunigt werden. Ein einfaches Beispiel ist eine Anwendung, die sequenziell auf Daten zugreift, z. b. den Präprozessor eines Compilers. In solchen Fällen liest die Netzwerkschicht des Betriebssystems Daten über das Netzwerk, bevor die Anwendung die Daten anfordert. Im Idealfall stellt das Netzwerk die Daten bereit, bevor Sie von der Anwendung aus dem Dateisystem angefordert werden, was zu einer nahezu sofortigen Reaktion führt. In der Praxis kommt dies selten vor, aber häufig beschleunigt das Lesen der Anwendungen, indem die nächste Anforderung erwartet wird.

Das lokale Zwischenspeichern kann auch dazu beitragen, den Netzwerk Datenverkehr zu verringern, indem ein Teil einer Datei im Netzwerk einmal gelesen und dann im lokalen Cache aufbewahrt wird. Nachfolgende Lesevorgänge für diesen Teil durch die Anwendung, die aus dem lokalen Cache gelesen wird.

Ein Anwendungstyp, der vom lokalen Caching profitieren kann, sind Batch Dateien. Befehls Prozessoren lesen und führen eine Batchdatei nacheinander aus. Für jede Zeile öffnet der Befehlsprozessor die Datei, sucht bis zum Anfang der Zeile, liest so viele Anforderungen, schließt die Datei und führt dann die Zeile aus. Jede Zeile ergibt viel Netzwerk Datenverkehr. Der Netzwerk Datenverkehr kann durch Zwischenspeichern der gesamten Batchdatei auf einem Client erheblich reduziert werden.

Die lokale Zwischenspeicherung hilft auch bei anderen Problemen, die mit Netzwerken verbunden sind, insbesondere bei Netzwerken, die über Modems und andere Thin Pipes arbeiten: langsame Reaktionszeit. Benutzer möchten nicht warten, bis die Daten über das Netzwerk abgerufen, geändert und dann zurückgeschrieben wurden. Durch das Lesen vor und das Schreiben Zwischenspeichern scheint es häufig, dass diese Funktionen viel schneller funktionieren, als Sie tatsächlich tun.

Eine Gefahr von lokalem Caching besteht darin, dass geschriebene Daten nur so viel Integrität wie der Client selbst aufweisen, solange die Daten auf dem Client zwischengespeichert werden. Im Allgemeinen sollten lokal zwischengespeicherte Daten so bald wie möglich auf den Server geleert werden. Mit modernen Betriebssystemen und Hardwareunterstützung, wie z. b. unterbrechungsfreie Stromversorgungen, verringert sich das Risiko, dass lokal zwischengespeicherte Daten verloren gehen. Das Risiko ist jedoch weiterhin vorhanden, und Sie sollten sowohl den Kompromiss zwischen Datenintegrität und offensichtlich Reaktionsgeschwindigkeit und den Kompromiss zwischen Datenintegrität und reduziertem Netzwerkverkehr berücksichtigen.

 

 



