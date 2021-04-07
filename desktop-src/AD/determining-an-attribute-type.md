---
title: Bestimmen eines Attribut Typs
description: Das systemFlags-Attribut eines attributeSchema-Objekts enthält einen Satz von Flags, die verschiedene Qualitäten des Attribut Objekts angeben, z. b. ob das Attribut erstellt oder nicht repliziert wird.
ms.assetid: 58f44ea4-ecbd-4650-b366-37b05a975c68
ms.tgt_platform: multiple
keywords:
- Bestimmen eines Attribut Typs "AD"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b64b4d8b0ae5d6cbac38c9c44ed8e4a7aa5d5f57
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104038768"
---
# <a name="determining-an-attribute-type"></a>Bestimmen eines Attribut Typs

Das [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) -Attribut eines [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekts enthält einen Satz von Flags, die verschiedene Qualitäten des Attribut Objekts angeben, z. b. ob das Attribut erstellt oder nicht repliziert wird. In der folgenden Tabelle werden die Flags des **systemFlags** -Attributs aufgelistet, die sich auf den Speichertyp des Attributs auswirken. 

| Flagwert | BESCHREIBUNG                                                                                                          |
|------------|----------------------------------------------------------------------------------------------------------------------|
| 0x00000001 | Wenn dieses Flag im [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) -Attribut vorhanden ist, wird das Attribut nicht repliziert. |
| 0x00000004 | Wenn dieses Flag im [**systemFlags**](/windows/desktop/ADSchema/a-systemflags) -Attribut vorhanden ist, wird das-Attribut erstellt.    |



 

Es ist möglich, eine Abfrage Zeichenfolge zu erstellen, die zum Abfragen von konstruierten oder nicht replizierten Attributen verwendet werden kann. Die folgende Abfrage Zeichenfolge findet beispielsweise alle nicht replizierten [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekte. Beachten Sie, dass die Abfrage Zeichenfolge die Dezimal Entsprechung des-Werts erfordert, nicht die hexadezimale Entsprechung des-Werts. Weitere Informationen zur abgleichsregel-OID, die von dieser Abfrage Zeichenfolge verwendet wird, finden [Sie unter Angeben von Vergleichswerten](how-to-specify-comparison-values.md).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.804:=1))
```



Das [**searchFlags**](/windows/desktop/ADSchema/a-searchflags) -Attribut des [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekts jedes Attributs definiert, ob ein Attribut indiziert ist. ein indiziertes Attribut hat den Wert 1, ein nicht indiziertes Attribut hat den Wert 0. Die folgende Abfrage Zeichenfolge findet z. b. die **attributeSchema** -Objekte, die indizierte Attribute darstellen.


```C++
(&(objectCategory=attributeSchema)(searchFlags=1))
```



Das [**ismembership ofpartialattributeset**](/windows/desktop/ADSchema/a-ismemberofpartialattributeset) -Attribut des [**attributeSchema**](/windows/desktop/ADSchema/c-attributeschema) -Objekts jedes Attributs definiert, ob ein Attribut in den globalen Katalog repliziert wird. Dieses Attribut hat den Wert **true** , wenn das Attribut ein Member des globalen Katalogs ist, oder **false** , wenn sich die Attribute nicht im globalen Katalog befinden. Beispielsweise durchsucht die folgende Abfrage Zeichenfolge die **attributeSchema** -Objekte, die repliziert werden, in den globalen Katalog.


```C++
(&(objectCategory=attributeSchema)(isMemberOfPartialAttributeSet=TRUE))
```



 

 