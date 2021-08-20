---
description: Anwendungen, die digitale XML-Signaturen signieren und überprüfen, sollten gemäß den folgenden bewährten Methoden geschrieben werden, um Denial-of-Service-Angriffe, Datenverlust und Kompromittieren privater Informationen zu vermeiden.
ms.assetid: aa972946-9860-49c1-ae94-3f315684c291
title: Sicherheitsüberlegungen zur digitalen XML-Signatur
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f4c66304d454d97a5583aab8458d98fd2a38208ff7b302a9139747787d10eda
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "117970444"
---
# <a name="xml-digital-signature-security-considerations"></a>Sicherheitsüberlegungen zur digitalen XML-Signatur

Anwendungen, die digitale XML-Signaturen signieren und überprüfen, sollten gemäß den folgenden bewährten Methoden geschrieben werden, um Denial-of-Service-Angriffe, Datenverlust und Kompromittieren privater Informationen zu vermeiden. Die folgende Liste enthält allgemeine Anleitungen. Entwicklern wird jedoch empfohlen, zusätzliche Sicherheitsanalysen für ihre Anwendungen durchzuführen und die neuesten bewährten Methoden für digitale Signaturen zu überprüfen, die vom W3C veröffentlicht werden.

-   [Überprüfen der Vertrauensstellung des Signaturschlüssels](#verify-trust-of-the-signing-key)
-   [Überprüfen Sie zunächst den Signaturschlüssel, und überprüfen Sie SignedInfo, und überprüfen Sie dann verweise.](#first-verify-the-signing-key-and-validate-signedinfo-then-validate-references)
-   [Verwenden Sie den minimalen Satz von kanonischen Algorithmen und Transformationen, die erforderlich sind.](#use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required)
-   [Sicherstellen, dass Ziel-URIs auf Ziele innerhalb des erwarteten Bereichs verweisen](#ensure-target-uris-point-to-destinations-within-the-expected-scope)
-   [Überprüfen Sie, ob die von der Anwendung genutzten Daten durch die Signatur überprüft werden.](#verify-the-data-consumed-by-the-application-is-verified-by-the-signature)
-   [Befolgen sie die bewährten kryptografischen Methoden.](#follow-best-cryptographic-practices)

## <a name="verify-trust-of-the-signing-key"></a>Überprüfen der Vertrauensstellung des Signaturschlüssels

Stellen Sie sicher, dass der Signaturschlüssel vertrauenswürdig ist, indem Sie das entsprechende [*X.509-Zertifikat*](../secgloss/x-gly.md) (und die Zertifikatkette) überprüfen, das in der signierten Nachricht enthalten ist. Alternativ kann die Vertrauensstellung mit dem Signaturschlüssel out-of-band eingerichtet werden, z. B. ein Administrator, der einen Satz vertrauenswürdiger Schlüssel konfiguriert, oder eine Anwendung, die einen vertrauenswürdigen Dienst über einen sicheren Kanal abfragt.

## <a name="first-verify-the-signing-key-and-validate-signedinfo-then-validate-references"></a>Überprüfen Sie zunächst den Signaturschlüssel, und überprüfen Sie SignedInfo, und überprüfen Sie dann verweise.

Überprüfen Sie die Vertrauenswürdigkeit des Signaturschlüssels und die Integrität des **SignedInfo-Elements,** bevor Sie Verweise überprüfen. Auf ähnliche Weise sollten Anwendungen **Manifestelemente** überprüfen, bevor verweise in den **Manifest-Elementen** aufgelöst werden. **Verweiselemente** ermöglichen die Angabe von Ziel-URIs, Transformationen und Kanonisierungsalgorithmen. Wenn sie nicht überprüft werden, können diese Felder möglicherweise verwendet werden, um Denial-of-Service-Angriffe, Datenverluste oder andere Angriffe zu erstellen.

## <a name="use-the-minimal-set-of-canonicalization-algorithms-and-transforms-required"></a>Verwenden Sie den minimalen Satz von kanonischen Algorithmen und Transformationen, die erforderlich sind.

XSLT und XPATH sollten nicht in nicht authentifizierten Elementen wie **KeyInfo** verwendet werden. Wenn eine Anwendung die Verwendung von XPath erfordert, beschränken Sie den Satz von XPATH-Ausdrücken auf diejenigen, die die Vorgänger- oder Selbstachse verwenden, und berechnen Sie nicht den Zeichenfolgenwert von Elementen. Standardmäßig unterstützt CryptXML einen begrenzten Satz von Kanonisierungsalgorithmen (siehe unterstützte URIs in [kryptografischen ALGORITHMEN für digitale XML-Signaturen).](xml-digital-signature-cryptographic-algorithms.md) Entwickler können zusätzliche Transformationen oder Kanonisierungsalgorithmen für die Verwendung in ihrer Anwendung implementieren. Die Verwendung komplexer Algorithmen bietet jedoch die Möglichkeit von Denial-of-Service-Angriffen oder dem Abbrechen der Aberkennungsmerkmale einer Signatur. In Fällen, in denen Transformationen für die Anwendung erforderlich sind, beschränken Sie die Anzahl der Transformationen, die pro Verweis angegeben werden können, auf die höchste Anzahl, die von der Anwendung benötigt wird. Diese Vorgehensweise verringert Denial-of-Service-Angriffe, die auf übermäßiger Nutzung von Transformationen basieren.

## <a name="ensure-target-uris-point-to-destinations-within-the-expected-scope"></a>Sicherstellen, dass Ziel-URIs auf Ziele innerhalb des erwarteten Bereichs verweisen

Anwendungen sollten die Ziel-URIs auf den kleinsten bereich beschränken, der von der Anwendung benötigt wird. Es kann beispielsweise erwartet werden, dass URIs auf Ziele innerhalb desselben Dokuments, Dateien in einem bestimmten Zielverzeichnis oder Netzwerkadressen innerhalb einer bestimmten DNS-Domäne verweisen. URIs, die von einem Angreifer so festgelegt werden, dass sie außerhalb der erwarteten Domäne zeigen, können dazu führen, dass eine Anwendung schädliche Inhalte abruft, schädliche HTTP-Anforderungen sendet (möglicherweise Abfragezeichenfolgen enthält) oder anwendungen zur Authentifizierung bei schädlichen Servern veranlassen.

## <a name="verify-the-data-consumed-by-the-application-is-verified-by-the-signature"></a>Überprüfen Sie, ob die von der Anwendung genutzten Daten durch die Signatur überprüft werden.

Wenn die Anwendung den Signaturschlüssel und die **SignedInfo-** und **Reference-Elemente** überprüft, die Anwendung jedoch wichtige Daten nutzt, auf die nicht von der Signatur verwiesen wird, bietet die Signatur keinen sinnvollen Schutz. Die semantische Bedeutung einer Signatur kann je nach Position der Signatur im Dokument variieren. Anwendungen wird empfohlen, die Position der Signatur in einem Dokument zu überprüfen. Überprüfen Sie außerdem die Position der Daten- und Elementnamen, auf die verwiesen wird, um Ersetzungs- und Umbruchangriffe zu minimieren.

## <a name="follow-best-cryptographic-practices"></a>Befolgen sie die bewährten kryptografischen Methoden.

Kryptografische Algorithmen werden mit der Zeit schwächer, wenn neue Angriffe erkannt werden und mehr Rechenleistung verfügbar wird. Programmieren Sie kryptografische Algorithmusbezeichner oder Schlüsselgrößen nicht hart in Ihre Anwendungen. Eine ausführlichere Liste der bewährten kryptografischen Methoden finden Sie unter Michael Plc und Steve Lipner, "SDL Minimum Cryptographic Standards", in *The Security Development Lifecycle* (Redmond, Washington: Microsoft Press, 2006), 251–258.

Weitere bewährte Methoden finden Sie auf der W3C-Website: https://www.w3.org .

> [!Note]  
> Diese Ressourcen sind in einigen Sprachen und Ländern oder Regionen möglicherweise nicht verfügbar.

 

 

 
