---
description: Eine Zertifizierungsstelle (ZS) beglaubigt die Identität von Benutzern, Computern und Unternehmen.
ms.assetid: c8ddce19-299c-45ca-9992-865928098dc3
title: Zertifizierungsstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11b5f48c897c74e5f0bf7d4d3b1e21b8f89d33e72cdfa46aefe726f714fbc267
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904499"
---
# <a name="certification-authorities"></a>Zertifizierungsstellen

Eine [*Zertifizierungsstelle*](/windows/desktop/SecGloss/c-gly) ist für den Nachweis der Identität von Benutzern, Computern und Organisationen verantwortlich. Die ZS authentifiziert eine Entität und bürgt durch die Ausstellung eines digital signierten Zertifikats für diese Entität. ZS können Zertifikate außerdem verwalten, widerrufen und erneuern.

Eine Zertifizierungsstelle kann öffentlich oder privat sein. Eine öffentliche Zertifizierungsstelle stellt Zertifizierungsdienste (in der Regel gegen Gebühr) für die Öffentlichkeit über das Internet bereit. Eine private Zertifizierungsstelle stellt diesen Dienst für mitglieder einer durch Trennzeichen getrennten Grundgesamtheit bereit, z. B. die Mitarbeiter eines Unternehmens oder Mitglieder einer anderen privaten Gruppe.

Die Art und Weise, mit der eine Zertifizierungsstelle einen Endbenutzer authentifiziert, ist unterschiedlich und übersteigt den Rahmen dieser Dokumentation. Natürlich variieren die Authentifizierungsmethoden jedoch je nach Anbietertyp. Beispielsweise kann eine private Zertifizierungsstelle die Identität von Endbenutzern einrichten, indem sie auf eine Gruppengruppe wie eine Mitarbeiterdatenbank oder Active Directory verweist. Die Authentifizierungsmethoden, die von einer öffentlichen Zertifizierungsstelle ausgeführt werden, sind im Allgemeinen komplexer und hängen teilweise von der Sicherheitsstufe ab, die vom Zertifikat garantiert wird.

Mit zunehmender Auffüllung einer Public Key-Infrastruktur (PKI) kann es für eine einzelne Zertifizierungsstelle schwierig werden, alle ausgestellten Zertifikate effektiv zu verwalten. Die Zertifizierungsstelle kann dies kompensieren, indem sie andere Zertifizierungsstellen in der PKI autorisiert, Zertifikate auszustellen. Die anfängliche Zertifizierungsstelle wird als Stamm bezeichnet, und die von ihr autorisierten Zertifizierungsstellen werden als untergeordnete Elemente bezeichnet. Untergeordnete Zertifizierungsstellen können auch ihre eigenen Niederlassungen innerhalb der vom Stamm festgelegten Grenzwerte festlegen. Die resultierende Struktur wird als Zertifikathierarchie bezeichnet. Die Zertifikate, die für Zertifizierungsstellen weiter unten in der Hierarchie ausgestellt werden, enthalten genügend Zertifikate, um einen Pfad zurück zum Stamm zu verfolgen. Dies wird als Zertifikatkette bezeichnet.

Der Begriff Zertifizierungsstelle kann sich sowohl auf die Organisation beziehen, die die Identität eines Endbenutzers angibt, als auch auf den Server, der von der Organisation zum Ausstellen und Verwalten von Zertifikaten verwendet wird. Ein Windows Server kann so konfiguriert werden, dass er als ZS-Server fungiert, und diese Dokumentation bezieht sich in der Regel auf den Server, wenn der Begriff ZS verwendet wird.

Die Zertifikatregistrierungs-API interagiert hauptsächlich mithilfe des [**IX509Enrollment-Objekts**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollment) mit einer Zertifizierungsstelle. Die [**Enroll-Methode**](/windows/desktop/api/CertEnroll/nf-certenroll-ix509enrollment-enroll) für dieses Objekt kann automatisch eine Zertifikatanforderung codieren, an die Zertifizierungsstelle übermitteln und das ausgestellte Zertifikat installieren. Sie können auch ein initialisiertes **IX509Enrollment-Objekt** für die Out-of-Band-Registrierung oder für die verzögerte Registrierung verwenden. Darüber hinaus können Sie das [**IX509EnrollmentStatus-Objekt**](/windows/desktop/api/CertEnroll/nn-certenroll-ix509enrollmentstatus) verwenden, um den Registrierungsstatus zu überwachen.

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[PKI-Elemente](about-pki-components.md)
</dt> </dl>

 

 
