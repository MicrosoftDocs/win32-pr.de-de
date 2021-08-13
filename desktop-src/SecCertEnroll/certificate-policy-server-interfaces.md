---
description: Die folgenden Schnittstellen können verwendet werden, um einen CEP-Server (Certificate Enrollment Policy) programmgesteuert zu konfigurieren.
ms.assetid: 48c7c21c-1b20-4a79-932d-bed19ff9833e
title: Zertifikatrichtlinien-Serverschnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d359f4e29e1238eda1109bbd2dca7d6df76cb6f3530e9a96b0f3d22d63af69
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902596"
---
# <a name="certificate-policy-server-interfaces"></a>Zertifikatrichtlinien-Serverschnittstellen

Die folgenden Schnittstellen können verwendet werden, um einen CEP-Server (Certificate Enrollment Policy) programmgesteuert zu konfigurieren.



| Schnittstelle                                                            | BESCHREIBUNG                                                                                                   |
|----------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| [**IX509EnrollmentPolicyServer**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmentpolicyserver)   | Stellt einen CEP-Server dar.                                                                                      |
| [**IX509PolicyServerListManager**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509policyserverlistmanager) | Verwaltet eine Auflistung von [**IX509PolicyServerUrl-Objekten.**](/windows/desktop/api/Certenroll/nn-certenroll-ix509policyserverurl)                         |
| [**IX509PolicyServerUrl**](/windows/desktop/api/Certenroll/nn-certenroll-ix509policyserverurl)                 | Gibt eigenschaftswerte an, die dem CEP-Server zugeordnet sind, oder ruft sie ab und aktualisiert die zugeordneten Registrierungswerte. |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



