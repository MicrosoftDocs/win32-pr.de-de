---
title: ISAN
description: Das Isan-Attribut enthält die internationale Standard mäßige audionummer (ISAN), die den Inhalt identifiziert.
ms.assetid: 2937d422-f062-4373-845e-dd200512ed0b
keywords:
- Windows Media-Format von Isan
topic_type:
- apiref
api_name:
- ISAN
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 88dc4a850edc43178deb043143ee8f9b37140507
ms.sourcegitcommit: 3e70ae762629e244028b437420ed50b5850db4e3
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/20/2020
ms.locfileid: "104389968"
---
# <a name="isan"></a>ISAN

Das **Isan** -Attribut enthält die internationale Standard mäßige audionummer (ISAN), die den Inhalt identifiziert.

## <a name="global-constant"></a>Globale Konstante

g \_ wszisan

## <a name="data-type"></a>Datentyp

**WMT \_ - \_ Typzeichenfolge**

## <a name="remarks"></a>Bemerkungen

ISAN ist ein internationaler Standard für die Identifizierung von audiovisuellen Works. Informationen zu Isan finden Sie auf der Standard [Website](https://www.isan.org/)von.

Das Metadateneditor-Objekt überprüft die ISA-Zeichenfolge, wenn Sie dieses Attribut festlegen. Die akzeptable Zeichen folgen Formatierung, wie in Abschnitt 4,1 der Isan-Spezifikation beschrieben, besteht aus 16 hexadezimalen Ziffern, die optional durch Leerzeichen oder Bindestriche in vierstellige Segmente voneinander getrennt sind. Die formatierte Zahl muss befolgt werden, auch optional durch ein Leerzeichen oder Bindestrich getrennt, durch ein gültiges Häkchen. Das Häkchen kann eine Dezimal Ziffer oder ein Großbuchstabe sein. Informationen zum Ableiten der Kontrollnummer finden Sie in Anhang A des Isan-Benutzerhandbuchs.

Auf die standardmäßige Isan-Zeichenfolge folgen möglicherweise Versionsinformationen. Falls vorhanden, bestehen Versionsinformationen aus acht hexadezimalen Ziffern, gefolgt von einer Kontrollnummer. Die Formatierung dieser Zeichen folgt denselben Regeln wie die Basis Zeichenfolge.

## <a name="examples"></a>Beispiele

Im folgenden finden Sie drei Zeichen folgen mit akzeptabler Formatierung für ein Beispiel-Isan.


```
00003BAB93520000G
0000 3BAB 9352 0000 G
0000-3BAB-9352-0000-G
```



Die folgende Zeichenfolge zeigt das Format eines Isan mit Versionsinformationen.


```C++
0000-3BAB-9352-0000-G-0000-0000-Q
```



## <a name="see-also"></a>Siehe auch

<dl> <dt>

[**Attributliste**](attribute-list.md)
</dt> </dl>

 

 




