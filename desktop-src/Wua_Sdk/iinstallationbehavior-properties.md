---
description: Die iinstallationbehavior-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: Iinstallationbehavior-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 210f495c19c530a6507ffbd0584f647fc952ae46
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958985"
---
# <a name="iinstallationbehavior-properties"></a>Iinstallationbehavior-Eigenschaften

Die [**iinstallationbehavior**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                                                 | BESCHREIBUNG                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Canrequestuserinput**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | Ruft einen booleschen Wert ab, der angibt, ob bei der Installation oder Deinstallation eines Updates Benutzereingaben angefordert werden können.                                                        |
| [**Auswirkung**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | Ruft eine [**installationimpact**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) -Enumeration ab, die angibt, wie sich die Installation oder die Installation des Updates auf den Computer auswirkt.                 |
| [**RebootBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | Ruft eine [**installationrebootbehavior**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) -Enumeration ab, die das Neustart Verhalten angibt, das beim Installieren oder Deinstallieren des Updates auftritt. |
| [**Requirements-netzwerkkonnektivitätskonnektivität**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | Ruft einen booleschen Wert ab, der angibt, ob die Installation oder die Installation eines Updates Netzwerk Konnektivität erfordert.                                                     |



 

 

 



