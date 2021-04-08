---
title: Aktivieren von PNP für Geräte
description: Aktivieren von PNP für Geräte
ms.assetid: 510237a9-2b74-4c2e-ad45-3f45117289a6
keywords:
- Windows Media Device Manager, PNP-Geräte
- Device Manager, PNP-Geräte
- Programmier Handbuch, PNP-Geräte
- Dienstanbieter, PNP-Geräte
- Erstellen von Dienstanbietern, PnP-Geräten
- PNP-Geräte
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d44c7ccdfd29453c1ab28e970c1b054d1278e620
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103855891"
---
# <a name="enabling-pnp-for-devices"></a>Aktivieren von PNP für Geräte

Windows Media Device Manager überwacht die Eingangs-und Entfernungs Benachrichtigungen von Geräten, die eine Portable Audioplayer-Geräteschnittstelle ankündigen. Beim Eintreffen eines solchen Geräts fragt Windows Media Device Manager einen Geräteparameter mit dem Namen " *wmdmspclsid* " für die Klassen-ID des Dienstanbieters ab, der für dieses Gerät zuständig ist. Windows Media Device Manager ruft [**IMDServiceProvider2:: anatedevice**](/windows/desktop/api/mswmdm/nf-mswmdm-imdserviceprovider2-createdevice) für diesen Dienstanbieter auf, um ein Geräte Objekt zu erstellen, das für die Anwendung als [**iwmdmdevice**](/windows/desktop/api/mswmdm/nn-mswmdm-iwmdmdevice) -Objekt verfügbar gemacht wird.

Ein Dienstanbieter kann entweder PNP-Geräte oder nicht-PNP-Geräte verarbeiten. Beide Typen können nicht verarbeitet werden.

Damit ein Gerät mit dem vorangehenden Mechanismus funktioniert (und somit die Eingangs-und Entfernungs Benachrichtigungen für das Gerät unter Windows Media Device Manager-Anwendungen) aktivieren kann, müssen die folgenden Anforderungen erfüllt sein:

-   Der Gerätetreiber dieses Geräts muss die Windows Media Device Manager portablen Audioplayer-Geräteschnittstelle ankündigen. Die GUID für diese Geräteschnittstelle wird wie folgt definiert:

    ```
    {0xf33fdc04, 0xd1ac, 0x4e8e, {0x9a, 0x30, 0x19, 0xbb, 0xd4, 0xb1, 0x8, 0xae} }
    ```

    

    > [!Note]  
    > Ein Gerät sollte diese Schnittstelle nicht ankündigen, wenn das Gerät die Volume-Schnittstelle (als volumeclassguid oder GUID \_ devinterface- \_ Volume in winioctl. h definiert) ankündigt. Wenn das Gerät die volumeschnittstelle ankündigt, ist es unter Windows Media Device Manager bereits PNP-fähig.

     

    -und/oder-

    Ein neuer Registrierungs Unterschlüssel für den Dienstanbieter muss innerhalb des unter Schlüssels HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Media Device Manager \\ knowndevices erstellt werden. Dieser Schlüssel sollte den Namen Ihres Dienstanbieters aufweisen und über die folgenden beiden REG SZ- \_ Wert Einträge verfügen:

    ```
    DeviceInterface         {25DBCE51-6C8F-4A72-8A6D-B54C2B4FC835}
    WMDMSPCLSID             {067B4B81-B1EC-489F-B111-940EBDC44EBE}
    ```

    

-   Das Gerät muss über einen Geräteparameter mit dem Namen "wmdmspclsid" verfügen. Der Wert dieses Parameters sollte als CLSID des Dienstanbieters in Form einer Zeichenfolge festgelegt werden. Weitere Informationen zu Geräteparametern finden Sie unter [Geräteparameter](device-parameters.md).

    > [!Note]  
    > Der Parameterwert muss die CLSID und nicht die ProgID des Dienstanbieters sein.

     

-   Der Dienstanbieter für dieses Gerät muss die IMDServiceProvider2-Schnittstelle implementieren.
-   Der Dienstanbieter Schlüssel unter HKEY \_ local \_ Machine \\ Software \\ Microsoft \\ Windows Media Device Manager \\ Plugins \\ SP \\ spname muss den folgenden DWORD-Wert enthalten.
    ```
    PnPAware    1
    ```

    

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[**Erstellen eines Dienstanbieters**](creating-a-service-provider.md)
</dt> </dl>

 

 




