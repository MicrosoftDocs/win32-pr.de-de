---
description: Erfahren Sie mehr über Erweiterbarkeit. Es werden Sowohl geräteunabhängige als auch gerätespezifische Erweiterungen von Konstanten und Strukturen bereitgestellt.
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: Erweiterbarkeit (Telefonie-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f29ad34b5156bdd652ab6b6f8901be7a2341bdc
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406563"
---
# <a name="extensibility"></a>Erweiterungen

Die Erweiterung von Konstanten und Strukturen wird sowohl geräteunabhängig als auch gerätespezifisch (herstellerspezifisch) bereitgestellt. In Konstanten, bei denen es sich um skalare Enumerationen handelt, ist ein Wertebereich für zukünftige allgemeine Erweiterungen reserviert. Die restlichen Werte werden als gerätespezifisch identifiziert. Ein Anbieter kann Bedeutungen für diese Werte auf beliebige Weise definieren. Ihre Interpretation wird auf den *Erweiterungsbezeichner* in der [**LINEDEVCAPS-Datenstruktur**](/windows/win32/api/tapi/ns-tapi-linedevcaps) basiert. Für Konstanten, die als Bitflags definiert sind, wird ein Bereich von Bits mit niedriger Reihenfolge reserviert, wobei die hochwertigen Bits erweiterungsspezifisch sein können. Es wird empfohlen, dass erweiterte Werte und Bitarrays Bits vom höchsten Wert oder dem höchsten Bit nach unten verwenden. Dadurch bleibt die Option, den Rahmen zwischen dem allgemeinen Teil und dem Erweiterungsteil zu verschieben, wenn dies in Zukunft erforderlich ist. Erweiterungen von Datenstrukturen wird ein Feld mit variabler Größe zugewiesen, wobei größe/offset Teil des festen Teils ist. TAPI beschreibt für jede Datenstruktur, welche gerätespezifischen Erweiterungen zulässig sind.

Zusätzlich zur Erkennung eines bestimmten Erweiterungsbezeichners muss die Anwendung die Versionsnummer der Erweiterung aushandeln, unter der die Anwendung und der Dienstanbieter arbeiten. Dies erfolgt in der zweiten Aushandlungsphase der [**LineGetDevCaps-Funktion.**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)

Ein Erweiterungsbezeichner ist ein global eindeutiger Bezeichner. Es gibt keine zentrale Registrierung für Erweiterungsbezeichner. Stattdessen werden sie vom Hersteller lokal von einem Hilfsprogramm generiert, das mit dem Toolkit verfügbar ist. Die Zahl besteht aus Teilen wie einer eindeutigen LAN-Adresse, Tageszeit und Zufallszahl, um globale Eindeutigkeit zu gewährleisten. Global eindeutige Bezeichner sind so konzipiert, dass sie von universell eindeutigen HP/DEC-Bezeichnern unterschieden werden können und daher vollständig mit ihnen kompatibel sind.

 

 
