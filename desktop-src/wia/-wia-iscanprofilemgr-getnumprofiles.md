---
description: Ruft die Anzahl der Überprüfungs Profile ab, die für den Benutzer im System erstellt wurden, unter dem Ihre Anwendung ausgeführt wird.
ms.assetid: 0667a885-d61f-4c44-b988-a42242c2678e
title: 'Iscanprofilemgr:: getnumprofiles-Methode (scanprofilemgr. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a8c3167bd428054054a32d7823ce57e562501533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "106358467"
---
# <a name="iscanprofilemgrgetnumprofiles-method"></a><span data-ttu-id="0dd16-103">Iscanprofilemgr:: getnumprofiles-Methode</span><span class="sxs-lookup"><span data-stu-id="0dd16-103">IScanProfileMgr::GetNumProfiles method</span></span>

<span data-ttu-id="0dd16-104">Ruft die Anzahl der Überprüfungs Profile ab, die für den Benutzer im System erstellt wurden, unter dem Ihre Anwendung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0dd16-104">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd16-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="0dd16-105">Syntax</span></span>


```C++
HRESULT GetNumProfiles(
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="0dd16-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="0dd16-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dd16-107">*pulnumprofiles* \[ vorgenommen\]</span><span class="sxs-lookup"><span data-stu-id="0dd16-107">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd16-108">Typ: \**ulong \** _</span><span class="sxs-lookup"><span data-stu-id="0dd16-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="0dd16-109">Ein Zeiger auf die Anzahl der Profile, die für den Benutzer erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="0dd16-109">A pointer to the number of profiles created for the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dd16-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0dd16-110">Return value</span></span>

<span data-ttu-id="0dd16-111">Type: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="0dd16-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="0dd16-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="0dd16-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="0dd16-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0dd16-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dd16-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="0dd16-114">Requirements</span></span>



| <span data-ttu-id="0dd16-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="0dd16-115">Requirement</span></span> | <span data-ttu-id="0dd16-116">Wert</span><span class="sxs-lookup"><span data-stu-id="0dd16-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd16-117">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="0dd16-117">Minimum supported client</span></span><br/> | <span data-ttu-id="0dd16-118">Nur Windows Vista \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0dd16-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="0dd16-119">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="0dd16-119">Minimum supported server</span></span><br/> | <span data-ttu-id="0dd16-120">Nur Windows Server 2008 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="0dd16-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="0dd16-121">Header</span><span class="sxs-lookup"><span data-stu-id="0dd16-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="0dd16-122"><dt>Scanprofilemgr. h</dt></span><span class="sxs-lookup"><span data-stu-id="0dd16-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="0dd16-123">IDL</span><span class="sxs-lookup"><span data-stu-id="0dd16-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0dd16-124"><dt>Scanprofiles. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0dd16-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dd16-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0dd16-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd16-126">**Iscanprofilemgr**</span><span class="sxs-lookup"><span data-stu-id="0dd16-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="0dd16-127">Profil Schema überprüfen</span><span class="sxs-lookup"><span data-stu-id="0dd16-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




