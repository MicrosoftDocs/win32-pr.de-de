---
title: Gekapselte Unions
description: Eine Union, die mit ihrer Diskriminanz in einer Struktur in enthalten ist, ist eine gekapselte Union.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- Datentypen MIDL, gekapselte Unions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6bc8f8f830d49430551af7d6450b0174742b9436afcdba764e9fa6494c957d9c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119895360"
---
# <a name="encapsulated-unions"></a>Gekapselte Unions

Eine Union, die mit ihrer Diskriminanz in einer Struktur in enthalten ist, ist eine gekapselte Union. Die gekapselte Union wird durch das Vorhandensein [](switch.md) des switch-Schlüsselworts angegeben. Dieser Union-Typ wird so benannt, da der MIDL-Compiler die Union und ihre Diskriminanz automatisch in einer Struktur für die Übertragung während eines Remoteprozeduraufrufs kapselt.

Wenn das Union-Tag fehlt (U1 \_ TYPE im obigen Beispiel), generiert der Compiler die -Struktur mit dem Union-Feld mit dem Namen *tagged \_ union*.

Die Form der Unions muss plattformübergreifend gleich sein, um Interkonnektivität sicherzustellen.

Eine Beschreibung der Form einer gekapselten Union finden Sie unter [**union**](union.md).

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

Verwandte Informationen finden Sie unter [MIDL-Basistypen](midl-base-types.md), [**char**](char-idl.md), **\[** [**\_ Kontexthandle**](context-handle.md) **\]** , [**Enumeration**](enum.md), **\[** [**zuerst \_ ist**](first-is.md) **\]** , **\[** [**handle**](handle.md) **\]** , **\[** [**ignorieren**](ignore.md) **\]** , [**int**](int.md), **\[** [**ignorieren**](ignore.md), **\]** zuletzt **\[** [**\_ ist**](last-is.md) **\]** , länge ist , max **\[** [**\_**](length-is.md) **\]** **\[** [**\_ ist**](max-is.md) **\]** , ms **\[** [**\_ union**](ms-union-attrib.md) **\]** , Nicht [gekapselte Unions](nonencapsulated-unions.md), **\[** [**ptr**](ptr.md), **\]** **\[** [**ref**](ref.md), Größe **\]** **\[** [**\_ ist**](size-is.md) **\]** , **\[** [**Zeichenfolge**](string.md) **\]** , [**Struktur**](struct.md), Switch , [**Switch**](switch.md)ist , Switch **\[** [**\_ ist**](switch-is.md) **\]** , **\[** [**\_ Switchtyp**](switch-type.md) **\]** , übertragen **\[** [**\_ als**](transmit-as.md) **\]** , [**Union**](union.md)und **\[** [**eindeutig**](unique.md)**\]**

 

 




