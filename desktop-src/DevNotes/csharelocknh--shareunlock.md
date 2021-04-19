---
description: Gibt eine freigegebene Sperre frei.
ms.assetid: c2e9eb68-aacb-4196-b09e-d2748efb7fd6
title: 'Csharelocknh:: shareunlock-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ShareUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 80c4311f4bf66000440dac38da6300888a8e5d59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106369665"
---
# <a name="csharelocknhshareunlock-method"></a><span data-ttu-id="dcba6-103">Csharelocknh:: shareunlock-Methode</span><span class="sxs-lookup"><span data-stu-id="dcba6-103">CShareLockNH::ShareUnlock method</span></span>

<span data-ttu-id="dcba6-104">Gibt eine freigegebene Sperre frei.</span><span class="sxs-lookup"><span data-stu-id="dcba6-104">Releases a shared lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="dcba6-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="dcba6-105">Syntax</span></span>


```C++
void ShareUnlock();
```



## <a name="parameters"></a><span data-ttu-id="dcba6-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="dcba6-106">Parameters</span></span>

<span data-ttu-id="dcba6-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="dcba6-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dcba6-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="dcba6-108">Return value</span></span>

<span data-ttu-id="dcba6-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="dcba6-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="dcba6-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="dcba6-110">Remarks</span></span>

<span data-ttu-id="dcba6-111">Jeder aufgerufene [**sharelock**](csharelocknh--sharelock.md) muss mit genau einem **share Unlock**-Aufrufvorgang gekoppelt werden.</span><span class="sxs-lookup"><span data-stu-id="dcba6-111">Each call to [**ShareLock**](csharelocknh--sharelock.md) must be paired with exactly one call to **ShareUnlock**.</span></span> <span data-ttu-id="dcba6-112">Nur ein Thread, der **sharelock** erfolgreich aufruft, kann **shareunlock** aufrufen. Andernfalls kann ein Deadlock auftreten.</span><span class="sxs-lookup"><span data-stu-id="dcba6-112">Only a thread that successfully calls **ShareLock** can call **ShareUnlock**; otherwise, a deadlock can occur.</span></span>

<span data-ttu-id="dcba6-113">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dcba6-113">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="dcba6-114">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="dcba6-114">Requirements</span></span>



| <span data-ttu-id="dcba6-115">Anforderung</span><span class="sxs-lookup"><span data-stu-id="dcba6-115">Requirement</span></span> | <span data-ttu-id="dcba6-116">Wert</span><span class="sxs-lookup"><span data-stu-id="dcba6-116">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="dcba6-117">DLL</span><span class="sxs-lookup"><span data-stu-id="dcba6-117">DLL</span></span><br/> | <dl> <span data-ttu-id="dcba6-118"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dcba6-118"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="dcba6-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dcba6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dcba6-120">**Sharelock**</span><span class="sxs-lookup"><span data-stu-id="dcba6-120">**ShareLock**</span></span>](csharelocknh--sharelock.md)
</dt> </dl>

 

 
