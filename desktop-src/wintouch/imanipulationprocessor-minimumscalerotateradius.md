---
title: IManipulationProcessor MinimumScaleRotateRadius (Eigenschaft)
description: Gibt an, wie groß die Entfernungs Kontakte in einer Skala oder Drehung sein müssen, um eine Manipulation zu initiieren.
ms.assetid: b4c49f41-c5ea-4c6a-872b-2d982e588b09
keywords:
- MinimumScaleRotateRadius-Eigenschaft, Windows-Fingereingabe
- MinimumScaleRotateRadius-Eigenschaft, Windows Touchscreen, IManipulationProcessor-Schnittstelle
- IManipulationProcessor Interface Windows-Fingereingabe, MinimumScaleRotateRadius (Eigenschaft)
topic_type:
- apiref
api_name:
- IManipulationProcessor.MinimumScaleRotateRadius
- IManipulationProcessor.get_MinimumScaleRotateRadius
- IManipulationProcessor.put_MinimumScaleRotateRadius
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location:
- manipulations.h
ms.openlocfilehash: 502d55e409f58127ddee94f5ba694a109c1ee1cb
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/25/2019
ms.locfileid: "103718618"
---
# <a name="imanipulationprocessorminimumscalerotateradius-property"></a><span data-ttu-id="b8a1c-106">IManipulationProcessor:: MinimumScaleRotateRadius (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="b8a1c-106">IManipulationProcessor::MinimumScaleRotateRadius property</span></span>

<span data-ttu-id="b8a1c-107">Gibt an, wie groß die Entfernungs Kontakte in einer Skala oder Drehung sein müssen, um eine Manipulation zu initiieren.</span><span class="sxs-lookup"><span data-stu-id="b8a1c-107">Specifies how large the distance contacts on a scale or rotate gesture need to be to trigger manipulation.</span></span>

<span data-ttu-id="b8a1c-108">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="b8a1c-108">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8a1c-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="b8a1c-109">Syntax</span></span>


```C++
HRESULT put_MinimumScaleRotateRadius(
  [in]  FLOAT MinimumScaleRotateRadius
);

HRESULT get_MinimumScaleRotateRadius(
  [out] FLOAT *MinimumScaleRotateRadius
);
```



## <a name="property-value"></a><span data-ttu-id="b8a1c-110">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="b8a1c-110">Property value</span></span>

<span data-ttu-id="b8a1c-111">Gibt den minimalen Abstand zwischen Kontakten an, um die Skalierung zu initiieren oder Gesten zu drehen.</span><span class="sxs-lookup"><span data-stu-id="b8a1c-111">Specifies the minimum distance between contacts to trigger scale or rotate gestures.</span></span>

## <a name="error-codes"></a><span data-ttu-id="b8a1c-112">Fehlercodes</span><span class="sxs-lookup"><span data-stu-id="b8a1c-112">Error codes</span></span>

## <a name="remarks"></a><span data-ttu-id="b8a1c-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b8a1c-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="b8a1c-114">Diese Eigenschaft wird in centipixels (hundert Sekunden) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b8a1c-114">This property is set in centipixels (100ths of a pixel).</span></span>

 

<span data-ttu-id="b8a1c-115">Wenn dieser Wert festgelegt wird, ignoriert der Manipulations Prozessor Gesten, die zu klein sind.</span><span class="sxs-lookup"><span data-stu-id="b8a1c-115">Setting this value will make the manipulation processor ignore gestures that have too small of a radius.</span></span> <span data-ttu-id="b8a1c-116">Dies ist hilfreich, wenn Sie verhindern möchten, dass ein Benutzer ein Objekt zu einem zu kleinen Radius bearbeitet.</span><span class="sxs-lookup"><span data-stu-id="b8a1c-116">This is useful if you want to prevent a user from manipulating an object to too small of a radius.</span></span> <span data-ttu-id="b8a1c-117">Wenn Sie z. b. einen Bearbeitungs Prozessor mit einem Kreis verwenden und sicherstellen möchten, dass ein RADIUS größer als 100 Pixel beibehalten wird, legen Sie diesen Wert auf 10000 fest.</span><span class="sxs-lookup"><span data-stu-id="b8a1c-117">For example, if you are using a manipulation processor with a circle and want the ensure that it maintains a radius greater than 100 pixels, you would set this value to 10000.</span></span>

## <a name="examples"></a><span data-ttu-id="b8a1c-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b8a1c-118">Examples</span></span>


```C++
pManip->put_MinimumScaleRotateRadius(4000.0f);  
```



## <a name="see-also"></a><span data-ttu-id="b8a1c-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="b8a1c-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a1c-120">**IManipulationProcessor**</span><span class="sxs-lookup"><span data-stu-id="b8a1c-120">**IManipulationProcessor**</span></span>](/windows/desktop/api/manipulations/nn-manipulations-imanipulationprocessor)
</dt> </dl>

 

 




