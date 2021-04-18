---
description: Anwendungen, die digitale XML-Signaturen signieren und überprüfen, sollten gemäß den folgenden bewährten Methoden geschrieben werden, um Denial-of-Service-Angriffe, Datenverlust und Gefährdung privater Informationen zu vermeiden.
ms.assetid: aa972946-9860-49c1-ae94-3f315684c291
title: Sicherheitsüberlegungen zur XML-digitalen Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4e54b4c5f3f863e0bc84172a7507bfe8609e2df7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106351424"
---
# <a name="xml-digital-signature-security-considerations"></a>Sicherheitsüberlegungen zur XML-digitalen Signatur

Anwendungen, die digitale XML-Signaturen signieren und überprüfen, sollten gemäß den folgenden bewährten Methoden geschrieben werden, um Denial-of-Service-Angriffe, Datenverlust und Gefährdung privater Informationen zu vermeiden. Die nachstehende Liste enthält allgemeine Anleitungen. Entwicklern wird jedoch empfohlen, für Ihre Anwendungen eine zusätzliche Sicherheitsanalyse durchzuführen und die neuesten bewährten Methoden für digitale Signaturen zu überprüfen.

-   [Überprüfen der Vertrauenswürdigkeit des Signatur Schlüssels](#verify-trust-of-the-signing-key)
-   [Überprüfen Sie zuerst den Signatur Schlüssel, und überprüfen Sie signetdinfo und dann Verweise überprüfen](#first-verify-the-signing-key-and-validate-signedinfo-then-validate-references)
-   [Verwenden Sie den minimalen Satz von Kanonisierungsalgorithmen und-Transformationen, die erforderlich sind](#use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required)
-   [Sicherstellen, dass die Ziel-URIs auf Ziele innerhalb des erwarteten Bereichs verweisen](#ensure-target-uris-point-to-destinations-within-the-expected-scope)
-   [Überprüfen Sie, ob die von der Anwendung genutzten Daten von der Signatur überprüft werden.](#verify-the-data-consumed-by-the-application-is-verified-by-the-signature)
-   [Befolgen Sie die besten kryptografiepraktiken](#follow-best-cryptographic-practices)

## <a name="verify-trust-of-the-signing-key"></a>Überprüfen der Vertrauenswürdigkeit des Signatur Schlüssels

Stellen Sie sicher, dass der Signatur Schlüssel vertrauenswürdig ist, indem Sie das entsprechende [*X. 509*](../secgloss/x-gly.md) -Zertifikat (und die in der signierten Nachricht enthaltene Zertifikat Kette) überprüfen Alternativ kann die Vertrauensstellung im Signatur Schlüssel auf Out-of-Band-Weise eingerichtet werden, z. b. ein Administrator, der einen Satz vertrauenswürdiger Schlüssel konfiguriert, oder eine Anwendung, die einen vertrauenswürdigen Dienst über einen sicheren Kanal abfragt.

## <a name="first-verify-the-signing-key-and-validate-signedinfo-then-validate-references"></a>Überprüfen Sie zuerst den Signatur Schlüssel, und überprüfen Sie signetdinfo und dann Verweise überprüfen

Überprüfen Sie die Vertrauenswürdigkeit im Signatur Schlüssel und die Integrität des **signetdinfo** -Elements vor der Überprüfung von verweisen. Analog dazu sollten-Anwendungen manifeselemente validieren, bevor Sie **die in** den manifeselementen enthaltenen Verweise auflösen  **Verweis** Elemente ermöglichen die Angabe von Ziel-URIs, Transformationen und Kanonisierungsalgorithmen. Wenn Sie nicht überprüft werden, können diese Felder möglicherweise verwendet werden, um Denial-of-Service-Angriffe, Datenverluste oder andere Angriffe zu erzeugen.

## <a name="use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required"></a>Verwenden Sie den minimalen Satz von Kanonisierungsalgorithmen und-Transformationen, die erforderlich sind

XSLT und XPath sollten nicht in nicht authentifizierten Elementen, z. b. **KeyInfo**, verwendet werden. Wenn eine Anwendung die Verwendung von XPath erfordert, schränken Sie den Satz von XPath-Ausdrücken ein, die nur für die zulässig sind, die die Vorgänger-oder Self-Achsen verwenden, und berechnen Sie den Zeichen folgen Wert von Elementen nicht. Standardmäßig unterstützt cryptxml einen begrenzten Satz von Kanonisierungsalgorithmen (Weitere Informationen finden Sie unter Unterstützte URIs in [kryptografischen XML-Signatur Algorithmen](xml-digital-signature-cryptographic-algorithms.md)). Entwickler können zusätzliche Transformationen oder Kanonisierungsalgorithmen zur Verwendung in Ihrer Anwendung implementieren. Die Verwendung komplexer Algorithmen birgt jedoch die Möglichkeit von Denial-of-Service-Angriffen oder durch das Unterbrechen der Ablehnungs Merkmale einer Signatur. In Fällen, in denen Transformationen von der Anwendung benötigt werden, begrenzen Sie die Anzahl der Transformationen, die pro Verweis auf die höchste von der Anwendung benötigte Anzahl festgelegt werden können. Diese Vorgehensweise mindert Denial-of-Service-Angriffe auf der Grundlage der übermäßigen Verwendung von Transformationen.

## <a name="ensure-target-uris-point-to-destinations-within-the-expected-scope"></a>Sicherstellen, dass die Ziel-URIs auf Ziele innerhalb des erwarteten Bereichs verweisen

Anwendungen sollten die Ziel-URIs auf den kleinsten von der Anwendung benötigten Bereich beschränken. Beispielsweise kann es sein, dass URIs auf Ziele innerhalb desselben Dokuments, auf Dateien in einem bestimmten Zielverzeichnis oder an Netzwerkadressen innerhalb einer bestimmten DNS-Domäne verweisen. URIs, die von einem Angreifer so festgelegt werden, dass er außerhalb der erwarteten Domäne steht, können dazu führen, dass eine Anwendung schädlichen Inhalt abruft, böswillige HTTP-Anforderungen (möglicherweise mit Abfrage Zeichenfolgen) sendet oder Anwendungen für schädliche Server authentifiziert.

## <a name="verify-the-data-consumed-by-the-application-is-verified-by-the-signature"></a>Überprüfen Sie, ob die von der Anwendung genutzten Daten von der Signatur überprüft werden.

Wenn die Anwendung den Signatur Schlüssel und die **signetdinfo** -und **Verweis** Elemente überprüft, die Anwendung jedoch wichtige Daten verbraucht, auf die nicht von der Signatur verwiesen wird, bietet die Signatur keinen sinnvollen Schutz. Die semantische Bedeutung einer Signatur kann abhängig von der Position der Signatur innerhalb des Dokuments variieren. Anwendungen wird empfohlen, die Position der Signatur innerhalb eines Dokuments zu überprüfen. Überprüfen Sie außerdem die Position der referenzierten Daten und Elementnamen, um Ersetzung und Wrapping Angriffe zu vermeiden.

## <a name="follow-best-cryptographic-practices"></a>Befolgen Sie die besten kryptografiepraktiken

Kryptografiealgorithmen werden im Laufe der Zeit schwächer, wenn neue Angriffe erkannt werden und mehr Rechenleistung verfügbar ist. Verwenden Sie keine hart Codierung für kryptografiealgorithmusbezeichner oder Schlüsselgrößen in Ihren Anwendungen. Eine ausführlichere Liste der besten kryptografiepraktiken finden Sie unter Michael Howard und Steve Lipner, "SDL-mindestkryptografiestandards" im *Security Development Lifecycle* (Redmond, Washington: Microsoft Press, 2006), 251 – 258.

Weitere bewährte Methoden finden Sie auf der W3C-Website: https://www.w3.org .

> [!Note]  
> Diese Ressourcen sind möglicherweise in einigen Sprachen und Ländern oder Regionen nicht verfügbar.

 

 

 
