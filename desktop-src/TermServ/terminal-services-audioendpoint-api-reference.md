---
title: Remotedesktopdienste audioendpoint-API-Referenz
description: Unterstützt Schnittstellen für die audioendpunkt Registrierung und den Datentransport.
ms.assetid: 0e3ea0e7-8c61-400e-b8ef-8a0403aedafa
ms.tgt_platform: multiple
keywords:
- Remotedesktopdienste Remotedesktopdienste, audioendpoint-API-Referenz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1958b21643083a14110ddad77f68024cc464dd36
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104388559"
---
# <a name="remote-desktop-services-audioendpoint-api-reference"></a>Remotedesktopdienste audioendpoint-API-Referenz

Ein *audioendpunkt* stellt ein Audiogerät, eine audioapi oder eine beliebige andere Audioquelle oder-Senke dar und wird verwendet, um Daten an die Audioengine zu senden oder Sie zu nutzen. Ein audioendpunkt muss über eine *Verbindung* mit dem Audiomodul verbunden sein, und jede Verbindung kann nur einen Endpunkt haben. Nachdem ein Endpunkt registriert wurde, fügt die Audioengine den Endpunkt an die Verbindung an.

Jedes Endpunkt Objekt muss die folgenden Schnittstellen implementieren:

-   [**Iaudioendpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpoint) , um dem Audiomodul zu ermöglichen, Informationen zum Endpunkt zu erhalten.
-   [**Iaudioendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointrt) , um Informationen über den Datenpuffer zu erhalten, bevor ein Verarbeitungs Durchlauf durchgeführt und der Endpunkt benachrichtigt wird, wenn der Durchlauf abgeschlossen ist.
-   Entweder die [**iaudioinputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioinputendpointrt) -oder die [**iaudiooutputendpointrt**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiooutputendpointrt) -Schnittstelle, abhängig davon, ob das Endpunkt Objekt Audiodaten erfasst oder rendert.
-   [**Iaudiodeviceendpoint**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudiodeviceendpoint)
-   [**Iaudioendpointcontrol**](/windows/desktop/api/Audioengineendpoint/nn-audioengineendpoint-iaudioendpointcontrol)

Die Audioengine verwendet diese Schnittstellen, um Informationen zu den Endpunkten zu erhalten, die an die Engine angefügt sind. Die Endpunkt Implementierung muss den Mechanismus bereitstellen, mit dem Daten an die Engine übertragen werden können, wie von diesen Schnittstellen angegeben.

Die Remotedesktopdienste audioendpoint-API unterstützt Enumerationstypen, Schnittstellen und Strukturen.

## <a name="in-this-section"></a>In diesem Abschnitt

-   [Remotedesktopdienste audioendpoint-Enumerationstypen](terminal-services-audioendpoint-enumeration-types.md)
-   [Remotedesktopdienste audioendpoint-Funktionen](remote-desktop-services-audioendpoint-functions.md)
-   [Remotedesktopdienste audioendpoint-Schnittstellen](terminal-services-audioendpoint-interfaces.md)
-   [Remotedesktopdienste audioendpoint-Strukturen](terminal-services-audioendpoint-structures.md)

## <a name="remarks"></a>Bemerkungen

Die Remotedesktopdienste audioendpoint-API ist für die Verwendung in Remotedesktop Szenarien vorgesehen. Es handelt sich nicht um Client Anwendungen.

 

 




