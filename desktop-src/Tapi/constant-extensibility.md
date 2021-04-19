---
description: Es werden bereit Stellungen zum Erweitern von Konstanten und Strukturen auf geräteunabhängige Weise und in Geräte spezifischer (Hersteller spezifischer) Art und Weise vorgenommen.
ms.assetid: 78430503-3e1f-49ab-be9c-d48bd21a840e
title: Konstante Erweiterbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a470ccb52af1bdc92596ac42bbafb74d4821db1e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347003"
---
# <a name="constant-extensibility"></a>Konstante Erweiterbarkeit

Es werden bereit Stellungen zum Erweitern von Konstanten und Strukturen auf geräteunabhängige Weise und in Geräte spezifischer (Hersteller spezifischer) Art und Weise vorgenommen.

In Konstanten, bei denen es sich um skalare Enumerationen handelt, ist ein Wertebereich für zukünftige allgemeine Erweiterungen reserviert. Der Rest der Werte wird als gerätespezifisch identifiziert. Ein Anbieter kann Bedeutungen für diese Werte in beliebiger Weise definieren. Die Interpretation dieser Werte ist an die Erweiterungs-ID gebunden, die durch die [**linedevcaps**](/windows/win32/api/tapi/ns-tapi-linedevcaps) -Datenstruktur bereitgestellt wird. Bei Konstanten, die als Bitflags definiert sind, ist ein Bereich von Bits mit niedriger Ordnung reserviert, wobei die höherwertigen Bits Erweiterungs spezifisch sein können. Es wird empfohlen, dass erweiterte Werte und Bitarrays Bits aus dem höchsten Wert oder dem großen Bit nach unten verwenden. Dadurch ist es nicht mehr möglich, den Rahmen zwischen dem allgemeinen Teil und dem Erweiterungs Teil zu verschieben, wenn dies in Zukunft notwendig ist. Erweiterungen zu Datenstrukturen werden einem Feld mit variabler Größe zugewiesen, wobei Größe/Offset Teil des fixierten Teils ist. TSPI beschreibt, welche gerätespezifischen Erweiterungen für jede Datenstruktur zulässig sind. Weitere Informationen finden Sie im Thema zur [Speicher Belegung](./memory-allocation.md) .

Zusätzlich zum Erkennen eines bestimmten Erweiterungs Bezeichners muss TAPI (im Auftrag einer Anwendung) die Erweiterungs Versionsnummer aushandeln, unter der die Anwendung und der Dienstanbieter arbeiten. Dies erfolgt mithilfe der [**TSPI- \_ linenegotiateextversion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) -und [**TSPI- \_ phonenegotiateextversion**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion) -Funktionen.

Ein Erweiterungs Bezeichner ist eine Globally Unique Identifier. Es gibt keine zentrale Registrierung für Erweiterungs-IDs. Stattdessen werden Sie vom Hersteller lokal durch ein Dienstprogramm generiert, das im Toolkit verfügbar ist. Um globale Eindeutigkeit zu gewährleisten, besteht die Zahl aus Teilen, wie z. b. einer (eindeutigen) LAN-Adresse, Tageszeit und einer Zufallszahl. Global eindeutige Bezeichner sind so konzipiert, dass Sie von allgemein eindeutigen HP/Dec-bezeichnerbezeichnerbezeichnerunter schieden werden und somit vollständig kompatibel sind.

 

 
