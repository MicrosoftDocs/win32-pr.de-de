---
description: Das Tagfeld in einem TLV-Triplet identifiziert den Typ der Datenstruktur, die zwischen Computern gesendet wird.
ms.assetid: 4723cc02-8c48-488e-95b8-c646a99b6aab
title: Codierte Tagbytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27face1fe04cf52c79d6c4047f87f58e98f2bc1a7b7656109341c9ce2be59d0b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904322"
---
# <a name="encoded-tag-bytes"></a>Codierte Tagbytes

Das *Tagfeld* in einem TLV-Triplet identifiziert den Typ der Datenstruktur, die zwischen Computern gesendet wird. Beispielsweise ist das Tag für eine ganze Zahl 0x02, und das Tag für einen Objektbezeichner ist 0x06. Obwohl mehrere Bytes zulässig sind, erfordert keiner der von der Zertifikatregistrierungs-API verwendeten Datentypen mehr als einen. Die folgende Abbildung zeigt  die Aufschlüsselung eines Tagwerts. Die Bits 7 und 6 identifizieren die ASN.1-Taggingklasse. Es gibt vier verfügbare Klassen, aber die Zertifikatregistrierungs-API verwendet Datentypen, die nur zur UNIVERSAL-Klasse gehören. Bit 5 gibt an, ob das Codierungsformular primitiv oder konstruiert ist. Basis- und Zeichenfolgentypen werden mithilfe primitiver Formulare codiert, konstruierte Typen mithilfe eines konstruierten Formulars. Weitere Informationen finden Sie unter [ASN.1-Typsystem.](about-asn-1-type-system.md) Die Bits 4 bis 0 enthalten die Tagnummer.

![der tlv tag byte](images/der-tlv-tagbyte.png)

In der folgenden Tabelle sind die von der Zertifikatregistrierungs-API unterstützten Datentypen, das verwendete Codierungsformular und der Tagwert aufgeführt.

| type              | ASN.1-Klasse | Codierungsformular | Tagwert                             |
|-------------------|-------------|---------------|---------------------------------------|
| BIT STRING        | Universal   | Primitiv     | 00000011<br/> (0x03)<br/> |
| BOOLEAN           | Universal   | Primitiv     | 00000001<br/> (0x01)<br/> |
| INTEGER           | Universal   | Primitiv     | 00000010<br/> (0x02)<br/> |
| NULL              | Universal   | Primitiv     | 00000101<br/> (0x05)<br/> |
| OBJEKTBEZEICHNER | Universal   | Primitiv     | 00000110<br/> (0x06)<br/> |
| OKTETTZEICHENFOLGE      | Universal   | Primitiv     | 00000100<br/> (0x04)<br/> |
| BMPString         | Universal   | Primitiv     | 00011110<br/> (0x1E)<br/> |
| IA5String         | Universal   | Primitiv     | 00010110<br/> (0x16)<br/> |
| PrintableString   | Universal   | Primitiv     | 00010011<br/> (0x13)<br/> |
| TeletexString     | Universal   | Primitiv     | 00010100<br/> (0x14)<br/> |
| UTF8String        | Universal   | Primitiv     | 00001100<br/> (0x0C)<br/> |
| SEQUENCE          | Universal   | Konstruiert   | 00110000<br/> (0x30)<br/> |
| SEQUENZ VON       | Universal   | Konstruiert   | 00110000<br/> (0x30)<br/> |
| SET               | Universal   | Konstruiert   | 00110001<br/> (0x31)<br/> |
| SET OF            | Universal   | Konstruiert   | 00110001<br/> (0x31)<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DER-Übertragungssyntax](about-der-transfer-syntax.md)
</dt> <dt>

[Codierte Länge und Wertbytes](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 




