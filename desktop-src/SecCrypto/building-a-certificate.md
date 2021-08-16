---
description: Erläutert die Aufrufe, die zum Erstellen eines Zertifikats erforderlich sind.
ms.assetid: 74154b3b-75fc-412f-835c-1a6f54e688c6
title: Erstellen eines Zertifikats
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e497f20e8a20d4e401ce89a85d1f8a312dad76865a6c3dfb523d8f2526125c3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117772975"
---
# <a name="building-a-certificate"></a>Erstellen eines Zertifikats

Die Reihenfolge der Aufrufe beim Erstellen eines Zertifikats lautet wie folgt:

1.  [*Die Zertifizierungsstelle*](../secgloss/c-gly.md) initialisiert Module durch Aufrufe von [**ICertPolicy**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) und [**ICertExit**](/windows/desktop/api/Certexit/nn-certexit-icertexit) (bei der Serverinitialisierung einmal). Die Zertifizierungsstelle initialisiert die Richtlinien- und Exitmodule, indem [**sie ICertPolicy2::Initialize**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-initialize) und [**ICertExit::Initialize aufruft.**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize)
2.  Der Vermittler ruft die Zertifizierungsstelle über [**ICertConfig**](/windows/desktop/api/Certcli/nn-certcli-icertconfig) auf (erfolgt einmal pro zwischengeschalteter Initialisierung). Der Vermittler findet die benötigte Konfigurationszeichenfolge, indem er [**ICertConfig::GetConfig aufruft.**](/windows/desktop/api/Certcli/nf-certcli-icertconfig-getconfig)
3.  Der Client ruft den Vermittler über eine schnittstelle auf, die für den Vermittler spezifisch ist (erfolgt einmal pro Anforderung). Der Client sendet eine [*Zertifikatanforderung*](../secgloss/c-gly.md) an den Vermittler. Dies kann beispielsweise sein, dass Microsoft Internet Explorer Anforderung über die Zertifikatregistrierungssteuerung [an](certificate-enrollment-control.md) die Microsoft-Internetinformationsdienste.
4.  Zwischengeschaltet zur Zertifizierungsstelle über [**ICertRequest**](/windows/desktop/api/Certcli/nn-certcli-icertrequest) (erfolgt einmal pro Anforderung). Der Vermittler sendet die Zertifikatanforderung über [**ICertRequest::Submit an die Zertifizierungsstelle.**](/windows/desktop/api/Certcli/nf-certcli-icertrequest-submit) Im Fall von Internetinformationsdienste kann dies über Seitenskripts Active Server werden.
5.  Die Zertifizierungsstelle ruft das Richtlinienmodul über die [**ICertPolicy-Schnittstelle**](/windows/desktop/api/Certpol/nn-certpol-icertpolicy) auf (einmal pro Anforderung). Die Zertifizierungsstelle benachrichtigt das Richtlinienmodul, dass eine Anforderung eingetroffen ist, indem sie [**ICertPolicy::VerifyRequest aufruft.**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest) Das Richtlinienmodul kann die Anforderung untersuchen und das Zertifikat ändern, indem es Methoden der [**ICertServerPolicy-Schnittstelle**](/windows/desktop/api/Certif/nn-certif-icertserverpolicy) aufruft. Das Richtlinienmodul kann dann angeben, dass die Anforderung OK ist (wenn dies der Fall ist, wird das Zertifikat zu diesem Zeitpunkt erstellt), die Anforderung verweigert oder die Anforderung angehalten werden soll.
6.  (Optional) Der Administrator ruft die Zertifizierungsstelle über die [**ICertAdmin-Schnittstelle**](/windows/desktop/api/Certadm/nn-certadm-icertadmin) auf. Wenn die Anforderung angehalten wird, kann der Administrator die Anforderung erneut senden oder verweigern oder Anforderungsattribute und Erweiterungen ändern. Beachten Sie, dass das Richtlinienmodul eine weitere Möglichkeit hat, die Anforderung zu verarbeiten, wenn die Anforderung erneut ausgegeben wird (als Ergebnis eines Aufrufs von [**ICertPolicy::VerifyRequest**](/windows/desktop/api/Certpol/nf-certpol-icertpolicy-verifyrequest)). Die Aufgabe des erneuten Sendens oder Verweigerns der Anforderung kann mit dem MMC-Snap-In der Zertifizierungsstelle oder einer anderen Anwendung ausgeführt werden, die **ICertAdmin verwendet.**
7.  Die Zertifizierungsstelle ruft das Exitmodul über die [**ICertExit-Schnittstelle**](/windows/desktop/api/Certexit/nn-certexit-icertexit) auf. Wenn das Exitmodul (als [**ICertExit::Initialize**](/windows/desktop/api/Certexit/nf-certexit-icertexit-initialize) in Schritt 1 aufgerufen wurde) angegeben hat, dass es an ausgestellten Zertifikaten oder ausstehenden Anforderungen interessiert ist, wird von der Zertifizierungsstelle [**ICertExit::Notify**](/windows/desktop/api/Certexit/nf-certexit-icertexit-notify)aufgerufen.
8.  Das Exitmodul ruft die Zertifizierungsstelle über die [**ICertServerExit-Schnittstelle**](/windows/desktop/api/Certif/nn-certif-icertserverexit) auf. Das Exitmodul kann die Anforderung und das neue Zertifikat durch Aufrufen der Methoden von **ICertServerExit untersuchen.**

 

 
