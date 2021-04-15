---
description: Mit Datenträger Kontingenten verwendete Schnittstellen.
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: Schnittstellen für Festplattenkontingente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104485622"
---
# <a name="disk-quota-interfaces"></a><span data-ttu-id="60b35-103">Schnittstellen für Festplattenkontingente</span><span class="sxs-lookup"><span data-stu-id="60b35-103">Disk Quota Interfaces</span></span>

<span data-ttu-id="60b35-104">Die folgenden Schnittstellen werden mit Datenträger Kontingenten verwendet.</span><span class="sxs-lookup"><span data-stu-id="60b35-104">The following interfaces are used with disk quotas.</span></span>



| <span data-ttu-id="60b35-105">Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="60b35-105">Interface</span></span>                                          | <span data-ttu-id="60b35-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="60b35-106">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="60b35-107">**Idiskquotacontrol**</span><span class="sxs-lookup"><span data-stu-id="60b35-107">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | <span data-ttu-id="60b35-108">Steuert die Festplattenkontingent-Einrichtungen eines einzelnen NTFS-Dateisystem Volumes.</span><span class="sxs-lookup"><span data-stu-id="60b35-108">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="60b35-109">**Idiskquotaevents**</span><span class="sxs-lookup"><span data-stu-id="60b35-109">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | <span data-ttu-id="60b35-110">Empfängt Kontingent bezogene Ereignis Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="60b35-110">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="60b35-111">**Idiskquotauser**</span><span class="sxs-lookup"><span data-stu-id="60b35-111">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | <span data-ttu-id="60b35-112">Stellt einen einzelnen Benutzer Kontingent Eintrag in der Volumekontingent-Informationsdatei dar.</span><span class="sxs-lookup"><span data-stu-id="60b35-112">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="60b35-113">**Idiskquotauserbatch**</span><span class="sxs-lookup"><span data-stu-id="60b35-113">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | <span data-ttu-id="60b35-114">Fügt einem Container, der in einem einzelnen-Befehl zur Aktualisierung übermittelt wird, mehrere Kontingent Benutzer Objekte hinzu.</span><span class="sxs-lookup"><span data-stu-id="60b35-114">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="60b35-115">**Ienumdiskquotauszer**</span><span class="sxs-lookup"><span data-stu-id="60b35-115">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | <span data-ttu-id="60b35-116">Listet Benutzer Kontingent Einträge auf dem Volume auf.</span><span class="sxs-lookup"><span data-stu-id="60b35-116">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

