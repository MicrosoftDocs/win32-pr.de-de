---
description: Gibt Zugriffs Steuerungs Berechtigungen für ein Verzeichnis auf einer Smartcard an.
ms.assetid: 361d9fa0-286e-4d2c-8452-3b5f48e77779
title: CARD_DIRECTORY_ACCESS_CONDITION-Enumeration (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_DIRECTORY_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: 9879fa73f6bb45b56f433d7bca7765ab5fc0daef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214528"
---
# <a name="card_directory_access_condition-enumeration"></a><span data-ttu-id="b9eba-103">\_ \_ Enumeration der Zugriffsbedingung für Karten Verzeichnisse \_</span><span class="sxs-lookup"><span data-stu-id="b9eba-103">CARD\_DIRECTORY\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="b9eba-104">Die Enumeration der **\_ \_ Zugriffsbedingung \_ für Karten Verzeichnisse** gibt Zugriffs Steuerungs Berechtigungen für ein Verzeichnis auf einer [*Smartcard*](../secgloss/s-gly.md)an.</span><span class="sxs-lookup"><span data-stu-id="b9eba-104">The **CARD\_DIRECTORY\_ACCESS\_CONDITION** enumeration specifies access control permissions for a directory on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="b9eba-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="b9eba-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc               = 0,
  UserCreateDeleteDirAc   = 1,
  AdminCreateDeleteDirAc  = 2
} CARD_DIRECTORY_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="b9eba-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="b9eba-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="b9eba-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**Invalidac**</span><span class="sxs-lookup"><span data-stu-id="b9eba-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="b9eba-108">Dieser Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="b9eba-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="b9eba-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**Userkreatedeletedirac**</span><span class="sxs-lookup"><span data-stu-id="b9eba-109"><span id="UserCreateDeleteDirAc"></span><span id="usercreatedeletedirac"></span><span id="USERCREATEDELETEDIRAC"></span>**UserCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="b9eba-110">Bestimmte Benutzer können das Verzeichnis lesen, schreiben und löschen.</span><span class="sxs-lookup"><span data-stu-id="b9eba-110">Specific users can read, write, and delete the directory.</span></span>

</dd> <dt>

<span data-ttu-id="b9eba-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**Adminkreatedeletedirac**</span><span class="sxs-lookup"><span data-stu-id="b9eba-111"><span id="AdminCreateDeleteDirAc"></span><span id="admincreatedeletedirac"></span><span id="ADMINCREATEDELETEDIRAC"></span>**AdminCreateDeleteDirAc**</span></span>
</dt> <dd>

<span data-ttu-id="b9eba-112">Administratoren können das Verzeichnis lesen, schreiben und löschen.</span><span class="sxs-lookup"><span data-stu-id="b9eba-112">Administrators can read, write, and delete the directory.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="b9eba-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="b9eba-113">Requirements</span></span>



| <span data-ttu-id="b9eba-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="b9eba-114">Requirement</span></span> | <span data-ttu-id="b9eba-115">Wert</span><span class="sxs-lookup"><span data-stu-id="b9eba-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="b9eba-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="b9eba-116">Minimum supported client</span></span><br/> | <span data-ttu-id="b9eba-117">Nur Windows XP, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9eba-117">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="b9eba-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="b9eba-118">Minimum supported server</span></span><br/> | <span data-ttu-id="b9eba-119">Windows Server 2003, Windows Server 2003 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="b9eba-119">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="b9eba-120">Header</span><span class="sxs-lookup"><span data-stu-id="b9eba-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="b9eba-121"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="b9eba-121"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9eba-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9eba-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9eba-123">Kryptografiedienstanbieter für Microsoft Base Smartcard</span><span class="sxs-lookup"><span data-stu-id="b9eba-123">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="b9eba-124">**Cardkreatedirectory**</span><span class="sxs-lookup"><span data-stu-id="b9eba-124">**CardCreateDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatedirectory)
</dt> <dt>

[<span data-ttu-id="b9eba-125">**Carddeletedirectory**</span><span class="sxs-lookup"><span data-stu-id="b9eba-125">**CardDeleteDirectory**</span></span>](/previous-versions/windows/desktop/secsmart/carddeletedirectory)
</dt> </dl>

 

 
