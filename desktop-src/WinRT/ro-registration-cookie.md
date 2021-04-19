---
description: Stellt Aktivierungs Factorys dar, die durch Aufrufen der Funktion roregisteractivationfactorys registriert werden.
ms.assetid: D74E5886-45DB-40DE-9740-D14341E78713
title: RO_REGISTRATION_COOKIE (roapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fe9b5242901c1beff4152bc16108976d6f7de275
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106348396"
---
# <a name="ro_registration_cookie"></a><span data-ttu-id="912be-103">Registrierungs Cookie für die \_ Registrierung \_</span><span class="sxs-lookup"><span data-stu-id="912be-103">RO\_REGISTRATION\_COOKIE</span></span>

<span data-ttu-id="912be-104">Stellt Aktivierungs Factorys dar, die durch Aufrufen der Funktion [**roregisteractivationfactorys**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) registriert werden.</span><span class="sxs-lookup"><span data-stu-id="912be-104">Represents activation factories that are registered by calling the [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function.</span></span>


```C++
typedef struct {}* RO_REGISTRATION_COOKIE;
```



## <a name="remarks"></a><span data-ttu-id="912be-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="912be-105">Remarks</span></span>

<span data-ttu-id="912be-106">Die Funktion [**roregisteractivationfactorys**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) gibt ein **\_ Registrierungs \_ Cookie für Registrierungs** stellen zurück, wenn eine aktivierbare Klassenfactorys beim Windows-Runtime registriert sind.</span><span class="sxs-lookup"><span data-stu-id="912be-106">The [**RoRegisterActivationFactories**](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories) function returns a **RO\_REGISTRATION\_COOKIE** when a activatable class factories are registered with the Windows Runtime.</span></span> <span data-ttu-id="912be-107">Die [**rorevokeactivationfactoryfunktion**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) verwendet das Cookie, um die Klassenfactorys zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="912be-107">The [**RoRevokeActivationFactories**](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories) function uses the cookie to remove the class factories.</span></span>

## <a name="requirements"></a><span data-ttu-id="912be-108">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="912be-108">Requirements</span></span>



| <span data-ttu-id="912be-109">Anforderung</span><span class="sxs-lookup"><span data-stu-id="912be-109">Requirement</span></span> | <span data-ttu-id="912be-110">Wert</span><span class="sxs-lookup"><span data-stu-id="912be-110">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="912be-111">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="912be-111">Minimum supported client</span></span><br/> | <span data-ttu-id="912be-112">Windows 8</span><span class="sxs-lookup"><span data-stu-id="912be-112">Windows 8</span></span><br/>                                                               |
| <span data-ttu-id="912be-113">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="912be-113">Minimum supported server</span></span><br/> | <span data-ttu-id="912be-114">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="912be-114">Windows Server 2012</span></span><br/>                                                     |
| <span data-ttu-id="912be-115">Header</span><span class="sxs-lookup"><span data-stu-id="912be-115">Header</span></span><br/>                   | <dl> <span data-ttu-id="912be-116"><dt>Roapi. h</dt></span><span class="sxs-lookup"><span data-stu-id="912be-116"><dt>Roapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="912be-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="912be-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="912be-118">**Roregisteractivationfactorys**</span><span class="sxs-lookup"><span data-stu-id="912be-118">**RoRegisterActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-roregisteractivationfactories)
</dt> <dt>

[<span data-ttu-id="912be-119">**Rorevokeactivationfactorys**</span><span class="sxs-lookup"><span data-stu-id="912be-119">**RoRevokeActivationFactories**</span></span>](/windows/win32/api/roapi/nf-roapi-rorevokeactivationfactories)
</dt> </dl>

 

 
