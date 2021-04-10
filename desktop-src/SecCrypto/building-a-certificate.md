---
description: Erläutert die Aufrufe, die erforderlich sind, um ein Zertifikat zu erstellen.
ms.assetid: 74154b3b-75fc-412f-835c-1a6f54e688c6
title: Zertifikat wird aufgebaut
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8f237fd729499aa5153f12f68657e2ce227da7b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868799"
---
# <a name="building-a-certificate"></a>Zertifikat wird aufgebaut

Die Reihenfolge der Aufrufe beim Aufbau eines Zertifikats lautet wie folgt:

1.  Die Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) initialisiert Module durch Aufrufe von [**icertpolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) und [**icertexit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) (erfolgt einmal bei der Server Initialisierung). Die Zertifizierungsstelle initialisiert die Richtlinie und beendet Module durch Aufrufen von [**ICertPolicy2:: Initialisieren**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-initialize) und [**icertexit:: Initialisieren**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize).
2.  Vermittler Ruft die Zertifizierungsstelle über [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) auf (erfolgt einmal pro Vermittler Initialisierung). Der Vermittler findet die erforderliche Konfigurations Zeichenfolge durch Aufrufen von [**ICertConfig:: GetConfig**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig).
3.  Client ruft den Vermittler über eine Schnittstelle auf, die für den Vermittler spezifisch ist (erfolgt einmal pro Anforderung). Der Client sendet eine [*Zertifikat Anforderung*](../secgloss/c-gly.md) an den Vermittler. Dies kann beispielsweise der Microsoft Internet Explorer sein, der eine Anforderung über die [Zertifikat Registrierungs Steuerung](certificate-enrollment-control.md) an Microsoft Internetinformationsdienste sendet.
4.  Vermittler zur Zertifizierungsstelle über [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) (erfolgt einmal pro Anforderung). Der Vermittler sendet die Zertifikat Anforderung über [**ICertRequest:: Submit**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit)an die Zertifizierungsstelle. Im Fall von Internetinformationsdienste kann dies über Active Server Seiten Skripts erfolgen.
5.  Die Zertifizierungsstelle Ruft das Richtlinien Modul über die [**icertpolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) -Schnittstelle auf (geschieht einmal pro Anforderung). Die Zertifizierungsstelle benachrichtigt das Richtlinien Modul, dass eine Anforderung durch Aufrufen von [**icertpolicy:: verifyrequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)eingegangen ist. Das Richtlinien Modul kann die Anforderung überprüfen und das Zertifikat durch Aufrufen von Methoden der [**icertserverpolicy**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) -Schnittstelle ändern. Das Richtlinien Modul kann dann angeben, dass die Anforderung OK ist (wenn dies der Fall ist, wird das Zertifikat zu diesem Zeitpunkt erstellt), muss die Anforderung verweigert werden, oder die Anforderung sollte angehalten werden.
6.  Optionale Der Administrator Ruft die Zertifizierungsstelle über die [**ICertAdmin**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) -Schnittstelle auf. Wenn die Anforderung angehalten wird, kann der Administrator die Anforderung erneut senden oder ablehnen oder Anforderungs Attribute und-Erweiterungen ändern. Beachten Sie Folgendes: Wenn die Anforderung erneut übermittelt wird, hat das Richtlinien Modul eine weitere Möglichkeit, die Anforderung zu verarbeiten (als Ergebnis eines Aufrufes von [**icertpolicy:: verifyrequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)). Die Aufgabe, die Anforderung erneut zu senden oder zu verweigern, kann mithilfe des MMC-Snap-Ins der Zertifizierungsstelle oder einer anderen Anwendung ausgeführt werden, die **ICertAdmin** verwendet.
7.  Die Zertifizierungsstelle Ruft das Beendigungs Modul über die [**icertexit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) -Schnittstelle auf. Wenn das Beendigungs Modul angegeben hat (wenn [**icertexit:: Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) aufgerufen wurde, in Schritt 1), dass es Zertifikate ausgestellt oder ausstehende Anforderungen ausstehend, wird die [**Zertifizierungsstelle icertexit:: notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify)aufrufen.
8.  Das Exit-Modul ruft die Zertifizierungsstelle über die [**icertserverexit**](/windows/desktop/api/Certif/nn-certif-icertserverexit) -Schnittstelle auf. Das Beendigungs Modul kann die Anforderung und das neue Zertifikat durch Aufrufen von Methoden von **icertserverexit** untersuchen.

 

 
