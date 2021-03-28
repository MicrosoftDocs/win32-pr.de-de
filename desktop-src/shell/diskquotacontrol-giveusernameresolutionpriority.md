---
description: Platziert das angegebene Benutzerobjekt für die Namensauflösung in der nächsten Zeile.
ms.assetid: 4c75f966-2e7d-4415-b1db-c98f8bdd4ce3
title: Diskquotacontrol. giveusernameresolutionpriority-Methode (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.GiveUserNameResolutionPriority
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 1acf50e0cec59a7ee14fbd9d7760fb68b27c4de5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104525331"
---
# <a name="diskquotacontrolgiveusernameresolutionpriority-method"></a><span data-ttu-id="07777-103">Diskquotacontrol. giveusernameresolutionpriority-Methode</span><span class="sxs-lookup"><span data-stu-id="07777-103">DiskQuotaControl.GiveUserNameResolutionPriority method</span></span>

<span data-ttu-id="07777-104">Platziert das angegebene Benutzerobjekt für die Namensauflösung in der nächsten Zeile.</span><span class="sxs-lookup"><span data-stu-id="07777-104">Places the specified user object next in line for name resolution.</span></span>

## <a name="syntax"></a><span data-ttu-id="07777-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="07777-105">Syntax</span></span>


```JScript
DiskQuotaControl.GiveUserNameResolutionPriority(
  oUser
)
```



## <a name="parameters"></a><span data-ttu-id="07777-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="07777-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="07777-107">*oUser*</span><span class="sxs-lookup"><span data-stu-id="07777-107">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="07777-108">Type: **Object**</span><span class="sxs-lookup"><span data-stu-id="07777-108">Type: **Object**</span></span>

<span data-ttu-id="07777-109">Ein Objekt Ausdruck, der das [**didiskquotauser**](didiskquotauser-object.md) -Objekt des Benutzers ergibt.</span><span class="sxs-lookup"><span data-stu-id="07777-109">An object expression that evaluates to the user's [**DIDiskQuotaUser**](didiskquotauser-object.md) object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="07777-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="07777-110">Return value</span></span>

<span data-ttu-id="07777-111">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="07777-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="07777-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="07777-112">Remarks</span></span>

<span data-ttu-id="07777-113">Wenn die asynchrone Namensauflösung aktiviert ist, werden Benutzer Objekte in eine Warteschlange eingefügt.</span><span class="sxs-lookup"><span data-stu-id="07777-113">If asynchronous name resolution is enabled, user objects are placed in a queue.</span></span> <span data-ttu-id="07777-114">Standardmäßig werden Sie in der Reihenfolge gewartet, in der Sie in die Warteschlange gestellt werden.</span><span class="sxs-lookup"><span data-stu-id="07777-114">By default, they are serviced in the order they are placed in the queue.</span></span> <span data-ttu-id="07777-115">Mit der **giveusernameresolutionpriority** -Methode wird ein Objekt an den Anfang der Warteschlange verschoben, sodass es in der Reihe ist, gewartet zu werden.</span><span class="sxs-lookup"><span data-stu-id="07777-115">The **GiveUserNameResolutionPriority** method moves an object to the front of the queue so that it is next in line to be serviced.</span></span>

<span data-ttu-id="07777-116">Verwenden Sie die [**usernameresolution**](diskquotacontrol-usernameresolution.md) -Eigenschaft, um die asynchrone Namensauflösung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="07777-116">Use the [**UserNameResolution**](diskquotacontrol-usernameresolution.md) property to enable asynchronous name resolution.</span></span>

## <a name="requirements"></a><span data-ttu-id="07777-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="07777-117">Requirements</span></span>



| <span data-ttu-id="07777-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="07777-118">Requirement</span></span> | <span data-ttu-id="07777-119">Wert</span><span class="sxs-lookup"><span data-stu-id="07777-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="07777-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="07777-120">Minimum supported client</span></span><br/> | <span data-ttu-id="07777-121">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07777-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="07777-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="07777-122">Minimum supported server</span></span><br/> | <span data-ttu-id="07777-123">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="07777-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="07777-124">Header</span><span class="sxs-lookup"><span data-stu-id="07777-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="07777-125"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="07777-125"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="07777-126">DLL</span><span class="sxs-lookup"><span data-stu-id="07777-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="07777-127"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="07777-127"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="07777-128">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="07777-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="07777-129">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="07777-129">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




