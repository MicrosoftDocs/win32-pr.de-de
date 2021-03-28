---
description: Macht den Benutzernamen Cache für die Sicherheits-ID ungültig.
ms.assetid: 52f4a051-0caf-43c1-b190-c83c20e9fcf8
title: Diskquotacontrol. invalidatesidnamecache-Methode (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.InvalidateSidNameCache
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 4e7202c1293d32d55e12e88671ed9960d376f63e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103958769"
---
# <a name="diskquotacontrolinvalidatesidnamecache-method"></a><span data-ttu-id="3a235-103">Diskquotacontrol. invalidatesidnamecache-Methode</span><span class="sxs-lookup"><span data-stu-id="3a235-103">DiskQuotaControl.InvalidateSidNameCache method</span></span>

<span data-ttu-id="3a235-104">Macht den Benutzernamen Cache für die Sicherheits-ID ungültig.</span><span class="sxs-lookup"><span data-stu-id="3a235-104">Invalidates the security ID user name cache.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a235-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a235-105">Syntax</span></span>


```JScript
DiskQuotaControl.InvalidateSidNameCache()
```



## <a name="parameters"></a><span data-ttu-id="3a235-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3a235-106">Parameters</span></span>

<span data-ttu-id="3a235-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="3a235-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3a235-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3a235-108">Return value</span></span>

<span data-ttu-id="3a235-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="3a235-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3a235-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3a235-110">Remarks</span></span>

<span data-ttu-id="3a235-111">Benutzernamen und zugehörige Sicherheits-IDs werden in einem Cache gespeichert.</span><span class="sxs-lookup"><span data-stu-id="3a235-111">User names and associated security IDs are stored in a cache.</span></span> <span data-ttu-id="3a235-112">Sie können diesen Cache durch Aufrufen von **invalidatesidnamecache** löschen.</span><span class="sxs-lookup"><span data-stu-id="3a235-112">You can clear this cache by calling **InvalidateSidNameCache**.</span></span> <span data-ttu-id="3a235-113">Wenn Sie anschließend ein neues Benutzerobjekt erstellen, müssen die Informationen vom Domänen Controller abgerufen werden, und der Cache muss wieder hergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3a235-113">If you subsequently create a new user object, the information will have to be obtained from the domain controller, and the cache will have to be reestablished.</span></span>

## <a name="requirements"></a><span data-ttu-id="3a235-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="3a235-114">Requirements</span></span>



| <span data-ttu-id="3a235-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="3a235-115">Requirement</span></span> | <span data-ttu-id="3a235-116">Wert</span><span class="sxs-lookup"><span data-stu-id="3a235-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a235-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="3a235-117">Minimum supported client</span></span><br/> | <span data-ttu-id="3a235-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a235-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="3a235-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="3a235-119">Minimum supported server</span></span><br/> | <span data-ttu-id="3a235-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="3a235-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="3a235-121">Header</span><span class="sxs-lookup"><span data-stu-id="3a235-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a235-122"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="3a235-122"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="3a235-123">DLL</span><span class="sxs-lookup"><span data-stu-id="3a235-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3a235-124"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="3a235-124"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a235-125">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="3a235-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a235-126">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="3a235-126">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




