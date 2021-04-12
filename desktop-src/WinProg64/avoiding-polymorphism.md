---
title: Vermeiden von Polymorphie
description: Die neuen Datentypen umfassen die beiden polymorphen Typen int \_ ptr und Long \_ ptr.
ms.assetid: 3d18016d-772c-45bc-8057-7281e71a8707
keywords:
- Polymorphie 64-Bit-Windows-Programmierung
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dec0fd26944d58a9ba0d253da8b8dbcd68156436
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311105"
---
# <a name="avoiding-polymorphism"></a><span data-ttu-id="25da5-104">Vermeiden von Polymorphie</span><span class="sxs-lookup"><span data-stu-id="25da5-104">Avoiding Polymorphism</span></span>

<span data-ttu-id="25da5-105">Die neuen Datentypen umfassen die beiden polymorphen Typen **int \_ ptr** und **Long \_ ptr**.</span><span class="sxs-lookup"><span data-stu-id="25da5-105">The new data types include two polymorphic types, **INT\_PTR** and **LONG\_PTR**.</span></span> <span data-ttu-id="25da5-106">Bei 32-Bit-Fenstern wird das **int- \_ ptr** **int** und der **lange \_ ptr** -Wert **Long** zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="25da5-106">On 32-bit Windows, the **INT\_PTR** maps to **int** and the **LONG\_PTR** maps to **long**.</span></span> <span data-ttu-id="25da5-107">Bei 64-Bit-Fenstern werden beide Typen dem systeminternen **\_ \_ Int64** -Typ zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="25da5-107">On 64-bit Windows, both types map to the **\_\_int64** intrinsic type.</span></span> <span data-ttu-id="25da5-108">Der mittlerer l-Compiler unterstützt diese Typen für Remote Prozedur Aufrufe, aber es gibt eine inhärente Einschränkung, die Sie berücksichtigen müssen, wenn Sie in einer verteilten Umgebung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25da5-108">The MIDL compiler supports these types for remote procedure calls, but there is an inherent limitation that you must keep in mind when using them in a distributed environment.</span></span> <span data-ttu-id="25da5-109">Stellen Sie sicher, dass Sie Ihren Code entsprechend kommentieren.</span><span class="sxs-lookup"><span data-stu-id="25da5-109">Be sure to comment your code accordingly.</span></span>

<span data-ttu-id="25da5-110">Unabhängig von der Platt Form Größe ist die Wire-Größe dieser polymorphen Typen immer 32 Bits.</span><span class="sxs-lookup"><span data-stu-id="25da5-110">Regardless of the platform size, the wire size of these polymorphic types is always 32 bits.</span></span> <span data-ttu-id="25da5-111">Wenn das Marshalling bei 64-Bit-Fenstern durchgeführt wird, erweitert das Lauf Zeit Bibliotheks Zeichen signierte Werte und weist der höherwertigen Bytes für einen Wert ohne Vorzeichen NULL zu.</span><span class="sxs-lookup"><span data-stu-id="25da5-111">When unmarshaling on 64-bit Windows, the run-time library sign extends signed values and assigns zero to the high-order bytes for an unsigned value.</span></span> <span data-ttu-id="25da5-112">Wenn Sie einen 64-Bit-Wert für die Übertragung platzieren, verkürzt die Laufzeit die höherwertigen Bytes.</span><span class="sxs-lookup"><span data-stu-id="25da5-112">When putting a 64-bit value on the wire, the run time truncates the high-order bytes.</span></span> <span data-ttu-id="25da5-113">Daher können nur die 32-Bit-Werte in niedriger Reihenfolge verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="25da5-113">Thus, only the low-order 32-bit values are usable.</span></span>

<span data-ttu-id="25da5-114">Verwenden Sie die polymorphen Typen nur, wenn dies für das Portieren erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="25da5-114">Use the polymorphic types only when necessary for porting.</span></span> <span data-ttu-id="25da5-115">Verwenden Sie für neue Schnittstellen die systeminternen ganzzahligen Typen **\_ \_ Int32** und **\_ \_ Int64**, oder verwenden Sie einen Zeigertyp oder ein Kontext Handle, je nachdem, welcher Typ für die übertragene Art von Daten am besten geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="25da5-115">For new interfaces, use the MIDL intrinsic integer types **\_\_int32** and **\_\_int64**, or use a pointer type or context handle, whichever is most appropriate for the kind of data being transferred.</span></span>

<span data-ttu-id="25da5-116">Der 64-Bit-Compiler unterstützt eine neue polymorphe intrinsische **\_ \_ int3264**.</span><span class="sxs-lookup"><span data-stu-id="25da5-116">The 64-bit compiler supports a new polymorphic intrinsic **\_\_int3264**.</span></span> <span data-ttu-id="25da5-117">Dieser Typ wurde ebenfalls entwickelt, um das Portieren zu unterstützen, in diesem Fall, um die **uint- \_ ptr** -Typen transparent zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="25da5-117">Again, this type was developed to support porting efforts, in this case to support the **UINT\_PTR** types transparently.</span></span> <span data-ttu-id="25da5-118">(Eine andere intrinsische, **\_ \_ long3264**-Unterstützung unterstützt den **ulong \_ ptr** -Typ.) Verwenden Sie **\_ \_ int3264** nicht direkt. verwenden Sie den **int- \_ ptr** -Typ, wenn Sie für Portierungs Gründe einen polymorphen Typ benötigen.</span><span class="sxs-lookup"><span data-stu-id="25da5-118">(Another intrinsic, **\_\_long3264**, will support the **ULONG\_PTR** type.) Do not use **\_\_int3264** directly; use the **INT\_PTR** type when you need a polymorphic type for porting reasons.</span></span>

 

 




