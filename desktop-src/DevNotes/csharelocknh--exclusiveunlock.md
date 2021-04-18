---
description: Gibt eine Sperre frei, die mithilfe von exclusivelock für den freigegebenen Modus abgerufen wurde.
ms.assetid: d38354f0-2eb3-4924-99b5-1331e587ce32
title: 'Csharelocknh:: exclusiveunlock-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.ExclusiveUnlock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: f5fae5d6131bfcb386d52880b530f3def9464442
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106360982"
---
# <a name="csharelocknhexclusiveunlock-method"></a><span data-ttu-id="21126-103">Csharelocknh:: exclusiveunlock-Methode</span><span class="sxs-lookup"><span data-stu-id="21126-103">CShareLockNH::ExclusiveUnlock method</span></span>

<span data-ttu-id="21126-104">Gibt eine Sperre frei, die mithilfe von [**exclusivelock**](csharelocknh--exclusivelock.md) für den freigegebenen Modus abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="21126-104">Releases a lock acquired by using [**ExclusiveLock**](csharelocknh--exclusivelock.md) to shared mode.</span></span>

## <a name="syntax"></a><span data-ttu-id="21126-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="21126-105">Syntax</span></span>


```C++
void ExclusiveUnlock();
```



## <a name="parameters"></a><span data-ttu-id="21126-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="21126-106">Parameters</span></span>

<span data-ttu-id="21126-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="21126-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="21126-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="21126-108">Return value</span></span>

<span data-ttu-id="21126-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="21126-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="21126-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="21126-110">Remarks</span></span>

<span data-ttu-id="21126-111">Jeder Rückruf von [**exclusivelock**](csharelocknh--exclusivelock.md) muss mit genau einem Rückruf von **exclusiveunlock** gekoppelt werden, um das Risiko eines Deadlocks zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="21126-111">Each call to [**ExclusiveLock**](csharelocknh--exclusivelock.md) must be paired with exactly one call to **ExclusiveUnlock** to avoid the risk of a deadlock.</span></span>

<span data-ttu-id="21126-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="21126-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="21126-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="21126-113">Requirements</span></span>



| <span data-ttu-id="21126-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="21126-114">Requirement</span></span> | <span data-ttu-id="21126-115">Wert</span><span class="sxs-lookup"><span data-stu-id="21126-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="21126-116">DLL</span><span class="sxs-lookup"><span data-stu-id="21126-116">DLL</span></span><br/> | <dl> <span data-ttu-id="21126-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="21126-117"><dt>Rwnh.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21126-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21126-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21126-119">**Exclusivelock**</span><span class="sxs-lookup"><span data-stu-id="21126-119">**ExclusiveLock**</span></span>](csharelocknh--exclusivelock.md)
</dt> </dl>

 

 
