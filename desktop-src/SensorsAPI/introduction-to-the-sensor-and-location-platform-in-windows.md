---
description: Das Betriebssystem Windows 7 bietet integrierte Unterstützung für Sensorgeräte.
ms.assetid: 751ba2fc-fbff-4418-82ac-eebc8a145b14
title: Übersicht über den Windows-Sensor und die Location-Plattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01b6d3132ad6e1bc299895bc39668edbe19b91c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958824"
---
# <a name="overview-of-the-windows-sensor-and-location-platform"></a>Übersicht über den Windows-Sensor und die Location-Plattform

Das Betriebssystem Windows 7 bietet integrierte Unterstützung für Sensorgeräte. Dies schließt die Unterstützung von Standort Sensoren ein, z. b. GPS-Geräte. Im Rahmen dieser Unterstützung bietet die Windows-Sensor-und-Location-Plattform eine Standardmethode für Gerätehersteller, um Sensor Geräte für Softwareentwickler und-Consumer verfügbar zu machen. Gleichzeitig bietet die Plattform Entwicklern eine standardisierte API und Gerätetreiber Schnittstelle (DDI) für die Arbeit mit Sensoren und Sensordaten.

## <a name="about-sensor-devices"></a>Informationen zu Sensor Geräten

Sensoren sind in vielen Konfigurationen enthalten, und aus einer bestimmten Sicht kann nahezu alles, was Daten über physische Phänomene bereitstellt, als Sensor bezeichnet werden. Obwohl es sich in der Regel um Sensoren als Hardware Geräte handelt, können logische Sensoren auch Informationen über die Emulation der Sensor Funktionalität in Software oder Firmware bereitstellen. Außerdem kann ein einzelnes Hardware Gerät mehrere Sensoren enthalten.

Der Windows-Sensor und die Location Platform organisieren Sensoren in *Kategorien*, die allgemeine Klassen von Sensor Geräten darstellen, und *Typen*, die bestimmte Arten von Sensoren darstellen. Beispielsweise würde ein Sensor in einem Videospiel Controller, der die Position und Bewegung der Hand eines Players (z. b. für ein Video-Bowlingspiel) erkennt, als Ausrichtungs Sensor kategorisiert werden, aber sein Typ wäre 3-D-Beschleunigungsmesser. Im Code stellt Windows Kategorien und Typen mithilfe von global eindeutigen Bezeichner(GUIDs) dar, von denen viele vordefiniert sind. Gerätehersteller können neue Kategorien und Typen erstellen, indem Sie neue GUIDs definieren und veröffentlichen, wenn dies erforderlich ist.

Standort Geräte bilden eine besonders interessante Kategorie. Mittlerweile sind die meisten Benutzer mit globalen Positionierungssystemen (GPS) vertraut. In Windows ist ein GPS-Sensor Teil der Kategorie Standort. Die Kategorie Speicherort kann andere Sensortypen enthalten. Einige dieser Sensortypen sind Software basiert, wie z. b. ein IP-Konflikt Löser, der Standortinformationen auf der Grundlage einer Internet Adresse, eines Mobil Telefonturms, der den Standort basierend auf nahe gelegenen Türmen bestimmt, oder eines Wi-Fi Netzwerkadressen Anbieters bereitstellt, der Standortinformationen aus dem verbundenen drahtlos Netzwerkhub liest.

## <a name="about-the-platform"></a>Informationen zur Plattform

Die Plattform für Windows-Sensoren und-Orte besteht aus den folgenden Entwickler-und Benutzer Komponenten:

-   Mit dem DDI können Windows eine Standardmethode bereitstellen, mit der Sensorgeräte eine Verbindung mit dem Computer herstellen und Daten für andere Subsysteme bereitstellen können.
-   Die Windows-Sensor-API stellt eine Reihe von Methoden, Eigenschaften und Ereignissen zum Arbeiten mit verbundenen Sensoren und Sensor Daten bereit.
-   Die Windows-Location-API, die auf der Windows-Sensor-API basiert, stellt eine Reihe von Programmier Objekten, einschließlich Skript Objekten, zum Arbeiten mit Standortinformationen bereit.
-   Mithilfe der Systemsteuerung Standort und andere Sensoren können Computer Administratoren Sensoren, einschließlich Standort Sensoren, für jeden Benutzer festlegen.

Diese Komponenten werden in den folgenden Abschnitten beschrieben.

## <a name="architecture-diagram"></a>Architekturdiagramm

Das folgende Diagramm zeigt die Beziehung zwischen den Komponenten.

![Diagramm für Sensor-und Positions Plattformen](images/platformarchitecture.png)

## <a name="device-driver-interface"></a>Gerätetreiber Schnittstelle

Sensor Hersteller können Gerätetreiber erstellen, um Sensoren mit Windows 7 zu verbinden. Sensor Gerätetreiber werden mithilfe des Windows-WPD-Treiber Modells implementiert, das auf dem Windows-Benutzermodus-Treiber Framework (UMDF) basiert. Viele Gerätetreiber wurden mithilfe dieser Frameworks geschrieben. Da diese Technologien eingerichtet werden, werden erfahrene Gerätetreiber Programmierer feststellen, dass Sie einen Sensor Treiber als vertraute Aufgabe schreiben. Der Sensor-DDI verwendet bestimmte Datentypen und Schnittstellen für die Datentypen "bidf" und "WPD" und definiert außerdem sensorspezifische WPD-Befehle und-Parameter, wo dies erforderlich ist. Weitere Informationen zum Erstellen von Sensorgeräte Treibern finden Sie im Windows-Treiberkit.

## <a name="sensor-api"></a>Sensor-API

Die Sensor-API ermöglicht C++-Entwicklern das Erstellen von Sensor basierten Programmen mithilfe eines Satzes von COM-Schnittstellen. Die API definiert Schnittstellen zur Ausführung allgemeiner Sensor Programmierungsaufgaben, die das Verwalten von Sensoren nach Kategorie, Typ oder ID, das Verwalten von Sensor Ereignissen, das Arbeiten mit einzelnen Sensoren und Sensor Auflistungen sowie das Arbeiten mit Sensordaten umfassen. Die Windows SDK enthält Header Dateien, Dokumentationen, Beispiele und Tools, mit denen Softwareentwickler die Verwendung von Sensoren in Windows-Programmen erleichtern können. In dieser Dokumentation wird die Sensor-API beschrieben.

## <a name="location-api"></a>Location-API

Die Location-API basiert auf der Sensor-API und bietet eine einfache Möglichkeit, Daten über den geografischen Standort abzurufen und gleichzeitig die Privatsphäre des Benutzers zu schützen. Die Location-API stellt die Funktionalität über einen Satz von COM-Schnittstellen bereit, die-Objekte darstellen. Diese Objekte können von Programmierern verwendet werden, die die Verwendung von com über die Programmiersprache C++ oder in Skriptsprachen, wie z. b. JScript, verstehen. Die Skriptunterstützung ermöglicht den einfachen Zugriff auf Speicherort Daten für Projekte, die in der lokalen Computer Zone ausgeführt werden, z. b. Mini Anwendungen. Die Windows SDK umfasst Header Dateien, Dokumentationen (einschließlich Referenz Dokumentation zur Skripterstellung), Beispiele und Tools, mit denen Sie Web-und Softwareentwickler bei der Verwendung von Standortinformationen in ihren Programmen unterstützen können.

## <a name="location-and-other-sensors-control-panel"></a>Systemsteuerung für Standort und andere Sensoren

Windows 7 enthält eine Systemsteuerung, mit der Computer Administratoren Sensoren systemweit oder für jeden Benutzer aktivieren oder deaktivieren können. Da einige Sensoren sensible Daten verfügbar machen können, ermöglicht Ihnen diese Benutzeroberfläche Administratoren, zu steuern, ob alle Programme Zugriff auf jeden Sensor für jeden Benutzer haben. Benutzer können auch Sensoreigenschaften anzeigen und die Sensor Beschreibung ändern, die auf der Benutzeroberfläche angezeigt wird.

In der Systemsteuerung ist auch eine Standard Speicherort Seite enthalten, auf der Benutzer ihren Speicherort angeben können. Wenn kein Sensor verfügbar ist, verwendet die Plattform den vom Benutzer bereitgestellten Speicherort. Benutzer können die Felder für die Hauptadresse bereitstellen, die die Adresse, die Stadt, den Bundesstaat oder die Provinz sowie das Land oder die Region enthalten.

## <a name="related-topics"></a>Zugehörige Themen

[Informationen zur Sensor-API](about-the-sensor-api.md)

[Windows Hardware Developer Central-Website](https://www.microsoft.com/whdc/device/sensors/default.mspx)

[Windows Developer Center](https://msdn.microsoft.com/windows/default.aspx?wt.svl=client)
