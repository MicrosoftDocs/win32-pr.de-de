---
title: Eingebettete Out-Only Referenzzeker
description: Eingebettete Out-Only Referenzzeker
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d36fc6229c0b155e3fa9a7f66e6cd1fbd742d7ec876264a8706ce81c4150d6ba
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/11/2021
ms.locfileid: "118930522"
---
# <a name="embedded-out-only-reference-pointers"></a>Eingebettete Out-Only Referenzzeker

Wenn Sie \[ [](/windows/desktop/Midl/out-idl) \] out-only-Verweiszeiger in Microsoft RPC verwenden, ordnen die generierten Serverstubs nur die erste Ebene von Zeigern zu, auf die über den Verweiszeiger zugegriffen werden kann. Zeiger auf tieferen Ebenen werden nicht von den Stubs zugeordnet, sondern müssen von der Serveranwendungsebene zugeordnet werden. Angenommen, eine Schnittstelle gibt ein \[  \] Out-Only-Array von Verweisze0ern an:

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

In diesem Beispiel weist der Serverstub Arbeitsspeicher für 10 Zeiger zu und legt den Wert jedes Zeigers auf NULL fest. Die Serveranwendung muss den Arbeitsspeicher für [](/windows/desktop/Midl/short) die 10 kurzen ganzen Zahlen zuordnen, auf die die Zeiger verweisen, und dann die 10 Zeiger so festlegen, dass sie auf die ganzen Zahlen zeigen.

Wenn die \[ [**Out-Only-Datenstruktur**](/windows/desktop/Midl/out-idl)geschachtelte Verweiszeiger enthält, ordnen die Serverstubs nur den ersten Zeiger zu, auf den über den \] Verweiszeiger zugegriffen werden kann. Beispiel:

``` syntax
/* IDL file (fragment) */
typedef struct 
{
    [ref] small * psValue;
} STRUCT1_TYPE;

typedef struct 
{
    [ref] STRUCT1_TYPE * ps1;
} STRUCT_TOP_TYPE;

Proc2([out, ref] STRUCT_TOP_TYPE * psTop);
```

Im vorherigen Beispiel weisen die Serverstubs den Zeiger *psTop* und der **Strukturstruktur TOP \_ TYPE \_ zu.** Der Verweiszeiger *ps1* in **STRUCT \_ TOP \_ TYPE** ist auf NULL festgelegt. Der Serverstub ordnet weder jede Ebene der Datenstruktur zu, noch ordnet er **STRUCT1 \_ TYPE** oder den eingebetteten Zeiger *psValue zu.*

 

 