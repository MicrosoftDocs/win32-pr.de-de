---
description: Das Windows 7-Betriebssystem bietet integrierte Unterstützung für Sensorgeräte.
ms.assetid: 751ba2fc-fbff-4418-82ac-eebc8a145b14
title: Übersicht über den Windows Sensor und die Standortplattform
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc4847d6d6137b91ce577cfce0dbc54cc8c6e19430e1318eaff145c24ce493af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118889729"
---
# <a name="overview-of-the-windows-sensor-and-location-platform"></a>Übersicht über den Windows Sensor und die Standortplattform

Das Windows 7-Betriebssystem bietet integrierte Unterstützung für Sensorgeräte. Dies umfasst unterstützung für Standortsensoren, z. B. GPS-Geräte. Im Rahmen dieser Unterstützung bietet die Windows Sensor- und Standortplattform eine Standardplattform für Gerätehersteller, um Sensorgeräte für Softwareentwickler und -kunden verfügbar zu machen. Gleichzeitig bietet die Plattform Entwicklern eine standardisierte API und Gerätetreiberschnittstelle (Device Driver Interface, DDI), um mit Sensoren und Sensordaten zu arbeiten.

## <a name="about-sensor-devices"></a>Informationen zu Sensorgeräten

Sensoren kommen in vielen Konfigurationen vor, und aus einer bestimmten Perspektive kann fast alles, was Daten zu physischen Datenübertragungen liefert, als Sensor bezeichnet werden. Obwohl sensoren in der Regel als Hardwaregeräte bezeichnet werden, können logische Sensoren auch Informationen durch Emulation von Sensorfunktionen in Software oder Firmware bereitstellen. Außerdem kann ein einzelnes Hardwaregerät mehrere Sensoren enthalten.

Die Windows Sensor- und Standortplattform organisiert Sensoren in *Kategorien,* die breite Klassen von Sensorgeräten darstellen, und typen *,* die bestimmte Arten von Sensoren darstellen. Beispielsweise würde ein Sensor in einem Videospielcontroller, der die Position und Bewegung der Hand eines Spielers erkennt (z. B. für ein Video-Spiel), als Ausrichtungssensor kategorisiert, aber sein Typ wäre ein 3D-Beschleunigungsmesser. Im Code stellt Windows Kategorien und Typen dar, indem guiDs (Globally Unique Identifier) verwendet werden, von denen viele vordefiniert sind. Gerätehersteller können neue Kategorien und Typen erstellen, indem sie bei Bedarf neue GUIDs definieren und veröffentlichen.

Standortgeräte machen eine besonders interessante Kategorie aus. Mittlerweile sind die meisten Personen mit globalen Positionierungssystemen (GPS) vertraut. In Windows ist ein GPS-Sensor Teil der Kategorie Standort. Die Kategorie Standort kann andere Sensortypen enthalten. Einige dieser Sensortypen sind softwarebasierte, z. B. ein IP-Konfliktlöser, der Standortinformationen basierend auf einer Internetadresse, einen Mobilfunkmastentriangulator, der den Standort anhand von nahe gelegenen Flüssen bestimmt, oder einen Wi-Fi-Netzwerkadressenanbieter, der Standortinformationen aus dem verbundenen Funknetzwerkhub liest.

## <a name="about-the-platform"></a>Informationen zur Plattform

Die Windows Sensor- und Standortplattform besteht aus den folgenden Entwickler- und Benutzerkomponenten:

-   Die DDI ermöglicht Windows eine Standard-Möglichkeit für Sensorgeräte, eine Verbindung mit dem Computer herzustellen und Daten für andere Subsysteme zur Verfügung zu stellen.
-   Die Windows Sensor-API bietet eine Reihe von Methoden, Eigenschaften und Ereignissen für die Arbeit mit verbundenen Sensoren und Sensordaten.
-   Die Windows Location-API, die auf der Windows Sensor-API basiert, bietet eine Reihe von Programmierobjekten, einschließlich Skriptobjekten, für die Arbeit mit Standortinformationen.
-   Mit Positions- und andere Sensoren Systemsteuerung können Computeradministratoren sensoren, einschließlich Standortsensoren, für jeden Benutzer festlegen.

In den folgenden Abschnitten wird jede dieser Komponenten beschrieben.

## <a name="architecture-diagram"></a>Architekturdiagramm

Das folgende Diagramm zeigt die Beziehung zwischen den Komponenten.

![Diagramm zur Sensor- und Standortplattform](images/platformarchitecture.png)

## <a name="device-driver-interface"></a>Gerätetreiberschnittstelle

Sensorhersteller können Gerätetreiber erstellen, um Sensoren mit Windows 7 zu verbinden. Sensorgerätetreiber werden mithilfe des Windows Portable Devices (WPD)-Treibermodells implementiert, das auf dem Windows User Mode Driver Framework (UMDF) basiert. Viele Gerätetreiber wurden mithilfe dieser Frameworks geschrieben. Da diese Technologien etabliert sind, finden erfahrene Programmierer von Gerätetreibern das Schreiben eines Sensortreibers als vertraute Aufgabe. Die Sensor-DDI verwendet bestimmte UMDF- und WPD-Datentypen und -Schnittstellen und definiert außerdem sensorspezifische WPD-Befehle und -Parameter, wo dies erforderlich ist. Weitere Informationen zum Erstellen von Sensorgerätetreibern finden Sie im Windows Driver Kit.

## <a name="sensor-api"></a>Sensor-API

Mit der Sensor-API können C++-Entwickler sensorbasierte Programme mithilfe einer Reihe von COM-Schnittstellen erstellen. Die API definiert Schnittstellen, um allgemeine Aufgaben zur Sensorprogrammierung auszuführen, z. B. das Verwalten von Sensoren nach Kategorie, Typ oder ID, das Verwalten von Sensorereignissen, das Arbeiten mit einzelnen Sensoren und Sensorsammlungen und das Arbeiten mit Sensordaten. Das Windows SDK enthält Headerdateien, Dokumentationen, Beispiele und Tools, die Softwareentwickler bei der Verwendung von Sensoren in Windows unterstützen. In dieser Dokumentation wird die Sensor-API beschrieben.

## <a name="location-api"></a>Standort-API

Die Standort-API basiert auf der Sensor-API und bietet eine einfache Möglichkeit, Daten über den geografischen Standort abzurufen und gleichzeitig die Privatsphäre der Benutzer zu schützen. Die Location-API stellt ihre Funktionalität über eine Reihe von COM-Schnittstellen bereit, die Objekte darstellen. Diese Objekte können von Programmierern verwendet werden, die die Verwendung von COM über die Programmiersprache C++ oder in Skriptsprachen wie JScript. Die Skriptunterstützung bietet einfachen Zugriff auf Standortdaten für Projekte, die in der Zone Lokaler Computer ausgeführt werden, z. B. Gadgets. Das Windows SDK enthält Headerdateien, Dokumentation (einschließlich Referenzdokumentation zur Skripterstellung), Beispiele und Tools, die Web- und Softwareentwickler bei der Verwendung von Standortinformationen in ihren Programmen unterstützen.

## <a name="location-and-other-sensors-control-panel"></a>Positions- und andere Sensoren Systemsteuerung

Windows 7 enthält eine Systemsteuerung, mit der Computeradministratoren sensoren systemweit oder für jeden Benutzer aktivieren oder deaktivieren können. Da einige Sensoren sensible Daten verfügbar machen können, können Administratoren über diese Benutzeroberfläche steuern, ob alle Programme für jeden Benutzer Zugriff auf die einzelnen Sensoren haben. Benutzer können auch Sensoreigenschaften anzeigen und die Sensorbeschreibung ändern, die auf der Benutzeroberfläche angezeigt wird.

Der Systemsteuerung stellt auch eine Seite Standardspeicherort zur Verfügung, auf der Benutzer ihren Standort bereitstellen können. Wenn kein Sensor verfügbar ist, verwendet die Plattform den vom Benutzer bereitgestellten Standort. Benutzer können Felder für Bürgeradressen angeben, z. B. Die Adresse der Straße, die Stadt, das Bundesland oder die Provinz sowie das Land oder die Region.

## <a name="related-topics"></a>Zugehörige Themen

[Informationen zur Sensor-API](about-the-sensor-api.md)

[Windows Hardware Developer Central-Website](https://www.microsoft.com/whdc/device/sensors/default.mspx)

[Windows Developer Center](https://msdn.microsoft.com/windows/default.aspx?wt.svl=client)
