---
description: Löscht die zwischengespeicherten Benutzerinformationen des-Objekts.
title: Didiskquotauser. Invalidate-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.Invalidate
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: e0ffd5b7-db1d-40a4-810a-ff43549b0c9b
ms.openlocfilehash: 2b07ae6fd210b8722378a771cda97c2c04572c66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525343"
---
# <a name="didiskquotauserinvalidate-method"></a><span data-ttu-id="c68c9-103">Didiskquotauser. Invalidate-Methode</span><span class="sxs-lookup"><span data-stu-id="c68c9-103">DIDiskQuotaUser.Invalidate method</span></span>

<span data-ttu-id="c68c9-104">Löscht die zwischengespeicherten Benutzerinformationen des-Objekts.</span><span class="sxs-lookup"><span data-stu-id="c68c9-104">Clears the object's cached user information.</span></span>

## <a name="syntax"></a><span data-ttu-id="c68c9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="c68c9-105">Syntax</span></span>


```JScript
DIDiskQuotaUser.Invalidate()
```



## <a name="parameters"></a><span data-ttu-id="c68c9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="c68c9-106">Parameters</span></span>

<span data-ttu-id="c68c9-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="c68c9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c68c9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="c68c9-108">Return value</span></span>

<span data-ttu-id="c68c9-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="c68c9-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c68c9-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c68c9-110">Remarks</span></span>

<span data-ttu-id="c68c9-111">Diese Methode löscht die im Cache des Objekts gespeicherten Benutzerinformationen.</span><span class="sxs-lookup"><span data-stu-id="c68c9-111">This method clears the user information stored in the object's cache.</span></span> <span data-ttu-id="c68c9-112">Wenn Sie das nächste Mal eine Anforderung für Kontingent bezogene Informationen erhalten, ruft das-Objekt die Informationen vom NTFS-Volume ab und aktualisiert den Cache.</span><span class="sxs-lookup"><span data-stu-id="c68c9-112">The next time a request is made for quota-related information, the object retrieves the information from the NTFS volume and refreshes the cache.</span></span>

## <a name="requirements"></a><span data-ttu-id="c68c9-113">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="c68c9-113">Requirements</span></span>



| <span data-ttu-id="c68c9-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="c68c9-114">Requirement</span></span> | <span data-ttu-id="c68c9-115">Wert</span><span class="sxs-lookup"><span data-stu-id="c68c9-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c68c9-116">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="c68c9-116">Minimum supported client</span></span><br/> | <span data-ttu-id="c68c9-117">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c68c9-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="c68c9-118">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="c68c9-118">Minimum supported server</span></span><br/> | <span data-ttu-id="c68c9-119">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="c68c9-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="c68c9-120">DLL</span><span class="sxs-lookup"><span data-stu-id="c68c9-120">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c68c9-121"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="c68c9-121"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c68c9-122">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="c68c9-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c68c9-123">**Didiskquotauser-Objekt**</span><span class="sxs-lookup"><span data-stu-id="c68c9-123">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> </dl>

 

 




