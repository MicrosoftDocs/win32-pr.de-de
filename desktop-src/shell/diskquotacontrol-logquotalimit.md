---
description: Legt einen booleschen Wert fest, der angibt, ob ein Eintrag des System Ereignis Protokolls durchgeführt wird, wenn ein Benutzer sein zugewiesenes Kontingent Limit überschreitet, oder ruft ihn ab.
ms.assetid: f7f6b0a0-0fd1-47bd-9950-d6d579819377
title: Diskquotacontrol. logquotalimit (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3db64d7fb06ed8bfb7ba8c2483eb413f3f01a224
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977169"
---
# <a name="diskquotacontrollogquotalimit-property"></a><span data-ttu-id="62b6a-103">Diskquotacontrol. logquotalimit (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="62b6a-103">DiskQuotaControl.LogQuotaLimit property</span></span>

<span data-ttu-id="62b6a-104">Legt einen booleschen Wert fest, der angibt, ob ein Eintrag des System Ereignis Protokolls durchgeführt wird, wenn ein Benutzer sein zugewiesenes Kontingent Limit überschreitet, oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="62b6a-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota limit.</span></span>

<span data-ttu-id="62b6a-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="62b6a-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="62b6a-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="62b6a-106">Syntax</span></span>


```JScript
bLogQuotaLimit = DiskQuotaControl.LogQuotaLimit
DiskQuotaControl.LogQuotaLimit = bLogQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="62b6a-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="62b6a-107">Property value</span></span>

<span data-ttu-id="62b6a-108">Diese Eigenschaft wird auf **true** festgelegt, wenn ein Eintrag des System Ereignis Protokolls durchgeführt wird, wenn der Benutzer das Kontingent Limit überschreitet, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="62b6a-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota limit, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="62b6a-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="62b6a-109">Requirements</span></span>



| <span data-ttu-id="62b6a-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="62b6a-110">Requirement</span></span> | <span data-ttu-id="62b6a-111">Wert</span><span class="sxs-lookup"><span data-stu-id="62b6a-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62b6a-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="62b6a-112">Minimum supported client</span></span><br/> | <span data-ttu-id="62b6a-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62b6a-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="62b6a-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="62b6a-114">Minimum supported server</span></span><br/> | <span data-ttu-id="62b6a-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="62b6a-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="62b6a-116">DLL</span><span class="sxs-lookup"><span data-stu-id="62b6a-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="62b6a-117"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="62b6a-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62b6a-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="62b6a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62b6a-119">**Defaultquotalimit**</span><span class="sxs-lookup"><span data-stu-id="62b6a-119">**DefaultQuotaLimit**</span></span>](diskquotacontrol-defaultquotalimit.md)
</dt> <dt>

[<span data-ttu-id="62b6a-120">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="62b6a-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="62b6a-121">**Logquotathreshold**</span><span class="sxs-lookup"><span data-stu-id="62b6a-121">**LogQuotaThreshold**</span></span>](diskquotacontrol-logquotathreshold.md)
</dt> </dl>

 

 




