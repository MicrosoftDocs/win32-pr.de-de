---
description: Werte werden vom dwOptions-Parameter von wlxloggedoutsas verwendet.
ms.assetid: a146427b-f3f1-4221-b2eb-ee7da451314a
title: WLX_LOGON_OPTION_XXX (winwlx. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fa8909f562b87eb3a8147b0684d9676b9ac55d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104347138"
---
# <a name="wlx_logon_option_xxx"></a><span data-ttu-id="354c9-103">wlx- \_ Anmelde \_ Option \_ xxx</span><span class="sxs-lookup"><span data-stu-id="354c9-103">WLX\_LOGON\_OPTION\_XXX</span></span>

<span data-ttu-id="354c9-104">\[Die Konstante der wlx- \_ Anmelde \_ Option \_ xxx ist nicht mehr für die Verwendung ab Windows Server 2008 und Windows Vista verfügbar.\]</span><span class="sxs-lookup"><span data-stu-id="354c9-104">\[The WLX\_LOGON\_OPTION\_XXX constant is no longer available for use as of Windows Server 2008 and Windows Vista.\]</span></span>

<span data-ttu-id="354c9-105">Die **wlx- \_ Anmelde \_ Option \_ xxx** -Werte werden vom *dwOptions* -Parameter von [**wlxloggedoutsas**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas)verwendet.</span><span class="sxs-lookup"><span data-stu-id="354c9-105">The **WLX\_LOGON\_OPTION\_XXX** values are used by the *dwOptions* parameter of [**WlxLoggedOutSAS**](/windows/desktop/api/Winwlx/nf-winwlx-wlxloggedoutsas).</span></span>

> [!Note]  
> <span data-ttu-id="354c9-106">Gina-DLLs werden in Windows Vista ignoriert.</span><span class="sxs-lookup"><span data-stu-id="354c9-106">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="354c9-107">Bei erfolgreicher Anmeldung kann die Gina-DLL diesen Wert verwenden, um die folgende Option anzugeben.</span><span class="sxs-lookup"><span data-stu-id="354c9-107">Upon a successful logon, your GINA DLL can use this value to specify the following option.</span></span>



| <span data-ttu-id="354c9-108">Konstante</span><span class="sxs-lookup"><span data-stu-id="354c9-108">Constant</span></span>                                                                                                                                                                                          | <span data-ttu-id="354c9-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="354c9-109">Description</span></span>                                                                                                                                                                      |
|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WLX_LOGON_OPT_NO_PROFILE"></span><span id="wlx_logon_opt_no_profile"></span><dl> <span data-ttu-id="354c9-110"><dt>**wlx \_ - \_ Anmeldung \_ ohne \_ Profil**</dt></span><span class="sxs-lookup"><span data-stu-id="354c9-110"><dt>**WLX\_LOGON\_OPT\_NO\_PROFILE**</dt></span></span> </dl> | <span data-ttu-id="354c9-111">Gibt an, dass Winlogon kein Profil für den angemeldeten Benutzer laden darf.</span><span class="sxs-lookup"><span data-stu-id="354c9-111">Specifies that Winlogon must not load a profile for the logged-on user.</span></span> <span data-ttu-id="354c9-112">In diesem Fall lädt entweder Ihre GINA-DLL das Profil, oder der Benutzer benötigt kein Profil.</span><span class="sxs-lookup"><span data-stu-id="354c9-112">In this case, either your GINA DLL will load the profile or the user does not need a profile.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="354c9-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="354c9-113">Requirements</span></span>



| <span data-ttu-id="354c9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="354c9-114">Requirement</span></span> | <span data-ttu-id="354c9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="354c9-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="354c9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="354c9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="354c9-117">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="354c9-117">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="354c9-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="354c9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="354c9-119">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="354c9-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="354c9-120">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="354c9-120">End of client support</span></span><br/>    | <span data-ttu-id="354c9-121">Windows XP</span><span class="sxs-lookup"><span data-stu-id="354c9-121">Windows XP</span></span><br/>                                                               |
| <span data-ttu-id="354c9-122">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="354c9-122">End of server support</span></span><br/>    | <span data-ttu-id="354c9-123">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="354c9-123">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="354c9-124">Header</span><span class="sxs-lookup"><span data-stu-id="354c9-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="354c9-125"><dt>Winwlx. h</dt></span><span class="sxs-lookup"><span data-stu-id="354c9-125"><dt>Winwlx.h</dt></span></span> </dl> |



 

 




