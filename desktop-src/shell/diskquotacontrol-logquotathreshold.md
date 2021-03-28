---
description: Legt einen booleschen Wert fest, der angibt, ob ein System Ereignisprotokoll-Eintrag erfolgt, wenn ein Benutzer seinen zugewiesenen Kontingent Schwellenwert überschreitet, oder ruft diesen booleschen Wert ab.
ms.assetid: 93bf5a4b-a887-4403-8c61-9ca8ba430c47
title: Diskquotacontrol. logquotathreshold (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.LogQuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: fbbf83ae978e46a3867d27c23e8b8f726ba0d7dc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104977168"
---
# <a name="diskquotacontrollogquotathreshold-property"></a><span data-ttu-id="0444d-103">Diskquotacontrol. logquotathreshold (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="0444d-103">DiskQuotaControl.LogQuotaThreshold property</span></span>

<span data-ttu-id="0444d-104">Legt einen booleschen Wert fest, der angibt, ob ein System Ereignisprotokoll-Eintrag erfolgt, wenn ein Benutzer seinen zugewiesenen Kontingent Schwellenwert überschreitet, oder ruft diesen booleschen Wert ab.</span><span class="sxs-lookup"><span data-stu-id="0444d-104">Sets or gets a Boolean value that indicates whether a system event log entry will be made when a user exceeds his or her assigned quota threshold.</span></span>

<span data-ttu-id="0444d-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="0444d-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="0444d-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="0444d-106">Syntax</span></span>


```JScript
bLogQuotaThreshold = DiskQuotaControl.LogQuotaThreshold
DiskQuotaControl.LogQuotaThreshold = bLogQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="0444d-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="0444d-107">Property value</span></span>

<span data-ttu-id="0444d-108">Diese Eigenschaft wird auf **true** festgelegt, wenn ein Eintrag des System Ereignis Protokolls durchgeführt wird, wenn der Benutzer den Schwellenwert für die Kontingent Warnung überschreitet, andernfalls **false** .</span><span class="sxs-lookup"><span data-stu-id="0444d-108">This property is set to **TRUE** if a system event log entry is made when the user exceeds his or her quota warning threshold, or **FALSE** otherwise.</span></span>

## <a name="requirements"></a><span data-ttu-id="0444d-109">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="0444d-109">Requirements</span></span>



| <span data-ttu-id="0444d-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0444d-110">Requirement</span></span> | <span data-ttu-id="0444d-111">Wert</span><span class="sxs-lookup"><span data-stu-id="0444d-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0444d-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0444d-112">Minimum supported client</span></span><br/> | <span data-ttu-id="0444d-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0444d-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="0444d-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0444d-114">Minimum supported server</span></span><br/> | <span data-ttu-id="0444d-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0444d-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="0444d-116">DLL</span><span class="sxs-lookup"><span data-stu-id="0444d-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0444d-117"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="0444d-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0444d-118">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="0444d-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0444d-119">**Defaultquotathreshold**</span><span class="sxs-lookup"><span data-stu-id="0444d-119">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="0444d-120">**Diskquotacontrol-Objekt**</span><span class="sxs-lookup"><span data-stu-id="0444d-120">**DiskQuotaControl Object**</span></span>](diskquotacontrol-object.md)
</dt> <dt>

[<span data-ttu-id="0444d-121">**Logquotalimit**</span><span class="sxs-lookup"><span data-stu-id="0444d-121">**LogQuotaLimit**</span></span>](diskquotacontrol-logquotalimit.md)
</dt> </dl>

 

 




