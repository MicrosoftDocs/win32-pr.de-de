---
description: In der Datenträgerverwaltung verwendete Schnittstellen.
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: Datenträger Verwaltungs Schnittstellen
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104217656"
---
# <a name="disk-management-interfaces"></a><span data-ttu-id="f5288-103">Datenträger Verwaltungs Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f5288-103">Disk Management Interfaces</span></span>

<span data-ttu-id="f5288-104">Die folgenden Schnittstellen werden in der Datenträgerverwaltung verwendet.</span><span class="sxs-lookup"><span data-stu-id="f5288-104">The following interfaces are used in disk management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f5288-105">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f5288-105">In this section</span></span>



| <span data-ttu-id="f5288-106">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="f5288-106">Interface</span></span>                                                     | <span data-ttu-id="f5288-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f5288-107">Description</span></span>                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f5288-108">**Idiskquotacontrol**</span><span class="sxs-lookup"><span data-stu-id="f5288-108">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | <span data-ttu-id="f5288-109">Steuert die Festplattenkontingent-Einrichtungen eines einzelnen NTFS-Dateisystem Volumes.</span><span class="sxs-lookup"><span data-stu-id="f5288-109">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="f5288-110">**Idiskquotaevents**</span><span class="sxs-lookup"><span data-stu-id="f5288-110">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | <span data-ttu-id="f5288-111">Empfängt Kontingent bezogene Ereignis Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="f5288-111">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="f5288-112">**Idiskquotauser**</span><span class="sxs-lookup"><span data-stu-id="f5288-112">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | <span data-ttu-id="f5288-113">Stellt einen einzelnen Benutzer Kontingent Eintrag in der Volumekontingent-Informationsdatei dar.</span><span class="sxs-lookup"><span data-stu-id="f5288-113">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="f5288-114">**Idiskquotauserbatch**</span><span class="sxs-lookup"><span data-stu-id="f5288-114">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | <span data-ttu-id="f5288-115">Fügt einem Container, der in einem einzelnen-Befehl zur Aktualisierung übermittelt wird, mehrere Kontingent Benutzer Objekte hinzu.</span><span class="sxs-lookup"><span data-stu-id="f5288-115">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="f5288-116">**Ienumdiskquotauszer**</span><span class="sxs-lookup"><span data-stu-id="f5288-116">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | <span data-ttu-id="f5288-117">Listet Benutzer Kontingent Einträge auf dem Volume auf.</span><span class="sxs-lookup"><span data-stu-id="f5288-117">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

