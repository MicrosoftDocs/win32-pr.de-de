---
description: Die folgenden Funktionen werden mit Windows-Security Center verwendet.
ms.assetid: FC28ACD2-A3C6-42A9-AE59-61892A139FB7
title: Windows Security Center-Funktionen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 250d5b3dd7213d9d7f9363ce6b1a83a1e170e01a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103860598"
---
# <a name="windows-security-center-functions"></a>Windows Security Center-Funktionen

Die folgenden Funktionen werden mit Windows-Security Center verwendet.

## <a name="in-this-section"></a>In diesem Abschnitt



| Thema                                                                           | BESCHREIBUNG                                                                                                                                                                              |
|---------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wscgetsecurityproviderhealth**](/windows/desktop/api/Wscapi/nf-wscapi-wscgetsecurityproviderhealth)<br/> | Ruft den aggregierten Integritäts Status der Sicherheitsanbieter Kategorien ab, die durch die angegebenen Enumerationswerte des [**WSC- \_ Sicherheits \_ Anbieters**](/windows/desktop/api/Wscapi/ne-wscapi-wsc_security_provider) dargestellt werden.<br/> |
| [**Wscregisterforchanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges)<br/>               | Registriert eine Rückruffunktion, die ausgeführt wird, wenn Windows Security Center (WSC) eine Änderung erkennt, die sich auf die Integrität eines der Sicherheitsanbieter auswirken könnte.<br/>                    |
| [**Wscunregisterchanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscunregisterchanges)<br/>                 | Bricht eine Rückruf Registrierung ab, die durch einen Aufrufen der [**wscregisterforchanges**](/windows/desktop/api/Wscapi/nf-wscapi-wscregisterforchanges) -Funktion durchgeführt wurde.<br/>                                               |



 

 

 




