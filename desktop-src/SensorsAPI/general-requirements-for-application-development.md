---
description: In diesem Thema wird beschrieben, was Sie tun müssen, um Programme zu erstellen, die die Sensor-API verwenden.
ms.assetid: a8d3228a-5f8b-4850-9e47-5dfb2335e655
title: Allgemeine Anforderungen für die Anwendungsentwicklung (Sensor-API)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 148057cd837e8eef26e73ff9cdef07ca01c70cb4a107e5f6e77f9ca43487407d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119003778"
---
# <a name="general-requirements-for-application-development-sensor-api"></a>Allgemeine Anforderungen für die Anwendungsentwicklung (Sensor-API)

In diesem Thema wird beschrieben, was Sie tun müssen, um Programme zu erstellen, die die Sensor-API verwenden.

Zum Erstellen einer Sensor-API-Anwendung müssen Sie Windows 7 und das Windows 7 Software Development Kit (SDK) auf Ihrem Computer installieren. In der folgenden Tabelle werden die spezifischen Dateien beschrieben, die Sie benötigen.



| Dateiname               | BESCHREIBUNG                                                                                                 |
|-------------------------|-------------------------------------------------------------------------------------------------------------|
| Sensorsapi.h            | Die Hauptheaderdatei für die Sensor-API. Diese Headerdatei enthält die Schnittstellendefinitionen.               |
| Sensors.h               | Die Headerdatei, die Definitionen plattformdefinierter Konstanten enthält.                                    |
| Initguid.h              | Die Headerdatei, die Definitionen zum Steuern der **GUID-Initialisierung** enthält.                          |
| FunctionDiscoveryKeys.h | Die Headerdatei, die Geräte-ID-Eigenschaftsschlüssel definiert, die erforderlich sind, wenn Sie eine Verbindung mit logischen Sensoren herstellen. |
| Sensorsapi.lib          | Eine statische Bibliothek, die **GUID-Definitionen** für die Sensor-API enthält.                                     |
| PortableDeviceGuids.lib | Eine statische Bibliothek, die **GUID-Definitionen** für Windows Portable Devices-Objekte enthält.                   |



 

Ihr Programm erfordert möglicherweise zusätzliche Dateien.

## <a name="supported-operating-systems"></a>Unterstützte Betriebssysteme

Sensor-API-Anwendungen werden in allen Editionen von Windows 7 ausgeführt, mit Ausnahme der Windows 7 Starter Edition.

## <a name="windows-portable-devices-interfaces"></a>Windows Schnittstellen für portable Geräte

Die Sensor-API verwendet bestimmte Windows Portable Devices (WPD)-Objekte, um Eigenschaftsschlüssel und -werte zu kapseln. In der folgenden Tabelle werden die Schnittstellen für diese Objekte beschrieben.



| Schnittstelle                                                                       | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                                                                                            |
|---------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [IPortableDeviceValues](/previous-versions//ms740012(v=vs.85))        | Diese Schnittstelle bietet eine praktische Möglichkeit, eine Eigenschaftentüte mit Name-Wert-Paaren zu erstellen. Namen werden durch **PROPERTYKEY-Werte** und Werte durch **PROPVARIANT-s** dargestellt. <br/> Die API verwendet diese Schnittstelle zum Festlegen und Abrufen von einzelnen Werten und Sätzen von Werten. Diese Schnittstelle kann von einer Methode oder, wenn ein neues Objekt erforderlich ist, durch Aufrufen von **CoCreateInstance** mit CLSID \_ PortableDeviceValues abgerufen werden.<br/> |
| [IPortableDeviceKeyCollection](/previous-versions//ms739549(v=vs.85)) | Diese Schnittstelle enthält eine Auflistung von **PROPERTYKEY-s.** Diese Schlüssel stellen Eigenschaftsnamen dar, die von **IPortableDeviceValues gespeichert werden können.** Die API verwendet dieses Sammlungsobjekt zum Festlegen und Abrufen von einzelnen Eigenschaftennamen und Sätzen von Eigenschaftsnamen.<br/> Diese Schnittstelle kann von einer Methode oder, wenn ein neues Objekt erforderlich ist, durch Aufrufen von **CoCreateInstance** mit CLSID \_ PortableDeviceKeyCollection abgerufen werden. <br/>    |



 

 

