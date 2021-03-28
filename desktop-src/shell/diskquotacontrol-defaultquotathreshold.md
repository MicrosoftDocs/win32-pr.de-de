---
description: Legt den Standard Kontingent Schwellenwert fest oder ruft ihn ab.
ms.assetid: d3f23e52-586f-4cb8-b91c-44a71f8f94b2
title: Diskquotacontrol. defaultquotathreshold (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: a4ce4205ee8bcc73c78bd1aabe7d8659ac3f5489
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977193"
---
# <a name="diskquotacontroldefaultquotathreshold-property"></a><span data-ttu-id="faefe-103">Diskquotacontrol. defaultquotathreshold (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="faefe-103">DiskQuotaControl.DefaultQuotaThreshold property</span></span>

<span data-ttu-id="faefe-104">Legt den Standard Kontingent Schwellenwert fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="faefe-104">Sets or gets the default quota threshold.</span></span>

<span data-ttu-id="faefe-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="faefe-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="faefe-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="faefe-106">Syntax</span></span>


```JScript
iDefaultQuotaThreshold = DiskQuotaControl.DefaultQuotaThreshold
DiskQuotaControl.DefaultQuotaThreshold = iDefaultQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="faefe-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="faefe-107">Property value</span></span>

<span data-ttu-id="faefe-108">Ein **ganzzahliger** Wert, der auf den Standard Warnungs Schwellenwert für neue Benutzer in Bytes festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="faefe-108">An **Integer** value that is set to the default warning threshold for new users, in bytes.</span></span>

## <a name="remarks"></a><span data-ttu-id="faefe-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="faefe-109">Remarks</span></span>

<span data-ttu-id="faefe-110">Der Standard Schwellenwert für Kontingente wird automatisch auf neue Benutzer des Volumes angewendet.</span><span class="sxs-lookup"><span data-stu-id="faefe-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="faefe-111">Wenn die Datenträger Nutzung eines Benutzers diesen Wert überschreitet und die [**logquotathreshold**](diskquotacontrol-logquotathreshold.md) -Eigenschaft auf **true** festgelegt ist, generiert das System einen Ereignisprotokoll Eintrag.</span><span class="sxs-lookup"><span data-stu-id="faefe-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="faefe-112">Wenn der Standard Schwellenwert z. b. 10,0 MB beträgt, lautet der Wert der Eigenschaft "10,0 MB".</span><span class="sxs-lookup"><span data-stu-id="faefe-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="faefe-113">Wenn für das Volume kein Standard Schwellenwert festgelegt ist, wird die-Eigenschaft auf "No Limit" oder die lokalisierte Entsprechung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="faefe-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="faefe-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="faefe-114">Requirements</span></span>



| <span data-ttu-id="faefe-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="faefe-115">Requirement</span></span> | <span data-ttu-id="faefe-116">Wert</span><span class="sxs-lookup"><span data-stu-id="faefe-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="faefe-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="faefe-117">Minimum supported client</span></span><br/> | <span data-ttu-id="faefe-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="faefe-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="faefe-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="faefe-119">Minimum supported server</span></span><br/> | <span data-ttu-id="faefe-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="faefe-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="faefe-121">DLL</span><span class="sxs-lookup"><span data-stu-id="faefe-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="faefe-122"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="faefe-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="faefe-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="faefe-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="faefe-124">**Diskquotacontrol**</span><span class="sxs-lookup"><span data-stu-id="faefe-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




