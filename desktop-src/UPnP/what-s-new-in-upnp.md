---
title: Neuerungen in den UPnP-APIs
description: Die UPnP-™-APIs verfügen über neue Features und aktualisierte Dokumentation für Windows XP SP2. In der folgenden Tabelle ist die neue Dokumentation aufgeführt.
ms.assetid: ad72d9b8-6db4-4b9b-9b10-ae3980521d7e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e27747c6185b5aecea86e240d388ab10410aa29f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "103714351"
---
# <a name="whats-new-in-the-upnp-apis"></a>Neuerungen in den UPnP-APIs

Die UPnP-™-APIs verfügen über neue Features und aktualisierte Dokumentation für Windows XP SP2. In der folgenden Tabelle ist die neue Dokumentation aufgeführt.



| Funktion                                                          | BESCHREIBUNG                                                                                                                                                                                                                                                                                                                                                                   |
|------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Iupnpremoteendpointinfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo)       | Diese neue Schnittstelle ermöglicht einem gehosteten Gerät das Abrufen von Informationen über einen Anforderer (d. h. einen Steuerungspunkt) und die Anforderung. Sie enthält drei Methoden, von denen jede einen anderen Informationstyp bereitstellt.                                                                                                                                                              |
| [Implementieren von Geräteverhalten](implementing-device-behavior.md) | Dieses Thema enthält einen neuen Abschnitt, in dem erläutert wird, wie Endpunkt Informationen mithilfe der neuen [**iupnpremoteendpointinfo**](/windows/desktop/api/Upnphost/nn-upnphost-iupnpremoteendpointinfo) -Schnittstelle abgerufen werden.                                                                                                                                                                                                     |
| [Konfigurationseinstellungen](configuration-settings.md)             | Dieses neue Thema enthält Informationen zu den Registrierungs Einstellungen, die das Verhalten der UPnP-APIs beeinflussen.                                                                                                                                                                                                                                                                    |
| [Gerätefehler Codes](device-error-codes.md)                     | In diesem neuen Thema wird erläutert, wie ein Fehlercode von einem Gerät in einen HRESULT-Wert und umgekehrt konvertiert wird. Ein Verständnis dieses Prozesses ist erforderlich, um einen HRESULT-Wert auszuwerten, der von der [**iupnpservice:: InvokeAction**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-invokeaction) -Methode und der [**iupnpservice:: querystatuevariable**](/windows/desktop/api/Upnp/nf-upnp-iupnpservice-querystatevariable) -Methode zurückgegeben wird. |



 

 

 




