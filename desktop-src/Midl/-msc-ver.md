---
title: /msc_ver Schalter
description: Der Schalter "/MSC \_ ver" wird verwendet, um es mittlerer l zu ermöglichen, Code zu generieren, der Optimierungen für verschiedene Versionen von Microsoft C/C++-Compilern enthält.
ms.assetid: cdcb8f3e-e791-44c2-8bea-e77f94cc1682
keywords:
- /msc_ver-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /msc_ver
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3620b3c8ffb1315a4d34eb0b4b2497c1cb3d805
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103857544"
---
# <a name="msc_ver-switch"></a><span data-ttu-id="8a17a-104">/MSC \_ ver-Schalter</span><span class="sxs-lookup"><span data-stu-id="8a17a-104">/msc\_ver switch</span></span>

<span data-ttu-id="8a17a-105">Der Schalter " **/MSC \_ ver** " wird verwendet, um es mittlerer l zu ermöglichen, Code zu generieren, der Optimierungen für verschiedene Versionen von Microsoft C/C++-Compilern enthält.</span><span class="sxs-lookup"><span data-stu-id="8a17a-105">The **/msc\_ver** switch is used to allow MIDL to generate code that includes optimizations for different versions of Microsoft C/C++ compilers.</span></span>

``` syntax
midl /msc_ver version_number
```

## <a name="switch-options"></a><span data-ttu-id="8a17a-106">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="8a17a-106">Switch Options</span></span>

<dl> <dt>

<span data-ttu-id="8a17a-107">*Versions \_ Nummer*</span><span class="sxs-lookup"><span data-stu-id="8a17a-107">*version\_number*</span></span> 
</dt> <dd>

<span data-ttu-id="8a17a-108">Gibt eine ganzzahlige Versionsnummer des Microsoft Visual C++ Compilers an, der verwendet wird, um die Client-und serverstubfunktionen der verteilten Anwendung zu kompilieren.</span><span class="sxs-lookup"><span data-stu-id="8a17a-108">Specifies an integer version number of the Microsoft Visual C++ compiler that will be used to compile the client and server stubs of the distributed application.</span></span> <span data-ttu-id="8a17a-109">Die Standard Versionsnummer ist 1100, was Visual C++ Version 5,0 entspricht.</span><span class="sxs-lookup"><span data-stu-id="8a17a-109">The default version number is 1100, which corresponds to Visual C++ version 5.0.</span></span> <span data-ttu-id="8a17a-110">Die Versionsnummer 1200 entspricht Visual C++ Version 6,0 usw.</span><span class="sxs-lookup"><span data-stu-id="8a17a-110">The version number 1200 corresponds to Visual C++ version 6.0, and so on.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="8a17a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8a17a-111">Remarks</span></span>

<span data-ttu-id="8a17a-112">Bestimmte Versions Werte von 1100 oder höher bewirken, dass der Mittell-Compiler Code mithilfe der **\_ \_ declspec (UUID ())** -Direktive generiert.</span><span class="sxs-lookup"><span data-stu-id="8a17a-112">In particular, version values of 1100 or greater cause the MIDL compiler to generate code utilizing the **\_\_declspec(uuid())** directive.</span></span> <span data-ttu-id="8a17a-113">Außerdem werden Makros aktiviert, die die Anweisungen **\_ \_ declspec (selectany)** und **\_ \_ declspec (novtable)** verwenden.</span><span class="sxs-lookup"><span data-stu-id="8a17a-113">It also activates macros that use the **\_\_declspec(selectany)** and **\_\_declspec(novtable)** directives.</span></span>

 

 




