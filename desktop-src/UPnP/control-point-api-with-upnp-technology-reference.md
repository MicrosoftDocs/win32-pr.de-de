---
title: Referenz zur Kontrollpunkt-API
description: Die folgenden Schnittstellen sind Teil der Steuerungspunkt-API mit UPnP-Technologie. Die Steuerungspunkt-API unterstützt Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic und C++.
ms.assetid: 6f73bf8c-0423-430f-a654-58d076712aae
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 24b3dab16874ebeb7b43ef1e8cf28def13d3ef1d7169a5aae4836b39da66636b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119058118"
---
# <a name="control-point-api-reference"></a>Referenz zur Kontrollpunkt-API

Die folgenden Schnittstellen sind Teil der Steuerungspunkt-API mit UPnP-Technologie. Die Steuerungspunkt-API unterstützt Microsoft Visual Basic Scripting Edition (VBScript), Microsoft Visual Basic und C++.



| Schnittstelle                                                                                      | BESCHREIBUNG                                                                                                                                                                                                                    |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPAddressFamilyControl**](/windows/desktop/api/Upnp/nn-upnp-iupnpaddressfamilycontrol)                                 | Ermöglicht einer Anwendung den Zugriff auf das Adressfamilienflag des Device Finder-Objekts.                                                                                                                                          |
| [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument)                                   | Ermöglicht einer Anwendung das Laden einer Gerätebeschreibung. Diese Schnittstelle ist sicher für die Skripterstellung.                                                                                                                                     |
| [**IUPnPDescriptionDocumentCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocumentcallback)                   | Ermöglicht es einer Anwendung, die Ergebnisse eines asynchronen Ladevorgang zu empfangen.                                                                                                                                               |
| [**IUPnPDevice**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevice)                                                             | Ermöglicht einer Anwendung das Abrufen von Informationen zu einem bestimmten Gerät.                                                                                                                                                        |
| [**IUPnPDeviceDocumentAccess**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccess)                                 | Ermöglicht einer Anwendung das Abrufen der URL eines Gerätebeschreibungsdokuments.                                                                                                                                                     |
| [**IUPnPDeviceDocumentAccessEx**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicedocumentaccessex)                             | Stellt eine Methode zum Abrufen des gesamten XML-Gerätebeschreibungsdokuments für ein bestimmtes Gerät zur                                                                                                                                  |
| [**IUPnPDeviceGrad**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder)                                                 | Ermöglicht es einer Anwendung, ein Gerät zu finden.                                                                                                                                                                                       |
| [**IUPnPDeviceGradAddCallbackWithInterface**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinderaddcallbackwithinterface) | Ermöglicht es einer Anwendung, asynchrone Suchergebnisse aus dem UPnP-Framework zusammen mit der GUID des Netzwerkadapters zu erhalten, über den die Geräteanzeige stammt.                                                  |
| [**IUPnPDeviceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefindercallback)                                 | Ermöglicht es einer Anwendung, asynchrone Suchergebnisse aus dem UPnP-Framework zu empfangen.                                                                                                                                         |
| [**IUPnPDevices**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevices)                                                           | Enumeriert eine Sammlung von Geräten.                                                                                                                                                                                            |
| [**IUPnPHttpHeaderControl**](/windows/desktop/api/Upnp/nn-upnp-iupnphttpheadercontrol)                                       | Ermöglicht einer Anwendung das Festlegen von HTTP-Headern des "Benutzer-Agents" von Klasseninstanzen, die [**die Schnittstellen IUPnPDeviceGrad**](/windows/desktop/api/Upnp/nn-upnp-iupnpdevicefinder) oder [**IUPnPDescriptionDocument**](/windows/desktop/api/Upnp/nn-upnp-iupnpdescriptiondocument) implementieren. |
| [**IUPnPService**](/windows/desktop/api/Upnp/nn-upnp-iupnpservice)                                                           | Ermöglicht einer Anwendung das Abrufen von Zustandsinformationen und das Aufrufen von Aktionen für einen Dienst.                                                                                                                                         |
| [**IUPnPServiceAsync**](/windows/desktop/api/Upnp/nn-upnp-iupnpserviceasync)                                                 | Asynchrones Abfragen von Zustandsvariablen und Aufrufen von Aktionen für eine Instanz eines Diensts.                                                                                                                                           |
| [**IUPnPServiceCallback**](/windows/desktop/api/Upnp/nn-upnp-iupnpservicecallback)                                           | Ermöglicht es einer Anwendung, Benachrichtigungen vom UPnP-Framework zu empfangen, wenn Ereignisse auftreten.                                                                                                                                      |
| [**IUPnPServices**](/windows/desktop/api/Upnp/nn-upnp-iupnpservices)                                                         | Enumeriert eine Auflistung von Diensten.                                                                                                                                                                                           |



 

 

 




