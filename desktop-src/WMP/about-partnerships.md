---
title: Informationen zu Partnerschaften
description: Informationen zu Partnerschaften
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player,Partnerschaften
- Windows Media Player Objektmodell,Partnerschaften
- Objektmodell,Partnerschaften
- Windows Media Player ActiveX Kontrolle, Partnerschaften
- ActiveX Kontrolle, Partnerschaften
- Windows Media Player Steuerung mobiler ActiveX,Partnerschaften
- Windows Media Player Mobil, Partnerschaften
- Synchronisieren von Geräten, Partnerschaften
- Gerätesynchronisierung,Partnerschaften
- Partnerschaften zwischen Geräten und Windows Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e4c018934ed06e5872d5866a463bdd909ea2501a1872ded29231be222572b2ae
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120004490"
---
# <a name="about-partnerships"></a>Informationen zu Partnerschaften

Eine Partnerschaft ist eine besondere Beziehung zwischen einem portablen Gerät und Windows Media Player. Benutzer können eine Partnerschaft für ein bestimmtes Gerät einrichten, indem sie die Windows Media Player Benutzeroberfläche verwenden. Sie können Partnerschaften programmgesteuert verwalten, indem Sie [IWMPSyncDevice::createPartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) und [IWMPSyncDevice::d eletePartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership)verwenden. Die **createPartnership-Methode** startet einen asynchronen Prozess, der endet, wenn das **CreatePartnershipComplete-Ereignis** über die **IWMPEvents2-Schnittstelle** empfangen wird.

Windows Media Player 10 oder höher unterstützt die Erstellung von Partnerschaften mit bis zu 16 Geräten. Jede Partnerschaft verfügt über einen zugeordneten Partnerschaftsindex. Sie können den Partnerschaftsindex für ein bestimmtes Gerät abrufen, indem Sie [IWMPSyncDevice::get \_ partnershipIndex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)aufrufen. Partnerschaftsindizes werden von 1 bis 16 nummeriert. Wenn ein bestimmtes Gerät keine Partnerschaft mit Windows Media Player hat, gibt **getPartnershipIndex** 0 (null) für den Index zurück.

Sie können den Partnerschaftsstatus eines bestimmten Geräts abrufen, indem Sie [IWMPSyncDevice::get \_ status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) aufrufen und dann den abgerufenen [WMPDeviceStatus-Wert](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) überprüfen. Windows Media Player ermöglicht eine Partnerschaft mit der Bibliothek eines Benutzers auf einem Computer für jedes Gerät. Dies bedeutet, dass die Erstellung einer neuen Partnerschaft jede vorhandene Partnerschaft zerstört, die das aktuelle Gerät möglicherweise mit einem anderen Computer hat. Um zu erfahren, wann sich der Status für ein Gerät ändert, können Sie das **DeviceStatusChange-Ereignis** empfangen.

Windows Media Player kann keine Partnerschaft mit einem Gerät mit dem Status **wmpdsManualDevice** erstellen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Gerätesynchronisierung**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Arbeiten mit portablen Geräten**](working-with-portable-devices.md)
</dt> </dl>

 

 




