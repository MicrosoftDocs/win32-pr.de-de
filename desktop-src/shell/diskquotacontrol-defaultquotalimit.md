---
description: Legt das Standardkontingentlimit fest oder ruft es ab.
title: DiskQuotaControl.DefaultQuotaLimit-Eigenschaft
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DiskQuotaControl.DefaultQuotaLimit
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 7d123bff-5dae-4430-be22-a822e231e43e
ms.openlocfilehash: 6031f0fbf6c3c872252e9a80204c07356c54d0cb
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843201"
---
# <a name="diskquotacontroldefaultquotalimit-property"></a><span data-ttu-id="fd378-103">DiskQuotaControl.DefaultQuotaLimit-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="fd378-103">DiskQuotaControl.DefaultQuotaLimit property</span></span>

<span data-ttu-id="fd378-104">Legt das Standardkontingentlimit fest oder ruft es ab.</span><span class="sxs-lookup"><span data-stu-id="fd378-104">Sets or gets the default quota limit.</span></span>

<span data-ttu-id="fd378-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="fd378-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="fd378-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="fd378-106">Syntax</span></span>


```JScript
iDefaultQuotaLimit = DiskQuotaControl.DefaultQuotaLimit
DiskQuotaControl.DefaultQuotaLimit = iDefaultQuotaLimit
```



## <a name="property-value"></a><span data-ttu-id="fd378-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="fd378-107">Property value</span></span>

<span data-ttu-id="fd378-108">Ein **Ganzzahlwert,** der die Standardkontingentgrenze für neue Benutzer in Bytes angibt oder empfängt.</span><span class="sxs-lookup"><span data-stu-id="fd378-108">An **Integer** value that specifies or receives the default quota limit for new users, in bytes.</span></span>

## <a name="requirements"></a><span data-ttu-id="fd378-109">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fd378-109">Requirements</span></span>



| <span data-ttu-id="fd378-110">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fd378-110">Requirement</span></span> | <span data-ttu-id="fd378-111">Wert</span><span class="sxs-lookup"><span data-stu-id="fd378-111">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fd378-112">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="fd378-112">Minimum supported client</span></span><br/> | <span data-ttu-id="fd378-113">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd378-113">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="fd378-114">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="fd378-114">Minimum supported server</span></span><br/> | <span data-ttu-id="fd378-115">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="fd378-115">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="fd378-116">DLL</span><span class="sxs-lookup"><span data-stu-id="fd378-116">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fd378-117"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="fd378-117"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fd378-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd378-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fd378-119">**DefaultQuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="fd378-119">**DefaultQuotaLimitText**</span></span>](diskquotacontrol-defaultquotalimittext.md)
</dt> <dt>

[<span data-ttu-id="fd378-120">**DiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="fd378-120">**DiskQuotaControl**</span></span>](diskquotacontrol-object.md)
</dt> </dl>

 

 




