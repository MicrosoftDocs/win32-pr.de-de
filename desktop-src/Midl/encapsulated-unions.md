---
title: Gekapselt Unions
description: Eine Union, die in der Diskriminante in einer Struktur in enthalten ist, ist eine gekapselte Union.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- Datentypen mittlerer l, gekapselte Unions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4489a043ff3690ddb31a8acccf359dcd76940aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340649"
---
# <a name="encapsulated-unions"></a>Gekapselt Unions

Eine Union, die in der Diskriminante in einer Struktur in enthalten ist, ist eine gekapselte Union. Die gekapselte Union wird durch das vorhanden sein des [**Switch**](switch.md) -Schlüssel Worts angegeben. Diese Art von Union hat den Namen, da der Mittelwert Compiler die Union und deren diskriminant in einer Struktur für die Übertragung während eines Remote Prozedur Aufrufes automatisch kapselt.

Wenn das Union-Tag fehlt (z. b. den \_ Typ U1 im obigen Beispiel), generiert der Compiler die Struktur mit dem Union-Feld mit dem Namen *markierte \_ Union*.

Die Form der Unions muss plattformübergreifend identisch sein, um die Konnektivität zu gewährleisten.

Eine Beschreibung der Form einer gekapselten Union finden Sie unter [**Union**](union.md).

## <a name="examples"></a>Beispiele

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

Weitere Informationen finden Sie unter " [Mittel l-Basis Typen](midl-base-types.md)", " [**char**](char-idl.md)", " **\[** [**context \_ handle**](context-handle.md)" **\]** , " [**Enumeration**](enum.md)", " **\[** [**First \_ is**](first-is.md)", " **\]** **\[** [**handle**](handle.md) **\]** **\[** [](ignore.md) **\]** [](int.md) **\[** [](ignore.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](ms-union-attrib.md) **\]** [](nonencapsulated-unions.md) **\[** [](ptr.md) **\]** **\[** [](ref.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** [](struct.md) [](switch.md) **\[** [**\_**](switch-is.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** [](union.md) **\[** [](unique.md) ", "Ignore", "int", "Ignore", "Last is", "length is", "is", "be", "be", "Union" und "Unique".**\]**

 

 




