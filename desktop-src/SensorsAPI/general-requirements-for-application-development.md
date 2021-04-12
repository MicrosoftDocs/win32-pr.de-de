---
description: In diesem Thema wird beschrieben, was Sie tun müssen, um Programme zu erstellen, die die Sensor-API verwenden.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Allgemeine Anforderungen für die Anwendungsentwicklung (Sensor-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 31ec328f659bb51eddf93cc69beb2fe6236113ee
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347648"
---
# <a name="general-requirements-for-application-development-sensor-api"></a>Allgemeine Anforderungen für die Anwendungsentwicklung (Sensor-API)

In diesem Thema wird beschrieben, was Sie tun müssen, um Programme zu erstellen, die die Sensor-API verwenden.

Zum Erstellen einer Sensor-API-Anwendung müssen Sie Windows 7 und das Windows 7 Software Development Kit (SDK) auf dem Computer installieren. In der folgenden Tabelle werden die jeweiligen Dateien beschrieben, die Sie benötigen.



| Dateiname               | BESCHREIBUNG                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| Sensorsapi. h            | Die Haupt Header Datei für die Sensor-API. Diese Header Datei enthält die Schnittstellendefinitionen.               |
| Sensoren. h               | Die Header Datei, die Definitionen von Platt Form definierten Konstanten enthält.                                    |
| Initguid. h              | Die Header Datei, die Definitionen zum Steuern der **GUID** -Initialisierung enthält.                          |
| Functiondiscoverykeys. h | Die Header Datei, die die Eigenschaften Schlüssel der Geräte-ID definiert, die erforderlich sind, wenn Sie eine Verbindung mit logischen Sensoren herstellen. |
| Sensorsapi. lib          | Eine statische Bibliothek, die **GUID** -Definitionen für die Sensor-API enthält.                                     |
| Portabledeviceguids. lib | Eine statische Bibliothek, die **GUID** -Definitionen für Objekte von tragbaren Windows-Geräten enthält.                   |



 

Das Programm erfordert möglicherweise zusätzliche Dateien.

## <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

Sensor-API-Anwendungen können mit Ausnahme von Windows 7 Starter Edition unter allen Editionen von Windows 7 ausgeführt werden.

## <a name="windows-portable-devices-interfaces"></a>Schnittstellen für tragbare Windows-Geräte

Die Sensor-API verwendet bestimmte Windows Portable Devices-Objekte (WPD) zum Kapseln von Eigenschafts Schlüsseln und-Werten. In der folgenden Tabelle werden die Schnittstellen für diese Objekte beschrieben.



| Schnittstelle                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [Iportablede vicevalues](/previous-versions//ms740012(v=vs.85))        | Diese Schnittstelle stellt eine bequeme Möglichkeit zum Erstellen eines Eigenschaften Behälters mit Name-Wert-Paaren dar. Namen werden durch **PropertyKey** s dargestellt, und die Werte werden durch **PROPVARIANT** s dargestellt. <br/> Die API verwendet diese Schnittstelle zum Festlegen und Abrufen einzelner Werte und Werte Sätze. Diese Schnittstelle kann durch Aufrufen von **CoCreateInstance** mit CLSID portabledevicevalues aus einer Methode abgerufen werden oder, wenn ein neues Objekt erforderlich ist \_ .<br/> |
| [Iportabledevicekeycollection](/previous-versions//ms739549(v=vs.85)) | Diese Schnittstelle enthält eine Auflistung von **PropertyKey** s. Diese Schlüsselstellen Eigenschaftsnamen dar, die von **iportabletovicevalues** gespeichert werden können. Die API verwendet dieses Sammlungsobjekt zum Festlegen und Abrufen von einzelnen Eigenschaftsnamen und Sätzen von Eigenschaftsnamen.<br/> Diese Schnittstelle kann aus einer-Methode abgerufen werden, oder, wenn ein neues-Objekt erforderlich ist, durch Aufrufen von **CoCreateInstance** mit der CLSID \_ portabledevicekeycollection. <br/>    |



 

 

