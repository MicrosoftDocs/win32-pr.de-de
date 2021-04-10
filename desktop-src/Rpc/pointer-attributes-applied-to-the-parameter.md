---
title: Zeiger Attribute, die auf den Parameter angewendet werden
description: Jedes Zeiger Attribut (\ Ref \, \ Unique \ und \ PTR \) verfügt über Eigenschaften, die die Speicher Belegung beeinflussen. In der folgenden Tabelle werden diese Eigenschaften zusammengefasst.
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039437"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a><span data-ttu-id="edb08-104">Zeiger Attribute, die auf den Parameter angewendet werden</span><span class="sxs-lookup"><span data-stu-id="edb08-104">Pointer Attributes Applied to the Parameter</span></span>

<span data-ttu-id="edb08-105">Jedes Zeiger Attribut ( \[ [ref](/windows/desktop/Midl/ref) \] , \[ [Unique](/windows/desktop/Midl/unique) \] und \[ [ptr](/windows/desktop/Midl/ptr) \] ) verfügt über Eigenschaften, die die Speicher Belegung beeinflussen.</span><span class="sxs-lookup"><span data-stu-id="edb08-105">Each pointer attribute (\[ [ref](/windows/desktop/Midl/ref)\], \[ [unique](/windows/desktop/Midl/unique)\], and \[ [ptr](/windows/desktop/Midl/ptr)\]) has characteristics that affect memory allocation.</span></span> <span data-ttu-id="edb08-106">In der folgenden Tabelle werden diese Eigenschaften zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="edb08-106">The following table summarizes these characteristics.</span></span>



| <span data-ttu-id="edb08-107">Zeiger Attribut</span><span class="sxs-lookup"><span data-stu-id="edb08-107">Pointer attribute</span></span>       | <span data-ttu-id="edb08-108">Client</span><span class="sxs-lookup"><span data-stu-id="edb08-108">Client</span></span>                                                                                                                                                                                                            | <span data-ttu-id="edb08-109">Server</span><span class="sxs-lookup"><span data-stu-id="edb08-109">Server</span></span>                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| <span data-ttu-id="edb08-110">Verweis ( \[ **ref** \] )</span><span class="sxs-lookup"><span data-stu-id="edb08-110">Reference (\[**ref**\])</span></span> | <span data-ttu-id="edb08-111">Die Client Anwendung muss zuordnen.</span><span class="sxs-lookup"><span data-stu-id="edb08-111">Client application must allocate.</span></span>                                                                                                                                                                                 | <span data-ttu-id="edb08-112">Spezielle Behandlung **\[ , \]** die nur für nicht auf oberster Ebene basierende Zeiger erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="edb08-112">Special handling needed for **\[out\]**-only nontop-level pointers.</span></span> |
| <span data-ttu-id="edb08-113">Eindeutig ( \[ **eindeutig** \] )</span><span class="sxs-lookup"><span data-stu-id="edb08-113">Unique (\[**unique**\])</span></span> | <span data-ttu-id="edb08-114">Wenn ein Parameter ist, muss die Client Anwendung Wenn eingebettet, kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="edb08-114">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="edb08-115">Wenn Sie von NULL in einen nicht-NULL-Wert wechseln, weist der Clientstub zu. Das Ändern von ungleich NULL in NULL kann zu einem verwaisen führen.</span><span class="sxs-lookup"><span data-stu-id="edb08-115">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |
| <span data-ttu-id="edb08-116">Vollständig ( \[ **ptr** \] )</span><span class="sxs-lookup"><span data-stu-id="edb08-116">Full (\[**ptr**\])</span></span>      | <span data-ttu-id="edb08-117">Wenn ein Parameter ist, muss die Client Anwendung Wenn eingebettet, kann NULL sein.</span><span class="sxs-lookup"><span data-stu-id="edb08-117">If a parameter, the client application must allocate; if embedded, can be null.</span></span> <span data-ttu-id="edb08-118">Wenn Sie von NULL in einen nicht-NULL-Wert wechseln, weist der Clientstub zu. Das Ändern von ungleich NULL in NULL kann zu einem verwaisen führen.</span><span class="sxs-lookup"><span data-stu-id="edb08-118">Changing from null to non-null causes the client stub to allocate; changing from non-null to null can cause orphaning.</span></span><br/> |                                                                     |



 

<span data-ttu-id="edb08-119">Das **\[ ref \]** -Attribut gibt an, dass der Zeiger auf einen gültigen Speicher zeigt.</span><span class="sxs-lookup"><span data-stu-id="edb08-119">The **\[ref\]** attribute indicates that the pointer points to valid memory.</span></span> <span data-ttu-id="edb08-120">Definitionsgemäß muss die Client Anwendung den gesamten Arbeitsspeicher zuordnen, der für die Verweis Zeiger erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="edb08-120">By definition, the client application must allocate all the memory that the reference pointers require.</span></span>

<span data-ttu-id="edb08-121">Der eindeutige Zeiger kann von NULL in einen nicht-NULL-Wert geändert werden.</span><span class="sxs-lookup"><span data-stu-id="edb08-121">The unique pointer can change from null to non-null.</span></span> <span data-ttu-id="edb08-122">Wenn der eindeutige Zeiger von NULL in einen nicht-NULL-Wert geändert wird, wird auf dem Client neuer Arbeitsspeicher zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="edb08-122">If the unique pointer changes from null to non-null, new memory is allocated on the client.</span></span> <span data-ttu-id="edb08-123">Wenn sich der eindeutige Zeiger von einem nicht-NULL-Wert in NULL ändert, kann das verwaisen Ergebnis sein.</span><span class="sxs-lookup"><span data-stu-id="edb08-123">If the unique pointer changes from non-null to null, orphaning can result.</span></span> <span data-ttu-id="edb08-124">Weitere Informationen finden Sie unter Arbeits [Speicher verwaisen](memory-orphaning.md).</span><span class="sxs-lookup"><span data-stu-id="edb08-124">For more information, see [Memory Orphaning](memory-orphaning.md).</span></span>

 

