---
title: Sensorplattform
description: Windows 7 hat sich geändert, wie Entwickler Sensoren verwenden.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c7072a19ee0a746b0764850230a06de1ca72be8ca4633f1350165297f1ef4036
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118203890"
---
# <a name="sensor-platform"></a>Sensorplattform

Windows 7 hat sich geändert, wie Entwickler Sensoren verwenden. Es umfasst native Unterstützung für Sensoren, erweitert um eine neue Entwicklungsplattform für die Arbeit mit Sensoren, einschließlich Standortsensoren wie GPS-Geräten (Global Positioning Systems).

Die *Windows Location-APIs* basieren auf der Sensorplattform und sind ein neues Feature Windows 7, mit dem Anwendungsentwickler auf die physischen Standortinformationen des Benutzers zugreifen können. Die *Windows Location-APIs* können Hardware abstrahieren, gleichzeitig mehrere Anwendungen unterstützen und nahtlos zwischen verschiedenen Technologien wechseln, wodurch der Anwendungsentwickler von der Verwaltung dieser Einschränkungen abweicht. Die *Location-APIs* können von Programmierern über die Programmiersprache C++ (von Programmierern, die mit Component Object Model (COM) vertraut sind) oder mit COM-Objekten in Skriptsprachen wie Microsoft JScript verwendet werden. Die Skriptunterstützung bietet einfachen Zugriff auf Standortdaten für Projekte wie Gadgets.

Windows 7 bietet eine solide, benutzerfreundliche Plattform für die Verwendung von Sensorgeräten, z. B. einem Umgebungslichtsensor oder einem Temperaturmessgerät, um umgebungsbezogenes Bewusstsein in Windows Anwendungen zu schaffen. PCs können Sensoren verwenden, die in den Computer integriert sind, über kabelgebundene oder drahtlose Verbindungen oder über ein Netzwerk oder das *Internet* verbunden sind.

Die *Sensor-* und *Standort-APIs* bieten eine Standard-Methode zum Ermitteln von Sensoren und zum programmgesteuerten Zugreifen auf daten, die von Sensoren zur Verfügung stellen.

Mit  der Sensorsteuerung können Benutzer Sensoren aktivieren oder deaktivieren, den Zugriff auf Sensoren steuern, die sensible Daten verfügbar machen können, Sensoreigenschaften anzeigen und die Beschreibungen von Sensoren ändern.

Die [Sensorklassenerweiterung](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) ist ein wesentlicher Bestandteil des Treiberentwicklungsmodells für die Sensorplattform. Sie stellt die folgenden Mechanismen bereit, die beim Schreiben eines [UMDF-Sensortreibers (User-Mode Driver Framework)](https://developer.microsoft.com/windows/hardware) verwendet werden:

-   Integration in die Sensorplattform
-   Sicherheitserzwingung

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sensor-API](../sensorsapi/portal.md)
</dt> <dt>