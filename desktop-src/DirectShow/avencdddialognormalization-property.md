---
description: Gibt die normalisierungs Ebene des Dialogs in Dezibel (DB) in einem Dolby Digital-Audiostream an. Diese Eigenschaft gilt für Dolby Digital-Audioencoder.
ms.assetid: c347f8b2-5132-45d6-af66-43d3c409b0d7
title: Avencdddialognormalisierung-Eigenschaft (codecapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 586f241dc8d032767ecb2678c1ee5704dc20e0ef
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/06/2021
ms.locfileid: "104482494"
---
# <a name="avencdddialognormalization-property"></a><span data-ttu-id="32802-104">Avencdddialognormalisierung (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="32802-104">AVEncDDDialogNormalization property</span></span>

<span data-ttu-id="32802-105">Gibt die normalisierungs Ebene des Dialogs in Dezibel (DB) in einem Dolby Digital-Audiostream an.</span><span class="sxs-lookup"><span data-stu-id="32802-105">Specifies the dialog normalization level, in decibels (dB), in a Dolby Digital audio stream.</span></span> <span data-ttu-id="32802-106">Diese Eigenschaft gilt für Dolby Digital-Audioencoder.</span><span class="sxs-lookup"><span data-stu-id="32802-106">This property applies to Dolby Digital audio encoders.</span></span>

<span data-ttu-id="32802-107">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="32802-107">This property is read/write.</span></span>

## <a name="data-type"></a><span data-ttu-id="32802-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="32802-108">Data type</span></span>

<span data-ttu-id="32802-109">**UInt32** (**VT \_ UI4**)</span><span class="sxs-lookup"><span data-stu-id="32802-109">**UINT32** (**VT\_UI4**)</span></span>

## <a name="property-guid"></a><span data-ttu-id="32802-110">Eigenschaften-GUID</span><span class="sxs-lookup"><span data-stu-id="32802-110">Property GUID</span></span>

<span data-ttu-id="32802-111">**Codecapi \_ avencdddialognormalisierung**</span><span class="sxs-lookup"><span data-stu-id="32802-111">**CODECAPI\_AVEncDDDialogNormalization**</span></span>

## <a name="property-value"></a><span data-ttu-id="32802-112">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="32802-112">Property value</span></span>

<span data-ttu-id="32802-113">Diese Eigenschaft verfügt über einen linearen Wertebereich.</span><span class="sxs-lookup"><span data-stu-id="32802-113">This property has a linear range of values.</span></span> <span data-ttu-id="32802-114">Um den unterstützten Bereich abzurufen, nennen Sie [**icodecapi:: getparameterrange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span><span class="sxs-lookup"><span data-stu-id="32802-114">To get the supported range, call [**ICodecAPI::GetParameterRange**](/windows/desktop/api/Strmif/nf-strmif-icodecapi-getparameterrange).</span></span>

## <a name="requirements"></a><span data-ttu-id="32802-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="32802-115">Requirements</span></span>



| <span data-ttu-id="32802-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="32802-116">Requirement</span></span> | <span data-ttu-id="32802-117">Wert</span><span class="sxs-lookup"><span data-stu-id="32802-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="32802-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="32802-118">Minimum supported client</span></span><br/> | <span data-ttu-id="32802-119">Windows 2000 Professional \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="32802-119">Windows 2000 Professional \[desktop apps \| UWP apps\]</span></span><br/>                     |
| <span data-ttu-id="32802-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="32802-120">Minimum supported server</span></span><br/> | <span data-ttu-id="32802-121">Windows 2000 Server \[ Desktop Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="32802-121">Windows 2000 Server \[desktop apps \| UWP apps\]</span></span><br/>                           |
| <span data-ttu-id="32802-122">Header</span><span class="sxs-lookup"><span data-stu-id="32802-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="32802-123"><dt>Codecapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="32802-123"><dt>Codecapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32802-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32802-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32802-125">Eigenschaften der Codec-API</span><span class="sxs-lookup"><span data-stu-id="32802-125">Codec API Properties</span></span>](codec-api-properties.md)
</dt> <dt>

[<span data-ttu-id="32802-126">**Icodecapi-Schnittstelle**</span><span class="sxs-lookup"><span data-stu-id="32802-126">**ICodecAPI Interface**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)
</dt> </dl>

 

 




