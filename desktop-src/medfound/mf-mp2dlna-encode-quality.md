---
description: Gibt die Codierungsqualität für die Digital Living Network Alliance (DLNA)-Medien Senke an.
ms.assetid: 4cf745ab-66ae-40f2-b5c4-3f72f1b9badb
title: MF_MP2DLNA_ENCODE_QUALITY-Attribut (Mfmp2dlna. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81c785ff12524d45d096d566014a5c0a5e24eea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104042342"
---
# <a name="mf_mp2dlna_encode_quality-attribute"></a><span data-ttu-id="49e7a-103">MF \_ MP2DLNA \_ \_ Qualitäts Attribut codieren</span><span class="sxs-lookup"><span data-stu-id="49e7a-103">MF\_MP2DLNA\_ENCODE\_QUALITY attribute</span></span>

<span data-ttu-id="49e7a-104">Gibt die Codierungsqualität für die Digital Living Network Alliance (DLNA)-Medien Senke an.</span><span class="sxs-lookup"><span data-stu-id="49e7a-104">Specifies the encoding quality for the Digital Living Network Alliance (DLNA) media sink.</span></span>

## <a name="data-type"></a><span data-ttu-id="49e7a-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="49e7a-105">Data type</span></span>

<span data-ttu-id="49e7a-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="49e7a-106">**UINT32**</span></span>

<span data-ttu-id="49e7a-107">Bereich: 0 – 18</span><span class="sxs-lookup"><span data-stu-id="49e7a-107">Range: 0–18</span></span>

## <a name="getset"></a><span data-ttu-id="49e7a-108">Abrufen/Festlegen</span><span class="sxs-lookup"><span data-stu-id="49e7a-108">Get/set</span></span>

<span data-ttu-id="49e7a-109">Um dieses Attribut abzurufen, nennen Sie [**imfattributes:: GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span><span class="sxs-lookup"><span data-stu-id="49e7a-109">To get this attribute, call [**IMFAttributes::GetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getuint32).</span></span>

<span data-ttu-id="49e7a-110">Um dieses Attribut festzulegen, nennen Sie [**imfattributes:: SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span><span class="sxs-lookup"><span data-stu-id="49e7a-110">To set this attribute, call [**IMFAttributes::SetUINT32**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setuint32).</span></span>

## <a name="remarks"></a><span data-ttu-id="49e7a-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49e7a-111">Remarks</span></span>

<span data-ttu-id="49e7a-112">Höhere Zahlen weisen auf eine bessere Codierungsqualität hin.</span><span class="sxs-lookup"><span data-stu-id="49e7a-112">Higher numbers indicate better encoding quality.</span></span> <span data-ttu-id="49e7a-113">Niedrigere Zahlen weisen auf eine schnellere Codierung hin, aber eine niedrigere Codierungsqualität.</span><span class="sxs-lookup"><span data-stu-id="49e7a-113">Lower numbers indicate faster encoding, but lower encoding quality.</span></span> <span data-ttu-id="49e7a-114">Der Standardwert ist 9.</span><span class="sxs-lookup"><span data-stu-id="49e7a-114">The default value is 9.</span></span>

<span data-ttu-id="49e7a-115">Wenn Sie dieses Attribut für die DLNA-Medien Senke festlegen möchten, Fragen Sie die Medien Senke nach der [**imfattributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) -Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="49e7a-115">To set this attribute on the DLNA media sink, query the media sink for the [**IMFAttributes**](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes) interface.</span></span> <span data-ttu-id="49e7a-116">Legen Sie das-Attribut vor Beginn des Streamings fest.</span><span class="sxs-lookup"><span data-stu-id="49e7a-116">Set the attribute before streaming begins.</span></span>

## <a name="requirements"></a><span data-ttu-id="49e7a-117">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="49e7a-117">Requirements</span></span>



| <span data-ttu-id="49e7a-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="49e7a-118">Requirement</span></span> | <span data-ttu-id="49e7a-119">Wert</span><span class="sxs-lookup"><span data-stu-id="49e7a-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="49e7a-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="49e7a-120">Minimum supported client</span></span><br/> | <span data-ttu-id="49e7a-121">Nur Windows 7 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49e7a-121">Windows 7 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="49e7a-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="49e7a-122">Minimum supported server</span></span><br/> | <span data-ttu-id="49e7a-123">Nur Windows Server 2008 R2 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="49e7a-123">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="49e7a-124">Header</span><span class="sxs-lookup"><span data-stu-id="49e7a-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="49e7a-125"><dt>Mfmp2dlna. h</dt></span><span class="sxs-lookup"><span data-stu-id="49e7a-125"><dt>Mfmp2dlna.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="49e7a-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49e7a-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49e7a-127">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="49e7a-127">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> </dl>

 

 




