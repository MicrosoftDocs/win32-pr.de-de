---
description: Gibt Zugriffs Steuerungs Berechtigungen für eine Datei auf einer Smartcard an.
ms.assetid: 995d959f-30dc-4e5c-be2d-6b447499415a
title: CARD_FILE_ACCESS_CONDITION-Enumeration (cardmod. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CARD_FILE_ACCESS_CONDITION
api_type:
- HeaderDef
api_location:
- Cardmod.h
ms.openlocfilehash: d3ef9fc81c9ab3bff5f3992c3aedeb3f923648ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106356733"
---
# <a name="card_file_access_condition-enumeration"></a><span data-ttu-id="e8e55-103">\_ \_ Zugriffsbedingungs-Enumeration für Kartendatei \_</span><span class="sxs-lookup"><span data-stu-id="e8e55-103">CARD\_FILE\_ACCESS\_CONDITION enumeration</span></span>

<span data-ttu-id="e8e55-104">Die Enumeration der **\_ kartendateizugriffsbedingung \_ \_** gibt Zugriffs Steuerungs Berechtigungen für eine Datei auf einer [*Smartcard*](../secgloss/s-gly.md)an.</span><span class="sxs-lookup"><span data-stu-id="e8e55-104">The **CARD\_FILE\_ACCESS\_CONDITION** enumeration specifies access control permissions for a file on a [*smart card*](../secgloss/s-gly.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="e8e55-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e8e55-105">Syntax</span></span>


```C++
typedef enum  { 
  InvalidAc                 = 0,
  EveryoneReadUserWriteAc   = 1,
  UserWriteExecuteAc        = 2,
  EveryoneReadAdminWriteAc  = 3,
  UnknownAc                 = 4
} CARD_FILE_ACCESS_CONDITION;
```



## <a name="constants"></a><span data-ttu-id="e8e55-106">Konstanten</span><span class="sxs-lookup"><span data-stu-id="e8e55-106">Constants</span></span>

<dl> <dt>

<span data-ttu-id="e8e55-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**Invalidac**</span><span class="sxs-lookup"><span data-stu-id="e8e55-107"><span id="InvalidAc"></span><span id="invalidac"></span><span id="INVALIDAC"></span>**InvalidAc**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-108">Dieser Wert ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="e8e55-108">This value is not valid.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**Everyonereaduserschreiteac**</span><span class="sxs-lookup"><span data-stu-id="e8e55-109"><span id="EveryoneReadUserWriteAc"></span><span id="everyonereaduserwriteac"></span><span id="EVERYONEREADUSERWRITEAC"></span>**EveryoneReadUserWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-110">Alle Benutzer können die Datei lesen.</span><span class="sxs-lookup"><span data-stu-id="e8e55-110">Everyone can read the file.</span></span> <span data-ttu-id="e8e55-111">Bestimmte Benutzer können in die Datei schreiben.</span><span class="sxs-lookup"><span data-stu-id="e8e55-111">Specific users can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**Userschreiteexecuteac**</span><span class="sxs-lookup"><span data-stu-id="e8e55-112"><span id="UserWriteExecuteAc"></span><span id="userwriteexecuteac"></span><span id="USERWRITEEXECUTEAC"></span>**UserWriteExecuteAc**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-113">Nur bestimmte Benutzer können die Datei lesen oder in diese schreiben.</span><span class="sxs-lookup"><span data-stu-id="e8e55-113">Only specific users can read or write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**Everyonereadadminschreiteac**</span><span class="sxs-lookup"><span data-stu-id="e8e55-114"><span id="EveryoneReadAdminWriteAc"></span><span id="everyonereadadminwriteac"></span><span id="EVERYONEREADADMINWRITEAC"></span>**EveryoneReadAdminWriteAc**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-115">Alle Benutzer können die Datei lesen.</span><span class="sxs-lookup"><span data-stu-id="e8e55-115">Everyone can read the file.</span></span> <span data-ttu-id="e8e55-116">Administratoren können in die Datei schreiben.</span><span class="sxs-lookup"><span data-stu-id="e8e55-116">Administrators can write to the file.</span></span>

</dd> <dt>

<span data-ttu-id="e8e55-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**Unknownac**</span><span class="sxs-lookup"><span data-stu-id="e8e55-117"><span id="UnknownAc"></span><span id="unknownac"></span><span id="UNKNOWNAC"></span>**UnknownAc**</span></span>
</dt> <dd>

<span data-ttu-id="e8e55-118">Die Zugriffsberechtigungen für die Datei sind unbekannt.</span><span class="sxs-lookup"><span data-stu-id="e8e55-118">Access permissions for the file are unknown.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e8e55-119">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="e8e55-119">Requirements</span></span>



| <span data-ttu-id="e8e55-120">Anforderung</span><span class="sxs-lookup"><span data-stu-id="e8e55-120">Requirement</span></span> | <span data-ttu-id="e8e55-121">Wert</span><span class="sxs-lookup"><span data-stu-id="e8e55-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e8e55-122">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="e8e55-122">Minimum supported client</span></span><br/> | <span data-ttu-id="e8e55-123">Nur Windows XP, Windows XP \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8e55-123">Windows XP, Windows XP \[desktop apps only\]</span></span><br/>                              |
| <span data-ttu-id="e8e55-124">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="e8e55-124">Minimum supported server</span></span><br/> | <span data-ttu-id="e8e55-125">Windows Server 2003, Windows Server 2003 \[ Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="e8e55-125">Windows Server 2003, Windows Server 2003 \[desktop apps only\]</span></span><br/>            |
| <span data-ttu-id="e8e55-126">Header</span><span class="sxs-lookup"><span data-stu-id="e8e55-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e8e55-127"><dt>Cardmod. h</dt></span><span class="sxs-lookup"><span data-stu-id="e8e55-127"><dt>Cardmod.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e8e55-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e8e55-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e8e55-129">Kryptografiedienstanbieter für Microsoft Base Smartcard</span><span class="sxs-lookup"><span data-stu-id="e8e55-129">Microsoft Base Smart Card Cryptographic Service Provider</span></span>](/previous-versions/windows/desktop/secsmart/microsoft-base-smart-card-cryptographic-service-provider)
</dt> <dt>

[<span data-ttu-id="e8e55-130">**Informationen zur Karten \_ Datei \_**</span><span class="sxs-lookup"><span data-stu-id="e8e55-130">**CARD\_FILE\_INFO**</span></span>](/previous-versions/windows/desktop/secsmart/card-file-info)
</dt> <dt>

[<span data-ttu-id="e8e55-131">**Cardkreatefile**</span><span class="sxs-lookup"><span data-stu-id="e8e55-131">**CardCreateFile**</span></span>](/previous-versions/windows/desktop/secsmart/cardcreatefile)
</dt> </dl>

 

 
