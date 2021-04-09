---
description: Eine Zertifizierungsstelle (ZS) beglaubigt die Identität von Benutzern, Computern und Unternehmen.
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: Zertifizierungsstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aedcbac1310c3bcc584f6f1572091044ae0d6aad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103866987"
---
# <a name="certification-authorities"></a>Zertifizierungsstellen

Eine [*Zertifizierungsstelle (Certification Authority*](/windows/desktop/SecGloss/c-gly) , ca) ist für das Testen der Identität von Benutzern, Computern und Organisationen verantwortlich. Die ZS authentifiziert eine Entität und bürgt durch die Ausstellung eines digital signierten Zertifikats für diese Entität. ZS können Zertifikate außerdem verwalten, widerrufen und erneuern.

Eine Zertifizierungsstelle kann öffentlich oder privat sein. Eine öffentliche Zertifizierungsstelle stellt dem öffentlichen Zertifizierungsdienst (in der Regel für eine Gebühr) über das Internet zur Verfügung. Eine private Zertifizierungsstelle stellt diesen Dienst den Mitgliedern einer durch Trennzeichen getrennten Auffüllung wie z. b. der Mitarbeiter eines Unternehmens oder der Mitglieder einer anderen privaten Gruppe zur Verfügung.

Die Methode, mit der eine Zertifizierungsstelle einen Endbenutzer authentifiziert, ist unterschiedlich und über den Rahmen dieser Dokumentation hinaus. Allerdings variieren Authentifizierungsmethoden je nach Anbietertyp. Eine private Zertifizierungsstelle kann z. b. die Identität von Endbenutzern durch den Verweis auf einen Gruppen Roer (z. b. eine Mitarbeiter Datenbank oder Active Directory) einrichten. Die Authentifizierungsmethoden, die von einer öffentlichen Zertifizierungsstelle ausgeführt werden, sind im Allgemeinen komplexer und hängen teilweise von der Sicherheitsstufe ab, die vom Zertifikat zugesichert wird.

Wenn die Auffüllung einer Public Key-Infrastruktur (PKI) zunimmt, kann es für eine einzelne Zertifizierungsstelle schwierig werden, alle ausgestellten Zertifikate effektiv zu verwalten. Die Zertifizierungsstelle kann kompensieren, indem andere Zertifizierungsstellen in der PKI zum Ausstellen von Zertifikaten autorisiert werden. Die erste Zertifizierungsstelle wird als "root" bezeichnet, und die Zertifizierungsstelle, die Sie autorisiert, werden als untergeordnete Elemente bezeichnet. Untergeordnete CAS können auch Ihre eigenen Niederlassungen innerhalb der vom Stamm festgelegten Grenzwerte festlegen. Die resultierende Struktur wird als Zertifikat Hierarchie bezeichnet. Die Zertifikate, die an die Zertifizierungsstelle unten in der Hierarchie ausgegeben werden, enthalten ausreichend Zertifikate, um einen Pfad zurück zum Stamm zu verfolgen. Dies wird als Zertifikat Kette bezeichnet.

Der Begriff Zertifizierungsstelle kann sowohl auf die Organisation, die für die Identität eines Endbenutzers bürgt, als auch auf den Server verweisen, der von der Organisation zum Ausstellen und Verwalten von Zertifikaten verwendet wird. Ein Windows Server kann so konfiguriert werden, dass er als Zertifizierungsstellen Server fungiert. diese Dokumentation bezieht sich in der Regel auf den Server, wenn der Begriff "ca" verwendet wird.

Die Zertifikatregistrierungs-API interagiert mit einer Zertifizierungsstelle vor allem mithilfe des [**IX509Enrollment**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) -Objekts. Die Methode [**registrieren**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) für dieses Objekt kann eine Zertifikat Anforderung automatisch codieren, an die Zertifizierungsstelle senden und das ausgestellte Zertifikat installieren. Sie können auch ein initialisiertes **IX509Enrollment** -Objekt für die Out-of-Band-Registrierung oder für die verzögerte Registrierung verwenden. Außerdem können Sie das [**IX509EnrollmentStatus**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) -Objekt verwenden, um den Registrierungsstatus zu überwachen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKI-Elemente](about-pki-components.md)
</dt> </dl>

 

 
