---
title: Strukturierte Speicherzugriffs Modi
description: Mechanismen zum Steuern des gleichzeitigen Zugriffs auf ein Objekt, von mehreren Prozessen und Benutzern, sind von entscheidender Bedeutung.
ms.assetid: 2d524c2b-f2b4-49f2-9be8-2037846eb9e9
keywords:
- Strukturierter Speicherplatz Halter-STG, Grundlagen, API-Funktionen, Flags für den Zugriff
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2e46a231cb5168d15564f0b86b064c8bfd19e38
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/16/2019
ms.locfileid: "106339190"
---
# <a name="structured-storage-access-modes"></a><span data-ttu-id="e131c-104">Strukturierte Speicherzugriffs Modi</span><span class="sxs-lookup"><span data-stu-id="e131c-104">Structured Storage Access Modes</span></span>

<span data-ttu-id="e131c-105">Mechanismen zum Steuern des gleichzeitigen Zugriffs auf ein Objekt, von mehreren Prozessen und Benutzern, sind von entscheidender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="e131c-105">Mechanisms for controlling simultaneous access to an object, by multiple processes and users, are essential.</span></span> <span data-ttu-id="e131c-106">COM bietet diese Mechanismen durch Definieren von Zugriffs Modi für Speicher-und Streamobjekte.</span><span class="sxs-lookup"><span data-stu-id="e131c-106">COM provides these mechanisms by defining access modes for both storage and stream objects.</span></span> <span data-ttu-id="e131c-107">Der für ein übergeordnete Speicher Objekt angegebene Zugriffsmodus wird von seinen untergeordneten Elementen geerbt, Sie können jedoch auch zusätzliche Einschränkungen für den untergeordneten Speicher oder Datenstrom platzieren.</span><span class="sxs-lookup"><span data-stu-id="e131c-107">The access mode specified for a parent storage object is inherited by its children, though you can place additional restrictions on the child storage or stream.</span></span> <span data-ttu-id="e131c-108">Ein gespeichertes Speicher-oder Datenstrom Objekt kann im gleichen Modus oder in einem stärker eingeschränkten Modus geöffnet werden als das übergeordnete Objekt, aber es kann nicht in einem weniger eingeschränkten Modus geöffnet werden als das übergeordnete Element.</span><span class="sxs-lookup"><span data-stu-id="e131c-108">A nested storage or stream object can be opened in the same mode or in a more restricted mode than that of its parent, but it cannot be opened in a less restricted mode than that of its parent.</span></span>

<span data-ttu-id="e131c-109">Sie geben Zugriffs Modi mithilfe der Werte an, die in [**STGM-Konstanten**](stgm-constants.md)aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="e131c-109">You specify access modes by using the values listed in [**STGM Constants**](stgm-constants.md).</span></span> <span data-ttu-id="e131c-110">Diese Werte dienen als Flags, die als Argumente an Methoden in der [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) -Schnittstelle und den zugehörigen API-Funktionen übermittelt werden.</span><span class="sxs-lookup"><span data-stu-id="e131c-110">These values serve as flags to be passed as arguments to methods in the [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage) interface and associated API functions.</span></span> <span data-ttu-id="e131c-111">In der Regel werden mehrere Flags im *grsmode*-Parameter mit einem booleschen **oder** -Vorgang kombiniert.</span><span class="sxs-lookup"><span data-stu-id="e131c-111">Typically, several flags are combined in the parameter *grfMode*, using a Boolean **OR** operation.</span></span>

<span data-ttu-id="e131c-112">Die Flags fallen in sechs Gruppen.</span><span class="sxs-lookup"><span data-stu-id="e131c-112">The flags fall into six groups.</span></span> <span data-ttu-id="e131c-113">Es kann immer nur ein Flag aus jeder Gruppe angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="e131c-113">Only one flag from each group can be specified at a time:</span></span>

-   [<span data-ttu-id="e131c-114">Transaktionsflags</span><span class="sxs-lookup"><span data-stu-id="e131c-114">Transaction Flags</span></span>](transaction-flags.md)
-   [<span data-ttu-id="e131c-115">Speichererstellungsflags</span><span class="sxs-lookup"><span data-stu-id="e131c-115">Storage Creation Flags</span></span>](storage-creation-flags.md)
-   [<span data-ttu-id="e131c-116">Temporäre erstellungsflags</span><span class="sxs-lookup"><span data-stu-id="e131c-116">Temporary Creation Flags</span></span>](temporary-creation-flags.md)
-   [<span data-ttu-id="e131c-117">Prioritätsflags</span><span class="sxs-lookup"><span data-stu-id="e131c-117">Priority Flags</span></span>](priority-flags.md)
-   [<span data-ttu-id="e131c-118">Zugriffs Berechtigungs Flags</span><span class="sxs-lookup"><span data-stu-id="e131c-118">Access Permission Flags</span></span>](access-permission-flags.md)
-   [<span data-ttu-id="e131c-119">Shared Access-Flags</span><span class="sxs-lookup"><span data-stu-id="e131c-119">Shared Access Flags</span></span>](shared-access-flags.md)

 

 




