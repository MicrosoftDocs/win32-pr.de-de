---
title: Informationen zu Partnerschaften
description: Informationen zu Partnerschaften
ms.assetid: d21813ed-efe0-48a2-a1bf-f10f4b7ac3e6
keywords:
- Windows Media Player, Partnerschaften
- Windows Media Player-Objektmodell, Partnerschaften
- Objektmodell, Partnerschaften
- Windows Media Player ActiveX-Steuerelement, Partnerschaften
- ActiveX-Steuerelement, Partnerschaften
- Windows Media Player Mobile ActiveX-Steuerelement, Partnerschaften
- Windows Media Player Mobile, Partnerschaften
- Synchronisieren von Geräten, Partnerschaften
- Geräte Synchronisierung, Partnerschaften
- Partnerschaften zwischen Geräten und Windows-Media Player
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cfc3fa20e1e8a4b6a4c7993ea7dcc5842719f2a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "104472244"
---
# <a name="about-partnerships"></a>Informationen zu Partnerschaften

Eine Partnerschaft ist eine besondere Beziehung zwischen einem tragbaren Gerät und Windows Media Player. Benutzer können mithilfe der Windows Media Player-Benutzeroberfläche eine Partnerschaft für ein bestimmtes Gerät einrichten. Partnerschaften können mithilfe von [iwmpsyncdevice:: createpartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-createpartnership) und [iwmpsyncdevice::d eletepartnership](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-deletepartnership)Programm gesteuert verwaltet werden. Die **createpartnership** -Methode startet einen asynchronen Prozess, der endet, wenn das **createpartnershipcomplete** -Ereignis über die **IWMPEvents2** -Schnittstelle empfangen wird.

Windows Media Player 10 oder höher unterstützt die Erstellung von Partnerschaften mit bis zu 16 Geräten. Jede Partnerschaft verfügt über einen zugeordneten Partnerschafts Index. Sie können den Partnerschafts Index für ein bestimmtes Gerät abrufen, indem Sie [iwmpsyncdevice:: get \_ partnershipindex](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_partnershipindex)aufrufen. Partnerschafts Indizes sind von 1 bis 16 nummeriert. Wenn ein bestimmtes Gerät nicht über eine Partnerschaft mit Windows Media Player verfügt, gibt **getpartnershipindex** für den Index 0 (null) zurück.

Sie können den Partnerschaftsstatus eines bestimmten Geräts abrufen, indem Sie [iwmpsyncdevice:: get- \_ Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) aufrufen und dann den abgerufenen [wmpdevicestatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) -Wert überprüfen. Windows Media Player ermöglicht eine Partnerschaft mit der Bibliothek eines Benutzers auf einem Computer für jedes Gerät. Dies bedeutet, dass das Erstellen einer neuen Partnerschaft eine vorhandene Partnerschaft zerstört, die das aktuelle Gerät möglicherweise mit einem anderen Computer hat. Wenn Sie wissen möchten, wann sich der Status für ein Gerät ändert, können Sie das **devicestatuschange** -Ereignis empfangen.

Windows Media Player kann keine Partnerschaft mit einem Gerät erstellen, das den Status **wmpdsmanualdevice** hat.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Geräte Synchronisierung**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Arbeiten mit tragbaren Geräten**](working-with-portable-devices.md)
</dt> </dl>

 

 




