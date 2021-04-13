---
title: Abfragen von Schema Objekten der Kategorie 1 oder 2
description: Das systemFlags-Attribut von attributeSchema-und classSchema-Objekten ist eine ganzzahlige Bitmaske, die Flags enthält, die zusätzliche System Qualitäten des Attributs oder der Klasse angeben.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Abfragen von Schema Objekten der Kategorie 1 oder 2
- Objekt-AD, Abfragen von Schema Objekten der Kategorie 1 oder 2
- Schema AD, Abfragen von Schema Objekten der Kategorie 1 oder 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c67b57821cbebc80b3b6e93d158bbb8af8f7103
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314619"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a>Abfragen von Schema Objekten der Kategorie 1 oder 2

Das **systemFlags** -Attribut von **attributeSchema** -und **classSchema** -Objekten ist eine ganzzahlige Bitmaske, die Flags enthält, die zusätzliche System Qualitäten des Attributs oder der Klasse angeben. Die [**ADS \_ Systemflag \_ enum**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) -Enumeration enthält Werte, die den Bits entsprechen, die Sie im **systemFlags** -Attribut festlegen können. Es gibt weitere **systemFlags** -Bits, die Sie nicht festlegen können, z. b. das 0x10-Bit, das angibt, ob das Attribut oder die Klasse Kategorie 1 oder Kategorie 2 ist. Das 0x10-Bit ist für Objekte der Kategorie 1 festgelegt, bei denen es sich um die Klassen und Attribute handelt, die in dem im System enthaltenen Basis Schema enthalten sind. Das-Bit ist nicht für Attribute und Klassen der Kategorie 2 festgelegt, bei denen es sich um Erweiterungen für das Schema handelt. Wenn für ein **attributeSchema** -oder **classSchema** -Objekt keine **systemFlags** -Eigenschaft vorhanden ist, ist es Kategorie 2.

Das **Bit mit der LDAP-abgleichsregel \_ \_ \_ \_ und** die abgleichsregel können verwendet werden, um nach Objekten zu suchen, für die das 0x10-Flag im **systemFlags** -Attribut Weitere Informationen finden Sie unter [Such Filter Syntax](/windows/desktop/ADSI/search-filter-syntax).

## <a name="querying-for-category-1"></a>Abfragen für Kategorie 1

Die folgende Abfrage Zeichenfolge sucht nach Kategorie 1-Attributen (**attributeSchema** -Objekte mit dem 0x10-Bit, das in der **systemFlags** -Eigenschaft festgelegt ist).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



Beachten Sie, dass die LDAP-Abfrage Syntax im obigen Beispiel Dezimalwerte erfordert. Daher muss der hexadezimale Wert des Flags in "Decimal" konvertiert werden. In diesem Fall ist Category 1 Bit 0x10, sodass der Filter Wert als 16 angegeben werden muss.

## <a name="querying-for-category-2"></a>Abfragen für Kategorie 2

Mit der folgenden Abfrage Zeichenfolge wird nach Kategorie 2 Attributen gesucht (**attributeSchema** -Objekte, für die das 0x10-Bit nicht in der **systemFlags** -Eigenschaft festgelegt ist).


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



Beachten Sie, dass diese Abfrage auch **attributeSchema** -Objekte zurückgibt, die nicht über eine **systemFlags** -Eigenschaft verfügen, und daher implizit nicht das angegebene Flag festgelegt haben.

 

 