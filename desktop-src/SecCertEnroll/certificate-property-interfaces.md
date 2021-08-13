---
description: Die folgenden Schnittstellen können verwendet werden, um eine Zertifikateigenschaft zu erstellen.
ms.assetid: c64fca58-fb2f-412f-b7c0-5db1979d051b
title: Schnittstellen für Zertifikateigenschaften
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e3d0ab8d9f8e9bb73d47b7e112dfa0ff6fb11f70031c64405b660ee5096dd78
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118902606"
---
# <a name="certificate-property-interfaces"></a>Schnittstellen für Zertifikateigenschaften

Die folgenden Schnittstellen können verwendet werden, um eine Zertifikateigenschaft zu erstellen.



| Schnittstelle                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ICertProperties**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperties)                                         | Verwalten sie eine Sammlung von [**ICertProperty-Objekten.**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                                                                                                                                                                    |
| [**ICertProperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                             | Ordnet einem Zertifikat eine externe Eigenschaft zu.                                                                                                                                                                                                       |
| [**ICertPropertyArchived**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)                             | Stellt eine Zertifikateigenschaft dar, die angibt, ob ein Zertifikat archiviert wurde.                                                                                                                                                                |
| [**ICertPropertyArchivedKeyHash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)               | Stellt einen SHA-1-Hash eines verschlüsselten privaten Schlüssels dar, der zur Archivierung an eine Zertifizierungsstelle übermittelt wird.                                                                                                                                                  |
| [**ICertPropertyAutoEnroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)                         | Stellt eine Zertifikateigenschaft dar, die eine Vorlage identifiziert, die zum Aktivieren der automatischen Registrierung des Zertifikats konfiguriert wurde.                                                                                                                        |
| [**ICertPropertyBackedUp**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)                             | Stellt eine Zertifikateigenschaft dar, die angibt, ob ein Zertifikat gesichert wurde, und, falls ja, das Datum und die Uhrzeit, zu der es gespeichert wurde.                                                                                                               |
| [**ICertPropertyDescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)                       | Ermöglicht es Ihnen, eine Zeichenfolge anzugeben und abzurufen, die beschreibende Informationen für ein Zertifikat enthält.                                                                                                                                                     |
| [**ICertPropertyEnrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)                         | Stellt eine Zertifikateigenschaft dar, die Zertifikat- und Zertifizierungsstelleninformationen enthält, die erstellt werden, wenn der Client die [**Enroll-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) für die [**IX509Enrollment-Schnittstelle**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) aufruft. |
| [**ICertPropertyEnrollmentPolicyServer**](/windows/desktop/api/Certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver) | Stellt eine externe Zertifikateigenschaft dar, die Informationen zu einem CEP-Server (Certificate Enrollment Policy) und einem Zertifikatregistrierungsserver (Certificate Enrollment Server, CES) enthält.                                                                                       |
| [**ICertPropertyFriendlyName**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)                     | Ermöglicht es Ihnen, eine Zeichenfolge anzugeben und abzurufen, die den Anzeigenamen eines Zertifikats enthält.                                                                                                                                                             |
| [**ICertPropertyKeyProvInfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)                       | Stellt eine Zertifikateigenschaft dar, die Informationen zu einem privaten Schlüssel enthält.                                                                                                                                                                          |
| [**ICertPropertyRenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)                               | Stellt eine Zertifikateigenschaft dar, die einen SHA-1-Hash des neuen Zertifikats enthält, das erstellt wird, wenn ein vorhandenes Zertifikat erneuert wird.                                                                                                                      |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Stellt eine Zertifikateigenschaft dar, die den DNS-Namen (Domain Naming System) des Computers enthält, auf dem die Anforderung erstellt wurde.                                                                                                                     |
| [**ICertPropertyRequestOriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Stellt eine Zertifikateigenschaft dar, die den DNS-Namen (Domain Naming System) des Computers enthält, auf dem die Anforderung erstellt wurde.                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



