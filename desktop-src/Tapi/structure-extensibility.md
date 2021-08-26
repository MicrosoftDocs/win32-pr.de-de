---
description: Erfahren Sie mehr über die Erweiterbarkeit von Strukturen. Es werden Sowohl geräteunabhängige als auch gerätespezifische Erweiterungen von Konstanten und Strukturen vorgenommen.
ms.assetid: d30f80c3-3535-4d78-b0a1-c9a7389f8fd4
title: Strukturerweiterbarkeit
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 378defd35304f6745d42723a44e21c0aa56a34e1f6c40c2f96d5f6743d61b805
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119991720"
---
# <a name="structure-extensibility"></a>Strukturerweiterbarkeit

Die Erweiterung von Konstanten und Strukturen wird sowohl geräteunabhängig als auch gerätespezifisch (herstellerspezifisch) bereitgestellt.

In Konstanten, bei denen es sich um skalare Enumerationen handelt, ist ein Wertebereich für zukünftige allgemeine Erweiterungen reserviert. Der Rest der Werte wird als gerätespezifisch identifiziert. Ein Anbieter kann Bedeutungen für diese Werte auf beliebige Weise definieren. Die Interpretation dieser Werte wird  mit dem Erweiterungsbezeichner in der [**LINEDEVCAPS-Datenstruktur**](/windows/win32/api/tapi/ns-tapi-linedevcaps) angegeben. Für Konstanten, die als Bitflags definiert sind, wird ein Bereich von bits niedriger Ordnung reserviert, bei denen die hohen Bits erweiterungsspezifisch sein können. Es wird empfohlen, dass erweiterte Werte und Bitarrays Bits des höchsten Werts oder eines hochwertigsten Bits nach unten verwenden. Dadurch bleibt die Option, den Rahmen zwischen dem gemeinsamen Teil und dem Erweiterungsteil zu verschieben, wenn dies in Zukunft notwendig ist. Erweiterungen für Datenstrukturen werden einem Feld mit unterschiedlicher Größe zugewiesen, bei dem Größe/Offset Teil des festen Teils ist. TSPI beschreibt für jede Datenstruktur, welche gerätespezifischen Erweiterungen zulässig sind.

Zusätzlich zur Erkennung eines bestimmten Erweiterungsbezeichners muss TAPI (im Auftrag einer Anwendung) die Versionsnummer der Erweiterung aushandeln, unter der die Anwendung und der Dienstanbieter arbeiten. Dies erfolgt mithilfe der [**Funktionen TSPI \_ lineNegotiateExtVersion**](/windows/win32/api/tspi/nf-tspi-tspi_linenegotiateextversion) und [**TSPI \_ phoneNegotiateExtVersion.**](/windows/win32/api/tspi/nf-tspi-tspi_phonenegotiateextversion)

Ein Erweiterungsbezeichner ist ein global eindeutiger Bezeichner. Es gibt keine zentrale Registrierung für Erweiterungsbezeichner. Stattdessen werden sie lokal vom Hersteller durch ein Hilfsprogramm generiert, das mit dem Toolkit verfügbar ist. Die Zahl besteht aus Teilen wie einer (eindeutigen) LAN-Adresse, Tageszeit und Zufallszahl, um globale Eindeutigkeit zu gewährleisten. Global eindeutige Bezeichner sind so konzipiert, dass sie von universell eindeutigen HP/DEC-Bezeichnern unterschieden werden können und daher vollständig kompatibel sind.

 

 
