---
description: Erfahren Sie mehr über die konstante Erweiterbarkeit. Es werden Sowohl geräteunabhängige als auch gerätespezifische Erweiterungen von Konstanten und Strukturen vorgenommen.
ms.assetid: 78430503-3e1f-49ab-be9c-d48bd21a840e
title: Konstante Erweiterbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 975d2901dcc3f7e574ffdacdabbcf457821ef932
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409973"
---
# <a name="constant-extensibility"></a>Konstante Erweiterbarkeit

Die Erweiterung von Konstanten und Strukturen wird sowohl geräteunabhängig als auch gerätespezifisch (herstellerspezifisch) bereitgestellt.

In Konstanten, bei denen es sich um skalare Enumerationen handelt, ist ein Wertebereich für zukünftige allgemeine Erweiterungen reserviert. Der Rest der Werte wird als gerätespezifisch identifiziert. Ein Anbieter kann Bedeutungen für diese Werte in beliebiger Weise definieren. Die Interpretation dieser Werte wird mit der Erweiterungs-ID in der [**LINEDEVCAPS-Datenstruktur**](/windows/win32/api/tapi/ns-tapi-linedevcaps) angegeben. Für Konstanten, die als Bitflags definiert sind, ist ein Bereich von low-order-Bits reserviert, wobei die hohen Bits erweiterungsspezifisch sein können. Es wird empfohlen, dass erweiterte Werte und Bitarrays Bits des höchsten Werts oder eines hohen Bitwerts nach unten verwenden. Dadurch bleibt die Option, den Rahmen zwischen dem gemeinsamen Teil und dem Erweiterungsteil zu verschieben, falls dies in Zukunft erforderlich ist. Erweiterungen für Datenstrukturen werden einem Feld mit unterschiedlicher Größe zugewiesen, bei dem Größe/Offset Teil des festen Teils ist. TSPI beschreibt, welche gerätespezifischen Erweiterungen für jede Datenstruktur zulässig sind. Weitere Informationen finden Sie im Thema [Speicherzuordnung.](./memory-allocation.md)

Zusätzlich zur Erkennung eines bestimmten Erweiterungsbezeichners muss TAPI (im Auftrag einer Anwendung) die Versionsnummer der Erweiterung aushandeln, unter der die Anwendung und der Dienstanbieter arbeiten. Dies erfolgt mithilfe der [**Funktionen TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) und [**TSPI \_ phoneNegotiateExtVersion.**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion)

Ein Erweiterungsbezeichner ist ein global eindeutiger Bezeichner. Es gibt keine zentrale Registrierung für Erweiterungsbezeichner. Stattdessen werden sie lokal vom Hersteller durch ein Hilfsprogramm generiert, das mit dem Toolkit verfügbar ist. Um die globale Eindeutigkeit zu gewährleisten, besteht die Zahl aus Teilen wie einer (eindeutigen) LAN-Adresse, Tageszeit und einer Zufallszahl. Global eindeutige Bezeichner sind so konzipiert, dass sie von universell eindeutigen HP/DEC-Bezeichnern unterschieden werden können und daher vollständig kompatibel sind.

 

 
