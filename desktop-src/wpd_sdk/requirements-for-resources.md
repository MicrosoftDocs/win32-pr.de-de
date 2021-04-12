---
description: Anforderungen für Ressourcen
ms.assetid: 6b654cd6-7e9f-4e12-a687-4110e600ba7b
title: Anforderungen für Ressourcen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5702555704137f4280e527f0fc26f176435238ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217189"
---
# <a name="requirements-for-resources"></a><span data-ttu-id="85b2c-103">Anforderungen für Ressourcen</span><span class="sxs-lookup"><span data-stu-id="85b2c-103">Requirements for Resources</span></span>

<span data-ttu-id="85b2c-104">Tragbare Windows-Geräte definieren die folgenden Ressourcen Kategorien als **PropertyKey** -Werte.</span><span class="sxs-lookup"><span data-stu-id="85b2c-104">Windows Portable Devices defines the following resource categories as **PROPERTYKEY** values.</span></span> <span data-ttu-id="85b2c-105">Diese Werte werden verwendet, um einzelne Ressourcen in einem-Objekt zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="85b2c-105">These values are used to describe individual resources in an object.</span></span> <span data-ttu-id="85b2c-106">Der *PID* -Member des Eigenschafts Schlüssels kann sich unterscheiden, um unterschiedliche Ressourcen desselben Typs für alle Typen außer dem Standardwert der **WPD- \_ Ressource \_** zu beschreiben, der nur eine Ressource beschreiben kann.</span><span class="sxs-lookup"><span data-stu-id="85b2c-106">The *pid* member of the property key can be different to describe different resources of the same type for all types except **WPD\_RESOURCE\_DEFAULT**, which can only describe one resource.</span></span> <span data-ttu-id="85b2c-107">Die Seite verknüpfte Beschreibung für jeden Ressourcentyp listet die Attribute auf, die von dieser Ressource unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="85b2c-107">The linked description page for each resource type lists the attributes supported by that resource.</span></span>



| <span data-ttu-id="85b2c-108">Ressourcenpropertykey</span><span class="sxs-lookup"><span data-stu-id="85b2c-108">Resource PROPERTYKEY</span></span>                                                | <span data-ttu-id="85b2c-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="85b2c-109">Description</span></span>                                                                                                    |
|---------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85b2c-110">**WPD- \_ Ressourcen \_ Standard**</span><span class="sxs-lookup"><span data-stu-id="85b2c-110">**WPD\_RESOURCE\_DEFAULT**</span></span>](wpd-resource-default.md)              | <span data-ttu-id="85b2c-111">Gibt die gesamte Datei hinter dem Objekt an.</span><span class="sxs-lookup"><span data-stu-id="85b2c-111">Specifies the whole file behind the object.</span></span> <span data-ttu-id="85b2c-112">Dies ist die einzige erforderliche Ressource für ein beliebiges Objekt mit einer Ressource.</span><span class="sxs-lookup"><span data-stu-id="85b2c-112">This is the only required resource for any object with a resource.</span></span> |
| [<span data-ttu-id="85b2c-113">**WPD- \_ Ressourcen \_ Album- \_ Grafik**</span><span class="sxs-lookup"><span data-stu-id="85b2c-113">**WPD\_RESOURCE\_ALBUM\_ART**</span></span>](wpd-resource-album-art.md)         | <span data-ttu-id="85b2c-114">Gibt ein Bild an, das die Albumgrafik für das-Objekt darstellt.</span><span class="sxs-lookup"><span data-stu-id="85b2c-114">Specifies an image that represents the album artwork for the object.</span></span>                                           |
| [<span data-ttu-id="85b2c-115">**WPD \_ \_ - \_ ressourcenaudioclip**</span><span class="sxs-lookup"><span data-stu-id="85b2c-115">**WPD\_RESOURCE\_AUDIO\_CLIP**</span></span>](wpd-resource-audio-clip.md)       | <span data-ttu-id="85b2c-116">Gibt einen Audioclip für das-Objekt an.</span><span class="sxs-lookup"><span data-stu-id="85b2c-116">Specifies an audio clip for the object.</span></span>                                                                        |
| [<span data-ttu-id="85b2c-117">**WPD- \_ Ressourcen \_ Kontakt \_ Foto**</span><span class="sxs-lookup"><span data-stu-id="85b2c-117">**WPD\_RESOURCE\_CONTACT\_PHOTO**</span></span>](wpd-resource-contact-photo.md) | <span data-ttu-id="85b2c-118">Gibt ein Bild an, das ein Foto der Person darstellt, auf die im Contact-Objekt verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="85b2c-118">Specifies an image that represents a photo of the individual referred to in the contact object.</span></span>                |
| [<span data-ttu-id="85b2c-119">**WPD- \_ Ressource \_ generisch**</span><span class="sxs-lookup"><span data-stu-id="85b2c-119">**WPD\_RESOURCE\_GENERIC**</span></span>](wpd-resource-generic.md)              | <span data-ttu-id="85b2c-120">Eine generische Ressource des nicht definierten Datentyps.</span><span class="sxs-lookup"><span data-stu-id="85b2c-120">A generic resource of undefined data type.</span></span> <span data-ttu-id="85b2c-121">Dies sollte als Bytearray behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="85b2c-121">This should be treated as a byte array.</span></span>                             |
| [<span data-ttu-id="85b2c-122">**Symbol für WPD- \_ Ressource \_**</span><span class="sxs-lookup"><span data-stu-id="85b2c-122">**WPD\_RESOURCE\_ICON**</span></span>](wpd-resource-icon.md)                    | <span data-ttu-id="85b2c-123">Symbol</span><span class="sxs-lookup"><span data-stu-id="85b2c-123">An icon.</span></span>                                                                                                       |
| [<span data-ttu-id="85b2c-124">**WPD- \_ Ressourcen \_ Miniaturansicht**</span><span class="sxs-lookup"><span data-stu-id="85b2c-124">**WPD\_RESOURCE\_THUMBNAIL**</span></span>](wpd-resource-thumbnail.md)          | <span data-ttu-id="85b2c-125">Ein Miniaturbild.</span><span class="sxs-lookup"><span data-stu-id="85b2c-125">A thumbnail image.</span></span>                                                                                             |



 

## <a name="related-topics"></a><span data-ttu-id="85b2c-126">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="85b2c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85b2c-127">**Programmierverzeichnis**</span><span class="sxs-lookup"><span data-stu-id="85b2c-127">**Programming Reference**</span></span>](programming-reference.md)
</dt> </dl>

 

 



