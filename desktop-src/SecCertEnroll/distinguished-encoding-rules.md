---
description: Abstract Syntax Notation One (ASN. 1) definiert die folgenden Regelsätze, die bestimmen, wie Datenstrukturen, die zwischen Computern gesendet werden, codiert und decodiert werden.
ms.assetid: 47735fa1-9d75-4c6b-b14c-6c7483f43a5d
title: Distinguished Encoding Rules
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6e12429c7c2185fc4910abd00e4641e7cd9d2f2f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104527002"
---
# <a name="distinguished-encoding-rules"></a>Distinguished Encoding Rules

Abstract Syntax Notation One (ASN. 1) definiert die folgenden Regelsätze, die bestimmen, wie Datenstrukturen, die zwischen Computern gesendet werden, codiert und decodiert werden.

-   Grundlegende Codierungsregeln (ber)
-   Kanonische Codierungsregeln (CER)
-   Distinguished Encoding Rules (der)
-   Gepackte Codierungsregeln (pro)

Der ursprüngliche Regelsatz wurde von der ber-Spezifikation definiert. CER und der wurden später als spezialisierte Teilmengen von ber entwickelt. Pro wurde als Reaktion auf Kritik in Bezug auf die Menge an Bandbreite entwickelt, die zum Übertragen von Daten mit ber oder den zugehörigen Varianten erforderlich ist Pro bietet erhebliche Einsparungen.

Der wurde erstellt, um die Anforderungen der X. 509-Spezifikation für die sichere Datenübertragung zu erfüllen. Von der Zertifikatregistrierungs-API wird der exklusiv verwendet. Weitere Informationen finden Sie in den nachfolgenden Themen.

-   [DER-Übertragungs Syntax](about-der-transfer-syntax.md)
-   [Der-Codierung von ASN. 1-Typen](about-der-encoding-of-asn-1-types.md)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[ASN. 1-Typsystem](about-asn-1-type-system.md)
</dt> <dt>

[Zertifikat Anforderungs Codierung](about-certificate-request-encoding.md)
</dt> <dt>

[Einführung in die ASN. 1-Syntax und-Codierung](about-introduction-to-asn-1-syntax-and-encoding.md)
</dt> </dl>

 

 



