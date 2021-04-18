---
description: In Ihrer Snap-in-Erweiterung müssen die aktuellen Konfigurations-und Analyse Informationen für die Benutzer angezeigt werden.
ms.assetid: 503bc283-c1cd-4258-a27e-4046553882fa
title: Anzeigen von Konfigurations-und Analyse Informationen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc2f0d598ced5f789d9b417d79df591a71f82ab4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106357927"
---
# <a name="displaying-configuration-and-analysis-information"></a><span data-ttu-id="4216f-103">Anzeigen von Konfigurations-und Analyse Informationen</span><span class="sxs-lookup"><span data-stu-id="4216f-103">Displaying Configuration and Analysis Information</span></span>

<span data-ttu-id="4216f-104">In Ihrer Snap-in-Erweiterung müssen die aktuellen Konfigurations-und Analyse Informationen für die Benutzer angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="4216f-104">Your snap-in extension must display the current configuration and analysis information to the users.</span></span>

<span data-ttu-id="4216f-105">Zum Anzeigen von Informationen muss der Erweiterungs Knoten "Anlagen-Snap-in" die Sicherheitskonfigurations-Snap-Ins mithilfe des Knotens "Dienste" erweitern.</span><span class="sxs-lookup"><span data-stu-id="4216f-105">To display information, the attachment snap-in extension node must extend the Security Configuration snap-ins using the Services node.</span></span> <span data-ttu-id="4216f-106">Der Knoten Dienste ist das MMC-Snap-in, mit dem die auf dem System installierten Dienste verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="4216f-106">The Services node is the MMC snap-in that administers services installed on the system.</span></span>

<span data-ttu-id="4216f-107">Die Knoten Typen, die erweitert werden können, lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4216f-107">The node types that can be extended are as follows:</span></span>

-   <span data-ttu-id="4216f-108">Konfigurations Dienste NodeType = {24a7f 717-1F-c-11d1-affb-00c04tb984f 9}</span><span class="sxs-lookup"><span data-stu-id="4216f-108">Configuration Services NodeType={24a7f717-1f0c-11d1-affb-00c04fb984f9}</span></span>
-   <span data-ttu-id="4216f-109">Inspektionsdienste NodeType = {678050c7-1ff8-11d1-affb-00C04FB984F9}</span><span class="sxs-lookup"><span data-stu-id="4216f-109">Inspection Services NodeType={678050c7-1ff8-11d1-affb-00c04fb984f9}</span></span>

<span data-ttu-id="4216f-110">Wenn der Knoten Dienste erweitert wird, benachrichtigt die MMC alle registrierten Snap-in-Erweiterungen.</span><span class="sxs-lookup"><span data-stu-id="4216f-110">When the Services node is expanded, the MMC notifies all registered snap-in extensions.</span></span> <span data-ttu-id="4216f-111">Jedes Anlage-Snap-in sollte sich selbst unter dem Knoten Dienste einfügen und die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="4216f-111">Each attachment snap-in should insert itself under the Services node, and perform the following tasks:</span></span>

-   <span data-ttu-id="4216f-112">Ruft **QueryInterface** auf, um einen Zeiger auf die [**iscesvcalltachmentdata**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) -Schnittstelle abzurufen, die von den Sicherheitskonfigurations-Snap-Ins verfügbar gemacht wird.</span><span class="sxs-lookup"><span data-stu-id="4216f-112">Call **QueryInterface** to get a pointer to the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) interface exposed by the Security Configuration snap-ins.</span></span>
-   <span data-ttu-id="4216f-113">Wenden Sie [**iscesvcalltachmentdata:: Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) an, um die Sicherheitskonfigurations-Snap-Ins zu informieren, dass die Snap-in-Erweiterung geladen ist, und um einen Kontext für die Kommunikation zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4216f-113">Call [**ISceSvcAttachmentData::Initialize**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-initialize) to inform the Security Configuration snap-ins that the snap-in extension is loaded and to establish a context for communications.</span></span>
-   <span data-ttu-id="4216f-114">Rufen Sie [**iscesvasetachmentdata:: GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) auf, um Konfigurationsinformationen aus der Datenbank abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4216f-114">Call [**ISceSvcAttachmentData::GetData**](/windows/desktop/api/Scesvc/nf-scesvc-iscesvcattachmentdata-getdata) to retrieve configuration information from the database.</span></span> <span data-ttu-id="4216f-115">Dieser Schritt kann entweder ausgeführt werden, wenn die Snap-in-Erweiterung selbst initialisiert wird oder wenn der Benutzer den Knoten öffnet.</span><span class="sxs-lookup"><span data-stu-id="4216f-115">This step can be performed either when the snap-in extension initializes itself or when the user opens its node.</span></span>

<span data-ttu-id="4216f-116">Weitere Informationen finden Sie unter [Hinzufügen eines Erweiterungs Knotens für einen Anlagen-Snap-in](adding-an-attachment-snap-in-extension-node.md).</span><span class="sxs-lookup"><span data-stu-id="4216f-116">For more information, see [Adding an Attachment Snap-in Extension Node](adding-an-attachment-snap-in-extension-node.md).</span></span>

 

 



