---
description: Gibt ein Bild an, das die Albumgrafik für das-Objekt darstellt.
ms.assetid: 7a31ebb6-c4ab-4899-9c2e-c960aac4f0f9
title: WPD_RESOURCE_ALBUM_ART
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4f4b800aa2ae22f2400f3195b85da6bd3bd35b4b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525904"
---
# <a name="wpd_resource_album_art"></a><span data-ttu-id="5fa1f-103">WPD- \_ Ressourcen \_ Album- \_ Grafik</span><span class="sxs-lookup"><span data-stu-id="5fa1f-103">WPD\_RESOURCE\_ALBUM\_ART</span></span>

<span data-ttu-id="5fa1f-104">Gibt ein Bild an, das die Albumgrafik für das-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-104">Specifies an image that represents the album artwork for the object.</span></span>

<span data-ttu-id="5fa1f-105">Dieser Ressourcentyp muss die folgenden Attribute unterstützen.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="5fa1f-106">Attributname</span><span class="sxs-lookup"><span data-stu-id="5fa1f-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="5fa1f-107">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="5fa1f-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="5fa1f-108">WPD- \_ Medien \_ Breite</span><span class="sxs-lookup"><span data-stu-id="5fa1f-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="5fa1f-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-109">Required.</span></span>                                              |
| [<span data-ttu-id="5fa1f-110">WPD- \_ Medien \_ Höhe</span><span class="sxs-lookup"><span data-stu-id="5fa1f-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="5fa1f-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-111">Required.</span></span>                                              |
| [<span data-ttu-id="5fa1f-112">Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_</span><span class="sxs-lookup"><span data-stu-id="5fa1f-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="5fa1f-113">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-113">Required.</span></span>                                              |
| [<span data-ttu-id="5fa1f-114">WPD- \_ Ressourcen \_ Attribut \_ kann \_ Lesen</span><span class="sxs-lookup"><span data-stu-id="5fa1f-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="5fa1f-115">Erforderlich, wenn diese Ressource von Clients gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="5fa1f-116">WPD- \_ Ressourcen \_ Attribut \_ kann \_ schreiben</span><span class="sxs-lookup"><span data-stu-id="5fa1f-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="5fa1f-117">Erforderlich, wenn Clients in diese Ressource schreiben können.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="5fa1f-118">Das WPD- \_ Ressourcen \_ Attribut \_ kann \_ gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="5fa1f-119">Erforderlich, wenn von Clients diese Ressource gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="5fa1f-120">WPD- \_ Ressourcen \_ Attribut \_ optimale \_ Lese \_ Puffer \_ Größe</span><span class="sxs-lookup"><span data-stu-id="5fa1f-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="5fa1f-121">Erforderlich, wenn Clients über Lesezugriff auf die Ressource verfügen.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="5fa1f-122">Größe des WPD- \_ Ressourcen \_ Attributs für \_ optimalen \_ Schreib \_ Puffer \_</span><span class="sxs-lookup"><span data-stu-id="5fa1f-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="5fa1f-123">Erforderlich, wenn Clients Schreibzugriff auf die Ressource haben.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="5fa1f-124">WPD- \_ Ressourcen \_ Attribut \_ Format</span><span class="sxs-lookup"><span data-stu-id="5fa1f-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="5fa1f-125">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5fa1f-125">Required.</span></span>                                              |
| [<span data-ttu-id="5fa1f-126">Ressourcen Schlüssel für WPD- \_ Ressourcen \_ Attribut \_ \_</span><span class="sxs-lookup"><span data-stu-id="5fa1f-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="5fa1f-127">Empfohlen</span><span class="sxs-lookup"><span data-stu-id="5fa1f-127">Recommended</span></span>                                            |



 

## <a name="see-also"></a><span data-ttu-id="5fa1f-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fa1f-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fa1f-129">**Anforderungen für Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="5fa1f-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



