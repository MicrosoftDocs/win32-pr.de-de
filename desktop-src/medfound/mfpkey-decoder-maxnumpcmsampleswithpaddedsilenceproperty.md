---
description: Gibt die maximale Anzahl zusätzlicher PCM-Beispiele an, die nach dem Decodieren einer Datei am Ende von zurückgegeben werden können.
ms.assetid: 82b3676c-7653-421c-aac7-7f20a642779f
title: MFPKEY_Decoder_MaxNumPCMSamplesWithPaddedSilence-Eigenschaft (wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4b1f97b55c2eedd8cc7d6d524379569073fa35d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343834"
---
# <a name="mfpkey_decoder_maxnumpcmsampleswithpaddedsilence-property"></a><span data-ttu-id="8e8e8-103">Mfpkey- \_ Decoder \_ MaxNumPCMSamplesWithPaddedSilence Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="8e8e8-103">MFPKEY\_Decoder\_MaxNumPCMSamplesWithPaddedSilence Property</span></span>

<span data-ttu-id="8e8e8-104">Gibt die maximale Anzahl zusätzlicher PCM-Beispiele an, die nach dem Decodieren einer Datei am Ende von zurückgegeben werden können.</span><span class="sxs-lookup"><span data-stu-id="8e8e8-104">Specifies the maximum number of additional PCM samples that might be returned at the end of after decoding a file.</span></span>

## <a name="constant-for-ipropertybag"></a><span data-ttu-id="8e8e8-105">Konstante für IPropertyBag</span><span class="sxs-lookup"><span data-stu-id="8e8e8-105">Constant for IPropertyBag</span></span>

<span data-ttu-id="8e8e8-106">Nur mit [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e8e8-106">Available only by using [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore).</span></span>

## <a name="data-type"></a><span data-ttu-id="8e8e8-107">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8e8e8-107">Data Type</span></span>

<span data-ttu-id="8e8e8-108">VT \_ I4</span><span class="sxs-lookup"><span data-stu-id="8e8e8-108">VT\_I4</span></span>

## <a name="default-value"></a><span data-ttu-id="8e8e8-109">Standardwert</span><span class="sxs-lookup"><span data-stu-id="8e8e8-109">Default Value</span></span>

<span data-ttu-id="8e8e8-110">2048</span><span class="sxs-lookup"><span data-stu-id="8e8e8-110">2048</span></span>

## <a name="remarks"></a><span data-ttu-id="8e8e8-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8e8e8-111">Remarks</span></span>

<span data-ttu-id="8e8e8-112">Diese Eigenschaft kann verwendet werden, um künstliche Stille zu schätzen, die zwischen den Liedern eingefügt wird, wenn Sie dem Decoder nacheinander zugeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8e8e8-112">This property can be used to estimate artificial silence that gets is inserted between songs as they are fed to the decoder one after another.</span></span>

<span data-ttu-id="8e8e8-113">Für die Windows Media Audio 10 Professional-und Windows Media Audio 9-Decoders ohne Verlust ist diese Eigenschaft stets gleich 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8e8e8-113">For the Windows Media Audio 10 Professional and Windows Media Audio 9 Lossless decoders, this property is always equal to 0.</span></span>

## <a name="requirements"></a><span data-ttu-id="8e8e8-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="8e8e8-114">Requirements</span></span>



| <span data-ttu-id="8e8e8-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="8e8e8-115">Requirement</span></span> | <span data-ttu-id="8e8e8-116">Wert</span><span class="sxs-lookup"><span data-stu-id="8e8e8-116">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8e8e8-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="8e8e8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="8e8e8-118">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e8e8-118">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="8e8e8-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="8e8e8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="8e8e8-120">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="8e8e8-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="8e8e8-121">Header</span><span class="sxs-lookup"><span data-stu-id="8e8e8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="8e8e8-122"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="8e8e8-122"><dt>Wmcodecdsp.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8e8e8-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8e8e8-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8e8e8-124">Eigenschaften von Media Foundation</span><span class="sxs-lookup"><span data-stu-id="8e8e8-124">Media Foundation Properties</span></span>](media-foundation-properties.md)
</dt> </dl>

 

 
