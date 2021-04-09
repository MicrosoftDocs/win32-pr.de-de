---
title: Ienumtfrenderingmarkup-Schnittstelle
description: Die ienumtfrenderingmarkup-Schnittstelle wird von TSF Manager implementiert und von Anwendungen verwendet. Diese Schnittstelle kann von itfcontextrenderingmarkup GetRenderingMarkup abgerufen werden und listet die renderingmarkup-Informationen auf.
ms.assetid: 6062a6f5-f973-4cd5-94d3-05aa418e0198
keywords:
- Ienumtfrenderingmarkup Interface Text Services-Framework
- Ienumtfrenderingmarkup Interface Text Services-Framework, beschrieben
topic_type:
- apiref
api_name:
- IEnumTfRenderingMarkup
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 3005c8fe37a26b11f5155b639f8c151cf59c2cf0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "104039401"
---
# <a name="ienumtfrenderingmarkup-interface"></a><span data-ttu-id="ed25e-106">Ienumtfrenderingmarkup-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="ed25e-106">IEnumTfRenderingMarkup interface</span></span>

<span data-ttu-id="ed25e-107">Die **ienumtfrenderingmarkup** -Schnittstelle wird von TSF Manager implementiert und von Anwendungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="ed25e-107">The **IEnumTfRenderingMarkup** interface is implemented by TSF Manager and used by applications.</span></span> <span data-ttu-id="ed25e-108">Diese Schnittstelle kann von [itfcontextrenderingmarkup:: GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) abgerufen werden und listet die renderingmarkup-Informationen auf.</span><span class="sxs-lookup"><span data-stu-id="ed25e-108">This interface can be retrieved by [ITfContextRenderingMarkup::GetRenderingMarkup](itfcontextrenderingmarkup-getrenderingmarkup.md) and enumerates the rendering markup information.</span></span>



| <span data-ttu-id="ed25e-109">Ienumtfrenderingmarkup-Methoden</span><span class="sxs-lookup"><span data-stu-id="ed25e-109">IEnumTfRenderingMarkup methods</span></span>            | <span data-ttu-id="ed25e-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ed25e-110">Description</span></span>                                                                                                                                            |
|-------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ed25e-111">Klonen</span><span class="sxs-lookup"><span data-stu-id="ed25e-111">Clone</span></span>](ienumtfrenderingmarkup-clone.md) | <span data-ttu-id="ed25e-112">Die **ienumtfrenderingmarkup:: Clone** -Methode erstellt eine Kopie des Enumeratorobjekts.</span><span class="sxs-lookup"><span data-stu-id="ed25e-112">The **IEnumTfRenderingMarkup::Clone** method creates a copy of the enumerator object.</span></span>                                                                  |
| [<span data-ttu-id="ed25e-113">Nächste</span><span class="sxs-lookup"><span data-stu-id="ed25e-113">Next</span></span>](ienumtfrenderingmarkup-next.md)   | <span data-ttu-id="ed25e-114">Die **ienumtfrenderingmarkup:: Next** -Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.</span><span class="sxs-lookup"><span data-stu-id="ed25e-114">The **IEnumTfRenderingMarkup::Next** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |
| [<span data-ttu-id="ed25e-115">Zurücksetzen</span><span class="sxs-lookup"><span data-stu-id="ed25e-115">Reset</span></span>](ienumtfrenderingmarkup-reset.md) | <span data-ttu-id="ed25e-116">Die **ienumtfrenderingmarkup:: Reset** -Methode setzt das Enumeratorobjekt zurück, indem die aktuelle Position an den Anfang der enumerationssequenz verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="ed25e-116">The **IEnumTfRenderingMarkup::Reset** method resets the enumerator object by moving the current position to the beginning of the enumeration sequence.</span></span> |
| [<span data-ttu-id="ed25e-117">Skip</span><span class="sxs-lookup"><span data-stu-id="ed25e-117">Skip</span></span>](ienumtfrenderingmarkup-skip.md)   | <span data-ttu-id="ed25e-118">Die **ienumtfrenderingmarkup:: Skip** -Methode ruft die angegebene Anzahl von Elementen in der Enumerationsfolge von der aktuellen Position ab.</span><span class="sxs-lookup"><span data-stu-id="ed25e-118">The **IEnumTfRenderingMarkup::Skip** method obtains, from the current position, the specified number of elements in the enumeration sequence.</span></span>          |



 

## <a name="members"></a><span data-ttu-id="ed25e-119">Member</span><span class="sxs-lookup"><span data-stu-id="ed25e-119">Members</span></span>

<span data-ttu-id="ed25e-120">Die **ienumtfrenderingmarkup** -Schnittstelle erbt von der [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) -Schnittstelle, verfügt jedoch nicht über zusätzliche Member.</span><span class="sxs-lookup"><span data-stu-id="ed25e-120">The **IEnumTfRenderingMarkup** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface but does not have additional members.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed25e-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ed25e-121">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="ed25e-122">Diese Schnittstelle befindet sich derzeit nicht in den öffentlichen Header Dateien.</span><span class="sxs-lookup"><span data-stu-id="ed25e-122">This interface is not currently in the public header files.</span></span> <span data-ttu-id="ed25e-123">Um diese API verwenden zu können, müssen Sie den [Prototyp](prototypes.md)als Mittelpunkt kompilieren.</span><span class="sxs-lookup"><span data-stu-id="ed25e-123">To use this API, you must MIDL-compile the [prototype](prototypes.md).</span></span>

 

 

 