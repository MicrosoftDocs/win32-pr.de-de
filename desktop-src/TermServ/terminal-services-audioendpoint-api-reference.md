---
title: Remotedesktopdienste AudioEndpoint-API-Referenz
description: Unterstützt Schnittstellen für die Registrierung von Audioendpunkten und den Datentransport.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste , AudioEndpoint-API-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae9a7aa83b519ca10128f9bea3b945492f387c0498c81f8b2959cb9830b91dbc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119000090"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a>Remotedesktopdienste AudioEndpoint-API-Referenz

Ein *Audioendpunkt* stellt ein Audiogerät, eine Audio-API oder eine beliebige andere Audioquelle oder -senke dar und wird verwendet, um Daten an die Audio-Engine zu senden oder diese zu nutzen. Ein Audioendpunkt muss über eine *Verbindung* mit der Audio-Engine verbunden sein, und mit jeder Verbindung kann nur ein Endpunkt verbunden sein. Nachdem ein Endpunkt registriert wurde, fügt die Audio-Engine den Endpunkt an die Verbindung an.

Jedes Endpunktobjekt muss die folgenden Schnittstellen implementieren:

-   [**IAudioEndpoint,**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) um der Audio-Engine das Abrufen von Informationen zum Endpunkt zu ermöglichen.
-   [**IAudioEndpointRT,**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) um Informationen zum Datenpuffer abzurufen, bevor ein Verarbeitungsdurchlauf ausgeführt und der Endpunkt benachrichtigt wird, wenn der Durchlauf abgeschlossen ist.
-   Entweder die [**IAudioInputEndpointRT-**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) oder [**IAudioOutputEndpointRT-Schnittstelle,**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) je nachdem, ob das Endpunktobjekt Audiodaten erfasst oder rendert.
-   [**IAudioDeviceEndpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [**IAudioEndpointControl**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

Die Audio-Engine verwendet diese Schnittstellen, um Informationen zu den Endpunkten abzurufen, die an die Engine angefügt sind. Die Endpunktimplementierung muss den Mechanismus zum Übermitteln oder Nutzen von Daten aus der Engine bereitstellen, wie von diesen Schnittstellen angegeben.

Die Remotedesktopdienste AudioEndpoint-API unterstützt Enumerationstypen, Schnittstellen und Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Remotedesktopdienste AudioEndpoint-Enumerationstypen](terminal-services-audioendpoint-enumeration-types.md)
-   [Remotedesktopdienste AudioEndpoint-Funktionen](remote-desktop-services-audioendpoint-functions.md)
-   [Remotedesktopdienste AudioEndpoint-Schnittstellen](terminal-services-audioendpoint-interfaces.md)
-   [Remotedesktopdienste AudioEndpoint-Strukturen](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a>Hinweise

Die Remotedesktopdienste AudioEndpoint-API ist für die Verwendung in Remotedesktop Szenarien vorgesehen. sie ist nicht für Clientanwendungen vorgesehen.

 

 




