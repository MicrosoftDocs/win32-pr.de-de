---
description: Erhält eine Lese-/Schreibsperre.
ms.assetid: fd212dd9-034b-4e0c-9111-e3460ea6f133
title: 'Csharelocknh:: exclusivelock-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 8b35b544c10e6dde2887e75971d747feade5517e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106362067"
---
# <a name="csharelocknhexclusivelock-method"></a><span data-ttu-id="658b5-103">Csharelocknh:: exclusivelock-Methode</span><span class="sxs-lookup"><span data-stu-id="658b5-103">CShareLockNH::ExclusiveLock method</span></span>

<span data-ttu-id="658b5-104">Erhält eine Lese-/Schreibsperre.</span><span class="sxs-lookup"><span data-stu-id="658b5-104">Acquires a reader/writer lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="658b5-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="658b5-105">Syntax</span></span>


```C++
void ExclusiveLock();
```



## <a name="parameters"></a><span data-ttu-id="658b5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="658b5-106">Parameters</span></span>

<span data-ttu-id="658b5-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="658b5-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="658b5-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="658b5-108">Return value</span></span>

<span data-ttu-id="658b5-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="658b5-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="658b5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="658b5-110">Remarks</span></span>

<span data-ttu-id="658b5-111">Jeder Rückruf von **exclusivelock** muss mit genau einem Rückruf von [**exclusiveunlock**](csharelocknh--exclusiveunlock.md) gekoppelt werden, um das Risiko eines Deadlocks zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="658b5-111">Each call to **ExclusiveLock** must be paired with exactly one call to [**ExclusiveUnlock**](csharelocknh--exclusiveunlock.md) to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="658b5-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="658b5-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="658b5-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="658b5-113">Requirements</span></span>



| <span data-ttu-id="658b5-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="658b5-114">Requirement</span></span> | <span data-ttu-id="658b5-115">Wert</span><span class="sxs-lookup"><span data-stu-id="658b5-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="658b5-116">DLL</span><span class="sxs-lookup"><span data-stu-id="658b5-116">DLL</span></span><br/> | <dl> <span data-ttu-id="658b5-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="658b5-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="658b5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="658b5-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="658b5-119">**Exclusiveunlock**</span><span class="sxs-lookup"><span data-stu-id="658b5-119">**ExclusiveUnlock**</span></span>](csharelocknh--exclusiveunlock.md)
</dt> </dl>

 

 
