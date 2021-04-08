---
description: WPD \_ - \_ Inhaltstyp \_ Dienst
ms.assetid: 87c4c228-69e0-4b55-b91f-fe6e561f6d18
title: WPD_CONTENT_TYPE_SERVICE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1655825828867e38ef1962d35bcb0cfebf4ed76e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103960403"
---
# <a name="wpd_content_type_service"></a><span data-ttu-id="036cc-103">WPD \_ - \_ Inhaltstyp \_ Dienst</span><span class="sxs-lookup"><span data-stu-id="036cc-103">WPD\_CONTENT\_TYPE\_SERVICE</span></span>

<span data-ttu-id="036cc-104">Ein-Objekt, das den Typ beschreibt, weil der WPD- \_ \_ Inhaltstyp \_ Dienst einen Geräte Dienst darstellt.</span><span class="sxs-lookup"><span data-stu-id="036cc-104">An object that describes its type as WPD\_CONTENT\_TYPE\_SERVICE represents a device service.</span></span>

<span data-ttu-id="036cc-105">Dieser Objekttyp unterstützt die folgenden Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="036cc-105">This type of object supports the following properties.</span></span>



| <span data-ttu-id="036cc-106">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="036cc-106">Property Name</span></span>                                                                                        | <span data-ttu-id="036cc-107">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="036cc-107">Required or Optional</span></span>                                                           |
|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [<span data-ttu-id="036cc-108">WPD- \_ Objekt- \_ ID</span><span class="sxs-lookup"><span data-stu-id="036cc-108">WPD\_OBJECT\_ID</span></span>](object-properties.md)                                               | <span data-ttu-id="036cc-109">Erforderlich, schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="036cc-109">Required, read-only.</span></span> <span data-ttu-id="036cc-110">Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="036cc-110">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="036cc-111">übergeordnete WPD- \_ Objekt- \_ \_ ID</span><span class="sxs-lookup"><span data-stu-id="036cc-111">WPD\_OBJECT\_PARENT\_ID</span></span>](object-properties.md)                                | <span data-ttu-id="036cc-112">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="036cc-112">Required.</span></span>                                                                      |
| [<span data-ttu-id="036cc-113">WPD- \_ Objekt \_ Name</span><span class="sxs-lookup"><span data-stu-id="036cc-113">WPD\_OBJECT\_NAME</span></span>](object-properties.md)                                           | <span data-ttu-id="036cc-114">Erforderlich, wenn das-Objekt eine Datei darstellt.</span><span class="sxs-lookup"><span data-stu-id="036cc-114">Required if the object represents a file.</span></span>                                      |
| [<span data-ttu-id="036cc-115">\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt</span><span class="sxs-lookup"><span data-stu-id="036cc-115">WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID</span></span>](object-properties.md)         | <span data-ttu-id="036cc-116">Erforderlich, schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="036cc-116">Required, read-only.</span></span> <span data-ttu-id="036cc-117">Ein Client kann diese Eigenschaft auch zum Zeitpunkt der Erstellung nicht festlegen.</span><span class="sxs-lookup"><span data-stu-id="036cc-117">A client cannot set this property, even at creation time.</span></span> |
| [<span data-ttu-id="036cc-118">WPD- \_ Objekt \_ IsHidden</span><span class="sxs-lookup"><span data-stu-id="036cc-118">WPD\_OBJECT\_ISHIDDEN</span></span>](object-properties.md)                                   | <span data-ttu-id="036cc-119">Erforderlich, wenn der Dienst dem Benutzer nicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="036cc-119">Required if the service should not be shown to the user.</span></span>                       |
| [<span data-ttu-id="036cc-120">WPD- \_ Objekt \_ IsSystem</span><span class="sxs-lookup"><span data-stu-id="036cc-120">WPD\_OBJECT\_ISSYSTEM</span></span>](object-properties.md)                                   | <span data-ttu-id="036cc-121">Erforderlich, wenn das Objekt ein Systemobjekt ist (stellt eine Systemdatei dar).</span><span class="sxs-lookup"><span data-stu-id="036cc-121">Required if the object is a system object (represents a system file).</span></span>          |
| [<span data-ttu-id="036cc-122">WPD- \_ Funktions \_ Objekt \_ Kategorie</span><span class="sxs-lookup"><span data-stu-id="036cc-122">WPD\_FUNCTIONAL\_OBJECT\_CATEGORY</span></span>](object-properties.md) | <span data-ttu-id="036cc-123">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="036cc-123">Required.</span></span> <span data-ttu-id="036cc-124">Dies stellt den Geräte Diensttyp dar.</span><span class="sxs-lookup"><span data-stu-id="036cc-124">This represents the device service type.</span></span>                             |
| [<span data-ttu-id="036cc-125">WPD- \_ Dienst \_ Version</span><span class="sxs-lookup"><span data-stu-id="036cc-125">WPD\_SERVICE\_VERSION</span></span>](object-properties.md)           | <span data-ttu-id="036cc-126">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="036cc-126">Required.</span></span>                                                                      |
| [<span data-ttu-id="036cc-127">WPD \_ - \_ Speichertyp</span><span class="sxs-lookup"><span data-stu-id="036cc-127">WPD\_STORAGE\_TYPE</span></span>](object-properties.md)                                                          | <span data-ttu-id="036cc-128">Erforderlich, wenn der Dienst zum Speichern von Objekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="036cc-128">Required if the service is used to store objects.</span></span>                              |
| [<span data-ttu-id="036cc-129">WPD- \_ Speicher \_ Kapazität</span><span class="sxs-lookup"><span data-stu-id="036cc-129">WPD\_STORAGE\_CAPACITY</span></span>](object-properties.md)                                                      | <span data-ttu-id="036cc-130">Erforderlich, wenn der Dienst zum Speichern von Objekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="036cc-130">Required if the service is used to store objects.</span></span>                              |



 

## <a name="typical-resources"></a><span data-ttu-id="036cc-131">Typische Ressourcen</span><span class="sxs-lookup"><span data-stu-id="036cc-131">Typical Resources</span></span>

<span data-ttu-id="036cc-132">Diese Objekte hosten keine Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="036cc-132">These objects do not host resources.</span></span>

## <a name="related-topics"></a><span data-ttu-id="036cc-133">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="036cc-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="036cc-134">**Anforderungen für Objekte**</span><span class="sxs-lookup"><span data-stu-id="036cc-134">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 



