---
title: Der Header
description: Der folgende Header stellt einen der Header Stile dar, der von der aktuellen Version von "Mittel l" generiert werden kann. Zur einfacheren Bereitstellung wird hier die vollständige Liste der Header Felder bereitgestellt.
ms.assetid: 2078d2d9-1757-4449-9cc1-a21804654722
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0afcc9ad880278fdbcb8efc45fdabdc22ad06224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103858437"
---
# <a name="the-header"></a>Der Header

Der folgende Header stellt einen der Header Stile dar, der von der aktuellen Version von "Mittel l" generiert werden kann. Zur einfacheren Bereitstellung wird hier die vollständige Liste der Header Felder bereitgestellt.

([**– OIF**](/windows/desktop/Midl/-oi) -Header)

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

Erweiterungen beginnend mit Windows 2000: <8> für 32-Bit, <12> für 64-Bit)

``` syntax
extension_version<1>
INTERPRETER_OPT_FLAGS2<1>
ClientCorrHint<2>
ServerCorrHint<2>
NotifyIndex<2>
[ FloatDoubleMask<2> ]
```

Die Erweiterungs \_ Version<1> gibt die Größe des Erweiterungs Abschnitts in Bytes an. Dies ermöglicht es der aktuellen NDR-Engine, den Erweiterungs Abschnitt auch dann ordnungsgemäß zu überspringen, wenn der Abschnitt von einer neueren Compilerversion mit mehr Feldern stammt, als die aktuelle Engine versteht.

Die \_ interpreteropt- \_ FLAGS2 werden wie folgt definiert:

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

Der **hasnewcorrdesc** -Member gibt an, ob neue Korrelations Deskriptoren in den vom Compiler generierten Format Zeichenfolgen verwendet werden. Der neue Korrelations Deskriptor bezieht sich auf die Funktion zum Verweigern von Angriffen. Die **clientcorrcheck** -und **servercorrcheck** -Elemente werden festgelegt, wenn die Routine die Korrelations Überprüfung auf der angegeben Seite benötigt.

Die Flags **hasnotify** und **HasNotify2** geben an, dass die Routine das Benachrichtigungs Feature verwendet, das von den Kennzeichen Attributen **\[ \] Benachrichtigen** bzw. **\[ Benachrichtigen \_ \]** definiert wird.

Der **clientcorrcheck** -Member ist ein Cache Größen Hinweis auf der Clientseite, und **servercorrcheck** ist ein Hinweis auf der Serverseite. Wenn die Größe Null ergibt, sollte eine Standardgröße verwendet werden.

Das **notifyindex** -Element ist ein Index für eine Benachrichtigungs Routine, wenn eine verwendet wird.

Das **floatdoublemask** -Element adressiert das Problem eines Gleit Komma Arguments für 64-Bit-Windows. Dieses Feld wird nur für 64-Bit-stubwerte generiert. Die Maske ist für die Assemblyroutinen erforderlich, die die Register/Upload-Register von/zum virtuellen Stapel ausführen, um Gleit Komma Argumente zu verarbeiten und ordnungsgemäß zu registrieren. Die Maske besteht aus 2 Bits pro Argument oder und nicht mit einem Gleit Komma Register. Das Codieren lautet wie folgt: die am wenigsten wichtigen Bits entsprechen dem ersten FP-Register, die nächsten 2 Bits entsprechen dem zweiten Register usw.

> [!Note]  
> Bei Objekt Routinen endet das erste Argument im zweiten Register, da dieser Zeiger zuerst ist. Für jedes Register ist die Bedeutung von Bits wie in der folgenden Tabelle dargestellt.

 



| Bits | Bedeutung                                          |
|------|--------------------------------------------------|
| 01   | Ein float-Wert muss in das Register geladen werden.  |
| 10   | Ein Double-Wert muss in das Register geladen werden. |



 

00 und 11 sind ungültige Werte für die Bits.

Zurzeit gibt es acht FP-Register in einem Intel-Architektur-64-Bit-Prozessor, sodass für die Maske nur die niedrigsten 16B-Bits festgelegt werden können. Die Masken Größe wurde auf eine Summe von 16 Bits festgelegt, die auf der nicht geänderten C-compilermaske basiert.

## <a name="header-streamlining-for-performance"></a>Header Optimierung für Leistung

Um den Code zu vereinfachen und die Leistung zu verbessern, versucht der Compiler, wann immer möglich, einen Header fester Größe zu generieren. Insbesondere wird der folgende Header für Async DCOM verwendet:

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

 

 