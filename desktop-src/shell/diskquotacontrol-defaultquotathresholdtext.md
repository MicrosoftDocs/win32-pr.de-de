---
description: Ruft den Standard Kontingent Schwellenwert als Text Zeichenfolge ab.
ms.assetid: 48b1cbd5-12dd-4c31-a14c-7904d29f6eb9
title: Diskquotacontrol. defaultquotader OLDTEXT-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaThresholdText
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: b3b209c7c8e71b49fd3b9fce90b9ea30b584bd65
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104128440"
---
# <a name="diskquotacontroldefaultquotathresholdtext-property"></a><span data-ttu-id="ddc4c-103">Diskquotacontrol. defaultquotader OLDTEXT-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="ddc4c-103">DiskQuotaControl.DefaultQuotaThresholdText property</span></span>

<span data-ttu-id="ddc4c-104">Ruft den Standard Kontingent Schwellenwert als Text Zeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="ddc4c-104">Gets the default quota threshold as a text string.</span></span>

<span data-ttu-id="ddc4c-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="ddc4c-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="ddc4c-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="ddc4c-106">Syntax</span></span>


```JScript
DefaultQuotaThresholdText = DiskQuotaControl.DefaultQuotaThresholdText
```



## <a name="property-value"></a><span data-ttu-id="ddc4c-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="ddc4c-107">Property value</span></span>

<span data-ttu-id="ddc4c-108">Ein Zeichen folgen Wert, der den Standard Kontingent Schwellenwert für das Volume enthält.</span><span class="sxs-lookup"><span data-stu-id="ddc4c-108">A string value that contains the default quota threshold for the volume.</span></span>

## <a name="remarks"></a><span data-ttu-id="ddc4c-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ddc4c-109">Remarks</span></span>

<span data-ttu-id="ddc4c-110">Der Standard Schwellenwert für Kontingente wird automatisch auf neue Benutzer des Volumes angewendet.</span><span class="sxs-lookup"><span data-stu-id="ddc4c-110">The default quota threshold is applied automatically to new users of the volume.</span></span> <span data-ttu-id="ddc4c-111">Wenn die Datenträger Nutzung eines Benutzers diesen Wert überschreitet und die [**logquotathreshold**](diskquotacontrol-logquotathreshold.md) -Eigenschaft auf **true** festgelegt ist, generiert das System einen Ereignisprotokoll Eintrag.</span><span class="sxs-lookup"><span data-stu-id="ddc4c-111">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span> <span data-ttu-id="ddc4c-112">Wenn der Standard Schwellenwert z. b. 10,0 MB beträgt, lautet der Wert der Eigenschaft "10,0 MB".</span><span class="sxs-lookup"><span data-stu-id="ddc4c-112">For example, if the default threshold is 10.0 MB, the value of the property is "10.0 MB".</span></span> <span data-ttu-id="ddc4c-113">Wenn für das Volume kein Standard Schwellenwert festgelegt ist, wird die-Eigenschaft auf "No Limit" oder die lokalisierte Entsprechung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="ddc4c-113">If the volume has no default threshold, the property is set to "No Limit" or the localized equivalent.</span></span>

## <a name="requirements"></a><span data-ttu-id="ddc4c-114">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="ddc4c-114">Requirements</span></span>



| <span data-ttu-id="ddc4c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ddc4c-115">Requirement</span></span> | <span data-ttu-id="ddc4c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="ddc4c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ddc4c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="ddc4c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ddc4c-118">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddc4c-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="ddc4c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="ddc4c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ddc4c-120">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="ddc4c-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="ddc4c-121">DLL</span><span class="sxs-lookup"><span data-stu-id="ddc4c-121">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ddc4c-122"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="ddc4c-122"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ddc4c-123">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="ddc4c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ddc4c-124">**Diskquotacontrol**</span><span class="sxs-lookup"><span data-stu-id="ddc4c-124">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




