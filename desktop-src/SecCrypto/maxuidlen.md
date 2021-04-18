---
description: Eine numerische Konstante, die die maximale Anzahl von Zeichen angibt, die von einigen Kryptografieanbietern von Microsoft beim Abrufen der Benutzer-ID verwendet werden.
ms.assetid: cc15a166-9a0c-41ce-9cb1-ecdc922565c0
title: Maxuidlen (Wincrypt. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 199d8e697deba86ffe48d4f76501f2d9d3a6d4e3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106347796"
---
# <a name="maxuidlen"></a><span data-ttu-id="4b3f1-103">Maxuidlen</span><span class="sxs-lookup"><span data-stu-id="4b3f1-103">MAXUIDLEN</span></span>

<span data-ttu-id="4b3f1-104">Maxuidlen ist eine numerische Konstante, die die maximale Anzahl von Zeichen angibt, die von einigen Kryptografieanbietern von Microsoft beim Abrufen der Benutzer-ID verwendet werden. maxuidlen ist in Wincrypt. h definiert.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-104">MAXUIDLEN is a numeric constant that specifies the maximum number of characters that some of the Microsoft cryptographic providers will use when obtaining the user ID.MAXUIDLEN is defined in Wincrypt.h.</span></span>



| <span data-ttu-id="4b3f1-105">Konstante/Wert</span><span class="sxs-lookup"><span data-stu-id="4b3f1-105">Constant/value</span></span>                                                                                                                                                                                                  | <span data-ttu-id="4b3f1-106">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="4b3f1-106">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                   |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MAXUIDLEN"></span><span id="maxuidlen"></span><dl> <span data-ttu-id="4b3f1-107"><dt>**Maxuidlen**</dt> <dt>64 (0x40)</dt></span><span class="sxs-lookup"><span data-stu-id="4b3f1-107"><dt>**MAXUIDLEN**</dt> <dt>64 (0x40)</dt></span></span> </dl> | <span data-ttu-id="4b3f1-108">Wenn der *pszcontainer* -Parameter der [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) -Funktion **null** ist, verwenden einige der Kryptografieanbieter von Microsoft den Anmelde Namen des aktuell angemeldeten Benutzers als Schlüssel Container Namen.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-108">When the *pszContainer* parameter of the [**CryptAcquireContext**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta) function is **NULL**, some of the Microsoft cryptographic providers use the logon name of the currently logged on user as the key container name.</span></span> <span data-ttu-id="4b3f1-109">Maxuidlen gibt die maximale Anzahl von Zeichen an, einschließlich des abschließenden **null** -Zeichens, das diese Anbieter für den Benutzernamen verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b3f1-109">MAXUIDLEN specifies the maximum number of characters, including the terminating **NULL** character, that these providers will use for the user name.</span></span><br/> |



## <a name="requirements"></a><span data-ttu-id="4b3f1-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="4b3f1-110">Requirements</span></span>



| <span data-ttu-id="4b3f1-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="4b3f1-111">Requirement</span></span> | <span data-ttu-id="4b3f1-112">Wert</span><span class="sxs-lookup"><span data-stu-id="4b3f1-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="4b3f1-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="4b3f1-113">Minimum supported client</span></span><br/> | <span data-ttu-id="4b3f1-114">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b3f1-114">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="4b3f1-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="4b3f1-115">Minimum supported server</span></span><br/> | <span data-ttu-id="4b3f1-116">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="4b3f1-116">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="4b3f1-117">Header</span><span class="sxs-lookup"><span data-stu-id="4b3f1-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="4b3f1-118"><dt>WinCrypt. h</dt></span><span class="sxs-lookup"><span data-stu-id="4b3f1-118"><dt>Wincrypt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4b3f1-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b3f1-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4b3f1-120">**CryptAcquireContext**</span><span class="sxs-lookup"><span data-stu-id="4b3f1-120">**CryptAcquireContext**</span></span>](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptacquirecontexta)
</dt> <dt>

[<span data-ttu-id="4b3f1-121">**Cpacquirecontext**</span><span class="sxs-lookup"><span data-stu-id="4b3f1-121">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> </dl>

 

 




