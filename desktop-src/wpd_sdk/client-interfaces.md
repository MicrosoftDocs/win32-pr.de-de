---
description: Clientschnittstellen
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: Clientschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b44db8fdd42b20fb2ff7a3224bccf5214147069baa9187facdb1c832c375a59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119590394"
---
# <a name="client-interfaces"></a>Clientschnittstellen

Anwendungen verwenden die methoden, die von den folgenden Schnittstellen unterstützt werden, um Vorgänge auf portablen Geräten durchzuführen. Zu diesen Vorgängen gehören das Öffnen einer Verbindung mit einem Gerät, das Abrufen von Daten von einem Gerät, das Schreiben von Daten auf ein Gerät und so weiter.



| Schnittstelle                                                                              | BESCHREIBUNG                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IEnumPortableDeviceObjectIDs**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)                   | Enumeriert die Objekte auf einem portablen Gerät.                                                                                                                                                                                        |
| [**IPortableDevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                                             | Bietet Low-Level-Zugriff auf ein portables Gerät.                                                                                                                                                                                     |
| [**IPortableDeviceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                     | Ruft eine Vielzahl von Gerätefunktionen ab, einschließlich unterstützter Formate, Befehle und funktionaler Objekte.                                                                                                                          |
| [**IPortableDeviceContent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                               | Stellt Methoden zum Erstellen, Aufzählen und Löschen von Inhalten auf einem Gerät zur Seite.                                                                                                                                                              |
| [**IPortableDeviceDataStream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)                         | Macht zusätzliche Methoden für einen **IStream verfügbar, der** für Datenübertragungen verwendet wird.                                                                                                                                                               |
| [**IPortableDeviceEventCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)                   | Wird von der Anwendung implementiert, um asynchrone Rückrufe zu empfangen.                                                                                                                                                                   |
| [**IPortableDeviceManager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)                               | Aufzählen von Geräten, die mit dem Computer verbunden sind, und bietet eine einfache Möglichkeit zum Anfordern von Installationsinformationen für das Gerät (einschließlich Hersteller, Angezeigter Name und Beschreibung).                                       |
| [**IPortableDeviceProperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                         | Lesen und Schreiben von Eigenschaften für ein Objekt auf dem Gerät.                                                                                                                                                                              |
| [**IPortableDevicePropertiesBulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)                 | Liest und schreibt asynchron mehrere Eigenschaften für mehrere Objekte auf einem Gerät.                                                                                                                                               |
| [**IPortableDevicePropertiesBulkCallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback) | Wird von der Anwendung implementiert, um den Fortschritt eines asynchronen Vorgangs zu verfolgen, der mithilfe der **IPortableDevicePropertiesBulk-Schnittstelle gestartet** wurde.                                                                          |
| [**IPortableDeviceResources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)                           | Ermöglicht den Zugriff auf die Daten eines Objekts.                                                                                                                                                                                                |
| [**IPortableDeviceService**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | Windows 7. Bietet Low-Level-Zugriff auf einen portablen Gerätedienst.                                                                                                                                                             |
| [**IPortableDeviceServiceCapabilities**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | Windows 7. Ruft eine Vielzahl von Dienstfunktionen ab, einschließlich unterstützter Formate, Befehle, Methoden und Renderingprofile.                                                                                                |
| [**IPortableDeviceServiceMethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | Windows 7. Ruft Methoden synchron und asynchron für einen Dienst auf.                                                                                                                                                      |
| [**IPortableDeviceServiceMethodCallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | Windows 7. Wird von der Anwendung implementiert, um den Abschluss eines asynchronen Dienstmethodenvorgang zu verfolgen, der durch Aufrufen von [ **IPortableDeviceServiceMethods::InvokeAsync begonnen wurde.**](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**IPortableDeviceServiceManager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | Windows 7. Listet Dienste auf, die von einem Gerät unterstützt werden, und ruft das gerät ab, das einem Dienst zugeordnet ist.                                                                                                             |



 

Das folgende Diagramm zeigt, wie eine Anwendung die meisten benötigten Schnittstellen erhält. Nicht alle Methoden aller Schnittstellen oder Schnittstellen, die von der Anwendung implementiert werden, werden angezeigt.

![Diagramm, das das Erstellen und Abrufen der meisten erforderlichen Clientschnittstellen zeigt](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 



