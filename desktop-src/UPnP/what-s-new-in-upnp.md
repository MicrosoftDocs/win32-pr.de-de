---
title: Neuerungen in den UPnP-APIs
description: Die UPnP™-APIs verfügen über neue Features und aktualisierte Dokumentation für Windows XP SP2. In der folgenden Tabelle ist die neue Dokumentation aufgeführt.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a68ab872eab498e80ec8d30f996f839c73432875d02ec8d32060595ce8d6482b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057998"
---
# <a name="whats-new-in-the-upnp-apis"></a>Neuerungen in den UPnP-APIs

Die UPnP™-APIs verfügen über neue Features und aktualisierte Dokumentation für Windows XP SP2. In der folgenden Tabelle ist die neue Dokumentation aufgeführt.



| Funktion                                                          | Beschreibung                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IUPnPRemoteEndpointInfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | Mit dieser neuen Schnittstelle kann ein gehostetes Gerät Informationen zu einem Anforderer (d. h. einem Steuerungspunkt) und der Anforderung abrufen. Sie enthält drei Methoden, von denen jede einen anderen Informationstyp bereitstellt.                                                                                                                                                              |
| [Implementieren des Geräteverhaltens](implementing-device-behavior.md) | Dieses Thema enthält einen neuen Abschnitt, in dem erläutert wird, wie Sie Endpunktinformationen mithilfe der neuen [**IUPnPRemoteEndpointInfo-Schnittstelle**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) abrufen.                                                                                                                                                                                                     |
| [Konfigurations-Einstellungen](configuration-settings.md)             | Dieses neue Thema enthält Informationen zu den Registrierungseinstellungen, die sich auf das Verhalten der UPnP-APIs auswirken.                                                                                                                                                                                                                                                                    |
| [Gerätefehlercodes](device-error-codes.md)                     | In diesem neuen Thema wird erläutert, wie ein Fehlercode von einem Gerät in einen HRESULT-Wert konvertiert wird und umgekehrt. Ein Verständnis dieses Prozesses ist erforderlich, um einen HRESULT-Wert auszuwerten, der von den Methoden [**IUPnPService::InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) und [**IUPnPService::QueryStateVariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) zurückgegeben wird. |



 

 

 




