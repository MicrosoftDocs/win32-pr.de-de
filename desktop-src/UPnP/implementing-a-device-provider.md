---
title: Implementieren eines Geräteanbieters
description: Um einen Geräteanbieter zu implementieren, erstellen Sie ein -Objekt, das die IUPnPDeviceProvider-Schnittstelle verfügbar macht.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19823357389a513a095081ce6ca79176af79897273274cc1f0e59a56e29b339f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118999650"
---
# <a name="implementing-a-device-provider"></a>Implementieren eines Geräteanbieters

Um einen Geräteanbieter zu implementieren, erstellen Sie ein -Objekt, das die [**IUPnPDeviceProvider-Schnittstelle**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) verfügbar macht. Dieses Objekt muss mithilfe der [**IUPnPRegistrar::RegisterDeviceProvider-Methode**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) beim Gerätehost registriert werden. Diese Methode verwendet die folgenden Parameter:

-   Der Name des Anbieters, der auf dem Computer eindeutig sein muss.
-   Die ProgID der Klasse, die den Geräteanbieter implementiert.
-   Eine Initialisierungszeichenfolge, die beim Starten an den Geräteanbieter übergeben wird.
-   Eine Container-ID. Eine Container-ID ist eine Zeichenfolge, die die Gruppe identifiziert, zu der das Gerät gehört. Alle Geräte mit demselben Containerbezeichner werden im gleichen Prozess gehostet.

 

 




