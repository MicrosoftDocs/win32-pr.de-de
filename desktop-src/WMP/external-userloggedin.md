---
title: Extern. userloggedin
description: In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online Stores entwickelt wurden. | Extern. userloggedin
ms.assetid: d02d9486-c692-4f46-bc29-f0aaa45cad0f
keywords:
- Extern. userloggedin-Windows-Media Player
topic_type:
- apiref
api_name:
- External.userLoggedIn
api_location:
- wmp.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a5454dd9d2fa2d771005448a4157c33b5634a30
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369721"
---
# <a name="externaluserloggedin"></a><span data-ttu-id="74af1-105">Extern. userloggedin</span><span class="sxs-lookup"><span data-stu-id="74af1-105">External.userLoggedIn</span></span>

> [!Note]  
> <span data-ttu-id="74af1-106">In diesem Thema werden die Funktionen beschrieben, die für die Verwendung durch Online-Speicher</span><span class="sxs-lookup"><span data-stu-id="74af1-106">This topic describes functionality designed for use by online stores.</span></span> <span data-ttu-id="74af1-107">Die Verwendung dieser Funktion außerhalb des Kontexts eines Online Stores wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="74af1-107">Use of this functionality outside the context of an online store is not supported.</span></span>

 

<span data-ttu-id="74af1-108">Die **userloggedin** -Eigenschaft ruft einen Wert ab, der angibt, ob der Benutzer am Online Store angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="74af1-108">The **userLoggedIn** property retrieves a value indicating whether the user is logged in to the online store.</span></span>

## <a name="syntax"></a><span data-ttu-id="74af1-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="74af1-109">Syntax</span></span>

``` syntax
window.external.userLoggedIn
```

## <a name="possible-values"></a><span data-ttu-id="74af1-110">Mögliche Werte</span><span class="sxs-lookup"><span data-stu-id="74af1-110">Possible Values</span></span>

<span data-ttu-id="74af1-111">Diese Eigenschaft ist ein Schreib geschützter **boolescher** Wert.</span><span class="sxs-lookup"><span data-stu-id="74af1-111">This property is a read-only **Boolean**.</span></span> <span data-ttu-id="74af1-112">**True** gibt an, dass der Benutzer angemeldet ist, und **false** gibt an, dass der Benutzer abgemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="74af1-112">**TRUE** indicates that the user is logged in, and **FALSE** indicates that the user is logged out.</span></span>

## <a name="requirements"></a><span data-ttu-id="74af1-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="74af1-113">Requirements</span></span>



| <span data-ttu-id="74af1-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="74af1-114">Requirement</span></span> | <span data-ttu-id="74af1-115">Wert</span><span class="sxs-lookup"><span data-stu-id="74af1-115">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="74af1-116">Version</span><span class="sxs-lookup"><span data-stu-id="74af1-116">Version</span></span><br/> | <span data-ttu-id="74af1-117">Windows Media Player 11.</span><span class="sxs-lookup"><span data-stu-id="74af1-117">Windows Media Player 11.</span></span><br/>                                                |
| <span data-ttu-id="74af1-118">DLL</span><span class="sxs-lookup"><span data-stu-id="74af1-118">DLL</span></span><br/>     | <dl> <span data-ttu-id="74af1-119"><dt>Wmp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="74af1-119"><dt>Wmp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="74af1-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74af1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="74af1-121">**Externes Objekt für den Typ 1-Online Speicher**</span><span class="sxs-lookup"><span data-stu-id="74af1-121">**External Object for Type 1 Online Stores**</span></span>](external-object-for-type-1-online-stores.md)
</dt> <dt>

[<span data-ttu-id="74af1-122">**Extern.-Anmelde Name**</span><span class="sxs-lookup"><span data-stu-id="74af1-122">**External.attemptLogin**</span></span>](external-attemptlogin.md)
</dt> <dt>

[<span data-ttu-id="74af1-123">**Externes. onloginchange-Ereignis**</span><span class="sxs-lookup"><span data-stu-id="74af1-123">**External.OnLoginChange Event**</span></span>](external-onloginchange-event.md)
</dt> </dl>

 

 





