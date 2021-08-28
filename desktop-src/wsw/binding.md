---
title: Kanalbindung
description: Bindungen geben das Wire Protocol und das lokale Verhalten für einen Kanal an.
ms.assetid: 82d465c5-b23d-4403-b360-8c710fbc6e1c
keywords:
- Binden von Webdiensten für Windows
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ae6e1b666f6b83915595f9fb138cc6ba2d81a434bbedd9871f27ba8fd6c6bbd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119026728"
---
# <a name="channel-binding"></a>Kanalbindung

Bindungen geben das Wire Protocol und das lokale Verhalten für einen Kanal an. Bindungen werden aus den folgenden Komponenten hergestellt:

-   Eine [**\_ WS-KANALBINDUNG, \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding)die das zu verwendende Übertragungsprotokoll identifiziert.
-   Eine [**\_ WS-SICHERHEITSBESCHREIBUNG, \_**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description)die angibt, wie der Kanal geschützt wird.
-   Eine gruppe [**WS \_ CHANNEL \_ PROPERTY**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property)s, die zusätzliche optionale Einstellungen angeben (siehe auch [**WS \_ CHANNEL PROPERTY \_ \_ ID**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).

 

 




