---
description: Die dvdadm. ConfirmPassword-Methode testet, ob das angegebene Kennwort mit dem zuvor gespeicherten Kennwort übereinstimmt.
ms.assetid: 4dddc28d-edf7-45a2-ae1f-1c37b5df2eea
title: ConfirmPassword-Methode (Segment. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62817247ca661f92ceb5ba0e2bc9bb11381d73ff
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357705"
---
# <a name="confirmpassword-method"></a><span data-ttu-id="9e1b1-103">ConfirmPassword-Methode</span><span class="sxs-lookup"><span data-stu-id="9e1b1-103">ConfirmPassword Method</span></span>

> [!Note]  
> <span data-ttu-id="9e1b1-104">Diese Komponente ist für die Verwendung in den Betriebssystemen Microsoft Windows 2000, Windows XP und Windows Server 2003 verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="9e1b1-105">Es kann in nachfolgenden Versionen geändert oder entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="9e1b1-106">Die- `DVDAdm.ConfirmPassword` Methode testet, ob das angegebene Kennwort mit dem zuvor gespeicherten Kennwort übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-106">The `DVDAdm.ConfirmPassword` method tests whether the specified password matches the previously saved password.</span></span>

``` syntax
[ bIsConfirmed = ] DVD.DVDAdm.ConfirmPassword(sUserName, sPassword)
```

## <a name="parameters"></a><span data-ttu-id="9e1b1-107">Parameter</span><span class="sxs-lookup"><span data-stu-id="9e1b1-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9e1b1-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span><span class="sxs-lookup"><span data-stu-id="9e1b1-108"><span id="sUserName"></span><span id="susername"></span><span id="SUSERNAME"></span>*sUserName*</span></span>
</dt> <dd>

<span data-ttu-id="9e1b1-109">Gibt den Namen des Benutzers als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-109">Specifies the user's name as a String.</span></span>

</dd> <dt>

<span data-ttu-id="9e1b1-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span><span class="sxs-lookup"><span data-stu-id="9e1b1-110"><span id="sPassword"></span><span id="spassword"></span><span id="SPASSWORD"></span>*sPassword*</span></span>
</dt> <dd>

<span data-ttu-id="9e1b1-111">Gibt das neue Kennwort als Zeichenfolge an.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-111">Specifies the new password as a String.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9e1b1-112">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9e1b1-112">Return Value</span></span>

<span data-ttu-id="9e1b1-113">Gibt true zurück, wenn das angegebene Kennwort mit dem vorhandenen Kennwort übereinstimmt, andernfalls false.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-113">Returns true if the specified password matches the existing password, false otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="9e1b1-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9e1b1-114">Remarks</span></span>

<span data-ttu-id="9e1b1-115">Derzeit wird der *sUserName* -Parameter für dieses und alle zugehörigen Methoden ignoriert.</span><span class="sxs-lookup"><span data-stu-id="9e1b1-115">Currently, the *sUserName* parameter is ignored on this and all related methods.</span></span>

## <a name="requirements"></a><span data-ttu-id="9e1b1-116">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="9e1b1-116">Requirements</span></span>



| <span data-ttu-id="9e1b1-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="9e1b1-117">Requirement</span></span> | <span data-ttu-id="9e1b1-118">Wert</span><span class="sxs-lookup"><span data-stu-id="9e1b1-118">Value</span></span> |
|-------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9e1b1-119">Header</span><span class="sxs-lookup"><span data-stu-id="9e1b1-119">Header</span></span><br/> | <dl> <span data-ttu-id="9e1b1-120"><dt>Segment. h</dt></span><span class="sxs-lookup"><span data-stu-id="9e1b1-120"><dt>Segment.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9e1b1-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e1b1-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9e1b1-122">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="9e1b1-122">**ChangePassword**</span></span>](changepassword-method.md)
</dt> <dt>

[<span data-ttu-id="9e1b1-123">Msdvdadm-Objekt</span><span class="sxs-lookup"><span data-stu-id="9e1b1-123">MSDVDAdm Object</span></span>](msdvdadm-object.md)
</dt> </dl>

 

 




