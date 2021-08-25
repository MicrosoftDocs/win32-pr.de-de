---
description: Abstrakte Syntax notation One (ASN.1) definiert die folgenden Regelsätze, die steuern, wie Datenstrukturen, die zwischen Computern gesendet werden, codiert und decodiert werden.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: Distinguished Encoding Rules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f4d592fdfbb2532f5c718aadaaf32e63f352ed6ab427e9908465fcb5998839f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119883070"
---
# <a name="distinguished-encoding-rules"></a>Distinguished Encoding Rules

Abstrakte Syntax notation One (ASN.1) definiert die folgenden Regelsätze, die steuern, wie Datenstrukturen, die zwischen Computern gesendet werden, codiert und decodiert werden.

-   Grundlegende Codierungsregeln (BER)
-   Kanonische Codierungsregeln (CER)
-   Distinguished Encoding Rules (DER)
-   Gepackte Codierungsregeln (PER)

Der ursprüngliche Regelsatz wurde durch die BER-Spezifikation definiert. CER und DER wurden später als spezialisierte Teilmengen von BER entwickelt. PER wurde als Reaktion auf Die Menge an Bandbreite entwickelt, die zum Übertragen von Daten mit BER oder seinen Varianten erforderlich ist. PER bietet erhebliche Einsparungen.

DER wurde erstellt, um die Anforderungen der X.509-Spezifikation für die sichere Datenübertragung zu erfüllen. Die Zertifikatregistrierungs-API verwendet DER ausschließlich. Weitere Informationen finden Sie in den folgenden Themen.

-   [DER-Übertragungssyntax](about-der-transfer-syntax.md)
-   [DER-Codierung von ASN.1-Typen](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN.1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Zertifikatanforderungscodierung](about-certificate-request-encoding.md)
</dt> <dt>

[Einführung in die ASN.1-Syntax und -Codierung](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



