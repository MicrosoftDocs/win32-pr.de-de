---
title: Parameter Deskriptoren
description: Wie bereits erwähnt, sind die OIF-Stil Parameter Deskriptoren vorhanden.
ms.assetid: c2dad284-abe5-4b38-b3a6-3c7373fc5b84
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 22f6f8b19eb6632c4111547925151865b03b9adc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103729409"
---
# <a name="parameter-descriptors"></a>Parameter Deskriptoren

Wie bereits erwähnt, gibt es die Parameter Deskriptoren [**– Oi**](/windows/desktop/Midl/-oi) und **– OIF** .

## <a name="the-oi-parameter-descriptors"></a>Die Parameter Deskriptoren von – Oi

Vollständig interpretierte stubvorgänge erfordern zusätzliche Informationen für jeden Parameter in einem RPC-Aufruf. Die Parameter Beschreibungen einer Prozedur folgen unmittelbar nach der Beschreibung der Prozedur.

[**Einfache – Oi**](/windows/desktop/Midl/-oi)

**Parameter Deskriptoren**

Das Format für die Beschreibung eines \[ **in** - \] oder Return simple type-Parameters ist:

``` syntax
FC_IN_PARAM_BASETYPE 
simple_type<1>
```

– oder –

``` syntax
FC_RETURN_PARAM_BASETYPE 
simple_type<1>
```

Dabei \_ ist Simple Type<1> das FC-Token, das den einfachen Typ angibt. Die Codes lauten wie folgt:

``` syntax
4e  FC_IN_PARAM_BASETYPE 
53  FC_RETURN_PARAM_BASETYPE
```

**Sonstige – Oi**

**Parameter Deskriptoren**

Das Format der Beschreibung für alle anderen Parametertypen lautet wie folgt:

``` syntax
param_direction<1> 
stack_size<1> 
type_offset<2>
```

Dabei muss die Parameter \_ Richtung<1> für jede dieser Beschreibungen eine der in der folgenden Tabelle aufgeführten Werte aufweisen.



| Hex | Flag                          | Bedeutung                                                     |
|-----|-------------------------------|-------------------------------------------------------------|
| 4d  | FC \_ in \_ param                 | Ein in-Parameter.                                            |
| 50  | FC \_ im \_ out-Parameter \_            | Ein in/out-Parameter.                                        |
| 51  | FC-out-Parameter \_ \_                | Ein out-Parameter.                                           |
| 52  | FC- \_ Rückgabe Parameter \_             | Ein-Prozedur Rückgabewert.                                   |
| 4f  | FC \_ in \_ param \_ ohne \_ freie \_ inst | Ein in xmit/Rep als Parameter, für den keine Freigabe erfolgt. |



 

Die Stapel \_ Größe<1> ist die Größe des Parameters auf dem Stapel, ausgedrückt als die Anzahl von Ganzzahlen, die der Parameter im Stapel einnimmt.

> [!Note]  
> Der [**– Oi**](/windows/desktop/Midl/-oi) -Modus wird auf 64-Bit-Plattformen nicht unterstützt.

 

Der \_ typoffset<2> Feld ist der Offset in der Zeichen folgen Tabelle des typformats, der den Typdeskriptor für das Argument angibt.

## <a name="the-oif-parameter-descriptors"></a>Die – OIF-Parameter Deskriptoren

Es gibt zwei mögliche Formate für eine Parameter Beschreibung: eine für Basis Typen, eine für alle anderen Typen.

Basis Typen:

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

In beiden Stapel \_ Offset<2> den Offset auf dem virtuellen Argument Stapel in Bytes angibt. Für Basis Typen wird der Argumenttyp direkt durch das Formatzeichen angegeben, das dem-Typ entspricht. Bei anderen Typen \_ gibt das> Feld typoffset<2 den Offset in der Zeichen folgen Tabelle des typformats an, in der sich der Typdeskriptor für das Argument befindet.

Das Feld "Parameter Attribut" ist wie folgt definiert:

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

-   Das **mustsize** -Bit wird nur festgelegt, wenn der Parameter eine Größe aufweisen muss.
-   Das **mustfree** -Bit wird festgelegt, wenn der Server die ndrfree-Routine des Parameters aufrufen muss \* .
-   Das **issimpleref** -Bit ist für einen Parameter festgelegt, bei dem es sich um einen Verweis Zeiger auf einen anderen Zeiger handelt, der keine Attribute zuordnen hat. Bei einem solchen Typ \_ stellt das typoffset<> Feld der Parameter Beschreibung, mit Ausnahme eines Verweis Zeigers auf einen Basistyp, den Offset für den Typ des Referenten bereit. der Verweis Zeiger wird einfach übersprungen.
-   Das **isdontcallfreeinst** Bit ist für eine bestimmte Darstellung \_ als Parameter festgelegt, deren freie instanzroutinen nicht aufgerufen werden sollen.
-   Die " **serverallocsize** "-Bits sind ungleich 0 (null), wenn der Parameter " \[ **out**" \] , " \[ **in**" oder "in", " \] \[ **out** " \] -Zeiger auf einen Zeiger oder ein Zeiger auf "enum16" ist und auf dem Stapel des Server interpreters initialisiert wird, anstatt einen Aufrufen von " **I \_ rpczuordnen**" Wenn der Wert ungleich 0 (null) ist, wird dieser Wert mit 8 multipliziert, um die Anzahl der Bytes für den Parameter zu erhalten. Beachten Sie, dass dies bedeutet, dass mindestens 8 Bytes immer für einen Zeiger zugeordnet werden.
-   Das **isbasetype** -Bit ist für einfache Typen festgelegt, die von der Main [**– OIF**](/windows/desktop/Midl/-oi) -interpreterschleife gemarshallt werden. Insbesondere wird ein einfacher Typ mit einem Range-Attribut nicht als Basistyp gekennzeichnet, um das Marshalling der Bereichs Routine durch die Verteilung mit einem FC- \_ Bereichs Token zu erzwingen.
-   Das **IsByValue** -Bit ist für Verbund Typen festgelegt, die als Wert gesendet werden, aber nicht für einfache Typen festgelegt sind, unabhängig davon, ob das Argument ein Zeiger ist. Die Verbund Typen, für die Sie festgelegt ist, sind Strukturen, Unions, über [**tragen \_ als**](/windows/desktop/Midl/transmit-as), [**darstellen \_ als**](/windows/desktop/Midl/represent-as), [**Wire \_ Marshal**](/windows/desktop/Midl/wire-marshal) und SAFEARRAY. Im Allgemeinen wurde das-Bit für den Vorteil der hauptinterpreterschleife im [**– Oicf**](/windows/desktop/Midl/-oi) -Interpreter eingeführt, um sicherzustellen, dass die nicht einfachen Argumente (die als Verbund-Typargumente bezeichnet werden) ordnungsgemäß dereferenziert werden. Dieses Bit wurde in früheren Versionen des interpreterers nie verwendet.

 

 