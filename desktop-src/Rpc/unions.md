---
title: Union-Schlüsselwort (RPC)
description: Unions benötigen besondere Mittel Schlüssel Schlüsselwörter zur Unterstützung ihrer Verwendung mit Remote Prozedur Aufruf (RPC).
ms.assetid: e7c8296c-893d-4df7-913a-f969733e1917
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c562815d78ab931bd4d6590b5465647e72f4bf6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315242"
---
# <a name="union-keyword-rpc"></a>Union-Schlüsselwort (RPC)

Einige Features der Programmiersprache C (z. b. Unions) erfordern spezielle Mittel Schlüssel Schlüsselwörter, um ihre Verwendung in Remote Prozedur aufrufen zu unterstützen. Eine Union in der Programmiersprache C ist eine Variable, die Objekte mit unterschiedlichen Typen und Größen enthält. Der Entwickler erstellt in der Regel eine Variable, um die in der Union gespeicherten Typen nachzuverfolgen. Um ordnungsgemäß in einer verteilten Umgebung auszuführen, muss die Variable, die den Typ der Union oder die *Diskriminante* angibt, auch für den Remote Computer verfügbar sein. In der Mitte werden der \[ [**\_ Switchtyp**](/windows/desktop/Midl/switch-type) \] und die \[ [**Switch \_ is**](/windows/desktop/Midl/switch-is) - \] Schlüsselwörter zur Identifizierung des diskriminatentyps und des Namens angegeben

Bei der Verwendung von "Mittel l" muss die Diskriminante mit der Union auf zwei Arten übertragen werden:

-   Die Union und die Diskriminante müssen als Parameter bereitgestellt werden.
-   Die Union und die Diskriminante müssen in einer Struktur verpackt werden.

Zwei grundlegende Typen von Unterscheidungs-Unions werden von mittlerer l bereitgestellt: [**nicht gekapselte \_ Union**](/windows/desktop/Midl/nonencapsulated-unions) und [**gekapselte \_**](/windows/desktop/Midl/encapsulated-unions) Die Diskriminante einer nicht gekapselten Union ist ein weiterer Parameter, wenn die Union ein Parameter ist. Es ist ein weiteres Feld, wenn die Union ein Feld einer Struktur ist. Die Definition einer gekapselten Union wird in eine Struktur Definition umgewandelt, deren erstes Feld die Diskriminante ist und deren zweite und letzte Felder die Union darstellen. Im folgenden Beispiel wird veranschaulicht, wie die Union und die Diskriminante als Parameter bereitgestellt werden:

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

Die Union im vorangehenden Beispiel kann einen einzelnen Wert enthalten: " **Short**", " **float**" oder " **char**". Die Typdefinition für die Union enthält das Attribut "Mittelwert **Switch \_ Type** ", das den Typ des Diskriminanten angibt. Hier \[ gibt Switch \_ Type (Short) \] an, dass der diskriminant vom Typ **Short** ist. Der Switch muss ein ganzzahliger Typ sein.

Wenn die Union ein Member einer Struktur ist, muss die Diskriminante ein Member derselben Struktur sein. Wenn die Union ein Parameter ist, muss der diskriminant ein weiterer Parameter sein. Der Prototyp für die Funktion **unionparamproc** im vorangehenden Beispiel zeigt den Diskriminanten *sutype* als letzten Parameter des Aufrufes. (Die Diskriminante kann an einer beliebigen Position im-Befehl angezeigt werden.) Der im Switch angegebene Typ des Parameters muss dem Typ entsprechen, der im **\[ Switch \_ Type \]** -Attribut angegeben **\[ \_ ist \]** .

Im folgenden Beispiel wird die Verwendung einer einzelnen-Struktur veranschaulicht, die den Diskriminanten mit der Union verpackt:

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

Der Microsoft RPC-Mittell-Compiler ermöglicht Union-Deklarationen außerhalb von [**typedef**](/windows/desktop/Midl/typedef) -Konstrukten. Diese Funktion ist eine Erweiterung der DCE-IDL. Weitere Informationen finden Sie unter [**Union**](/windows/desktop/Midl/union).

 

 