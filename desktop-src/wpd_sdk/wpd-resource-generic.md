---
description: Gibt einen Ressourcentyp an, der nicht anderweitig von tragbaren Windows-Geräten definiert wird.
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8b5cdf3e9ae615529f441a20d885980b601d3c24
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128948"
---
# <a name="wpd_resource_generic"></a><span data-ttu-id="f01bb-103">WPD- \_ Ressource \_ generisch</span><span class="sxs-lookup"><span data-stu-id="f01bb-103">WPD\_RESOURCE\_GENERIC</span></span>

<span data-ttu-id="f01bb-104">Gibt einen Ressourcentyp an, der nicht anderweitig von tragbaren Windows-Geräten definiert wird.</span><span class="sxs-lookup"><span data-stu-id="f01bb-104">Specifies a resource type not otherwise defined by Windows Portable Devices.</span></span> <span data-ttu-id="f01bb-105">Sie können eigene benutzerdefinierte Ressourcen definieren, die beliebige benutzerdefinierte oder von Windows Portable Geräte definierte Attribute unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f01bb-105">You can define your own custom resources that support any custom or Windows Portable Devices-defined attributes.</span></span> <span data-ttu-id="f01bb-106">Jede Ressource, die Sie erstellen, muss jedoch die folgenden Attribute unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f01bb-106">However, any resource you create must support the following attributes.</span></span>



| <span data-ttu-id="f01bb-107">Attributname</span><span class="sxs-lookup"><span data-stu-id="f01bb-107">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="f01bb-108">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="f01bb-108">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="f01bb-109">Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_</span><span class="sxs-lookup"><span data-stu-id="f01bb-109">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="f01bb-110">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f01bb-110">Required.</span></span>                                              |
| [<span data-ttu-id="f01bb-111">WPD- \_ Ressourcen \_ Attribut \_ kann \_ Lesen</span><span class="sxs-lookup"><span data-stu-id="f01bb-111">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="f01bb-112">Erforderlich, wenn diese Ressource von Clients gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="f01bb-112">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="f01bb-113">WPD- \_ Ressourcen \_ Attribut \_ kann \_ schreiben</span><span class="sxs-lookup"><span data-stu-id="f01bb-113">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="f01bb-114">Erforderlich, wenn Clients in diese Ressource schreiben können.</span><span class="sxs-lookup"><span data-stu-id="f01bb-114">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="f01bb-115">Das WPD- \_ Ressourcen \_ Attribut \_ kann \_ gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="f01bb-115">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="f01bb-116">Erforderlich, wenn von Clients diese Ressource gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="f01bb-116">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="f01bb-117">WPD- \_ Ressourcen \_ Attribut \_ optimale \_ Lese \_ Puffer \_ Größe</span><span class="sxs-lookup"><span data-stu-id="f01bb-117">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="f01bb-118">Erforderlich, wenn Clients über Lesezugriff auf die Ressource verfügen.</span><span class="sxs-lookup"><span data-stu-id="f01bb-118">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="f01bb-119">Größe des WPD- \_ Ressourcen \_ Attributs für \_ optimalen \_ Schreib \_ Puffer \_</span><span class="sxs-lookup"><span data-stu-id="f01bb-119">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="f01bb-120">Erforderlich, wenn Clients Schreibzugriff auf die Ressource haben.</span><span class="sxs-lookup"><span data-stu-id="f01bb-120">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="f01bb-121">WPD- \_ Ressourcen \_ Attribut \_ Format</span><span class="sxs-lookup"><span data-stu-id="f01bb-121">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="f01bb-122">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f01bb-122">Required.</span></span>                                              |
| [<span data-ttu-id="f01bb-123">Ressourcen Schlüssel für WPD- \_ Ressourcen \_ Attribut \_ \_</span><span class="sxs-lookup"><span data-stu-id="f01bb-123">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="f01bb-124">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="f01bb-124">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="f01bb-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f01bb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f01bb-126">**Anforderungen für Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="f01bb-126">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



