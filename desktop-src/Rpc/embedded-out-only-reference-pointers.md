---
title: Eingebettete Out-Only Verweis Zeiger
description: Eingebettete Out-Only Verweis Zeiger
ms.assetid: b0fcba9e-b285-4d29-9ffc-c8d6d7818824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4072e9aa3cc3f0f673e4bb737016bc035a3ac496
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "106341323"
---
# <a name="embedded-out-only-reference-pointers"></a>Eingebettete Out-Only Verweis Zeiger

Wenn Sie \[ [](/windows/desktop/Midl/out-idl) \] in Microsoft RPC nur Out-Reference-Zeiger verwenden, weisen die generierten serverstubvorgänge nur die erste Ebene von Zeigern zu, auf die vom Verweis Zeiger aus zugegriffen werden kann. Zeiger auf tieferen Ebenen werden nicht durch die stubweise zugeordnet, sondern müssen von der Server Anwendungsebene zugeordnet werden. Angenommen, eine Schnittstelle gibt ein \[ **out** \] -only-Array von Verweis Zeigern an:

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

In diesem Beispiel ordnet der Server-Stub Speicher für 10 Zeiger zu und legt den Wert jedes Zeigers auf NULL fest. Die Serveranwendung muss den Arbeitsspeicher für die 10 [**kurzen**](/windows/desktop/Midl/short) Ganzzahlen zuordnen, auf die von den Zeigern verwiesen wird, und dann die 10 Zeiger so festlegen, dass Sie auf die ganzen Zahlen zeigen.

Wenn die \[ [**out**](/windows/desktop/Midl/out-idl) \] -only-Datenstruktur eingebundene Verweis Zeiger enthält, wird nur der erste Zeiger, auf den der Verweis Zeiger zugreifen kann Beispiel:

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

Im vorherigen Beispiel weisen die Server-Stub den Zeiger *pstopp* und den **\_ obersten \_ Typ** der Struktur Struktur zu. Der Verweis Zeiger *ps1* in **struct \_ Top \_ Type** wird auf NULL festgelegt. Der Serverstub weist nicht jede Ebene der Datenstruktur zu und weist auch den STRUCT1- **\_ Typ** oder den eingebetteten Zeiger, *psvalue*, zu.

 

 