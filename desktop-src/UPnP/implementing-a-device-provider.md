---
title: Implementieren eines Geräte Anbieters
description: Um einen Geräte Anbieter zu implementieren, erstellen Sie ein Objekt, das die iupnpdeviceprovider-Schnittstelle verfügbar macht.
ms.assetid: 3ba1200d-68d4-4f03-805c-7fff2d76b16f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb8cd2bea433b884bf6ddf3828fb148c726cd867
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471725"
---
# <a name="implementing-a-device-provider"></a>Implementieren eines Geräte Anbieters

Um einen Geräte Anbieter zu implementieren, erstellen Sie ein Objekt, das die [**iupnpdeviceprovider**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpdeviceprovider) -Schnittstelle verfügbar macht. Dieses Objekt muss beim Geräte Host mit der [**iupnpregistrinnerpregistrinsterdeviceprovider**](/windows/desktop/api/Upnphost/nf-upnphost-iupnpregistrar-registerdeviceprovider) -Methode registriert werden. Diese Methode übernimmt die folgenden Parameter:

-   Der Name des Anbieters, der auf dem Computer eindeutig sein muss.
-   Die ProgID der Klasse, die den Geräte Anbieter implementiert.
-   Eine Initialisierungs Zeichenfolge, die beim Starten an den Geräte Anbieter übermittelt wird.
-   Eine Container-ID. Eine Container-ID ist eine Zeichenfolge, die die Gruppe identifiziert, zu der das Gerät gehört. Alle Geräte mit demselben Container Bezeichner werden im gleichen Prozess gehostet.

 

 




