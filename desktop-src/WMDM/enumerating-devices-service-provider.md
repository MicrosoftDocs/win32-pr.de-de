---
title: Aufzählen von Geräten (WMDM)
description: Windows Media Geräte-Manager verwaltet einen Cache verbundener Geräte. Erfahren Sie, wie Windows Media Geräte-Manager den Cache verwaltet oder aktualisiert.
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Media Geräte-Manager,Aufzählen von Geräten
- Geräte-Manager,Aufzählen von Geräten
- Programmierhandbuch,Aufzählen von Geräten
- Dienstanbieter,Aufzählen von Geräten
- Erstellen von Dienstanbietern,Aufzählen von Geräten
- Aufzählen von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f9b2fd3a891e2c52710bd9a2f6d46a78e9eb238
ms.sourcegitcommit: 51ef825fb48f15e1aa30e8795988f10dc2b2155c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/14/2021
ms.locfileid: "112067907"
---
# <a name="enumerating-devices-wmdm"></a>Aufzählen von Geräten (WMDM)

Windows Media Device Manager maintains a cache of connected devices that is updated when a Windows Media Device Manager application starts, when a Plug and Play (PnP) device connects or disconnects, or when the application calls [**IWMDeviceManager2::Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize). Dieser Cache wird für die Anwendung verfügbar gemacht, wenn [**sie IWMDeviceManager::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) oder [**IWMDeviceManager2::EnumDevices2 aufruft.**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2) Jedes Gerät wird als [**IWMDMDevice-Schnittstelle**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) für die Anwendung verfügbar gemacht. Wenn der Dienstanbieter für die Handhabung von PnP-Geräten registriert ist, Geräte-Manager Windows Media Geräte-Manager die aktuelle Liste der verbundenen Geräte. Wenn der Dienstanbieter für die Verarbeitung von Nicht-PnP-Geräten registriert ist, ist der Dienstanbieter für die Suche nach angeschlossenen Geräten verantwortlich. Ein Dienstanbieter kann nur für PnP- oder Nicht-PnP-Geräte registriert werden, nie für beides.

Die folgenden Aktionen zeigen, wie Windows Media Geräte-Manager ihren Cache verwaltet oder aktualisiert. Beachten Sie, dass der Cache nie aktualisiert wird, wenn ein Nicht-PnP-Gerät eine Verbindung herstellt oder die Verbindung trennt.

Eine Windows Media Geräte-Manager-Anwendung wird gestartet

-   Windows Media Geräte-Manager ruft eine Liste der angeschlossenen PnP-Geräte aus dem PnP-Subsystem ab und ruft [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) auf dem SP auf, der für jedes verbundene Gerät registriert ist. (Der richtige Dienstanbieter wird durch Abfragen des WMDMSPCLSID-Geräteparameters nach der Klassen-ID des für dieses Gerät zuständigen Dienstanbieters gefunden. Weitere [Informationen finden Sie](device-parameters.md) unter Geräteparameter.) Alle zurückgegebenen Geräte werden dem Windows Media-Geräte-Manager von Geräten hinzugefügt.
-   Windows Media Geräte-Manager sucht alle bei ihm registrierten Nicht-PnP-Dienstanbieter und ruft [**IMDServiceProvider::EnumDevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) auf jedem Dienstanbieter auf, um von jedem Dienstanbieter eine Liste der Geräte zu erhalten. Alle zurückgegebenen Geräte werden dem Cache hinzugefügt.

Die Anwendung ruft IWMDeviceManager/2::EnumDevices/2 auf.

-   Windows Media Geräte-Manager gibt die zwischengespeicherte Geräteliste zurück.

Ein PnP-Gerät stellt eine Verbindung

-   Windows Media Geräte-Manager sucht den entsprechenden Dienstanbieter und ruft **IMDServiceProvider2::CreateDevice** auf und fügt das Gerät dem Cache hinzu.
-   Wenn die Anwendung [**IWMDMNotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)implementiert, ruft Windows Media Geräte-Manager [**IWMDMNotification::WMDMMessage**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) mit einer Ankunftsbenachrichtigung auf.

Die Verbindung eines PnP-Geräts wird getrennt.

-   Windows Media Geräte-Manager entfernt das Element aus dem Cache.
-   Wenn die Anwendung IWMDMNotification implementiert, ruft Windows Media Geräte-Manager IWMDMNotification::WMDMMessage mit einer Abflugbenachrichtigung auf.

Die Anwendung ruft IWMDeviceManager2::Reinitialize auf.

-   Aktualisiert den Cache mit allen verbundenen Geräten.

Ein Nicht-PnP-Gerät verbindet oder trennt die Verbindung.

-   Windows Media Geräte-Manager wird nicht über die Ankunft oder den Abflug informiert und führt keine Maßnahmen aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 




