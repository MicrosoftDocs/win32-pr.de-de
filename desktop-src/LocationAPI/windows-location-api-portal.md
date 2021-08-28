---
description: Standort-API
ms.assetid: 0182461a-df06-46ea-a9c2-7aedbde5033b
title: Standort-API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19850dc1f85b227f2a5c9e03d9e0130b70c42d38e7ca0bee6308f9963042c613
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119693110"
---
# <a name="location-api"></a>Standort-API

\[Die Win32-Speicherort-API und steht für die Verwendung in den Betriebssystemen zur Verfügung, die im Abschnitt Anforderungen angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [**Windows. Devices.Geolocation-API.**](/uwp/api/Windows.Devices.Geolocation) Verwenden Sie die [W3C-Geolocation-API,](/previous-versions/windows/internet-explorer/ie-developer/samples/gg589513(v=vs.85))um von einer Website aus auf den Standort zuzugreifen. \]

## <a name="purpose"></a>Zweck

Computer sind heute mobiler als je zuvor. Von kleinen Laptops bis hin zu Tablet-PCs können viele Computer überall dort sein, wo der Benutzer hin möchte. Programme, die die Mobilität des Computers nutzen, können das Leben von Menschen erheblich verbessern. Beispielsweise scheint ein Programm, das Restaurants in der Nähe finden und Wegbeschreibungen bereitstellen kann, eine natürliche Eignung für einen tragbaren Computer zu sein. Während die Technologie zum Bestimmen des aktuellen Standorts des Benutzers üblich und kostengünstig ist, kann das Erstellen von Lösungen auf dieser Technologie eine schwierige Aufgabe sein.

Um ein standortorientiertes Programm zu erstellen, müssen Sie möglicherweise eine Vielzahl von Problemen beheben, einschließlich:

-   GPS-Geräte (Global Positioning System), die virtuelle COM-Ports verwenden, die jeweils nur für ein Programm Zugriff bieten.
-   Kenntnisse und Programmierung für Protokolle, z. B. die NMEA-Spezifikation (National Sender Electronics Association) sowie proprietäre Anbietererweiterungen.
-   Beschränkt auf die Programmierung für bekannte, vertikale Hardwarelösungen.
-   Implementieren von Logik zum Verarbeiten von Übergängen zwischen verschiedenen Standortanbietern, z. B. GPS-Empfängern, verbundenen Netzwerken, Mobilfunknetzen, dem Internet und Benutzereinstellungen.

In dieser Dokumentation wird die Windows Application Programming Interface (API) für Speicherorte beschrieben. Die Standort-API vereinfacht die standortbezogene Programmierung, indem sie eine Standard-Möglichkeit zum Abrufen von Daten zum Benutzerstandort und zum Standardisieren von Formaten für Standortdatenberichte bereitstellt. Die Standort-API verarbeitet automatisch Übergänge zwischen Standortdatenanbietern und wählt immer den genauesten Anbieter für die aktuelle Situation aus.

## <a name="developer-audience"></a>Entwicklergruppe

Die Location-API stellt ihre Funktionalität über eine Reihe von COM-Schnittstellen bereit. Die Funktion der Standort-API kann von Programmierern verwendet werden, die mit der Verwendung von COM über die Programmiersprache C++ oder mit der Verwendung von COM-Objekten in Skriptsprachen wie Microsoft JScript vertraut sind.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [C++-Programmierreferenz zur Speicherort-API](windows-location-programming-reference.md)
-   [Referenz zum Objektmodell der Standort-API](windows-location-script-programming-reference.md)

 

 
