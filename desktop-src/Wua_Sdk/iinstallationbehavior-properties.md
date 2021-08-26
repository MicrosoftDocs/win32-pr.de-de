---
description: Die IInstallationBehavior-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: abb8e247-44c4-491c-b8ea-9f32d7420c45
title: IInstallationBehavior-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e3a4bcb1f444d628ebff221d19143d0dd5f472149da24f86b46811bb9efc2c99
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994770"
---
# <a name="iinstallationbehavior-properties"></a>IInstallationBehavior-Eigenschaften

Die [**IInstallationBehavior-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iinstallationbehavior) definiert die folgenden Eigenschaften.



| Eigenschaft                                                                                 | BESCHREIBUNG                                                                                                                                                                    |
|------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CanRequestUserInput**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_canrequestuserinput)                 | Ruft einen booleschen Wert ab, der angibt, ob die Installation oder Deinstallation eines Updates benutzereingabeaufforderungen kann.                                                        |
| [**Auswirkung**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_impact)                                           | Ruft eine [**InstallationImpact-Enumeration**](/windows/win32/api/wuapi/ne-wuapi-installationimpact) ab, die angibt, wie sich die Installation oder Deinstallation des Updates auf den Computer auswirken.                 |
| [**RebootBehavior**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_rebootbehavior)                           | Ruft eine [**InstallationRebootBehavior-Enumeration ab,**](/windows/win32/api/wuapi/ne-wuapi-installationrebootbehavior) die das Neustartverhalten angibt, das beim Installieren oder Deinstallieren des Updates auftritt. |
| [**RequiresNetworkConnectivity**](/windows/desktop/api/Wuapi/nf-wuapi-iinstallationbehavior-get_requiresnetworkconnectivity) | Ruft einen booleschen Wert ab, der angibt, ob die Installation oder Deinstallation eines Updates Netzwerkkonnektivität erfordert.                                                     |



 

 

 



