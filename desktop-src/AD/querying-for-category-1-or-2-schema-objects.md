---
title: Abfragen von Schemaobjekten der Kategorie 1 oder 2
description: Das systemFlags-Attribut von attributeSchema- und classSchema-Objekten ist eine ganzzahlige Bitmaske, die Flags enthält, die zusätzliche Systemqualitäten des Attributs oder der Klasse angeben.
ms.assetid: 5cc8f296-df3e-4643-9694-543f069a2cc7
ms.tgt_platform: multiple
keywords:
- Abfragen von Ad-Schemaobjekten der Kategorie 1 oder 2
- Objekt AD , Abfragen von Schemaobjekten der Kategorie 1 oder 2
- Schema-AD, Abfragen von Schemaobjekten der Kategorie 1 oder 2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f934ba0401c7d782706e1e853819ba935c1315a267c668614878ec41045f63b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119025348"
---
# <a name="querying-for-category-1-or-2-schema-objects"></a>Abfragen von Schemaobjekten der Kategorie 1 oder 2

Das **systemFlags-Attribut** von **attributeSchema-** und **classSchema-Objekten** ist eine ganzzahlige Bitmaske, die Flags enthält, die zusätzliche Systemqualitäten des Attributs oder der Klasse angeben. Die [**ADS \_ SYSTEMFLAG-ENUM-Enumeration \_**](/windows/win32/api/iads/ne-iads-ads_systemflag_enum) enthält Werte, die den Bits entsprechen, die Sie im **systemFlags-Attribut** festlegen können. Es gibt zusätzliche **systemFlags-Bits,** die Sie nicht festlegen können, z. B. das 0x10 Bit, das angibt, ob das Attribut oder die Klasse Kategorie 1 oder Kategorie 2 ist. Das 0x10 Bit wird für Objekte der Kategorie 1 festgelegt, bei denen es sich um die Klassen und Attribute handelt, die im Basisschema des Systems enthalten sind. Das Bit ist nicht für Attribute und Klassen der Kategorie 2 festgelegt, bei denen es sich um Erweiterungen des Schemas handelt. Wenn für ein **attributeSchema-** oder **classSchema-Objekt** keine **systemFlags-Eigenschaft** vorhanden ist, handelt es sich um Kategorie 2.

Die **LDAP MATCHING RULE BIT \_ \_ \_ AND-Abgleichsregel \_** kann verwendet werden, um nach Objekten zu suchen, für die das 0x10-Flag im **systemFlags-Attribut** festgelegt ist. Weitere Informationen finden Sie unter [Suchfiltersyntax.](/windows/desktop/ADSI/search-filter-syntax)

## <a name="querying-for-category-1"></a>Abfragen von Kategorie 1

Die folgende Abfragezeichenfolge sucht nach Attributen der Kategorie 1 (**attributeSchema-Objekte** mit dem in der **systemFlags-Eigenschaft** festgelegten 0x10 Bit).


```C++
(&(objectCategory=attributeSchema)(systemFlags:1.2.840.113556.1.4.803:=16) )
```



Beachten Sie, dass die LDAP-Abfragesyntax im obigen Beispiel Dezimalwerte erfordert. daher muss der Hexadezimalwert des Flags in decimal konvertiert werden. In diesem Fall wird kategorie 1 bit 0x10, sodass der Filterwert als 16 angegeben werden muss.

## <a name="querying-for-category-2"></a>Abfragen von Kategorie 2

Die folgende Abfragezeichenfolge sucht nach Attributen der Kategorie 2 (**attributeSchema-Objekte,** für die in der **systemFlags-Eigenschaft** kein 0x10 Bit festgelegt ist).


```C++
(&(objectCategory=attributeSchema)(!(systemFlags:1.2.840.113556.1.4.803:=16)))
```



Beachten Sie, dass diese Abfrage auch **attributeSchema-Objekte** zurückgibt, die nicht über eine **systemFlags-Eigenschaft** verfügen und daher implizit nicht das angegebene Flag festgelegt haben.

 

 