---
description: Gibt die gesamte Datei hinter dem Objekt an. Es ist auch eine Möglichkeit, auf jeden Ressourcentyp zu verweisen, einschließlich derjenigen, die nicht von anderen mobilen Windows-Geräten (z. b. einem benutzerdefinierten Objekttyp) abgedeckt werden.
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d04d6c7ec7d0623e2ed42c61115c6ae2145bf066
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104529891"
---
# <a name="wpd_resource_default"></a><span data-ttu-id="8a161-104">WPD- \_ Ressourcen \_ Standard</span><span class="sxs-lookup"><span data-stu-id="8a161-104">WPD\_RESOURCE\_DEFAULT</span></span>

<span data-ttu-id="8a161-105">Gibt die gesamte Datei hinter dem Objekt an.</span><span class="sxs-lookup"><span data-stu-id="8a161-105">Specifies the whole file behind the object.</span></span> <span data-ttu-id="8a161-106">Es ist auch eine Möglichkeit, auf jeden Ressourcentyp zu verweisen, einschließlich derjenigen, die nicht von anderen mobilen Windows-Geräten (z. b. einem benutzerdefinierten Objekttyp) abgedeckt werden.</span><span class="sxs-lookup"><span data-stu-id="8a161-106">It is also a way of referring to any resource type, including those not covered by other Windows Portable Devices resource types, such as a custom object type.</span></span>

<span data-ttu-id="8a161-107">Alle Ressourcen, die in die angegebene Ressource eingebettet sind, werden eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8a161-107">Any resources embedded within the specified resource will be included.</span></span> <span data-ttu-id="8a161-108">Beispielsweise kann die Standardressource eines Stamm Ordners von Kontakten alle in der Liste eingefügten Kontakte enthalten.</span><span class="sxs-lookup"><span data-stu-id="8a161-108">For example, the default resource of a root folder of contacts may include all the nested contacts.</span></span> <span data-ttu-id="8a161-109">Allerdings werden alle untergeordneten Ressourcen, die nur durch Metadaten oder Verweise *verknüpft* sind, nicht eingeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8a161-109">However, any child resources that are merely *linked* by metadata or references are not included.</span></span> <span data-ttu-id="8a161-110">Ein Beispiel hierfür wäre eine Wiedergabeliste, die nur über Metadatenverweise oder Textpfad-Verweise in der Datei mit Audiodateien verknüpft werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a161-110">An example of this would be a playlist, which might only link to audio files through metadata references or textual path references in the file.</span></span>

<span data-ttu-id="8a161-111">Der einzige zulässige *PID* -Wert für diesen **PropertyKey** ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="8a161-111">The only allowed *pid* value for this **PROPERTYKEY** is zero.</span></span>

<span data-ttu-id="8a161-112">Dieser Ressourcentyp muss die folgenden Attribute unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8a161-112">This type of resource must support the following attributes.</span></span>



| <span data-ttu-id="8a161-113">Attributname</span><span class="sxs-lookup"><span data-stu-id="8a161-113">Attribute Name</span></span>                                                                                                            | <span data-ttu-id="8a161-114">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="8a161-114">Required or Optional</span></span>                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [<span data-ttu-id="8a161-115">Gesamtgröße des WPD- \_ Ressourcen \_ Attributs \_ \_</span><span class="sxs-lookup"><span data-stu-id="8a161-115">WPD\_RESOURCE\_ATTRIBUTE\_TOTAL\_SIZE</span></span>](resource-attribute-properties.md)              | <span data-ttu-id="8a161-116">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8a161-116">Required.</span></span>                                              |
| [<span data-ttu-id="8a161-117">WPD- \_ Ressourcen \_ Attribut \_ kann \_ Lesen</span><span class="sxs-lookup"><span data-stu-id="8a161-117">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_READ</span></span>](attributes.md)                                     | <span data-ttu-id="8a161-118">Erforderlich, wenn diese Ressource von Clients gelesen werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a161-118">Required if clients can read this resource.</span></span>            |
| [<span data-ttu-id="8a161-119">WPD- \_ Ressourcen \_ Attribut \_ kann \_ schreiben</span><span class="sxs-lookup"><span data-stu-id="8a161-119">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_WRITE</span></span>](attributes.md)                                   | <span data-ttu-id="8a161-120">Erforderlich, wenn Clients in diese Ressource schreiben können.</span><span class="sxs-lookup"><span data-stu-id="8a161-120">Required if clients can write to this resource.</span></span>        |
| [<span data-ttu-id="8a161-121">Das WPD- \_ Ressourcen \_ Attribut \_ kann \_ gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="8a161-121">WPD\_RESOURCE\_ATTRIBUTE\_CAN\_DELETE</span></span>](attributes.md)                                 | <span data-ttu-id="8a161-122">Erforderlich, wenn von Clients diese Ressource gelöscht werden kann.</span><span class="sxs-lookup"><span data-stu-id="8a161-122">Required if clients can delete this resource.</span></span>          |
| [<span data-ttu-id="8a161-123">WPD- \_ Ressourcen \_ Attribut \_ optimale \_ Lese \_ Puffer \_ Größe</span><span class="sxs-lookup"><span data-stu-id="8a161-123">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_READ\_BUFFER\_SIZE</span></span>](attributes.md)   | <span data-ttu-id="8a161-124">Erforderlich, wenn Clients über Lesezugriff auf die Ressource verfügen.</span><span class="sxs-lookup"><span data-stu-id="8a161-124">Required if clients have read access to the resource.</span></span>  |
| [<span data-ttu-id="8a161-125">Größe des WPD- \_ Ressourcen \_ Attributs für \_ optimalen \_ Schreib \_ Puffer \_</span><span class="sxs-lookup"><span data-stu-id="8a161-125">WPD\_RESOURCE\_ATTRIBUTE\_OPTIMAL\_WRITE\_BUFFER\_SIZE</span></span>](attributes.md) | <span data-ttu-id="8a161-126">Erforderlich, wenn Clients Schreibzugriff auf die Ressource haben.</span><span class="sxs-lookup"><span data-stu-id="8a161-126">Required if clients have write access to the resource.</span></span> |
| [<span data-ttu-id="8a161-127">WPD- \_ Ressourcen \_ Attribut \_ Format</span><span class="sxs-lookup"><span data-stu-id="8a161-127">WPD\_RESOURCE\_ATTRIBUTE\_FORMAT</span></span>](resource-attribute-properties.md)                       | <span data-ttu-id="8a161-128">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8a161-128">Required.</span></span>                                              |
| [<span data-ttu-id="8a161-129">Ressourcen Schlüssel für WPD- \_ Ressourcen \_ Attribut \_ \_</span><span class="sxs-lookup"><span data-stu-id="8a161-129">WPD\_RESOURCE\_ATTRIBUTE\_RESOURCE\_KEY</span></span>](resource-attribute-properties.md)                                              | <span data-ttu-id="8a161-130">Empfohlen.</span><span class="sxs-lookup"><span data-stu-id="8a161-130">Recommended.</span></span>                                           |



 

## <a name="see-also"></a><span data-ttu-id="8a161-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8a161-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a161-132">**Anforderungen für Ressourcen**</span><span class="sxs-lookup"><span data-stu-id="8a161-132">**Requirements for Resources**</span></span>](requirements-for-resources.md)
</dt> </dl>

 

 



