---
description: Grundlegendes zur Internationalisierung
ms.assetid: 9147cd20-eeae-4ad4-8d51-ac1d68a4b2c5
title: Grundlegendes zur Internationalisierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8df3fc38ab844ec991c0e87f286ffb48c3d48ec7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106360738"
---
# <a name="understanding-internationalization"></a>Grundlegendes zur Internationalisierung

Die Entwicklung internationalisierter Softwareprodukte erfordert nicht nur die Produktion von korrekter Code, sondern auch einen Entwurf, der es dem Produkt ermöglicht, viele Gebiets Schemas zu unterstützen. Entwickler und ihre Vorgesetzten sollten sich mit dem Aufwand und der Aufmerksamkeit befassen, die für die Erstellung weltweit Einsatz fähiger Anwendungen erforderlich sind, und zwar unabhängig davon, ob Sie als einzelne Binärdateien bereitgestellt werden, die für die Verwendung in vielen verschiedenen Märkten bereit stehen, oder als mehrere Binärdateien, die jeweils für ein einzelnes Gebiets Schema spezifisch sind. Als Entwickler müssen Sie sicherstellen, dass ihre Verwaltung weiß, dass die Internationalisierung mehr als nur die Code Entwicklung umfasst. Der Entwurf für die Internationalisierung am Anfang des Produktzyklen spart Zeit, Geld und Aufwand.

**Internationalisierung** ist die Erstellung von Software, die sich an Gebiets Schemas auf der ganzen Welt anpasst. Bei einem Gebiets **Schema handelt es sich um eine Sammlung** von sprachbezogenen Benutzereinstellungen. Ein Gebiets Schema wird durch die Kopplung einer Sprache und einer geografischen Region angegeben. Beispielsweise sind Englisch (USA) und Englisch (Vereinigtes Königreich) zwei verschiedene Gebiets Schemas, wie z. b. Englisch (Kanada) und Französisch (Kanada).

Internationalisierte Software weist folgende Attribute auf:

-   Die **weltweite Bereitschaft** deckt den Entwurf und die Implementierung ab, die Gebiets Schema unabhängigen Code von Gebiets Schema abhängigen Ressourcen trennen und zwei Hauptbereiche umfasst:
    -   Bei der **Globalisierung** handelt es sich um den Prozess der Entwicklung eines Programm Kerns mit Features und Code Entwürfen, die unabhängig von Sprache oder Gebiets Schema sind. Stattdessen unterstützt der Entwurf die Eingabe, Anzeige und Ausgabe von Unicode-unterstützten sprach Skripts sowie Daten, die sich auf bestimmte Gebiets Schemas beziehen.
    -   **Lokalisier barkeit** ist der Entwurf der Software Codebasis und der Ressourcen, sodass ein Programm, wie unten definiert, in verschiedene sprach Editionen ohne Änderungen am Quellcode lokalisiert werden kann. Beispielsweise müssen Zeichen folgen Puffer im Code und die Textfelder in der Benutzeroberfläche groß genug sein, um längere Text Zeichenfolgen in Sprachen wie Deutsch oder Niederländisch aufnehmen zu können.
-   **Lokalisierung** Dies umfasst das Übersetzen und Anpassen eines Produkts für einen bestimmten Markt, und es geht hauptsächlich um das Erstellen von Ressourcen Dateien, anstatt Quellcode zu schreiben.

Beispielsweise ist die Verwendung der von der Microsoft Win32-API bereitgestellten NLS (National Language Support) ein Softwareentwicklungsprozess, der die weltweite Bereitschaft unterstützt, während das Ändern der Benutzeroberflächen Elemente, die Übersetzung von Text und die Standardisierung der Terminologie in der Regel durch eine Person, die ein Sprachspezialist ist (z. b. ein Konvertierungsprogramm) Selbst wenn Ihre Code Entwicklung die Welt Bereitschaft hervorgehoben hat, müssen Sie die Lokalisierung verstehen, da sich Ihre Entwurfsentscheidungen auf die Arbeit des Konvertierungs Programms auswirken.

 

 



