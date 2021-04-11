---
description: Es werden bereit Stellungen zum Erweitern von Konstanten und Strukturen auf geräteunabhängige Weise und in Geräte spezifischer (Hersteller spezifischer) Art und Weise vorgenommen.
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: Erweiterbarkeit (telefonieapi)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ca446a03a9bdbe6d906e7accf261645401cd937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215993"
---
# <a name="extensibility"></a>Erweiterungen

Es werden bereit Stellungen zum Erweitern von Konstanten und Strukturen auf geräteunabhängige Weise und in Geräte spezifischer (Hersteller spezifischer) Art und Weise vorgenommen. In Konstanten, bei denen es sich um skalare Enumerationen handelt, ist ein Wertebereich für zukünftige allgemeine Erweiterungen reserviert. Die restlichen Werte werden als gerätespezifisch identifiziert. Ein Anbieter kann Bedeutungen für diese Werte in beliebiger Weise definieren. Die Interpretation wird an den *Erweiterungs Bezeichner* in der Datenstruktur [**linedevcaps**](/windows/win32/api/tapi/ns-tapi-linedevcaps) gebunden. Bei Konstanten, die als Bitflags definiert sind, ist ein Bereich von Bits mit niedriger Ordnung reserviert, wobei die höherwertigen Bits Erweiterungs spezifisch sein können. Es wird empfohlen, dass erweiterte Werte und Bitarrays Bits aus dem höchsten Wert oder dem großen Bit nach unten verwenden. Dadurch bleibt die Option zum Verschieben des Rahmens zwischen dem gemeinsamen Teil und dem Erweiterungs Teil bestehen, wenn dies in der Zukunft erforderlich ist. Erweiterungen zu Datenstrukturen werden einem Feld mit variabler Größe zugewiesen, wobei Größe/Offset Teil des fixierten Teils ist. TAPI beschreibt für jede Datenstruktur, welche gerätespezifischen Erweiterungen zulässig sind.

Zusätzlich zum Erkennen eines bestimmten Erweiterungs Bezeichners muss die Anwendung die Erweiterungs Versionsnummer aushandeln, unter der die Anwendung und der Dienstanbieter betrieben werden. Dies erfolgt in der zweiten Versions Aushandlungs Phase der [**linegetdevcaps**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps) -Funktion.

Ein Erweiterungs Bezeichner ist eine Globally Unique Identifier. Es gibt keine zentrale Registrierung für Erweiterungs-IDs. Stattdessen werden Sie vom Hersteller lokal durch ein Dienstprogramm generiert, das im Toolkit verfügbar ist. Die Anzahl besteht aus Teilen, wie z. b. einer eindeutigen LAN-Adresse, Tageszeit und Zufallszahl, um globale Eindeutigkeit sicherzustellen. Global eindeutige Bezeichner sind so konzipiert, dass Sie von allgemein eindeutigen HP/Dec-bezeichnerbezeichnerbezeichnerunter schieden werden und somit vollständig kompatibel sind.

 

 
