---
title: Registrieren eines Geräts beim Gerätehost
description: Sie können entweder ein ausgeführtes gerät oder ein nicht ausgeführtes Gerät registrieren.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8425578dbd5ccc76685c2a142bee8d2167c4058341c32e4b03bcedca15041579
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867580"
---
# <a name="how-to-register-a-device-with-the-device-host"></a>Registrieren eines Geräts beim Gerätehost

Sie können entweder ein ausgeführtes gerät oder ein nicht ausgeführtes Gerät registrieren.

## <a name="registering-a-running-device"></a>Registrieren eines ausgeführten Geräts

Geräte werden über die [**IUPnPRegistrar-Schnittstelle**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) registriert. Nur Administratoren dürfen ausgeführte Geräte registrieren. Um ein Gerät zu registrieren, das über ein ausgeführtes Gerätesteuerungsobjekt verfügt, muss eine Anwendung [**IUPnPRegistrar::RegisterRunningDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)aufrufen und Folgendes übergeben:

-   Der Text der Gerätebeschreibung.
-   Ein **IUnknown-Zeiger** auf das Gerätesteuerungsobjekt.
-   Eine Initialisierungszeichenfolge, die an die [**IUPnPDeviceControl::Initialize-Methode**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) des Gerätesteuerelementobjekts übergeben wird.
-   Der Speicherort des Ressourcenverzeichnisses.
-   Die Lebensdauer des Geräts.
-   Der Device ID-Parameter (ein OUT-Parameter), der der Rückgabewert dieses Aufrufs ist. Ein Zeiger auf die Geräte-ID wird in C++ zurückgegeben.

## <a name="registering-a-non-running-device"></a>Registrieren eines nicht ausgeführten Geräts

Standardmäßig dürfen nur Administratoren und interaktive Benutzer nicht ausgeführte Geräte registrieren. Um ein Gerät bei einem Gerätesteuerungsobjekt zu registrieren, das nicht ausgeführt wird, verwendet die Anwendung die [**IUPnPRegistrar::RegisterDevice-Methode.**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice)

Um ein Gerät programmgesteuert bei einem nicht ausgeführten Gerätesteuerungsobjekt zu registrieren, muss die Anwendung [**IUPnPRegistrar::RegisterDevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) aufrufen und die folgenden Parameter übergeben:

-   Der Text der Gerätebeschreibung.
-   Die ProgID des Gerätesteuerungsobjekts.
-   Eine Initialisierungszeichenfolge, die an die [**IUPnPDeviceControl::Initialize-Methode**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) des Gerätesteuerelementobjekts übergeben wird.
-   Eine Container-ID.
-   Der Speicherort des Ressourcenverzeichnisses.
-   Die Lebensdauer des Geräts.
-   Der Device ID-Parameter (ein OUT-Parameter), der der Rückgabewert dieses Aufrufs ist. Ein Zeiger auf die Geräte-ID wird in C++ zurückgegeben.

Die Registrierungen nicht ausgeführter Geräte können so konfiguriert werden, dass sie über Systemstarts hinweg beibehalten werden (die Geräte werden während der Herunterfahrensphase nicht veröffentlicht). Wenn sie auf diese Weise konfiguriert sind, werden Geräte daher bei jedem Start des Computers veröffentlicht und angekündigt.

 

 




