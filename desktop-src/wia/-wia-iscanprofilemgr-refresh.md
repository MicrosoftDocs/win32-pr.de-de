---
description: Listet alle Scan Profile im System erneut auf.
ms.assetid: f5e49645-e81a-4750-8ea5-f0c698a61752
title: 'Iscanprofilemgr:: Refresh-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.Refresh
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e4af44e95889abf35fe13e1669411513458a16c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "103959087"
---
# <a name="iscanprofilemgrrefresh-method"></a><span data-ttu-id="84b5c-103">Iscanprofilemgr:: Refresh-Methode</span><span class="sxs-lookup"><span data-stu-id="84b5c-103">IScanProfileMgr::Refresh method</span></span>

<span data-ttu-id="84b5c-104">Listet alle Scan Profile im System erneut auf.</span><span class="sxs-lookup"><span data-stu-id="84b5c-104">Re-enumerates all the scan profiles in the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="84b5c-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="84b5c-105">Syntax</span></span>


```C++
HRESULT Refresh();
```



## <a name="parameters"></a><span data-ttu-id="84b5c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="84b5c-106">Parameters</span></span>

<span data-ttu-id="84b5c-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="84b5c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="84b5c-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="84b5c-108">Return value</span></span>

<span data-ttu-id="84b5c-109">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="84b5c-109">Type: **HRESULT**</span></span>

<span data-ttu-id="84b5c-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="84b5c-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="84b5c-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="84b5c-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="84b5c-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84b5c-112">Remarks</span></span>

<span data-ttu-id="84b5c-113">Verwenden Sie diese Methode, wenn mehrere [**iscanprofilemgr**](-wia-iscanprofilemgr.md) -Objekte gleichzeitig Profile erstellen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="84b5c-113">Use this method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="84b5c-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="84b5c-114">Requirements</span></span>



| <span data-ttu-id="84b5c-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="84b5c-115">Requirement</span></span> | <span data-ttu-id="84b5c-116">Wert</span><span class="sxs-lookup"><span data-stu-id="84b5c-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="84b5c-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="84b5c-117">Minimum supported client</span></span><br/> | <span data-ttu-id="84b5c-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84b5c-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="84b5c-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="84b5c-119">Minimum supported server</span></span><br/> | <span data-ttu-id="84b5c-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="84b5c-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="84b5c-121">Header</span><span class="sxs-lookup"><span data-stu-id="84b5c-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="84b5c-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="84b5c-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="84b5c-123">IDL</span><span class="sxs-lookup"><span data-stu-id="84b5c-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="84b5c-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="84b5c-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="84b5c-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="84b5c-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="84b5c-126">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="84b5c-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="84b5c-127">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="84b5c-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




