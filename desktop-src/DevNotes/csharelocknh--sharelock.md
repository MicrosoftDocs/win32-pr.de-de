---
description: Erhält eine freigegebene Sperre.
ms.assetid: dff9a842-573a-4530-820d-6fd9001e502a
title: 'Csharelocknh:: sharelock-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: d0c77564deceab29a8bee0cbffbd477559117cbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106357651"
---
# <a name="csharelocknhsharelock-method"></a><span data-ttu-id="fc7e9-103">Csharelocknh:: sharelock-Methode</span><span class="sxs-lookup"><span data-stu-id="fc7e9-103">CShareLockNH::ShareLock method</span></span>

<span data-ttu-id="fc7e9-104">Erhält eine freigegebene Sperre.</span><span class="sxs-lookup"><span data-stu-id="fc7e9-104">Obtains a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc7e9-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="fc7e9-105">Syntax</span></span>


```C++
void ShareLock();
```



## <a name="parameters"></a><span data-ttu-id="fc7e9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc7e9-106">Parameters</span></span>

<span data-ttu-id="fc7e9-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="fc7e9-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fc7e9-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="fc7e9-108">Return value</span></span>

<span data-ttu-id="fc7e9-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="fc7e9-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fc7e9-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fc7e9-110">Remarks</span></span>

<span data-ttu-id="fc7e9-111">Jeder aufgerufene **sharelock** muss mit genau einem [**share Unlock**](csharelocknh--shareunlock.md)-Aufrufvorgang gekoppelt werden.</span><span class="sxs-lookup"><span data-stu-id="fc7e9-111">Each call to **ShareLock** must be paired with exactly one call to [**ShareUnlock**](csharelocknh--shareunlock.md).</span></span> <span data-ttu-id="fc7e9-112">Nur ein Thread, der **sharelock** erfolgreich aufruft, kann **shareunlock** aufrufen. Andernfalls kann ein Deadlock auftreten.</span><span class="sxs-lookup"><span data-stu-id="fc7e9-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="fc7e9-113">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="fc7e9-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="fc7e9-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fc7e9-114">Requirements</span></span>



| <span data-ttu-id="fc7e9-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="fc7e9-115">Requirement</span></span> | <span data-ttu-id="fc7e9-116">Wert</span><span class="sxs-lookup"><span data-stu-id="fc7e9-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="fc7e9-117">DLL</span><span class="sxs-lookup"><span data-stu-id="fc7e9-117">DLL</span></span><br/> | <dl> <span data-ttu-id="fc7e9-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="fc7e9-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fc7e9-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc7e9-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fc7e9-120">**Share Unlock**</span><span class="sxs-lookup"><span data-stu-id="fc7e9-120">**ShareUnlock**</span></span>](csharelocknh--shareunlock.md)
</dt> </dl>

 

 
