---
description: Zertifikatdienste sind eine Grundlage für die Public Key-Infrastruktur (PKI), die die Mittel zum Schützen und Authentifizieren von Informationen bietet.
ms.assetid: c18f46ca-e805-4b33-8014-79dc34c18531
title: Zertifikate und öffentliche Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d8d5f1996549184b8c56388bdb3ae8395eee077bca31b03e074f4dda8568805b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117770620"
---
# <a name="certificates-and-public-keys"></a>Zertifikate und öffentliche Schlüssel

Zertifikatdienste sind eine Grundlage für die Public Key-Infrastruktur (PKI), die die Mittel zum Schützen und Authentifizieren von Informationen bietet. Die Beziehung zwischen einem Zertifikatinhaber, der Identität des Zertifikatinhabers und dem öffentlichen Schlüssel des Zertifikatinhabers ist ein wichtiger Teil der PKI. [](../secgloss/p-gly.md) Diese Infrastruktur besteht aus den folgenden Teilen:

-   [Das Paar aus öffentlichem und privatem Schlüssel](#the-publicprivate-key-pair)
-   [Die Zertifikatanforderung](#the-certificate-request)
-   [Die Zertifizierungsstelle](#the-certification-authority)
-   [Das Zertifikat](#the-certificate-request)
-   [Die Zertifikatsperrliste](#the-certificate-revocation-list)
-   [Ihr öffentlicher Schlüssel, der für die Verschlüsselung verwendet wird](#your-public-key-used-for-encryption)
-   [Ihr öffentlicher Schlüssel, der für die Signaturüberprüfung verwendet wird](#your-public-key-used-for-signature-verification)
-   [Rolle "Microsoft-Zertifikatdienste"](#microsoft-certificate-services-role)

## <a name="the-publicprivate-key-pair"></a>Das Paar aus öffentlichem und privatem Schlüssel

PKI erfordert die Verwendung von [*Paaren aus öffentlichem und privatem Schlüssel.*](../secgloss/p-gly.md) Die Mathematik von Paaren aus öffentlichem und privatem Schlüssel geht über den Rahmen dieser Dokumentation hinaus, aber es ist wichtig, die funktionale Beziehung zwischen einem öffentlichen und einem privaten Schlüssel zu beachten. Kryptografische PKI-Algorithmen verwenden den öffentlichen Schlüssel des [*Empfängers*](../secgloss/c-gly.md) einer [](../secgloss/p-gly.md) verschlüsselten Nachricht zum Verschlüsseln von Daten sowie den zugehörigen privaten Schlüssel und nur den zugehörigen privaten Schlüssel, um die verschlüsselte Nachricht zu entschlüsseln. [](../secgloss/p-gly.md)

Ebenso wird eine [*digitale Signatur des*](../secgloss/d-gly.md) Inhalts, die weiter unten ausführlicher beschrieben wird, mit dem privaten Schlüssel des Signaturers erstellt. Der entsprechende öffentliche Schlüssel, der für alle verfügbar ist, wird verwendet, um diese Signatur zu überprüfen. Die Geheimnisse des privaten Schlüssels müssen beibehalten werden, da das Framework nach der Kompromittung des privaten Schlüssels getrennt wird.

Wenn genügend Zeit und Ressourcen vorhanden sind, kann ein Paar aus öffentlichem und privatem Schlüssel kompromittiert werden, d.&a; der private Schlüssel kann gefunden werden. Je länger der Schlüssel, desto schwieriger ist es, Brute-Force-Angriffe zum Aufschlüsseln des privaten Schlüssels zu verwenden. In der Praxis können ausreichend starke Schlüssel verwendet werden, um die rechtzeitige Bestimmung des privaten Schlüssels nicht möglich zu machen, wodurch die Public Key-Infrastruktur zu einem funktionierenden Sicherheitsmechanismus wird.

Ein privater Schlüssel kann im geschützten Format auf einem Datenträger gespeichert werden. In diesem Fall kann er nur mit diesem computer verwendet werden, es sei denn, er wird physisch auf einen anderen Computer verschoben. Eine Alternative ist ein Schlüssel auf einer Smartcard, der auf einem anderen Computer verwendet werden kann, vorausgesetzt, er verfügt über einen Smartcardleser und unterstützende Software.

Der öffentliche Schlüssel, aber nicht der private Schlüssel des Betreffs eines digitalen Zertifikats ist in der [*Zertifikatanforderung enthalten.*](../secgloss/c-gly.md) (Daher muss ein Paar aus öffentlichem und privatem Schlüssel vorhanden sein, bevor die Zertifikatanforderung gestellt wird.) Dieser öffentliche Schlüssel wird Teil des ausgestellten Zertifikats.

## <a name="the-certificate-request"></a>Die Zertifikatanforderung

Bevor ein Zertifikat ausgestellt wird, muss [*eine Zertifikatanforderung*](../secgloss/c-gly.md) generiert werden. Diese Anforderung gilt für eine Entität, z. B. einen Endbenutzer, einen Computer oder eine Anwendung. Gehen Sie zur Diskussion davon aus, dass die Entität sie selbst ist. Details zu Ihrer Identität sind in der Zertifikatanforderung enthalten. Nachdem die Anforderung generiert wurde, wird sie an eine [*Zertifizierungsstelle*](../secgloss/c-gly.md) übermittelt. Die Zertifizierungsstelle verwendet dann Ihre Identitätsinformationen, um zu bestimmen, ob die Anforderung die Kriterien der Zertifizierungsstelle für die Ausstellung eines Zertifikats erfüllt. Wenn die Zertifizierungsstelle die Anforderung genehmigt, stellt sie Ihnen als Entität in der Anforderung ein Zertifikat aus.

## <a name="the-certification-authority"></a>Die Zertifizierungsstelle

Vor der Ausstellung Ihres Zertifikats überprüft die Zertifizierungsstelle Ihre Identität. Wenn das Zertifikat ausgestellt wird, ist Ihre Identität an das Zertifikat gebunden, das Ihren öffentlichen Schlüssel enthält. Ihr Zertifikat enthält auch die digitale Signatur der Zertifizierungsstelle (die von jedem Benutzer überprüft werden kann, der Ihr Zertifikat erhält).

Da Ihr Zertifikat die Identität der ausstellenden Zertifizierungsstelle enthält, kann eine betroffene Partei, die dieser Zertifizierungsstelle vertraut, diese Vertrauensstellung auf Ihr Zertifikat ausdehnen. Die Ausstellung eines Zertifikats stellt keine Vertrauensstellung her, sondern überträgt die Vertrauensstellung. Wenn der Zertifikatverbraucher der ausstellenden Zertifizierungsstelle nicht vertraut, vertraut er Ihrem Zertifikat nicht (oder zumindest nicht).

Eine Kette signierter Zertifikate ermöglicht auch die Übertragung von Vertrauensstellungen an andere Zertifizierungsstelle. Dadurch können Parteien, die verschiedene Zertifizierungsstellen verwenden, weiterhin Zertifikate vertrauen (vorausgesetzt, es gibt eine gemeinsame Zertifizierungsstelle in der Kette, d. h. eine Zertifizierungsstelle, die von beiden Seiten als vertrauenswürdig eingestuft wird).

## <a name="the-certificate"></a>Das Zertifikat

Zusätzlich zu Ihrem öffentlichen Schlüssel und der Identität der ausstellenden Zertifizierungsstelle enthält das ausgestellte Zertifikat Informationen zu den Zwecken Ihres Schlüssels und Zertifikats. Darüber hinaus enthält sie den Pfad zur Liste der gesperrten Zertifikate der Zertifizierungsstelle und gibt die Gültigkeitsdauer des Zertifikats (Anfangs- und Enddatum) an.

Vorausgesetzt, der Zertifikatverbraucher vertraut der ausstellenden Zertifizierungsstelle für Ihr Zertifikat, muss der Zertifikatverbraucher ermitteln, ob das Zertifikat noch gültig ist, indem er das Anfangs- und Enddatum des Zertifikats mit der aktuellen Uhrzeit vergleicht und überprüft, ob ihr Zertifikat nicht in der Liste der gesperrten Zertifikate der Zertifizierungsstelle enthalten ist.

## <a name="the-certificate-revocation-list"></a>Die Zertifikatsperrliste

Wenn das Zertifikat in einem gültigen Zeitraum verwendet wird und der Zertifikatverbraucher der ausstellenden Zertifizierungsstelle vertraut, muss der Zertifikatverbraucher vor der Verwendung des Zertifikats noch eins überprüfen: die Zertifikatsperrliste (Certificate [*Revocation List,*](../secgloss/c-gly.md) CRL). Der Zertifikatverbraucher überprüft die Zertifikatsperrliste der Zertifizierungsstelle (der Pfad, der als Erweiterung in Ihrem Zertifikat enthalten ist), um sicherzustellen, dass Ihr Zertifikat nicht in der Liste der gesperrten Zertifikate enthalten ist. CrLs sind vorhanden, da ein Zertifikat manchmal nicht abgelaufen ist, aber nicht mehr als vertrauenswürdig eingestuft werden kann. Die Zertifizierungsstelle veröffentlicht in regelmäßigen Abständen eine aktualisierte Zertifikatsperrliste. Zertifikatverbraucher sind für den Vergleich von Zertifikaten mit der aktuellen Zertifikatsperrliste verantwortlich, bevor das Zertifikat als vertrauenswürdig eingestuft wird.

## <a name="your-public-key-used-for-encryption"></a>Ihr öffentlicher Schlüssel, der für die Verschlüsselung verwendet wird

Wenn ein Absender eine Nachricht verschlüsseln möchte, bevor sie an Sie gesendet wird, ruft der Absender zuerst Ihr Zertifikat ab. Nachdem der Absender festgestellt hat, dass die Zertifizierungsstelle vertrauenswürdig ist und Ihr Zertifikat gültig und nicht widerrufen wurde, verwendet [](../secgloss/p-gly.md) der Absender Ihren öffentlichen Schlüssel (recall it is part of the certificate) mit kryptografischen Algorithmen, um die Klartextnachricht in Chiffretext zu [*verschlüsseln.*](../secgloss/c-gly.md) Wenn Sie den Chiffretext erhalten, verwenden Sie Ihren privaten Schlüssel, um den Chiffretext zu entschlüsseln.

Wenn ein Drittanbieter die Verschlüsselungstext-E-Mail abfingt, kann der Drittanbieter sie ohne Zugriff auf Ihren privaten [*Schlüssel nicht entschlüsseln.*](../secgloss/p-gly.md)

Beachten Sie, dass der Großteil der hier aufgeführten Aktivitäten von Software und nicht direkt vom Benutzer verarbeitet wird.

## <a name="your-public-key-used-for-signature-verification"></a>Ihr öffentlicher Schlüssel, der für die Signaturüberprüfung verwendet wird

Eine [*digitale Signatur wird*](../secgloss/d-gly.md) als Bestätigung verwendet, dass eine Nachricht nicht geändert wurde, und als Bestätigung der Identität des Absenders der Nachricht. Diese digitale Signatur hängt von Ihrem privaten Schlüssel und dem Nachrichteninhalt ab. Mithilfe der Nachricht als Eingabe und Ihres privaten Schlüssels erstellen kryptografische Algorithmen die digitale Signatur. Der Inhalt der Nachricht wird durch den Signaturprozess nicht geändert. Ein Empfänger kann Ihren öffentlichen Schlüssel verwenden (nachdem er die Gültigkeit Ihres Zertifikats, die ausstellende Zertifizierungsstelle und den Sperrstatus überprüft hat), um zu bestimmen, ob die Signatur dem Nachrichteninhalt entspricht, und um zu bestimmen, ob die Nachricht von Ihnen gesendet wurde.

Wenn ein Drittanbieter die beabsichtigte Nachricht abfing, sie ändert (auch geringfügig), und die ursprüngliche Signatur an den Empfänger weiterspart, kann der Empfänger bei der Untersuchung der Nachricht und Signatur feststellen, dass die Nachricht verdächtig ist. Wenn ein Drittanbieter eine Nachricht erstellt und mit einer digitalen Signatur unter der Guise sendet, die er von Ihnen stammt, kann der Empfänger mitHilfe Ihres öffentlichen Schlüssels feststellen, dass die Nachricht und die Signatur nicht übereinstimmen.

[*Nichtabruf wird*](../secgloss/n-gly.md) auch von digitalen Signaturen unterstützt. Wenn der Absender einer signierten Nachricht das Senden der Nachricht verweigert, kann der Empfänger die Signatur verwenden, um diesen Anspruch zu widerlegen.

Beachten Sie, dass der Großteil der hier aufgeführten Aktivitäten auch von Software und nicht direkt vom Benutzer verarbeitet wird.

## <a name="microsoft-certificate-services-role"></a>Rolle "Microsoft-Zertifikatdienste"

Microsoft-Zertifikatdienste haben die Rolle, Zertifikate auszugeben oder Zertifikatanforderungen zu verweigern, wie von Richtlinienmodulen, die für die Sicherstellung der Identität des Zertifikat anfordernden Benutzers verantwortlich sind. Zertifikatdienste bieten auch die Möglichkeit, ein Zertifikat zu widerrufen und die Zertifikatsperrliste zu veröffentlichen. Zertifikatdienste können auch ausgestellte Zertifikate zentral verteilen (z. B. an einen Verzeichnisdienst). Die Möglichkeit, Zertifikate zusammen mit der Veröffentlichung von Zertifikatsperrlisten aus- und zu verteilen, zu widerrufen und zu verwalten, bietet die erforderlichen Funktionen für die Public Key-Infrastruktur.

 

 
