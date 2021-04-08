---
description: Die folgenden Schnittstellen können verwendet werden, um eine Zertifikat Eigenschaft zu erstellen.
ms.assetid: c64fca58-fb2f-412f-b7c0-5db1979d051b
title: Zertifikat Eigenschafts Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00d0052675436a28438d5f1600a5b0097f8e177a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103749577"
---
# <a name="certificate-property-interfaces"></a>Zertifikat Eigenschafts Schnittstellen

Die folgenden Schnittstellen können verwendet werden, um eine Zertifikat Eigenschaft zu erstellen.



| Schnittstelle                                                                          | BESCHREIBUNG                                                                                                                                                                                                                                               |
|------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Icertproperties**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperties)                                         | Verwaltet eine Auflistung von [**icertproperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty) -Objekten.                                                                                                                                                                                    |
| [**Icertproperty**](/windows/desktop/api/CertEnroll/nn-certenroll-icertproperty)                                             | Ordnet eine externe Eigenschaft einem Zertifikat zu.                                                                                                                                                                                                       |
| [**Icertpropertyarchiviert**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchived)                             | Stellt eine Zertifikat Eigenschaft dar, die angibt, ob ein Zertifikat archiviert wurde.                                                                                                                                                                |
| [**Icertpropertyarchivedkeyhash**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyarchivedkeyhash)               | Stellt einen SHA-1-Hash eines verschlüsselten privaten Schlüssels dar, der für die Archivierung an eine Zertifizierungsstelle gesendet wurde.                                                                                                                                                  |
| [**Icertpropertyautoenroll**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyautoenroll)                         | Stellt eine Zertifikat Eigenschaft dar, die eine Vorlage identifiziert, die so konfiguriert wurde, dass die automatische Registrierung des Zertifikats aktiviert wird.                                                                                                                        |
| [**Icertpropertybackedup**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertybackedup)                             | Stellt eine Zertifikat Eigenschaft dar, die angibt, ob ein Zertifikat gesichert wurde, und wenn ja, das Datum und die Uhrzeit der Speicherung.                                                                                                               |
| [**Icertpropertydescription**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertydescription)                       | Ermöglicht das angeben und Abrufen einer Zeichenfolge, die beschreibende Informationen für ein Zertifikat enthält.                                                                                                                                                     |
| [**Icertpropertyeinschreibung**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyenrollment)                         | Stellt eine Zertifikat Eigenschaft dar, die Informationen zu Zertifikaten und Zertifizierungsstellen enthält, die erstellt werden, wenn der Client die Methode [**registrieren**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) für die [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Schnittstelle aufruft. |
| [**Icertpropertyregistrimentpolicyserver**](/windows/desktop/api/Certenroll/nn-certenroll-icertpropertyenrollmentpolicyserver) | Stellt eine externe Zertifikat Eigenschaft dar, die Informationen zu einem Zertifikatregistrierungs-Richtlinien Server (CEP) und einem Zertifikat Registrierungs Server (CES) enthält.                                                                                       |
| [**Icertpropertyfriendlyname**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyfriendlyname)                     | Ermöglicht das angeben und Abrufen einer Zeichenfolge, die den anzeigen Amen eines Zertifikats enthält.                                                                                                                                                             |
| [**Icertpropertykeyprovinfo**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertykeyprovinfo)                       | Stellt eine Zertifikat Eigenschaft dar, die Informationen über einen privaten Schlüssel enthält.                                                                                                                                                                          |
| [**Icertpropertyrenewal**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrenewal)                               | Stellt eine Zertifikat Eigenschaft dar, die einen SHA-1-Hash des neuen Zertifikats enthält, das erstellt wird, wenn ein vorhandenes Zertifikat erneuert wird.                                                                                                                      |
| [**Icertpropertyrequestoriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Stellt eine Zertifikat Eigenschaft dar, die den DNS-Namen (Domain Name System) des Computers enthält, auf dem die Anforderung erstellt wurde.                                                                                                                     |
| [**Icertpropertyrequestoriginator**](/windows/desktop/api/CertEnroll/nn-certenroll-icertpropertyrequestoriginator)           | Stellt eine Zertifikat Eigenschaft dar, die den DNS-Namen (Domain Name System) des Computers enthält, auf dem die Anforderung erstellt wurde.                                                                                                                     |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[CertEnroll-Schnittstellen](certenroll-interfaces.md)
</dt> </dl>

 

 



