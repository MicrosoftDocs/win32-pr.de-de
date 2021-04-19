---
description: Listet die von der Anlage-Engine bereitgestellten Schnittstellen auf.
ms.assetid: 451587bd-a7ab-446b-b647-be98de251915
title: Sicherheits Verwaltungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9b3a205757a3bf324a5308a5f6fbc3d63374b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106373243"
---
# <a name="security-management-interfaces"></a><span data-ttu-id="a6a4e-103">Sicherheits Verwaltungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="a6a4e-103">Security Management Interfaces</span></span>

<span data-ttu-id="a6a4e-104">Dieser Abschnitt enthält Referenzseiten für die folgenden Gruppen von Schnittstellen:</span><span class="sxs-lookup"><span data-stu-id="a6a4e-104">This section contains reference pages for the following groups of interfaces:</span></span>

-   [<span data-ttu-id="a6a4e-105">Schnittstellen des Anlagen Moduls</span><span class="sxs-lookup"><span data-stu-id="a6a4e-105">Attachment Engine Interfaces</span></span>](#attachment-engine-interfaces)

## <a name="attachment-engine-interfaces"></a><span data-ttu-id="a6a4e-106">Schnittstellen des Anlagen Moduls</span><span class="sxs-lookup"><span data-stu-id="a6a4e-106">Attachment Engine Interfaces</span></span>



| <span data-ttu-id="a6a4e-107">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="a6a4e-107">Interface</span></span>                                                            | <span data-ttu-id="a6a4e-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a6a4e-108">Description</span></span>                                                                                                                                                                                                                                                                                                                |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a6a4e-109">**Iscesvstreamtachmentdata**</span><span class="sxs-lookup"><span data-stu-id="a6a4e-109">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)               | <span data-ttu-id="a6a4e-110">Ruft Konfigurations-und Analysedaten zu einem angegebenen Sicherheitsdienst aus den Snap-Ins für die Sicherheitskonfiguration ab. Die Sicherheitskonfigurations-Snap-Ins machen diese Schnittstelle verfügbar, welche Anlagen-Snap-in-Erweiterungen zum Abfragen von Konfigurations-oder Analyse Informationen aufruft.</span><span class="sxs-lookup"><span data-stu-id="a6a4e-110">Retrieves configuration and analysis data about a specified security service from the Security Configuration snap-ins. The Security Configuration snap-ins expose this interface, which attachment snap-in extensions call to query configuration or analysis information.</span></span>                                                 |
| [<span data-ttu-id="a6a4e-111">**Iscesvplattachmentpersistinfo**</span><span class="sxs-lookup"><span data-stu-id="a6a4e-111">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) | <span data-ttu-id="a6a4e-112">Ruft geänderte Konfigurations-oder Analyse Informationen von einem Anlage-Snap-in ab.</span><span class="sxs-lookup"><span data-stu-id="a6a4e-112">Retrieves modified configuration or analysis information from an attachment snap-in.</span></span> <span data-ttu-id="a6a4e-113">Mithilfe der Sicherheitskonfigurations-Snap-Ins wird diese Schnittstelle aufgerufen, um geänderte Informationen aus der Erweiterungs-Snap-in-Erweiterung abzurufen.</span><span class="sxs-lookup"><span data-stu-id="a6a4e-113">The Security Configuration snap-ins calls this interface to retrieve any modified information from the attachment snap-in extension.</span></span> <span data-ttu-id="a6a4e-114">Das Sicherheitskonfigurations-Snap-in speichert diese Daten dann entsprechend in der Sicherheitsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="a6a4e-114">The Security Configuration snap-in then stores this data appropriately in the security database.</span></span> |



 

<span data-ttu-id="a6a4e-115">Weitere Informationen zu den COM-Schnittstellen, die von Snap-in-Erweiterungen implementiert werden müssen, finden Sie in der Dokumentation zu [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) .</span><span class="sxs-lookup"><span data-stu-id="a6a4e-115">For more information about the COM interfaces that must be implemented by snap-in extensions, see the [Microsoft Management Console](/previous-versions/windows/desktop/mmc/microsoft-management-console-start-page) documentation.</span></span>

 

 
