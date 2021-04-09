---
description: Löscht alle Überprüfungs Profile, die für den Benutzer in dem System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: Iscanprofilemgr::D eleteallprofilesforuser-Methode (scanprofilemgr. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: c5d723379bb542346e3612f70c19a1629d325ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104130024"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a><span data-ttu-id="d044a-103">Iscanprofilemgr::D eleteallprofilesforuser-Methode</span><span class="sxs-lookup"><span data-stu-id="d044a-103">IScanProfileMgr::DeleteAllProfilesForUser method</span></span>

<span data-ttu-id="d044a-104">Löscht alle Überprüfungs Profile, die für den Benutzer in dem System verfügbar sind, unter dem Ihre Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d044a-104">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="d044a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="d044a-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a><span data-ttu-id="d044a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="d044a-106">Parameters</span></span>

<span data-ttu-id="d044a-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="d044a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d044a-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="d044a-108">Return value</span></span>

<span data-ttu-id="d044a-109">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="d044a-109">Type: **HRESULT**</span></span>

<span data-ttu-id="d044a-110">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="d044a-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="d044a-111">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="d044a-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="d044a-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="d044a-112">Requirements</span></span>



| <span data-ttu-id="d044a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="d044a-113">Requirement</span></span> | <span data-ttu-id="d044a-114">Wert</span><span class="sxs-lookup"><span data-stu-id="d044a-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="d044a-115">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="d044a-115">Minimum supported client</span></span><br/> | <span data-ttu-id="d044a-116">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d044a-116">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="d044a-117">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="d044a-117">Minimum supported server</span></span><br/> | <span data-ttu-id="d044a-118">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="d044a-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="d044a-119">Header</span><span class="sxs-lookup"><span data-stu-id="d044a-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="d044a-120"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="d044a-120"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="d044a-121">IDL</span><span class="sxs-lookup"><span data-stu-id="d044a-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d044a-122"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d044a-122"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d044a-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d044a-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d044a-124">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="d044a-124">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="d044a-125">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="d044a-125">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




