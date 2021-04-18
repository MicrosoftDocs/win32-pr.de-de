---
description: Die iupdateserviceregistration-Schnittstelle definiert die folgenden Eigenschaften.
ms.assetid: 2bcde8b4-7bff-4887-8080-89da817afb5f
title: Iupdateserviceregistration-Eigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 716c06f2fc8ed9a7ce12542a09440cf0ec0b5c49
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106344867"
---
# <a name="iupdateserviceregistration-properties"></a>Iupdateserviceregistration-Eigenschaften

Die **iupdateserviceregistration** -Schnittstelle definiert die folgenden Eigenschaften.



| Eigenschaft                                                                                      | BESCHREIBUNG                                                                                                                                          |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Ispendingregistrationwithau**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_ispendingregistrationwithau) | Ruft einen booleschen Wert ab, der angibt, ob der Dienst beim Hinzufügen auch bei automatische Updates registriert wird.                                  |
| [**RegistrationState**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_registrationstate)                     | Ruft einen [**updateserviceregistrationstate**](/windows/win32/api/wuapi/ne-wuapi-updateserviceregistrationstate) -Wert ab, der den aktuellen Status der Dienst Registrierung angibt. |
| [**Dienst**](/windows/desktop/api/Wuapi/nf-wuapi-iupdateserviceregistration-get_service)                                         | Ruft einen Zeiger auf eine [**IUpdateService2**](/windows/desktop/api/Wuapi/nn-wuapi-iupdateservice2) -Schnittstelle ab. Diese Eigenschaft ist die Standard Eigenschaft.                                    |



 

 

 



