---
title: union-Schlüsselwort (RPC)
description: Unions erfordern spezielle MIDL-Schlüsselwörter, um ihre Verwendung mit Remote Procedure Call (RPC) zu unterstützen.
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fde18cca09f4db81af8eada2ae102a1bea373ed7859b3a7fc2bb9637f28d584
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "119011008"
---
# <a name="union-keyword-rpc"></a>union-Schlüsselwort (RPC)

Einige Features der Programmiersprache C, z. B. Unions, erfordern spezielle MIDL-Schlüsselwörter, um ihre Verwendung in Remoteprozeduraufrufen zu unterstützen. Eine Union in der Programmiersprache C ist eine Variable, die Objekte verschiedener Typen und Größen enthält. Der Entwickler erstellt in der Regel eine Variable, um die in der Union gespeicherten Typen nachzuverfolgen. Um in einer verteilten Umgebung ordnungsgemäß zu funktionieren, muss die Variable, die den Typ der Union angibt, oder die *diskriminante*, auch für den Remotecomputer verfügbar sein. MIDL stellt den \[ [**\_ Switchtyp**](/windows/desktop/Midl/switch-type) bereit, \] und \[ [**switch \_ ist**](/windows/desktop/Midl/switch-is) \] schlüsselwörter, um den diskriminanten Typ und Namen zu identifizieren.

MIDL erfordert, dass die Diskriminanz auf zwei Arten mit der Union übertragen wird:

-   Die Union und die Diskriminanz müssen als Parameter bereitgestellt werden.
-   Die Union und die Diskriminanz müssen in einer -Struktur gepackt werden.

Midl stellt zwei grundlegende Typen von Unterscheidungs-Unions bereit: [**nicht gekapselte \_ Union**](/windows/desktop/Midl/nonencapsulated-unions) und [**gekapselte \_ Union.**](/windows/desktop/Midl/encapsulated-unions) Die Diskriminanz einer nicht gekapselten Union ist ein weiterer Parameter, wenn die Union ein Parameter ist. Es ist ein weiteres Feld, wenn die Union ein Feld einer -Struktur ist. Die Definition einer gekapselten Union wird in eine Strukturdefinition umgewandelt, deren erstes Feld diskriminant ist und deren zweite und letzte Felder die Union sind. Im folgenden Beispiel wird veranschaulicht, wie die Union und diskriminant als Parameter angegeben werden:

``` syntax
typedef [switch_type(short)] union 
{
    [case(0)]    short     sVal;
    [case(1)]    float     fVal;
    [case(2)]    char      chVal;
    [default]    ;
} DISCRIM_UNION_PARAM_TYPE;
 
short UnionParamProc(
    [in, switch_is(sUtype)] DISCRIM_UNION_PARAM_TYPE Union,
    [in] short sUtype);
```

Die Union im vorherigen Beispiel kann einen einzelnen Wert enthalten: **entweder short**, **float** oder **char**. Die Typdefinition für die Union enthält das MIDL-Switchtypattribut, das den Typ des Diskriminanten angibt. **\_** Hier \[ \_ gibt switch type(short) \] an, dass das diskriminante vom Typ **short** ist. Der Schalter muss ein ganzzahliger Typ sein.

Wenn die Union ein Member einer -Struktur ist, muss der Diskriminant ein Member derselben Struktur sein. Wenn die Union ein Parameter ist, muss die Diskriminanz ein anderer Parameter sein. Der Prototyp für die Funktion **UnionParamProc** im vorherigen Beispiel zeigt den diskriminanten *sUtype* als letzten Parameter des Aufrufs. (Die Diskriminanz kann an jeder Position im Aufruf angezeigt werden.) Der Typ des parameters, der im Switch angegeben **\[ \_ ist, muss \]** mit dem im **\[ \_ \] Switchtypattribut** angegebenen Typ übereinstimmen.

Im folgenden Beispiel wird die Verwendung einer einzelnen -Struktur veranschaulicht, die die Diskriminanz mit der Union packt:

``` syntax
typedef struct 
{
    short utype;  /* discriminant can precede or follow union */
    [switch_is(utype)] union 
    {
       [case(0)]   short     sVal;
       [case(1)]   float     fVal;
       [case(2)]   char      chVal;
       [default]   ;
    } u;
} DISCRIM_UNION_STRUCT_TYPE;
 
short UnionStructProc(
    [in] DISCRIM_UNION_STRUCT_TYPE u1);
```

Der Microsoft RPC MIDL-Compiler [](/windows/desktop/Midl/typedef) lässt Union-Deklarationen außerhalb von typedef-Konstrukten zu. Dieses Feature ist eine Erweiterung der DCE-IDL. Weitere Informationen finden Sie unter [**union**](/windows/desktop/Midl/union).

 

 