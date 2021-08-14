---
description: Die folgenden Schnittstellen können verwendet werden, um einen Benutzer oder Computer in einer Zertifikathierarchie zu registrieren.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Schnittstellen für die Zertifikatregistrierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb71c1240791e26781797b547b0a62aaad1612a2bce06738cecfa02c8173b215
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902741"
---
# <a name="certificate-enrollment-interfaces"></a>Schnittstellen für die Zertifikatregistrierung

Die folgenden Schnittstellen können verwendet werden, um einen Benutzer oder Computer in einer Zertifikathierarchie zu registrieren.



| Schnittstelle                                              | BESCHREIBUNG                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | Registriert einen Computer oder Benutzer in einer Zertifikathierarchie.                                                                                                                              |
| [**IX509Enrollment2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | Erweitert die [**IX509Enrollment-Schnittstelle,**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) um die Initialisierung aus einer Vorlage zu ermöglichen.                                                                          |
| [**IX509EnrollmentHelper**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | Definiert Methoden, mit denen eine Webanwendung ein Zertifikat registrieren, Anmeldeinformationen des Richtlinienservers im Anmeldeinformationscache speichern und Richtlinienserver und Registrierungsserver registrieren kann. |
| [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | Ruft detaillierte Fehlerinformationen zu einer Zertifikatregistrierungstransaktion ab.                                                                                                    |
| [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | X.509 Simple Computer Enrollment Protocol Interface<br/>                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 




