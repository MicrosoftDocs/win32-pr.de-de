---
description: Gibt ein kleines Bild&\# 8212 an; normalerweise eine kleinere Version eines größeren Bilds im Objekt.
ms.assetid: ad1eac9d-b182-49b2-bd2c-2d76e2026d80
title: WPD_RESOURCE_THUMBNAIL
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4fc26af624f756f55ccb10ccf3f8c7bf3e6a6035
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128945"
---
# <a name="wpd_resource_thumbnail"></a><span data-ttu-id="e29e4-103">WPD- \_ Ressourcen \_ Miniaturansicht</span><span class="sxs-lookup"><span data-stu-id="e29e4-103">WPD\_RESOURCE\_THUMBNAIL</span></span>

<span data-ttu-id="e29e4-104">Gibt ein kleines Bild an – in der Regel eine kleinere Version eines größeren Bilds im-Objekt.</span><span class="sxs-lookup"><span data-stu-id="e29e4-104">Specifies a small picture—typically a smaller version of a larger picture in the object.</span></span>

<span data-ttu-id="e29e4-105">Dieser Ressourcentyp muss die folgenden Attribute unterstützen.</span><span class="sxs-lookup"><span data-stu-id="e29e4-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="e29e4-106">Attributname</span><span class="sxs-lookup"><span data-stu-id="e29e4-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="e29e4-107">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="e29e4-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="e29e4-108">WPD- \_ Medien \_ Breite</span><span class="sxs-lookup"><span data-stu-id="e29e4-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="e29e4-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e29e4-109">Required.</span></span>                                              |
| [<span data-ttu-id="e29e4-110">WPD- \_ Medien \_ Höhe</span><span class="sxs-lookup"><span data-stu-id="e29e4-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="e29e4-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e29e4-111">Required.</span></span>                                              |
| [<span data-ttu-id="e29e4-112">Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_</span><span class="sxs-lookup"><span data-stu-id="e29e4-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="e29e4-113">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e29e4-113">Required.</span></span>                                              |
| [<span data-ttu-id="e29e4-114">WPD- \_ Ressourcen \_ Attribut \_ kann \_ Lesen</span><span class="sxs-lookup"><span data-stu-id="e29e4-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="e29e4-115">Erforderlich, wenn diese Ressource von Clients gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e29e4-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="e29e4-116">WPD- \_ Ressourcen \_ Attribut \_ kann \_ schreiben</span><span class="sxs-lookup"><span data-stu-id="e29e4-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="e29e4-117">Erforderlich, wenn Clients in diese Ressource schreiben können.</span><span class="sxs-lookup"><span data-stu-id="e29e4-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="e29e4-118">Das WPD- \_ Ressourcen \_ Attribut \_ kann \_ gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="e29e4-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="e29e4-119">Erforderlich, wenn von Clients diese Ressource gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="e29e4-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="e29e4-120">WPD- \_ Ressourcen \_ Attribut \_ optimale \_ Lese \_ Puffer \_ Größe</span><span class="sxs-lookup"><span data-stu-id="e29e4-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="e29e4-121">Erforderlich, wenn Clients über Lesezugriff auf die Ressource verfügen.</span><span class="sxs-lookup"><span data-stu-id="e29e4-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="e29e4-122">Größe des WPD- \_ Ressourcen \_ Attributs für \_ optimalen \_ Schreib \_ Puffer \_</span><span class="sxs-lookup"><span data-stu-id="e29e4-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="e29e4-123">Erforderlich, wenn Clients Schreibzugriff auf die Ressource haben.</span><span class="sxs-lookup"><span data-stu-id="e29e4-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="e29e4-124">WPD- \_ Ressourcen \_ Attribut \_ Format</span><span class="sxs-lookup"><span data-stu-id="e29e4-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="e29e4-125">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="e29e4-125">Required.</span></span>                                              |
| [<span data-ttu-id="e29e4-126">Ressourcen Schlüssel für WPD- \_ Ressourcen \_ Attribut \_ \_</span><span class="sxs-lookup"><span data-stu-id="e29e4-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="e29e4-127">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="e29e4-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="e29e4-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e29e4-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e29e4-129">**Anforderungen für Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="e29e4-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



