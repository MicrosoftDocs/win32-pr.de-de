---
description: Ändert eine freigegebene Sperre in eine partielle Sperre.
ms.assetid: 82122671-b0bd-47ad-9a25-ee8ebd3779be
title: 'Csharelocknh:: sharedtopartial-Methode'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CShareLockNH.SharedToPartial
api_type:
- COM
api_location:
- Rwnh.dll
ms.openlocfilehash: a997c5a437063a4c55b74d837dc77fd506688158
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/22/2021
ms.locfileid: "106368495"
---
# <a name="csharelocknhsharedtopartial-method"></a><span data-ttu-id="cb68b-103">Csharelocknh:: sharedtopartial-Methode</span><span class="sxs-lookup"><span data-stu-id="cb68b-103">CShareLockNH::SharedToPartial method</span></span>

<span data-ttu-id="cb68b-104">Ändert eine freigegebene Sperre in eine partielle Sperre.</span><span class="sxs-lookup"><span data-stu-id="cb68b-104">Changes a shared lock to a partial lock.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb68b-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cb68b-105">Syntax</span></span>


```C++
BOOL SharedToPartial();
```



## <a name="parameters"></a><span data-ttu-id="cb68b-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="cb68b-106">Parameters</span></span>

<span data-ttu-id="cb68b-107">Diese Methode hat keine Parameter.</span><span class="sxs-lookup"><span data-stu-id="cb68b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="cb68b-108">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="cb68b-108">Return value</span></span>

<span data-ttu-id="cb68b-109">Gibt **true** zurück, wenn die teilsperre abgerufen wird. Andernfalls wird " **false** " zurückgegeben, und die Sperre bleibt im freigegebenen Modus.</span><span class="sxs-lookup"><span data-stu-id="cb68b-109">Returns **TRUE** if the partial lock is obtained; otherwise, it returns **FALSE** and the lock remains in shared mode.</span></span>

## <a name="remarks"></a><span data-ttu-id="cb68b-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb68b-110">Remarks</span></span>

<span data-ttu-id="cb68b-111">Dieser Funktion ist keine Import Bibliothek oder Header Datei zugeordnet. Sie müssen ihn mithilfe der [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) -Funktion und der [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) -Funktion aufrufen.</span><span class="sxs-lookup"><span data-stu-id="cb68b-111">This function has no associated import library or header file; you must call it using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions.</span></span>

## <a name="requirements"></a><span data-ttu-id="cb68b-112">Anforderungen</span><span class="sxs-lookup"><span data-stu-id="cb68b-112">Requirements</span></span>



| <span data-ttu-id="cb68b-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="cb68b-113">Requirement</span></span> | <span data-ttu-id="cb68b-114">Wert</span><span class="sxs-lookup"><span data-stu-id="cb68b-114">Value</span></span> |
|----------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cb68b-115">DLL</span><span class="sxs-lookup"><span data-stu-id="cb68b-115">DLL</span></span><br/> | <dl> <span data-ttu-id="cb68b-116"><dt>Rwnh.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cb68b-116"><dt>Rwnh.dll</dt></span></span> </dl> |



 

 
