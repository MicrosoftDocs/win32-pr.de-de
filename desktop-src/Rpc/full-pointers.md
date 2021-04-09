---
title: Vollständige Zeiger
description: Im Gegensatz zu eindeutigen Zeigern unterstützen vollständige Zeiger Aliasing.
ms.assetid: 38023942-a4c2-4de7-b7d5-10d508cf083b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 18687b496ddd28dca9e70afca8deafb18774500a
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "103948845"
---
# <a name="full-pointers"></a><span data-ttu-id="5a7c9-103">Vollständige Zeiger</span><span class="sxs-lookup"><span data-stu-id="5a7c9-103">Full Pointers</span></span>

<span data-ttu-id="5a7c9-104">Im Gegensatz zu [eindeutigen](unique-pointers.md) Zeigern unterstützen vollständige Zeiger Aliasing.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-104">Unlike [unique](unique-pointers.md) pointers, full pointers support aliasing.</span></span> <span data-ttu-id="5a7c9-105">Dies bedeutet, dass mehrere Zeiger auf dieselben Daten verweisen können, wie in der folgenden Abbildung dargestellt:</span><span class="sxs-lookup"><span data-stu-id="5a7c9-105">This means that multiple pointers can refer to the same data, as shown in the following figure:</span></span>

![zwei Zeiger, die auf dieselben Daten verweisen](images/prog-a02.png)

<span data-ttu-id="5a7c9-107">Ein vollständiger Zeiger weist die folgenden Eigenschaften auf:</span><span class="sxs-lookup"><span data-stu-id="5a7c9-107">A full pointer has the following characteristics:</span></span>

-   <span data-ttu-id="5a7c9-108">Der Wert kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-108">It can have the value null.</span></span>
-   <span data-ttu-id="5a7c9-109">Sie kann während des-Aufrufes von NULL in ungleich NULL wechseln.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-109">It can change from null to non-null during the call.</span></span> <span data-ttu-id="5a7c9-110">Wenn der Wert in einen nicht-NULL-Wert geändert wird, ordnet der Clientstub der Rückgabe einen neuen Arbeitsspeicher zu.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-110">When the value changes to non-null, the client stub allocates new memory allocated on return.</span></span> <span data-ttu-id="5a7c9-111">Das Client Programm sollte diesen Arbeitsspeicher freigeben, bevor er beendet wird.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-111">The client program should free this memory before it terminates.</span></span>
-   <span data-ttu-id="5a7c9-112">Sie kann während des Aufrufes von ungleich NULL zu NULL wechseln.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-112">It can change from non-null to null during the call.</span></span> <span data-ttu-id="5a7c9-113">Wenn der Wert in NULL geändert wird, ist die Anwendung dafür verantwortlich, den Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-113">When the value changes to null, the application is responsible for freeing the memory.</span></span>
-   <span data-ttu-id="5a7c9-114">Der Wert kann von einem nicht-NULL-Wert in einen anderen Wert geändert werden.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-114">The value can change from one non-null value to another.</span></span>
-   <span data-ttu-id="5a7c9-115">Auf den Speicher, auf den ein vollständiger Zeiger zeigt, wird möglicherweise ein anderer Zeiger oder Name im Vorgang aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-115">The storage that a full pointer points to may be accessed by another pointer or name in the operation.</span></span>
-   <span data-ttu-id="5a7c9-116">Rückgabe Daten werden in den vorhandenen Speicher geschrieben, wenn der Zeiger nicht den Wert NULL hat.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-116">Return data is written into existing storage if the pointer does not have the value null.</span></span>

<span data-ttu-id="5a7c9-117">Verwenden Sie das \[ [**ptr**](/windows/desktop/Midl/ptr) - \] Attribut, um einen vollständigen Zeiger anzugeben, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="5a7c9-117">Use the \[ [**ptr**](/windows/desktop/Midl/ptr) \] attribute to specify a full pointer, as shown in the following example:</span></span>

``` syntax
/* IDL file */
[ 
  uuid(ba209999-0c6c-11d2-97cf-00c04f8eea45),
  version(1.0)
]
interface FullPtrInterface
{
  void RemoteFn([in,ptr,string]) char *ptrName1,
                [in,ptr,string]  char *ptrName2);
}
```

<span data-ttu-id="5a7c9-118">In diesem Beispiel werden die Parameter *ptrName1* und *ptrName2* als vollständige Zeiger auf eine Zeichenfolge definiert.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-118">In this example the parameters *ptrName1* and *ptrName2* are defined as full pointers to a string.</span></span> <span data-ttu-id="5a7c9-119">Beide Zeiger können auf dieselbe Speicheradresse zeigen, die eine einzelne Zeichenfolge enthält.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-119">It is possible for both pointers to point to the same memory address containing a single string.</span></span>

<span data-ttu-id="5a7c9-120">\[**ptr** \] ist beim Bereitstellen von Aliasing-Unterstützung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-120">\[**ptr**\] is required when providing aliasing support.</span></span> <span data-ttu-id="5a7c9-121">Da es jedoch die meiste Verarbeitung aller in RPC verfügbaren Zeiger erfordert, wird es für die meisten Anwendungen nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="5a7c9-121">However, since it requires the most processing of all the pointers available in RPC, it is not recommended for most applications.</span></span>

 

 