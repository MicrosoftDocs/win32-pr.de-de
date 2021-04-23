---
description: Frame Stepping-Eigenschaftensatz
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Frame Stepping-Eigenschaftensatz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e0ccd79feda0e5e2e537390fe5598822fb3787f6
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908448"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="43377-103">Frame Stepping-Eigenschaftensatz</span><span class="sxs-lookup"><span data-stu-id="43377-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="43377-104">Decoder, die framegenaue Suchfunktionen unter Microsoft DirectShow implementieren, müssen den AM \_ KSPROPSETID \_ FrameStep-Eigenschaftensatz implementieren, der in Verbindung mit der [**IVideoFrameStep-Schnittstelle**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="43377-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



| <span data-ttu-id="43377-105">Bezeichnung</span><span class="sxs-lookup"><span data-stu-id="43377-105">Label</span></span> | <span data-ttu-id="43377-106">Wert</span><span class="sxs-lookup"><span data-stu-id="43377-106">Value</span></span> |
|-------------------|----------------------------|
| <span data-ttu-id="43377-107">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="43377-107">Property Set GUID</span></span> | <span data-ttu-id="43377-108">AM \_ KSPROPSETID \_ FrameStep</span><span class="sxs-lookup"><span data-stu-id="43377-108">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="43377-109">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="43377-109">Property ID</span></span>                              | <span data-ttu-id="43377-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="43377-110">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43377-111">AM \_ PROPERTY \_ FRAMESTEP \_ STEP</span><span class="sxs-lookup"><span data-stu-id="43377-111">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="43377-112">Weist den Decoder an, einen Schrittvorgang zu starten, und übergibt eine [**AM \_ PROPERTY \_ FRAMESTEP-Struktur,**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) die die Anzahl der Schritte angibt.</span><span class="sxs-lookup"><span data-stu-id="43377-112">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="43377-113">AM \_ PROPERTY \_ FRAMESTEP \_ CANCEL</span><span class="sxs-lookup"><span data-stu-id="43377-113">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="43377-114">Weist den Decoder an, den aktuellen Schrittvorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="43377-114">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="43377-115">Dieser Eigenschaft sind keine Instanzdaten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="43377-115">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="43377-116">AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEP</span><span class="sxs-lookup"><span data-stu-id="43377-116">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="43377-117">Der Decoder gibt S \_ OK für diese Anweisung zurück, um anzugeben, dass die Frameschritte ausgeführt werden können, \_ andernfalls S FALSE.</span><span class="sxs-lookup"><span data-stu-id="43377-117">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="43377-118">Es werden keine Instanzdaten übergeben, wenn diese Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="43377-118">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="43377-119">AM \_ PROPERTY \_ FRAMESTEP \_ CANSTEPMULTIPLE</span><span class="sxs-lookup"><span data-stu-id="43377-119">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="43377-120">Der Decoder gibt S \_ OK für diese Anweisung zurück, um anzugeben, dass mehrere Frames gleichzeitig schrittweise sind, \_ andernfalls S FALSE.</span><span class="sxs-lookup"><span data-stu-id="43377-120">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="43377-121">Es werden keine Instanzdaten übergeben, wenn diese Eigenschaft festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="43377-121">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="43377-122">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="43377-122">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="43377-123">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="43377-123">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



