---
description: Tritt auf, wenn die Namensinformationen für ein didiskquotauser-Objekt aufgelöst wurden.
ms.assetid: df32cb17-ad90-4535-a36b-60c5b4e9999f
title: Onusernamechanged-Funktion (dskquota. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OnUserNameChanged
api_type:
- DllExport
api_location:
- Shell32.dll
ms.openlocfilehash: 98906f281c6c93a64754c1aa5cecfc6624599c40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/08/2021
ms.locfileid: "104346438"
---
# <a name="onusernamechanged-function"></a><span data-ttu-id="166c5-103">Onusernamechanged-Funktion</span><span class="sxs-lookup"><span data-stu-id="166c5-103">OnUserNameChanged function</span></span>

<span data-ttu-id="166c5-104">Tritt auf, wenn die Namensinformationen für ein [**didiskquotauser**](didiskquotauser-object.md) -Objekt aufgelöst wurden.</span><span class="sxs-lookup"><span data-stu-id="166c5-104">Occurs when the name information for a [**DIDiskQuotaUser**](didiskquotauser-object.md) object has been resolved.</span></span>

## <a name="parameters"></a><span data-ttu-id="166c5-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="166c5-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="166c5-106">*oUser*</span><span class="sxs-lookup"><span data-stu-id="166c5-106">*oUser*</span></span> 
</dt> <dd>

<span data-ttu-id="166c5-107">Das **Objekt** , das das [**didiskquotauser**](didiskquotauser-object.md) -Objekt ergibt, das dem Benutzer zugeordnet ist, dessen Name aufgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="166c5-107">The **Object** that evaluates to the [**DIDiskQuotaUser**](didiskquotauser-object.md) object associated with the user whose name has been resolved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="166c5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="166c5-108">Return value</span></span>

<span data-ttu-id="166c5-109">Diese Funktion gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="166c5-109">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="166c5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="166c5-110">Remarks</span></span>

<span data-ttu-id="166c5-111">Wenn ein Client [**Benutzer aufzählt**](didiskquotauser-object.md)oder die Methode [**adduser**](diskquotacontrol-adduser.md) oder [**FINDUSER**](diskquotacontrol-finduser.md) aufruft, muss der Benutzername in die zugehörige Sicherheits-ID (SID) aufgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="166c5-111">When a client [**enumerates users**](didiskquotauser-object.md), or calls the [**AddUser**](diskquotacontrol-adduser.md) or [**FindUser**](diskquotacontrol-finduser.md) method, the user name must be resolved to the associated security ID (SID).</span></span> <span data-ttu-id="166c5-112">Da dieses Verfahren zeitaufwändig sein kann, kann ein Client eine Namensauflösung in einem Hintergrund Thread asynchron durchgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="166c5-112">Because this procedure can be time-consuming, a client can have name resolution done asynchronously on a background thread.</span></span> <span data-ttu-id="166c5-113">Wenn der Name eines Benutzers aufgelöst wird, benachrichtigt das [**diskquotacontrol**](diskquotacontrol-object.md) -Objekt seinen Client, indem er das **onusernamechanged** -Ereignis auslöst.</span><span class="sxs-lookup"><span data-stu-id="166c5-113">When a user's name is resolved, the [**DiskQuotaControl**](diskquotacontrol-object.md) object notifies its client by firing the **OnUserNameChanged** event.</span></span> <span data-ttu-id="166c5-114">Ein " **didiskquotauser** "-Objekt, das dem Benutzer zugeordnet ist, wird als Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="166c5-114">A **DIDiskQuotaUser** object associated with the user is passed as a parameter.</span></span> <span data-ttu-id="166c5-115">Dieses Objekt ermöglicht es dem Client, die Kontingent Einstellungen des Benutzers zu ändern.</span><span class="sxs-lookup"><span data-stu-id="166c5-115">This object allows the client to modify the user's quota settings.</span></span>

## <a name="requirements"></a><span data-ttu-id="166c5-116">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="166c5-116">Requirements</span></span>



| <span data-ttu-id="166c5-117">Anforderung</span><span class="sxs-lookup"><span data-stu-id="166c5-117">Requirement</span></span> | <span data-ttu-id="166c5-118">Wert</span><span class="sxs-lookup"><span data-stu-id="166c5-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="166c5-119">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="166c5-119">Minimum supported client</span></span><br/> | <span data-ttu-id="166c5-120">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="166c5-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="166c5-121">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="166c5-121">Minimum supported server</span></span><br/> | <span data-ttu-id="166c5-122">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="166c5-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="166c5-123">Header</span><span class="sxs-lookup"><span data-stu-id="166c5-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="166c5-124"><dt>Dskquota. h</dt></span><span class="sxs-lookup"><span data-stu-id="166c5-124"><dt>Dskquota.h</dt></span></span> </dl>                         |
| <span data-ttu-id="166c5-125">DLL</span><span class="sxs-lookup"><span data-stu-id="166c5-125">DLL</span></span><br/>                      | <dl> <span data-ttu-id="166c5-126"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="166c5-126"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="166c5-127">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="166c5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="166c5-128">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="166c5-128">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




