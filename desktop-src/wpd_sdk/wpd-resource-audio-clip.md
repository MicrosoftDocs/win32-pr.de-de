---
description: Gibt einen Audioclip für das-Objekt an.
ms.assetid: 24c15df0-4190-4c75-b89b-0c73d645c9ca
title: WPD_RESOURCE_AUDIO_CLIP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7013fb59670c92903f89509f720f7c597ef916fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106355335"
---
# <a name="wpd_resource_audio_clip"></a><span data-ttu-id="79f61-103">WPD \_ \_ - \_ ressourcenaudioclip</span><span class="sxs-lookup"><span data-stu-id="79f61-103">WPD\_RESOURCE\_AUDIO\_CLIP</span></span>

<span data-ttu-id="79f61-104">Gibt einen Audioclip für das-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="79f61-104">Specifies an audio clip for the object.</span></span>

<span data-ttu-id="79f61-105">Dieser Ressourcentyp muss die folgenden Attribute unterstützen.</span><span class="sxs-lookup"><span data-stu-id="79f61-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="79f61-106">Attributname</span><span class="sxs-lookup"><span data-stu-id="79f61-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="79f61-107">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="79f61-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="79f61-108">WPD \_ - \_ Audiobitrate</span><span class="sxs-lookup"><span data-stu-id="79f61-108">WPD\_AUDIO\_BITRATE</span></span>](audio-properties.md)                                                             | <span data-ttu-id="79f61-109">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="79f61-109">Recommended.</span></span>                                           |
| [<span data-ttu-id="79f61-110">Anzahl von WPD \_ - \_ Audiokanälen \_</span><span class="sxs-lookup"><span data-stu-id="79f61-110">WPD\_AUDIO\_CHANNEL\_COUNT</span></span>](audio-properties.md)                                                | <span data-ttu-id="79f61-111">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="79f61-111">Optional.</span></span>                                              |
| [<span data-ttu-id="79f61-112">WPD \_ - \_ \_ audioformatcode</span><span class="sxs-lookup"><span data-stu-id="79f61-112">WPD\_AUDIO\_FORMAT\_CODE</span></span>](audio-properties.md)                                                    | <span data-ttu-id="79f61-113">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="79f61-113">Optional.</span></span>                                              |
| [<span data-ttu-id="79f61-114">WPD \_ - \_ \_ audiobittiefe</span><span class="sxs-lookup"><span data-stu-id="79f61-114">WPD\_AUDIO\_BIT\_DEPTH</span></span>](audio-properties.md)                                                        | <span data-ttu-id="79f61-115">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="79f61-115">Optional.</span></span>                                              |
| [<span data-ttu-id="79f61-116">WPD \_ - \_ Audioblock \_ Ausrichtung</span><span class="sxs-lookup"><span data-stu-id="79f61-116">WPD\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](audio-properties.md)                                            | <span data-ttu-id="79f61-117">Dies ist optional.</span><span class="sxs-lookup"><span data-stu-id="79f61-117">Optional.</span></span>                                              |
| [<span data-ttu-id="79f61-118">Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_</span><span class="sxs-lookup"><span data-stu-id="79f61-118">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="79f61-119">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="79f61-119">Required.</span></span>                                              |
| [<span data-ttu-id="79f61-120">WPD- \_ Ressourcen \_ Attribut \_ kann \_ Lesen</span><span class="sxs-lookup"><span data-stu-id="79f61-120">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="79f61-121">Erforderlich, wenn diese Ressource von Clients gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="79f61-121">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="79f61-122">WPD- \_ Ressourcen \_ Attribut \_ kann \_ schreiben</span><span class="sxs-lookup"><span data-stu-id="79f61-122">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="79f61-123">Erforderlich, wenn Clients in diese Ressource schreiben können.</span><span class="sxs-lookup"><span data-stu-id="79f61-123">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="79f61-124">Das WPD- \_ Ressourcen \_ Attribut \_ kann \_ gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="79f61-124">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="79f61-125">Erforderlich, wenn von Clients diese Ressource gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="79f61-125">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="79f61-126">WPD- \_ Ressourcen \_ Attribut \_ optimale \_ Lese \_ Puffer \_ Größe</span><span class="sxs-lookup"><span data-stu-id="79f61-126">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="79f61-127">Erforderlich, wenn Clients über Lesezugriff auf die Ressource verfügen.</span><span class="sxs-lookup"><span data-stu-id="79f61-127">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="79f61-128">Größe des WPD- \_ Ressourcen \_ Attributs für \_ optimalen \_ Schreib \_ Puffer \_</span><span class="sxs-lookup"><span data-stu-id="79f61-128">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="79f61-129">Erforderlich, wenn Clients Schreibzugriff auf die Ressource haben.</span><span class="sxs-lookup"><span data-stu-id="79f61-129">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="79f61-130">WPD- \_ Ressourcen \_ Attribut \_ Format</span><span class="sxs-lookup"><span data-stu-id="79f61-130">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="79f61-131">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="79f61-131">Required.</span></span>                                              |
| [<span data-ttu-id="79f61-132">Ressourcen Schlüssel für WPD- \_ Ressourcen \_ Attribut \_ \_</span><span class="sxs-lookup"><span data-stu-id="79f61-132">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="79f61-133">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="79f61-133">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="79f61-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79f61-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="79f61-135">**Anforderungen für Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="79f61-135">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



