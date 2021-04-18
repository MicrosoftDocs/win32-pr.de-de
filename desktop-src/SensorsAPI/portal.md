---
description: .
ms.assetid: a6ea76e6-9721-453a-a657-96f53660e09d
title: Sensor-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c4d6fd7805607afa80fcee27568004906a0a8e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345029"
---
# <a name="sensor-api"></a>Sensor-API

## <a name="purpose"></a>Zweck

Windows 7 umfasst systemeigene Unterstützung für Sensoren, bei denen es sich um Geräte handelt, die physische Phänomene wie Temperatur oder Standort messen können. In dieser Dokumentation wird die Sensor-API beschrieben, die es Anwendungen ermöglicht, Daten von Sensoren auf standardisierte Weise zu erhalten und zu verwenden.

Als Menschen verlassen wir uns auf unsere Sinne, um uns Informationen zur Welt rund um die Welt bereitzustellen. Wenn wir Computer erstellen, die einige unserer Aufgaben Unternehmen, fügen wir Sensor Mechanismen hinzu, damit die Computer angemessen auf veränderliche Bedingungen reagieren können.

Auto Mobil Engines verwenden z. b. normalerweise eine Vielzahl von Sensoren. Diese Sensoren werden von einem integrierten Computer überwacht, der kontinuierlich Einstellungen anpasst, wie z. b. Engine-zeitliche Steuerung, um die Leistung und Effizienz zu maximieren. Ein Fernsehgerät kann einen Umgebungslichtsensor verwenden, um die Helligkeit des Bilds an geänderte Raumbedingungen anzupassen. Sogar etwas so einfaches wie eine Türklingel Schaltfläche fungiert als rudimentärer Sensor zum Erkennen einer menschlichen Präsenz an der Tür.

Obwohl die rein mechanische Türglocke ihren Zweck erfüllt, werden die von komplexen Sensoren bereitgestellten Informationen weitaus leistungsfähiger, wenn Sie mit Software kombiniert werden. Moderne Sensoren können sehr schnell und in einer Vielzahl von Formaten viele Daten bereitstellen, sodass Software einen natürlichen Mechanismus zur Erstellung von Sensordaten bereitstellt.

Softwareentwickler können heutzutage Programme schreiben, die Sensoren verwenden, aber eine fehlende Standardisierung macht das Programmieren für Sensoren zu einer schwierigen Aufgabe. Nachdem ein Sensor basiertes Programm abgeschlossen ist, ist es in der Regel immer von einem bestimmten Hardwaretyp abhängig. Die Verwendung einer oder mehrerer vertikaler Lösungen zum Aktivieren der Bereitstellung eines softwarebasierten Systems hat die Integration von Sensoren in Computer Hardware eingeschränkt. bisher gab es bei Windows-basierten Computern keine Ausnahme.

Windows 7 bietet systemeigene Unterstützung für Sensoren, erweitert durch eine neue Entwicklungsplattform zum Arbeiten mit Sensoren, einschließlich Standort Sensoren wie GPS-Geräten. Die Plattform für Windows-Sensoren und-Orte bietet Geräteherstellern standardmäßig die Möglichkeit, Sensor Geräte für Softwareentwickler und-Consumer verfügbar zu machen, während Entwicklern eine standardisierte Anwendungsprogrammierschnittstelle (Application Programming Interface, API) für die Arbeit mit Sensoren und Sensor Daten zur Verfügung steht.

Sensoren sind Geräte oder Mechanismen, mit denen physische Phänomene gemessen, beschreibende Daten bereitgestellt oder Informationen über den Status eines physischen Objekts oder einer Umgebung bereitgestellt werden können. Computer können integrierte Sensoren, Sensoren, die über Kabel-oder drahtlos Verbindungen verbunden sind, oder Sensoren nutzen, die Daten über ein Netzwerk oder das Internet bereitstellen.

Die Sensor-API bietet eine Standardmethode zum programmgesteuerten Zugriff auf Daten, die von Sensoren bereitgestellt werden. Die Sensor-API standardisiert Folgendes:

-   Sensor Kategorien,-Typen und-Eigenschaften.
-   Datenformate für Standard Sensortypen.
-   COM-Schnittstellen zum Arbeiten mit Sensoren und Auflistungen von Sensoren.
-   Ereignis Mechanismen für den asynchronen Empfang von Sensordaten.

Die Sensor-API ermöglicht außerdem das Definieren von benutzerdefinierten Sensor Kategorien,-Typen,-Eigenschaften,-Datenformaten und-Ereignissen.

## <a name="developer-audience"></a>Entwicklergruppe

Die Sensor-API stellt die Funktionalität über einen Satz von COM-Schnittstellen bereit. In dieser Dokumentation wird davon ausgegangen, dass Sie über Kenntnisse in der Programmierung mit der Programmiersprache C++ verfügen, und Sie verfügen über grundlegende Kenntnisse der Verwendung von COM-Objekten und-Schnittstellen. Aus Gründen der Kürze verwenden viele Codebeispiele in dieser Dokumentation (und in den Codebeispielen) Active Template Library (ATL)-Objekte, um com-Funktionen zu implementieren.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Erste Schritte](getting-started.md)
-   [Informationen zur Sensor-API](about-the-sensor-api.md)
-   [Programmier Handbuch zur Sensor-API](sensor-api-programming-guide.md)
-   [Programmier Referenz zur Sensor-API](sensor-api-programming-reference.md)

 

 



