---
description: Das Längenfeld in einem TLV-Wert gibt die Anzahl der Bytes an, die im Wertfeld codiert sind.
ms.assetid: d72371f9-fe55-468d-b15b-0f8948674619
title: Codierte Länge und Wert Bytes
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b45eaec36875446d7493f37fc150f7b5f9d1a59c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106354641"
---
# <a name="encoded-length-and-value-bytes"></a>Codierte Länge und Wert Bytes

Das *Längen* Feld in einem TLV-Wert gibt die Anzahl der Bytes an, die im *Wertfeld* codiert sind. Das Feld *Wert* enthält den Inhalt, der zwischen den Computern gesendet wird. Wenn das *Wertfeld* weniger als 128 Bytes enthält, ist für das *Längen* Feld nur ein Byte erforderlich. Bit 7 des *Längen* Felds ist 0 (null), und die verbleibenden Bits identifizieren die Anzahl der Bytes, die gesendet werden. Wenn das *Wertfeld* mehr als 127 Bytes enthält, ist Bit 7 des *Längen* Felds eins (1), und die restlichen Bits identifizieren die Anzahl der Bytes, die für die Länge benötigt werden. Beispiele sind in der folgenden Abbildung dargestellt.

![der TLV-Längenbyte](images/der-tlv-lengthbyte.png)

## <a name="related-topics"></a>Zugehörige Themen

<dl> <dt>

[DER-Übertragungs Syntax](about-der-transfer-syntax.md)
</dt> <dt>

[Codierte tagbytes](about-encoded-tag-bytes.md)
</dt> </dl>

 

 



