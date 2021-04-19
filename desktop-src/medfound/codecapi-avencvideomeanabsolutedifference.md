---
description: Steuert das signalisieren von MF Sample Extension \_ meanabsolutedifference durch imfattribute für jedes Ausgabe Beispiel.
ms.assetid: 61C0F431-FBF5-4B17-8F3A-0F6AD2BA33B7
title: CODECAPI_AVEncVideoMeanAbsoluteDifference-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f58a7bc0da9fce88c0b8137d800d527d4717801c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106345465"
---
# <a name="codecapi_avencvideomeanabsolutedifference-property"></a><span data-ttu-id="267b1-103">Codecapi \_ avencvideomeanabsolutedifference (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="267b1-103">CODECAPI\_AVEncVideoMeanAbsoluteDifference property</span></span>

<span data-ttu-id="267b1-104">Steuert das signalisieren von [MF Sample Extension \_ meanabsolutedifference](mfsampleextension-meanabsolutedifference.md) durch [**imfattribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) für jedes Ausgabe Beispiel.</span><span class="sxs-lookup"><span data-stu-id="267b1-104">Controls the signaling of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) through [**IMFAttribute**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) on each output sample.</span></span>

## <a name="data-type"></a><span data-ttu-id="267b1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="267b1-105">Data type</span></span>

<span data-ttu-id="267b1-106">**Ulong** (VT \_ UI4)</span><span class="sxs-lookup"><span data-stu-id="267b1-106">**ULONG** (VT\_UI4)</span></span>

## <a name="property-guid"></a><span data-ttu-id="267b1-107">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="267b1-107">Property GUID</span></span>

<span data-ttu-id="267b1-108">**Codecapi \_ avencvideomeanabsolutedifference**</span><span class="sxs-lookup"><span data-stu-id="267b1-108">**CODECAPI\_AVEncVideoMeanAbsoluteDifference**</span></span>

## <a name="remarks"></a><span data-ttu-id="267b1-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="267b1-109">Remarks</span></span>

<span data-ttu-id="267b1-110">Wenn die Anwendung einen Wert ungleich 0 (null) festlegt, sollte der Encoder jedes Ausgabe Beispiel das [mfsampleextension-Beispiel Attribut " \_ meanabsolutedifference](mfsampleextension-meanabsolutedifference.md) " hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="267b1-110">If the application sets a non-zero value then the encoder should add the [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) sample attribute to each output sample.</span></span> <span data-ttu-id="267b1-111">Das mfsampleextension- \_ Attribut "meanabsolutedifference" gibt den Mittelwert der absoluten Differenz zwischen den Quell Beispielen und den vorhergesagten Beispielen auf der Y-Ebene an.</span><span class="sxs-lookup"><span data-stu-id="267b1-111">The MFSampleExtension\_MeanAbsoluteDifference attribute indicates the mean absolute difference between the source samples and the predicted samples in the Y plane.</span></span>

<span data-ttu-id="267b1-112">Wenn der Encoder 0 für **getparameterrange** zurückgibt, unterstützt der Encoder die Ausgabe von [MF Sample Extension " \_ meanabsolutedifference](mfsampleextension-meanabsolutedifference.md) " nicht in den Ausgabe Beispielen.</span><span class="sxs-lookup"><span data-stu-id="267b1-112">If the encoder returns 0 for **GetParameterRange**, then the encoder does not support the output of [MFSampleExtension\_MeanAbsoluteDifference](mfsampleextension-meanabsolutedifference.md) on the output samples.</span></span>

<span data-ttu-id="267b1-113">Der Standardwert muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="267b1-113">The default value should be 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="267b1-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="267b1-114">Requirements</span></span>



| <span data-ttu-id="267b1-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="267b1-115">Requirement</span></span> | <span data-ttu-id="267b1-116">Wert</span><span class="sxs-lookup"><span data-stu-id="267b1-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="267b1-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="267b1-117">Minimum supported client</span></span><br/> | <span data-ttu-id="267b1-118">\[Nur Desktop-Apps Windows 8.1\]</span><span class="sxs-lookup"><span data-stu-id="267b1-118">Windows 8.1 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="267b1-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="267b1-119">Minimum supported server</span></span><br/> | <span data-ttu-id="267b1-120">Nur Windows Server 2012 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="267b1-120">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="267b1-121">Header</span><span class="sxs-lookup"><span data-stu-id="267b1-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="267b1-122"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="267b1-122"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="267b1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="267b1-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="267b1-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="267b1-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 




