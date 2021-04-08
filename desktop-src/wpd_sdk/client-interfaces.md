---
description: Client Schnittstellen
ms.assetid: fbe53f17-940a-485e-82b2-c11ae39b3300
title: Client Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5d7c85ec5cb9b35e30d68b1d784cdebf230fdaa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866524"
---
# <a name="client-interfaces"></a>Client Schnittstellen

Anwendungen verwenden die Methoden, die von den folgenden Schnittstellen unterstützt werden, um Vorgänge auf tragbaren Geräten auszuführen. Zu diesen Vorgängen gehören das Öffnen einer Verbindung mit einem Gerät, das Abrufen von Daten von einem Gerät, das Schreiben von Daten auf ein Gerät usw.



| Schnittstelle                                                                              | BESCHREIBUNG                                                                                                                                                                                                                         |
|----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ienumportabledeviceobjectids**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-ienumportabledeviceobjectids)                   | Listet die Objekte auf einem tragbaren Gerät auf.                                                                                                                                                                                        |
| [**Iportabledevice**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevice)                                             | Ermöglicht den Zugriff auf ein tragbares Gerät auf niedriger Ebene.                                                                                                                                                                                     |
| [**Iportabledecovicecapabili**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)                     | Ruft eine Vielzahl von Gerätefunktionen ab, einschließlich unterstützter Formate, Befehle und funktionaler Objekte.                                                                                                                          |
| [**Iportabledevicecontent**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecontent)                               | Stellt Methoden zum Erstellen, aufzählen und Löschen von Inhalten auf einem Gerät bereit.                                                                                                                                                              |
| [**Iportabledevicedatastream**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicedatastream)                         | Macht zusätzliche Methoden für einen **IStream** verfügbar, der für Datenübertragungen verwendet wird.                                                                                                                                                               |
| [**Iportabledeviceeventcallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceeventcallback)                   | Wird von der Anwendung implementiert, um asynchrone Rückrufe zu empfangen.                                                                                                                                                                   |
| [**Iportabledebug-Manager**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicemanager)                               | Listet Geräte auf, die mit dem Computer verbunden sind, und bietet eine einfache Möglichkeit, Installationsinformationen für das Gerät anzufordern (einschließlich Hersteller, Anzeige Name und Beschreibung).                                       |
| [**Iportabledeviceproperties**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledeviceproperties)                         | Lese-und Schreib Eigenschaften für ein Objekt auf dem Gerät.                                                                                                                                                                              |
| [**Iportabledevicepropertiesbulk**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulk)                 | Liest und schreibt mehrere Eigenschaften für mehrere Objekte auf einem Gerät asynchron.                                                                                                                                               |
| [**Iportabledevicepropertiesbulkcallback**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledevicepropertiesbulkcallback) | Wird von der Anwendung implementiert, um den Fortschritt eines asynchronen Vorgangs zu verfolgen, der mit der **iportabledevicepropertiesbulk** -Schnittstelle begonnen wurde.                                                                          |
| [**Iportabledeviceresources**](/windows/desktop/api/PortableDeviceApi/nn-portabledeviceapi-iportabledeviceresources)                           | Ermöglicht den Zugriff auf die Daten eines Objekts.                                                                                                                                                                                                |
| [**Iportablede viceservice**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservice)                               | Nur Windows 7. Bietet Zugriff auf niedriger Ebene auf einen Dienst für tragbare Geräte.                                                                                                                                                             |
| [**Iportablede viceservicecapabili**](/windows/desktop/api/portabledeviceapi/nn-portabledeviceapi-iportabledevicecapabilities)              | Nur Windows 7. Ruft eine Vielzahl von Dienstfunktionen ab, einschließlich unterstützter Formate, Befehle, Methoden und renderingprofile.                                                                                                |
| [**Iportabledeviceservicemethods**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethods)                 | Nur Windows 7. Ruft Methoden synchron und asynchron für einen Dienst auf.                                                                                                                                                      |
| [**Iportablede viceservicemethodcallback**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemethodcallback)   | Nur Windows 7. Wird von der Anwendung implementiert, um den Abschluss eines asynchronen Dienst Methoden Vorgangs zu verfolgen, der durch den Aufruf von [ **iportabledeviceservicemethods:: InvokeAsync** begonnen wurde.](/windows/desktop/api/PortableDeviceAPI/nf-portabledeviceapi-iportabledeviceservicemethods-invokeasync) |
| [**Iportablede viceservicemanager**](/windows/desktop/api/PortableDeviceAPI/nn-portabledeviceapi-iportabledeviceservicemanager)                 | Nur Windows 7. Listet die Dienste auf, die von einem Gerät unterstützt werden, und ruft das Gerät ab, das einem Dienst zugeordnet ist.                                                                                                             |



 

Im folgenden Diagramm wird gezeigt, wie eine Anwendung die meisten benötigten Schnittstellen abruft. Es werden nicht alle Methoden aller Schnittstellen oder Schnittstellen angezeigt, die von der Anwendung implementiert werden.

![Diagramm, das die Erstellung und den Abruf der meisten erforderlichen Client Schnittstellen anzeigt](images/wpd-sdk-interface-diagram.gif)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Programmierverzeichnis**](programming-reference.md)
</dt> </dl>

 

 



