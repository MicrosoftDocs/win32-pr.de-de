---
title: Ziehpunkte
description: So viele wie zwei Teile in der Format Zeichenfolgen-Beschreibung einer Prozedur Adress Handles.
ms.assetid: 11c6742c-b2f5-4201-8b1c-7e31ae52e0da
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d1c1ce68b74440fc9339fb9cf9170bfdd1fdfcd
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104316065"
---
# <a name="handles"></a>Ziehpunkte

So viele wie zwei Teile in der Format Zeichenfolgen-Beschreibung einer Prozedur Adress Handles. Der erste Teil ist der Handle \_ -Typ<1> Feld der Beschreibung einer Prozedur, das verwendet wird, um implizite Handles anzugeben. Dieser Teil ist immer vorhanden. Der zweite Teil ist eine Parameter Beschreibung eines beliebigen expliziten Handles in der Prozedur. Beide werden in den folgenden Abschnitten erläutert, zusammen mit einer Erörterung der zusätzlichen Unterstützung von Unterstützung der stubdeskriptorstruktur für Bindungs handle-Probleme.

## <a name="implicit-handles"></a>Implizite Handles

Wenn eine Prozedur ein implizites Handle für die Bindung verwendet, \_ enthält der Handlertyp<1> Feld der Beschreibung eines der Prozeduren einen von drei gültigen Werten, die nicht NULL sind. Unterstützung für implizite Handles in der \_ Stub-deskriptorstruktur finden Sie unter Unterstützung für implizites Handle für implizite Handles \_ :

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

Wenn die Prozedur ein automatisches Handle verwendet, enthält das " **pautohandle** "-Element die Adresse der definierten Stub-Variablen "– Auto Handle".

Wenn die Prozedur ein implizites Primitives Handle verwendet, enthält das **pprimitivehandle** -Element die Adresse der definierten Stub-Variable – primitiver handle.

Wenn die Prozedur schließlich einen impliziten generischen Handle verwendet, enthält das **pgenericbindinginfo** -Element die Adresse des Zeigers zur entsprechenden **generischen \_ Bindungs \_ Informations** Struktur. Die Datenstruktur " **mittlerer l- \_ Stub- \_ DESC** " enthält einen Zeiger auf eine Auflistung **generischer \_ Bindungs \_ paar** Strukturen. Der Eintrag in der Null-Position dieser Auflistung ist für die **Bind** -und **Bindung** -Routinen reserviert, die dem generischen Bindungs handle entsprechen, auf das **pgenericbindinginfo** in **impliziten \_ \_ Handlerinformationen** verweist. Der Typ des impliziten Bindungs Handles wird in der Format Zeichenfolge angegeben.

## <a name="explicit-handles"></a>Explizite Handles

Es gibt drei mögliche explizite Handlertypen: Kontext, generisch und primitiv. Im Fall eines expliziten Handles (oder eines reinen \[  \] Kontext Handles, das auf die gleiche Weise behandelt wird), werden die Bindungs handle-Informationen als einer der Parameter der Prozedur angezeigt. Die drei möglichen Beschreibungen lauten wie folgt.

Primitiv

``` syntax
FC_BIND_PRIMITIVE, flag<1>, offset<2>.
```

Das Flag<1> gibt an, ob das Handle von einem Zeiger übermittelt wird.

Der Offset<2> stellt den Offset vom Anfang des Stapels zum primitiven Handle bereit.

> [!Note]  
> Eine primitive handle-Beschreibung in der Typformat Zeichenfolge wird auf eine einzelne FC- \_ Ignorierung reduziert.

 

Allgemein

``` syntax
FC_BIND_GENERIC, flag_and_size<1>, offset<2>, binding_routine_pair_index<1>, FC_PAD
```

Das Flag \_ und die \_ Größe<1> die den oberen Flag-Halbbyte und den unteren Halbbyte-Wert aufweist. Das Flag gibt an, ob das Handle von einem Zeiger übermittelt wird. Das Größen Feld gibt die Größe des benutzerdefinierten – generischen Handle-Typs an. Diese Größe ist auf 32-Bit-Systemen auf 1, 2 oder 4 Bytes und auf 64-Bit-Systemen auf 1, 2, 4 oder 8 Bytes beschränkt.

Das> Feld Offset<2 gibt den Offset vom Anfang des Stapels des Zeigers auf die Daten der angegebenen Größe an.

Der Bindungs \_ Routine- \_ Paar \_ Index<1> Feld gibt den Index im Feld agenericbindingroutinepaars des Stub-Deskriptors an die **Bind** -und **Bindung** -Routine Funktionszeiger für das generische Handle an.

> [!Note]  
> Eine generische handle-Beschreibung im Typformat ist nur die Beschreibung des zugehörigen Datentyps.

 

Kontext

``` syntax
FC_BIND_CONTEXT flags<1> offset<2> context_rundown_routine_index<1> param_num<1>
```

Die Flags<1> die Übergabe des Handles und des Typs angeben. Gültige Flags sind in der folgenden Tabelle aufgeführt.



| Hex | Flag                                   |
|-----|----------------------------------------|
| 80  | Handle \_ param \_ erfolgt \_ über \_ ptr.            |
| 40  | Handle \_ param \_ ist \_ in                  |
| 20  | Handle- \_ param \_ ist \_ out                 |
| 21  | Handle \_ param \_ ist \_ Return              |
| 08  | NDR \_ Strict- \_ Kontext \_ handle           |
| 04  | der NDR- \_ Kontext \_ handle ist \_ nicht \_ serialisiert.    |
| 02  | NDR- \_ Kontext \_ handle \_ serialisieren        |
| 01  | der NDR- \_ Kontext \_ handle \_ darf nicht \_ \_ NULL sein. |



 

Die ersten vier Flags sind immer vorhanden, die letzten vier wurden in Windows 2000 hinzugefügt.

Das> Feld Offset<2 gibt den Offset vom Anfang des Stapels bis zum Kontext Handle an.

Der Context- \_ Rundown- \_ Routine \_ Index<1> stellt einen Index im **apfnndrrundownroutinen** -Feld des Stub-Deskriptors für die für dieses Kontext Handle verwendete rundownroutine bereit. Der Compiler generiert immer einen Index. Bei Routinen, die keine Rundown-Routine aufweisen, handelt es sich hierbei um einen Index für eine Tabellenposition, die NULL enthält.

Für in **– Oi2** integrierte stubwerte gibt die param- \_ Zahl<1> die Ordinalzahl an, beginnend bei Null, um anzugeben, welcher Kontext Handle in der angegebenen Prozedur enthalten ist.

Bei früheren Versionen des interpreters stellt die param- \_ Zahl<1> die Parameter Nummer des Kontext Handles in der Prozedur bereit, beginnend bei Null.

> [!Note]  
> Die Beschreibung des Kontext Handles in der typformatzeichenfolge weist nicht den Offset<2> in der Beschreibung auf.

 

## <a name="the-new-oif-header"></a>Der neue – OIF-Header

Wie bereits erwähnt, wird der [**– OIF**](/windows/desktop/Midl/-oi) -Header auf den **– Oi** -Header erweitert. Aus praktischer Gründen werden alle Felder hier angezeigt:

(Der alte Header)

``` syntax
handle_type<1> 
Oi_flags<1>
[rpc_flags<4>]
proc_num<2>  
stack_size<2>
[explicit_handle_description<>]
```

(Die [**– OIF**](/windows/desktop/Midl/-oi) -Erweiterungen)

``` syntax
constant_client_buffer_size<2>
constant_server_buffer_size<2>
INTERPRETER_OPT_FLAGS<1>
number_of_params<1>
```

Die Konstante \_ Client \_ Puffer \_ Größe<2> gibt die Größe des marshallingpuffers an, der vom Compiler vorab berechnet werden könnte. Dies kann nur eine partielle Größe sein, da das clientmustsize-Flag die Größenänderung auslöst.

Die Konstante \_ Server \_ Puffer \_ Größe<2> gibt die Größe des marshallingpuffers an, der vom Compiler voraus berechnet wird. Dies kann nur eine partielle Größe sein, da das servermustsize-Flag die Größenänderung auslöst.

Die \_ interpreteropt- \_ Flags sind in ndrtypes. h definiert:

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

-   Das "servermustsize"-Bit wird festgelegt, wenn der Server einen Puffergrößen Durchlauf ausführen muss.
-   Das clientmustsize-Bit wird festgelegt, wenn der Client einen Puffergrößen Durchlauf ausführen muss.
-   Das hasreturn-Bit wird festgelegt, wenn die Prozedur über einen Rückgabewert verfügt.
-   Das haspipes-Bit wird festgelegt, wenn das pipepaket zur Unterstützung eines Pipe-Arguments verwendet werden muss.
-   Das hasasyncuuid-Bit ist festgelegt, wenn es sich bei der Prozedur um eine asynchrone DCOM-Prozedur handelt.
-   Das hasExtensions-Bit gibt an, dass Windows 2000-Erweiterungen und spätere Erweiterungen verwendet werden.
-   Das hasasynchandle-Bit gibt eine asynchrone RPC-Prozedur an.

Das hasasynchandle-Bit wurde anfänglich für eine andere DCOM-Implementierung der async-Unterstützung verwendet und konnte daher nicht für die asynchrone Unterstützung im aktuellen Stil in DCOM verwendet werden. Das hasasyncuuid-Bit gibt dies derzeit an.

 

 