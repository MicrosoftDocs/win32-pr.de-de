---
title: Kanalbindung
description: Bindungen geben das Wire-Protokoll und das lokale Verhalten eines Kanals an.
ms.assetid: 82d465c5-b23d-4403-b360-8c710fbc6e1c
keywords:
- Binden von Webdiensten für Windows
- Wwsapi
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 723a729b87dc26849dbd1f84038805c5e47a0ea4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104310288"
---
# <a name="channel-binding"></a>Kanalbindung

Bindungen geben das Wire-Protokoll und das lokale Verhalten eines Kanals an. Bindungen bestehen aus den folgenden Komponenten:

-   Eine [**WS \_ - \_ channelbindung**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_binding), die das zu verwendende Übertragungsprotokoll identifiziert.
-   Eine [**WS- \_ Sicherheits \_ Beschreibung**](/windows/desktop/api/WebServices/ns-webservices-ws_security_description), die angibt, wie der Kanal gesichert werden soll.
-   Eine Set [**WS \_ Channel- \_ Eigenschaft**](/windows/desktop/api/WebServices/ns-webservices-ws_channel_property), die zusätzliche optionale Einstellungen angibt (siehe auch [**ID der WS- \_ \_ Channeleigenschaft \_**](/windows/desktop/api/WebServices/ne-webservices-ws_channel_property_id)).

 

 




