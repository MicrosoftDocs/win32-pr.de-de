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
# <a name="embedded-out-only-reference-pointers"></a><span data-ttu-id="beffa-103">Eingebettete Out-Only Verweis Zeiger</span><span class="sxs-lookup"><span data-stu-id="beffa-103">Embedded Out-Only Reference Pointers</span></span>

<span data-ttu-id="beffa-104">Wenn Sie \[ [](/windows/desktop/Midl/out-idl) \] in Microsoft RPC nur Out-Reference-Zeiger verwenden, weisen die generierten serverstubvorgänge nur die erste Ebene von Zeigern zu, auf die vom Verweis Zeiger aus zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="beffa-104">When you use \[[**out**](/windows/desktop/Midl/out-idl)\]-only reference pointers in Microsoft RPC, the generated server stubs allocate only the first level of pointers accessible from the reference pointer.</span></span> <span data-ttu-id="beffa-105">Zeiger auf tieferen Ebenen werden nicht durch die stubweise zugeordnet, sondern müssen von der Server Anwendungsebene zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="beffa-105">Pointers at deeper levels are not allocated by the stubs, but must be allocated by the server application layer.</span></span> <span data-ttu-id="beffa-106">Angenommen, eine Schnittstelle gibt ein \[ **out** \] -only-Array von Verweis Zeigern an:</span><span class="sxs-lookup"><span data-stu-id="beffa-106">For example, suppose an interface specifies an \[**out**\]-only array of reference pointers:</span></span>

``` syntax
/* IDL file (fragment) */
typedef [ref] short * PREF;

Proc1([out] PREF array[10]);
```

<span data-ttu-id="beffa-107">In diesem Beispiel ordnet der Server-Stub Speicher für 10 Zeiger zu und legt den Wert jedes Zeigers auf NULL fest.</span><span class="sxs-lookup"><span data-stu-id="beffa-107">In this example, the server stub allocates memory for 10 pointers and sets the value of each pointer to null.</span></span> <span data-ttu-id="beffa-108">Die Serveranwendung muss den Arbeitsspeicher für die 10 [**kurzen**](/windows/desktop/Midl/short) Ganzzahlen zuordnen, auf die von den Zeigern verwiesen wird, und dann die 10 Zeiger so festlegen, dass Sie auf die ganzen Zahlen zeigen.</span><span class="sxs-lookup"><span data-stu-id="beffa-108">The server application must allocate the memory for the 10 [**short**](/windows/desktop/Midl/short) integers referenced by the pointers and then set the 10 pointers to point to the integers.</span></span>

<span data-ttu-id="beffa-109">Wenn die \[ [**out**](/windows/desktop/Midl/out-idl) \] -only-Datenstruktur eingebundene Verweis Zeiger enthält, wird nur der erste Zeiger, auf den der Verweis Zeiger zugreifen kann</span><span class="sxs-lookup"><span data-stu-id="beffa-109">When the \[[**out**](/windows/desktop/Midl/out-idl)\]-only data structure includes nested reference pointers, the server stubs allocate only the first pointer accessible from the reference pointer.</span></span> <span data-ttu-id="beffa-110">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="beffa-110">For example:</span></span>

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

<span data-ttu-id="beffa-111">Im vorherigen Beispiel weisen die Server-Stub den Zeiger *pstopp* und den **\_ obersten \_ Typ** der Struktur Struktur zu.</span><span class="sxs-lookup"><span data-stu-id="beffa-111">In the preceding example, the server stubs allocate the pointer *psTop* and the structure **STRUCT\_TOP\_TYPE**.</span></span> <span data-ttu-id="beffa-112">Der Verweis Zeiger *ps1* in **struct \_ Top \_ Type** wird auf NULL festgelegt.</span><span class="sxs-lookup"><span data-stu-id="beffa-112">The reference pointer *ps1* in **STRUCT\_TOP\_TYPE** is set to null.</span></span> <span data-ttu-id="beffa-113">Der Serverstub weist nicht jede Ebene der Datenstruktur zu und weist auch den STRUCT1- **\_ Typ** oder den eingebetteten Zeiger, *psvalue*, zu.</span><span class="sxs-lookup"><span data-stu-id="beffa-113">The server stub does not allocate every level of the data structure, nor does it allocate the **STRUCT1\_TYPE** or its embedded pointer, *psValue*.</span></span>

 

 