---
description: Sensor-API
ms.assetid: a6ea76e6-9721-453a-a657-96f53660e09d
title: Sensor-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a36259910fb7583c91b695f69066aa2abf9be1e0
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2021
ms.locfileid: "108118408"
---
# <a name="sensor-api"></a>Sensor-API

## <a name="purpose"></a>Zweck

Windows 7 bietet native Unterstützung für Sensoren, bei denen es sich um Geräte handelt, die physische Körper wie Temperatur oder Standort messen können. In dieser Dokumentation wird die Sensor-API beschrieben, mit der Anwendungen Daten von Sensoren auf standardisierte Weise abrufen und verwenden können.

Als Menschen verlassen wir uns auf unsere Sinne, um uns Informationen über die Welt um uns herum zu liefern. Wenn wir Computer erstellen, um einen Teil unserer Arbeit zu übernehmen, fügen wir Sensormechanismen hinzu, damit die Computer angemessen auf sich ändernde Bedingungen reagieren können.

Beispielsweise verwenden Automobil-Engines in der Regel eine Vielzahl von Sensoren. Diese Sensoren werden von einem integrierten Computer überwacht, der die Einstellungen, z. B. die Zeitsteuerung des Triebwerks, kontinuierlich an die Leistungs- und Effizienzoptimierung animiert. Ein Fernsehgerät kann einen Umgebungslichtsensor verwenden, um die Helligkeit des Bilds an die sich ändernden Raumbedingungen anzupassen. Auch etwas so einfaches wie eine Türknüpftaste fungiert als ein rudimentärer Sensor, um eine menschliche Präsenz an der Tür zu erkennen.

Während die rein maschinelle Türtür ihren Zweck erfüllt, werden die von komplexen Sensoren bereitgestellten Informationen viel leistungsfähiger, wenn sie mit Software kombiniert werden. Moderne Sensoren können sehr schnell und in einer Vielzahl von Formaten viele Daten bereitstellen, sodass Software einen natürlichen Mechanismus bietet, um Sensordaten sinnvoll zu nutzen.

Heute können Softwareentwickler Programme schreiben, die Sensoren verwenden, aber eine fehlende Standardisierung macht die Programmierung für Sensoren zu einer mühsamen Aufgabe. Nachdem ein sensorbasiertes Programm abgeschlossen wurde, ist es in der Regel für immer von einem bestimmten Hardwaretyp abhängig. Die Verwendung einer oder mehrere vertikaler Lösungen, um die Bereitstellung eines softwarebasierten Systems zu ermöglichen, hat die Integration von Sensoren mit Computerhardware eingeschränkt, und bisher waren Windows-basierte Computer keine Ausnahme.

Windows 7 bietet native Unterstützung für Sensoren, erweitert um eine neue Entwicklungsplattform für die Arbeit mit Sensoren, einschließlich Standortsensoren wie GPS-Geräten. Die Windows Sensor and Location-Plattform bietet Geräteherstellern standardmäßig die Möglichkeit, Sensorgeräte softwareentwicklern und -consumern zur Verfügung zu stellen, während Entwicklern eine standardisierte Anwendungsprogrammierschnittstelle (Application Programming Interface, API) für die Arbeit mit Sensoren und Sensordaten zur Verfügung gestellt wird.

Sensoren sind Geräte oder Mechanismen, die physische Zustände messen, beschreibende Daten oder Informationen zum Zustand eines physischen Objekts oder einer physischen Umgebung bereitstellen können. Computer können integrierte Sensoren, Sensoren, die über kabelgebundene oder drahtlose Verbindungen verbunden sind, oder Sensoren, die Daten über ein Netzwerk oder das Internet bereitstellen, verwenden.

Die Sensor-API bietet eine Standardlösung für den programmgesteuerten Zugriff auf Daten, die von Sensoren bereitgestellt werden. Die Sensor-API standardisiert Folgendes:

-   Sensorkategorien, -typen und -eigenschaften.
-   Datenformate für Standardsensortypen.
-   COM-Schnittstellen für die Arbeit mit Sensoren und Sammlungen von Sensoren.
-   Ereignismechanismen für den asynchronen Empfang von Sensordaten.

Mit der Sensor-API können Sie auch benutzerdefinierte Sensorkategorien, -typen, -eigenschaften, -datenformate und -ereignisse definieren.

## <a name="developer-audience"></a>Entwicklergruppe

Die Sensor-API stellt ihre Funktionalität über eine Reihe von COM-Schnittstellen bereit. In dieser Dokumentation wird davon ausgegangen, dass Sie über kenntnisse der Programmierung mithilfe der Programmiersprache C++ verfügen und grundlegende Kenntnisse über die Verwendung von COM-Objekten und -Schnittstellen haben. Aus Gründen der Kürze verwenden viele Codebeispiele in dieser Dokumentation (sowie in den Codebeispielen) Active Template Library -Objekte (ATL), um COM-Funktionen zu implementieren.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Erste Schritte](getting-started.md)
-   [Informationen zur Sensor-API](about-the-sensor-api.md)
-   [Programmierhandbuch für die Sensor-API](sensor-api-programming-guide.md)
-   [Programmierreferenz zur Sensor-API](sensor-api-programming-reference.md)

 

 



