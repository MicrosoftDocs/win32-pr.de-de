---
description: Gibt an, dass die Datei vor dem mdat-Feld in der generierten Datei geschrieben wird.
ms.assetid: 97B68B0A-8266-4FCF-8CD9-35890E1AC774
title: MF_MPEG4SINK_MOOV_BEFORE_MDAT-Attribut (mspdl. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b5d345dc027c457ceb6123ce3854fff4b74f987
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106348055"
---
# <a name="mf_mpeg4sink_moov_before_mdat-attribute"></a><span data-ttu-id="6c5a1-103">MF \_ MPEG4SINK \_ vor dem \_ \_ mdat-Attribut</span><span class="sxs-lookup"><span data-stu-id="6c5a1-103">MF\_MPEG4SINK\_MOOV\_BEFORE\_MDAT attribute</span></span>

<span data-ttu-id="6c5a1-104">Gibt an, dass "muov" vor dem Feld "mdat" in der generierten Datei geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-104">Indicates that 'moov' will be written before 'mdat' box in the generated file.</span></span>

## <a name="data-type"></a><span data-ttu-id="6c5a1-105">Datentyp</span><span class="sxs-lookup"><span data-stu-id="6c5a1-105">Data type</span></span>

<span data-ttu-id="6c5a1-106">**UINT32**</span><span class="sxs-lookup"><span data-stu-id="6c5a1-106">**UINT32**</span></span>

## <a name="remarks"></a><span data-ttu-id="6c5a1-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c5a1-107">Remarks</span></span>

<span data-ttu-id="6c5a1-108">Das Standardverhalten der MPEG4 Media-Senke ist das Schreiben von "muov" nach dem Feld "mdat".</span><span class="sxs-lookup"><span data-stu-id="6c5a1-108">The default behavior of the mpeg4 media sink is to write 'moov' after 'mdat' box.</span></span> <span data-ttu-id="6c5a1-109">Das Festlegen dieses Attributs bewirkt, dass die generierte Datei "muov" vor dem Feld "mdat" schreibt.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-109">Setting this attribute causes the generated file to write 'moov' before 'mdat' box.</span></span>

<span data-ttu-id="6c5a1-110">Damit die MPEG4-Senke dieses Attribut verwenden kann, darf der weiter gegebene Bytestream nicht langsam suchen oder Remote für sein.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-110">In order for the mpeg4 sink to use this attribute, the byte stream passed in must not be slow seek or remote for .</span></span>

<span data-ttu-id="6c5a1-111">Diese Funktion umfasst ein zusätzliches Kopieren/remuxing von Dateien.</span><span class="sxs-lookup"><span data-stu-id="6c5a1-111">This feature involves an additional file copying/remuxing.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c5a1-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6c5a1-112">Requirements</span></span>



| <span data-ttu-id="6c5a1-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6c5a1-113">Requirement</span></span> | <span data-ttu-id="6c5a1-114">Wert</span><span class="sxs-lookup"><span data-stu-id="6c5a1-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="6c5a1-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6c5a1-115">Minimum supported client</span></span><br/> | <span data-ttu-id="6c5a1-116">Windows 8 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6c5a1-116">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                  |
| <span data-ttu-id="6c5a1-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6c5a1-117">Minimum supported server</span></span><br/> | <span data-ttu-id="6c5a1-118">Windows Server 2012 \[ -Desktop-Apps \| UWP-apps\]</span><span class="sxs-lookup"><span data-stu-id="6c5a1-118">Windows Server 2012 \[desktop apps \| UWP apps\]</span></span><br/>                        |
| <span data-ttu-id="6c5a1-119">Header</span><span class="sxs-lookup"><span data-stu-id="6c5a1-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c5a1-120"><dt>Mspdl. h</dt></span><span class="sxs-lookup"><span data-stu-id="6c5a1-120"><dt>Mfidl.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6c5a1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c5a1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6c5a1-122">Alphabetische Liste der Media Foundation Attribute</span><span class="sxs-lookup"><span data-stu-id="6c5a1-122">Alphabetical List of Media Foundation Attributes</span></span>](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[<span data-ttu-id="6c5a1-123">Medientyp Attribute</span><span class="sxs-lookup"><span data-stu-id="6c5a1-123">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> </dl>

 

 




