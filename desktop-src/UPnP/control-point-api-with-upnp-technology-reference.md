---
title: API-Referenz für Steuerungspunkt
description: Die folgenden Schnittstellen sind Teil der Steuerungspunkt-API mit UPnP-Technologie. Die Kontrollpunkt-API unterstützt Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic und C++.
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 691a0d764f612d957ac11b3b052859f081bc7285
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104309696"
---
# <a name="control-point-api-reference"></a>API-Referenz für Steuerungspunkt

Die folgenden Schnittstellen sind Teil der Steuerungspunkt-API mit UPnP-Technologie. Die Kontrollpunkt-API unterstützt Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic und C++.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iupnpaddressfamilycontrol**](/windows/desktop/api/Upnp/nn-upnp-iupnpaddressfamilycontrol)                                 | Ermöglicht es einer Anwendung, auf das Adress familienflag des Device Finder-Objekts zuzugreifen.                                                                                                                                          |
| [**Iupnpdescriptiondocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)                                   | Ermöglicht es einer Anwendung, eine Geräte Beschreibung zu laden. Diese Schnittstelle ist für die Skripterstellung sicher.                                                                                                                                     |
| [**Iupnpdescriptiondocumentcallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocumentcallback)                   | Ermöglicht es einer Anwendung, die Ergebnisse eines asynchronen Ladevorgangs zu empfangen.                                                                                                                                               |
| [**Iupnpdevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)                                                             | Ermöglicht einer Anwendung das Abrufen von Informationen zu einem bestimmten Gerät.                                                                                                                                                        |
| [**Iupnpdevicedocumentaccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess)                                 | Ermöglicht einer Anwendung das Abrufen der URL eines Geräte Beschreibungs Dokuments.                                                                                                                                                     |
| [**Iupnpdevicedocumentaccessex**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccessex)                             | Stellt eine Methode zum Abrufen des gesamten XML-Geräte Beschreibungs Dokuments für ein bestimmtes Gerät bereit.                                                                                                                                  |
| [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)                                                 | Ermöglicht einer Anwendung das Auffinden eines Geräts.                                                                                                                                                                                       |
| [**Iupnpdevicefinderaddcallbackwithinterface**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface) | Ermöglicht es einer Anwendung, asynchrone Suchergebnisse aus dem UPnP-Framework zusammen mit der GUID des Netzwerkadapters zu empfangen, über den die Geräte Ankündigung erfolgte.                                                  |
| [**Iupnpdevicefindercallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback)                                 | Ermöglicht es einer Anwendung, asynchrone Suchergebnisse aus dem UPnP-Framework zu empfangen.                                                                                                                                         |
| [**Iupnpdevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)                                                           | Listet eine Auflistung von Geräten auf.                                                                                                                                                                                            |
| [**Iupnphttpheadercontrol**](/windows/desktop/api/Upnp/nn-upnp-iupnphttpheadercontrol)                                       | Ermöglicht einer Anwendung das Festlegen von HTTP-Headern vom Typ "User Agent" aus Klassen Instanzen, die die [**IUPnPDeviceFinder**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) -oder [**iupnpdescriptiondocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) -Schnittstellen implementieren. |
| [**Iupnpservice**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)                                                           | Ermöglicht es einer Anwendung, Zustandsinformationen abzurufen und Aktionen für einen Dienst aufzurufen.                                                                                                                                         |
| [**Iupnpserviceasync**](/windows/desktop/api/Upnp/nn-upnp-iupnpserviceasync)                                                 | Asynchrones Abfragen von Zustandsvariablen und Aufrufen von Aktionen für eine Instanz eines Diensts.                                                                                                                                           |
| [**Iupnpservicecallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpservicecallback)                                           | Ermöglicht es einer Anwendung, Benachrichtigungen vom UPnP-Framework zu empfangen, wenn Ereignisse auftreten.                                                                                                                                      |
| [**Iupnpservices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices)                                                         | Listet eine Auflistung von Diensten auf.                                                                                                                                                                                           |



 

 

 




