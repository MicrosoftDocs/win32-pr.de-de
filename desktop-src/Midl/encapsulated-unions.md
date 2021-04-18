---
title: Gekapselt Unions
description: Eine Union, die in der Diskriminante in einer Struktur in enthalten ist, ist eine gekapselte Union.
ms.assetid: d32c18b4-b2f6-4ce2-94fe-a495a3c15d14
keywords:
- Datentypen mittlerer l, gekapselte Unions
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4489a043ff3690ddb31a8acccf359dcd76940aa7
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106340649"
---
# <a name="encapsulated-unions"></a><span data-ttu-id="09026-104">Gekapselt Unions</span><span class="sxs-lookup"><span data-stu-id="09026-104">Encapsulated Unions</span></span>

<span data-ttu-id="09026-105">Eine Union, die in der Diskriminante in einer Struktur in enthalten ist, ist eine gekapselte Union.</span><span class="sxs-lookup"><span data-stu-id="09026-105">A union that is contained with its discriminant in a structure within is an encapsulated union.</span></span> <span data-ttu-id="09026-106">Die gekapselte Union wird durch das vorhanden sein des [**Switch**](switch.md) -Schlüssel Worts angegeben.</span><span class="sxs-lookup"><span data-stu-id="09026-106">The encapsulated union is indicated by the presence of the [**switch**](switch.md) keyword.</span></span> <span data-ttu-id="09026-107">Diese Art von Union hat den Namen, da der Mittelwert Compiler die Union und deren diskriminant in einer Struktur für die Übertragung während eines Remote Prozedur Aufrufes automatisch kapselt.</span><span class="sxs-lookup"><span data-stu-id="09026-107">This type of union is so named because the MIDL compiler automatically encapsulates the union and its discriminant in a structure for transmission during a remote procedure call.</span></span>

<span data-ttu-id="09026-108">Wenn das Union-Tag fehlt (z. b. den \_ Typ U1 im obigen Beispiel), generiert der Compiler die Struktur mit dem Union-Feld mit dem Namen *markierte \_ Union*.</span><span class="sxs-lookup"><span data-stu-id="09026-108">If the union tag is missing (U1\_TYPE in the example above), the compiler will generate the structure with the union field named *tagged\_union*.</span></span>

<span data-ttu-id="09026-109">Die Form der Unions muss plattformübergreifend identisch sein, um die Konnektivität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="09026-109">The shape of unions must be the same across platforms to ensure interconnectivity.</span></span>

<span data-ttu-id="09026-110">Eine Beschreibung der Form einer gekapselten Union finden Sie unter [**Union**](union.md).</span><span class="sxs-lookup"><span data-stu-id="09026-110">For a description of the form of an encapsulated union, see [**union**](union.md).</span></span>

## <a name="examples"></a><span data-ttu-id="09026-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09026-111">Examples</span></span>

``` syntax
typedef union _S1_TYPE switch (long l1) U1_TYPE 
{ 
    case 1024: 
        float f1; 
    case 2048: 
        double d2; 
} S1_TYPE; 
 
/* in generated header file */ 
typedef struct _S1_TYPE 
{ 
    long l1; 
    union 
    { 
        float f1; 
        double d2; 
    } U1_TYPE; 
} S1_TYPE;
```

<span data-ttu-id="09026-112">Weitere Informationen finden Sie unter " [Mittel l-Basis Typen](midl-base-types.md)", " [**char**](char-idl.md)", " **\[** [**context \_ handle**](context-handle.md)" **\]** , " [**Enumeration**](enum.md)", " **\[** [**First \_ is**](first-is.md)", " **\]** **\[** [**handle**](handle.md) **\]** **\[** [](ignore.md) **\]** [](int.md) **\[** [](ignore.md) **\]** **\[** [**\_**](last-is.md) **\]** **\[** [**\_**](length-is.md) **\]** **\[** [**\_**](max-is.md) **\]** **\[** [**\_**](ms-union-attrib.md) **\]** [](nonencapsulated-unions.md) **\[** [](ptr.md) **\]** **\[** [](ref.md) **\]** **\[** [**\_**](size-is.md) **\]** **\[** [](string.md) **\]** [](struct.md) [](switch.md) **\[** [**\_**](switch-is.md) **\]** **\[** [**\_**](switch-type.md) **\]** **\[** [**\_**](transmit-as.md) **\]** [](union.md) **\[** [](unique.md) ", "Ignore", "int", "Ignore", "Last is", "length is", "is", "be", "be", "Union" und "Unique".**\]**</span><span class="sxs-lookup"><span data-stu-id="09026-112">For related information, see [MIDL Base Types](midl-base-types.md), [**char**](char-idl.md), **\[**[**context\_handle**](context-handle.md)**\]**, [**enum**](enum.md), **\[**[**first\_is**](first-is.md)**\]**, **\[**[**handle**](handle.md)**\]**, **\[**[**ignore**](ignore.md)**\]**, [**int**](int.md), **\[**[**ignore**](ignore.md)**\]**, **\[**[**last\_is**](last-is.md)**\]**, **\[**[**length\_is**](length-is.md)**\]**, **\[**[**max\_is**](max-is.md)**\]**, **\[**[**ms\_union**](ms-union-attrib.md)**\]**, [Nonencapsulated Unions](nonencapsulated-unions.md), **\[**[**ptr**](ptr.md)**\]**, **\[**[**ref**](ref.md)**\]**, **\[**[**size\_is**](size-is.md)**\]**, **\[**[**string**](string.md)**\]**, [**struct**](struct.md), [**switch**](switch.md), **\[**[**switch\_is**](switch-is.md)**\]**, **\[**[**switch\_type**](switch-type.md)**\]**, **\[**[**transmit\_as**](transmit-as.md)**\]**, [**union**](union.md), and **\[**[**unique**](unique.md)**\]**</span></span>

 

 




