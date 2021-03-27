---
description: Löscht einen Benutzer aus dem Volume.
ms.assetid: 56a07388-b7d8-41a4-b29a-8a57fe0b9d19
title: Diskquotacontrol. DeleteUser-Methode (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DeleteUser
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: c159375727ef115631a8a047d69ce235a5b8f2a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104214426"
---
# <a name="diskquotacontroldeleteuser-method"></a><span data-ttu-id="7924f-103">Diskquotacontrol. DeleteUser-Methode</span><span class="sxs-lookup"><span data-stu-id="7924f-103">DiskQuotaControl.DeleteUser method</span></span>

<span data-ttu-id="7924f-104">Löscht einen Benutzer aus dem Volume.</span><span class="sxs-lookup"><span data-stu-id="7924f-104">Deletes a user from the volume.</span></span>

## <a name="syntax"></a><span data-ttu-id="7924f-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="7924f-105">Syntax</span></span>


```JScript
DiskQuotaControl.DeleteUser(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="7924f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="7924f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7924f-107">*oUser*</span><span class="sxs-lookup"><span data-stu-id="7924f-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="7924f-108">Type: **Object**</span><span class="sxs-lookup"><span data-stu-id="7924f-108">Type: **Object**</span></span>

<span data-ttu-id="7924f-109">Ein Objekt Ausdruck, der das [**didiskquotauser**](didiskquotauser-object.md) -Objekt des Benutzers ergibt.</span><span class="sxs-lookup"><span data-stu-id="7924f-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7924f-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="7924f-110">Return value</span></span>

<span data-ttu-id="7924f-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="7924f-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="7924f-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7924f-112">Remarks</span></span>

<span data-ttu-id="7924f-113">Diese Methode schlägt fehl, wenn der Benutzer über Speicherplatz auf dem Volume verfügt.</span><span class="sxs-lookup"><span data-stu-id="7924f-113">This method fails if the user owns any storage on the volume.</span></span> <span data-ttu-id="7924f-114">Bevor Sie einen Benutzer aus einem Volume löschen, muss der gesamte Speicher für diesen Benutzer gelöscht, auf ein anderes Volume verschoben werden, oder der Besitz muss an einen anderen Benutzer übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="7924f-114">Before you delete a user from a volume, all storage for that user must be deleted, be moved to another volume, or have its ownership transferred to another user.</span></span>

## <a name="requirements"></a><span data-ttu-id="7924f-115">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="7924f-115">Requirements</span></span>



| <span data-ttu-id="7924f-116">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7924f-116">Requirement</span></span> | <span data-ttu-id="7924f-117">Wert</span><span class="sxs-lookup"><span data-stu-id="7924f-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7924f-118">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="7924f-118">Minimum supported client</span></span><br/> | <span data-ttu-id="7924f-119">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7924f-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7924f-120">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="7924f-120">Minimum supported server</span></span><br/> | <span data-ttu-id="7924f-121">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="7924f-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="7924f-122">Header</span><span class="sxs-lookup"><span data-stu-id="7924f-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="7924f-123"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="7924f-123"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="7924f-124">DLL</span><span class="sxs-lookup"><span data-stu-id="7924f-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7924f-125"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="7924f-125"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7924f-126">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="7924f-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7924f-127">**AddUser**</span><span class="sxs-lookup"><span data-stu-id="7924f-127">**AddUser**</span></span>](diskquotacontrol-adduser.md)
</dt> <dt>

[<span data-ttu-id="7924f-128">**Diskquotacontrol**</span><span class="sxs-lookup"><span data-stu-id="7924f-128">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




