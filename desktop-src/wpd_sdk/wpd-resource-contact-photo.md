---
description: Gibt ein Bild an, das ein Foto der Person darstellt, auf die im Contact-Objekt verwiesen wird.
ms.assetid: e26487d8-cd21-4d4a-ba68-ae915eff1304
title: WPD_RESOURCE_CONTACT_PHOTO
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25ee8a283492eba61989eca3f3bfa96bdba2f0ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106343659"
---
# <a name="wpd_resource_contact_photo"></a><span data-ttu-id="7595c-103">WPD- \_ Ressourcen \_ Kontakt \_ Foto</span><span class="sxs-lookup"><span data-stu-id="7595c-103">WPD\_RESOURCE\_CONTACT\_PHOTO</span></span>

<span data-ttu-id="7595c-104">Gibt ein Bild an, das ein Foto der Person darstellt, auf die im Contact-Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7595c-104">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>

<span data-ttu-id="7595c-105">Dieser Ressourcentyp muss die folgenden Attribute unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7595c-105">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="7595c-106">Attributname</span><span class="sxs-lookup"><span data-stu-id="7595c-106">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="7595c-107">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="7595c-107">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="7595c-108">WPD- \_ Medien \_ Breite</span><span class="sxs-lookup"><span data-stu-id="7595c-108">WPD\_MEDIA\_WIDTH</span></span>](media-properties.md)                                                                 | <span data-ttu-id="7595c-109">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7595c-109">Required.</span></span>                                              |
| [<span data-ttu-id="7595c-110">WPD- \_ Medien \_ Höhe</span><span class="sxs-lookup"><span data-stu-id="7595c-110">WPD\_MEDIA\_HEIGHT</span></span>](media-properties.md)                                                               | <span data-ttu-id="7595c-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7595c-111">Required.</span></span>                                              |
| [<span data-ttu-id="7595c-112">Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_</span><span class="sxs-lookup"><span data-stu-id="7595c-112">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="7595c-113">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7595c-113">Required.</span></span>                                              |
| [<span data-ttu-id="7595c-114">WPD- \_ Ressourcen \_ Attribut \_ kann \_ Lesen</span><span class="sxs-lookup"><span data-stu-id="7595c-114">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="7595c-115">Erforderlich, wenn diese Ressource von Clients gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="7595c-115">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="7595c-116">WPD- \_ Ressourcen \_ Attribut \_ kann \_ schreiben</span><span class="sxs-lookup"><span data-stu-id="7595c-116">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="7595c-117">Erforderlich, wenn Clients in diese Ressource schreiben können.</span><span class="sxs-lookup"><span data-stu-id="7595c-117">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="7595c-118">Das WPD- \_ Ressourcen \_ Attribut \_ kann \_ gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="7595c-118">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="7595c-119">Erforderlich, wenn von Clients diese Ressource gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="7595c-119">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="7595c-120">WPD- \_ Ressourcen \_ Attribut \_ optimale \_ Lese \_ Puffer \_ Größe</span><span class="sxs-lookup"><span data-stu-id="7595c-120">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="7595c-121">Erforderlich, wenn Clients über Lesezugriff auf die Ressource verfügen.</span><span class="sxs-lookup"><span data-stu-id="7595c-121">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="7595c-122">Größe des WPD- \_ Ressourcen \_ Attributs für \_ optimalen \_ Schreib \_ Puffer \_</span><span class="sxs-lookup"><span data-stu-id="7595c-122">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="7595c-123">Erforderlich, wenn Clients Schreibzugriff auf die Ressource haben.</span><span class="sxs-lookup"><span data-stu-id="7595c-123">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="7595c-124">WPD- \_ Ressourcen \_ Attribut \_ Format</span><span class="sxs-lookup"><span data-stu-id="7595c-124">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="7595c-125">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7595c-125">Required.</span></span>                                              |
| [<span data-ttu-id="7595c-126">Ressourcen Schlüssel für WPD- \_ Ressourcen \_ Attribut \_ \_</span><span class="sxs-lookup"><span data-stu-id="7595c-126">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="7595c-127">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="7595c-127">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="7595c-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7595c-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7595c-129">**Anforderungen für Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="7595c-129">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



