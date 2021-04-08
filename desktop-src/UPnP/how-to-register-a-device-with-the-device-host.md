---
title: Registrieren eines Geräts beim Geräte Host
description: Sie können entweder ein Betriebs Endes Gerät oder ein Gerät registrieren, das nicht ausgeführt wird.
ms.assetid: 40e30881-d5fb-4cf9-8dd7-0d50d2621d5c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d3be1561d82741ce33e7eb05e63b015d5cb38f52
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104037001"
---
# <a name="how-to-register-a-device-with-the-device-host"></a>Registrieren eines Geräts beim Geräte Host

Sie können entweder ein Betriebs Endes Gerät oder ein Gerät registrieren, das nicht ausgeführt wird.

## <a name="registering-a-running-device"></a>Registrieren eines laufenden Geräts

Geräte werden mithilfe der [**iupnpregistrinar**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpregistrar) -Schnittstelle registriert. Nur Administratoren sind berechtigt, die Ausführung von Geräten zu registrieren. Um ein Gerät zu registrieren, das ein Geräte Steuerungsobjekt enthält, muss eine Anwendung [**iupnpregistranar:: registerrunningdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerrunningdevice)aufrufen und dabei Folgendes übergeben:

-   Der Text der Beschreibung des Geräts.
-   Ein **IUnknown** -Zeiger auf das Geräte Steuerungsobjekt.
-   Eine Initialisierungs Zeichenfolge, die an die [**iupnpdevicecontrol:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) -Methode des Geräte Steuerungs Objekts übergeben wird.
-   Der Speicherort des Ressourcen Verzeichnisses.
-   Die Lebensdauer des Geräts.
-   Der Geräte-ID-Parameter (ein out-Parameter), der der Rückgabewert dieses Aufrufes ist. Ein Zeiger auf die Geräte-ID wird in C++ zurückgegeben.

## <a name="registering-a-non-running-device"></a>Registrieren eines Geräts, das nicht ausgeführt wird

Standardmäßig sind nur Administratoren und interaktive Benutzer berechtigt, nicht laufende Geräte zu registrieren. Zum Registrieren eines Geräts bei einem Geräte Steuerungsobjekt, das nicht ausgeführt wird, verwendet die Anwendung die [**iupnpregistrinster:: registerdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) -Methode.

Zum programmgesteuerten Registrieren eines Geräts bei einem Geräte Steuerungsobjekt, das nicht ausgeführt wird, muss die Anwendung [**iupnpregistranar:: registerdevice**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdevice) aufrufen und die folgenden Parameter übergeben:

-   Der Text der Beschreibung des Geräts.
-   Die ProgID des Geräte Steuerungs Objekts.
-   Eine Initialisierungs Zeichenfolge, die an die [**iupnpdevicecontrol:: Initialize**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpdevicecontrol-initialize) -Methode des Geräte Steuerungs Objekts übergeben wird.
-   Eine Container-ID.
-   Der Speicherort des Ressourcen Verzeichnisses.
-   Die Lebensdauer des Geräts.
-   Der Geräte-ID-Parameter (ein out-Parameter), der der Rückgabewert dieses Aufrufes ist. Ein Zeiger auf die Geräte-ID wird in C++ zurückgegeben.

Die Registrierungen nicht laufender Geräte können so konfiguriert werden, dass Sie über Systemstarts hinweg beibehalten werden (die Geräte werden während der Herunterfahr Phase nicht veröffentlicht). Wenn Sie auf diese Weise konfiguriert werden, werden Geräte bei jedem Neustart des Computers veröffentlicht und angekündigt.

 

 




