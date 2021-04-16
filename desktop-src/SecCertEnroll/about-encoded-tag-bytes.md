---
description: Das Tagfeld in einem TLV-Dreieck identifiziert den Typ der Datenstruktur, die zwischen den Computern gesendet wird.
ms.assetid: 4723cc02-8c48-488e-95b8-c646a99b6aab
title: Codierte tagbytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5a5994f7beea0aba6896e94cb992a1e72eb70914
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104558120"
---
# <a name="encoded-tag-bytes"></a>Codierte tagbytes

Das *Tagfeld* in einem TLV-Dreieck identifiziert den Typ der Datenstruktur, die zwischen den Computern gesendet wird. Beispielsweise ist das-Tag für eine Ganzzahl 0x02, und das-Tag für einen Objekt Bezeichner ist 0x06. Obwohl mehrere Bytes zulässig sind, erfordert keiner der von der Zertifikatregistrierungs-API verwendeten Datentypen mehr als eins. Die folgende Abbildung zeigt die Aufschlüsselung eines *Tagwerts* . Bits 7 und 6 identifizieren die ASN. 1-Tagging-Klasse. Es gibt vier verfügbare Klassen, aber die Zertifikatregistrierungs-API verwendet Datentypen, die nur zur universellen Klasse gehören. Bit 5 gibt an, ob das Codierungs Formular primitiv oder erstellt ist. Basis-und Zeichen folgen Typen werden mithilfe von primitiven Formularen (konstruierte Typen) mithilfe eines konstruierten Formulars codiert. Weitere Informationen finden Sie unter [ASN. 1 Type System](about-asn-1-type-system.md). Bits 4 bis 0 enthalten die Tagnummer.

![der TLV-tagbyte](images/der-tlv-tagbyte.png)

In der folgenden Tabelle werden die von der Zertifikatregistrierungs-API unterstützten Datentypen, das verwendete Codierungs Formular und der Tagwert aufgelistet.

| type              | ASN. 1-Klasse | Codierungs Formular | Tagwert                             |
|-------------------|-------------|---------------|---------------------------------------|
| Bitzeichenfolge        | Universeller   | Primitiv     | 00000011<br/> 0x03<br/> |
| BOOLEAN           | Universeller   | Primitiv     | 00000001<br/> 0x01<br/> |
| INTEGER           | Universeller   | Primitiv     | 00000010<br/> 0x02<br/> |
| NULL              | Universeller   | Primitiv     | 00000101<br/> 0x05<br/> |
| Objekt Bezeichner | Universeller   | Primitiv     | 00000110<br/> 0x06<br/> |
| Oktett-Zeichenfolge      | Universeller   | Primitiv     | 00000100<br/> 0x04<br/> |
| Bmpstring         | Universeller   | Primitiv     | 00011110<br/> 0x1E<br/> |
| IA5String         | Universeller   | Primitiv     | 00010110<br/> (0x16)<br/> |
| PrintableString   | Universeller   | Primitiv     | 00010011<br/> 0x13<br/> |
| Teletexstring     | Universeller   | Primitiv     | 00010100<br/> 0x14<br/> |
| UTF8String        | Universeller   | Primitiv     | 00001100<br/> (0x0c)<br/> |
| SEQUENCE          | Universeller   | Baute   | 00110000<br/> 0x30<br/> |
| Sequenz von       | Universeller   | Baute   | 00110000<br/> 0x30<br/> |
| SET               | Universeller   | Baute   | 00110001<br/> 0x31<br/> |
| Satz von            | Universeller   | Baute   | 00110001<br/> 0x31<br/> |



 

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DER-Übertragungs Syntax](about-der-transfer-syntax.md)
</dt> <dt>

[Codierte Länge und Wert Bytes](about-encoded-length-and-value-bytes.md)
</dt> </dl>

 

 




