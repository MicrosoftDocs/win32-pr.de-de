---
description: Setzt die interne Anzahl der abgerufenen Schnittstellen in der-Enumeration zurück.
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: 'Ienumumuseridentity:: Reset-Methode (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 05b3c5d38575fa1b2957c28070d642ad15f846ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/07/2021
ms.locfileid: "104215934"
---
# <a name="ienumuseridentityreset-method"></a><span data-ttu-id="bf2b0-103">Ienumumuseridentity:: Reset-Methode</span><span class="sxs-lookup"><span data-stu-id="bf2b0-103">IEnumUserIdentity::Reset method</span></span>

<span data-ttu-id="bf2b0-104">\[**Ienumumuseridentity:: Reset** wird nicht unterstützt und kann in Zukunft geändert oder nicht verfügbar sein.</span><span class="sxs-lookup"><span data-stu-id="bf2b0-104">\[**IEnumUserIdentity::Reset** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bf2b0-105">Verwenden Sie stattdessen [Benutzerkonten mit schneller Benutzerumschaltung und Remotedesktop](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="bf2b0-105">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="bf2b0-106">Setzt die interne Anzahl der abgerufenen Schnittstellen in der-Enumeration zurück.</span><span class="sxs-lookup"><span data-stu-id="bf2b0-106">Resets the internal count of retrieved interfaces in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf2b0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="bf2b0-107">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="bf2b0-108">Parameter</span><span class="sxs-lookup"><span data-stu-id="bf2b0-108">Parameters</span></span>

<span data-ttu-id="bf2b0-109">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="bf2b0-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf2b0-110">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="bf2b0-110">Return value</span></span>

<span data-ttu-id="bf2b0-111">Typ: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bf2b0-111">Type: **HRESULT**</span></span>

<span data-ttu-id="bf2b0-112">Wenn diese Methode erfolgreich ausgeführt wird, gibt Sie **S \_ OK** zurück.</span><span class="sxs-lookup"><span data-stu-id="bf2b0-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="bf2b0-113">Andernfalls wird ein **HRESULT** -Fehlercode zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bf2b0-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf2b0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bf2b0-114">Remarks</span></span>

<span data-ttu-id="bf2b0-115">[**Ienumumuseridentity**](ienumuseridentity.md) behält eine interne Anzahl bei, die angibt, welche Schnittstelle als nächstes abgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="bf2b0-115">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="bf2b0-116">Durch Aufrufen dieser Methode wird der Wert dieser Anzahl zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="bf2b0-116">Calling this method will reset the value of this count.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf2b0-117">Requirements (Anforderungen)</span><span class="sxs-lookup"><span data-stu-id="bf2b0-117">Requirements</span></span>



| <span data-ttu-id="bf2b0-118">Anforderung</span><span class="sxs-lookup"><span data-stu-id="bf2b0-118">Requirement</span></span> | <span data-ttu-id="bf2b0-119">Wert</span><span class="sxs-lookup"><span data-stu-id="bf2b0-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bf2b0-120">Unterstützte Mindestversion (Client)</span><span class="sxs-lookup"><span data-stu-id="bf2b0-120">Minimum supported client</span></span><br/> | <span data-ttu-id="bf2b0-121">Nur Windows XP \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf2b0-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="bf2b0-122">Unterstützte Mindestversion (Server)</span><span class="sxs-lookup"><span data-stu-id="bf2b0-122">Minimum supported server</span></span><br/> | <span data-ttu-id="bf2b0-123">Nur Windows Server 2003 \[ -Desktop-Apps\]</span><span class="sxs-lookup"><span data-stu-id="bf2b0-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bf2b0-124">Ende des Supports (Client)</span><span class="sxs-lookup"><span data-stu-id="bf2b0-124">End of client support</span></span><br/>    | <span data-ttu-id="bf2b0-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="bf2b0-125">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="bf2b0-126">Ende des Supports (Server)</span><span class="sxs-lookup"><span data-stu-id="bf2b0-126">End of server support</span></span><br/>    | <span data-ttu-id="bf2b0-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="bf2b0-127">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="bf2b0-128">Header</span><span class="sxs-lookup"><span data-stu-id="bf2b0-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="bf2b0-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="bf2b0-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="bf2b0-130">IDL</span><span class="sxs-lookup"><span data-stu-id="bf2b0-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bf2b0-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bf2b0-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="bf2b0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="bf2b0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bf2b0-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bf2b0-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf2b0-134">Weitere Informationen</span><span class="sxs-lookup"><span data-stu-id="bf2b0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf2b0-135">**Iumumuseridentity**</span><span class="sxs-lookup"><span data-stu-id="bf2b0-135">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="bf2b0-136">**Iendumuseridentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="bf2b0-136">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="bf2b0-137">**Iendumuseridentity:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="bf2b0-137">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> <dt>

[<span data-ttu-id="bf2b0-138">**Ienumumuseridentity:: Next**</span><span class="sxs-lookup"><span data-stu-id="bf2b0-138">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




