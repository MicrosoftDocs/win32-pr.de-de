---
title: " in, String und Out, Zeichen folgen Prototyp"
description: Der folgende Funktionsprototyp verwendet die beiden Parameter a \ in, String \ Parameter und a \ Out, String \ Parameter.
ms.assetid: acb0ec4f-1846-4fa2-98c2-2081b52a8260
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c216197fb33a666029429d98761b3219b27b176
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103949056"
---
# <a name="in-string-and-out-string-prototype"></a><span data-ttu-id="180cf-103">\[in, String \] und \[ out, Zeichen folgen \] Prototyp</span><span class="sxs-lookup"><span data-stu-id="180cf-103">\[in, string\] and \[out, string\] Prototype</span></span>

<span data-ttu-id="180cf-104">Der folgende Funktionsprototyp verwendet zwei Parameter: einen \[ [**in**](/windows/desktop/Midl/in), einen [**Zeichen**](/windows/desktop/Midl/string) folgen \] Parameter und einen \[ [**out**](/windows/desktop/Midl/out-idl)- **Zeichen** folgen \] Parameter.</span><span class="sxs-lookup"><span data-stu-id="180cf-104">The following function prototype uses two parameters: an \[[**in**](/windows/desktop/Midl/in), [**string**](/windows/desktop/Midl/string)\] parameter and an \[[**out**](/windows/desktop/Midl/out-idl), **string**\] parameter.</span></span>

``` syntax
void Analyze(
    [in, string]                       *pszInput,
    [out, string, size_is(STRSIZE)]    *pszOutput);
```

<span data-ttu-id="180cf-105">Der erste Parameter ist \[ nur [**in**](/windows/desktop/Midl/in) \] .</span><span class="sxs-lookup"><span data-stu-id="180cf-105">The first parameter is \[[**in**](/windows/desktop/Midl/in)\] only.</span></span> <span data-ttu-id="180cf-106">Diese Eingabe Zeichenfolge wird nur vom Client an den Server übertragen.</span><span class="sxs-lookup"><span data-stu-id="180cf-106">This input string is only transmitted from the client to the server.</span></span> <span data-ttu-id="180cf-107">Der Server verwendet ihn als Grundlage für die weitere Verarbeitung.</span><span class="sxs-lookup"><span data-stu-id="180cf-107">The server uses it as the basis for further processing.</span></span> <span data-ttu-id="180cf-108">Die Zeichenfolge wird nicht geändert und wird vom Client nicht erneut benötigt, sodass Sie nicht an den Client zurückgegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="180cf-108">The string is not modified and is not required again by the client, so it does not have to be returned to the client.</span></span>

<span data-ttu-id="180cf-109">Der zweite Parameter, der die Antwort des Arztes darstellt, ist \[ [](/windows/desktop/Midl/out-idl) \] nur out.</span><span class="sxs-lookup"><span data-stu-id="180cf-109">The second parameter, representing the doctor's response, is \[[**out**](/windows/desktop/Midl/out-idl)\] only.</span></span> <span data-ttu-id="180cf-110">Diese Antwort Zeichenfolge wird nur vom Server an den Client übermittelt.</span><span class="sxs-lookup"><span data-stu-id="180cf-110">This response string is only transmitted from the server to the client.</span></span> <span data-ttu-id="180cf-111">Die Zuordnungs Größe wird bereitgestellt, damit die Server-stubspeicher für Sie Speicher belegen können.</span><span class="sxs-lookup"><span data-stu-id="180cf-111">The allocation size is provided so that the server stubs can allocate memory for it.</span></span> <span data-ttu-id="180cf-112">Da *pszoutput* ein \[ [**ref**](/windows/desktop/Midl/ref) - \] Zeiger ist, muss dem Client vor dem-Befehl ausreichend Arbeitsspeicher für die Zeichenfolge zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="180cf-112">Since *pszOutput* is a \[[**ref**](/windows/desktop/Midl/ref)\] pointer, the client must have sufficient memory allocated for the string before the call.</span></span> <span data-ttu-id="180cf-113">Die Antwort Zeichenfolge wird in diesen Bereich des Arbeitsspeichers geschrieben, wenn die Remote Prozedur zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="180cf-113">The response string is written into this area of memory when the remote procedure returns.</span></span>

 

 