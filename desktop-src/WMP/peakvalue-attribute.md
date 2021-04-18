---
title: Attribut "Peer Wert"
description: Das peakvalue-Attribut ist ein 16-Bit-Amplitude-Wert, der die maximale Volumeebene angibt.
ms.assetid: 5d80a1f3-015c-4740-bd1c-f3bbf88a9df2
keywords:
- Media Player "Peer Value"-Attribut
topic_type:
- apiref
api_name:
- PeakValue
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 74fde522e043adb8b11c25bede763bed6b252f2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106354787"
---
# <a name="peakvalue-attribute"></a><span data-ttu-id="01d0e-104">Attribut "Peer Wert"</span><span class="sxs-lookup"><span data-stu-id="01d0e-104">PeakValue Attribute</span></span>

<span data-ttu-id="01d0e-105">Das **peakvalue** -Attribut ist ein 16-Bit-Amplitude-Wert, der die maximale Volumeebene angibt.</span><span class="sxs-lookup"><span data-stu-id="01d0e-105">The **PeakValue** attribute is a 16-bit amplitude value indicating the peak volume level.</span></span>

## <a name="applies-to"></a><span data-ttu-id="01d0e-106">Gilt für</span><span class="sxs-lookup"><span data-stu-id="01d0e-106">Applies To</span></span>

-   [<span data-ttu-id="01d0e-107">Audioelemente</span><span class="sxs-lookup"><span data-stu-id="01d0e-107">Audio Items</span></span>](audio-item-attributes.md)
-   [<span data-ttu-id="01d0e-108">Häufig verwendete Windows Media-Dateien</span><span class="sxs-lookup"><span data-stu-id="01d0e-108">Commonly Used Windows Media Files</span></span>](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a><span data-ttu-id="01d0e-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01d0e-109">Remarks</span></span>

<span data-ttu-id="01d0e-110">Dieses Attribut ist sowohl in der Bibliothek als auch in der digitalen Mediendatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="01d0e-110">This attribute is stored in both the library and the digital media file.</span></span>

<span data-ttu-id="01d0e-111">Dieser Wert wird von Windows Media Player in einer der folgenden Instanzen festgelegt:</span><span class="sxs-lookup"><span data-stu-id="01d0e-111">Windows Media Player sets this value in either of the following instances:</span></span>

-   <span data-ttu-id="01d0e-112">Nachdem eine Datei durch eine Datei gerissen wurde.</span><span class="sxs-lookup"><span data-stu-id="01d0e-112">After it has ripped a file.</span></span>
-   <span data-ttu-id="01d0e-113">Nachdem eine Datei wiedergegeben wurde (bei aktivierter Erweiterung für das automatische Volume).</span><span class="sxs-lookup"><span data-stu-id="01d0e-113">After it has played a file (when the Auto Volume Leveling enhancement is enabled).</span></span>

<span data-ttu-id="01d0e-114">Die SDK-Konstante für das Windows Media-Format für dieses Attribut ist g \_ wszpeer Value.</span><span class="sxs-lookup"><span data-stu-id="01d0e-114">The Windows Media Format SDK constant for this attribute is g\_wszPeakValue.</span></span>

<span data-ttu-id="01d0e-115">Um zu ermitteln, ob Sie den Wert dieses Attributs ändern können, verwenden Sie die [Media. isread onlyitem](media-isreadonlyitem.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="01d0e-115">To determine whether you can change the value of this attribute, use the [Media.isReadOnlyItem](media-isreadonlyitem.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="01d0e-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="01d0e-116">Requirements</span></span>



| <span data-ttu-id="01d0e-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="01d0e-117">Requirement</span></span> | <span data-ttu-id="01d0e-118">Wert</span><span class="sxs-lookup"><span data-stu-id="01d0e-118">Value</span></span> |
|--------------------|---------------------------------------------------|
| <span data-ttu-id="01d0e-119">Version</span><span class="sxs-lookup"><span data-stu-id="01d0e-119">Version</span></span><br/> | <span data-ttu-id="01d0e-120">Windows Media Player 9-Serie oder höher</span><span class="sxs-lookup"><span data-stu-id="01d0e-120">Windows Media Player 9 Series or later</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="01d0e-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01d0e-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01d0e-122">**Attribut Verweis**</span><span class="sxs-lookup"><span data-stu-id="01d0e-122">**Attribute Reference**</span></span>](attribute-reference.md)
</dt> </dl>

 

 





