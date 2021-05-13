---
description: Ruft die aktuelle Datenträgerverwendung des Benutzers als Textzeichenfolge ab.
title: DIDiskQuotaUser.QuotaUsedText (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaUsedText
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: be27a17c-77ec-4016-8c2e-16fbc88c7c7a
ms.openlocfilehash: bf818bdcd22b734c6f4638a837af97bfecef1695
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/12/2021
ms.locfileid: "109843211"
---
# <a name="didiskquotauserquotausedtext-property"></a><span data-ttu-id="6cfa9-103">DIDiskQuotaUser.QuotaUsedText (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="6cfa9-103">DIDiskQuotaUser.QuotaUsedText property</span></span>

<span data-ttu-id="6cfa9-104">Ruft die aktuelle Datenträgerverwendung des Benutzers als Textzeichenfolge ab.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-104">Gets the user's current disk usage as a text string.</span></span>

<span data-ttu-id="6cfa9-105">Diese Eigenschaft ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-105">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cfa9-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="6cfa9-106">Syntax</span></span>


```JScript
QuotaUsedText = DIDiskQuotaUser.QuotaUsedText
```



## <a name="property-value"></a><span data-ttu-id="6cfa9-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="6cfa9-107">Property value</span></span>

<span data-ttu-id="6cfa9-108">Ein Zeichenfolgenwert, der auf die Derzeit verwendete Speicherplatzmenge festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-108">A string value that is set to the amount of disk space currently in use.</span></span> <span data-ttu-id="6cfa9-109">Wenn die NTFS-Dateikomprimierung aktiviert ist, gibt diese Eigenschaft den Speicherplatz an, den die Daten in einem unkomprimierten Zustand benötigen würden.</span><span class="sxs-lookup"><span data-stu-id="6cfa9-109">If NTFS file compression is enabled, this property reflects the amount of disk space that the data would require in an uncompressed state.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cfa9-110">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="6cfa9-110">Requirements</span></span>



| <span data-ttu-id="6cfa9-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="6cfa9-111">Requirement</span></span> | <span data-ttu-id="6cfa9-112">Wert</span><span class="sxs-lookup"><span data-stu-id="6cfa9-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cfa9-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="6cfa9-113">Minimum supported client</span></span><br/> | <span data-ttu-id="6cfa9-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cfa9-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="6cfa9-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="6cfa9-115">Minimum supported server</span></span><br/> | <span data-ttu-id="6cfa9-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="6cfa9-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="6cfa9-117">DLL</span><span class="sxs-lookup"><span data-stu-id="6cfa9-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cfa9-118"><dt>Shell32.dll (Version 5.0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="6cfa9-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cfa9-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6cfa9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cfa9-120">**DIDiskQuotaUser-Objekt**</span><span class="sxs-lookup"><span data-stu-id="6cfa9-120">**DIDiskQuotaUser Object**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="6cfa9-121">**QuotaLimitText**</span><span class="sxs-lookup"><span data-stu-id="6cfa9-121">**QuotaLimitText**</span></span>](didiskquotauser-quotalimittext.md)
</dt> <dt>

[<span data-ttu-id="6cfa9-122">**QuotaThresholdText**</span><span class="sxs-lookup"><span data-stu-id="6cfa9-122">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> <dt>

[<span data-ttu-id="6cfa9-123">**QuotaUsed**</span><span class="sxs-lookup"><span data-stu-id="6cfa9-123">**QuotaUsed**</span></span>](didiskquotauser-quotaused.md)
</dt> </dl>

 

 




