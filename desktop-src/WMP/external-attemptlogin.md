---
title: Extern.-Anmelde Methode
description: Mit der Methode "Methode" wird ein Dialogfeld angezeigt, in dem der Benutzer versuchen kann, sich beim Online Shop anzumelden.
ms.assetid: 04fe476f-6d0e-4faa-9e4a-f87bed782205
keywords:
- Media Player der Methode "Methode"
- Methode "-Anmeldung", Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, Methode "Methode anmelden"
topic_type:
- apiref
api_name:
- External.attemptLogin
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 86958c241f2399efbe342371b8cd4cfd376ff628
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357688"
---
# <a name="externalattemptlogin-method"></a><span data-ttu-id="29c3f-106">Extern.-Anmelde Methode</span><span class="sxs-lookup"><span data-stu-id="29c3f-106">External.attemptLogin method</span></span>

<span data-ttu-id="29c3f-107">Mit **der Methode "** Methode" wird ein Dialogfeld angezeigt, in dem der Benutzer versuchen kann, sich beim Online Shop anzumelden.</span><span class="sxs-lookup"><span data-stu-id="29c3f-107">The **attemptLogin** method displays a dialog box so the user can attempt to log in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="29c3f-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="29c3f-108">Syntax</span></span>


```JScript
External.attemptLogin()
```



## <a name="parameters"></a><span data-ttu-id="29c3f-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="29c3f-109">Parameters</span></span>

<span data-ttu-id="29c3f-110">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="29c3f-110">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="29c3f-111">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="29c3f-111">Return value</span></span>

<span data-ttu-id="29c3f-112">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="29c3f-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="29c3f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="29c3f-113">Remarks</span></span>

<span data-ttu-id="29c3f-114">Wenn der Anmeldeversuch zu einer Änderung des Anmeldestatus führt, löst Windows Media Player das [onloginchange](external-onloginchange-event.md) -Ereignis aus.</span><span class="sxs-lookup"><span data-stu-id="29c3f-114">If the log-in attempt results in a change of log-in status, Windows Media Player raises the [OnLoginChange](external-onloginchange-event.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="29c3f-115">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="29c3f-115">Requirements</span></span>



| <span data-ttu-id="29c3f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="29c3f-116">Requirement</span></span> | <span data-ttu-id="29c3f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="29c3f-117">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="29c3f-118">Version</span><span class="sxs-lookup"><span data-stu-id="29c3f-118">Version</span></span><br/> | <span data-ttu-id="29c3f-119">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="29c3f-119">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="29c3f-120">DLL</span><span class="sxs-lookup"><span data-stu-id="29c3f-120">DLL</span></span><br/>     | <dl> <span data-ttu-id="29c3f-121"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="29c3f-121"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="29c3f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="29c3f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="29c3f-123">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="29c3f-123">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="29c3f-124">**Externes. onloginchange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="29c3f-124">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> <dt>

[<span data-ttu-id="29c3f-125">**Extern. userloggedin**</span><span class="sxs-lookup"><span data-stu-id="29c3f-125">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> <dt>

[<span data-ttu-id="29c3f-126">**Iwmpcontentpartner:: Login**</span><span class="sxs-lookup"><span data-stu-id="29c3f-126">**IWMPContentPartner::Login**</span></span>](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-login)
</dt> <dt>

[<span data-ttu-id="29c3f-127">**Verwalten der Anmeldung**</span><span class="sxs-lookup"><span data-stu-id="29c3f-127">**Managing Login**</span></span>](managing-login.md)
</dt> </dl>

 

 





