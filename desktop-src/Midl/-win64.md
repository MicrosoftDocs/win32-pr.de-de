---
title: /Win64-Schalter
description: Der/Win64-Schalter weist den Mittelwert Compiler an, Stub-Dateien oder eine Typbibliotheks Datei für eine 64-Bit-Umgebung zu generieren. Beachten Sie, dass dieser Schalter veraltet ist.
ms.assetid: 6f4780d3-6415-42af-a8ee-3884a8cebe26
keywords:
- /Win64-Schalter-Mittel l
topic_type:
- apiref
api_name:
- /win64
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e61906126607c0a8d4b81ef76805bb4b7e0d4145
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "104312299"
---
# <a name="win64-switch"></a><span data-ttu-id="138b2-104">/Win64-Schalter</span><span class="sxs-lookup"><span data-stu-id="138b2-104">/win64 switch</span></span>

<span data-ttu-id="138b2-105">Der **/Win64** -Schalter weist den Mittelwert Compiler an, Stub-Dateien oder eine Typbibliotheks Datei für eine 64-Bit-Umgebung zu generieren.</span><span class="sxs-lookup"><span data-stu-id="138b2-105">The **/win64** switch directs the MIDL compiler to generate stub files, or a type library file, for a 64-bit environment.</span></span>

> [!Note]  
> <span data-ttu-id="138b2-106">Dieser Schalter ist veraltet.</span><span class="sxs-lookup"><span data-stu-id="138b2-106">This switch is obsolete.</span></span> <span data-ttu-id="138b2-107">Verwenden Sie stattdessen den Schalter " [**/ia64**](-ia64.md) " oder " [**/amd64**](-amd64.md) ".</span><span class="sxs-lookup"><span data-stu-id="138b2-107">Please use the [**/ia64**](-ia64.md) or [**/amd64**](-amd64.md) switch instead.</span></span> <span data-ttu-id="138b2-108">Der Schalter " **/Win64** " entspricht dem Schalter " **/ia64** ".</span><span class="sxs-lookup"><span data-stu-id="138b2-108">The **/win64** switch is equivalent to the **/ia64** switch.</span></span>

 

``` syntax
midl /win64
```

## <a name="switch-options"></a><span data-ttu-id="138b2-109">Optionen wechseln</span><span class="sxs-lookup"><span data-stu-id="138b2-109">Switch Options</span></span>

<span data-ttu-id="138b2-110">Dieser Switch hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="138b2-110">This switch has no parameters.</span></span>

## <a name="remarks"></a><span data-ttu-id="138b2-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="138b2-111">Remarks</span></span>

<span data-ttu-id="138b2-112">Der Schalter **/Win64** entspricht dem Festlegen des [**/env**](-env.md) -Schalters auf Win64.</span><span class="sxs-lookup"><span data-stu-id="138b2-112">The **/win64** switch is equivalent to setting the [**/env**](-env.md) switch to win64.</span></span>

> [!Note]  
> <span data-ttu-id="138b2-113">Es ist nicht möglich, mit MIDL.exe einen 64-Bit-TLB unter Windows 2000 zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="138b2-113">It is not possible to use MIDL.exe to produce a 64bit tlb on Windows 2000.</span></span>

 

## <a name="see-also"></a><span data-ttu-id="138b2-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="138b2-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="138b2-115">**/ENV**</span><span class="sxs-lookup"><span data-stu-id="138b2-115">**/env**</span></span>](-env.md)
</dt> <dt>

[<span data-ttu-id="138b2-116">**/ia64**</span><span class="sxs-lookup"><span data-stu-id="138b2-116">**/ia64**</span></span>](-ia64.md)
</dt> <dt>

[<span data-ttu-id="138b2-117">**/amd64**</span><span class="sxs-lookup"><span data-stu-id="138b2-117">**/amd64**</span></span>](-amd64.md)
</dt> </dl>

 

 




