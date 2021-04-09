---
description: Dienst Objekt
ms.assetid: 4ce4e7f7-579d-41a5-a4e1-935ba0afce83
title: Dienst Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7a3aabfc4e4366c54a5d30dbe5825f178378133d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "103868671"
---
# <a name="service-object"></a><span data-ttu-id="2a949-103">Dienst Objekt</span><span class="sxs-lookup"><span data-stu-id="2a949-103">Service Object</span></span>

<span data-ttu-id="2a949-104">Das Dienst Objekt muss die folgenden Eigenschaften unterstützen.</span><span class="sxs-lookup"><span data-stu-id="2a949-104">The service object must support the following properties.</span></span>



| <span data-ttu-id="2a949-105">Eigenschaftsname</span><span class="sxs-lookup"><span data-stu-id="2a949-105">Property Name</span></span>                                                                                                                      | <span data-ttu-id="2a949-106">Erforderlich oder optional</span><span class="sxs-lookup"><span data-stu-id="2a949-106">Required or Optional</span></span>                                                                  |
|------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="2a949-107">[WPD- \_ Objekt- \_ ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a949-107">[WPD\_OBJECT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                         | <span data-ttu-id="2a949-108">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2a949-108">Required.</span></span> <span data-ttu-id="2a949-109">.</span><span class="sxs-lookup"><span data-stu-id="2a949-109">.</span></span>                                                                           |
| <span data-ttu-id="2a949-110">[übergeordnete WPD- \_ Objekt- \_ \_ ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a949-110">[WPD\_OBJECT\_PARENT\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                   | <span data-ttu-id="2a949-111">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2a949-111">Required.</span></span>                                                                             |
| <span data-ttu-id="2a949-112">[WPD- \_ Objekt \_ Name](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a949-112">[WPD\_OBJECT\_NAME](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                   | <span data-ttu-id="2a949-113">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2a949-113">Required.</span></span>                                                                             |
| <span data-ttu-id="2a949-114">[\_ \_ persistente \_ eindeutige \_ ID für WPD-Objekt](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a949-114">[WPD\_OBJECT\_PERSISTENT\_UNIQUE\_ID](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span> | <span data-ttu-id="2a949-115">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2a949-115">Required.</span></span>                                                                             |
| <span data-ttu-id="2a949-116">[WPD- \_ Objekt \_ IsHidden](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a949-116">[WPD\_OBJECT\_ISHIDDEN](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="2a949-117">Erforderlich, wenn das Dienst Objekt dem Benutzer nicht angezeigt werden soll.</span><span class="sxs-lookup"><span data-stu-id="2a949-117">Required if the service object should not be shown to the user.</span></span>                       |
| <span data-ttu-id="2a949-118">[WPD- \_ Objekt \_ IsSystem](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a949-118">[WPD\_OBJECT\_ISSYSTEM](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="2a949-119">Erforderlich, wenn das Objekt ein Systemobjekt ist (z. b. eine Systemdatei).</span><span class="sxs-lookup"><span data-stu-id="2a949-119">Required if the object is a system object (for example, it represents a system file).</span></span> |
| <span data-ttu-id="2a949-120">[WPD- \_ Funktions \_ Objekt \_ Kategorie](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a949-120">[WPD\_FUNCTIONAL\_OBJECT\_CATEGORY](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>     | <span data-ttu-id="2a949-121">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2a949-121">Required.</span></span> <span data-ttu-id="2a949-122">Dies stellt den Geräte Diensttyp dar, z. b. Dienst Kontakte.</span><span class="sxs-lookup"><span data-stu-id="2a949-122">This represents the Device Service type, such as SERVICE Contacts.</span></span>          |
| <span data-ttu-id="2a949-123">[WPD- \_ Dienst \_ Version](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a949-123">[WPD\_SERVICE\_VERSION](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                       | <span data-ttu-id="2a949-124">Erforderlich.</span><span class="sxs-lookup"><span data-stu-id="2a949-124">Required.</span></span>                                                                             |
| <span data-ttu-id="2a949-125">[WPD \_ - \_ Speichertyp](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a949-125">[WPD\_STORAGE\_TYPE](/previous-versions/windows/hardware/drivers/ff597893(v=vs.85))</span></span>                                                | <span data-ttu-id="2a949-126">Erforderlich, wenn der Dienst zum Speichern von Objekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2a949-126">Required if the service is used to store objects.</span></span>                                     |
| <span data-ttu-id="2a949-127">[WPD- \_ Speicher \_ Kapazität](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="2a949-127">[WPD\_STORAGE\_CAPACITY](/previous-versions/windows/hardware/drivers/ff597865(v=vs.85))</span></span>                                    | <span data-ttu-id="2a949-128">Erforderlich, wenn der Dienst zum Speichern von Objekten verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2a949-128">Required if the service is used to store objects.</span></span>                                     |



 

## <a name="typical-resources"></a><span data-ttu-id="2a949-129">Typische Ressourcen</span><span class="sxs-lookup"><span data-stu-id="2a949-129">Typical Resources</span></span>

<span data-ttu-id="2a949-130">Diese Objekte Hosten in der Regel keine Ressourcen.</span><span class="sxs-lookup"><span data-stu-id="2a949-130">These objects typically do not host resources.</span></span>

## <a name="typical-formats"></a><span data-ttu-id="2a949-131">Typische Formate</span><span class="sxs-lookup"><span data-stu-id="2a949-131">Typical Formats</span></span>

<span data-ttu-id="2a949-132">In der folgenden Liste werden typische Formate identifiziert, die vom Dienst Objekt verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2a949-132">The following list identifies typical formats used by the Service object.</span></span> <span data-ttu-id="2a949-133">Dieses Objekt ist jedoch nicht auf diese Formate beschränkt.</span><span class="sxs-lookup"><span data-stu-id="2a949-133">However, this object is not limited to these formats.</span></span>

-   <span data-ttu-id="2a949-134">Das WPD- \_ Objekt \_ Format ist \_ nicht angegeben.</span><span class="sxs-lookup"><span data-stu-id="2a949-134">WPD\_OBJECT\_FORMAT\_UNSPECIFIED</span></span>

## <a name="related-topics"></a><span data-ttu-id="2a949-135">Zugehörige Themen</span><span class="sxs-lookup"><span data-stu-id="2a949-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2a949-136">**Anforderungen für Objekte**</span><span class="sxs-lookup"><span data-stu-id="2a949-136">**Requirements for Objects**</span></span>](requirements-for-objects.md)
</dt> </dl>

 

 
