---
title: Top-Level und eingebettete Zeiger
description: Um zu verstehen, wie Zeiger und die zugehörigen Datenelemente in Microsoft RPC zugeordnet werden, müssen Sie zwischen Zeigern der obersten Ebene und eingebetteten Zeigern unterscheiden.
ms.assetid: 217b9200-827c-4d36-9412-5e65858b8a97
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee84fcecdb70c67d7c99b4bbd3753c244a87cd07
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "104471676"
---
# <a name="top-level-and-embedded-pointers"></a><span data-ttu-id="7482e-103">Top-Level und eingebettete Zeiger</span><span class="sxs-lookup"><span data-stu-id="7482e-103">Top-Level and Embedded Pointers</span></span>

<span data-ttu-id="7482e-104">Um zu verstehen, wie Zeiger und die zugehörigen Datenelemente in Microsoft RPC zugeordnet werden, müssen Sie zwischen *Zeigern der obersten Ebene* und *eingebetteten Zeigern* unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="7482e-104">To understand how pointers and their associated data elements are allocated in Microsoft RPC, you have to differentiate between *top-level pointers* and *embedded pointers*.</span></span> <span data-ttu-id="7482e-105">Es ist auch hilfreich, auf den Satz aller Zeiger zu verweisen, die keine Zeiger auf oberster Ebene sind.</span><span class="sxs-lookup"><span data-stu-id="7482e-105">It is also useful to refer to the set of all pointers that are not top-level pointers.</span></span>

<span data-ttu-id="7482e-106">*Zeiger der obersten Ebene* sind solche, die als Parameternamen in Funktionsprototypen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="7482e-106">*Top-level pointers* are those that are specified as the names of parameters in function prototypes.</span></span> <span data-ttu-id="7482e-107">Zeiger der obersten Ebene und ihre Verweise werden immer auf dem Server zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="7482e-107">Top-level pointers and their referents are always allocated on the server.</span></span>

<span data-ttu-id="7482e-108">*Eingebettete Zeiger* sind Zeiger, die in Datenstrukturen wie Arrays, Strukturen und Unions eingebettet sind.</span><span class="sxs-lookup"><span data-stu-id="7482e-108">*Embedded pointers* are pointers that are embedded in data structures such as arrays, structures, and unions.</span></span> <span data-ttu-id="7482e-109">Wenn eingebettete Zeiger nur Ausgaben in einen Puffer schreiben und bei Eingaben NULL sind, kann die Serveranwendung ihre Werte in einen nicht-NULL-Wert ändern.</span><span class="sxs-lookup"><span data-stu-id="7482e-109">When embedded pointers only write output to a buffer and are null on input, the server application can change their values to non-null.</span></span> <span data-ttu-id="7482e-110">In diesem Fall weisen die clientstubdaten neuen Arbeitsspeicher für diese Daten zu.</span><span class="sxs-lookup"><span data-stu-id="7482e-110">In this case, the client stubs allocate new memory for this data.</span></span>

<span data-ttu-id="7482e-111">Wenn der eingebettete Zeiger auf dem Client vor dem-Befehl nicht NULL ist, wird der Client bei der Rückgabe keinen Arbeitsspeicher zuordnen.</span><span class="sxs-lookup"><span data-stu-id="7482e-111">If the embedded pointer is not null on the client before the call, the stubs do not allocate memory on the client on return.</span></span> <span data-ttu-id="7482e-112">Stattdessen versuchen die stubvorgänge, den dem eingebetteten Zeiger zugeordneten Arbeitsspeicher auf dem Client zu schreiben, der diesem Zeiger zugeordnet ist, wobei die bereits vorhandenen Daten überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="7482e-112">Instead, the stubs attempt to write the memory associated with the embedded pointer into the existing memory on the client associated with that pointer, overwriting the data already there.</span></span>

> [!Note]  
> <span data-ttu-id="7482e-113">Für Daten, die aus einem Puffer gelesen oder geschrieben werden und der die Puffergröße nicht angibt, muss die Ausgabe Länge kleiner oder gleich der Eingabe Länge sein.</span><span class="sxs-lookup"><span data-stu-id="7482e-113">For data read from or writen to a buffer, and which does not specify the buffer size, output length must be less than or equal to input length.</span></span> <span data-ttu-id="7482e-114">Eine RPC-Ausnahme wird ausgelöst, wenn ein Überlauf erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="7482e-114">An RPC exception is raised when overflow is detected.</span></span> <span data-ttu-id="7482e-115">Für Zeichen folgen Daten wird die Ausgabe Länge durch die Überprüfung der Länge der Eingabe Zeichenfolge bestimmt.</span><span class="sxs-lookup"><span data-stu-id="7482e-115">For string data, output length is determined by checking length of the input string.</span></span> <span data-ttu-id="7482e-116">Daher dürfen Ausgabe Zeichenfolgen die Länge von Eingabe Zeichenfolgen nicht überschreiten</span><span class="sxs-lookup"><span data-stu-id="7482e-116">Therefore, output strings cannot exceed length of input strings.</span></span> <span data-ttu-id="7482e-117">Die Best Practices-Anleitung besteht darin, dies zu vermeiden, indem Sie immer einen Größen spezifischen Parameter einschließen, um die Größe des Puffers anzugeben.</span><span class="sxs-lookup"><span data-stu-id="7482e-117">Best practice guidance is to avoid this by always including a size-specified parameter to indicate size of the buffer.</span></span>

 

<span data-ttu-id="7482e-118">Eingebettete schreibgeschützte Zeiger werden unter [Kombinieren von Zeiger-und direktionalen Attributen](combining-pointer-and-directional-attributes.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="7482e-118">Embedded write-only pointers are discussed in [Combining Pointer and Directional Attributes](combining-pointer-and-directional-attributes.md).</span></span>

<span data-ttu-id="7482e-119">Der Begriff *nontop-Level-Zeiger* bezieht sich auf alle Zeiger, die nicht als Parameternamen im Funktionsprototyp angegeben werden, einschließlich eingebetteter Zeiger und mehrerer Ebenen von gruppierten Zeigern.</span><span class="sxs-lookup"><span data-stu-id="7482e-119">The term *nontop-level pointers* refers to all pointers that are not specified as parameter names in the function prototype, including both embedded pointers and multiple levels of nested pointers.</span></span>

 

 




