---
description: Verhindert, dass mehr als ein Thread eine Sperre erhält.
ms.assetid: 9cdcc6d5-b2f1-4c88-b859-1c15a80e70a9
title: Csharelocknh::P artizuweisung-Methode
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.PartialLock
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: 0b7b7d55c9fd8d979aa14f12939df922e7a89099
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106366039"
---
# <a name="csharelocknhpartiallock-method"></a><span data-ttu-id="ca70b-103">Csharelocknh::P artizuweisung-Methode</span><span class="sxs-lookup"><span data-stu-id="ca70b-103">CShareLockNH::PartialLock method</span></span>

<span data-ttu-id="ca70b-104">Verhindert, dass mehr als ein Thread eine Sperre erhält.</span><span class="sxs-lookup"><span data-stu-id="ca70b-104">Prevents more than one thread from completing acquiring a lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca70b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="ca70b-105">Syntax</span></span>


```C++
void PartialLock();
```



## <a name="parameters"></a><span data-ttu-id="ca70b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca70b-106">Parameters</span></span>

<span data-ttu-id="ca70b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="ca70b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ca70b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="ca70b-108">Return value</span></span>

<span data-ttu-id="ca70b-109">Diese Methode gibt keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="ca70b-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca70b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca70b-110">Remarks</span></span>

<span data-ttu-id="ca70b-111">Obwohl **partitenzuweisung** wirksam ist, können andere Threads, die [**sharelock**](csharelocknh--sharelock.md) aufrufen, die Sperre eingeben.</span><span class="sxs-lookup"><span data-stu-id="ca70b-111">While **PartialLock** is in effect, other threads calling [**ShareLock**](csharelocknh--sharelock.md) can enter the lock.</span></span>

<span data-ttu-id="ca70b-112">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="ca70b-112">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca70b-113">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="ca70b-113">Requirements</span></span>



| <span data-ttu-id="ca70b-114">Anforderung</span><span class="sxs-lookup"><span data-stu-id="ca70b-114">Requirement</span></span> | <span data-ttu-id="ca70b-115">Wert</span><span class="sxs-lookup"><span data-stu-id="ca70b-115">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="ca70b-116">DLL</span><span class="sxs-lookup"><span data-stu-id="ca70b-116">DLL</span></span><br/> | <dl> <span data-ttu-id="ca70b-117"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ca70b-117"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
