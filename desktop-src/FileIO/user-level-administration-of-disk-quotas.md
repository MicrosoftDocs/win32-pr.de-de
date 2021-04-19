---
description: So erhalten Sie mehr freien Speicherplatz, nachdem Sie das Kontingent Kontingent überschritten haben.
ms.assetid: a73b6a11-36f1-4437-a83d-e89918b1b0ae
title: Verwaltung von Datenträger Kontingenten auf Benutzerebene
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0cc130cf925899ccf0a86af20ff6772689ecdfbd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "106356978"
---
# <a name="user-level-administration-of-disk-quotas"></a><span data-ttu-id="fa094-103">Verwaltung von Datenträger Kontingenten auf Benutzerebene</span><span class="sxs-lookup"><span data-stu-id="fa094-103">User-level Administration of Disk Quotas</span></span>

<span data-ttu-id="fa094-104">Datenträger Kontingente sind für den Benutzer transparent.</span><span class="sxs-lookup"><span data-stu-id="fa094-104">Disk quotas are transparent to the user.</span></span> <span data-ttu-id="fa094-105">Wenn ein Benutzer fragt, wie viel Speicherplatz auf einem Datenträger frei ist, meldet das System nur die verfügbare Kontingent Menge, die dem Benutzer zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="fa094-105">When a user asks how much space is free on a disk, the system reports only the available quota allowance the user has available.</span></span> <span data-ttu-id="fa094-106">Wenn der Benutzer dieses Kontingent überschreitet, gibt das System den Fehler Datenträger " **\_ \_ vollständig** " zurück, so wie er darauf hindeuten würde, dass der Datenträger voll ist.</span><span class="sxs-lookup"><span data-stu-id="fa094-106">If the user exceeds this allowance, the system returns the **ERROR\_DISK\_FULL** error, just as it would to indicate that the disk was full.</span></span>

<span data-ttu-id="fa094-107">Der Benutzer muss einen der folgenden Schritte ausführen, um mehr freien Speicherplatz zu erhalten, nachdem das Kontingent Kontingent überschritten wurde:</span><span class="sxs-lookup"><span data-stu-id="fa094-107">To obtain more free disk space after exceeding the quota allowance, the user must do one of the following:</span></span>

-   <span data-ttu-id="fa094-108">Löschen Sie einige Dateien.</span><span class="sxs-lookup"><span data-stu-id="fa094-108">Delete some files.</span></span>
-   <span data-ttu-id="fa094-109">Einen anderen Benutzer beanspruchen den Besitz einiger Dateien.</span><span class="sxs-lookup"><span data-stu-id="fa094-109">Have another user claim ownership of some files.</span></span>
-   <span data-ttu-id="fa094-110">Lassen Sie den Administrator das Kontingent Kontingent erhöhen.</span><span class="sxs-lookup"><span data-stu-id="fa094-110">Have the administrator increase the quota allowance.</span></span>

<span data-ttu-id="fa094-111">Programme, die den tatsächlichen Umfang des freien Speicherplatzes abrufen müssen, können die [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) -Funktion aufrufen und den *totalnumoffreebytes* -Parameter überprüfen.</span><span class="sxs-lookup"><span data-stu-id="fa094-111">Programs that need to retrieve the actual amount of free disk space can call the [**GetDiskFreeSpaceEx**](/windows/desktop/api/FileAPI/nf-fileapi-getdiskfreespaceexa) function and look at the *TotalNumberOfFreeBytes* parameter.</span></span>

 

 



