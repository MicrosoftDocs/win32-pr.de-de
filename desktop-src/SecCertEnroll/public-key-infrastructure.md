---
description: Bei der Kryptografie mit öffentlichem Schlüssel (auch als Kryptografie mit asymmetrischem Schlüssel bezeichnet) wird ein Schlüsselpaar zum Verschlüsseln und Entschlüsseln von Inhalten verwendet.
ms.assetid: 93f65367-ca4b-4b44-9833-0653cfd3f3d3
title: Public Key-Infrastruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55e4ff0b2b3912bc44851be105c2e2b15200eb62
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106347455"
---
# <a name="public-key-infrastructure"></a>Public Key-Infrastruktur

Bei der Kryptografie mit öffentlichem Schlüssel (auch als Kryptografie mit asymmetrischem Schlüssel bezeichnet) wird ein Schlüsselpaar zum Verschlüsseln und Entschlüsseln von Inhalten verwendet. Das Schlüsselpaar besteht aus einem öffentlichen und einem privaten Schlüssel, der mathematisch verknüpft ist. Eine Person, die eine sichere Kommunikation mit anderen durchführen möchte, kann den [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly) verteilen, muss den geheimen [*Schlüssel des privaten Schlüssels*](/windows/desktop/SecGloss/p-gly) jedoch beibehalten. Inhalte, die mit einem der Schlüssel verschlüsselt wurden, können mit dem anderen entschlüsselt werden. Nehmen wir beispielsweise an, dass Bob eine sichere e-Mail-Nachricht an Alice senden möchte. Dies kann auf folgende Weise erreicht werden:

1.  Bob und Alice verfügen über eigene Schlüsselpaare. Sie haben Ihre privaten Schlüssel sicher in sich selbst aufbewahrt und ihre öffentlichen Schlüssel direkt an Sie gesendet.
2.  Bob verwendet den öffentlichen Schlüssel von Alice, um die Nachricht zu verschlüsseln und an Sie zu senden.
3.  Alice verwendet Ihren privaten Schlüssel zum Entschlüsseln der Nachricht.

In diesem vereinfachten Beispiel wird mindestens ein offensichtliches Problem hervorgehoben, das Bob über den öffentlichen Schlüssel verfügen muss, den er zum Verschlüsseln der Nachricht verwendet hat. Das heißt, er kann nicht mit Sicherheit wissen, dass der Schlüssel, den er für die Verschlüsselung verwendet hat, tatsächlich zu Alice gehört. Es ist möglich, dass eine andere Partei, die den Kommunikationskanal zwischen Bob und Alice überwacht, einen anderen Schlüssel ersetzt.

Das Konzept der Public Key-Infrastruktur wurde entwickelt, um dieses Problem und andere zu beheben. Eine Public Key-Infrastruktur (PKI) besteht aus Software-und Hardware Elementen, die von einem vertrauenswürdigen Drittanbieter verwendet werden können, um die Integrität und den Besitz eines öffentlichen Schlüssels zu gewährleisten. Die vertrauenswürdige Partei, die als Zertifizierungsstelle ( [*Certification Authority*](/windows/desktop/SecGloss/c-gly) , ca) bezeichnet wird, erreicht dies in der Regel durch die Ausgabe signierter (verschlüsselter) Binär Zertifikate, die die Identität des Zertifikat Antragstellers bestätigen und diese Identität an den im Zertifikat enthaltenen öffentlichen Schlüssel binden. Die Zertifizierungsstelle signiert das Zertifikat mit dem privaten Schlüssel. Der entsprechende öffentliche Schlüssel wird für alle interessierten Parteien in einem selbst signierten Zertifizierungsstellen Zertifikat ausgegeben. Wenn eine Zertifizierungsstelle verwendet wird, kann das vorherige Beispiel folgendermaßen geändert werden:

1.  Angenommen, die Zertifizierungsstelle hat ein signiertes digitales Zertifikat ausgestellt, das den öffentlichen Schlüssel enthält. Das Zertifikat wird von der Zertifizierungsstelle selbst signiert, indem der private Schlüssel verwendet wird, der dem öffentlichen Schlüssel im Zertifikat entspricht.
2.  Alice und Bob stimmen zu, dass Sie die Zertifizierungsstelle zum Überprüfen Ihrer Identitäten verwenden.
3.  Alice fordert von der Zertifizierungsstelle ein Zertifikat für öffentliche Schlüssel an.
4.  Die Zertifizierungsstelle überprüft Ihre Identität, berechnet einen Hash der Inhalte, aus denen Ihr Zertifikat besteht, signiert den Hash mithilfe des privaten Schlüssels, der dem öffentlichen Schlüssel im veröffentlichten Zertifizierungsstellen Zertifikat entspricht, erstellt ein neues Zertifikat, indem der Zertifikat Inhalt und der signierte Hash verkettet werden, und das neue Zertifikat wird öffentlich verfügbar.
5.  Bob Ruft das Zertifikat ab, entschlüsselt den signierten Hash mithilfe des öffentlichen Schlüssels der Zertifizierungsstelle, berechnet einen neuen Hash des Zertifikats Inhalts und vergleicht die beiden Hashes. Wenn die Hashwerte Stimmen, wird die Signatur überprüft, und Bob kann davon ausgehen, dass der öffentliche Schlüssel im Zertifikat tatsächlich zu Alice gehört.
6.  Bob verwendet den überprüften öffentlichen Schlüssel von Alice, um eine Nachricht zu verschlüsseln.
7.  Alice verwendet Ihren privaten Schlüssel zum Entschlüsseln der Nachricht aus Bob.

Zusammengefasst ermöglicht der Zertifikat Signier Vorgang Bob, sicherzustellen, dass der öffentliche Schlüssel während der Übertragung nicht manipuliert oder beschädigt wurde. Vor dem Ausstellen eines Zertifikats erstellt die Zertifizierungsstelle einen Hashwert für den Inhalt, signiert (verschlüsselt) den Hash mithilfe seines eigenen privaten Schlüssels und schließt den verschlüsselten Hash in das ausgegebene Zertifikat ein. Bob überprüft den Zertifikat Inhalt, indem er den Hash mit dem öffentlichen Schlüssel der Zertifizierungsstelle entschlüsselt, einen separaten Hash der Zertifikat Inhalte durchführt und die beiden Hashes vergleicht. Wenn Sie einander entsprechen, kann Bob sicher sein, dass das Zertifikat und der öffentliche Schlüssel nicht geändert wurden.

Eine typische PKI besteht aus den folgenden Elementen.

| Element                            | BESCHREIBUNG                                                                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zertifizierungsstelle<br/> | Fungiert als Stamm der Vertrauensstellung in einer Public Key-Infrastruktur und stellt Dienste bereit, mit denen die Identität von Einzelpersonen, Computern und anderen Entitäten in einem Netzwerk authentifiziert wird.<br/>      |
| Registrierungsstelle<br/>  | Wird von einer Stamm Zertifizierungsstelle zertifiziert, um Zertifikate für bestimmte vom Stamm zugelassene Verwendungen auszustellen. In einer Microsoft-PKI wird eine Registrierungsstelle (Registration Authority, RA) in der Regel als untergeordnete Zertifizierungsstelle bezeichnet.<br/> |
| Zertifikat Datenbank<br/>    | Speichert Zertifikat Anforderungen und ausgestellte und widerrufene Zertifikate und Zertifikat Anforderungen für die Zertifizierungsstelle oder RA.<br/>                                                                       |
| Zertifikatspeicher<br/>       | Speichert ausgestellte Zertifikate und ausstehende oder abgelehnte Zertifikat Anforderungen auf dem lokalen Computer.<br/>                                                                                  |
| Schlüssel Archivierungs Server<br/>     | Speichert verschlüsselte private Schlüssel in der Zertifikat Datenbank zur Wiederherstellung nach dem Verlust.<br/>                                                                                              |



 

Die Zertifikatregistrierungs-API ermöglicht es Ihnen, Zertifikat-und Schlüssel Archivierungsanforderungen an Zertifizierungs-und Registrierungsstellen zu übermitteln und das ausgestellte Zertifikat auf einem lokalen Computer zu installieren. Sie können die Zertifikat Datenbank oder den Zertifikat Speicher nicht direkt bearbeiten.

In den folgenden Themen wird die Public Key-Infrastruktur von Microsoft ausführlicher erläutert:

-   [X. 509-Zertifikate für öffentliche Schlüssel](about-x-509-public-key-certificates.md)
-   [PKI-Elemente](about-pki-components.md)
-   [Trust-Modelle](about-trust-models.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Zertifikatregistrierungs-API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

