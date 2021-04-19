---
description: Administratoren können die Menge der Daten steuern, die von den einzelnen Benutzern auf einem NTFS-Dateisystem Volume gespeichert werden können.
ms.assetid: 42efbd5b-6455-4319-a76e-cdb666fc36b8
title: Verwalten der Datenträger Kontingente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5231d7683f0af40e7006193be8d5ff9390e21b65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106363719"
---
# <a name="managing-disk-quotas"></a><span data-ttu-id="6d8bf-103">Verwalten der Datenträger Kontingente</span><span class="sxs-lookup"><span data-stu-id="6d8bf-103">Managing Disk Quotas</span></span>

<span data-ttu-id="6d8bf-104">Das NTFS-Dateisystem unterstützt Datenträger *Kontingente*, mit denen Administratoren die Menge der Daten steuern können, die von den einzelnen Benutzern auf einem NTFS-Dateisystem Volume gespeichert werden können.</span><span class="sxs-lookup"><span data-stu-id="6d8bf-104">The NTFS file system supports *disk quotas*, which allow administrators to control the amount of data that each user can store on an NTFS file system volume.</span></span> <span data-ttu-id="6d8bf-105">Administratoren können das System optional so konfigurieren, dass ein Ereignis protokolliert wird, wenn sich Benutzer in Ihrer Nähe befinden, und den Benutzern, die ihr Kontingent überschreiten, weiteren Speicherplatz verweigern.</span><span class="sxs-lookup"><span data-stu-id="6d8bf-105">Administrators can optionally configure the system to log an event when users are near their quota, and to deny further disk space to users who exceed their quota.</span></span> <span data-ttu-id="6d8bf-106">Administratoren können auch Berichte generieren und mit dem Ereignis Monitor Kontingent Probleme nachverfolgen.</span><span class="sxs-lookup"><span data-stu-id="6d8bf-106">Administrators can also generate reports, and use the event monitor to track quota issues.</span></span>

<span data-ttu-id="6d8bf-107">Sie können bestimmen, ob ein Dateisystem Datenträger Kontingente unterstützt, indem Sie die [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) -Funktion aufrufen und das Bitflag für die **Datei \_ Volumen \_ Kontingente** untersuchen.</span><span class="sxs-lookup"><span data-stu-id="6d8bf-107">You can determine whether a file system supports disk quotas by calling the [**GetVolumeInformation**](/windows/desktop/api/FileAPI/nf-fileapi-getvolumeinformationa) function and examining the **FILE\_VOLUME\_QUOTAS** bit flag.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6d8bf-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6d8bf-108">In this section</span></span>



| <span data-ttu-id="6d8bf-109">Thema</span><span class="sxs-lookup"><span data-stu-id="6d8bf-109">Topic</span></span>                                                                                                   | <span data-ttu-id="6d8bf-110">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6d8bf-110">Description</span></span>                                                                                                                                      |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d8bf-111">Verwaltung von Datenträger Kontingenten auf Benutzerebene</span><span class="sxs-lookup"><span data-stu-id="6d8bf-111">User-level Administration of Disk Quotas</span></span>](user-level-administration-of-disk-quotas.md)<br/>     | <span data-ttu-id="6d8bf-112">So erhalten Sie mehr freien Speicherplatz, nachdem Sie das Kontingent Kontingent überschritten haben.</span><span class="sxs-lookup"><span data-stu-id="6d8bf-112">How to get more free disk space after exceeding the quota allowance.</span></span><br/>                                                                  |
| [<span data-ttu-id="6d8bf-113">Verwaltung von Datenträger Kontingenten auf System Ebene</span><span class="sxs-lookup"><span data-stu-id="6d8bf-113">System-level Administration of Disk Quotas</span></span>](system-level-administration-of-disk-quotas.md)<br/> | <span data-ttu-id="6d8bf-114">Der Systemadministrator kann Kontingente für bestimmte Benutzer auf einem Volume festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d8bf-114">The system administrator can set quotas for specific users on a volume.</span></span> <span data-ttu-id="6d8bf-115">Der Administrator kann auch Standard Kontingente für das Volume festlegen.</span><span class="sxs-lookup"><span data-stu-id="6d8bf-115">The administrator can also set default quotas for the volume.</span></span><br/> |
| [<span data-ttu-id="6d8bf-116">Limits für Datenträger Kontingente</span><span class="sxs-lookup"><span data-stu-id="6d8bf-116">Disk Quota Limits</span></span>](disk-quota-limits.md)<br/>                                                   | <span data-ttu-id="6d8bf-117">Beschreibt zwei Arten von Datenträger Kontingent Limits und wie die Datenträger Kontingent Limits gemessen werden.</span><span class="sxs-lookup"><span data-stu-id="6d8bf-117">Describes two types of disk quota limits and how disk quota limits are measured.</span></span><br/>                                                      |
| [<span data-ttu-id="6d8bf-118">Schnittstellen für Festplattenkontingente</span><span class="sxs-lookup"><span data-stu-id="6d8bf-118">Disk Quota Interfaces</span></span>](disk-quota-interfaces.md)<br/>                                           | <span data-ttu-id="6d8bf-119">Mit Datenträger Kontingenten verwendete Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="6d8bf-119">Interfaces used with disk quotas.</span></span><br/>                                                                                                     |



 

 

 




