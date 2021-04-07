---
description: Frame Step-Eigenschaften Satz
ms.assetid: 01abe1fe-fc2f-44cb-9546-45a8d682a179
title: Frame Step-Eigenschaften Satz
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f503a38a2f548e0df0a6e88b3ae7afaebdd8cd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "103746640"
---
# <a name="frame-stepping-property-set"></a><span data-ttu-id="ce0a5-103">Frame Step-Eigenschaften Satz</span><span class="sxs-lookup"><span data-stu-id="ce0a5-103">Frame Stepping Property Set</span></span>

<span data-ttu-id="ce0a5-104">Decoderer, die Frame-exakte Suchvorgänge unter Microsoft DirectShow implementieren, müssen den "am \_ kspropsetid"- \_ framestep-Eigenschafts Satz implementieren, der in Verbindung mit der [**ivideoframestep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) -Schnittstelle verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-104">Decoders that implement frame-accurate seeking under Microsoft DirectShow must implement the AM\_KSPROPSETID\_FrameStep property set, which is used in conjunction with the [**IVideoFrameStep**](/windows/desktop/api/Strmif/nn-strmif-ivideoframestep) interface.</span></span>



|                   |                            |
|-------------------|----------------------------|
| <span data-ttu-id="ce0a5-105">Eigenschaftensatz-GUID</span><span class="sxs-lookup"><span data-stu-id="ce0a5-105">Property Set GUID</span></span> | <span data-ttu-id="ce0a5-106">AM \_ kspropabtid- \_ framestep</span><span class="sxs-lookup"><span data-stu-id="ce0a5-106">AM\_KSPROPSETID\_FrameStep</span></span> |



 



| <span data-ttu-id="ce0a5-107">Eigenschafts-ID</span><span class="sxs-lookup"><span data-stu-id="ce0a5-107">Property ID</span></span>                              | <span data-ttu-id="ce0a5-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ce0a5-108">Description</span></span>                                                                                                                                                                     |
|------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce0a5-109">AM- \_ Eigenschafts \_ framestep- \_ Schritt</span><span class="sxs-lookup"><span data-stu-id="ce0a5-109">AM\_PROPERTY\_FRAMESTEP\_STEP</span></span>            | <span data-ttu-id="ce0a5-110">Weist den Decoder an, einen Schritt Vorgang zu starten, und übergibt eine [**am \_ Property \_ framestep**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) -Struktur, die die Anzahl von Schritten angibt.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-110">Instructs the decoder to begin a step operation and passes an [**AM\_PROPERTY\_FRAMESTEP**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-am_framestep_step) structure that specifies the number of steps.</span></span>            |
| <span data-ttu-id="ce0a5-111">AM \_ Eigenschaften \_ framestep \_ Abbrechen</span><span class="sxs-lookup"><span data-stu-id="ce0a5-111">AM\_PROPERTY\_FRAMESTEP\_CANCEL</span></span>          | <span data-ttu-id="ce0a5-112">Weist den Decoder an, den aktuellen Schritt Vorgang abzubrechen.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-112">Instructs the decoder to cancel the current step operation.</span></span> <span data-ttu-id="ce0a5-113">Dieser Eigenschaft sind keine Instanzdaten zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-113">No instance data is associated with this property.</span></span>                                                                  |
| <span data-ttu-id="ce0a5-114">AM, \_ Eigenschaften \_ framestep, \_ canstep</span><span class="sxs-lookup"><span data-stu-id="ce0a5-114">AM\_PROPERTY\_FRAMESTEP\_CANSTEP</span></span>         | <span data-ttu-id="ce0a5-115">Der Decoder gibt S \_ OK für diese Anweisung zurück, um anzugeben, dass er Frame-Stepping ausführen kann, \_ andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-115">The decoder returns S\_OK on this instruction to indicate that it can perform frame stepping, S\_FALSE otherwise.</span></span> <span data-ttu-id="ce0a5-116">Wenn diese Eigenschaft festgelegt ist, werden keine Instanzdaten übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-116">No instance data is passed when this property is set.</span></span>         |
| <span data-ttu-id="ce0a5-117">AM \_ Property \_ framestep \_ canstepmultiple</span><span class="sxs-lookup"><span data-stu-id="ce0a5-117">AM\_PROPERTY\_FRAMESTEP\_CANSTEPMULTIPLE</span></span> | <span data-ttu-id="ce0a5-118">Der Decoder gibt s \_ OK für diese Anweisung zurück, um anzugeben, dass er mehrere Frames gleichzeitig ausführen kann, \_ andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-118">The decoder returns S\_OK on this instruction to indicate that it can step multiple frames at a time, S\_FALSE otherwise.</span></span> <span data-ttu-id="ce0a5-119">Wenn diese Eigenschaft festgelegt ist, werden keine Instanzdaten übermittelt.</span><span class="sxs-lookup"><span data-stu-id="ce0a5-119">No instance data is passed when this property is set.</span></span> |



 

## <a name="related-topics"></a><span data-ttu-id="ce0a5-120">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="ce0a5-120">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce0a5-121">Eigenschaftensätze</span><span class="sxs-lookup"><span data-stu-id="ce0a5-121">Property Sets</span></span>](property-sets.md)
</dt> </dl>

 

 



