---
description: Die folgenden Funktionen werden mit Windows-Sicherheit Center verwendet.
ms.assetid: FC28ACD2-A3C6-42A9-AE59-61892A139FB7
title: Windows-Sicherheit Center Functions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0205620498bf6346208075863cf953eb912048478e1559a7829ba3f3ff52d2f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118666371"
---
# <a name="windows-security-center-functions"></a>Windows-Sicherheit Center Functions

Die folgenden Funktionen werden mit Windows-Sicherheit Center verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                           | Beschreibung                                                                                                                                                                              |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**WscGetSecurityProviderHealth**](/windows/desktop/api/Wscapi/nf-wscapi-wscgetsecurityproviderhealth)<br/> | Ruft den aggregierten Integritätsstatus der Sicherheitsanbieterkategorien ab, die durch die angegebenen [**WSC \_ SECURITY \_ PROVIDER-Enumerationswerte**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) dargestellt werden.<br/> |
| [**WscRegisterForChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges)<br/>               | Registriert eine Rückruffunktion, die ausgeführt wird, wenn Windows-Sicherheit Center (WSC) eine Änderung erkennt, die sich auf die Integrität eines der Sicherheitsanbieter auswirken kann.<br/>                    |
| [**WscUnRegisterChanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscunregisterchanges)<br/>                 | Bricht eine Rückrufregistrierung ab, die durch einen Aufruf der [**WscRegisterForChanges-Funktion durchgeführt**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) wurde.<br/>                                               |



 

 

 




