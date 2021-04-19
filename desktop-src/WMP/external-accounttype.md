---
title: Extern. AccountType
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt. Die AccountType-Eigenschaft ruft den Kontotyp des aktuellen Benutzers ab.
ms.assetid: 4fb6de90-a32d-4483-bbae-b23cbff93bd5
keywords:
- Externe. AccountType-Windows-Media Player
topic_type:
- apiref
api_name:
- External.accountType
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16fce659f38af19157536a4bf763362c35fc9dfa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366770"
---
# <a name="externalaccounttype"></a><span data-ttu-id="7119f-106">Extern. AccountType</span><span class="sxs-lookup"><span data-stu-id="7119f-106">External.accountType</span></span>

> [!Note]  
> <span data-ttu-id="7119f-107">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="7119f-107">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="7119f-108">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7119f-108">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="7119f-109">Die **AccountType** -Eigenschaft ruft den Kontotyp des aktuellen Benutzers ab.</span><span class="sxs-lookup"><span data-stu-id="7119f-109">The **accountType** property retrieves the account type of the current user.</span></span>

``` syntax
window.external.accountType
      
```

## <a name="possible-values"></a><span data-ttu-id="7119f-110">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="7119f-110">Possible Values</span></span>

<span data-ttu-id="7119f-111">Diese Eigenschaft ist eine schreibgeschützte **Zeichenfolge** , die den Kontotyp darstellt.</span><span class="sxs-lookup"><span data-stu-id="7119f-111">This property is a read-only **String** that represents the account type.</span></span> <span data-ttu-id="7119f-112">Zeichen folgen, die verschiedene Konto Typen darstellen, werden im Online Store definiert.</span><span class="sxs-lookup"><span data-stu-id="7119f-112">Strings that represent various account types are defined by the online store.</span></span>

## <a name="remarks"></a><span data-ttu-id="7119f-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7119f-113">Remarks</span></span>

<span data-ttu-id="7119f-114">Diese Eigenschaft ruft den Kontotyp durch Aufrufen der [iwmpcontentpartner:: getcontentpartnerinfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) -Methode ab, die vom Plug-in des Online Stores implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="7119f-114">This property retrieves the account type by calling the [IWMPContentPartner::GetContentPartnerInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcontentpartnerinfo) method, which is implemented by the online store's plug-in.</span></span> <span data-ttu-id="7119f-115">Wenn der aktuelle Benutzer beim Online Shop angemeldet ist oder das Plug-in die Anmelde Informationen des Benutzers zwischengespeichert hat, kann die **getcontentpartnerinfo** -Methode den Kontotyp des Benutzers bestimmen und ihn an den Windows-Media Player zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="7119f-115">If the current user is logged in to the online store or the plug-in has cached the user's credentials, the **getContentPartnerInfo** method can determine the user's account type and return it to Windows Media Player.</span></span> <span data-ttu-id="7119f-116">Der Kontotyp ist eine Zeichenfolge, die von Windows Media Player nicht interpretiert wird.</span><span class="sxs-lookup"><span data-stu-id="7119f-116">The account type is a string that Windows Media Player does not interpret.</span></span> <span data-ttu-id="7119f-117">Stattdessen übergibt Windows Media Player die Zeichenfolge aus dem Plug-in des Online Stores an das Skript auf der Discovery-Seite des Online Stores.</span><span class="sxs-lookup"><span data-stu-id="7119f-117">Rather, Windows Media Player passes the string from the online store's plug-in to the script on the online store's discovery page.</span></span>

<span data-ttu-id="7119f-118">Wenn der aktuelle Benutzer nicht beim Online Store angemeldet ist und das Plug-in des Online Stores keine zwischengespeicherten Anmelde Informationen für den Benutzer besitzt, ruft diese Eigenschaft die Zeichenfolge ab, die die **getcontentpartnerinfo** -Methode in dieser Situation zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="7119f-118">If the current user is not logged in to the online store and the online store's plug-in does not have cached credentials for the user, this property retrieves whatever string the **getContentPartnerInfo** method returns in that situation.</span></span>

## <a name="requirements"></a><span data-ttu-id="7119f-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7119f-119">Requirements</span></span>



| <span data-ttu-id="7119f-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7119f-120">Requirement</span></span> | <span data-ttu-id="7119f-121">Wert</span><span class="sxs-lookup"><span data-stu-id="7119f-121">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="7119f-122">Version</span><span class="sxs-lookup"><span data-stu-id="7119f-122">Version</span></span><br/> | <span data-ttu-id="7119f-123">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="7119f-123">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="7119f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7119f-124">DLL</span></span><br/>     | <dl> <span data-ttu-id="7119f-125"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7119f-125"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7119f-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7119f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7119f-127">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="7119f-127">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="7119f-128">**Extern. userloggedin**</span><span class="sxs-lookup"><span data-stu-id="7119f-128">**External.userLoggedIn**</span></span>](external-userloggedin.md)
</dt> </dl>

 

 





