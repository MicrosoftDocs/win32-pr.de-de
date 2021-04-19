---
description: Es werden bereit Stellungen zum Erweitern von Konstanten und Strukturen auf geräteunabhängige Weise und in Geräte spezifischer (Hersteller spezifischer) Art und Weise vorgenommen.
ms.assetid: d30f80c3-3535-4d78-b0a1-c9a7389f8fd4
title: Erweiterbarkeit von Strukturen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b00fcf80b1ecfb7cc4d31b9ff040b101707ae236
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355429"
---
# <a name="structure-extensibility"></a>Erweiterbarkeit von Strukturen

Es werden bereit Stellungen zum Erweitern von Konstanten und Strukturen auf geräteunabhängige Weise und in Geräte spezifischer (Hersteller spezifischer) Art und Weise vorgenommen.

In Konstanten, bei denen es sich um skalare Enumerationen handelt, ist ein Wertebereich für zukünftige allgemeine Erweiterungen reserviert. Der Rest der Werte wird als gerätespezifisch identifiziert. Ein Anbieter kann Bedeutungen für diese Werte in beliebiger Weise definieren. Die Interpretation dieser Werte ist an den *Erweiterungs Bezeichner* gebunden, der über die [**linedevcaps**](/windows/win32/api/tapi/ns-tapi-linedevcaps) -Datenstruktur bereitgestellt wird. Bei Konstanten, die als Bitflags definiert sind, ist ein Bereich von Bits mit niedriger Ordnung reserviert, wobei die höherwertigen Bits Erweiterungs spezifisch sein können. Es wird empfohlen, dass erweiterte Werte und Bitarrays Bits aus dem höchsten Wert oder dem großen Bit nach unten verwenden. Dadurch bleibt die Option zum Verschieben des Rahmens zwischen dem gemeinsamen Teil und dem Erweiterungs Teil bestehen, wenn dies in Zukunft erforderlich ist. Erweiterungen zu Datenstrukturen werden einem Feld mit variabler Größe zugewiesen, wobei Größe/Offset Teil des fixierten Teils ist. TSPI beschreibt für jede Datenstruktur, welche gerätespezifischen Erweiterungen zulässig sind.

Zusätzlich zum Erkennen eines bestimmten Erweiterungs Bezeichners muss TAPI (im Auftrag einer Anwendung) die Erweiterungs Versionsnummer aushandeln, unter der die Anwendung und der Dienstanbieter betrieben werden. Dies erfolgt mithilfe der [**TSPI- \_ linenegotiateextversion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) -und [**TSPI- \_ phonenegotiateextversion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) -Funktionen.

Ein Erweiterungs Bezeichner ist eine Globally Unique Identifier. Es gibt keine zentrale Registrierung für Erweiterungs-IDs. Stattdessen werden Sie vom Hersteller lokal durch ein Dienstprogramm generiert, das im Toolkit verfügbar ist. Die Zahl besteht aus Teilen, wie z. b. einer (eindeutigen) LAN-Adresse, Tageszeit und Zufallszahl, um globale Eindeutigkeit sicherzustellen. Global eindeutige Bezeichner sind so konzipiert, dass Sie von allgemein eindeutigen HP/Dec-bezeichnerbezeichnerbezeichnerunter schieden werden und somit vollständig kompatibel sind.

 

 
