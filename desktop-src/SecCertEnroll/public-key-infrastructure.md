---
description: Die Kryptografie mit öffentlichem Schlüssel (auch als Kryptografie mit asymmetrischem Schlüssel bezeichnet) verwendet ein Schlüsselpaar zum Verschlüsseln und Entschlüsseln von Inhalten.
ms.assetid: 93f65367-ca4b-4b44-9833-0653cfd3f3d3
title: Public Key-Infrastruktur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 09a306f227a3e39c32b7e0eef2dbf1dc4ae9d59942096fb71428339d8a166a04
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "120101130"
---
# <a name="public-key-infrastructure"></a>Public Key-Infrastruktur

Die Kryptografie mit öffentlichem Schlüssel (auch als Kryptografie mit asymmetrischem Schlüssel bezeichnet) verwendet ein Schlüsselpaar zum Verschlüsseln und Entschlüsseln von Inhalten. Das Schlüsselpaar besteht aus einem öffentlichen und einem privaten Schlüssel, die mathematisch miteinander verknüpft sind. Eine Person, die sicher mit anderen kommunizieren möchte, kann den [*öffentlichen Schlüssel*](/windows/desktop/SecGloss/p-gly) verteilen, muss den [*privaten Schlüssel*](/windows/desktop/SecGloss/p-gly) jedoch geheim halten. Inhalte, die mit einem der Schlüssel verschlüsselt werden, können mithilfe des anderen entschlüsselt werden. Angenommen, Bob möchte eine sichere E-Mail an Alice senden. Dies kann auf folgende Weise erreicht werden:

1.  Sowohl Bob als auch Alice verfügen über eigene Schlüsselpaare. Sie haben ihre privaten Schlüssel sicher für sich selbst aufbewahrt und ihre öffentlichen Schlüssel direkt untereinander gesendet.
2.  Bob verwendet den öffentlichen Schlüssel von Alice, um die Nachricht zu verschlüsseln und an sie zu senden.
3.  Alice verwendet ihren privaten Schlüssel, um die Nachricht zu entschlüsseln.

In diesem vereinfachten Beispiel wird mindestens ein offensichtliches Problem hervorgehoben, das Bob hinsichtlich des öffentlichen Schlüssels haben muss, den er zum Verschlüsseln der Nachricht verwendet hat. Das heißt, er weiß nicht mit Sicherheit, dass der Schlüssel, den er für die Verschlüsselung verwendet hat, tatsächlich Alice gehört hat. Es ist möglich, dass eine andere Partei, die den Kommunikationskanal zwischen Bob und Alice überwacht, einen anderen Schlüssel ersetzt hat.

Das Public Key-Infrastrukturkonzept wurde weiterentwickelt, um dieses und andere Probleme zu lösen. Eine Public Key-Infrastruktur (PKI) besteht aus Software- und Hardwareelementen, die ein vertrauenswürdiger Drittanbieter verwenden kann, um die Integrität und den Besitz eines öffentlichen Schlüssels herzustellen. Die vertrauenswürdige Partei, die als [*Zertifizierungsstelle*](/windows/desktop/SecGloss/c-gly) bezeichnet wird, erreicht dies in der Regel durch Ausstellen signierter (verschlüsselter) binärer Zertifikate, die die Identität des Zertifikatsubjekts bestätigen und diese Identität an den öffentlichen Schlüssel binden, der im Zertifikat enthalten ist. Die Zertifizierungsstelle signiert das Zertifikat mithilfe ihres privaten Schlüssels. Er stellt den entsprechenden öffentlichen Schlüssel für alle interessierten Parteien in einem selbstsignieren Zertifizierungsstellenzertifikat aus. Wenn eine Zertifizierungsstelle verwendet wird, kann das vorherige Beispiel wie folgt geändert werden:

1.  Angenommen, die Zertifizierungsstelle hat ein signiertes digitales Zertifikat ausgestellt, das den öffentlichen Schlüssel enthält. Die Zertifizierungsstelle signiert dieses Zertifikat selbst mithilfe des privaten Schlüssels, der dem öffentlichen Schlüssel im Zertifikat entspricht.
2.  Alice und Bob stimmen zu, die Zertifizierungsstelle zum Überprüfen ihrer Identitäten zu verwenden.
3.  Alice fordert ein Zertifikat mit öffentlichem Schlüssel von der Zertifizierungsstelle an.
4.  Die Zertifizierungsstelle überprüft ihre Identität, berechnet einen Hash des Inhalts, aus dem ihr Zertifikat besteht, signiert den Hash mithilfe des privaten Schlüssels, der dem öffentlichen Schlüssel im veröffentlichten Zertifizierungsstellenzertifikat entspricht, erstellt ein neues Zertifikat durch Verketten des Zertifikatinhalts und des signierten Hashs und macht das neue Zertifikat öffentlich verfügbar.
5.  Bob ruft das Zertifikat ab, entschlüsselt den signierten Hash mithilfe des öffentlichen Schlüssels der Zertifizierungsstelle, berechnet einen neuen Hash des Zertifikatinhalts und vergleicht die beiden Hashes. Wenn die Hashes übereinstimmen, wird die Signatur überprüft, und Bob kann davon ausgehen, dass der öffentliche Schlüssel im Zertifikat tatsächlich alice gehört.
6.  Bob verwendet alices verifizierten öffentlichen Schlüssel, um eine Nachricht an sie zu verschlüsseln.
7.  Alice verwendet ihren privaten Schlüssel, um die Nachricht von Bob zu entschlüsseln.

Zusammenfassend lässt sich feststellen, dass Bob beim Signieren des Zertifikats überprüfen kann, ob der öffentliche Schlüssel während der Übertragung nicht manipuliert oder beschädigt wurde. Vor dem Ausstellen eines Zertifikats hasht die Zertifizierungsstelle den Inhalt, signiert (verschlüsselt) den Hash mithilfe eines eigenen privaten Schlüssels und schließt den verschlüsselten Hash in das ausgestellte Zertifikat ein. Bob überprüft den Inhalt des Zertifikats, indem er den Hash mit dem öffentlichen Schlüssel der Zertifizierungsstelle entschlüsselt, einen separaten Hash des Zertifikatinhalts ausführt und die beiden Hashes vergleicht. Wenn sie übereinstimmen, kann Bob sicher sein, dass das Zertifikat und der darin enthaltene öffentliche Schlüssel nicht geändert wurden.

Eine typische PKI besteht aus den folgenden Elementen.

| Element                            | BESCHREIBUNG                                                                                                                                                                               |
|------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Zertifizierungsstelle<br/> | Fungiert als Vertrauensstamm in einer Public Key-Infrastruktur und stellt Dienste bereit, die die Identität von Personen, Computern und anderen Entitäten in einem Netzwerk authentifizieren.<br/>      |
| Registrierungsstelle<br/>  | Wird von einer Stammzertifizierungsstelle zertifiziert, um Zertifikate für bestimmte Vom Stamm zugelassene Verwendungen auszustellen. In einer Microsoft-PKI wird eine Registrierungsstelle in der Regel als untergeordnete Zertifizierungsstelle bezeichnet.<br/> |
| Zertifikatdatenbank<br/>    | Speichert Zertifikatanforderungen sowie ausgestellte und widerrufene Zertifikate und Zertifikatanforderungen für die Zertifizierungsstelle oder ra.<br/>                                                                       |
| Zertifikatspeicher<br/>       | Speichert ausgestellte Zertifikate und ausstehende oder abgelehnte Zertifikatanforderungen auf dem lokalen Computer.<br/>                                                                                  |
| Schlüsselarchivserver<br/>     | Speichert verschlüsselte private Schlüssel zur Wiederherstellung nach einem Verlust in der Zertifikatdatenbank.<br/>                                                                                              |



 

Mit der Zertifikatregistrierungs-API können Sie Zertifikat- und Schlüsselarchivanforderungen an Zertifizierungs- und Registrierungsstellen übermitteln und das ausgestellte Zertifikat auf einem lokalen Computer installieren. Sie können die Zertifikatdatenbank oder den Zertifikatspeicher nicht direkt bearbeiten.

In den folgenden Themen wird die Public Key-Infrastruktur von Microsoft ausführlicher erläutert:

-   [X.509-Zertifikate mit öffentlichem Schlüssel](about-x-509-public-key-certificates.md)
-   [PKI-Elemente](about-pki-components.md)
-   [Vertrauensstellungsmodelle](about-trust-models.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[Informationen zur Zertifikatregistrierungs-API](about-the-certificate-enrollment-api.md)
</dt> </dl>

 

