---
description: Die Location-API definiert die folgenden Enumerationstypen.
ms.assetid: a1d9d274-2861-4818-8fa1-d8d66edf27b3
title: Strukturen und Enumerationstypen (Location-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67a73c27cb2ad6dc0dcd0c2b92f4e9ba52e98fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106359158"
---
# <a name="structures-and-enumeration-types-location-api"></a>Strukturen und Enumerationstypen (Location-API)

\[Die Win32-Location-API ist für die Verwendung in den Betriebssystemen verfügbar, die im Abschnitt "Anforderungen" angegeben sind. Es kann in nachfolgenden Versionen geändert oder entfernt werden. Verwenden Sie stattdessen die [**Windows. Devices. Geolokation**](/uwp/api/Windows.Devices.Geolocation) -API. \]

Die Location-API definiert die folgenden Enumerationstypen.



| Enumeration                                                                       | Beschreibung                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------|
| [**\_gewünschte \_ Genauigkeit für Speicherort**](/previous-versions/windows/desktop/legacy/dd756639(v=vs.85))                  | Definiert die möglichen gewünschten Genauigkeits Typen.                         |
| [**Standort \_ \_ Status Bericht**](/windows/win32/api/locationapi/ne-locationapi-location_report_status) | Definiert den möglichen Status für neue Berichte eines bestimmten Berichts Typs. |



 

## <a name="location-constants-from-the-sensor-api"></a>Location-Konstanten von der Sensor-API

Die Sensor-API definiert auch standortbezogene Eigenschaften Schlüssel und-Konstanten. Die in "Sensors. h" definierten Eigenschafts Schlüssel können zum Abrufen von Standortdaten aus einem Bericht durch Aufrufen von " [**ilocationreport:: GetValue**](/windows/win32/api/locationapi/nf-locationapi-ilocationreport-getvalue)" verwendet werden.

 

 
