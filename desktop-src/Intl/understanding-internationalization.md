---
description: Grundlegendes zur Internationalisierung
ms.assetid: 9147cd20-eeae-4ad4-8d51-ac1d68a4b2c5
title: Grundlegendes zur Internationalisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ed47364da56e2c5ab5e13001b1b49360b23caa39997484e5058022516f437b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119638790"
---
# <a name="understanding-internationalization"></a>Grundlegendes zur Internationalisierung

Die Entwicklung internationalisierter Softwareprodukte erfordert nicht nur die Produktion von richtigem Code, sondern auch einen Entwurf, der es dem Produkt ermöglicht, viele Lokale zu unterstützen. Entwickler und ihre Vorgesetzten sollten sich des Aufwands und der Detailgenauigkeit bewusst sein, die erforderlich sind, um weltweit einsatzbereite Anwendungen zu erstellen, unabhängig davon, ob sie sie als einzelne Binärdateien für die Verwendung in vielen verschiedenen Märkten oder als mehrere Binärdateien liefern, die jeweils für ein einzelnes Gebiet spezifisch sind. Stellen Sie als Entwickler sicher, dass Ihre Verwaltung versteht, dass die Internationalisierung mehr als nur die Codeentwicklung umfasst. Wenn Sie zu Beginn Ihres Produktzyklus für die Internationalisierung entwerfen, sparen Sie Zeit, Geld und Aufwand.

**Internationalisierung** ist die Erstellung von Software, die sich an Diesindizes auf der ganzen Welt anpasst. Ein **-Locale** ist eine Sammlung sprachbezogener Benutzereinstellungen. Ein Locale wird durch die Kopplung einer Sprache und einer geografischen Region angegeben. Englisch (USA) und Englisch (Vereinigtes Königreich) sind z. B. zwei unterschiedliche Lokale, ebenso wie Englisch (Kanada) und Französisch (Kanada).

Internationalisierte Software verfügt über die folgenden Attribute:

-   **Weltbereitschaft umfasst** Entwurf und Implementierung, die lokal unabhängigen Code von vom Lokalen abhängigen Ressourcen trennen und zwei Hauptbereiche umfassen:
    -   **Globalisierung ist** der Prozess der Entwicklung eines Programmkerns mit Features und Codeentwurf, die unabhängig von Sprache oder Locale sind. Stattdessen unterstützt der Entwurf die Eingabe, Anzeige und Ausgabe von Unicode-unterstützten Sprachskripts sowie Daten im Zusammenhang mit bestimmten Lokalen.
    -   **Lokalisierbarkeit** ist der Entwurf der Softwarecodebasis und der Ressourcen, damit ein Programm, wie unten definiert, ohne Änderungen am Quellcode in verschiedene Spracheditionen lokalisiert werden kann. Beispielsweise müssen Zeichenfolgenpuffer im Code und Textfelder in der Benutzeroberfläche groß genug sein, um längere Textzeichenfolgen in Sprachen wie Deutsch oder Niederländisch aufnehmen zu können.
-   **Lokalisierung** Dies umfasst die Übersetzung und Anpassung eines Produkts für einen bestimmten Markt, und es geht hauptsächlich darum, Ressourcendateien zu erstellen, anstatt Quellcode zu schreiben.

Beispielsweise ist die Verwendung des von der Microsoft Win32-API bereitgestellten National Language Support (NLS) ein Softwareentwicklungsprozess, der die Weltbereitschaft unterstützt. Das Ändern der Benutzeroberflächenelemente, das Übersetzen von Text und die Standardisierung der Terminologie sind Lokalisierungsschritte, die normalerweise von einer Person ausgeführt werden, die ein Sprachspezialisten ist, z. B. ein Translator. Auch wenn ihre Codeentwicklung die Bereitschaft der Welt unterstreicht, müssen Sie die Lokalisierung verstehen, da sich Ihre Entwurfsentscheidungen auf die Arbeit des Translators auswirken.

 

 



