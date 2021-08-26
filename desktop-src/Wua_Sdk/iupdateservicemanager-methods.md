---
description: Die IUpdateServiceManager-Schnittstelle definiert die folgenden Methoden.
ms.assetid: b2ae49bc-3fb6-4cb9-82ce-387409096159
title: IUpdateServiceManager-Methoden
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1486727db4ed4e9b561c19a1a2f3994bca0085e836ae774fda1c7db76df38144
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119994350"
---
# <a name="iupdateservicemanager-methods"></a>IUpdateServiceManager-Methoden

Die [**IUpdateServiceManager-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservicemanager) definiert die folgenden Methoden.



| Methode                                                                           | Beschreibung                                                                                                                                      |
|----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [**AddScanPackageService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addscanpackageservice)     | Registriert ein Scanpaket als Dienst bei Windows Update-Agent (WUA) und gibt dann eine [**IUpdateService-Schnittstelle**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice) zurück.    |
| [**AddService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-addservice)                           | Registriert einen Dienst bei WUA.                                                                                                                    |
| [**RegisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-registerservicewithau)     | Registriert einen Dienst bei Automatische Updates.                                                                                                      |
| [**RemoveService**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-removeservice)                     | Entfernt eine Dienstregistrierung aus WUA.                                                                                                         |
| [**Setoption**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-setoption)                             | Legt Optionen für das -Objekt fest, das die Dienst-ID angibt, und legt fest, ob beim Ändern der Registrierung von Automatische Updates eine Warnung angezeigt werden soll. |
| [**UnregisterServiceWithAU**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateservicemanager-unregisterservicewithau) | Aufheben der Registrierung eines Diensts bei Automatische Updates.                                                                                                    |



 

 

 



