---
title: Informationen zu Geräten
description: Informationen zu Geräten
ms.assetid: 9e68c5eb-5fcb-4d7d-8dbb-7e951f253df8
keywords:
- Windows Media Player, Synchronisieren von Geräten
- Windows Media Player-Objektmodell, Synchronisieren von Geräten
- Objektmodell, Synchronisieren von Geräten
- Windows Media Player ActiveX-Steuerelement, Synchronisieren von Geräten
- ActiveX-Steuerelement, Synchronisieren von Geräten
- Windows Media Player Mobile ActiveX-Steuerelement, Synchronisieren von Geräten
- Windows Media Player Mobile, Synchronisieren von Geräten
- Synchronisieren von Geräten, Informationen zu
- Geräte Synchronisierung, Informationen zu
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e89a074e4edb5bdbc7d90391398d5e0e4133505a
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/19/2020
ms.locfileid: "106339867"
---
# <a name="about-devices"></a>Informationen zu Geräten

Portable Geräte sind Hardware Geräte, die Benutzer zum Nutzen digitaler Medieninhalte nutzen, wenn Sie nicht mehr von Ihrem Computer entfernt sind. In der Regel sind tragbare Geräte Akku Betrieb. Einige Geräte können nur Musik abspielen. Andere Geräte können Videos und Musik abspielen.

Einige Geräte unterstützen die automatische Synchronisierung digitaler Medieninhalte mit Windows Media Player. Andere Geräte unterstützen nur die manuelle Übertragung. Sie können bestimmen, ob ein bestimmtes Gerät die automatische Synchronisierung unterstützt, indem Sie [iwmpsyncdevice:: get- \_ Status](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_status) aufrufen und dann den abgerufenen [wmpdevicestatus](/previous-versions/windows/desktop/api/wmp/ne-wmp-wmpdevicestatus) -Wert überprüfen. Wenn der abgerufene Wert **wmpdsmanualdevice** lautet, unterstützt das Gerät keine automatische Synchronisierung.

Die Geräte, die mit dem Computer des Benutzers verbunden sind, können aufgelistet werden. Verwenden Sie zu diesem Zweck zuerst [iwmpsyncservices:: get \_ devicecount](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-get_devicecount) , um die Anzahl der Geräte abzurufen. Nennen Sie dann in einer-Schleife [iwmpsyncservices:: getdevice](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncservices-getdevice), und übergeben Sie jedes Mal den entsprechenden Indexwert. Mit [iwmpsyncdevice:: get- \_ Verbindung](/previous-versions/windows/desktop/api/wmp/nf-wmp-iwmpsyncdevice-get_connected) können Sie auswerten, ob ein bestimmtes Gerät zurzeit verbunden ist.

Wenn Sie wissen möchten, wenn Geräte eine Verbindung herstellen oder trennen, können Sie die Ereignisse **deviceconnetct** und **devicedisconnect** empfangen. Diese Ereignisse werden über die **IWMPEvents2** -Schnittstelle empfangen.

Die **iwmpsyncdevice** -Schnittstelle stellt zusätzliche Methoden bereit, mit denen Sie Informationen zu einem Gerät erhalten oder festlegen können. Beispiel:

-   Mit den Methoden **get \_ FriendlyName** und **Put \_ FriendlyName** können Sie den Namen des benutzerdefinierten Geräts abrufen und angeben.
-   Mit der Methode " **get \_ DeviceName** " können Sie den Gerätenamen abrufen, den Benutzer in der Windows XP-Shell sehen.
-   Die **getiteminfo** -Methode ermöglicht das Abrufen von Metadaten von Geräten.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Informationen zur Geräte Synchronisierung**](about-device-synchronization.md)
</dt> <dt>

[**IWMPEvents2-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents2)
</dt> <dt>

[**Iwmpsyncdevice-Schnittstelle**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpsyncdevice)
</dt> <dt>

[**Arbeiten mit tragbaren Geräten**](working-with-portable-devices.md)
</dt> </dl>

 

 




