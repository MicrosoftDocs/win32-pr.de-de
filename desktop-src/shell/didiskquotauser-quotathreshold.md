---
description: Legt den Warnungs Schwellenwert des Benutzers in Bytes fest oder ruft ihn ab.
ms.assetid: 5289d472-d591-4604-91f9-252dd4a1b62b
title: Didiskquotauser. quotathreshold (Eigenschaft)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DIDiskQuotaUser.QuotaThreshold
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 7ce336c84d086c4e4be369278a77e40e59474bc5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103862115"
---
# <a name="didiskquotauserquotathreshold-property"></a><span data-ttu-id="d2ce3-103">Didiskquotauser. quotathreshold (Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="d2ce3-103">DIDiskQuotaUser.QuotaThreshold property</span></span>

<span data-ttu-id="d2ce3-104">Legt den Warnungs Schwellenwert des Benutzers in Bytes fest oder ruft ihn ab.</span><span class="sxs-lookup"><span data-stu-id="d2ce3-104">Sets or gets the user's warning threshold, in bytes.</span></span>

<span data-ttu-id="d2ce3-105">Dies ist eine Eigenschaft mit Lese- und Schreibzugriff.</span><span class="sxs-lookup"><span data-stu-id="d2ce3-105">This property is read/write.</span></span>

## <a name="syntax"></a><span data-ttu-id="d2ce3-106">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2ce3-106">Syntax</span></span>


```JScript
iQuotaThreshold = DIDiskQuotaUser.QuotaThreshold
DIDiskQuotaUser.QuotaThreshold = iQuotaThreshold
```



## <a name="property-value"></a><span data-ttu-id="d2ce3-107">Eigenschaftswert</span><span class="sxs-lookup"><span data-stu-id="d2ce3-107">Property value</span></span>

<span data-ttu-id="d2ce3-108">Ein **ganzzahliger** Wert, der den Warnungs Schwellenwert des Benutzers angibt oder empfängt.</span><span class="sxs-lookup"><span data-stu-id="d2ce3-108">An **Integer** value that specifies or receives the user's warning threshold.</span></span> <span data-ttu-id="d2ce3-109">Wenn die Datenträger Nutzung eines Benutzers diesen Wert überschreitet und die [**logquotathreshold**](diskquotacontrol-logquotathreshold.md) -Eigenschaft auf **true** festgelegt ist, generiert das System einen Ereignisprotokoll Eintrag.</span><span class="sxs-lookup"><span data-stu-id="d2ce3-109">If a user's disk usage exceeds this value and the [**LogQuotaThreshold**](diskquotacontrol-logquotathreshold.md) property is set to **TRUE**, the system generates an event log entry.</span></span>

## <a name="requirements"></a><span data-ttu-id="d2ce3-110">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="d2ce3-110">Requirements</span></span>



| <span data-ttu-id="d2ce3-111">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d2ce3-111">Requirement</span></span> | <span data-ttu-id="d2ce3-112">Wert</span><span class="sxs-lookup"><span data-stu-id="d2ce3-112">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d2ce3-113">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d2ce3-113">Minimum supported client</span></span><br/> | <span data-ttu-id="d2ce3-114">Windows 2000 Professional \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2ce3-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="d2ce3-115">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d2ce3-115">Minimum supported server</span></span><br/> | <span data-ttu-id="d2ce3-116">Windows 2000 Server \[nur Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d2ce3-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                          |
| <span data-ttu-id="d2ce3-117">DLL</span><span class="sxs-lookup"><span data-stu-id="d2ce3-117">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d2ce3-118"><dt>Shell32.dll (Version 5,0 oder höher)</dt></span><span class="sxs-lookup"><span data-stu-id="d2ce3-118"><dt>Shell32.dll (version 5.0 or later)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d2ce3-119">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="d2ce3-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d2ce3-120">**Defaultquotathreshold**</span><span class="sxs-lookup"><span data-stu-id="d2ce3-120">**DefaultQuotaThreshold**</span></span>](diskquotacontrol-defaultquotathreshold.md)
</dt> <dt>

[<span data-ttu-id="d2ce3-121">**Didiskquotauser**</span><span class="sxs-lookup"><span data-stu-id="d2ce3-121">**DIDiskQuotaUser**</span></span>](didiskquotauser-object.md)
</dt> <dt>

[<span data-ttu-id="d2ce3-122">**QuotaLimit**</span><span class="sxs-lookup"><span data-stu-id="d2ce3-122">**QuotaLimit**</span></span>](didiskquotauser-quotalimit.md)
</dt> <dt>

[<span data-ttu-id="d2ce3-123">**Quotader OLDTEXT**</span><span class="sxs-lookup"><span data-stu-id="d2ce3-123">**QuotaThresholdText**</span></span>](didiskquotauser-quotathresholdtext.md)
</dt> </dl>

 

 




