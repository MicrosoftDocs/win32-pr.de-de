---
title: Ziehpunkte
description: Bis zu zwei Teile in der Formatzeichenfolgenbeschreibung eines Prozedur-Adresshandles.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1bb31dcf075b7b07b65d2a976a37386e164d8cadc11903a33c22172c433a3a51
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118929537"
---
# <a name="handles"></a>Ziehpunkte

Bis zu zwei Teile in der Formatzeichenfolgenbeschreibung eines Prozedur-Adresshandles. Der erste Teil ist der Handletyp<1> feld der Beschreibung einer Prozedur, der verwendet \_ wird, um implizite Handles anzugeben. Dieser Teil ist immer vorhanden. Der zweite Teil ist eine Parameterbeschreibung eines beliebigen expliziten Handles in der Prozedur. Beides wird in den folgenden Abschnitten erläutert, zusammen mit einer Beschreibung der zusätzlichen MIDL-Compilerunterstützung der Stubdeskriptorstruktur für Bindungshandleprobleme.

## <a name="implicit-handles"></a>Implizite Handles

Wenn eine Prozedur ein implizites Handle für die Bindung verwendet, enthält der Handletyp<1>-Feld der Beschreibung der Prozedur einen von drei gültigen Werten ungleich \_ Null. Die MIDL-Compilerunterstützung für implizite Handles finden Sie im Feld IMPLICIT \_ HANDLE \_ INFO der Stubdeskriptorstruktur:

``` syntax
typedef  (__RPC_FAR * GENERIC_BINDING_ROUTINE)();

typedef struct 
  {
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE  pfnUnbind;
  } GENERIC_BINDING_ROUTINE_PAIR;
  
typedef struct __GENERIC_BINDING_INFO 
  {
  void __RPC_FAR*          pObj;
  unsigned char            Size;
  GENERIC_BINDING_ROUTINE  pfnBind;
  GENERIC_BINDING_ROUTINE    pfnUnbind;
  } GENERIC_BINDING_INFO,  *PGENERIC_BINDING_INFO;

union 
  {
  handle_t*                pAutoHandle;
  handle_t*                pPrimitiveHandle;
  PGENERIC_BINDING_INFO    pGenericBindingInfo;
  } IMPLICIT_HANDLE_INFO;
```

Wenn die Prozedur ein automatisches Handle verwendet, enthält **der pAutoHandle-Member** die Adresse der stub-defined-auto-Handlevariablen.

Wenn die Prozedur ein implizites primitives Handle verwendet, enthält der **pPrimitiveHandle-Member** die Adresse der Stub-Defined-Primitive-Handlevariablen.

Wenn die Prozedur schließlich ein implizites generisches Handle verwendet, enthält der **pGenericBindingInfo-Member** die Adresse des Zeigers auf die entsprechende **GENERISCHE BINDING \_ \_ INFO-Struktur.** Die DATENstruktur **MIDL \_ STUB \_ DESC** enthält einen Zeiger auf eine Auflistung generischer **BINDING \_ \_ PAIR-Strukturen.** Der Eintrag an der Nullposition dieser  Auflistung  ist für die Bindungs- und Bindungsroutinen reserviert, die dem generischen Bindungshandliment entspricht, auf das **pGenericBindingInfo** in **IMPLICIT HANDLE INFO \_ \_ verweist.** Der Typ des impliziten Bindungshandpunkts wird in der Formatzeichenfolge angegeben.

## <a name="explicit-handles"></a>Explizite Handles

Es gibt drei mögliche explizite Handletypen: context, generic und primitive. Bei einem expliziten Handle (oder einem ausschließlichen Out-Kontexthand handle, das auf die gleiche Weise behandelt wird) werden die Bindungshand handle-Informationen als einer der Parameter der \[  \] Prozedur angezeigt. Die drei möglichen Beschreibungen lauten wie folgt.

Primitiv

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

Das Flag<1>, ob das Handle von einem Zeiger übergeben wird.

Der Offset<2> gibt den Offset vom Anfang des Stapels zum primitiven Handle an.

> [!Note]  
> Eine primitive Handlebeschreibung in der Typformatzeichenfolge wird auf eine einzelne FC \_ IGNORE-Datei reduziert.

 

Allgemein

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

Das Flag und die Größe<1> das obere Flag nibble und die niedrigere \_ \_ Nibble-Größe. Das Flag gibt an, ob das Handle von einem Zeiger übergeben wird. Das Feld size gibt die Größe des benutzerdefinierten generischen Handletyps an. Diese Größe ist auf 1, 2 oder 4 Bytes auf 32-Bit-Systemen und 1, 2, 4 oder 8 Bytes auf 64-Bit-Systemen beschränkt.

Der Offset<2> gibt den Offset vom Anfang des Stapels des Zeigers auf die Daten der angegebenen Größe an.

Der Bindungsroutinenpaarindex<1>-Feld gibt den Index im \_ \_ Feld \_ aGenericBindingRoutinePairs des  Stubdeskriptors an die Bindungs- und **Bindungsroutinenfunktionszeder** für das generische Handle zurück.

> [!Note]  
> Eine generische Handlebeschreibung im Typformat ist nur die Beschreibung des verknüpften Datentyps.

 

Kontext

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

Die Flags<1>, wie das Handle übergeben wird und um welchen Typ es sich handelt. Gültige Flags werden in der folgenden Tabelle angezeigt.



| Hex | Flag                                   |
|-----|----------------------------------------|
| 80  | HANDLE \_ PARAM \_ IST ÜBER \_ \_ PTR            |
| 40  | HANDLE \_ PARAM \_ IS \_ IN                  |
| 20  | HANDLE \_ PARAM \_ IS \_ OUT                 |
| 21  | HANDLE \_ PARAM \_ IS \_ RETURN              |
| 08  | NDR \_ STRICT \_ CONTEXT \_ HANDLE           |
| 04  | \_NDR-KONTEXTHAND \_ HANDLE NO \_ \_ SERIALIZE    |
| 02  | NDR \_ CONTEXT \_ HANDLE \_ SERIALIZE        |
| 01  | NDR-KONTEXTHAND \_ HANDLE DARF NICHT NULL \_ \_ \_ \_ SEIN |



 

Die ersten vier Flags waren immer vorhanden, die letzten vier wurden Windows 2000 hinzugefügt.

Der Offset<2> Felds stellt den Offset vom Anfang des Stapels zum Kontexthand handle zurVerkn.

Der Kontextrundownroutinenindex<1> stellt einen Index im \_ \_ Feld \_ **apfnNdrRundownRoutines** des Stubdeskriptors für die Rundownroutine zur Anwendung, die für dieses Kontexthand handle verwendet wird. Der Compiler generiert immer einen Index. Bei Routinen ohne Rundownroutine ist dies ein Index für eine Tabellenposition, die NULL enthält.

Für stubs, die in **–Oi2** erstellt wurden, stellt der Parameter num<1> die Ordnungszahl ab 0 (null) zur Verfügung und gibt an, welches Kontexthand handle es in der angegebenen Prozedur \_ ist.

Bei früheren Versionen des Interpreters stellt der Parameter num<1> die Parameternummer des Kontexthandpunkts \_ ab 0 (null) in seiner Prozedur zur Verfügung.

> [!Note]  
> Eine Kontexthandpunktbeschreibung in der Typformatzeichenfolge hat nicht den Offset<2> in der Beschreibung.

 

## <a name="the-new-oif-header"></a>Der neue –Oif-Header

Wie bereits erwähnt, wird der [**Header –Oif**](/windows/desktop/Midl/-oi) auf den **Header –Oi** erweitert. Der Einfachheit halber werden hier alle Felder angezeigt:

(Der alte Header)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

(Die [**-Oif-Erweiterungen)**](/windows/desktop/Midl/-oi)

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

Die konstante Clientpuffergröße<2> gibt die Größe des Marshallingpuffers an, der vom Compiler \_ \_ \_ vorberechnt werden konnte. Dies kann nur eine Teilgröße sein, da das ClientMustSize-Flag die Größengröße auslöst.

Die konstante Serverpuffergröße<2> die Größe des Marshallingpuffers wie vom Compiler \_ \_ \_ vorausbesetzt. Dies kann nur eine Teilgröße sein, da das ServerMustSize-Flag die Größengröße auslöst.

Die INTERPRETER \_ OPT \_ FLAGS werden in Ndrtypes.h definiert:

``` syntax
typedef struct
  {
  unsigned char   ServerMustSize      : 1;    // 0x01
  unsigned char   ClientMustSize      : 1;    // 0x02
  unsigned char   HasReturn           : 1;    // 0x04
  unsigned char   HasPipes            : 1;    // 0x08
  unsigned char   Unused              : 1;
  unsigned char   HasAsyncUuid        : 1;    // 0x20
  unsigned char   HasExtensions       : 1;    // 0x40
  unsigned char   HasAsyncHandle      : 1;    // 0x80
  } INTERPRETER_OPT_FLAGS, *PINTERPRETER_OPT_FLAGS;
```

-   Das ServerMustSize-Bit wird festgelegt, wenn der Server einen Puffergrößer-Pass ausführen muss.
-   Das ClientMustSize-Bit wird festgelegt, wenn der Client einen Puffergrößer-Pass ausführen muss.
-   Das HasReturn-Bit wird festgelegt, wenn die Prozedur über einen Rückgabewert verfügt.
-   Das HasPipes-Bit wird festgelegt, wenn das Pipepaket verwendet werden muss, um ein Pipeargument zu unterstützen.
-   Das HasAsyncUuid-Bit wird festgelegt, wenn die Prozedur eine asynchrone DCOM-Prozedur ist.
-   Das HasExtensions-Bit gibt an, dass Windows 2000- und höher-Erweiterungen verwendet werden.
-   Das HasAsyncHandle-Bit gibt eine asynchrone RPC-Prozedur an.

Das HasAsyncHandle-Bit wurde ursprünglich für eine andere DCOM-Implementierung der asynchronen Unterstützung verwendet und konnte daher nicht für die aktuelle asynchrone Stilunterstützung in DCOM verwendet werden. Das HasAsyncUuid-Bit gibt dies derzeit an.

 

 