---
title: Isan
description: Das ISAN-Attribut enthält die Isan -Eigenschaft (International Standard Number, Internationale Standard-Nummer der Zahl der Toten), die den Inhalt identifiziert.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- ISAN-Windows-Medienformat
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec2af088938219ed48f2b281c627c0b64cc8e13fdea630b54a51a6f23db1b448
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119808820"
---
# <a name="isan"></a>Isan

Das **ISAN-Attribut** enthält die Isan -Eigenschaft (International Standard Number, Internationale Standard-Nummer der Zahl der Toten), die den Inhalt identifiziert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszZWN

## <a name="data-type"></a>Datentyp

**\_WMT-TYPZEICHENFOLGE \_**

## <a name="remarks"></a>Hinweise

ISAN ist ein internationaler Standard für die Identifizierung von Erkennungsarbeiten. Informationen zu ISAN finden Sie auf der [Standardwebsite](https://www.isan.org/).

Das Metadaten-Editor-Objekt überprüft die ISAN-Zeichenfolge, wenn Sie dieses Attribut festlegen. Die zulässige Zeichenfolgenformatierung, wie in Abschnitt 4.1 der ISAN-Spezifikation beschrieben, besteht aus 16 Hexadezimalziffern, die optional durch Leerzeichen oder Bindestriche in vierstellige Segmente getrennt sind. Auf die formatierte Zahl muss optional durch ein Leerzeichen oder Bindestrich ein gültiges Häkungszeichen folgen. Das Häkungszeichen kann eine Dezimalstelle oder ein Großbuchstaben sein. Informationen zum Ableiten der Prüfnummer finden Sie im Anhang A des ISAN-Benutzerhandbuchs.

Auf die ISAN-Standardzeichenfolge können Versionsinformationen folgen. Falls vorhanden, bestehen Versionsinformationen aus acht Hexadezimalziffern, gefolgt von einer Prüfnummer. Die Formatierung dieser Zeichen folgt den gleichen Regeln wie die einfache Zeichenfolge.

## <a name="examples"></a>Beispiele

Im Folgenden finden Sie drei Zeichenfolgen, die für ein ISAN-Beispiel akzeptiert werden können.


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



Die folgende Zeichenfolge zeigt das Format eines ISAN mit Versionsinformationen.


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




