---
title: Sensor Plattform
description: Windows 7 hat sich geändert, wie Entwickler Sensoren verwenden.
ms.assetid: ed323658-dfd6-4c1b-ada2-5d68ebb56482
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 98fe94fd48ffa16080054a22b4d377ab4757d61d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039227"
---
# <a name="sensor-platform"></a>Sensor Plattform

Windows 7 hat sich geändert, wie Entwickler Sensoren verwenden. Es umfasst systemeigene Unterstützung für Sensoren, erweitert durch eine neue Entwicklungsplattform für die Verwendung von Sensoren, einschließlich Standort Sensoren wie z. b. Global Positionierungs Systems (GPS).

Die *Windows-Location*-APIs basieren auf der Sensor Plattform und sind ein neues Feature von Windows 7, mit dem Anwendungsentwickler auf die Informationen zum physischen Standort des Benutzers zugreifen können. Mit den *Windows-Location*-APIs können Hardware abstrahiert, mehrere Anwendungen gleichzeitig unterstützt und nahtlos zwischen verschiedenen Technologien gewechselt werden, sodass der Anwendungsentwickler die Last der Verwaltung dieser Einschränkungen trägt. Die *Location*-APIs können von Programmierern über die Programmiersprache C++ (von Programmierern, die mit Component Object Model (com) vertraut sind) oder durch die Verwendung von COM-Objekten in Skriptsprachen wie Microsoft JScript verwendet werden. Die Skriptunterstützung ermöglicht den einfachen Zugriff auf Speicherort Daten für Projekte wie Mini Anwendungen.

Windows 7 bietet eine solide, leicht zu verwendende Plattform für die Verwendung von Sensorgeräten, z. b. einem Umgebungslichtsensor oder einem Temperaturmessgerät, um Umweltbewusstsein in Windows-Anwendungen zu schaffen. PCs können Sensoren verwenden, die in den Computer integriert sind, über Kabel-oder drahtlos Verbindungen verbunden sind oder über ein Netzwerk oder das *Internet* verbunden sind.

Die *Sensor* -und *Location*-APIs bieten eine Standardmethode zum Ermitteln von Sensoren und zum programmgesteuerten Zugriff auf Daten, die von Sensoren bereitgestellt werden.

In der Systemsteuerung des *Sensors* können Benutzer Sensoren aktivieren oder deaktivieren, den Zugriff auf Sensoren steuern, die sensible Daten verfügbar machen, Sensor Eigenschaften anzeigen und die Beschreibungen der Sensoren ändern.

Die [Sensor Klassen Erweiterung](/windows-hardware/drivers/sensors/about-the-sensor-class-extension) ist ein zentraler Bestandteil des Treiber Entwicklungsmodells für die Sensorplattform. Es stellt die folgenden Mechanismen bereit, die verwendet werden, wenn ein Treiber für den [Benutzermodus-Treiber-Frameworks (Endf)](https://developer.microsoft.com/windows/hardware) geschrieben wird:

-   Integration mit der Sensor Plattform
-   Sicherheits Durchsetzung

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Sensor-API](../sensorsapi/portal.md)
</dt> <dt>