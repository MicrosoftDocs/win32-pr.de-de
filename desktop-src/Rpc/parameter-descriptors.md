---
title: Parameterdeskriptoren
description: Wie bereits erwähnt, sind die Parameterdeskriptoren \8211;Oi und \ 8211;Oif vorhanden.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b4a13b052d49629333bd9cb121b4d1b661722cb3a7a69ad2a17d3e2740a0cd8e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118927549"
---
# <a name="parameter-descriptors"></a>Parameterdeskriptoren

Wie bereits erwähnt, sind Die Parameterdeskriptoren [**–Oi**](/windows/desktop/Midl/-oi) und **–Oif** vorhanden.

## <a name="the-oi-parameter-descriptors"></a>Die –Oi-Parameterdeskriptoren

Vollständig interpretierte Stubs erfordern zusätzliche Informationen für jeden Parameter in einem RPC-Aufruf. Die Parameterbeschreibungen einer Prozedur folgen unmittelbar nach der Beschreibung der Prozedur.

[**Simple –Oi**](/windows/desktop/Midl/-oi)

**Parameterdeskriptoren**

Das Format für die Beschreibung eines in - \[  \] oder -Rückgabeparameters vom Typ ist:

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

– oder –

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

Wobei simple \_ type<1> das FC-Token ist, das den einfachen Typ angibt. Die Codes sind wie folgt:

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

**Other –Oi**

**Parameterdeskriptoren**

Das Format für die Beschreibung für alle anderen Parametertypen lautet:

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

Wenn die \_ Parameterrichtung<1> Feld für jede dieser Beschreibungen muss eine der in der folgenden Tabelle aufgeführten Sein.



| Hex | Flag                          | Bedeutung                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| 4d  | FC \_ IN \_ PARAM                 | Ein in-Parameter.                                            |
| 50  | FC \_ IN \_ OUT \_ PARAM            | Ein In/Out-Parameter.                                        |
| 51  | FC \_ OUT \_ PARAM                | Ein out-Parameter.                                           |
| 52  | FC \_ RETURN \_ PARAM             | Ein Prozedurrückgabewert.                                   |
| 4f  | FC \_ IN \_ PARAM \_ NO \_ FREE \_ INST | Ein in xmit/rep als Parameter, für den keine Freigabe erfolgt. |



 

Die \_ Stapelgröße<1> entspricht der Größe des Parameters im Stapel, ausgedrückt als die Anzahl der ganzen Zahlen, die der Parameter im Stapel belegt.

> [!Note]  
> Der [**-Oi-Modus**](/windows/desktop/Midl/-oi) wird auf 64-Bit-Plattformen nicht unterstützt.

 

Der \_ Typoffset<2> Feld ist der Offset in der Zeichenfolgentabelle des Typformats, der den Typdeskriptor für das Argument angibt.

## <a name="the-oif-parameter-descriptors"></a>Die -Oif-Parameterdeskriptoren

Es gibt zwei mögliche Formate für eine Parameterbeschreibung: eines für Basistypen, eins für alle anderen Typen.

Basistypen:

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_format_char<1> 
unused<1>
```

Sonstiges:

``` syntax
PARAM_ATTRIBUTES<2> 
stack_offset<2> 
type_offset<2>
```

In beiden \_ Stapeloffsets<2> gibt den Offset auf dem virtuellen Argumentstapel in Bytes an. Bei Basistypen wird der Argumenttyp direkt durch das Formatzeichen angegeben, das dem Typ entspricht. Bei anderen Typen gibt der \_ Typoffset<2> Feld den Offset in der Zeichenfolgentabelle des Typformats an, in der sich der Typdeskriptor für das Argument befindet.

Das Parameterattributfeld ist wie folgt definiert:

``` syntax
typedef struct
  {
  unsigned short  MustSize            : 1;    // 0x0001
  unsigned short  MustFree            : 1;    // 0x0002
  unsigned short  IsPipe              : 1;    // 0x0004
  unsigned short  IsIn                : 1;    // 0x0008
  unsigned short  IsOut               : 1;    // 0x0010
  unsigned short  IsReturn            : 1;    // 0x0020
  unsigned short  IsBasetype          : 1;    // 0x0040
  unsigned short  IsByValue           : 1;    // 0x0080
  unsigned short  IsSimpleRef         : 1;    // 0x0100
  unsigned short  IsDontCallFreeInst  : 1;    // 0x0200
  unsigned short  SaveForAsyncFinish  : 1;    // 0x0400
  unsigned short  Unused              : 2;
  unsigned short  ServerAllocSize     : 3;    // 0xe000
  } PARAM_ATTRIBUTES, *PPARAM_ATTRIBUTES;
```

-   Das **MustSize-Bit** wird nur festgelegt, wenn die Größe des Parameters festgelegt werden muss.
-   Das **MustFree-Bit** wird festgelegt, wenn der Server die NdrFree-Routine des Parameters aufrufen \* muss.
-   Das **IsSimpleRef-Bit** wird für einen Parameter festgelegt, der ein Verweiszeiger auf einen anderen Zeiger als einen anderen Zeiger ist und über keine zugeordneten Attribute verfügt. Bei einem solchen Typ stellt der Typoffset der Parameterbeschreibung \_<> Feld mit Ausnahme eines Verweiszeigers auf einen Basistyp den Offset zum Typ des Referenzreferenzs bereit. Der Verweiszeiger wird einfach übersprungen.
-   Das **IsDontCallFreeInst-Bit** wird für bestimmte \_ Darstellende als Parameter festgelegt, deren Routinen für freie Instanzen nicht aufgerufen werden sollen.
-   Die **ServerAllocSize-Bits** sind ungleich 0 (null), wenn der Parameter \[ **out** \] ist, \[ **in**, oder \] \[ **in,out** Zeiger auf Zeiger oder Zeiger auf \] enum16, und wird im Stapel des Serverinterpreters initialisiert, anstatt einen Aufruf von I **\_ RpcAllocate** zu verwenden. Wenn der Wert ungleich 0 (null) ist, wird dieser Wert mit 8 multipliziert, um die Anzahl der Bytes für den Parameter abzurufen. Beachten Sie, dass auf diese Weise immer mindestens 8 Bytes für einen Zeiger zugeordnet werden.
-   Das **IsBasetype-Bit** wird für einfache Typen festgelegt, die von der [**Main-Oif-Interpreterschleife**](/windows/desktop/Midl/-oi) gemarshallt werden. Insbesondere wird ein einfacher Typ mit einem Bereichsattribut nicht als Basistyp gekennzeichnet, um das Marshalling der Bereichsroutine durch die Verteilung mithilfe eines FC \_ RANGE-Tokens zu erzwingen.
-   Das **IsByValue-Bit** wird für zusammengesetzte Typen festgelegt, die als Wert gesendet werden, aber nicht für einfache Typen, unabhängig davon, ob das Argument ein Zeiger ist. Die zusammengesetzten Typen, für die sie festgelegt ist, sind Strukturen, Unions, [**übertragen \_ als**](/windows/desktop/Midl/transmit-as), [**stellen \_ als**](/windows/desktop/Midl/represent-as)dar, [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) und SAFEARRAY. Im Allgemeinen wurde das Bit zum Vorteil der Hauptinterpreterschleife im [**-Oicf-Interpreter**](/windows/desktop/Midl/-oi) eingeführt, um sicherzustellen, dass die nicht einfachen Argumente (als zusammengesetzte Typargumente bezeichnet) ordnungsgemäß dereferenziert werden. Dieses Bit wurde in früheren Versionen des Interpreters nie verwendet.

 

 