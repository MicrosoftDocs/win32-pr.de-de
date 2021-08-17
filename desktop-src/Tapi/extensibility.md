---
description: Erfahren Sie mehr über Erweiterbarkeit. Es werden Sowohl geräteunabhängige als auch gerätespezifische Erweiterungen von Konstanten und Strukturen vorgenommen.
ms.assetid: bc0a18f3-1f58-4a24-8afb-c31f3b561375
title: Erweiterbarkeit (Telefonie-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 89b9b130c27ffb01131181ad0b765d6a41b3eae0bbfc84cc2ab325c3a13230a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140673"
---
# <a name="extensibility"></a>Erweiterungen

Die Erweiterung von Konstanten und Strukturen wird sowohl geräteunabhängig als auch gerätespezifisch (herstellerspezifisch) bereitgestellt. In Konstanten, bei denen es sich um skalare Enumerationen handelt, ist ein Wertebereich für zukünftige allgemeine Erweiterungen reserviert. Die restlichen Werte werden als gerätespezifisch identifiziert. Ein Anbieter kann Bedeutungen für diese Werte in beliebiger Weise definieren. Ihre Interpretation wird mit  dem Erweiterungsbezeichner in der [**LINEDEVCAPS-Datenstruktur**](/windows/win32/api/tapi/ns-tapi-linedevcaps) angegeben. Für Konstanten, die als Bitflags definiert sind, wird ein Bereich von bits niedriger Ordnung reserviert, bei denen die hohen Bits erweiterungsspezifisch sein können. Es wird empfohlen, dass erweiterte Werte und Bitarrays Bits des höchsten Werts oder eines hochwertigsten Bits nach unten verwenden. Dadurch bleibt die Option, den Rahmen zwischen dem gemeinsamen Teil und dem Erweiterungsteil zu verschieben, wenn dies in Zukunft notwendig ist. Erweiterungen für Datenstrukturen werden einem Feld mit unterschiedlicher Größe zugewiesen, bei dem Größe/Offset Teil des festen Teils ist. TAPI beschreibt für jede Datenstruktur, welche gerätespezifischen Erweiterungen zulässig sind.

Zusätzlich zur Erkennung eines bestimmten Erweiterungsbezeichners muss die Anwendung die Versionsnummer der Erweiterung aushandeln, unter der die Anwendung und der Dienstanbieter arbeiten. Dies erfolgt in der zweiten Versionsphase der [**lineGetDevCaps-Funktion.**](/windows/win32/api/tapi/nf-tapi-linegetdevcaps)

Ein Erweiterungsbezeichner ist ein global eindeutiger Bezeichner. Es gibt keine zentrale Registrierung für Erweiterungsbezeichner. Stattdessen werden sie lokal vom Hersteller durch ein Hilfsprogramm generiert, das mit dem Toolkit verfügbar ist. Die Zahl besteht aus Teilen wie einer eindeutigen LAN-Adresse, Tageszeit und Zufallszahl, um globale Eindeutigkeit zu gewährleisten. Globally Unique Identifiers sind so konzipiert, dass sie von universell eindeutigen HP/DEC-Bezeichnern unterschieden werden können und daher vollständig kompatibel sind.

 

 
