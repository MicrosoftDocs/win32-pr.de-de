---
title: Auflisten von Geräten (WMDM)
description: Auflisten von Geräten
ms.assetid: 7602da65-4c98-4766-b206-2129dad4cc2a
keywords:
- Windows Media Device Manager, Auflisten von Geräten
- Device Manager, Auflisten von Geräten
- Programmier Handbuch zum Auflisten von Geräten
- Dienstanbieter, Auflisten von Geräten
- Erstellen von Dienstanbietern, Auflisten von Geräten
- Auflisten von Geräten
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 316b87f6ad3f5680e0c22da832da7b1efec24629
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/23/2019
ms.locfileid: "103719553"
---
# <a name="enumerating-devices-wmdm"></a>Auflisten von Geräten (WMDM)

Windows Media Device Manager verwaltet einen Cache verbundener Geräte, die beim Starten einer Windows Media Device Manager-Anwendung aktualisiert werden, wenn ein Plug & Play (PNP)-Gerät eine Verbindung herstellt oder trennt oder wenn die Anwendung [**IWMDeviceManager2:: Reinitialize**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-reinitialize)aufruft. Dieser Cache wird für die Anwendung verfügbar gemacht, wenn er [**iwmdevicemanager:: enumdevices**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager-enumdevices) oder [**IWMDeviceManager2:: EnumDevices2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdevicemanager2-enumdevices2)aufruft. Jedes Gerät wird für die Anwendung als [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Schnittstelle verfügbar gemacht. Wenn der Dienstanbieter für die Behandlung von PNP-Geräten registriert ist, ist die aktuelle Liste der verbundenen Geräte in Windows Media Device Manager bekannt. Wenn der Dienstanbieter für die Behandlung von nicht-PnP-Geräten registriert ist, ist der Dienstanbieter für die Ermittlung angefügter Geräte verantwortlich. Ein Dienstanbieter kann nur für PNP-oder nicht-PNP-Geräte registriert werden.

Die folgenden Aktionen zeigen, wie der Cache von Windows Media Device Manager verwaltet oder aktualisiert wird. Beachten Sie, dass der Cache nie aktualisiert wird, wenn ein nicht-PNP-Gerät eine Verbindung herstellt oder die Verbindung trennt.

Ein Windows Media Device Manager-Anwendung wird gestartet.

-   Windows Media Device Manager ruft eine Liste angefügter PNP-Geräte aus dem PNP-Subsystem ab und ruft [**IMDServiceProvider2:: foratedevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) auf dem SP auf, der für jedes verbundene Gerät registriert ist. (Er ermittelt den korrekten Dienstanbieter durch Abfragen des wmdmspclsid-Geräte Parameters auf die Klassen-ID des für dieses Gerät Verantwortlichen Dienstanbieters. Weitere Informationen finden Sie unter [Geräteparameter](device-parameters.md) .) Alle zurückgegebenen Geräte werden dem Windows Media Device Manager-Cache von Geräten hinzugefügt.
-   Windows Media Device Manager findet alle nicht-PNP-Dienstanbieter, die bei ihm registriert sind, und ruft [**imdserviceprovider:: enumdevices**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider-enumdevices) für jeden Dienstanbieter auf, um eine Liste der Geräte von jedem Dienstanbieter zu erhalten. Alle zurückgegebenen Geräte werden dem Cache hinzugefügt.

Die Anwendung ruft iwmdevicemanager/2:: enumdevices/2 auf.

-   Die Liste der zwischengespeicherten Geräte wird von Windows Media Device Manager zurückgegeben.

Ein PNP-Gerät verbindet

-   Windows Media Device Manager findet den relevanten Dienstanbieter und ruft **IMDServiceProvider2:: anatedevice** auf und fügt das Gerät seinem Cache hinzu.
-   Wenn die Anwendung [**iwmdmnotification**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmnotification)implementiert, ruft Windows Media Device Manager mit einer Ankunfts Benachrichtigung [**iwmdmnotification:: wmdmmess**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmnotification-wmdmmessage) auf.

Ein PNP-Gerät trennt die Verbindung.

-   Windows Media Device Manager entfernt das Element aus dem Cache.
-   Wenn die Anwendung iwmdmnotification implementiert, ruft Windows Media Device Manager iwmdmnotification:: wmdmmess mit einer Abflug Benachrichtigung auf.

Die Anwendung ruft IWMDeviceManager2:: Reinitialize auf.

-   Aktualisiert den Cache mit allen verbundenen Geräten.

Ein nicht-PNP-Gerät stellt eine Verbindung her und trennt die Verbindung

-   Windows Media Device Manager wird nicht über die Ankunft oder den Abbruch informiert und führt keine Aktion aus.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 




