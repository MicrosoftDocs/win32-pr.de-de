---
description: Das Feld Length in einem TLV-Triplet identifiziert die Anzahl der bytes, die im Feld Wert codiert sind.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Codierte Länge und Wertbytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ea44ec9892e9407cbe587dbb60219b758ac95392e64dfabcf4866e02a1ad9343
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118904474"
---
# <a name="encoded-length-and-value-bytes"></a>Codierte Länge und Wertbytes

Das *Feld Length* in einem TLV-Triplet identifiziert die Anzahl der bytes, die im Feld *Wert* codiert sind. Das Feld *Wert* enthält den Inhalt, der zwischen Computern gesendet wird. Wenn das Feld *Wert* weniger als 128 Bytes enthält, benötigt das *Feld Length* nur ein Byte. Bit 7 des *Felds Length* ist null (0), und die verbleibenden Bits geben die Anzahl der gesendeten Bytes des Inhalts an. Wenn das *Feld Wert* mehr als 127 Bytes enthält, ist Bit 7 des *Felds Length* eins (1), und die verbleibenden Bits geben die Anzahl der Bytes an, die für die Länge erforderlich sind. Beispiele sind in der folgenden Abbildung dargestellt.

![der tlv length byte](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DER-Übertragungssyntax](about-der-transfer-syntax.md)
</dt> <dt>

[Codierte Tagbytes](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



