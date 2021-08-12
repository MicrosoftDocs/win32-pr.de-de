---
title: Aktivieren von PnP für Geräte
description: Aktivieren von PnP für Geräte
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Medien Geräte-Manager,PnP-Geräte
- Geräte-Manager,PnP-Geräte
- Programmierhandbuch,PnP-Geräte
- Dienstanbieter,PnP-Geräte
- Erstellen von Dienstanbietern, PnP-Geräten
- PnP-Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e574aa0d5462c2fcbb0592e9d3faaf927cd7e5213e6eec3d8e7f016eabfb7abc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118584998"
---
# <a name="enabling-pnp-for-devices"></a>Aktivieren von PnP für Geräte

Windows Medien Geräte-Manager überwacht Benachrichtigungen zum Ein- und Entfernen von Geräten, die eine Portable Audio Player-Geräteschnittstelle anknten. Bei der Ankunft eines solchen Geräts fragt Windows Media Geräte-Manager einen Geräteparameter namens *WMDMSPCLSID* nach der Klassen-ID des für dieses Gerät verantwortlichen Dienstanbieters ab. Windows Media Geräte-Manager ruft [**IMDServiceProvider2::CreateDevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) für diesen Dienstanbieter auf, um ein Geräteobjekt zu erstellen, das für die Anwendung als [**IWMDMDevice-Objekt verfügbar**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) gemacht wird.

Ein Dienstanbieter kann entweder PnP-Geräte oder Nicht-PnP-Geräte verarbeiten. Er kann nicht beide Typen verarbeiten.

Damit ein Gerät mit dem oben genannten Mechanismus funktioniert (und somit Benachrichtigungen zum Ein- und Entfernen des Geräts unter Windows Media Geräte-Manager-Anwendungen) aktiviert, müssen die folgenden Anforderungen erfüllt sein:

-   Der Gerätetreiber dieses Geräts muss die Geräteschnittstelle Windows Media Geräte-Manager Portable Audio Player ankn.) Die GUID für diese Geräteschnittstelle ist wie die folgenden definiert:

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > Ein Gerät sollte diese Schnittstelle nicht anbenennen, wenn das Gerät die Volume-Schnittstelle anklasst (definiert als VolumeClassGuid oder GUID \_ DEVINTERFACE \_ VOLUME in winioctl.h). Wenn das Gerät die Volumeschnittstelle ank angekündigt, ist sie bereits PnP-fähig unter Windows Medienschnittstelle Geräte-Manager.

     

    -AND/OR-

    Ein neuer Registrierungsunterschlüssel für den Dienstanbieter muss im Unterschlüssel HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows Media Geräte-Manager \_ \\ \\ \\ \\ KnownDevices erstellt werden. Dieser Schlüssel muss den Namen Ihres Dienstanbieters und die folgenden beiden Reg \_ SZ-Werteinträge enthalten:

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   Das Gerät muss über einen Geräteparameter mit dem Namen WMDMSPCLSID verfügen. Der Wert dieses Parameters sollte als CLSID des Dienstanbieters in einer Zeichenfolgenform festgelegt werden. Weitere Informationen zu Geräteparametern finden Sie unter [Geräteparameter.](device-parameters.md)

    > [!Note]  
    > Der Parameterwert muss die CLSID und nicht die ProgID des Dienstanbieters sein.

     

-   Der Dienstanbieter für dieses Gerät muss die IMDServiceProvider2-Schnittstelle implementieren.
-   Der Dienstanbieterschlüssel unter HKEY \_ LOCAL MACHINE SOFTWARE Microsoft Windows Media Geräte-Manager Plugins SP SPName muss den folgenden \_ \\ \\ \\ \\ \\ \\ DWORD-Wert enthalten.
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 




