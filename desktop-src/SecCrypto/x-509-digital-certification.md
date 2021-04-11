---
description: Die digitale Zertifizierung umfasst einen Prozess zum Signieren des Zertifikats. Dieser Prozess wird beschrieben.
ms.assetid: bb0382fd-2924-429f-933b-84ab61debf20
title: Digitale X.509-Zertifizierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f2f737a658e3e2c44876a23206f23a3d45ff3e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104216195"
---
# <a name="x509-digital-certification"></a>Digitale X.509-Zertifizierung

Eine primäre Aufgabe eines [*digitalen Zertifikats*](../secgloss/d-gly.md) besteht darin, den Zugriff auf den [*öffentlichen Schlüssel*](../secgloss/p-gly.md)des Antragstellers bereitzustellen. Das Zertifikat bestätigt auch, dass der öffentliche Schlüssel des Zertifikats zum Betreff des Zertifikats gehört. Eine Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) kann z. b. eine spezielle Nachricht (die Zertifikat Informationen) digital signieren, die den Namen eines Benutzers enthält, z. b. "Alice" und ihren öffentlichen Schlüssel. Dies muss so erfolgen, dass jeder Benutzer überprüfen kann, ob das Zertifikat ausgestellt und von keinem anderen als der Zertifizierungsstelle signiert wurde. Wenn die Zertifizierungsstelle vertrauenswürdig ist und überprüft werden kann, ob das Zertifikat von Alice von dieser Zertifizierungsstelle ausgestellt wurde, kann jeder Empfänger von Alice das Zertifikat für den öffentlichen Schlüssel von Alice von diesem Zertifikat vertrauen.

Die typische Implementierung der digitalen Zertifizierung umfasst einen Prozess zum Signieren des Zertifikats.

Der Prozess sieht folgendermaßen aus:

1.  Alice sendet eine signierte [*Zertifikat Anforderung*](../secgloss/c-gly.md) mit Ihrem Namen, Ihrem öffentlichen Schlüssel und möglicherweise zusätzlichen Informationen an eine Zertifizierungsstelle.
2.  Die Zertifizierungsstelle erstellt die Nachricht *m* aus der Anforderung von Alice. Die Zertifizierungsstelle signiert die Nachricht mit Ihrem privaten Schlüssel und erstellt eine separate Signatur Nachricht ( *sig*). Die Zertifizierungsstelle gibt die Nachricht, *m* und die Signatur, *sig*, an Alice zurück. *M* und *sig* bilden das Zertifikat von Alice.
3.  Alice sendet beide Teile Ihres Zertifikats an Bob, um ihm Zugriff auf Ihren öffentlichen Schlüssel zu verschaffen.
4.  Bob überprüft die Signatur, *sig* mithilfe des öffentlichen Schlüssels der Zertifizierungsstelle. Wenn die Signatur gültig ist, akzeptiert Sie den öffentlichen Schlüssel im Zertifikat als öffentlichen Schlüssel von Alice.

Wie bei jeder [*digitalen Signatur*](../secgloss/d-gly.md)kann jeder Empfänger mit Zugriff auf den öffentlichen Schlüssel der Zertifizierungsstelle ermitteln, ob eine bestimmte Zertifizierungsstelle das Zertifikat signiert hat. Dieser Prozess erfordert keinen Zugriff auf geheime Informationen. Das soeben vorgestellte Szenario geht davon aus, dass Bob Zugriff auf den öffentlichen Schlüssel der Zertifizierungsstelle hat. Bob hätte Zugriff auf diesen Schlüssel, wenn er über eine Kopie des Zertifikats der Zertifizierungsstelle verfügt, das den öffentlichen Schlüssel enthält.

Digitale [*X. 509*](../secgloss/x-gly.md) -Zertifikate enthalten nicht nur den Namen und den öffentlichen Schlüssel eines Benutzers, sondern auch andere Informationen über den Benutzer. Diese Zertifikate sind mehr als Schritt Steine in einer digitalen Vertrauens Hierarchie. Sie ermöglichen es der Zertifizierungsstelle, dem Empfänger eines Zertifikats die Möglichkeit zu geben, nicht nur den öffentlichen Schlüssel des Zertifikats zu vertrauen, sondern auch andere Informationen über den Betreff des Zertifikats. Andere Informationen können z. b. eine e-Mail-Adresse, eine Autorisierung zum Signieren von Dokumenten eines bestimmten Werts oder die Autorisierung sein, um eine Zertifizierungsstelle zu werden und andere Zertifikate zu signieren.

X. 509-Zertifikate und viele andere Zertifikate haben eine gültige Zeitspanne. Ein Zertifikat kann ablaufen und ist nicht mehr gültig. Ein Zertifikat kann von einer Zertifizierungsstelle aus verschiedenen Gründen widerrufen werden. Um Widerrufungen zu verarbeiten, verwaltet eine Zertifizierungsstelle eine Liste mit gesperrten Zertifikaten, die als [*Zertifikat Sperr Liste*](../secgloss/c-gly.md) (CRL) bezeichnet wird. Netzwerk Benutzer greifen auf die CRL zu, um die Gültigkeit eines Zertifikats zu bestimmen.

 

 
