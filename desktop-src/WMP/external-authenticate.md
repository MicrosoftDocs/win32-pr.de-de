---
title: Extern. Authenticate-Methode
description: Die authentifizieren-Methode initiiert den Versuch, den Benutzer zu authentifizieren.
ms.assetid: db4cd2c6-b735-40b1-af96-82a40bda9d97
keywords:
- Authentifizieren von Methoden Fenster Media Player
- authentifizieren-Methode, Windows Media Player, externe Klasse
- Externe Klasse, Windows Media Player, authentifizieren-Methode
topic_type:
- apiref
api_name:
- External.authenticate
api_location:
- wmp.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aa2bba0afb80c4285ad8fa8d2c20191321315d60
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106356492"
---
# <a name="externalauthenticate-method"></a><span data-ttu-id="96fda-106">Extern. Authenticate-Methode</span><span class="sxs-lookup"><span data-stu-id="96fda-106">External.authenticate method</span></span>

<span data-ttu-id="96fda-107">Die **Authentifizieren** -Methode initiiert den Versuch, den Benutzer zu authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="96fda-107">The **authenticate** method initiates an attempt to authenticate the user.</span></span>

## <a name="syntax"></a><span data-ttu-id="96fda-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="96fda-108">Syntax</span></span>


```JScript
External.authenticate(
  AuthenticationIndex
)
```



## <a name="parameters"></a><span data-ttu-id="96fda-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="96fda-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="96fda-110">*Authenticationindex* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="96fda-110">*AuthenticationIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="96fda-111">**Number** (**Long**), der den Index einer Webseite mit Authentifizierungs Erfolg angibt.</span><span class="sxs-lookup"><span data-stu-id="96fda-111">**Number** (**long**) that specifies the index of an authentication-success webpage.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="96fda-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="96fda-112">Return value</span></span>

<span data-ttu-id="96fda-113">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="96fda-113">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="96fda-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96fda-114">Remarks</span></span>

<span data-ttu-id="96fda-115">Bestimmte Links auf einer Ermittlungs Seite haben Ziele, die erst angezeigt werden sollen, nachdem der Benutzer authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="96fda-115">Certain links on a discovery page have targets that should be displayed only after the user has been authenticated.</span></span> <span data-ttu-id="96fda-116">Die Seite Ermittlung, Windows Media Player und das Plug-in für den Online Store führen die folgenden Schritte aus, um den Benutzer zu authentifizieren und die Zielwebseite anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="96fda-116">The discovery page, Windows Media Player, and the online store's plug-in use the following steps to authenticate the user and display the target webpage:</span></span>

1.  <span data-ttu-id="96fda-117">Bei einem Skript auf einer Ermittlungs Seite wird die *externe* aufgerufen. **Authentifizieren** -Methode.</span><span class="sxs-lookup"><span data-stu-id="96fda-117">Script on a discovery page calls the *External*.**authenticate** method.</span></span>
2.  <span data-ttu-id="96fda-118">Windows Media Player zeigt ein Dialogfeld an, in dem Sie einen Benutzernamen und ein Kennwort erhalten.</span><span class="sxs-lookup"><span data-stu-id="96fda-118">Windows Media Player displays a dialog box to obtain a user name and password.</span></span>
3.  <span data-ttu-id="96fda-119">Windows Media Player ruft [iwmpcontentpartner:: Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate)auf, wodurch der Authentifizierungs Versuch initiiert und sofort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="96fda-119">Windows Media Player calls [IWMPContentPartner::Authenticate](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-authenticate), which initiates the authentication attempt and returns immediately.</span></span>
4.  <span data-ttu-id="96fda-120">Wenn der Authentifizierungs Versuch abgeschlossen ist, ruft das Plug-in des Online Stores [iwmpcontentpartnercallback:: notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify)auf und übergibt dabei wmpcnauthresult und einen booleschen Wert, der angibt, ob der Versuch erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="96fda-120">When the authentication attempt is complete, the online store's plug-in calls [IWMPContentPartnerCallback::Notify](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartnercallback-notify), passing wmpcnAuthResult and a Boolean value that indicates whether the attempt was successful.</span></span>
5.  <span data-ttu-id="96fda-121">Wenn der Authentifizierungs Versuch erfolgreich war, ruft Windows Media Player [iwmpcontentpartner:: getiteminfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)auf und übergibt g \_ sziteminfo \_ authenticationerfolgreiches URL, um die URL einer Webseite mit Authentifizierungs Erfolg zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="96fda-121">If the authentication attempt was successful, Windows Media Player calls [IWMPContentPartner::GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo), passing g\_szItemInfo\_AuthenticationSuccessURL, to obtain the URL of an authentication-success webpage.</span></span> <span data-ttu-id="96fda-122">In diesem-Befehl übergibt Windows Media Player denselben Index, der von der Ermittlungs Seite an den *externen* weitergegeben wurde. **Authentifizieren** -Methode.</span><span class="sxs-lookup"><span data-stu-id="96fda-122">In this call, Windows Media Player passes the same index that the discovery page passed to the *External*.**authenticate** method.</span></span>
6.  <span data-ttu-id="96fda-123">Windows Media Player zeigt die Webseite Authentifizierung-Erfolg an.</span><span class="sxs-lookup"><span data-stu-id="96fda-123">Windows Media Player displays the authentication-success webpage.</span></span>

## <a name="requirements"></a><span data-ttu-id="96fda-124">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="96fda-124">Requirements</span></span>



| <span data-ttu-id="96fda-125">Anforderung</span><span class="sxs-lookup"><span data-stu-id="96fda-125">Requirement</span></span> | <span data-ttu-id="96fda-126">Wert</span><span class="sxs-lookup"><span data-stu-id="96fda-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="96fda-127">Version</span><span class="sxs-lookup"><span data-stu-id="96fda-127">Version</span></span><br/> | <span data-ttu-id="96fda-128">Windows Media Player 11</span><span class="sxs-lookup"><span data-stu-id="96fda-128">Windows Media Player 11</span></span><br/>                                                 |
| <span data-ttu-id="96fda-129">DLL</span><span class="sxs-lookup"><span data-stu-id="96fda-129">DLL</span></span><br/>     | <dl> <span data-ttu-id="96fda-130"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="96fda-130"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96fda-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="96fda-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96fda-132">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="96fda-132">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="96fda-133">**Extern.-Anmelde Name**</span><span class="sxs-lookup"><span data-stu-id="96fda-133">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="96fda-134">**Extern. userloggedin**</span><span class="sxs-lookup"><span data-stu-id="96fda-134">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





