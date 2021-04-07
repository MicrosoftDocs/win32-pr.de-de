---
description: Bei den Zertifikat Diensten handelt es sich um eine Grundlage für die Public Key-Infrastruktur (PKI), die das Mittel zum schützen und Authentifizieren von Informationen bietet.
ms.assetid: c18f46ca-e805-4b33-8014-79dc34c18531
title: Zertifikate und öffentliche Schlüssel
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 07e01993673fe16c8401368ffaa7e8815c450dd5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103863339"
---
# <a name="certificates-and-public-keys"></a>Zertifikate und öffentliche Schlüssel

Bei den Zertifikat Diensten handelt es sich um eine Grundlage für die Public Key-Infrastruktur (PKI), die das Mittel zum schützen und Authentifizieren von Informationen bietet. Die Beziehung zwischen einem Zertifikat Inhaber, der Identität des Zertifikat Inhabers und dem [*öffentlichen Schlüssel*](../secgloss/p-gly.md) des Zertifikat Inhabers ist ein wichtiger Bestandteil der PKI. Diese Infrastruktur besteht aus den folgenden Teilen:

-   [Das Paar aus öffentlichem und privatem Schlüssel](#the-publicprivate-key-pair)
-   [Die Zertifikat Anforderung](#the-certificate-request)
-   [Die Zertifizierungsstelle](#the-certification-authority)
-   [Das Zertifikat](#the-certificate-request)
-   [Die Zertifikat Sperr Liste.](#the-certificate-revocation-list)
-   [Der öffentliche Schlüssel, der für die Verschlüsselung verwendet wird](#your-public-key-used-for-encryption)
-   [Der öffentliche Schlüssel, der für die Signatur Überprüfung verwendet wird.](#your-public-key-used-for-signature-verification)
-   [Rolle "Microsoft-Zertifikat Dienste"](#microsoft-certificate-services-role)

## <a name="the-publicprivate-key-pair"></a>Das Paar aus öffentlichem und privatem Schlüssel

PKI erfordert die Verwendung von [*öffentlichen/privaten Schlüsselpaaren*](../secgloss/p-gly.md). Die Mathematik aus öffentlichen/privaten Schlüsselpaaren geht über den Rahmen dieser Dokumentation hinaus, aber es ist wichtig, die funktionale Beziehung zwischen einem öffentlichen und einem privaten Schlüssel zu beachten. PKI- [*Kryptografiealgorithmen*](../secgloss/c-gly.md) verwenden den [*öffentlichen Schlüssel*](../secgloss/p-gly.md) des Empfängers einer verschlüsselten Nachricht, um Daten zu verschlüsseln, und den zugehörigen [*privaten Schlüssel*](../secgloss/p-gly.md) und nur den zugehörigen privaten Schlüssel, um die verschlüsselte Nachricht zu entschlüsseln.

Analog dazu wird eine [*digitale Signatur*](../secgloss/d-gly.md) des Inhalts, die in größerem Umfang ausführlicher beschrieben wird, mit dem privaten Schlüssel des Signatur Gebers erstellt. Der entsprechende öffentliche Schlüssel, der allen Benutzern zur Verfügung steht, wird verwendet, um diese Signatur zu überprüfen. Die Geheimnisse des privaten Schlüssels müssen beibehalten werden, da das Framework entfernt wird, nachdem der private Schlüssel kompromittiert wurde.

Wenn Sie genügend Zeit und Ressourcen haben, kann ein paar aus öffentlichem und privatem Schlüssel kompromittiert werden, d. h., der private Schlüssel kann ermittelt werden. Desto schwieriger ist es, Brute-Force zu verwenden, um den privaten Schlüssel zu ermitteln. In der Praxis können ausreichend starke Schlüssel verwendet werden, damit der private Schlüssel nicht rechtzeitig ermittelt werden kann, sodass die Public Key-Infrastruktur zu einem funktionierenden Sicherheitsmechanismus wird.

Ein privater Schlüssel kann im geschützten Format auf einem Datenträger gespeichert werden. in diesem Fall kann er nur mit diesem Computer verwendet werden, es sei denn, er wird physisch auf einen anderen Computer verschoben. Eine Alternative besteht darin, einen Schlüssel auf einer Smartcard zu verwenden, der auf einem anderen Computer verwendet werden kann, sofern er über einen Smartcardleser und unterstützende Software verfügt.

Der öffentliche Schlüssel, jedoch nicht der private Schlüssel des Subjekts eines digitalen Zertifikats, ist als Teil der [*Zertifikat Anforderung*](../secgloss/c-gly.md)enthalten. (Aus diesem Grund muss ein öffentliches/privates Schlüsselpaar vorhanden sein, bevor die Zertifikat Anforderung angefordert wird.) Der öffentliche Schlüssel wird Teil des ausgestellten Zertifikats.

## <a name="the-certificate-request"></a>Die Zertifikat Anforderung

Bevor ein Zertifikat ausgestellt wird, muss eine [*Zertifikat Anforderung*](../secgloss/c-gly.md) generiert werden. Diese Anforderung gilt für eine Entität, z. b. für einen Endbenutzer, einen Computer oder eine Anwendung. Gehen Sie zur Diskussion davon aus, dass die Entität selbst ist. Details Ihrer Identität sind in der Zertifikat Anforderung enthalten. Nachdem die Anforderung generiert wurde, wird Sie an eine Zertifizierungsstelle ( [*Certification Authority*](../secgloss/c-gly.md) , ca) übermittelt. Die Zertifizierungsstelle verwendet dann Ihre Identitätsinformationen, um zu bestimmen, ob die Anforderung die Kriterien der Zertifizierungsstelle zum Ausstellen eines Zertifikats erfüllt. Wenn die Zertifizierungsstelle die Anforderung genehmigt, gibt Sie ein Zertifikat als die in der Anforderung benannte Entität aus.

## <a name="the-certification-authority"></a>Die Zertifizierungsstelle

Vor der Ausgabe Ihres Zertifikats überprüft die Zertifizierungsstelle Ihre Identität. Wenn das Zertifikat ausgestellt wird, wird Ihre Identität an das Zertifikat gebunden, das Ihren öffentlichen Schlüssel enthält. Ihr Zertifikat enthält auch die digitale Signatur der Zertifizierungsstelle (die von jedem Benutzer, der Ihr Zertifikat empfängt, überprüft werden kann).

Da Ihr Zertifikat die Identität der ausstellenden Zertifizierungsstelle enthält, kann eine interessierte Partei, die dieser Zertifizierungsstelle vertraut, diese Vertrauensstellung auf Ihr Zertifikat ausweiten. Die Ausstellung eines Zertifikats stellt keine Vertrauensstellung her, sondern überträgt die Vertrauensstellung. Wenn der zertifikatconsumer der ausstellenden Zertifizierungsstelle nicht vertraut, wird das Zertifikat nicht (oder zumindest nicht) als vertrauenswürdig eingestuft.

Eine Kette signierter Zertifikate ermöglicht auch das Übertragen von Vertrauens Stellungen an andere Zertifizierungsstellen. Dadurch können Parteien, die unterschiedliche Zertifizierungsstellen verwenden, weiterhin Zertifikate Vertrauen (vorausgesetzt, es gibt eine gemeinsame Zertifizierungsstelle in der Kette, d. h. eine Zertifizierungsstelle, die von beiden Parteien als vertrauenswürdig eingestuft wird).

## <a name="the-certificate"></a>Das Zertifikat

Zusätzlich zu Ihrem öffentlichen Schlüssel und der Identität der ausstellenden Zertifizierungsstelle enthält das ausgegebene Zertifikat Informationen zu den Zwecken Ihres Schlüssels und Zertifikats. Außerdem enthält Sie den Pfad zur Liste der gesperrten Zertifikate der Zertifizierungsstelle und gibt die Gültigkeitsdauer des Zertifikats an (Anfangs-und Enddatum).

Wenn der zertifikatconsumer der ausstellenden Zertifizierungsstelle das Zertifikat vertraut, muss der zertifikatconsumer feststellen, ob das Zertifikat noch gültig ist, indem es die Anfangs-und Enddatum des Zertifikats mit der aktuellen Uhrzeit vergleicht und sicherstellt, dass Ihr Zertifikat nicht in der Liste der von der Zertifizierungsstelle gesperrten Zertifikate enthalten ist.

## <a name="the-certificate-revocation-list"></a>Die Zertifikat Sperr Liste.

Vorausgesetzt, dass das Zertifikat in einem gültigen Zeitraum verwendet wird und der zertifikatconsumer der ausstellenden Zertifizierungsstelle vertraut, gibt es noch ein Element, das der Zertifikat Consumer vor der Verwendung des Zertifikats überprüfen muss: die [*Zertifikat Sperr Liste*](../secgloss/c-gly.md) (CRL). Der zertifikatconsumer überprüft die CRL der Zertifizierungsstelle (der Pfad, der als Erweiterung in Ihrem Zertifikat enthalten ist), um sicherzustellen, dass Ihr Zertifikat nicht in der Liste der gesperrten Zertifikate enthalten ist. CRLs sind vorhanden, da ein Zertifikat nicht abgelaufen ist, aber nicht mehr als vertrauenswürdig eingestuft werden kann. Von der Zertifizierungsstelle wird in regelmäßigen Abständen eine aktualisierte CRL veröffentlicht. Zertifikatconsumer sind für den Vergleich von Zertifikaten mit der aktuellen CRL zuständig, bevor Sie das vertrauenswürdige Zertifikat berücksichtigen.

## <a name="your-public-key-used-for-encryption"></a>Der öffentliche Schlüssel, der für die Verschlüsselung verwendet wird

Wenn ein Absender eine Nachricht verschlüsseln möchte, bevor Sie Sie an Sie senden, ruft der Absender zuerst das Zertifikat ab. Nachdem der Absender festgestellt hat, dass die Zertifizierungsstelle vertrauenswürdig ist und das Zertifikat gültig und nicht widerrufen ist, verwendet der Absender ihren öffentlichen Schlüssel (Rückruf ist Teil des Zertifikats) mit Kryptografiealgorithmen, um die [*Klartext*](../secgloss/p-gly.md) -Nachricht in [*Chiffre Text*](../secgloss/c-gly.md)zu verschlüsseln. Wenn Sie den Chiffre Text erhalten, verwenden Sie den privaten Schlüssel, um den Chiffre Text zu entschlüsseln.

Wenn eine dritte Partei die Chiffre Text-e-Mail-Nachricht abfängt, kann Sie nicht ohne Zugriff auf Ihren [*privaten Schlüssel*](../secgloss/p-gly.md)entschlüsselt werden.

Beachten Sie, dass der größte Teil der hier aufgeführten Aktivitäten von Software, nicht direkt vom Benutzer verarbeitet wird.

## <a name="your-public-key-used-for-signature-verification"></a>Der öffentliche Schlüssel, der für die Signatur Überprüfung verwendet wird.

Eine [*digitale Signatur*](../secgloss/d-gly.md) wird als Bestätigung verwendet, dass eine Nachricht nicht geändert wurde, und als Bestätigung der Identität des Absenders der Nachricht. Diese digitale Signatur ist abhängig von Ihrem privaten Schlüssel und dem Nachrichten Inhalt. Mithilfe der Nachricht als Eingabe und Ihres privaten Schlüssels erstellen Kryptografiealgorithmen die digitale Signatur. Der Inhalt der Nachricht wird vom Signatur Prozess nicht geändert. Ein Empfänger kann Ihren öffentlichen Schlüssel (nach dem Überprüfen der Gültigkeit des Zertifikats, der ausstellenden Zertifizierungsstelle und des Sperr Status) verwenden, um zu bestimmen, ob die Signatur dem Nachrichten Inhalt entspricht, und um festzustellen, ob die Nachricht von Ihnen gesendet wurde.

Wenn die beabsichtigte Nachricht von einem Drittanbieter abgefangen, geändert (sogar etwas) und die ursprüngliche Signatur an den Empfänger weitergeleitet wird, kann der Empfänger nach der Untersuchung der Nachricht und der Signatur ermitteln, ob die Nachricht Fehler verdächtig ist. Wenn eine dritte Person eine Nachricht erstellt und Sie mit einer gefälschten, digitalen Signatur unter dem von Ihnen stammenden Zeichen sendet, kann der Empfänger den öffentlichen Schlüssel verwenden, um zu bestimmen, ob die Nachricht und die Signatur einander nicht entsprechen.

[](../secgloss/n-gly.md) Die Nichtabstreitbarkeit wird auch von digitalen Signaturen unterstützt. Wenn der Absender einer signierten Nachricht das Senden der Nachricht ablehnt, kann der Empfänger die Signatur verwenden, um diesen Anspruch zu widerlegen.

Beachten Sie, dass der größte Teil der hier aufgeführten Aktivitäten auch von Software behandelt wird, nicht direkt vom Benutzer.

## <a name="microsoft-certificate-services-role"></a>Rolle "Microsoft-Zertifikat Dienste"

Die Microsoft-Zertifikat Dienste haben die Rolle, Zertifikate auszugeben oder Anforderungen für Zertifikate zu verweigern, die von Richtlinien Modulen gesteuert werden, die für die Sicherstellung der Identität der Zertifikatanforderer zuständig sind. Zertifikat Dienste bieten außerdem die Möglichkeit, ein Zertifikat zu widerrufen und die CRL zu veröffentlichen. Zertifikat Dienste können auch zentral (z. b. an einen Verzeichnisdienst) ausgestellte Zertifikate verteilen. Die Möglichkeit, Zertifikate zusammen mit der Veröffentlichung von CRLs auszugeben, zu verteilen, zu widerrufen und zu verwalten, stellt die erforderlichen Funktionen für die Public Key-Infrastruktur bereit.

 

 
