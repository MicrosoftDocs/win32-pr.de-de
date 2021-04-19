---
description: Die folgenden Schnittstellen können verwendet werden, um einen Benutzer oder Computer in einer Zertifikatshierarchie anzumelden.
ms.assetid: 653bc971-8bda-4e23-a56a-dbeb36eeaf6d
title: Zertifikat Registrierungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6e13e8db7d2938b7facb0b055303c1bdc18392a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106352582"
---
# <a name="certificate-enrollment-interfaces"></a>Zertifikat Registrierungs Schnittstellen

Die folgenden Schnittstellen können verwendet werden, um einen Benutzer oder Computer in einer Zertifikatshierarchie anzumelden.



| Schnittstelle                                              | BESCHREIBUNG                                                                                                                                                                         |
|--------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment)             | Registriert einen Computer oder Benutzer in einer Zertifikatshierarchie.                                                                                                                              |
| [**IX509Enrollment2**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollment2)           | Erweitert die [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Schnittstelle, um die Initialisierung aus einer Vorlage zu ermöglichen.                                                                          |
| [**IX509EnrollmentHelper**](/windows/desktop/api/Certenroll/nn-certenroll-ix509enrollmenthelper) | Definiert Methoden, mit denen eine Webanwendung ein Zertifikat registrieren, Anmelde Informationen für den Richtlinien Server im Anmelde Informations Cache speichern und Richtlinien Server und Registrierungs Server registrieren kann. |
| [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) | Ruft ausführliche Fehlerinformationen zu einer Zertifikat Registrierungs Transaktion ab.                                                                                                    |
| [**IX509SCEPEnrollment**](/windows/desktop/api/Certenroll/nn-certenroll-ix509scepenrollment)     | X. 509-Schnittstelle für einfaches Computer-anmeldungprotokoll<br/>                                                                                                                      |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 




