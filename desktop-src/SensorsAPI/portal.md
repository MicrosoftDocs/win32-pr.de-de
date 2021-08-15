---
description: Sensor-API
ms.assetid: a6ea76e6-9721-453a-a657-96f53660e09d
title: Sensor-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fc5c3fd3cbdbf2aac9a161a6cb8bc150d2828c2d48a346b94843878cda49a6a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889671"
---
# <a name="sensor-api"></a>Sensor-API

## <a name="purpose"></a>Zweck

Windows 7 bietet native Unterstützung für Sensoren, bei denen es sich um Geräte handelt, die physische Körper wie Temperatur oder Standort messen können. In dieser Dokumentation wird die Sensor-API beschrieben, mit der Anwendungen Daten von Sensoren auf standardisierte Weise abrufen und verwenden können.

Als Menschen verlassen wir uns auf unsere Sinne, um uns Informationen über die Welt um uns herum zu liefern. Wenn wir Computer erstellen, um einen Teil unserer Arbeit zu übernehmen, fügen wir Sensormechanismen hinzu, damit die Computer angemessen auf sich ändernde Bedingungen reagieren können.

Beispielsweise verwenden Automobil-Engines in der Regel eine Vielzahl von Sensoren. Diese Sensoren werden von einem integrierten Computer überwacht, der die Einstellungen, z. B. die Zeitsteuerung des Triebwerks, kontinuierlich an passt, um die Leistung und Effizienz zu maximieren. Ein Fernsehgerät kann einen Umgebungslichtsensor verwenden, um die Helligkeit des Bilds an die sich ändernden Raumbedingungen anzupassen. Auch etwas so einfaches wie eine Türknüpftaste fungiert als ein rudimentärer Sensor, um eine menschliche Präsenz an der Tür zu erkennen.

Während die rein maschinelle Türtür ihren Zweck erfüllt, werden die von komplexen Sensoren bereitgestellten Informationen viel leistungsfähiger, wenn sie mit Software kombiniert werden. Moderne Sensoren können sehr schnell und in einer Vielzahl von Formaten viele Daten bereitstellen, sodass Software einen natürlichen Mechanismus zum Sinnvollen von Sensordaten bietet.

Heute können Softwareentwickler Programme schreiben, die Sensoren verwenden, aber eine fehlende Standardisierung macht die Programmierung für Sensoren zu einer mühsamen Aufgabe. Nachdem ein sensorbasiertes Programm abgeschlossen wurde, ist es normalerweise für immer von einem bestimmten Hardwaretyp abhängig. Die Verwendung einer oder mehrere vertikaler Lösungen, um die Bereitstellung eines softwarebasierten Systems zu ermöglichen, hat die Integration von Sensoren mit Computerhardware eingeschränkt. Bisher waren Windows computerbasierte Computer keine Ausnahme.

Windows 7 bietet native Unterstützung für Sensoren, erweitert um eine neue Entwicklungsplattform für die Arbeit mit Sensoren, einschließlich Standortsensoren wie GPS-Geräten. Die Windows Sensor- und Standortplattform ist eine Standardplattform für Gerätehersteller, um Sensorgeräte für Softwareentwickler und -verbraucher verfügbar zu machen, während entwicklern eine standardisierte Anwendungsprogrammierschnittstelle (APPLICATION Programming Interface, API) für die Arbeit mit Sensoren und Sensordaten zur Verfügung steht.

Sensoren sind Geräte oder Mechanismen, die physische Datenübertragungen messen, beschreibende Daten bereitstellen oder Informationen über den Zustand eines physischen Objekts oder einer Physischen Umgebung bereitstellen können. Computer können integrierte Sensoren, Sensoren, die über kabelgebundene oder drahtlose Verbindungen verbunden sind, oder Sensoren verwenden, die Daten über ein Netzwerk oder das Internet bereitstellen.

Die Sensor-API stellt eine Standard-Möglichkeit für den programmgesteuerten Zugriff auf Daten bereit, die Sensoren bereitstellen. Die Sensor-API standardisiert:

-   Sensorkategorien, -typen und -eigenschaften.
-   Datenformate für Standardsensortypen.
-   COM-Schnittstellen für die Arbeit mit Sensoren und Sammlungen von Sensoren.
-   Ereignismechanismen für den asynchronen Empfang von Sensordaten.

Mit der Sensor-API können Sie auch benutzerdefinierte Sensorkategorien, Typen, Eigenschaften, Datenformate und Ereignisse definieren.

## <a name="developer-audience"></a>Entwicklergruppe

Die Sensor-API stellt ihre Funktionalität über eine Reihe von COM-Schnittstellen bereit. In dieser Dokumentation wird davon ausgegangen, dass Sie über kenntnisse Kenntnisse der Programmierung mit der Programmiersprache C++ verfügen und grundlegende Kenntnisse zur Verwendung von COM-Objekten und -Schnittstellen haben. Aus Gründen der Kürze verwenden viele Codebeispiele in dieser Dokumentation (sowie in den Codebeispielen) ATL-Objekte (Active Template Library), um COM-Funktionen zu implementieren.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Erste Schritte](getting-started.md)
-   [Informationen zur Sensor-API](about-the-sensor-api.md)
-   [Programmierhandbuch zur Sensor-API](sensor-api-programming-guide.md)
-   [Referenz zur Sensor-API-Programmierung](sensor-api-programming-reference.md)

 

 



