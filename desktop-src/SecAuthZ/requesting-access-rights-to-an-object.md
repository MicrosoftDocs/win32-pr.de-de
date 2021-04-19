---
description: Wenn Sie ein Handle für ein Objekt öffnen, verfügt das zurückgegebene Handle über eine bestimmte Kombination von Zugriffsrechten für das Objekt.
ms.assetid: 581de4ba-0f90-42d7-b7db-1324d42595e2
title: Anfordern von Zugriffsrechten für ein Objekt
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5eb2e13bd5f5e51ed194b60c6ab63d1eda8eddfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106360086"
---
# <a name="requesting-access-rights-to-an-object"></a><span data-ttu-id="ded52-103">Anfordern von Zugriffsrechten für ein Objekt</span><span class="sxs-lookup"><span data-stu-id="ded52-103">Requesting Access Rights to an Object</span></span>

<span data-ttu-id="ded52-104">Wenn Sie ein Handle für ein Objekt öffnen, verfügt das zurückgegebene Handle über eine bestimmte Kombination von Zugriffsrechten für das Objekt.</span><span class="sxs-lookup"><span data-stu-id="ded52-104">When you open a handle to an object, the returned handle has some combination of access rights to the object.</span></span> <span data-ttu-id="ded52-105">Einige Funktionen, wie z. b. " [**kreatesemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea)", benötigen keinen bestimmten Satz angeforderter Zugriffsrechte.</span><span class="sxs-lookup"><span data-stu-id="ded52-105">Some functions, such as [**CreateSemaphore**](/windows/desktop/api/winbase/nf-winbase-createsemaphorea), do not require a specific set of requested access rights.</span></span> <span data-ttu-id="ded52-106">Diese Funktionen versuchen immer, das Handle für den Vollzugriff zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ded52-106">These functions always try to open the handle for full access.</span></span> <span data-ttu-id="ded52-107">Andere Funktionen, wie z. b. " [**kreatefile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) " und " [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess)", ermöglichen es Ihnen, den gewünschten Satz von Zugriffsrechten anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ded52-107">Other functions, such as [**CreateFile**](/windows/desktop/api/fileapi/nf-fileapi-createfilea) and [**OpenProcess**](/windows/desktop/api/processthreadsapi/nf-processthreadsapi-openprocess), allow you to specify the set of access rights that you want.</span></span> <span data-ttu-id="ded52-108">Sie sollten nur die benötigten Zugriffsrechte anfordern, anstatt ein Handle für den Vollzugriff zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ded52-108">You should request only the access rights that you need, rather than opening a handle for full access.</span></span> <span data-ttu-id="ded52-109">Dadurch wird verhindert, dass das Handle unbeabsichtigt verwendet wird, und erhöht die Wahrscheinlichkeit, dass die Zugriffs Anforderung erfolgreich ist, wenn die DACL des Objekts nur eingeschränkten Zugriff zulässt.</span><span class="sxs-lookup"><span data-stu-id="ded52-109">This prevents using the handle in an unintended way, and increases the chances that the access request will succeed if the object's DACL only allows limited access.</span></span>

<span data-ttu-id="ded52-110">Verwenden Sie [generische Zugriffsrechte](generic-access-rights.md) , um den Zugriffstyp anzugeben, der beim Öffnen eines Handles für ein Objekt erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ded52-110">Use [generic access rights](generic-access-rights.md) to specify the type of access needed when opening a handle to an object.</span></span> <span data-ttu-id="ded52-111">Dies ist in der Regel einfacher, als alle entsprechenden Standard-und spezifischen Rechte anzugeben.</span><span class="sxs-lookup"><span data-stu-id="ded52-111">This is typically simpler than specifying all the corresponding standard and specific rights.</span></span> <span data-ttu-id="ded52-112">Verwenden Sie alternativ die maximal \_ zulässige Konstante, um anzufordern, dass das Objekt mit allen Zugriffsrechten geöffnet wird, die für den Aufrufer gültig sind.</span><span class="sxs-lookup"><span data-stu-id="ded52-112">Alternatively, use the MAXIMUM\_ALLOWED constant to request that the object be opened with all the access rights that are valid for the caller.</span></span>

> [!Note]  
> <span data-ttu-id="ded52-113">Die maximal \_ zulässige Konstante kann nicht in einem ACE verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ded52-113">The MAXIMUM\_ALLOWED constant cannot be used in an ACE.</span></span>

 

<span data-ttu-id="ded52-114">Um die SACL in der [*Sicherheits Beschreibung*](/windows/desktop/SecGloss/s-gly)eines Objekts zu erhalten oder festzulegen, fordern Sie beim Öffnen eines Handles für das Objekt das [Zugriffs \_ System- \_ Sicherheits Zugriffsrecht](sacl-access-right.md) an.</span><span class="sxs-lookup"><span data-stu-id="ded52-114">To get or set the SACL in an object's [*security descriptor*](/windows/desktop/SecGloss/s-gly), request the [ACCESS\_SYSTEM\_SECURITY access right](sacl-access-right.md) when opening a handle to the object.</span></span>

 

 
