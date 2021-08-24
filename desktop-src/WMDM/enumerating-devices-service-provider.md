---
title: Auflisten von Geräten (WMDM)
description: Windows Medien Geräte-Manager verwaltet einen Cache verbundener Geräte. Erfahren Sie, wie Windows Media Geräte-Manager den Cache verwaltet oder aktualisiert.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Medien Geräte-Manager,Aufzählen von Geräten
- Geräte-Manager,Aufzählen von Geräten
- Programmierhandbuch,Aufzählen von Geräten
- Dienstanbieter, Aufzählen von Geräten
- Erstellen von Dienstanbietern, Aufzählen von Geräten
- Aufzählen von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 500375f01e718ab6f9824868ffabd7c83e11c3e812ce0288f0c15186bc1d2de9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119767050"
---
# <a name="enumerating-devices-wmdm"></a>Auflisten von Geräten (WMDM)

Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize). Dieser Cache wird für die Anwendung verfügbar gemacht, wenn [**er IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) oder [**IWMDeviceManager2::EnumDevices2 aufruft.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) Jedes Gerät wird der Anwendung als [**IWMDMDevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) verfügbar gemacht. Wenn der Dienstanbieter für die Verarbeitung von PnP-Geräten registriert ist, erkennt Windows Media Geräte-Manager die aktuelle Liste der verbundenen Geräte. Wenn der Dienstanbieter für die Verarbeitung von Nicht-PnP-Geräten registriert ist, ist der Dienstanbieter für die Ermittlung angefügter Geräte verantwortlich. Ein Dienstanbieter kann nur für PnP- oder Nicht-PnP-Geräte registriert werden, nie beides.

Die folgenden Aktionen zeigen, wie Windows Media Geräte-Manager den Cache verwaltet oder aktualisiert. Beachten Sie, dass der Cache nie aktualisiert wird, wenn ein Nicht-PnP-Gerät eine Verbindung herstellt oder die Verbindung trennt.

Eine Windows Media Geräte-Manager-Anwendung wird gestartet.

-   Windows Media Geräte-Manager ruft eine Liste der angefügten PnP-Geräte aus dem PnP-Subsystem ab und ruft [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) für den SP auf, der für jedes verbundene Gerät registriert ist. (Der richtige Dienstanbieter wird ermittelt, indem der WMDMSPCLSID-Geräteparameter nach der Klassen-ID des für dieses Gerät verantwortlichen Dienstanbieters abgefragt wird. Weitere Informationen finden Sie unter [Geräteparameter.)](device-parameters.md) Alle zurückgegebenen Geräte werden dem Windows Media Geräte-Manager Cache von Geräten hinzugefügt.
-   Windows Media Geräte-Manager sucht alle Nicht-PnP-Dienstanbieter, die bei ihm registriert sind, und ruft [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) für jeden Dienstanbieter auf, um von jedem Dienstanbieter eine Liste von Geräten abzurufen. Alle zurückgegebenen Geräte werden dem Cache hinzugefügt.

Die Anwendung ruft IWMDeviceManager/2::EnumDevices/2 auf.

-   Windows Medien Geräte-Manager gibt die zwischengespeicherte Geräteliste zurück.

Ein PnP-Gerät stellt eine Verbindung her.

-   Windows Media Geräte-Manager sucht den relevanten Dienstanbieter und ruft **IMDServiceProvider2::CreateDevice** auf und fügt das Gerät dem Cache hinzu.
-   Wenn die Anwendung [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)implementiert, ruft Windows Media Geräte-Manager [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) mit einer Eingangsbenachrichtigung auf.

Ein PnP-Gerät trennt die Verbindung

-   Windows Media Geräte-Manager entfernt das Element aus seinem Cache.
-   Wenn die Anwendung IWMDMNotification implementiert, ruft Windows Media Geräte-Manager IWMDMNotification::WMDMMessage mit einer Abflugbenachrichtigung auf.

Die Anwendung ruft IWMDeviceManager2::Reinitialize auf.

-   Aktualisiert den Cache mit allen verbundenen Geräten.

Ein Nicht-PnP-Gerät stellt eine Verbindung her oder trennt die Verbindung.

-   Windows Media Geräte-Manager wird nicht über die Ankunft oder Ankunft informiert und führt keine Maßnahmen aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 




