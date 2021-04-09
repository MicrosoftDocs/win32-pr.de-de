---
description: .
ms.assetid: 0182461a-df06-46ea-a9c2-7aedbde5033b
title: Location-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f643565e80f72ffcefe6981c924b3739b1c4f5f0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103864872"
---
# <a name="location-api"></a>Location-API

\[Die Win32-Speicherort-API und ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API. Verwenden Sie die [W3C-geolozierungs-API](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85)), um auf den Speicherort von einer Website zuzugreifen. \]

## <a name="purpose"></a>Zweck

Computer sind heute mobiler als je zuvor. Von kleinen Laptops bis hin zu Tablet PCs können viele Computer überall dort unterwegs sein, wo der Benutzer unterwegs ist. Programme, die die Mobilität des Computers nutzen, können dem Leben der Menschen einen beträchtlichen nutzen verleihen. Beispielsweise wäre ein Programm, das in Restaurants in der Nähe von Restaurants suchen und Führungs Richtungen bereitstellen könnte, eine natürliche Anpassung für einen tragbaren Computer. Obwohl die Technologie zum Ermitteln des aktuellen Standorts des Benutzers allgemein und kostengünstig ist, kann das Entwickeln von Lösungen auf dieser Technologie eine gewaltige Aufgabe sein.

Um ein Standort fähiges Programm zu erstellen, müssen Sie möglicherweise eine Vielzahl von Problemen überwinden, einschließlich:

-   Geräte des globalen Positions Systems (GPS), die virtuelle COM-Ports verwenden, die jeweils nur für ein Programm den Zugriff ermöglichen.
-   Verstehen und Programmieren für Protokolle, wie z. b. die Spezifikation der National Marine Electronics Association (NMEA), sowie proprietäre Lieferanten Erweiterungen.
-   Sie sind auf die Programmierung bekannter, vertikaler Hardwarelösungen beschränkt.
-   Implementieren von Logik zur Handhabung von Übergängen zwischen verschiedenen Standort Anbietern, z. b. GPS-Empfängern, verbundenen Netzwerken, Mobil Telefonnetzwerken, Internet und Benutzereinstellungen.

In dieser Dokumentation wird die Windows-Location-API (Application Programming Interface) beschrieben. Mit der Location-API können Sie die Standort bewusste Programmierung vereinfachen, indem Sie eine Standardmethode zum Abrufen von Daten über den Benutzer Speicherort und zur Standardisierung von Formaten für Standortdaten Berichte bereitstellen. Die Location-API übernimmt automatisch die Übergänge Zwischenstandort Datenanbietern und wählt immer den genauesten Anbieter für die aktuelle Situation aus.

## <a name="developer-audience"></a>Entwicklergruppe

Die Location-API stellt die Funktionalität über einen Satz von COM-Schnittstellen bereit. Location-API-Funktionen können von Programmierern verwendet werden, die mit der Verwendung von com über die Programmiersprache C++ oder mit COM-Objekten in Skriptsprachen, wie z. b. Microsoft JScript, vertraut sind.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Location-API C++ Programmier Referenz](windows-location-programming-reference.md)
-   [Speicherort-API-Objektmodell Referenz](windows-location-script-programming-reference.md)

 

 
