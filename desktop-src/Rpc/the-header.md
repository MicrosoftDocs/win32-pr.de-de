---
title: Der Header
description: Der folgende Header stellt einen der Headerstile dar, die von der aktuellen Midl-Version generiert werden können. Der Einfachheit halber finden Sie hier die vollständige Liste der Headerfelder.
ms.assetid: 2078d2d9-1757-4449-9cc1-a21804654722
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b27ee00425f3611234b0cd001f254b1499a0d4873d05846c65a2828c3eeffe57
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118924539"
---
# <a name="the-header"></a>Der Header

Der folgende Header stellt einen der Headerstile dar, die von der aktuellen Midl-Version generiert werden können. Der Einfachheit halber finden Sie hier die vollständige Liste der Headerfelder.

([**–Oif-Header)**](/windows/desktop/Midl/-oi)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

Erweiterungen ab Windows 2000: <8> für 32-Bit, <12> für 64-Bit)

``` syntax
extension_version<1>
INTERPRETER_OPT_FLAGS2<1>
ClientCorrHint<2>
ServerCorrHint<2>
NotifyIndex<2>
[ FloatDoubleMask<2> ]
```

Die \_ Erweiterungsversion<1> gibt die Größe des Erweiterungsabschnitts in Bytes an. Auf diese Weise kann die aktuelle NDR-Engine den Erweiterungsabschnitt ordnungsgemäß durchgehen, auch wenn der Abschnitt aus einer späteren Compilerversion mit mehr Feldern stammen sollte, als die aktuelle Engine versteht.

Interpreter \_ OPT \_ FLAGS2 werden wie folgt definiert:

``` syntax
typedef struct
  {
  unsigned char   HasNewCorrDesc      : 1;    // 0x01
  unsigned char   ClientCorrCheck     : 1;    // 0x02
  unsigned char   ServerCorrCheck     : 1;    // 0x04
  unsigned char   HasNotify           : 1;    // 0x08
  unsigned char   HasNotify2          : 1;    // 0x10
  unsigned char   Unused              : 3;
  } INTERPRETER_OPT_FLAGS2, *PINTERPRETER_OPT_FLAGS2;
```

Der **HasNewCorrDesc-Member** gibt an, ob neue Korrelationsdeskriptoren in den vom Compiler generierten Formatzeichenfolgen verwendet werden. Der neue Korrelationsdeskriptor bezieht sich auf die Denial-of-Attack-Funktionalität. Die **Member ClientCorrCheck** und **ServerCorrCheck** werden festgelegt, wenn die Routine die Korrelationsprüfung auf der angegebenen Seite benötigt.

Die **Flags HasNotify** und **HasNotify2** geben an, dass die Routine die Benachrichtigungsfunktion verwendet, die durch die Attribute **\[ notify \]** bzw. **\[ notify \_ \]** definiert ist.

Der **ClientCorrCheck-Member** ist ein Cachegrößenhinweis auf clientseitiger Seite, und **ServerCorrCheck** ist ein Hinweis auf serverseitiger Seite. Wenn die Größe als 0 (null) angezeigt wird, sollte eine Standardgröße verwendet werden.

Das **NotifyIndex-Element** ist ein Index für eine Benachrichtigungsroutine, sofern eins verwendet wird.

Das **FloatDoubleMask-Element** behandelt das Problem eines Gleitkommaarguments für 64-Bit-Windows. Dieses Feld wird nur für 64-Bit-Stubs generiert. Die Maske wird für die Assemblyroutinen benötigt, die Register vom/zum virtuellen Stapel herunterladen/hochladen, um Gleitkommaargumente zu verarbeiten und ordnungsgemäß zu registrieren. Die Maske besteht aus 2 Bits pro Argument oder stattdessen pro Gleitkommaregister. Die Codierung sieht wie folgt aus: Die am wenigsten signifikanten Bits entsprechen dem ersten FP-Register, die nächsten 2 Bits entsprechen dem zweiten Register usw.

> [!Note]  
> Bei Objektroutinen endet das erste Argument im zweiten Register, da dieser Zeiger zuerst ist. Für jedes Register ist die Bedeutung von Bits wie in der folgenden Tabelle dargestellt.

 



| Bits | Bedeutung                                          |
|------|--------------------------------------------------|
| 01   | Ein float-Wert sollte in das Register geladen werden.  |
| 10   | Ein double-Wert sollte in das Register geladen werden. |



 

00 und 11 sind ungültige Werte für die Bits.

Derzeit gibt es acht FP-Register in einem Intel Architecture-64-Bit-Prozessor, sodass für die Maske nur 16b niedrigste Bits festgelegt werden können. Die Maskengröße wurde auf insgesamt 16 Bits festgelegt, basierend darauf, dass die C-Compilermaske unverändert bleibt.

## <a name="header-streamlining-for-performance"></a>Header Streamlining for Performance

Um Code zu vereinfachen und die Leistung zu verbessern, versucht der Compiler nach Möglichkeit, einen Header mit fester Größe zu generieren. Insbesondere wird der folgende Header für asynchrone DCOM verwendet:

``` syntax
typedef struct _NDR_DCOM_OI2_PROC_HEADER
  {
  unsigned char               HandleType;        // The Oi header
  INTERPRETER_FLAGS           OldOiFlags;        //
  unsigned short              RpcFlagsLow;       //
  unsigned short              RpcFlagsHi;        //
  unsigned short              ProcNum;           //
  unsigned short              StackSize;         //
  // expl handle descr is never generated        //
  unsigned short              ClientBufferSize;  // The Oi2 header
  unsigned short              ServerBufferSize;  //
  INTERPRETER_OPT_FLAGS       Oi2Flags;          //
  unsigned char               NumberParams;      //
  } NDR_DCOM_OI2_PROC_HEADER, *PNDR_DCOM_OI2_PROC_HEADER;
```

 

 